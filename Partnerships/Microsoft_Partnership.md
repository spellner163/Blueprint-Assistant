# Microsoft Partnership

## Collaboration Patterns

**Frequency:** Quarterly engineering touchpoints, sometimes more frequent

**Roadmap Planning:** Less agile than expected (6-12 month commitments)

**Market Intelligence:** Microsoft proactively seeks Blueprint's field observations

**Customer Reality:** Microsoft's new PAD customers are migration customers, not net-new

## API Development & Integration

### Seamless Export
- Blueprint migrations appear directly in users' Power Automate environments
- Joint API development eliminated manual file upload steps

### SDK Lag Pattern
- Microsoft SDK often trails UI feature releases
- **Workaround:** Direct Robin script mapping when SDK unavailable

## Technical Influence Examples

### Variable Scoping
- **Problem:** PAD only supported global variables, source platforms had scoped variables
- **Blueprint Impact:** Convinced Microsoft to add native support through business case
- **Outcome:** Added to Microsoft roadmap, released in Jan 2026. Customer adoption pending.

### GoTo Actions
- **Problem:** PAD enforced linear workflows, breaking non-linear migrations
- **Blueprint Impact:** Influenced addition of flexible goto statements
- **Outcome:** Go To now exists in PAD, but only works within the same subflow, and Microsoft's documentation does not say so
- **Business Case:** Without flexibility, customers rebuild from scratch vs. migrate

### PowerFX Integration
- Ongoing collaboration on expression language support
- Blueprint provides field feedback on integration challenges

## Open Items and Dependencies (as of Oct 2026)

- **Anchor comments:** The Correlator and Migration Agent get a semi-live source-to-PAD link only once Microsoft adds anchor comments. Timing is Microsoft's (`Research/Correlator.md`, `Migration_Agent_POV.md`).
- **Unlimited migrate license:** The FY2027 pivot document says Microsoft may buy an unlimited migrate license from Blueprint "in the next few weeks." This is pending and unconfirmed. It is one reason Blueprint is stepping back from being "the migration company."
- **Year-one subsidy:** Microsoft offered to subsidize year one for joint customers. Migration capacity may also be available through a Microsoft engagement (`Company_Overview.md`).
- **Agents calling subflows:** Microsoft plans to let Copilot agents call subflows directly, which would remove the need for Blueprint to extract them (`Agents_and_RPA_POV.md`).
- **Documentation gap:** Robin, PAD's underlying language, has had no official reference since 2021.
- **Market position:** Microsoft is a Leader in the 2026 Gartner RPA Magic Quadrant, but large organizations mostly use it as a secondary RPA tool (`2026-RPA-Magic-Quadrant-Digest.md`).
- **Native governance risk:** Microsoft building PAD governance itself is the main competitive threat (`AI_Competitive_Risk.md`).

## Partnership Value Exchange

**Blueprint provides Microsoft:**
- Real-world migration use cases and blockers
- Enterprise customer feedback on PAD capabilities
- Market insights on RPA → PAD transition patterns

**Microsoft provides Blueprint:**
- Roadmap influence on migration-critical features
- Early access to API updates and beta features
- Co-selling opportunities and migration incentives

## Managing Microsoft Dependency

**Challenge:** Roadmap locks 6-12 months out, difficult for Blueprint to respond quickly to customer blockers

**Mitigation:** Proactive engineering relationship to influence roadmap before customer blockers surface

**Strategy:** Lead with Blueprint workarounds, advocate for native Microsoft solutions long-term
