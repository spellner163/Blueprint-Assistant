# Static Correlator

## Strategic Context

The Static Correlator maps each migrated PAD action back to its origin in the source RPA tool (UiPath, Blue Prism, AA360) — and vice versa. It's generated during export as a reference/navigation aid, not a replacement for the source tool. Originally blocked on Microsoft adding unique block identifiers; Esteban's static, one-time-generated approach unblocks it by correlating on what we already know at export time.

**Current Status:** Design discussed (Sean, Dmitry, Esteban — June 2026). Esteban revising the PRD, then planning tickets with Dmitry.

---

## The Problem

When a migrated bot has a to-do or looks wrong in PAD, the fix itself is usually quick. The expensive part is *locating where the action came from in the source tool* and reconstructing what it was doing there. Sean cited a real case (an `if` branch landing outside its loop) that took 1–2 hours to diagnose — almost entirely spent screenshotting source and target side-by-side to find the mismatch.

This cost is invisible and recurring. Migration delivery teams are a black box: an SI sends one or two people to import/export, then hands off to an unknown number of people who finish the migration. We don't know how many bots they touch or how long each takes. The Correlator attacks the single biggest time sink in that post-migration cleanup.

## Why This Is a Good Strategic Bet

It targets the highest-leverage moment in a migration: the manual cleanup that determines whether a project feels fast or painful. Cutting "where did this come from?" from hours to a click directly improves delivery velocity and customer experience.

It's also low-risk to start: export already produces the full generated flow (the same data Estimator analyzes locally), so the correlation data is accurate to what actually ships — no new pipeline required.

And if built in-product, it creates visibility we don't otherwise get. Putting it behind product accounts would let us see delivery team size, bots-per-person, and time-per-bot — data we can't currently obtain even by asking. That intelligence compounds across every future migration.

## V1 vs. Later

**V1 (deliver first)**

- Click a PAD action → see roughly where it maps in the source, plus immediate before/after neighbor actions. Linear "before / after" model — no full graph rendering.
- UiPath-style collapsible **Outline view** (nested nodes, one hierarchy level at a time).
- Focus on **UiPath first** — highest customer value, not the easiest source. (AA360 is easiest but near-pointless since it's already linear.)
- Worst-case fallback is acceptable: if a case is too complex, show a single action ID.
- Simple temp-variable correlation: click a temp variable (e.g. `_TP1`) → "migrated as part of this action, along with these others."
- **Built in-product (Angular).** Long-term target is in-product, so start there rather than build a throwaway static-HTML download.
- Assume the user still has access to the source tool. Generate on export; no long-term storage.

**Later (V2+)**

- Full variable search ("TP variable search" — one variable → every source action it touches).
- "Why did this become that?" guidance, and eventually an AI chat layer.
- Downloadable/exportable version — solve only if needed.
- Selectors — deferred unless feedback demands it.
- Extreme-scale handling (200+ subflows, 30k+ actions, 200+ variables, deeply nested Blue Prism) — aggressive collapsing or "too many — refer to source."

## Open Questions

Nonlinear/cyclical flows aren't proven solvable — Blue Prism especially (hook/try-catch blocks, forward GoTos, branches whose exit point can't be shown visually). Flow-chart presentation specifically is unconfirmed. Re-establishing the source link is reliable for AA360 (line numbers) but largely broken for UiPath/Blue Prism today — recoverable but unscoped. Temp variables generated in C# mapping code aren't tracked anywhere and would need to be recovered by analyzing the generated Robin.
