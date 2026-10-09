# Migrator — Current Capabilities

> **Update 2026-10-09:** The "60–90% reduction in migration effort" figure under Migration Philosophy is superseded for any external use by the approved POV figures: 70–75% less effort and 95–99% of actions converted (`Automated_Migration_POV.md`). Everything else here (no out-of-the-box promise, TODO/INFO/SRC comments) stands. Migrator is now the Modernize use case; migration capacity is sold as credits alongside the platform subscription. Confirm with Sean how credits map to the per-main license counting below.

*Last updated: March 2026. Source: Sean Ellner (direct walkthrough).*

---

## Core Architecture

Migrator is a cloud-hosted SaaS platform (on-prem available for sufficiently large deals, but strongly discouraged — Blueprint prefers cloud). Users import source RPA processes into Migrator, where they are converted into Blueprint's proprietary **COM (Common Object Model)** language. COM acts as a platform-agnostic intermediate representation, enabling a hub-and-spoke model for outbound migration to multiple targets.

**Currently, the only supported migration target is Power Automate Desktop (PAD).** This is a deliberate business decision — Microsoft is a major investor and customer. The architecture supports future targets, but no others are active today.

---

## Supported Source Platforms

Import is strictly **file-based** — Migrator does not connect directly to source environments via API or agent. Users must export from their source tool first.

| Platform | Required Import File |
|---|---|
| Blue Prism | `.bprelease` file |
| UiPath | Package folder with `project.json` |
| Automation Anywhere A360 | Exported `.zip` with `manifest.json` |

---

## Migration Philosophy

Blueprint **does not promise that migrated bots will work out of the box.** The documented promise is a **60–90% reduction in migration effort**, scaled to process complexity. The remaining work is left for the user to complete, clearly marked with Blueprint-generated comments in the migrated code:

| Prefix | Meaning |
|---|---|
| `TODO:` | Something the user must do to make the bot production-ready |
| `INFO:` | Helpful context, especially for patterns that change significantly between RPA platforms |
| `SRC:` | Original source code context, included to reduce back-and-forth when intent is unclear |

Compiler errors in the generated PAD code are generally self-explanatory and do not receive comments unless the fix is non-obvious.

Blueprint recommends users keep the **original source process and the migrated PAD process open side by side** while completing migration work. For undocumented processes, the source bot is often the only reliable record of intent.

---

## Dashboards

### Statistics Dashboard
High-level overview of the raw data comprising the user's automation estate — process counts, action volumes, and other aggregate metrics.

### Application Dashboard
High-level overview of all applications touched by RPA processes in the estate. Useful for understanding dependencies and scope.

### Estimator Dashboard
The most widely used feature outside of migration itself. The Estimator performs a **simulated export to PAD** — it generates the full PAD code (including all TODO/INFO/SRC comments and the effect of any enabled Rules) exactly as a real migration would produce, but does not create the actual flow or push anything to an environment.

**Purpose:** Effort estimation before committing to a migration.

**Key capabilities:**
- Output is **identical** to a real migration — no differences whatsoever, including Rules application
- TODOs are categorized by type
- In-product calculator lets users assign time estimates per TODO type; Blueprint provides defaults that users can modify
- Entire estimation can be **exported to Excel** as a detailed, line-item template for high-accuracy project scoping
- Services companies commonly use the Estimator (via Migrate Dashboard licenses) to bid on migration engagements before winning the work

---

## Rules

Rules allows users to identify improvement opportunities across their migration estate and encode fixes that apply automatically on future migrations.

**What Rules can identify:**
- Custom actions with no proper target mapping
- Sub-processes reused across multiple bots (candidates to become shared external desktop flows)
- Missing dependencies
- Work queues referenced in processes that need to be populated

**How Rules work:**
- Users create a rule: "whenever you see X, map it to Y" — same pattern applies to unresolved references and work queues
- For reuse candidates, the **Reuse** capability creates an external desktop flow for the shared component; all future migrations call that flow rather than inlining it as a subflow
- **Enabled rules apply automatically to all future migrations** — no manual trigger required
- Rules can be **scoped to folders** (since users can organize imported processes into folder hierarchies within Migrator)
- All rule configurations are manageable from the Rules page
- A **Rules wizard** surfaces on export, guiding users through any missed opportunities and confirming which rules will be applied to the migration

---

## Export

When a user is ready to perform a real migration (not just estimate), they have two export options:

1. **Direct to connected PAD environment** — Blueprint pushes the migrated flow directly to the user's linked PAD instance
2. **Solution file** — Blueprint generates a PAD solution file the user can import manually to any environment

---

## Licensing

Two distinct license types exist, both tracked at the **main** level and both accounting for duplicates.

### Migrate Dashboard Licenses
- Consumed **on import**
- Intended for analysis and estimation only — no export to PAD
- Commonly purchased by SI/services companies to bid on migration projects, independent of whether they win the engagement

### Migration Licenses
- Consumed **on export** to PAD

### Duplicate Handling
Neither license type charges for duplicate processes. Duplicates are tracked by the process's **original GUID** from the source platform — even if the process is modified after import, the same GUID prevents an additional license charge on reimport.

### What Counts as a "Main"

Licenses are counted per **main** (i.e., per call tree), not per action, object, or file. Blueprint chose this unit because customers found "migrating individual call trees" intuitive in a way that action counts or other metrics were not.

| Platform | Main Definition |
|---|---|
| Blue Prism | Programmatically defined; user cannot alter it |
| UiPath | Programmatically defined; user cannot alter it |
| Power Automate Desktop | Programmatically defined; user cannot alter it |
| A360 | No programmatic main — Blueprint defines it as **any root process that calls at least one other process** |
