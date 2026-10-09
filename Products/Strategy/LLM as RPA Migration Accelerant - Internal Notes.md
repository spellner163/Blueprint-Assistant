# LLM as RPA Migration Accelerant — Why It Doesn't Work
*Internal notes — April 2026*

---

## The Core Problem

LLMs are fundamentally documentation-bound. To generate valid code or logic, they need accurate, complete documentation about the tool they're targeting. RPA platforms — Power Automate, UiPath, Automation Anywhere, and the rest — are notoriously underdocumented, and what documentation exists frequently omits the constraints and edge cases that actually matter in practice.

This creates a compounding failure: the AI confidently suggests solutions that look syntactically valid but are architecturally impossible. You don't know they're wrong until you try to build them.

---

## Problem 1: RPA Isn't a Normal Programming Language

LLMs are trained extensively on programming languages, and they're reasonably good at generating code. But RPA isn't just code — it's a visual, action-based execution model that needs to compile into UI-representable steps the platform can actually execute. Even when a platform uses .NET, C#, or a proprietary scripting language under the hood, the surface layer the developer works in has its own constraints that aren't captured in general programming training data.

The AI doesn't understand what's possible in the execution environment — it understands what looks correct to a language model.

---

## Problem 2: Documentation Is Inaccurate, Not Just Incomplete

The documentation problem is worse than "missing constraints." RPA platform documentation fails in three distinct ways:

1. **It omits what actions can't do.** The Go To action in Power Automate Desktop is an example: it only works within the same subflow, but Microsoft's documentation doesn't state this.  
	On Mar 9, 2026, I troubleshooted this issue using Perplexity and selecting NVIDIA’s “Nemotron 3 Super” modal. It recommend cross-subflow Go To jumps — which are completely impossible — with full confidence.
2. **It sometimes omits what actions *can* do.** Functionality is occasionally wider than documented, meaning both developers and LLMs miss valid approaches because the documentation undersells the action.

3. **It is sometimes affirmatively wrong.** When documentation inaccurately describes behavior, an LLM trained on it doesn't generate incomplete suggestions — it generates confidently incorrect ones. This is the worst failure mode because there's no signal that something is wrong until you build it and it breaks.

Community resources and blog posts exist, but these are a different category than official documentation. Any software developer knows the experience of following a community-suggested fix that worked for someone else and doesn't work for you. LLMs often can't distinguish between "this is documented behavior" and "this is a workaround someone posted that may or may not generalize." Official documentation is the most reliable training signal, and for RPA platforms, it's a weak link in the chain.

---

## Problem 3: Acceleration Becomes Deceleration

The intuition that LLM assistance would speed up migration assumes that suggestions are mostly correct and occasionally need tweaking. In practice, with RPA:

- The suggestion success rate is low enough that every output requires careful validation
- Validating an impossible suggestion often requires attempting to build it, hitting a wall, debugging why it fails, and then starting over with a correct approach
- The net effect is that the developer spends *more* time than if they had designed the solution from scratch, because they're now debugging an incorrect premise instead of building from a known-good one

---

## Problem 4: The User Trust Risk

Blueprint already faces friction where users will escalate over minor imperfections — small behavioral differences, minor inefficiencies, anything that falls short of the source automation's behavior. This is true even when those differences represent minimal real-world impact.

If Blueprint were to integrate an LLM assistant that recommended impossible or incorrect implementations, users would inevitably encounter those suggestions, attempt to implement them, fail, and likely attribute the failure to Blueprint. The reputational downside is asymmetric: users don't credit AI-assisted suggestions when they work, but they would likely hold Blueprint accountable when they don't.

Baking an unreliable suggestion layer into the product would likely accelerate escalations, not reduce them.

**The Microsoft Copilot data point.** Power Automate Desktop ships with a first-party Copilot built by the team that wrote the platform. They have the source code, the constraint documentation, and the full internal knowledge base. Even with all of that, their own Copilot fails to produce correct output for anything beyond simple flow structures. If Microsoft can't make an in-product LLM work reliably for PAD with perfect platform knowledge, the premise that a third-party LLM with access to public documentation would do meaningfully better is not credible. 

---

## The Structural Argument

The partner's pressure is understandable — LLMs have genuinely accelerated software development in many contexts, and it's reasonable to ask whether that applies here. But RPA migration is a domain where the usual conditions for LLM usefulness don't hold:

| Condition for LLM Usefulness                           | Status in RPA Migration                                        |
| ------------------------------------------------------ | -------------------------------------------------------------- |
| Accurate, complete documentation of target environment | ❌ RPA docs are incomplete and inconsistent                     |
| Standard programming constructs                        | ❌ Visual/action model with hidden constraints                  |
| Errors are fast to detect and correct                  | ❌ Invalid suggestions require build-and-fail cycles            |
| High suggestion hit rate                               | ❌ Hallucination of impossible implementations is common        |
| Output is independently verifiable                     | ⚠️ Requires deep PAD knowledge to validate                     |
| In-product AI by the platform vendor works             | ❌ PAD's own Copilot fails on anything beyond simple structures |

