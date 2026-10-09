# UST / Schroders

## Key Contacts
- **Remya** (UST) — Primary migration lead
- **Jerin** (UST) — Optional participant, not present at retro

## Engagement Overview
- **SI:** UST
- **End Client:** Schroders
- **Migration Type:** Blue Prism → Power Automate Desktop (PAD)
- **Scale:** 350+ processes initially scoped; reduced during engagement; ~90–95% complete as of March 2026
- **Duration**: April 2025-Aug 2025
- **Blueprint Versions used**: 8.2, 8.3, 8.4
- **Addendum:** 15 additional bots added out of scope — migration beginning next month using existing licenses
- **Blueprint Contacts:** Stef (CS), Jeff (technical support/Solution Files)

---

## Updates

### 2026-03-04 | Feedback Session — Migration Retrospective

**Source:** 7:30 AM MS Teams call with Remya (UST). Sean Ellner (Blueprint, Product) conducted the session.

**Status at time of call:** ~90–95% of original scope completed. 15 out-of-scope bots queued for next month.

---

### Critical Feedback

- **Early migration quality was poor.** Claimed "Everything was a TODO" early on. Said there were too many .NET scripts. Quality improved significantly by the end of the engagement.
- **Unnecessary steps inserted into migrated output.** Extra steps added overhead to post-migration cleanup throughout the project.
- **Performance degradation post-migration.** Processes that ran in ~30 min in Blue Prism now take 1–1.5 hrs in PAD. Partially inherent to PAD's architecture, but Blueprint-migrated steps (redundant open/close operations, filtering, SQL queries) contributed. At 500–600 items with 3–5 sec delays per step, the delta is material to the business.
- **License visibility gap (resolved).** Team assumed licenses were consumed on export, not import, and ran short mid-project. Addressed — license balance popup now shown at import.
- **Excel launch instability.** Intermittent Excel launch failures required adding manual delays as a workaround. Possibly machine-related but still an active pain point.

---

### Positive Feedback

- **Strong quality trajectory.** Early Solution Files were rough; later Solution Files went well. Customer: *"From the beginning if we see, the last Solution Files were pretty good."*
- **Team became advocates.** By the end, the team was proactively requesting the tool for new work. *"It became a friend for us"* — credited with helping deliver the project on time despite a tight deadline.
- **High value on complex processes.** For large processes with many steps and subflows, the tool enabled step-by-step Blue Prism/PAD comparison that would have been very difficult manually. *"For the future process, we could understand that these fixes can be applied to other processes. That easiness we got from this package itself."*
- **Excellent support.** Jeff was specifically called out for personally preparing Solution Files when issues arose. Team was kept informed of new releases throughout. *"We got very good support from your team... whenever we had some issues we got those Solution Files ready by Jeff himself."*
- **Issue tracker was effective.** All items closed — resolved by Blueprint, fixed on the customer side, or deemed out of scope.

---

### Additional Context

- Customer had no reliable documentation for source processes. Documents existed but were outdated — schedules, paths, and functionality had changed post-production without being recorded anywhere.
- A team that originally managed the source systems (Indonesian team) was transitioned out mid-engagement, leaving a support gap that caused delays on ~5–10% of processes still pending resolution.
- Some processes had embedded Python scripts with undocumented encryption logic; SMEs could not explain the functionality, leaving those bots unresolvable within the project scope.
- Customer is currently monitoring PAD execution using logs within Power Platform (cloud flow → desktop flow pattern with try/catch on every step). No third-party monitoring tooling in use.
