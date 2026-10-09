# Agents and RPA POV

**Source:** [[Blueprint_Agents_and_RPA_Point_of_View.pdf]] (2 pages). This file is the text companion; the PDF is the source of truth. If the PDF changes, update this file.
**Topic:** Copilot agents + Power Automate Desktop: PAD flows as agent tools
**Audience:** External (customers, SIs, Microsoft)

---

## Headline

**Your agents need tools. You already have them.**

When RPA and agents come up together, most people picture agents replacing their bots. That sounds appealing if RPA seems brittle, expensive to maintain and old-fashioned. But it misses the bigger opportunity. The fastest way to make agents useful is to let them use the automations you already run: your Power Automate Desktop (PAD) flows, called as agent tools.

## Key messages at a glance

1. An agent without tools can decide, but it can't do.
2. Your PAD flows are proven tools you already own.
3. People use these bots to get work done. Agents can too.
4. Deterministic where it must be right, AI where it can adapt.
5. The agent decides; the flow executes. Right tool, right job.
6. Blueprint turns flows into agent tools: Discover, Decide, Define, Deploy.

## 1. A carpenter with no tools

Picture a newly trained carpenter placed on a home renovation. They know everything about carpentry and can make every right decision, but no one has given them a single tool. Knowledge alone builds nothing. A Copilot agent is in the same position. It can understand a request, reason about it and choose what to do next, but it needs tools to act on the systems where the work happens.

**Comparison (diagram):**

| The common assumption: agents replace the bots | The Blueprint view: agents use the bots as tools |
|---|---|
| Agent → computer use (rebuilt from scratch) → application | Agent → calls an existing PAD flow as a tool → application |
| Rebuilds work that already runs reliably | Reuses automations that are tuned and approved |
| Probabilistic result on every run | Deterministic: done right, every time |
| Model cost on every step of every run | Near-zero cost per run |
| Screens, and the data on them, sent to a model | Runs locally, under existing governance |

**Tagline:** Don't replace your bots with agents. Give your agents your bots.

## 2. Why PAD flows make ideal agent tools

- **You already own them.** Most enterprises have hundreds of RPA automations that have been tuned, vetted and approved, and they're doing real work today. People already use these bots to get work done, so why shouldn't agents?
- **They're deterministic.** Every business has tasks that must be done right, and the same way, every time. The flow runs defined logic; the agent supplies the judgment about when to run it.
- **They reach what APIs can't.** Many legacy applications have no API, and many modern ones lack the methods a process needs. Desktop flows work through the user interface, so agents can reach those systems too.
- **They avoid the gaps in computer use.** Computer use is still immature and slow, costs money on every step, and sends screens to a model. A proven flow has none of those problems.

The result is a hybrid: the agent decides, the flow executes. The right tool for the right job.

## 3. Available today: Discover, Decide, Define, Deploy

Blueprint turns your PAD estate into agent tools in four steps.

1. **Discover (find relevant flows):** AI search runs over functional descriptions Blueprint extracts from each flow's code, so you can find flows that match an agent's responsibilities.
2. **Decide (score suitability):** An agent-suitability score rolls up size, number of arguments, application interactions, hardcoded sensitive values, run history, decision complexity and exception handling. Every subflow and subtree is scored too.
3. **Define (describe the tool):** Blueprint automatically generates the text fields an agent needs to decide when and how to use the tool, including trigger prompts and argument descriptions.
4. **Deploy (connect it):** Pick the Copilot agent from a list and choose the connection reference. Blueprint configures everything, and the agent is ready to use its new tool.

## 4. Coming next (roadmap)

- **Opportunity scanning:** Blueprint scans all your agents and flows in the background and brings you a list of matches: places where existing, relevant, suitable flows could expand or improve an agent. You click to accept.
- **Subflows and subtrees as tools:** The full Discover-to-Deploy process for subflows and subtrees, with automatic extraction into standalone flows. Microsoft plans to let agents call subflows directly, which would remove the need to extract them.
- **New agents from your estate:** Blueprint finds flows that work in the same domain, such as shipping, infers the higher-level process they support, and creates a new agent for it, with description, instructions and flows connected as tools.

**Continuous, not one-time.** Flows, agents, processes and applications all change. Blueprint is designed to run on an ongoing basis, keeping agents matched to the best tools as your estate evolves. This is how we help Microsoft customers move from a history of RPA to a future with agents, building on what already works.

*Roadmap capabilities describe current plans and may change. Microsoft platform plans are subject to Microsoft's own timelines.*
