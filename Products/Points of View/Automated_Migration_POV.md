# Automated Migration POV

**Source:** [[Blueprint_Automated_Migration_Point_of_View.pdf]] (2 pages). This file is the text companion; the PDF is the source of truth. If the PDF changes, update this file.
**Topic:** Automated migration: moving RPA to Microsoft Power Platform
**Audience:** External (customers, SIs, Microsoft)

---

## Headline

**Don't rewrite your RPA estate. Convert it.**

For organizations weighing a move to Microsoft Power Platform, what happens to existing automations is part of the decision, not an afterthought. Most businesses depend on their bots and can't leave them behind, so the time, cost and risk of moving them belong in the business case. Historically that meant a long, expensive manual rewrite. Blueprint's automated conversion changes the equation.

## Key messages at a glance

1. Migration belongs in the Power Platform business case.
2. Most businesses can't leave their bots behind.
3. 70–75% less effort than a manual rewrite.
4. 95–99% of actions convert; developers finish the rest.
5. Functional equivalence: no drift, edge cases preserved.
6. Migrate, then govern, on the same Blueprint platform.

## 1. The bigger picture

Organizations choose Power Platform for strategic reasons. Many are consolidating several point vendors into one comprehensive automation suite. They want a large, reputable vendor behind it, and they want to be positioned for the future with a company known for technical innovation. Power Platform's broad approach to automation, with many implementation options that work together, means you won't get stuck or hit a dead end. If you're going to ride on a platform, it should be the platform with a future.

The move often spans more than RPA, including Lotus Notes, Appian and Pega. Whatever the scope, the cost and risk of bringing existing automations along are weighed in the same business case, and the easier the migration, the stronger that case becomes. This POV focuses on migrating RPA from **UiPath**, **Blue Prism** and **Automation Anywhere Automation 360** to Power Automate Desktop (PAD).

## 2. The old way: a manual rewrite

Historically, migrating RPA to PAD meant a manual rewrite, usually by a systems integrator: long, expensive and risky. Many bots were built years ago and have passed through many owners, so the knowledge of what they do, and why, is often gone. A rewrite must rediscover every edge case the original bot learned to handle, and the longer it runs, the longer you pay for two platforms.

## 3. A fundamentally different approach: automated conversion

Blueprint converts each source automation into a **functionally equivalent** PAD flow that does exactly what the old one did, edge cases included. There's no functional drift, and results are far more predictable than new development.

**Headline figures**

| Figure | Meaning |
|---|---|
| 70–75% | less effort than a manual rewrite of the estate |
| 95–99% | of actions converted automatically |
| 200+ | companies' RPA estates behind these metrics |
| 21M+ | PAD actions produced by conversion |

**Relative migration effort (diagram):** a manual rewrite (SI, bot by bot) is 100% of effort. Blueprint automated conversion ("convert, then complete") is ~25–30%, split between planning/analysis/conversion/testing and developer completion of the remaining actions. That's 70–75% less effort, roughly 3× faster.

The remaining actions, along with any issues in the converted ones, are finished by a developer, and Blueprint guides that work. The savings figure (the **Blueprint Efficiency Metric**) is conservative: some underlying data is several years old, and the conversion engine keeps improving. Selector conversion, historically the hardest part of any migration, has improved dramatically in recent years. Blueprint now converts UI Automation (UIA) and Microsoft Active Accessibility (MSAA), variable-based, image, anchor and SAP selectors, and creates fallback selectors automatically. Some selectors still need a developer's attention, and Blueprint's selector report shows exactly which ones, so they can be included in estimates up front.

## 4. How it works: plan, migrate, govern

Sources: UiPath · Blue Prism · Automation 360 → Target: Power Automate Desktop

- **Plan (estate level):** Import the whole estate: size, complexity, applications, missing dependencies and cloud-flow potential. Triage each bot, then produce estimates, a plan and a target operating model.
- **Migrate:** done incrementally, one bot per developer, many in parallel.
  - **Analyze:** Re-import the latest version. Understand it fast with AI descriptions, process and structure diagrams, and dependencies. Set mapping rules and reuse.
  - **Convert:** Generate the PAD flow with your choices (local variables, subflows, libraries) and standards from your operating model applied at conversion.
  - **Complete:** TODO guidance in the code, bulk find and replace, a selector report, test generation and as-built specifications. Then test, approve and retire the old bot.
- **Govern (ongoing):** Keep the new PAD estate healthy: maintain with impact analysis, monitor business outcomes, and modernize, including flows as Copilot agent tools.

## 5. Move at the pace your business needs

- **Move fast:** Get off the legacy platform before license renewal and minimize time running two platforms. Migrate first, then improve or reimagine inside Power Platform.
- **Take your time:** Move gradually, reimagining some automations with cloud flows, Power Apps or agents while migrating the rest. Most estates end up as a mix.

## Tagline

**Bring your bots with you. Automatically.**

*Figures are averages across Blueprint conversion data; results for any estate depend on its size, complexity and quality.*
