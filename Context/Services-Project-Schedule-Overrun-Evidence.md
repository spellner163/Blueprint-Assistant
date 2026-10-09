# How Often Do Services Projects Miss Their Deadline — And Why
### Public-evidence review · researched 20 Aug 2026

---

## Bottom line

Yes, this is well documented — far better than migration pricing was. Four numbers carry most of the weight:

- **73.4%** of professional-services engagements were delivered on time in 2024 — down from 80.2% in 2021, five consecutive years of decline. So roughly **1 in 4 client engagements is late**, and worsening. *(SPI Research, n=403 PS firms — verified directly)*
- **Fewer than 10%** of completed SAP S/4HANA transformations stayed on schedule; the average ran **30% longer than planned**. *(Horváth, n=200, Q1 2025 — verified directly)*
- **63%** of organisations that had implemented RPA said their **expected speed to implement was not achieved**. *(Deloitte Global RPA Survey — verified directly, with an important caveat below)*
- **Over 60%** of data migration projects had overruns on time and/or budget. *(Bloor Research, Philip Howard)*

And one structural finding that matters more than any single percentage: **the distribution is fat-tailed, not normal.** The *median* IT project overruns by roughly zero. The *mean* is badly inflated by a minority that detonate. Flyvbjerg's 5,392-project dataset gives a mean cost-overrun ratio of 1.8 against a **median of 1.0** — and a maximum of 280×.

That reframes the argument. "Services projects run late on average" is weak and easy to dispute. "One in four is late, and one in six goes catastrophically wrong in a way you cannot forecast from your own plan" is the accurate version, and it's an argument about **risk**, not averages.

---

## 1. The base rate — how often

Sorted by how much the methodology can bear weight.

### Tier 1: Professional services delivery (most relevant to services-company client work)

**SPI Research, "Professional Services Maturity Benchmark"** — n=403 PS firms, surveyed Sep–Dec 2024, seven vertical markets. Verified directly from the PDF:

| Year | Projects delivered on time | Project overrun |
|---|---|---|
| 2020 | 79.7% | — |
| 2021 | 80.2% | — |
| 2022 | 76.2% | — |
| 2023 | 75.7% | 9.6% |
| 2024 | **73.4%** | **11.3%** |

Report's own words: *"On-time project delivery rates also fell, from 80.2% in 2021 to 73.4% in 2024, indicating increasing challenges in resource management and execution efficiency."*

This is the single best series for the question as asked: same definition every year, disclosed and stable sample, firms delivering client engagements. **Caveat:** distributed by Kantata, a PSA software vendor with an obvious interest in "delivery is getting worse." SPI runs the underlying survey independently.

Cross-check from a different panel: Statista, sourcing Kimble/Sage, puts software professional services at **73.7% on time in 2023** — near-identical, though on a much smaller sample (45–89 orgs/year).

### Tier 2: Peer-reviewed and audited

| Source | Finding | Sample |
|---|---|---|
| **Flyvbjerg et al., *JMIS* 2022** | Cost-overrun ratio mean **1.8**, median **1.0**, max **280.4**. Schedule overruns separately confirmed power-law distributed (n=962, α=3.3) | 5,392 IT projects; ~half obtained via **FOIA** of US federal filings, not self-report |
| **Flyvbjerg & Budzier, *HBR* 2011** | Mean cost overrun 27%; **1 in 6 projects is a "black swan"** averaging 200% cost overrun and **~70% schedule overrun** | 1,471 IT projects, avg value $167M |
| **Flyvbjerg et al., *PMJ* 2025** | For IT: **40.9% exceed budget**; of those, 18.3% in the extreme tail averaging **453%** overrun. IT is the only one of 23 project types with Pareto α ≤ 1 — *"infinite and unpredictable risk"* | 11,011 projects, 23 types, 126 countries, $4.64tn |
| **Moløkken-Østvold, Simula 2004** | **62% had schedule overruns**, averaging **25%**; 76% had effort overruns averaging 41% | 52 projects, 18 Norwegian companies |
| **Moløkken & Jørgensen, 2003 review** | *"Most projects (60–80%) encounter effort and/or schedule overruns… a more likely average effort and cost overrun is between 30 and 40%"* | Review of prior surveys |
| **Sauer & Cuthbertson, Oxford 2003** | Only 16% met all targets; average **schedule overrun 23%**, budget 18% | 1,500 UK IT project managers (self-reported) |
| **McKinsey–Oxford 2012** | Large IT projects run **45% over budget but only 7% over time**, delivering 56% less value. Each additional project year adds 15% to cost overrun | 5,400+ projects, all >$15M initial budget |
| **GAO 2025 (DOD IT)** | **7 of 24 (29%) behind schedule**; worst slip 4 years. 12 of 24 had cost increases | 24 DOD critical IT business programs |
| **NISTA/IPA UK major projects 2024-25** | Delivery confidence: 14% Green, 63% Amber, **15% Red**. Red-rated whole-life cost jumped from £97bn to £198bn in one year | 213 government major projects, £996bn |

