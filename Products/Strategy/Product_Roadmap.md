# Product Roadmap — 6 (Migrator + ALC)

*Owner: Sean Ellner · Audience: Tony (CPO/CTO), Martin (CEO), product & dev team · Status: Draft for alignment · Last updated: 2026-06-09*

> This is a strategic communication tool, not a date contract. It states what we're building next quarter, why it matters, and how it ladders up to the business outcome. We expect to adjust as we learn.

---

## North Star for the Quarter

**Net revenue retention and expansion.** Every initiative below is justified by its contribution to retention or expansion — not by feature completeness.

This framing matters because of where we are: ALC has genuine PMF signal (zero churn in two years) but almost all sales have ridden in on a migration engagement, and customers recognize value without yet feeling standalone urgency ("the Ferrari problem"). The quarter is built to (a) harden the value we already deliver so renewals stay safe, and (b) test the next expansion vector.

---

## The Two Bets

We are deliberately running **one ship + one explore** this quarter. Two net-new product initiatives to GA in 13 weeks with ~11 engineers is not honest planning, so we commit one to a shippable milestone and run the other as a genuine pass/fail discovery.

### Bet 1 — The Correlator *(SHIP)*

**What it is:** A Blueprint product that maps every migrated Power Automate Desktop action back to its source-tool origin — UiPath, Blue Prism, or Automation Anywhere A360 — and the reverse. When a migrated bot has a TODO or "looks wrong" in PAD, the fix itself is usually quick; what eats the hours is hunting through the source tool to find where the action came from and understand what it was doing. The Correlator eliminates that hunt.

**Hypothesis:** We believe that giving migration developers and SIs a bidirectional map between PAD actions and their source-tool origin will cut post-migration triage time and deflect support tickets, because the source-origin hunt — not the fix — is what consumes the time today (a recent real case took 1–2 hours).

**Why it serves the north star:** This is the value story that keeps accounts renewing. The UST/Schroders retro flagged post-migration cleanup overhead and performance overhead as the main detractors; the Aubay engagement showed how much Product/CS time is burned when customers escalate before investigating the source. Both are source-origin discovery problems. Cutting that time protects the relationship and the renewal.

**Success metrics:**

- **Triage deflection (headline):** % of triage / source-origin items resolved *with the Correlator* rather than raised as a support ticket — measured from our own ticket volume.
- Product/CS hours spent on source-origin investigation: down materially.
- Median resolution time on triage items, where we can capture it.
- Adoption: % of active migration developers using the Correlator weekly.

**v1 scope:** Bidirectional PAD ↔ source action mapping across Blue Prism, UiPath, and AA360.
**Later (not this quarter):** the "why" layer (why X became Y), then an optional AI chat over the mapping.
**Effort:** Large. The correlation engine sits on top of the COM translation layer across three source platforms; that's the hard part.

### Bet 2 — AI Agent Tooling from the RPA Estate *(EXPLORE)*

**What it is:** A capability that discovers, recommends, harvests, and creates AI agent tooling from a customer's *existing* RPA estate — extending ALC's "Opportunities" feature from "RPA → API candidate" into "RPA → agent tool."

**Hypothesis:** We believe that surfacing and harvesting agent tooling from a customer's estate will unlock standalone expansion/NRR value, because the longitudinal estate data Blueprint already holds is the defensible foundation agents need — and it points ALC at the next thing customers will be under pressure to do with their automations.

**Why it's explore, not ship:** The scope is still loose, the desirability is unproven, and it's the bigger, more strategic bet. We treat it with the same discipline as the early-adopter program: a real pass/fail test, not a validation lap before a decision we've already made.

**Exit criteria (go/no-go by end of quarter):**

- A concrete definition of what an "agent tool" deliverable actually is.
- The estate signals that reliably flag good harvest candidates.
- A working prototype of the discovery + recommendation pass on real estate data.
- Desirability validated with 1–2 existing ALC customers.
- A go/no-go recommendation with a sized build plan for next quarter.

**Effort:** Medium (discovery / prototype, not GA).

**Strategic fit:** Consistent with the AI competitive-risk thesis — the right long-term posture is for Blueprint's estate data to be the foundation AI is built *on top of*, not replaced by. This bet is a first concrete move in that direction.

---

### Changes in Fiscal Year 2027
Moving forward we will be a single product company.  Our product is the Blueprint platform (perhaps the Blueprint automation management platform).  We are eliminating MAP, Migrate and ALC as customer-facing product names.  Our website will list only one product with three use cases: Maintain; Monitor; Modernize.  We are one platform for a customer's entire automation estate.

We maintain it, we monitor it and we modernize it.  We will list all three use cases with a short description of the capabilities of each on the Product drop-down menu.  Migrate will be listed under the Modernize use case.  We are no longer going to predominantly highlight migration as a separate use case.  We do not want to be the migration company any more (especially if Microsoft buys an unlimited migrate license from us in the next few weeks).

We are going to sell Blueprint for $5,000/month; $50,000/year; and $140,000/3-year commitment.  One caveat to the above is for large automation estates and global system integrators.  For those (which we won't define explicitly on the website) we will encourage them to contact us for pricing.

The website will also have a "Solutions" drop down menu.  Under solutions, I believe we should list - Power Automate migration; RPA estate assessment; Migration analysis & planning; and Agentic RPA.  These are solutions that we will monetize separately from a Blueprint subscription.  They will combine our technology with some templates/reports that are not currently in the product with our consulting expertise.

Our selling model is going to change from "We'll give you a free PoC so we can prove that Blueprint works" to "Start with Blueprint for $5,000.  No long-term commitment. If you don't see the value, you can cancel at any time.

They will become a customer on Day 1.  We will be onboarding customers rather than courting a prospect through an indefinite free evaluation.

|**Blueprint**|**Monthly**|**Annual**|**3-Years**|
|---|---|---|---|
|Complete Platform|$5,000/month|$50,000/year|$140,000|
|Users|Unlimited|Unlimited|Unlimited|
|Features|All|All|All|
|Support|Included|Included|Included|
|Commitment|Cancel anytime|Annual|36 months|
|Migration Credits|Not Included*|Not Included*|Not Included*|
|Automations|Unlimited**|Unlimited**|Unlimited**|
*Migration capacity can be purchased separately or may be available through your Microsoft engagement  
**Large automation estates and global systems integrators: contact us for enterprise pricing.

We will no longer be a company selling several specialized RPA products through enterprise solution sales.  We will be a company selling one automation platform through a simple subscription, with migration and consulting solutions surrounding it.  **This is a big shift for us.**

