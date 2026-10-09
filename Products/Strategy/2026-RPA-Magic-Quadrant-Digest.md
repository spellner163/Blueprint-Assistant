# Gartner Magic Quadrant for Robotic Process Automation — 2026 (Digest)

*Published 24 June 2026 · ID G00839318 · Authors: Arthur Villa, Melanie Alexander, and 3 others.*

> This is a paraphrased digest for internal reference, not a verbatim reproduction of the Gartner report. Figures, placements, and characterizations are summarized from the source. © Gartner, Inc.

## Overview

The report evaluates 10 enterprise RPA vendors. Gartner frames RPA as still the most cost-effective, reliable way to automate UI interactions for task-based workflows, especially against OS-based applications that lack APIs.

**Strategic planning assumption:** By 2028, "computer use" (CU) capabilities will become a viable technical alternative for UI automation of *web-based* applications.

**Market definition:** RPA is software that automates tasks in business and IT processes using scripts that emulate human interaction with an application UI. Scripts can be recorded or built via low-code/no-code GUIs, then deployed to different runtimes (each runtime executable is a "bot"). Two primary modes:

- **Unattended automation** — bots move data in/out of systems without human interaction; typically system-triggered and server-executed.
- **Attended automation** — a human in the loop; bots extract/prepare information at the point of need; typically human-triggered and run on a local device.

## Quadrant Placements

| Quadrant | Vendors |
|---|---|
| **Leaders** | UiPath, Automation Anywhere, Microsoft |
| **Challengers** | Appian, Pegasystems |
| **Visionaries** | ServiceNow, SS&C Blue Prism |
| **Niche Players** | EvoluteIQ, Laiye, Samsung SDS |

*(As of May 2026. Axes: Ability to Execute vs. Completeness of Vision.)*

---

## Vendor Strengths and Cautions

### UiPath — Leader
Solution: UiPath Platform (Studio, Orchestrator, Autopilot). Global operations, serves every buyer segment; top industries are banking/financial services/insurance, manufacturing, and professional services. Roadmap: restructured Orchestrator information architecture, extending AI assistance into operations via Autopilot, and solutions authored directly in Studio on desktop.

- **Strengths:** Highest RPA-specific revenue and the largest volume of RPA client inquiries; 10,000+ customers and an extensive partner network. Strong product capabilities — agentic CU, natural-language development, proprietary self-healing (computer vision + semantic selectors), and an AI Trust Layer for governance, PII masking and central policy control. Broad geographic strategy (developer UI in 10 languages, cloud across eight regions, 6,500+ delivery/reseller partners).
- **Cautions:** Shifting to unified "Platform Units" pricing, which existing customers may find disruptive; the engagement model can challenge organizations with strong internal governance. Its 2026 repositioning toward a "business orchestration platform" risks confusing buyers who just want tactical, task-based UI automation.

### Automation Anywhere — Leader
Global operations, customer base focused on large enterprises; top industries are banking/financial services, manufacturing, and healthcare. Roadmap: richer orchestration layer/runtime, a context-intelligence layer for AI agents, and policy-based lifecycle management of processes and components.

- **Strengths:** Strong customer experience (three-tiered global support, dedicated key-accounts program, CoE Manager, quarterly business reviews for ROI). Product capabilities include a generative recorder that self-corrects UI failures in real time via vision models + DOM parsing, an AES-256 encrypted credential vault, and object-based UI automation inside Citrix, VMware and multiuser Microsoft Remote Desktop via embedded remote agents. Good market understanding (packaged solutions, centralized governance, consumption-based pricing, Pathfinder scaling framework).
- **Cautions:** Focus is shifting to agentic automation with signaled reduction in RPA-specific R&D — traditional-RPA buyers should confirm the roadmap keeps innovating. Feature gaps: no native mobile-app automation and no native automated test-case generation; cloud deployments limited to a single external key vault per tenant (multi-vault planned for the July 2026 release).

### Microsoft — Leader
Solution: Power Automate for desktop (desktop flow designer, machine runtime, PowerAutomate.com, Flow checker). Global; serves large enterprises and SMBs; top industries are financial services, healthcare/life sciences, manufacturing. Roadmap: end-to-end process observability, agentic + deterministic automation composition, passwordless auth for unattended bots.

