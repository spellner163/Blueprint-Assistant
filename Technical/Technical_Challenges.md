# Technical Migration Challenges

## Variable Scoping Incompatibility

**Problem:** Power Automate Desktop treats all variables as global; source platforms use limited scope

**Technical Solution:** Prefixed variables mimicking scoped behavior
- **Methodology:** First letter of subflow name + underscore + variable name (e.g., "S_variable_name")
- **Impact:** 100-200% code increase, functionally correct but creates "garbage code"

**Strategic Solution:** Influenced Microsoft to add native variable scoping. It was released in January 2026, so customers on an up-to-date PAD can now choose local variables at conversion (`Automated_Migration_POV.md`). Customer adoption is still pending, and the prefix approach remains for customers who are not up to date.

## Linearity Constraints (GoTo Implementation)

**Problem:** PAD enforced linear workflows; Blue Prism/UiPath support non-linear flows

**Customer Impact:** Made migrations unusable for jump-between-blocks patterns

**Solution:** Worked with Microsoft to add flexible "goto" actions. A Go To action now exists in PAD, but it only works within the same subflow (cross-subflow jumps are impossible, and Microsoft's documentation does not say so).

**Remaining limits:** Nonlinear and cyclical Blue Prism flows (hook/try-catch blocks, forward GoTos) are still hard to show and correlate; see `Research/Correlator.md`.

**Business Case:** Without flexibility, customers would rebuild from scratch vs. migrate

## File Copy Action Optimization

**Problem:** A360 file copy migrating to 50+ lines of PAD code

**Root Cause:** A360 allows file/folder copy with overwrite, PAD only folder copy

**Solution:** Created reusable subflow function with argument parsing
- **Logic:** Check file extension → if no extension (folder) use native PAD → if extension exists, create in temp then move

## Selector Types Migration

**Problem:** PAD supports fewer selector types than UiPath (strict, fuzzy, anchor, image, AA). Selector conversion has historically been the hardest part of any migration.

**Solution:** Three-tiered selector approach leveraging PAD's sequential testing, with fallback selectors created automatically
- **First:** Verbatim from source tool
- **Second:** Removed class attributes, kept top/bottom UI elements
- **Third:** Only target element as fallback

**Current state (`Automated_Migration_POV.md`):** Blueprint converts UIA, MSAA, variable-based, image, anchor and SAP selectors. Some selectors still need a developer, and the selector report shows exactly which ones so they can be included in estimates up front. Microsoft has also added self-healing selectors in PAD.

## Unsupported Features in Power Automate

**Problem:** Missing native constructs (queues, reusable components, custom code)

**Blueprint Solution:** Rules enable custom mappings and reusable components (e.g., Reuse creates an external desktop flow for a shared sub-process). Enabled rules apply automatically to all future migrations; see `Migrator_Capabilities.md`.

**Value:** Provides capabilities Microsoft hasn't built yet

## Enterprise Adoption Challenges

### Risk Aversion
**Challenge:** "Why risk breaking what already works?"

**Blueprint Approach:** Position tools as optional accelerators, not forced changes. Show value in incremental adoption.

### On-Prem vs. Cloud Requirements
**Reality:** Enterprises (HSBC) ask for on-prem initially due to security reviews

**Strategy:** Blueprint is cloud-hosted SaaS. On-prem is available only for sufficiently large deals and is strongly discouraged; Blueprint prefers cloud. Treat on-prem as an exception, not the default path.

### Customer Support Intensity
**Challenge:** Large enterprises (MetLife) attempting migration without SIs require more handholding

**Solution:** Increase Customer Success involvement, classroom training, presales prep

**Recognition:** SI-free enterprise migrations need different support model
