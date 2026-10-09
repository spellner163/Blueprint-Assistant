# Blueprint Context Index

## Purpose
Entry point for Blueprint project context. Read this first, then load relevant documents based on conversation topic.

**Naming:** From FY2027 Blueprint is one platform with three use cases (Maintain, Monitor, Modernize). Older files still say Migrator, ALC, or Blueprint Control. Read those as Modernize and Maintain/Monitor. See `Company_Overview.md`.

## Prerequisites (Always Load)
1. `Prerequisites/Company_Overview.md` - Product, pricing, business model, team
2. `Prerequisites/Sean_Role_Context.md` - Role, stakeholders, working preferences

## Document Directory

### Technical/
| Document | Load When |
|----------|-----------|
| `4_Bucket_System.md` | Troubleshooting migration issues, customer escalations, categorizing reported problems. Also load the relevant `Partners_Customers/` file if the customer is known (`On Going Projects/` for active, `Project Retrospectives/` for completed). |
| `Platform_Architecture.md` | Infrastructure questions, deployment decisions, COM architecture, system design |
| `Technical_Challenges.md` | Variable scoping, workflow linearity, selectors, platform gaps, major migration blockers |

### Partnerships/
| Document | Load When |
|----------|-----------|
| `Microsoft_Partnership.md` | Microsoft collaboration, API gaps, roadmap influence, SDK limitations, anchor comments, the unlimited-license possibility |
| `SI_Challenges.md` | SI partner issues, enablement strategy, skill gaps, motivation problems. Also load the relevant `Partners_Customers/` file for that SI's history. |

### Partners_Customers/Project Retrospectives/
| Document | Load When |
|----------|-----------|
| `UST_Schroders.md` | Any conversation referencing UST, Schroders, Remya, or their Blue Prism → PAD migration engagement |
| `Aubay.md` | Any conversation referencing Aubay, their escalations, or their migration engagement. Last logged update was 2025-02-13 mid-escalation with no resolution recorded; confirm current status if it resurfaces. |

**Structure:** One file per customer/SI partner. Active engagements live in `On Going Projects/`; completed engagements move to `Project Retrospectives/`. Static context at the top, timestamped updates in reverse chronological order below. Load the relevant customer file whenever a specific customer or SI is mentioned by name, or when discussing a customer escalation, feedback, or prior history.

`On Going Projects/` (Optum / UHG, with Cognizant as the SI) is kept in the vault as HTML and is not in this repo yet.

### Products/Current Product Capabilities/
| Document | Load When |
|----------|-----------|
| `Migrator_Capabilities.md` | What Modernize/Migrator does, how it works, features, licensing, supported platforms, migration philosophy, the Estimator, Rules, COM, export options |
| `ALC_Capabilities.md` | What Maintain/Monitor (ALC) does at a feature level: navigation, environment connections, PAD-only features. Not for GTM strategy or pricing; use `ALC_Strategy_and_PMF.md` for that. |

### Products/Strategy/
| Document | Load When |
|----------|-----------|
| `ALC_Strategy_and_PMF.md` | Why ALC exists, who it's for, GTM motion, ICP, early adopter program, product-market fit. Note the update block at the top: pricing and sales-model sections are superseded by the FY2027 pivot. |
| `AI_Competitive_Risk.md` | AI as a competitive threat, AI's impact on RPA migration or lifecycle management, long-term defensibility |
| `Product_Roadmap.md` | The 2026 roadmap, quarterly priorities, the Correlator and AI Agent Tooling initiatives, and the FY2027 single-platform pivot and pricing (source of record). Load alongside `ALC_Strategy_and_PMF.md` and `AI_Competitive_Risk.md` as needed. |
| `2026-RPA-Magic-Quadrant-Digest.md` | The competitive RPA vendor landscape, market sizing, computer use (CU) and BOAT convergence |
| `LLM as RPA Migration Accelerant - Internal Notes.md` | Whether LLMs can accelerate RPA migration code generation, partner/customer pressure for AI-assisted migration, why Blueprint's approach differs |

### Products/Research/
| Document | Load When |
|----------|-----------|
| `ALC Features for Buyers.md` | Articulating specific Maintain/Monitor features to buyers: compliance drift detection, outcome monitoring, estate visibility. Not for pricing. |
| `Correlator.md` | The Static Correlator: mapping migrated PAD actions to their source origin and back. Problem, rationale, V1 vs. later scope, open design questions. |

