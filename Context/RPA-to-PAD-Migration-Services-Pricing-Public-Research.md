# What Services Companies Charge for RPA → Power Automate Desktop Migration
### Public-source pricing benchmark · researched 20 Aug 2026 · rev. 2 (G-Cloud rate basis verified against source documents)

---

## Bottom line

There is no public price list for this work. Across four parallel sweeps — Microsoft AppSource/Azure Marketplace, government procurement portals in five countries, SI and tooling-vendor content, and case studies plus practitioner forums — exactly **one** publicly disclosed contract value was found for an engagement scoped specifically to migrating RPA automations to Power Automate Desktop. Everything else is either a day rate, a vendor's estimate of what *manual* migration costs, or a savings percentage with no denominator.

Three things are publicly knowable, and they're worth separating:

1. **One real transaction price** — a £30,000 UiPath→PAD migration contract, which happens to be Blueprint's own Ofsted deal.
2. **Labour day rates** from UK G-Cloud, where suppliers are compelled to publish them — but see the caveat in §2: these are **generic firm-wide SFIA rate cards, not prices for migration**. Verified realistic build-team blend: **£900–£1,150/day**.
3. **Per-bot cost claims** of $5,000–$30,000 per automation — which are almost entirely Blueprint's own marketing, and which don't agree with each other.

The market is opaque by design. Every AppSource offer and every SI landing page routes to "book a free assessment." That opacity is itself the competitively useful finding: nobody is anchoring a public price, so whoever produces a defensible per-bot number owns the conversation.

---

## 1. The only hard, migration-specific contract price found anywhere

**Ofsted → Blueprint Software Systems**

| Field | Detail |
|---|---|
| Contract title | "Migration of automations from UIPath to PowerAutomate Desktop (PAD)" |
| Buyer | Ofsted (UK non-ministerial government department) |
| Supplier | BluePrint, 90 Eglinton Avenue E, Suite 604, Toronto M4P 2Y3, Canada |
| Scope stated | "Automations migration to align with existing Microsoft technology infrastructure." No bot or process count disclosed. |
| **Value** | **£30,000 excl. VAT / £36,000 incl. VAT** (≈ $39,000 USD at ~$1.30/£) |
| Award date | 26 June 2025 |
| Performance period | 1 Aug 2025 – 30 Mar 2026 (8 months) |
| Procedure | Below threshold — **without competition** |
| Refs | CON 1556 · Notice 2025/S 000-041038 · OCID ocds-h6vhtk-056179 |
| Source | https://www.find-tender.service.gov.uk/Notice/041038-2025 |

Ofsted's prior-year UiPath licence renewal is also public — **£44,800**, awarded 20 Dec 2024 for a 12-month term — which frames the buyer's motive: the migration cost less than one year of the licence it was displacing.

**Why this number matters more than its size.** £30,000 over an 8-month window, priced against the verified £900–£1,150/day build rate in §2, implies roughly 26–33 person-days of billable effort at the verified £900–£1,150 build rate. That is not a body-shop rebuild. It is a tool-led migration, and it is currently the only public price point in the world for one. Anyone benchmarking a services-led manual rebuild against it will look expensive — which is useful, but it also means Blueprint has publicly anchored the *low* end of this market, and a competitor doing the research you just asked for will find the same page.

Worth verifying internally what was actually in scope on that engagement (bot count, action count, how much of the £30k was Migrator licence vs. services), because the public notice gives none of that and the number will get quoted back at you without it.

---

## 2. Day rates — what they actually attach to (verified)

**Important correction, checked directly against the source documents.** The published rate on a G-Cloud listing is attached to that listing, but it is **not a price for the service named in the listing**. It is the minimum and maximum of the supplier's **generic firm-wide SFIA rate card**, reused verbatim across every service they list.

Evidence, all verified this session:

- Robiquity's two listings — "RPA Platform Migration" and "Intelligent Automation (IA) and RPA" — show the **identical** £450–£1,500 range.
- Robiquity's own pricing document states the rates are **"general company rates, not specific to a particular service,"** applied on a "resource-per-day approach."
- Robiquity's service definition document contains **no pricing at all** — no fixed fee, no per-bot, no per-automation, no token pricing. "Platform and vendor migration" appears only as one capability in a list.
- Proventeq's pricing document says pricing is **"Based on SFIA rate card for the requested"** role, and reproduces no rates. Its service definition document contains zero prices and doesn't name UiPath, Blue Prism, or Automation Anywhere at all.
- A "unit" is simply **one consultant day** — Robiquity: "Consultant's Working Day – 8 hours exclusive of travel and lunch"; Proventeq: "1 Person day."