- **Strengths:** Cost-effective — pricing typically 20–40% below most-compared competitors, plus a free version for individual/attended use in newer Windows deployments. Deep integration with Microsoft Office apps (Word, Excel), a top-three integration target across nearly all RPA providers.
- **Cautions:** Licensing is complex and *not* free for enterprise RPA use — entitlements vary across Dynamics 365, Windows and Microsoft 365, and most orgs pay extra for Azure orchestration and Dataverse, making licensing opaque. Based on thousands of inquiries, large orgs use it as a *secondary* RPA tool (Microsoft-app automation, citizen development, or negotiating leverage), almost never as primary. Customers report sluggish performance, unreliable connections and limited development capabilities that constrain scaling for critical processes.

### Appian — Challenger
Solution: Appian RPA (Appian Designer, RPA Agent, RPA Orchestrator). Global; top industries are public sector, financial services, insurance. Roadmap: multitenant Appian Community Edition, RPA as a tool for AI agents in Appian Agent Studio, custom business-attribute tracking across process paths.

- **Strengths:** Attractive packaging — a premium bundle with unlimited RPA bots and tightly integrated automation for broader process transformation. Strong customer experience (dedicated success managers, Insight to Action program, Operations Console, and Process HQ process intelligence for native ROI measurement).
- **Cautions:** Weak stand-alone brand awareness — rarely considered unless the org already runs the Appian platform. Product strategy is moving away from stand-alone task automation toward process-oriented orchestration, which may not fit buyers who only want task automation. Per-bot pricing exists but it's usually sold as a platform bundle with a fixed bot allotment, making it hard to scale RPA alone.

### Pegasystems — Challenger
Solution: Pega Robotic Automation (Robot Studio, Robot Runtime, Robot Manager, Robotics Autopilot).

