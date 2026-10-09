# Blueprint Company Overview

*Updated 2026-10-09. The FY2027 single-platform pivot (source: `Products/Strategy/Product_Roadmap.md`) is confirmed final by Sean. Older documents may still use the retired product names (MAP, Migrate/Migrator, ALC/Blueprint Control) and the prior pricing; treat this file as authoritative.*

## Company
~25-person RPA migration company. The only company doing programmatic (tool-led) RPA migration — no external documentation exists, and the competition is services-led: SIs rebuilding bots manually, not another migration tool. Blueprint is deliberately stepping back from being "the migration company," partly in case Microsoft purchases an unlimited migrate license.

## Product
One product: the **Blueprint platform**, sold under a single subscription. MAP, Migrate, and ALC are retired as customer-facing names. The website lists one product with three use cases — **Maintain, Monitor, Modernize** — and migration sits under Modernize. The underlying capabilities are unchanged; only packaging and pricing changed. Blueprint is one automation platform for a customer's entire automation estate.

## Capabilities (internal names in parentheses; older docs still use them)
**Modernize (formerly Migrator):** Converts bots from UiPath/Blue Prism/A360 → Power Automate Desktop. Uses Common Object Model as translation layer. Approved external figures (`Products/Points of View/Automated_Migration_POV.md`): 70–75% less effort than a manual rewrite; 95–99% of actions converted automatically, with developers finishing the rest; 200+ estates and 21M+ PAD actions behind the metrics. Cloud-hosted SaaS; on-prem exists only for sufficiently large deals and is strongly discouraged. Full detail: `Migrator_Capabilities.md`.

**MAP:** Analyze RPA processes for the purpose of migration. Includes the Estimation dashboard, static code analysis, and Blueprint-generated Assessments.

**Maintain / Monitor (formerly ALC / Blueprint Control):** RPA lifecycle management and governance. Features include auto-documentation, structure/dependency mapping, application analysis, compliance scanning (Best Practices), version awareness/restore (Changes), reuse detection (Opportunities), flow activity and anomaly detection, testing, and collaborative reviews. Full detail: `ALC_Capabilities.md`.
- **Platform scope:** ALC connects directly to PAD and A360 environments (one environment per platform at a time) and imports UiPath and Blue Prism files. Several features are PAD-only (Ideas, Flow Activity, Find and Replace, Changes, Logs, automated Tests). It is not PAD-only overall.
- Product is ~2 years old. Zero churn to date — all customers who purchased have renewed. Caveat - very few customers.
- Almost all ALC sales to date have occurred during or alongside a Migrator engagement. Very few standalone sales exist yet.
- Most heavily used features: auto-documentation, structure diagrams, application analysis (migration-adjacent utility).
- Least used features: opportunity analysis, testing, collaborative reviews (higher-value but require more organizational maturity).
- Common customer reaction: recognize significant value ("Ferrari") but struggle to justify purchase internally without migration context as the trigger.
- Strategic question still open: can the Maintain/Monitor value create standalone urgency outside of a migration sales cycle?

**In development:** Correlator and Migration Agent (maps migrated PAD actions to their source origin; conversational agent built into it), AI Agent Tooling from the RPA estate (explore), Business Outcome Monitoring. See `Product_Roadmap.md`.

## Business Model
- **Customers:** System Integrators (Avanade, Hitachi, TCS) and Fortune 2000 enterprises
- **Microsoft:** Major investor, purchases licenses as migration incentives. Offered to subsidize year one for joint customers (offer made when the product was still called ALC). Migration capacity may be available through a Microsoft engagement.
- **Positioning:** "One automation platform for the entire estate." Replaces the "digital moving company" / migration-first framing.
- **Sales pitch:** "Start with Blueprint for $5,000. No long-term commitment. Cancel anytime." Customers become customers on Day 1, replacing the old indefinite free-PoC courtship model.
- **Pricing (FY2027):** Complete Platform — $5,000/month, $50,000/year, or $140,000/3-year commitment. Unlimited users, all features, unlimited automations, support included. Migration capacity is sold separately as credits. Large automation estates and global SIs: custom enterprise pricing (contact us, not published on the website).
  - *Superseded, still referenced in older docs and decks:* Migration ~$100K/deal; ALC $45-55K/year (Foundation, up to 400 flows), $80-95K/year (Enterprise, 400+ flows); per-main ALC licensing.
- **Solutions (sold separately from the subscription):** Power Automate migration; RPA estate assessment; Migration analysis & planning; Agentic RPA. These combine platform tech with templates/reports not in the core product plus consulting expertise.
- **Revenue model:** The platform subscription is the primary recurring revenue source; migration and consulting are sold as add-on solutions around it.

## Team
- Martin (CEO) — still handles sales himself, plus executive engagements and partnerships
- Tony Higgins (CPO/CTO) — runs product with Sean
- Dev team of 11
- Stef (Head of Customer Success), Matt (Head of Presales), Francis (Head of Marketing)
- A marketing hire has been made. There is no separate sales team. Leads historically came through Microsoft. Hiring is closed for now.
