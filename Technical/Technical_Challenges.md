# Technical Migration Challenges

## Variable Scoping Incompatibility

**Problem:** Power Automate Desktop treats all variables as global; source platforms use limited scope

**Technical Solution:** Prefixed variables mimicking scoped behavior
- **Methodology:** First letter of subflow name + underscore + variable name (e.g., "S_variable_name")
- **Impact:** 100-200% code increase, functionally correct but creates "garbage code"

**Strategic Solution:** Influenced Microsoft to add native variable scoping to roadmap

## Linearity Constraints (GoTo Implementation)

**Problem:** PAD enforced linear workflows; Blue Prism/UiPath support non-linear flows

**Customer Impact:** Made migrations unusable for jump-between-blocks patterns

**Solution:** Worked with Microsoft to add flexible "goto" actions to roadmap

**Business Case:** Without flexibility, customers would rebuild from scratch vs. migrate

## File Copy Action Optimization

**Problem:** A360 file copy migrating to 50+ lines of PAD code

**Root Cause:** A360 allows file/folder copy with overwrite, PAD only folder copy

**Solution:** Created reusable subflow function with argument parsing
- **Logic:** Check file extension → if no extension (folder) use native PAD → if extension exists, create in temp then move

## Selector Types Migration

**Problem:** PAD only supports AA and UIA selectors; UiPath supports multiple types (strict, fuzzy, anchor, image, AA)

**Solution:** Three-tiered selector approach leveraging PAD's sequential testing
- **First:** Verbatim from source tool
- **Second:** Removed class attributes, kept top/bottom UI elements
- **Third:** Only target element as fallback

## Unsupported Features in Power Automate

**Problem:** Missing native constructs (queues, reusable components, custom code)

**Blueprint Solution:** Rules Engine enables custom mappings and reusable components

**Value:** Provides capabilities Microsoft hasn't built yet

## Enterprise Adoption Challenges

### Risk Aversion
**Challenge:** "Why risk breaking what already works?"

**Blueprint Approach:** Position tools as optional accelerators, not forced changes. Show value in incremental adoption.

### On-Prem vs. Cloud Requirements
**Reality:** Enterprises (HSBC) demand on-prem initially due to security reviews

**Strategy:** Start on-prem with migration path to hosted services later

### Customer Support Intensity
**Challenge:** Large enterprises (MetLife) attempting migration without SIs require more handholding

**Solution:** Increase Customer Success involvement, classroom training, presales prep

**Recognition:** SI-free enterprise migrations need different support model