- **Strengths:** Flexible, layered UI targeting — mix and match identification modes at the element level, code injection into supported apps (runs in the app's memory space for fast event-driven interactions), HTML/DOM targeting, accessibility/UI automation, and OCR as fallback. Distinctive market understanding — targets COOs/heads of shared services rather than the CIO, aligning to value drivers like productivity, cost reduction, SLA attainment and operational scale. Strong customer experience (24/7 global support, among the most customer-success programs of evaluated vendors).
- **Cautions:** 2026 roadmap is heavily weighted to AI-assisted automation across the broader platform, with limited, iterative RPA-specific innovation that lags competitors. SMB viability is limited — geared to large enterprises; technical requirements, contract size and lock-in may deter smaller buyers, and commercial practices weigh on sentiment.

### ServiceNow — Visionary
Solution: ServiceNow RPA Hub (RPA Desktop Design Studio, AI Desktop Actions — formerly Agentic Desktop). *ServiceNow did not respond to requests for supplemental information; Gartner's analysis relies on other credible sources.*

- **Strengths:** Intelligent automation via Now Assist (generate automations from text instructions, multiple model providers) plus emerging CU (AI Desktop Actions). Developer-focused — unlike most RPA vendors it targets professional developers, bringing SDLC best practices: built-in source/version control, collaboration tooling, value identification/prioritization, GenAI-assisted development. Strong viability — 8,000+ customer logos, 2,000+ partners.
- **Cautions:** Low RPA visibility — inquiries mostly come from existing ServiceNow (ITSM/LCAP) customers; not marketed as a stand-alone RPA platform, and its RPA-specific ecosystem (bots, connectors, templates) is less developed. Customers report integration challenges with external/legacy systems and slow performance on large datasets.

### SS&C Blue Prism — Visionary
Solutions: SS&C Blue Prism Enterprise, Cloud, and WorkHQ (Capture, Desktop, Design Studio). Global, strong in Europe, North America and Southeast Asian financial centers; top industries are financial services, healthcare, public sector. Roadmap: priority levels for session queuing, broader asset management, natural-language automation development.

- **Strengths:** Robust unattended automation — configurable monitoring and host-level failure detection enable automated restarts and dynamic scaling, with centralized independent queues. Strong market understanding via the Robotic Operating Model 2 (ROM2) framework, a dedicated customer-success function, a reported 94% CSAT and 99% SLA adherence for incident resolution.
- **Cautions:** Declining sales momentum — much lower inquiry/contract activity than prior years, and a higher share of Blue Prism customers evaluating alternatives (citing innovation pace and cost). Slower to GA emerging capabilities — native CU planned for 2H26; lacks out-of-the-box agile PM, native ideation or backlog management. Licensing is costly — minimum 15% support fee atop high base license prices for on-prem, common 3–5 year terms, and scaling cost challenges despite volume discounts.

### EvoluteIQ — Niche Player
Solution: EIQ Platform (EIQ Automation Studio, Workflow Designer, EIQ Enterprise Connectors, EIQ Process Flows). Mostly large-enterprise customers; key markets U.S., U.K., Europe; top industries healthcare, banking, finance, insurance. Roadmap: agentic control plane, next-gen large action model abstracting thousands of actions, unified governance fabric for policies/approvals/lineage.

- **Strengths:** Industry-specific solutions (e.g., autonomous medical coding, care management). Strong RPA-migration capabilities — native import tools and agentic script comprehension to consolidate fragmented RPA estates onto one platform.
- **Cautions:** Sells primarily as an end-to-end process-automation platform, embedding RPA in broader editions rather than as stand-alone RPA — misaligned for buyers wanting simple task-based tools. Small delivery bench (~625 trained/active personnel) may constrain large-scale global rollouts. Edition-based pricing looks simple but can bring surprise costs/forced upgrades when limits are exceeded, plus a 25% premium for 24/7 support (above industry average).

### Laiye — Niche Player
Solution: Laiye Work Execution Platform. Roadmap: multi-agent collaboration platform, more LLM capability in bot task assignment, unified/centralized AI management layer.

- **Strengths:** AI-augmented, AI-native architecture — generate production-ready workflows from natural-language descriptions, with a computer-use agent using visual language models to interact with UI elements. Strong community ecosystem in APAC, especially China (800,000+ developers, per the vendor). Multichannel sales execution (direct, SI partnerships, digital), with partner training, developer academies, certifications and use-case competitions.
- **Cautions:** Older licensing models persist (node-based "binding machine," "floating license"); mostly single-year contracts expose customers to YoY renewal price swings, and several common components are missing from its most-sold base package. Aggressively shifting focus from RPA to agentic automation — existing clients face one-time migration/assessment to adopt new capabilities.

### Samsung SDS — Niche Player
Solution: Brity Automation (Windows Client RPA Designer, RPA Bot, web-based Workflow Builder, Orchestrator, Automation Agent). Operations mainly in South Korea; mostly midsize/large enterprises in APAC; top industries financial/insurance, public sector, manufacturing. Roadmap: efficiency in operations/execution management, CU agents, better asset deployment/sharing across tenants.

- **Strengths:** Strong SMB focus — largest share of sub-1,000-employee customers among evaluated vendors, with tailored support, simplified deployment and accessible pricing that lowers adoption barriers and lets customers scale at their own pace.
- **Cautions:** Limited geographic reach — partner/delivery network concentrated in APAC, minimal presence in North America, Middle East and Africa. Limited RPA innovation/support — development centered on adjacent capabilities, limited direct technical support, no defined plans to grow RPA staff or footprint. Conservative, iterative partner strategy that may not accelerate growth outside core markets.

---

## Vendors Added and Dropped

**Dropped:** IBM, Salesforce, SAP. *(A vendor leaving the MQ often reflects changed market/inclusion criteria or a shift in that vendor's focus, not necessarily a changed opinion of the vendor.)*

## Inclusion Criteria (summary)

To be included, vendors had to, among other things:

- Show a clear, active go-to-market and sales strategy primarily for RPA software (website, Peer Insights, marketing).
- Sell RPA directly to paying customers with at least first-line support (not sold solely for use by the vendor's own consultants); offer a commercially supported enterprise (non-open-source) product.
- Have presence in multiple regions — ≥30 paying RPA customers (unique logos) in each of at least two regions (North America; Latin America; EMEA; APAC incl. Japan/China) as of 31 Jan 2026, with no more than 65% of logos from a single region.
- Report ≥$30M in FY25 RPA software-license revenue (excluding services/consulting/SI support) **and** ≥50% YoY RPA-license revenue growth in FY25.
- Offer native capabilities including: screen scraping with ≥5 UI connectors (e.g., Selenium IDE, Microsoft Active Accessibility, Microsoft UI Automation, Java connector, SAP WinGUI, Windows GUI, mainframe emulator); enterprise IT capabilities (DR, HA, CI/CD, SDLC management, collaboration); both attended and unattended automation; orchestration/administration (central orchestrator required); and bot deployment across desktops, VMs, and public/private clouds.

**Excluded** vendors that lacked screen scraping; offered only PaaS/back-end without a desktop runtime, orchestration, or a front-end IDE; required a specific third-party/white-labeled component for core RPA; or sold RPA only bundled with services for use by their own consultants.

## Evaluation Criteria and Weighting

**Ability to Execute** (how well vendors compete and deliver):

| Criterion | Weight |
|---|---|
| Product or Service | High |
| Overall Viability | Low |
| Sales Execution / Pricing | High |
| Market Responsiveness / Record | Not Rated |
| Marketing Execution | Medium |
| Customer Experience | High |
| Operations | Low |

*Market Responsiveness is not rated — Gartner considers the market mature enough that buyers no longer value rapid direction changes.*

**Completeness of Vision** (vision and strategy):

| Criterion | Weight |
|---|---|
| Market Understanding | Medium |
| Marketing Strategy | Medium |
| Sales Strategy | High |
| Offering (Product) Strategy | Low |
| Business Model | Medium |
| Vertical / Industry Strategy | High |
| Innovation | Medium |
| Geographic Strategy | Medium |

*(Weighting as labeled in the report; where a specific label was ambiguous in the source table, treat as approximate.)*

## Quadrant Definitions (paraphrased)

- **Leaders** understand enterprise needs and where to expand functionality, add AI-augmented capabilities to core RPA, and pair a strong vision with the ability to execute it. A Leader isn't always the best fit for every customer — focused/smaller vendors may offer superior support or specialized capabilities.
- **Challengers** attract a large customer base but are often confined to one part of the market. They typically use RPA to bolster a broader automation platform and upsell RPA to existing customers rather than win new RPA-first logos.
- **Visionaries** are the market's innovators, responding to emerging demands with new opportunities; they appeal to leading-edge customers but haven't yet proven sustained mainstream execution.
- **Niche Players** specialize in specific verticals, functions or geographies (or are moving into RPA from adjacent markets). They can be the best choice for a particular use case — specialized expertise, focused support, flexible terms, lower cost.

## Context

RPA remains the foundation for task automation — bridging legacy-system gaps, orchestrating UI-based workflows and enabling integration where APIs are unavailable. AI, computer vision and agentic automation are reshaping the market toward more complex processes. Buyer priorities evolve: new buyers prize price, ease of development and quick ROI; experienced buyers value analytics, governance and stability.

## Market Overview

- **2025 RPA revenue:** $3.9 billion, up 9.1% YoY.
- RPA endures because there's still no cost-effective, reliable alternative for automating OS-based applications through UI interactions where APIs are missing.

**Three trends shaping the market's future:**

1. **Computer use (CU).** Unlike deterministic RPA, CU is probabilistic and more adaptable at runtime — but currently slow, expensive, inaccurate, and best on web apps (unreliable for OS-based apps and Citrix/RDP). As it improves and cheapens it will significantly disrupt RPA, so all major providers are investing to combine deterministic RPA with CU (predictable fixed-cost UI automation plus dynamic agent-driven automation).
2. **XXL vendors withdrawing from stand-alone RPA.** After seven years of acquisitions to bolster automation portfolios, several megavendors now appear ready to cede the stand-alone RPA market — driven by a focus on AI-agent CU, difficulty running a profitable stand-alone RPA business, and a broader shift toward full automation platforms.
3. **Convergence into BOAT** (Business Orchestration and Automation Technologies). Nearly every vendor here bundles RPA with IDP, LCAP, iPaaS, BPA and agentic automation. Gartner positions UI-based automation as a last resort after API-based integration is exhausted. The risk: buyers who only need RPA may be oversold on full-suite platforms — application leaders should confirm their provider can meet RPA-specific needs without over-buying.

**Current landscape:** The market has matured and consolidated; growth has slowed from 40%+ YoY six years ago. Buyer inquiries have shifted from basic use cases to governance frameworks, ROI metrics, CoE best practices and scaling across departments/geographies. Rapid change makes buyers wary of long-term contracts, favoring flexible terms; price competition has intensified with incentives for high spenders and migration subsidies. Declining-interest topics: attended automation (RDA), citizen development (rarely sustainable/secure without central governance), and security concerns (largely subsided — Gartner has never seen RPA used as an attack vector).

## Acronyms

AI (artificial intelligence) · API (application programming interface) · BPA (business process automation) · CI/CD (continuous integration/continuous delivery) · CU (computer use) · IDP (intelligent document processing) · ITSM (IT service management) · LCAP (low-code application platform) · iPaaS (integration platform as a service) · OS (operating system) · RDA (remote desktop automation) · RDP (Remote Desktop Protocol) · RPA (robotic process automation) · SMB (small and midsize businesses) · UI (user interface).

---

*Source: Gartner, "Magic Quadrant for Robotic Process Automation," 24 June 2026 (G00839318). Summarized/paraphrased for internal use — not for redistribution or verbatim reproduction.*