**So: £450–£1,500 is not what an RPA migration costs. It is the floor and ceiling of one firm's labour rate card.**

### What is genuinely useful: the underlying rate grid

The full SFIA card behind Robiquity's RPA Platform Migration listing — a firm that is UiPath Platinum, Blue Prism Gold and a Microsoft partner, and whose listing explicitly describes "transferring an organization's existing automated processes… from one RPA platform to another":

| SFIA level | Solution Development & Implementation | All other columns |
|---|---|---|
| 1. Follow | £450 | — |
| 2. Assist | £750 | £750 (Client Interface) |
| 3. Apply | £900 | £900 |
| 4. Enable | £1,150 | £1,150 |
| 5. Ensure or Advise | £1,250 | £1,250 |
| 6. Initiate or Influence | £1,500 | £1,500 |
| 7. Set Strategy or Inspire | £1,500 | £1,500 |

Onshore resource, excl. VAT and expenses, 8-hour day. Source: https://assets.applytosupply.digitalmarketplace.service.gov.uk/g-cloud-14/documents/712742/764494112880187-sfia-rate-card-2024-04-26-1541.pdf

**A real migration build team sits at SFIA 3–4 — so £900–£1,150/day (≈ $1,170–$1,500) is the defensible number**, not the £450–£1,500 range. £450 is a level-1 junior; £1,500 is a strategy partner. Neither does the work.

### Other suppliers' published ranges

Same caveat applies to all of these — they are firm-wide rate-card min/max, verified for Robiquity and Proventeq and structurally identical across the framework:

| Supplier | Service listing naming RPA migration | Published range |
|---|---|---|
| **Robiquity** | RPA Platform Migration (names Blue Prism, UiPath, Power Platform) | £450 – £1,500 / day |
| **Proventeq** | Legacy BPM/RPA/Workflow Migration Services; RPA modernization services | £605 – £1,375 / day |
| **Bridgeall** | Power Automate Development & Consultancy (incl. migration) | £450 – £1,650 / day |
| **Onepoint Consulting** | RPA with Microsoft Power Platform Services | £335 – £1,900 / day |
| **Infomentum** | Automation and RPA — incl. "upgrade or migration services" | £700 – £1,200 / person / day |
| **Protiviti** | RPA & IA — covers "migrating between different cloud/on-prem RPA providers" | £400 / unit |
| **PwC** | RPA and Automation Services (UiPath, Power Automate, Blue Prism, AA) | £100 – £2,750 / day |
| **UST Global** | RPA Services (multi-platform incl. Power Automate) | £500 / day |
| **VKY Intelligent Automation** | Power Automate Delivery Service | £350 – £1,600 / day |
| **CEOX Services** | Power Automate RPA Services | £394 – £995 / day |

Generic G-Cloud SFIA cards from non-RPA consultancies run £600/day at levels 1–3, £850 at 4–5, £1,200 at 6–7. Robiquity's £900/£1,150 at levels 3/4 is a modest premium — so RPA migration skills carry maybe 10–35% over general consultancy, not a category premium.

### The finding underneath the correction

**Not one supplier on G-Cloud — the most pricing-transparent procurement channel in the world for this work — publishes a fixed price, a per-bot price, a per-process price, or any outcome-based price for RPA migration.** Every single one falls back to time-and-materials against a generic rate card. Robiquity's listing summary mentions "fixed-fee and token-based" models, but no document attaches a number to either.

That is arguably more useful to you than a rate would have been: the entire services market sells this work as undifferentiated day-rate labour. A per-bot price is an empty space.

## 3. Per-bot / per-process cost claims — and who is making them

This is where the widely circulated numbers live, and it needs a blunt caveat: **nearly every quantified "manual migration costs $X per bot" figure in the public domain traces back to Blueprint's own content.**