Some LLM research touts productivity gains in RPA contexts, but on closer inspection these gains are about *extending* existing automations — handling unstructured data, adding cognitive capabilities on top of working flows. That is a different thing from using LLMs to generate net new RPA migration code. The research doesn't map onto the migration use case, and it tends not to specify which RPA platforms were tested, which matters enormously given how differently these platforms behave.

The places where LLMs do add genuine value in migration work — parsing source automations for intent, summarizing business logic, generating specs — are useful precisely because they don't involve generating RPA flow code. Those applications don't require the LLM to know what PAD can and can't do. The moment you cross into code generation, the documentation problem becomes a problem.

---

# What Would It Actually Take?

Working backwards from the problems above, there are four distinct layers that would need to exist for an LLM migration assistant to be reliable.

**1. A proprietary constraint database**

The documentation problem can't be solved by pointing an LLM at better documentation, because the documentation doesn't exist. Someone has to create it. Blueprint would need to build and maintain a ground-truth knowledge base for each platform — not just what each action does, but what it can't do, what its interactions with other actions produce, what breaks across version updates, and what practitioners have discovered through trial and error. This has to be validated through systematic testing, not written from memory or inference. It requires ongoing maintenance every time a platform releases an update.

This is also exactly the kind of knowledge Blueprint already has in the heads of its practitioners. The question is whether it can be extracted, structured, and kept current at scale.

**2. A formal action vocabulary**

The reason in-product Copilots partially work for simple structures is that simple structures involve a small, well-defined action set with predictable behavior. For an LLM to generate reliably correct complex flows, it needs something like an API spec — a formal, machine-readable description of each action, its valid parameters, its constraints, its known interactions with other actions, and its version-specific quirks. This constrains the model's output space in the same way type systems constrain code. Suggestions that violate the schema are never generated in the first place.

**3. A validation layer before surfacing suggestions**

Even with good grounding, the "fails late" problem doesn't go away entirely. An LLM can know a constraint and still violate it in complex multi-step logic. The fix is a validation pass between generation and surfacing — something that checks the suggestion against the constraint database before the developer sees it. This is analogous to a linter or type checker: it doesn't guarantee correctness, but it catches the class of errors that are rule-based and verifiable without execution.

**4. A feedback loop from real migration work**

The way models like GitHub Copilot improved was through massive real-world signal — millions of completions, accepted or rejected, feeding back into what the model treats as correct. Blueprint has something analogous at a smaller scale: a body of migration work that represents a dataset of correct implementations. Over time, accepted and rejected suggestions could reinforce the model's sense of what actually works in practice. This is what turns a static knowledge base into something that improves.

**The honest cost**

The pieces above aren't technically exotic — RAG grounded in a proprietary knowledge base, a formal action vocabulary, a validation layer, and a feedback loop are all established patterns. The cost is in the knowledge work, not the engineering. Building and validating a constraint database across multiple RPA platforms, keeping it current across version updates, and doing it rigorously enough to trust the output is a significant ongoing investment. The risk is that platforms evolve faster than the knowledge base can keep up — which is what makes Microsoft's position so telling. They own PAD and still can't do this reliably with their own Copilot.

What Blueprint would be building is essentially the thing that should exist as official documentation but doesn't. That's a real moat if executed well, because it's not something a third-party LLM provider can replicate without the same practitioner investment. But it's also a maintenance burden that never goes away.

The key question for any partner conversation: who funds the knowledge base work? That's the actual cost center, and the answer to that question determines whether this is a genuine roadmap item or a theoretical possibility.

---

# Bottom Line

LLMs aren't a useful accelerant for RPA migration because the thing that makes them powerful (pattern completion against training data) breaks down when the training data doesn't capture the actual constraints of the execution environment. The result isn't acceleration — it's a confidence-weighted source of wrong answers that slows skilled practitioners down and creates product trust risk if surfaced to end users.

The specific failure mode in RPA is also more expensive than in other domains. In standard software development, a wrong suggestion fails fast — it doesn't compile, tests break. In RPA, an invalid suggestion can look completely valid, get partially built, and only fail when you hit the actual constraint in execution. By that point you've invested real build time in a dead end. That asymmetry is what makes LLM-assisted RPA code generation uniquely counterproductive rather than just occasionally wrong.

Blueprint's value is in converting practitioner knowledge into reliable, validated, automated migration. That's not something you can shortcut with a model that doesn't know what Go To can and can't do — and that Microsoft's own Copilot, with full platform knowledge, also can't reliably do.