### Products/Points of View/
Two-page POVs: the approved way to position key themes and features. The PDF is the source of truth (vault only); each `.md` is the text companion. Load the `.md`.

| Document | Load When |
|----------|-----------|
| `Automated_Migration_POV.md` | Positioning migration: manual rewrite vs. automated conversion, headline figures (70–75% less effort, 95–99% of actions converted, 200+ estates, 21M+ PAD actions), plan–migrate–govern. **Source of record for migration claims.** |
| `Agents_and_RPA_POV.md` | PAD flows as Copilot agent tools; Discover/Decide/Define/Deploy. Load alongside `Product_Roadmap.md`. |
| `RPA_and_AI_POV.md` | RPA's future relative to APIs, computer use and GenAI; "use AI to build the bot, not to be the bot." Load alongside `AI_Competitive_Risk.md`. |
| `PAD_Governance_POV.md` | Governance for PAD at scale; the Maintain/Monitor/Modernize feature map; Business Outcome Monitoring. Load alongside `ALC_Capabilities.md`. |
| `Migration_Agent_POV.md` | The Migration Agent inside the Correlator. Internal (September 2026). Includes Tony's final wording decisions; respect them in future edits. Load alongside `Research/Correlator.md`. |

### Context/
| Document | Load When |
|----------|-----------|
| `RPA-to-PAD-Migration-Services-Pricing-Public-Research.md` | Migration pricing strategy, benchmarking against market day rates, building a pricing argument |
| `Services-Project-Schedule-Overrun-Evidence.md` | Why tool-led migration beats services-led rebuilds, timeline-overrun statistics, migration-risk sales messaging |

### Hiring/ (closed for now)
Hiring is closed. Do not load these unless hiring reopens or Sean asks about a past candidate.

| Document | Load When |
|----------|-----------|
| `TES_Hiring.md` | Interviewing for Technical Enablement Specialist |
| `GTM_Hiring.md` | Interviewing for a GTM/marketing role |
| `Interview_Practices.md` | Preparing for any interview, evaluation frameworks |
| `Candidate_Evaluations.md` | Referencing past candidates or writing feedback |

### Vault-only (not in this repo)
These are in Sean's Obsidian vault. Ask for them if needed:
- `Migration Review Kit/` (the `/migration-review` command, `pad_skeleton.py`, `optum_rewrite.py`)
- `Partners_Customers/On Going Projects/` (Optum PAD Framework and Framework Comparison, HTML)
- `Products/`: BOM requirements spec, epic and prototype; the REFramework migration review (internal only); POV PDFs; Migration Agent POV v2 HTML and logo
- `Ideas/`: AI Agent Tooling, Anomaly Detection, Embedded Delivery Expert
- `assets/` (mockups, slides) and `skills/` (deliverables, Jira tickets, leadership briefing, customer tracker)

## Quick Routing Guide
**Customer escalation or bug report?** → `4_Bucket_System.md` + relevant `Partners_Customers/` file if the customer is known

**Technical architecture question?** → `Platform_Architecture.md`

**Microsoft API or roadmap discussion?** → `Microsoft_Partnership.md`

**SI partner not engaging properly?** → `SI_Challenges.md` + relevant `Partners_Customers/` file

**Major technical blockers in migration?** → `Technical_Challenges.md`

**What does the product do, or how do I explain it?** → `Migrator_Capabilities.md` and/or `ALC_Capabilities.md`, plus the relevant POV

**Pricing, packaging, FY2027 pivot?** → `Company_Overview.md`, then `Product_Roadmap.md`

**ALC strategy, PMF, standalone GTM?** → `ALC_Strategy_and_PMF.md` (+ `Product_Roadmap.md`)

**AI competitive threat or defensibility?** → `AI_Competitive_Risk.md`

**Partner asks for LLM-assisted migration?** → `LLM as RPA Migration Accelerant - Internal Notes.md`

**Correlator or Migration Agent?** → `Research/Correlator.md` + `Migration_Agent_POV.md`

**Discussion about a specific customer/SI?** → their `Partners_Customers/` file for history and context
