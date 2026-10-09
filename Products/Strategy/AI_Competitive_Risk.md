# AI Competitive Risk Assessment for ALC

> **Naming:** "ALC" here means the Maintain and Monitor use cases of the single Blueprint platform (FY2027). See `Company_Overview.md`.

## Verdict
AI poses no meaningful near-to-medium term existential threat to ALC. The primary competitive threat is Microsoft building governance natively into PAD.

## Why AI Is Neutralized Near-Term

RPA is notoriously underdocumented and constantly evolving. Public AI models are trained on public data — which for RPA platform behavioral differences is sparse, outdated, and frequently wrong. Blueprint's real moat is its proprietary corpus of real migration data: thousands of actual bots, real edge cases, real platform behaviors across the world's most complex automation estates. No public model has access to this, and it widens over time.

ALC's most defensible features require longitudinal estate awareness — version history, change impact analysis, dependency tracking over time, compliance drift detection. These require having been embedded in a customer's environment continuously accumulating data. AI cannot replicate this without that foundation.

## The Real Threat: Microsoft

Microsoft building PAD governance natively is more proximate and more dangerous than AI disruption. It would leverage Microsoft's existing distribution, compress Blueprint's differentiation, and eliminate the primary inbound channel simultaneously. The correct defensive response is to get so deeply embedded at shared customers that Blueprint becomes unavoidable infrastructure — which is also why Microsoft's current offer to subsidize ALC year-one should not be deprioritized.

## Long-Term Watch (3-5 Year Horizon)
If AI models improve at ingesting proprietary codebases, ALC's analytical features (documentation, structure mapping) face some compression. The right response is ensuring Blueprint's estate data becomes the foundation that AI is built on top of, not replaced by.

## Update (Oct 2026)
- **AI is now inside the product, deliberately:** The Migration Agent (in development) uses AI only where the deterministic engine stops, grounded in Blueprint's source bot, correlation link, migration reasoning and a machine-derived PAD action reference. ALC already uses generative AI for auto-documentation and AI-generated test cases. See `Migration_Agent_POV.md` and `ALC_Capabilities.md`.
- **Why generic LLMs still fall short for migration:** RPA documentation is incomplete and sometimes wrong, and PAD's own Copilot fails beyond simple flows. See `LLM as RPA Migration Accelerant - Internal Notes.md`.
- **Agent tooling is no longer contrarian:** August 2026 market research found that "agents call proven bots" went from contrarian to consensus between January and August 2026. Every major RPA platform now ships the plumbing, so determinism alone no longer differentiates the AI Agent Tooling bet. The remaining edge is provenance (years of production history) and the estate data. That research and the PRD are in the vault, not this repo.
- **Computer use:** It is competent on short, single-application, web-shaped tasks and far behind on long, multi-app, must-be-identical work. Gartner's 2026 assumption is that computer use becomes a viable alternative for web-based UI automation by 2028 (`2026-RPA-Magic-Quadrant-Digest.md`).
- **Microsoft stays the proximate threat:** Native PAD governance, and a possible unlimited migrate license (`Microsoft_Partnership.md`).