**Note the McKinsey asymmetry — 45% over budget but only 7% over time.** That gap is informative: schedule is the constraint teams defend, and they defend it by spending more money, adding people, or quietly cutting scope. A project that hits its date having consumed 45% more budget did not "deliver on time" in any meaningful sense. It also means published schedule-overrun figures systematically *understate* the problem relative to cost figures.

### Tier 3: Industry surveys (directional only)

- **PMI Pulse 2018** (n=5,402): **57% on time**, 52% within budget, 52% experienced scope creep (up from 43% five years earlier), 15% deemed outright failures. PMI stopped reporting a clean "% on time" after ~2018.
- **KPMG/AIPM/IPMA Global 2019** (n≈500, 57 countries): **30% delivered on time**, 36% on budget, 19% met all objectives.
- **Wellingtone State of PM 2026**: *"Only 36% of organisations always or mostly complete projects on time."* Sample undisclosed.
- **Panorama ERP Report 2026** (n=170): ~25% over schedule, median duration 9 months. Their 2024 report (n=131) said **over half** exceeded timelines with a 15.5-month median — Panorama's methodology shifts yearly, so treat any single year as a snapshot.

---

## 2. Migration and replatforming specifically

This is where the evidence is strongest and most relevant, because migrations concentrate exactly the risk factors that cause slippage.

| Finding | Figure | Sample | Year |
|---|---|---|---|
| **SAP S/4HANA transformations** | **Less than 10% stayed on schedule.** Average project ran **30% longer than planned**. Budget "heavily exceeded" in 25%, "strongly exceeded" in a further 40%. 65% report strong-to-very-strong quality deficits | n=200 SAP users, ≥€200M revenue, DACH/N&E Europe/USA | Q1 2025 |
| **SAP migrations (separate study)** | *"Nearly 60 percent of SAP migration projects are delayed and over budget as organizations underestimate complexity, allow expansion of scope, and fail to understand internal constraints"* | ISG, n=200 senior decision-makers | 2026 |
| **Data migration** | *"More than 60% of data migration projects have overruns on time and/or budget."* Root cause: inadequate data profiling before migration | Bloor Research (Philip Howard) | 2007 |
| **Legacy modernization** | **74% of organizations have initiated but failed to complete** a legacy system modernization project | Advanced, n=400 enterprises ≥$1bn | 2020 |
| **RPA implementation** | **63% said their expected speed to implement had not been achieved** | Deloitte — but see caveat | 2017/18 |
| **RPA projects** | *"We have seen as many as 30 to 50% of initial RPA projects fail"* | EY — practitioner observation, not a survey | 2016 |
| **RPA scaling** | Only **3%** of organizations had scaled to 50+ robots | Deloitte, n=424 | 2017 |

**The Deloitte 63% needs handling carefully.** Verified from the primary PDF: the figure is *"63% of respondents said that their expected speed to implement had not been achieved"*, and it applies to the **n=32 subgroup that had actually implemented RPA**, not the full 400+ base. Forbes and others have restated it as "Deloitte's survey of 400 global firms found that 63 percent of surveyed organizations did not meet delivery deadlines for RPA projects" — which inflates the base and converts an expectation-miss into a deadline-miss. Quote it as *"of organisations that had implemented RPA, 63% said the speed of implementation fell short of expectations (Deloitte, n=32)"* and it's bulletproof. Quote the Forbes version and it's refutable.

