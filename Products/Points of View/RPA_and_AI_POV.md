# RPA and AI POV

**Source:** [[Blueprint_RPA_Point_of_View.pdf]] (2 pages). This file is the text companion; the PDF is the source of truth. If the PDF changes, update this file.
**Topic:** RPA & AI: the future of enterprise automation
**Audience:** External (customers, SIs, Microsoft)

---

## Headline

**RPA isn't going away. It's becoming the foundation for enterprise AI automation.**

Every few years someone declares robotic process automation (RPA) obsolete. The latest reasons are API-driven cloud flows and, more recently, GenAI "computer use," where a model reads the screen and decides what to click. Both are real advances, and both belong in a modern automation strategy. But neither one replaces desktop automation. For large enterprises, especially in regulated industries, the reasons matter.

## Key messages at a glance

1. RPA isn't dying. It's becoming the foundation for enterprise AI.
2. Deterministic where it must be right, AI where it can adapt.
3. Agents call flows; they don't replace them.
4. Use AI to build the bot, not to be the bot.
5. Use APIs where they're good; use the UI where they aren't.
6. RPA's old pains are being fixed. Consolidate, govern, modernize.

## 1. APIs are the best option wherever they exist, but they don't reach everything

When an application has a complete, reliable API, a cloud flow is usually the right tool. The problem is coverage. Many of the systems enterprises still depend on have no API at all: mainframe terminals, thick-client applications, apps delivered through Citrix, and homegrown line-of-business tools. Even modern SaaS applications often lack the specific methods a process needs. In those cases the user interface isn't a workaround. It's the only way in, and desktop flows are still essential.

## 2. Computer use is promising, but it isn't ready for critical work

Today computer use works reliably only on simpler interfaces, and it runs far slower than a coded Power Automate Desktop (PAD) flow. It will improve. Still, we believe it will be some time before it matches the speed and reliability of well-built deterministic automation. Some of its limits won't go away as it improves:

- **It's probabilistic.** It gets the task right most of the time, while a deterministic flow does the same thing every time. For steps that must be right, "most of the time" isn't good enough.
- **It costs money every run.** Each step pays for model processing; a coded flow costs almost nothing extra per run, and at thousands of runs a day the gap becomes a major budget item.
- **It's hard to audit.** Deterministic flows give the same result from the same input and can be regression-tested, while model-driven automation can change behavior when the model is updated, even if nobody touched the automation.
- **It exposes data.** Screenshots sent to a model often show personal, financial or health data, raising security and data-residency questions a local desktop flow doesn't.

## 3. The future is hybrid

We believe enterprises will demand hybrid automation, not a choice between old and new. Steps that must succeed every time will stay deterministic, whether in cloud or desktop flows. Parts of a process that benefit from judgment and can tolerate some variation, such as reading unstructured documents, triaging exceptions or interpreting intent, will use GenAI.

**The hybrid model (diagram), three layers:**

- **Where it can adapt:** AI agents & computer use. Probabilistic; handles judgment and variation (unstructured documents, exception triage, interpreting intent, deciding the next step). At design time, AI also helps build the flows.
- **Where it must be right:** Deterministic flows. Same logic, same result, every run; auditable; near-zero cost per run. Cloud flows work through APIs; desktop flows (PAD) work through the UI, governed with Blueprint (standards, control). Agents call these flows as tools.
- **Where the work lives:** Applications with good APIs (modern SaaS and cloud services where the API covers what the process needs), and applications without (enough) API (mainframe, thick clients, Citrix, homegrown tools, and SaaS missing the methods you need).

AI handles the parts of a process that benefit from judgment. It calls deterministic flows for the steps that must be right, and those flows reach every application, whether through its API or its user interface. Blueprint governs the desktop flows.

Agents won't replace flows; they'll call them. A governed library of deterministic flows gives agents dependable tools to act through safely, and Microsoft's own platform direction reflects this. GenAI is also making deterministic automation faster to build, giving you AI productivity at design time and deterministic reliability at run time.

**Tagline:** Use AI to *build* the bot, not to *be* the bot.

## 4. The old pains of RPA are being fixed

The main reason moving off RPA looked attractive was maintenance cost. UI automation was brittle, and selectors broke whenever an application changed. RPA's promise of letting business users ("citizen developers") build their own automations also often came at the cost of engineering discipline, which led to inconsistent standards, weak governance and a lot of rework.

Both problems are now being solved. Microsoft has introduced self-healing selectors that make UI automation more resilient. Blueprint was built to bring rigor, standards and control to PAD development without slowing developers down. The case for abandoning RPA is weaker today than it has ever been.

## 5. What this means for enterprises

Don't rip out your automation estate to chase the next technology. Many organizations run mixed estates across UiPath, Blue Prism and Automation Anywhere. Blueprint migrates those estates to PAD automatically, and consolidating on PAD puts your deterministic automation in the same Microsoft ecosystem as your agents and AI. Govern it, modernize it and hold it to engineering standards. It then becomes the reliable foundation your agentic future is built on.
