# ALC Features for Buyers

## Strategic Context

ALC has near-zero churn but almost no standalone sales — virtually every purchase has been tied to a Migrator engagement. The core problem: ALC is comprehensive but no single feature creates enough urgency to justify a $45–55K standalone purchase. Customers recognize value but can't build internal buy-in for it independently (the "Ferrari problem"). A compounding issue is that the people who feel the pain — CoE leads, Heads of Automation — often lack budget authority. This research explores features that could be sold directly to buyers with purchasing power (IT audit, risk, finance, operations leadership), independent of a migration cycle.

**Current Status:** Research complete. Next step is presenting ranked opportunities to internal stakeholders, with mock-ups and a recommended prioritization.

---

## ALC Feature Opportunities — Research & Analysis (March 2026)

Sean commissioned three research reports on RPA pain points to identify new ALC feature investments. Key constraint: prioritize PAD-specific problems given Microsoft's centrality to Blueprint's revenue.

### Research Topics Covered

- RPA compliance (SOX, GDPR, HIPAA, PCI-DSS, audit trails, controls frameworks)
- RPA outcome monitoring (transaction-level success/exception/failure taxonomy, logging gaps)
- Shadow automation and bot sprawl (ungoverned citizen-dev bots, credential risks, CoE governance)

### Recommended Opportunities (Ranked)

**1. Compliance Drift Detection & Audit Readiness** _(Highest priority)_ PAD estates are compliance-blind relative to legacy RPA platforms. Enterprises in regulated industries (financial services, healthcare) face auditor/regulator pressure to demonstrate control over their automation estate. ALC's existing compliance scanning is the foundation — reframe it as audit readiness and drift detection to reach CISO and Internal Audit as budget holders, not just CoE leads. This is the strongest candidate for standalone purchase urgency. Builds on existing capability with no new technical infrastructure required.

Original research ~2 years ago showed low interest among PAD customers, but likely surveyed the wrong people at the wrong moment (migration-context buyers, not estate managers). Regulated industries with mature PAD estates (financial services, healthcare) are the right target — specifically IT audit/risk functions and CoE leads who've faced auditor questions about automation. Recommend using early adopter program interviews (regulated industry, mature estates) as the probe rather than investing in the feature first.

**2. RPA Outcome Monitoring / ROI Dashboard** – Feature concept under active design. Core idea: use queue completion rate (not bot success rate) as the primary proxy for business value, combined with customer-input baseline data to surface dollar/capacity metrics that bridge "operational data" and "executive ROI story."

GTM framing: do NOT lead with cost savings (weak — most orgs feel they've underdelivered on savings). Lead with **capacity freed / organizational growth enablement**. Framing: "See what your team is capable of now." FTE equivalents freed and throughput are headline metrics; cost savings are supporting evidence. Avoids the layoff narrative and survives scrutiny from sophisticated buyers.

*Status: Data model complete (`ALC_ROI_Data_Model.html`). Lovable prototype in progress. March 2026.*

- 8 metric cards: Staff Hours Freed, Team Capacity Expanded, Work Items Completed, Active Automations, Capacity Reinvested, ROI Ratio, Stale Flows, Capacity Recovered
- Metrics use completed runs only — referred and failed items excluded since they don't save time or money
- Configure Baseline requires 3 fields per process (FTE count, annual pay, time per iteration) — all AI-estimated via PAD signals, user confirms before metrics compute
- Manual entry uses source type ("Exact Record" vs "Estimate") rather than confidence scores — confidence indicators are AI-only
- "ROI & Health" nav item left of Ideas; Configure Baseline accessible from both the ROI dashboard and the Manage dropdown

**3. Estate Visibility (Previously called Shadow Automation Discovery)** _(Validate before committing)_ PAD's low barrier (any M365 user can build flows) makes shadow automation more acute than legacy platforms. Market need is well-documented. Feasibility depends on whether PAD/Dataverse telemetry surfaces enough signal to discover unregistered flows without invasive agent deployment. Requires technical validation with Tony before roadmapping.

**4. Business Outcome Monitoring** _(Retention deepener, not acquisition hook)_ Surfaces the gap between "bot ran" and "bot did the right thing" — PAD flows, especially migration-generated ones, are often uninstrumented. ALC can identify flows with zero logging as a unique, structurally-informed insight. Valuable for retention and upsell but unlikely to drive standalone purchases from buyers without mature, high-volume estates.

### Strategic Framing

All three opportunities support repositioning ALC as the **PAD estate control layer** — language grounded in how ISACA, Baker Tilly, and ZenGRC describe formal RPA controls frameworks. Sharper than the current "migration companion" framing and more credible to executive buyers.

Need to find what problem is urgent enough to justify a standalone ALC purchase outside a migration cycle.