---

## 3. The reasons

### Ranked causes for migration/transformation specifically (strongest source)

Horváth's S/4HANA study, n=200, lists the cited causes of schedule and budget deviation:

1. Expansion of project scope during execution
2. Weaknesses in project management
3. **Underestimated testing and data migration phases**
4. Revision loops of concepts and processes
5. Lack of decision-making authority
6. Inadequate planning; insufficient consideration of the right transformation approach
7. Underestimated project complexity and resource requirements
8. **Overestimated organizational competencies**
9. Inadequate selection and availability of project managers and staff
10. Underestimated IT role and perspective
11. Poor prioritization of objectives and requirements
12. Integration of too many topics into the transformation

### Ranked causes, general (PMI Pulse 2018, n=5,402, up to 3 selections)

| Cause | % |
|---|---|
| Change in organization's priorities | 39% |
| Inadequate vision or goal for the project | 37% |
| **Inaccurate cost estimates** | 35% |
| Change in project objectives | 29% |
| **Limited/taxed resources** | 29% |
| Inadequate/poor communication | 28% |
| Poor change management | 28% |
| Inadequate sponsor support | 26% |
| Inadequate resource forecasting | 26% |
| **Inaccurate requirements gathering** | 25% |
| Risks not defined | 22% |
| Resource dependency | 21% |

### Ranked causes of "challenged" projects (Standish 1994 — historically important, methodologically weak)

1. Lack of user input — 12.8%
2. **Incomplete requirements & specifications — 12.3%**
3. **Changing requirements & specifications — 11.8%**
4. Lack of executive support — 7.5%
5. Technology incompetence — 7.0%
6. Lack of resources — 6.4%
7. Unrealistic expectations — 5.9%
8. Unclear objectives — 5.3%
9. **Unrealistic time frames — 4.3%**
10. New technology — 3.7%

### ERP-specific (Panorama 2015, ranked reasons for schedule overrun)

Unrealistic timeline 14% · Expanded project scope 13% · Technical issues 13% · Resource constraints 13% · Data issues 12% · Organizational issues 10%

### The behavioural explanation

Flyvbjerg's ranked top-ten biases in project management (2021), from a meta-analysis of 2,062 projects showing mean cost-overrun ratio 1.39–1.43 (p<0.0001):

1. **Strategic misrepresentation** — *"deliberate distortion of information for strategic advantage; political bias rather than innocent error."* This is the deliberate lowball to win the bid or the approval. Flyvbjerg ranks it **first**, above optimism bias.
2. **Optimism bias** — the same underestimate, without intent.
3. Uniqueness bias — "our project is different, so past data doesn't apply."
4. Planning fallacy · 5. Overconfidence · 6. Hindsight · 7. Availability · 8. **Base rate fallacy** · 9. Anchoring · 10. Escalation of commitment.

Supporting mechanisms worth knowing by name:

- **Planning fallacy** (Kahneman & Tversky) — estimates built from an "inside view" of project specifics are systematically optimistic; the fix is **reference-class forecasting** against a population of comparable past projects. Kahneman's own caution: *"awareness of a perceptual or cognitive illusion does not by itself produce more accurate perception"* — knowing about the bias doesn't remove it. The UK Department for Transport adopted reference-class forecasting in 2004 and mandates cost uplifts of **15–57%** depending on project type.
- **Brooks's Law** — *"Adding manpower to a late software project makes it later."* Communication paths grow as (n²−n)/2, so 10 people means 45 interfaces. Directly relevant: the standard services response to a slipping migration is to add developers, which makes it worse.
- **Student syndrome / 90% syndrome** (Goldratt) — work expands to consume the buffer, and projects sit at "90% done" indefinitely.

### The pattern across every list

Strip the wording differences and the top causes converge on three things:

1. **Scope turned out to be different from what was assumed** — incomplete requirements, expanded scope, discovered complexity, data issues.
2. **The original estimate was wrong** — sometimes honestly (optimism bias), sometimes not (strategic misrepresentation to win the work).
3. **The client couldn't feed the project fast enough** — resource constraints, sign-off delays, lack of decision-making authority, SME availability, overestimated organizational competencies.