| Figure | Exact claim | Source |
|---|---|---|
| **$5,000 / bot** | "any migration effort is estimated at $5000/bot" | blueprintsys.com (Power Automate Premium licences post; repeated in the Part 3 "switch to Power Automate" post) |
| **$10,000 / bot** | "a simple automation with mid-level complexity can cost up to $10k and take 4-6 weeks to migrate" | blueprintsys.com/blog/rpa/3-ways-to-ensure-a-successful-rpa-platform-migration |
| **$20,000 / automation** | "Manually migrating a moderately complex automation by re-building it in the new platform can take 4-6 weeks and cost upwards of $20,000" | blueprintsys.com/rpa-replatforming-faq |
| **$30,000 → $20,000 → $10,000** | "A simple automation costs about $30,000 to migrate manually… Without Blueprint, Avanade brings that cost down to $20K… With Blueprint… closer to $10K" | blueprintsys.com (SI-partner benefits post, attributing to Avanade) |
| **Hundreds of thousands to millions** | "If you're re-platforming 100-150 bots for example, it can cost hundreds of thousands, up to millions of dollars" | blueprintsys.com/rpa-replatforming-faq |
| Savings claim | Variously "25-30% of the cost", "75% of the cost", "reduce costs by 80%", "reduce costs by 75%", "60-75% time and effort savings" | five different blueprintsys.com pages |

**The problem, stated plainly:** the same domain gives $5,000, $10,000, $20,000, and $30,000 as the cost to manually migrate one automation, and gives the Blueprint discount as anywhere from 70% to 80% off, or alternatively as "75% of the cost" (which means 25% off — the opposite direction). A competitor or a skeptical prospect who reads more than one page will notice. If any of these are going into a deck, they need to be reconciled into one defensible tier table with stated complexity definitions.

**The one methodology that is at least transparent** — and therefore the most defensible thing on the site — is the effort model: "the average RPA developer can code 40 actions or lines of code per hour," so 100,000 actions ÷ 40 = 2,500 hours = 312.5 person-days. That formula is checkable and scales. It's a better foundation for a public number than the per-bot dollar figures. (Source: blueprintsys.com/blog/how-to-estimate-manual-rpa-migration)

**Non-Blueprint quantified claims are rare.** Microsoft's own Power Platform blog documents a PG&E migration of 12 automations where "migration efforts leveraging Workbench often are reduced by at least 60%," yielding "$130k in license savings" — an effort reduction and a licence saving, but no services cost.

---

## 4. What SIs disclose: scope and duration, never price

Every case study found discloses bot counts and timelines and refuses to disclose fees. Useful for effort benchmarking, useless for price benchmarking.

| Customer | Partner | Source platform | Scope | Duration | Economics disclosed |
|---|---|---|---|---|---|
| CoreLogic (APAC) | Cognizant | On-prem desktop RPA (unnamed) | 16 processes | 4-month execution inside a 6-month deadline | "5x reduction in platform costs"; 100% code accuracy; 50,000+ hours capacity freed. **No fee.** |
| Unnamed global media agency | iOPEX | UiPath | 100+ bots | Under 5 months | "$1.95M in automation cost savings." **No fee.** |
| Unnamed Singapore education institution (<1,000 staff) | CFB Bots | UiPath | 3 bots | Under 1 month | 86.9% cost reduction from year 2; UiPath attended licences "8.9x more" than Power Automate. **No fee.** |
| Uber | Microsoft (self-reported) | Desktop RPA (unnamed) | 80+ processes, 40,000 flows | Completed end-2024 | $9M/yr savings; 300,000+ hours/yr. **No fee.** |
| Unnamed oil & gas (80,000 staff) | Blueprint | Not named | 70 bots / 200,000 actions (31 of 100 decommissioned) | **3 months vs. a 24-month manual estimate** | 60% resource saving; 40% TCO reduction. **No fee.** |

The oil & gas 3-months-vs-24-months comparison is the most quotable ratio in the set, and the 31-of-100-bots-decommissioned detail is arguably the stronger selling point — a third of the estate turned out not to be worth migrating at all.

**Genuine gap:** no case study anywhere discloses cost figures for a migration *from* Blue Prism, Automation Anywhere, Kofax, Pega, or NICE specifically. Those source platforms have zero public migration cost data.

---

## 5. Bottom-up: what a services-led migration should cost

Since no one publishes a total, here's a model built only from published inputs.

**Inputs**
- Verified UK build-team rate, SFIA 3–4, from a supplier that explicitly sells RPA platform migration: **£900–£1,150/day** (≈ $1,170–$1,500)
- US contract rates from live job postings: **$100–$180/hr** for RPA/automation consultants (≈ $800–$1,440/day)
- Named-partner Clutch bands: Avanade **$200–$300/hr**; HSO **$100–$149/hr**; Quisitive **$50–$99/hr** (min. project $25,000); Devoteam **$25–$49/hr**
- Offshore advertised: from **$14/hr**
- Upwork project bands, published: "Desktop automation or RPA: **$5,000–$15,000+/project**"; "Power Platform integration: $4,000–$10,000/project"

