# ALC — Current Capabilities

> **Update 2026-10-09:** ALC is now the Maintain and Monitor use cases of the Blueprint platform. The per-main licensing (under revision as of March 2026) is replaced by the FY2027 subscription with unlimited automations (`Company_Overview.md`).

*Last updated: March 2026. Source: Sean Ellner (direct walkthrough).*

---

## Overview

ALC (Automation Lifecycle Control) can operate standalone or in tandem with Migrator. Its purpose is to give users full control over their automation lifecycle — from idea submission through development, testing, monitoring, and documentation. While Migrator is focused on the act of migration, ALC is the ongoing management layer for an automation estate.

---

## Environment Connections

ALC supports direct API connections to PAD and A360 environments. UiPath and Blue Prism are file-based only — no direct environment connection is available for those platforms. Only one environment is supported at a time per platform.

| Platform | Connection Method |
|---|---|
| Power Automate Desktop | Microsoft 365 authentication; user selects a single environment |
| Automation Anywhere A360 | Instance URL + username + password or API key; one environment at a time |
| UiPath | File-based import only |
| Blue Prism | File-based import only |

For PAD and A360, file-based import remains available as an alternative to the direct connection.

---

## Licensing

ALC is currently licensed **per main**, identical to how Migrator export licenses are counted. (Note: licensing model is actively being revised as of March 2026.)

---

## Features

### Ideas *(PAD only)*
An open backlog where users can submit automation ideas. Users manage the backlog themselves. Once development begins on an idea, users can link a specific process to it — provided that process has also been imported into ALC — giving the idea a traceable connection to its resulting automation throughout the development lifecycle.

### Apps
Full details on all applications accessed by automations in the estate. Significantly more detailed than the Application Dashboard available in Migrator.

### Best Practices
Users define a set of rules that represent their development standards. ALC checks existing processes against those rules and surfaces any violations, allowing teams to enforce consistent coding and design practices across their estate.

### Opportunities
Surfaces opportunities for improvement within the existing estate, including candidates for process reuse, consolidation, and transformation from RPA automations to API calls.

### Reviews
A collaboration area for teams to comment on and approve RPA processes, with a UI modeled loosely on GitHub's review experience. This is not a pull request system — there are no branches, merges, or code changes. It is purely a structured space for review commentary and approval sign-off.

### Tests
Allows users to configure test cases that validate what an automation is actually doing, not just whether it ran without errors. A process that completes successfully may still produce incorrect outcomes — Tests addresses this gap.

- Test cases can be **user-generated** or **AI-generated**
- Tests can be run **manually** (user documents the outcome themselves) or **fully automated**
- Fully automated testing is **PAD-only**: ALC connects a cloud flow on a schedule in the user's configured PAD environment and captures all relevant statistics automatically

### Test Runs
Displays the results of test cases configured in the Tests feature. Serves as the historical record of test execution and outcomes.

### Flow Activity *(PAD only)*
Live telemetry of PAD RPA processes. Provides more detailed statistics than what is available natively within Power Automate Desktop.

### Diagrams
Renders a call tree diagram of a process and its sub-processes, showing what calls what. Particularly useful for large, complex processes where understanding the execution structure is non-trivial.

### Find and Replace *(PAD only)*
Enables bulk replacements directly in the underlying Robinscript of PAD flows. Allows teams to make estate-wide changes without opening each flow individually in PAD.

### Changes *(PAD only)*
Version history for Power Automate Desktop flows. ALC can either integrate with Microsoft's native PAD versioning or use its own versioning system. Both options surface additional detail that Microsoft does not natively expose — specifically, **deltas** showing exactly what changed between each version.

### Logs *(PAD only)*
Surfaces all logs from a PAD flow across all of its runs in a single, consolidated view. Addresses a known usability gap in PAD, where locating run logs natively is unintuitive and fragmented.

### Auto Document Generation
Generates a document or specification for a process using all data ALC has collected about it, combined with generative AI to produce a high-level description of what the bot does. Users can generate documentation on demand, ensuring they always have an up-to-date source of truth for any automation in their estate.