A migration off an undocumented legacy estate maximises all three simultaneously. Nobody knows what the old automations actually do, the estimate has to be made before anyone finds out, and the only people who could tell you are the client's own busy staff. Horváth's list naming *"underestimated testing and data migration phases"* and *"overestimated organizational competencies"* is that exact failure mode, measured.

---

## 4. Statistics not to use

Citation hygiene matters here, because most of the widely circulated numbers are compromised.

- **Standish CHAOS.** The most-quoted source in the industry and the least defensible. The 1994 original (16.2% successful / 52.7% challenged / 31.1% failed; 189% average cost overrun, 222% average time overrun) is real and citable *as a historical artefact*, but every serious review found the methodology indefensible: Jørgensen & Moløkken (2006) found **three conflicting definitions of "cost overrun" in the same document**, noted Standish solicited *"failure stories"* from executives, and reported that **Standish refused to disclose its methodology**. Eveleens & Verhoef (IEEE Software 2010) showed the same underlying data could yield **6% or 94%** success depending on institutional estimating bias, and that the definitions are one-sided — penalising overruns while ignoring underruns. Post-2000 CHAOS figures are paywalled and secondary sources contradict each other on the same year (2012 is variously 37/42/21 and 27/56/17). Don't build anything on it.
- **"83% of data migrations fail or exceed budget and schedule," attributed to Gartner.** Untraceable. No Gartner report says this. It appears to be a drifted restatement of Bloor's figure. Use Bloor's actual, verifiable **">60% have overruns on time and/or budget."**
- **"75% of cloud migrations ran over budget, 37% behind schedule" (McKinsey 2021)** and **"90% of CIOs have experienced failed ERP-to-cloud migrations" (CSA 2019).** Found only in a single secondary blog. No primary document located.
- **"1 in 3 cloud migrations fail" (Unisys).** The primary release is about failure to realise expected *benefits*, and contains no schedule language at all. Secondary coverage invented the framing.
- **Geneca's "75% of projects doomed from the start."** Measures executive *sentiment*, not delivery outcomes. Also lead-gen content from a custom-dev shop.
- **No verifiable Gartner, Forrester, or IDC primary figure exists** for "% of IT projects delivered late." Every instance found was an uncredited blog citation. Likewise no Forrester or HFS figure for RPA failure rates.
- **No SI has ever publicly stated its own overrun rate.** The closest thing to an admission is litigation defence language, which is non-admissive by construction.

---

## 5. How to use this

**Lead with the professional-services number, not the scary one.** "Roughly one in four client engagements is delivered late, and that's been getting worse for five straight years" (SPI, n=403) is defensible, recent, and about exactly the thing being discussed. The Standish-derived "70% of projects fail" folklore is a liability — anyone who checks it finds the critiques.

**For migration work specifically, the SAP number is the sharpest instrument.** *Fewer than 10% of S/4HANA transformations stayed on schedule; the average ran 30% long* (n=200, Q1 2025). It's recent, independent, properly sampled, and it's a like-for-like legacy replatforming exercise.

**Argue risk, not averages.** The median project is roughly on plan; the mean is wrecked by a fat tail. Flyvbjerg's framing — *one in six is a black swan with ~200% cost and ~70% schedule overrun*, and IT is the only project category with theoretically unbounded variance — is a much stronger argument than any average, and it's the argument that justifies paying for predictability rather than paying for days.

**The causes are the real story for a migration pitch.** Every ranked list puts discovered scope, wrong estimates, and client-side resource constraints at the top. A manual rebuild of an undocumented RPA estate is a machine for generating all three. Anything that inventories the estate before the estimate is made attacks the top cause directly — and "31 of 100 bots turned out not to be needed" is that argument in one line.

**Note what nobody publishes.** No SI discloses its overrun rate, and no public dataset tracks RPA migration schedule performance specifically. The RPA-adjacent numbers that exist (Deloitte's 63%, EY's 30–50%) are thin — one is an n=32 subgroup, the other is an anecdote. That gap is worth being honest about rather than papering over.

---

## Sources

