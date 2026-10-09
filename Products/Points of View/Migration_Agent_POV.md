# Migration Agent POV

**Source:** [[Blueprint_Migration_Agent_Point_of_View.pdf]] (2 pages). This file is the text companion; the PDF is the source of truth. If the PDF changes, update this file. The editable HTML source is `Products/Research/Migration_Agent_POV_v2.html` (needs `Blueprint_logo.png` beside it). A one-page earlier version is `Products/Research/Migration_Agent_POV.pdf`.
**Topic:** The Migration Agent: a conversational agent built into Blueprint's Correlator
**Audience:** Internal (September 2026). Used to align staff on how to describe the feature externally. The Correlator and Migration Agent are in development.
**Status:** Revised September 24, 2026 with Tony Higgins's review comments (all applied). On September 25, at Tony's request, the document-type label was removed from the masthead entirely (no "Point of View" or "Explainer"); it now shows only the "MIGRATION AGENT" pill. File and folder names still say POV.

---

## Headline

**Migration gets you most of the way. The agent helps you finish.**

Blueprint's deterministic engine gets bots most of the way to Power Automate Desktop (PAD). What remains is manual finishing work. It's slower than it needs to be because the context behind the code is lost in translation, not because the work is hard. The Migration Agent, built into Blueprint's Correlator, puts that context back: a conversational agent that works from what the bot used to do, what it became, and why.

## Key messages at a glance

1. Finishing is the manual work of migrations.
2. What's missing is context: what the bot used to do.
3. Today developers need both tools for reference.
4. General-purpose AI doesn't know your bot or how it was converted.
5. Blueprint did the translation, so it can explain it.
6. Deterministic engine first. Grounded AI for the rest.

## 1. The last stretch of every migration

Every migration ends with a finishing phase: the manual work of resolving Blueprint TODOs and compiler errors before a bot is ready for production. The team migrating, usually a systems integrator (SI) and sometimes the customer's own developers, owns that work. The Migration Agent exists to reduce it.

**Today, finishing means working in two tools at once:** the source bot open in the legacy RPA tool and the PAD result in the PAD Designer, flipping back and forth to work out what came from where. Sometimes even this isn't possible, when there's no access to the source RPA tool.

**Access can also run out.** When a migration is prompted by source licenses nearing renewal, the source platform may not stay available for the whole project.

**General-purpose AI assistants struggle here.** The language behind PAD, Robin, has had no official reference since 2021, so they guess at syntax. And they don't know the bot they're looking at: what it used to do, how it was converted, whether it runs unattended, or which variables it uses. Their answers are generic, vary from one attempt to the next, and can quietly break how the bot runs.

**Comparison (diagram):**

| Today: two tools, matched by hand | With the Migration Agent: one view, with the context |
|---|---|
| Source platform ↔ PAD Designer; the developer flips back and forth | Source step (parsed by Blueprint), correlated to its PAD result; the Migration Agent can answer questions about either side |
| Work out what came from where, step by step | Source and PAD side by side, already linked |
| Some SIs have no source-platform access | No second tool, and no source-platform access, required |
| Access can end as source licenses near renewal | |

## 2. What the Migration Agent does

A conversational agent built into Blueprint's Correlator. With the source bot and PAD result side by side, a developer can:

1. **Explain (the code):** Ask what any piece of code does and why it was migrated the way it was.
2. **Resolve (Blueprint TODOs):** Get recommendations that fit the bot's constraints, such as how it runs.
3. **Fix (compiler errors):** Work through errors in the migrated flow with the source and the PAD result both in view.
4. **Write (new PAD actions):** Write new actions when a step needs to be built, grounded in what PAD actually supports.

**A real conversation:** no length limit, and asks for missing information instead of guessing.

## 3. Based on Blueprint Technology and Knowledge

**What the agent draws on (diagram):** four inputs feed the Migration Agent (conversational, grounded, inside the Correlator), which serves the developer finishing the migration. All of it sits on Blueprint's deterministic migration engine.

- **Source bot:** parsed and sanitized by Blueprint during migration
- **Correlation link:** what became what; semi-live once Microsoft adds anchor comments
- **Migration reasoning:** why a mapping was made and why a TODO was left
- **PAD action reference:** machine-derived from PAD's actions and variants

The four points:

- **Blueprint did the translation.** Blueprint holds the source bot, the PAD result, and the link between them. When Microsoft adds anchor comments, Blueprint will have a semi-live link: users can see what became what, and what Blueprint generated versus what they added.
- **Blueprint knows why.** Blueprint can draw on its own internal documentation, sanitized, to explain the reasoning behind its migration decisions: why a mapping was made, and why a TODO was left. Other tools can't accurately explain a migration decision, because no other tool made it.
- **Grounded, not guessed.** The agent draws on a complete, machine-derived reference of PAD's actions and variants. Its answers are grounded in what PAD actually supports.
- **Built on a deterministic foundation.** General-purpose AI tends to produce poor migrations. Blueprint uses AI only where the deterministic engine stops, and ties it to what that engine produced.

## What it isn't

- Not AI migration. The deterministic engine still does the migration.
- Not a replacement for human review.
- It's designed not to invent UI selectors.

## Tagline

**Blueprint's engine migrates your bots. The agent helps you finish them.**

*The Correlator and Migration Agent are in development and plans may change. Anchor comments depend on Microsoft's timelines.*

## Wording decisions (for future edits)

Tony Higgins (CPO/CTO) reviewed this POV on September 24, 2026; his calls are final. Keep them unless he or Sean says otherwise.

**From Tony's review:**
- Refer to the company as **"Blueprint," never "we"/"our"**, throughout.
- Don't say migrations **"stall,"** and don't describe finishing as unpredictable or as a place where timelines slip or margin erodes. Frame it as manual work that exists and that the agent reduces.
- "what the bot used to **do**," not "used to be."
- "what **came from where**," not "what became what" (in the problem framing; the diagram and correlation-link labels still say "what became what").
- Mention **"how it was converted"** as something general-purpose AI doesn't know.
- "Their answers **are** generic" (not "tend to be"); "not because the work is hard" (no "mainly").
- Don't mention competitors' migration products. The "flamed out" sentence was removed.
- Don't call out that source platforms make code hard to get at (the A360 Control Room / Blue Prism sentence was removed).
- Section 3 title: **"Based on Blueprint Technology and Knowledge."**
- "**Blueprint's** Correlator," not "the Correlator," in running text.

**Sean's earlier softening, still in place:**
- "no *official* reference since 2021" (a community knowledge base does exist publicly)
- "answers are *grounded in*" what PAD supports, not "limited to"
- "PAD's actions and variants," not "every"
- "*Other tools can't accurately* explain," not "no other tool can explain"
- General-purpose AI "*tends to* produce poor migrations"
- "*designed not to* invent UI selectors" (the "real conversation" line was later changed by Sean, on September 25, to the plainer "no length limit, and asks for missing information")
- The license-renewal point is framed as an occasional risk, not a common pattern
- No proof points or performance claims (including the PAD Copilot comparison) until there's a formal eval