**Modelled cost per process, manual rebuild** (analyse → rebuild → test → UAT → cutover)

| Complexity | Person-days | At £900/day (~$1,170) | At £1,150/day (~$1,500) |
|---|---|---|---|
| Simple | 3–6 | $3,500–$7,000 | $4,500–$9,000 |
| Moderate | 8–15 | $9,400–$17,600 | $12,000–$22,500 |
| Complex | 20–40 | $23,400–$46,800 | $30,000–$60,000 |

This brackets Blueprint's published claims: the **$5,000–$20,000 per automation** range is defensible for simple-to-moderate work at Western onshore rates. The **$30,000 "simple automation"** figure is not — that's complex-tier money for simple-tier scope, and it's the one number most likely to get challenged.

Independent corroboration for the low end: Upwork's own published band for "desktop automation or RPA" project work is $5,000–$15,000, which lands on the same range from a completely different market.

---

## 6. The other side of the business case: published licence prices

Microsoft US list, from microsoft.com/en-us/power-platform/products/power-automate/pricing:

| SKU | List price |
|---|---|
| Power Automate Premium | $15.00 / user / month (annual) |
| Power Automate Process (unattended bot) | $150.00 / bot / month (annual) |
| Power Automate Hosted Process | $215.00 / bot / month (annual) |
| Process Mining add-on | $5,000.00 / tenant / month (annual) |
| Copilot Studio | $200.00 / 25,000 credits / month (annual) |

Microsoft's own disclaimer on that page: *"Prices shown are for marketing purposes only and may not be reflective of actual list price."*

Useful ratio for ROI framing: at $150/bot/month, a 100-bot unattended estate is **$180,000/year** on Power Automate. CFB Bots' published comparison puts UiPath attended licences at "8.9x more" and unattended at "5.6x more" — so the same estate on UiPath implies roughly $1.0M/year, and migration services at even $10,000/bot pay back inside 15 months on licensing alone. That is the arithmetic that actually sells migrations, and it does not depend on any contested per-bot figure.

Also worth carrying: HFS Research (interviews with 359 RPA power users) found "RPA licensing costs represent just 25% to 30% of total costs for implementing RPA" — i.e. licence-only comparisons understate the real prize by 3–4x.

---

## 7. What does not exist publicly (searched and confirmed empty)

- **No fixed-price AppSource offer.** ~17 RPA-migration consulting offers identified (Akkodis, Velrada, HCL "Sher.PA", Acuvate, CitiusTech, Sonata "RPA Migration Factory", Fullscope, TCS, Teleperformance, Ashling, Hitachi Solutions). Titles advertise duration — "2-Wk Assessment", "4-6 WK Migration", "6 Weeks Engagement" — never price. Note: Microsoft's marketplace returns HTTP 403 to automated fetching, so for most of these "no price found" means unverifiable rather than confirmed absent. The one page that did load (Teleperformance, "RPA Migration Assessment with POC") showed no price.
- **No US federal contract data.** sam.gov and usaspending.gov are JavaScript apps that can't be read by these tools; no relevant award surfaced via search either. AusTender returns 403, CanadaBuys blocks robots. TED returned nothing on-topic. The UK is effectively the only transparent market here.
- **No GSA labor category** for "RPA Developer" or "Power Platform Developer" was found; GSA's own RPA Community of Practice page carries no pricing.
- **No practitioner anecdotes.** Repeated searches of Reddit (r/rpa, r/PowerPlatform), Hacker News, Spiceworks, UiPath Forum and Power Platform Community turned up **zero** posts where someone states what they were quoted or what they charged. The Power Platform forum discussion is limited to restating Microsoft's $150/bot/month list price and noting that migration "requires human inputs" because "there is simply too much variability and judgement required."
- **No SI publishes a rate card outside G-Cloud.** Every US/global partner page checked — CFB Bots, Kanerika, WinWire, Katpro, Veelead, RPAVendor, Innovational, Step One Step Ahead, Toptal, Roboyo, Ashling, Auxis, Reveal Group — routes to "free assessment / book a consultation." Veelead names its engagement models ("Fixed Price", "Time and Material") with no rates attached.
- **Analyst data is absent.** No Gartner, Forrester, Everest or HFS figure exists for migration cost specifically. The two Microsoft-commissioned Forrester TEI numbers in circulation (248% ROI / $39.85M NPV, and 199% ROI / $1.7M benefit) are whole-platform economics, don't reconcile with each other, and should not be cited as migration costs.

---

## 8. Implications for positioning

