# Blueprint Context Index

## Purpose
Entry point for Blueprint project context. Read this first, then load relevant documents based on conversation topic.

## Prerequisites (Always Load)
1. `Company_Overview.md` - Products, business model, team
2. `Sean_Role_Context.md` - Role, stakeholders, working preferences

## Document Directory

### Technical/
| Document | Load When |
|----------|-----------|
| `4_Bucket_System.md` | Troubleshooting migration issues, customer escalations, categorizing reported problems |
| `Platform_Architecture.md` | Infrastructure questions, deployment decisions, COM architecture, system design |
| `Technical_Challenges.md` | Variable scoping, workflow linearity, platform gaps, major migration blockers |

### Partnerships/
| Document | Load When |
|----------|-----------|
| `Microsoft_Partnership.md` | Microsoft collaboration, API gaps, roadmap influence, SDK limitations |
| `SI_Challenges.md` | SI partner issues, enablement strategy, skill gaps, motivation problems |

### Partners_Customers/
| Document | Load When |
|----------|-----------|
| `Aubay.md` | Any conversation referencing Aubay, their escalations, or their migration engagement |
| *(Add new customer files as engagements develop)* | |

**Structure:** One file per customer/SI partner. Static context (contacts, platform, enablement status, competency assessment) at the top. Timestamped updates in reverse chronological order below. Load the relevant customer file whenever a specific customer or SI is mentioned by name, or when discussing a customer escalation that may have prior history.

### Products/
| Document | Load When |
|----------|-----------|
| `ALC_Strategy_and_PMF.md` | Any discussion about ALC/Blueprint Control strategy, product-market fit, the early adopter program, Martin's Blueprint Control deck, ICP/pricing, ARR projections, or the standalone GTM question |
| `AI_Competitive_Risk.md` | Any discussion about AI as a competitive threat to Blueprint, AI's impact on RPA migration or lifecycle management, or long-term product defensibility |

### Hiring/
| Document | Load When |
|----------|-----------|
| `TES_Hiring.md` | Interviewing for Technical Enablement Specialist |
| `GTM_Hiring.md` | Interviewing for GTM/marketing role |
| `Interview_Practices.md` | Preparing for any interview, evaluation frameworks |
| `Candidate_Evaluations.md` | Referencing past candidates or writing feedback |

## Quick Routing Guide
**Customer escalation or bug report?** → Load `4_Bucket_System.md` + relevant `Partners_Customers/` file if customer is known

**Technical architecture question?** → Load `Platform_Architecture.md`

**Microsoft API or roadmap discussion?** → Load `Microsoft_Partnership.md`

**SI partner not engaging properly?** → Load `SI_Challenges.md` + relevant `Partners_Customers/` file

**Major technical blockers in migration?** → Load `Technical_Challenges.md`

**ALC strategy, PMF, Blueprint Control discussion?** → Load `ALC_Strategy_and_PMF.md`

**AI competitive threat or long-term product defensibility?** → Load `AI_Competitive_Risk.md`

**Interviewing candidates?** → Load relevant Hiring/ document + `Interview_Practices.md`

**Discussion about a specific customer/SI?** → Load their `Partners_Customers/` file for history and context