**Verified directly this session**
- SPI Research / Kantata, 2025 Professional Services Maturity Benchmark (n=403) — https://get.kantata.com/rs/677-LEJ-696/images/2025-ps-maturity-benchmark.pdf
- Deloitte Global RPA Survey — https://werkflo.com.au/assets/files/Deloitte-us-cons-global-rpa-survey-2018S.pdf
- Horváth, SAP S/4HANA transformation study (n=200, Q1 2025) — https://www.horvath-partners.com/en/press/detail/study-shows-sap-s-4hana-transformations-rarely-go-as-planned-60-percent-exceed-budget-and-schedule-two-thirds-dissatisfied-with-result-quality

**Academic**
- Flyvbjerg et al., "The Empirical Reality of IT Project Cost Overruns: Discovering A Power-Law Distribution," *JMIS* 39(3), 2022 — https://arxiv.org/abs/2210.01573
- Flyvbjerg & Budzier, "Why Your IT Project May Be Riskier Than You Think," *HBR* 2011 — https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2229735
- Flyvbjerg et al., "The Uniqueness of IT Cost Risk: A Cross-Group Comparison of 23 Project Types," *PMJ* 57(1), 2025 — https://journals.sagepub.com/doi/10.1177/87569728251340590
- Flyvbjerg, "Top Ten Behavioral Biases in Project Management," *PMJ* 2021 — https://journals.sagepub.com/doi/10.1177/87569728211049046
- Jørgensen & Moløkken-Østvold, "How large are software cost overruns? A review of the 1994 CHAOS report," *IST* 48(4), 2006 — https://web-backend.simula.no/sites/default/files/publications/Jorgensen.2006.4.pdf
- Moløkken-Østvold, Norwegian BEST-Pro survey, Simula 2004 — https://web-backend.simula.no/sites/default/files/publications/SE.3.Moloekken-Oestvold.2004.pdf
- Eveleens & Verhoef, "The Rise and Fall of the Chaos Report Figures," *IEEE Software* 27(1), 2010 — https://www.cs.vu.nl/~x/the_rise_and_fall_of_the_chaos_report_figures.pdf
- Sauer & Cuthbertson, "The State of IT Project Management in the UK 2002–2003," Oxford — https://www.academia.edu/28996125/The_State_of_IT_Project_Management_in_the_UK_2002_2003

**Industry and audit**
- McKinsey–Oxford, "Delivering large-scale IT projects on time, on budget, and on value," 2012 — https://www.mckinsey.com/capabilities/tech-and-ai/our-insights/delivering-large-scale-it-projects-on-time-on-budget-and-on-value
- PMI Pulse of the Profession 2018 — https://www.pmi.org/-/media/pmi/documents/public/pdf/learning/thought-leadership/pulse/pulse-of-the-profession-2018.pdf
- KPMG/AIPM/IPMA Global Project Management Survey 2019 — https://ipma.world/app/uploads/2019/11/PM-Survey-FullReport-2019-FINAL.pdf
- Panorama Consulting ERP Report 2026 — https://4439340.fs1.hubspotusercontent-na1.net/hubfs/4439340/Reports/ERP%20Report/2026-erp-report-panorama-consulting-group.pdf
- Panorama Consulting ERP Report 2015 (ranked overrun causes) — https://www.panorama-consulting.com/wp-content/uploads/2016/07/2015-ERP-Report-3.pdf
- Bloor Research, "Data Migration" white paper (Philip Howard) — https://www.existbi.com/wp-content/uploads/2015/12/Bloor-Data_Migration-White-Paper.pdf
- Advanced, legacy modernization report (n=400) — https://www.businesswire.com/news/home/20200528005186/en/
- EY, "Get Ready for Robots," 2016 — https://eyfs.ie/wp-content/uploads/2016/11/ey-get-ready-for-robots.pdf
- ISG SAP migration research, 2026 — https://www.theregister.com/2026/02/05/sap_migrations_research/
- NISTA Annual Report on Major Projects 2024-25 — https://www.gov.uk/government/publications/nista-annual-report-2024-2025/nista-annual-report-2024-25
- GAO, DOD IT systems over budget and delayed, 2025 — https://www.gao.gov/blog/dod-efforts-buy-and-maintain-it-systems-are-billions-over-budget-and-delayed
- Standish Group, CHAOS Report 1994 — https://cs.franklin.edu/~smithw/ITEC495_Resources/chaos%20report.pdf