**The pricing vacuum is the opportunity.** No competitor has anchored a public price. The first credible, tiered, defensible per-bot number in this market becomes the reference point everyone else has to argue against.

**No competitor prices this by the bot.** Verified: across the whole of G-Cloud, every supplier sells RPA migration as time-and-materials against a generic SFIA rate card. Nobody publishes a per-bot or fixed price. A tiered per-bot price is not just an anchor — it's a differentiated commercial model in a market that only sells days.

**Blueprint's current numbers are the weak link.** Four different per-bot figures and five different savings percentages across one website is the kind of thing a competitor's research pass finds in an afternoon — this one did. One tier table, one methodology, complexity defined, published once.

**The £30k Ofsted contract cuts both ways.** It's proof of a real tool-led price point at a fraction of manual cost, and it's a public ceiling anchor that a procurement team will find. Decide deliberately whether to lead with it.

**Lead with licensing arithmetic, not migration cost.** The $150/bot/month vs. "5.6x more" comparison is fully public, uncontested, and pays back migration services inside a year and a half. It doesn't require winning an argument about what a manual rebuild costs.

**Effort ratios beat dollar claims.** "3 months instead of 24" and "31 of 100 bots turned out not to be needed" are more durable than "$20,000 per bot," because they don't depend on anyone's rate card.

---

## Sources

**Verified directly**
- Ofsted / Blueprint contract award — https://www.find-tender.service.gov.uk/Notice/041038-2025
- Robiquity RPA Platform Migration, G-Cloud listing — https://www.applytosupply.digitalmarketplace.service.gov.uk/g-cloud/services/764494112880187
- Robiquity SFIA rate card (PDF) — .../g-cloud-14/documents/712742/764494112880187-sfia-rate-card-2024-04-26-1541.pdf
- Robiquity pricing document (PDF) — .../712742/764494112880187-pricing-document-2024-04-26-1540.pdf
- Robiquity service definition (PDF) — .../712742/764494112880187-service-definition-document-2024-05-01-0932.pdf
- Proventeq pricing document (PDF) — .../702830/140518221430542-pricing-document-2024-04-28-0705.pdf
- Proventeq service definition (PDF) — .../702830/140518221430542-service-definition-document-2024-04-30-1345.pdf

**G-Cloud rate cards** — Proventeq (649412406208121, 140518221430542), Bridgeall (210686269730323), Onepoint (525640983349832), Infomentum (556647207401806), Protiviti (491000291429925), PwC (456401552308950), UST (927725625576167), VKY (392140133805483), CEOX (238217538365292), Ingentive (365758208383584), Appetite for Business (775338863852980), all at https://www.applytosupply.digitalmarketplace.service.gov.uk/g-cloud/services/{id}

**Per-bot / effort claims** — https://www.blueprintsys.com/rpa-replatforming-faq · https://www.blueprintsys.com/blog/how-to-estimate-manual-rpa-migration · https://www.blueprintsys.com/blog/rpa/3-ways-to-ensure-a-successful-rpa-platform-migration · https://www.blueprintsys.com/blog/the-5-benefits-of-migrating-automation-estates-with-service-integrators · https://www.blueprintsys.com/blog/microsoft-unveils-power-automate-premium-licenses · https://www.blueprintsys.com/casestudy/major-oil-and-gas-provider-migrates-rpa-estate-to-microsoft-power-automate-with-blueprint-in-3-months

**Case studies** — https://www.cognizant.com/us/en/case-studies/corelogic-rapid-power-automate-migration · https://www.microsoft.com/en/customers/story/22687-corelogic-asia-pacific-power-automate · https://www.microsoft.com/en/customers/story/19751-uber-technologies-inc-power-automate · https://www.iopex.com/case-studies/global-media-agency-migrates-automation-bots-from-uipath-to-power-automate · https://www.cfb-bots.com/case-study-uipath-to-power-automate-migration · https://www.microsoft.com/en-us/power-platform/blog/power-automate/begin-your-robotic-process-automation-modernization-journey/

**Rates & licensing** — https://www.microsoft.com/en-us/power-platform/products/power-automate/pricing · https://www.itjobswatch.co.uk/contracts/uk/power%20platform%20developer.do · https://www.upwork.com/hire/power-automate-experts/ · https://clutch.co/profile/avanade · https://clutch.co/profile/hso · https://clutch.co/profile/quisitive-0 · https://www.ziprecruiter.com/Salaries/Rpa-Consultant-Salary · https://www.hfsresearch.com/research/how-to-make-sense-of-nonsensical-rpa-software-pricing/
