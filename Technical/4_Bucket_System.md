# 4-Bucket Migration Issue Classification System

## Purpose
Framework for categorizing migration issues to determine root cause and appropriate response.

## The Four Buckets

### 1. Microsoft Limitation (Target Platform Constraint)
**Definition:** Limitations in Power Automate Desktop that Blueprint cannot change

**Customer Positioning:** "Blueprint can't bypass PAD's rules — we ensure your process still runs within those constraints."

**Examples:**
- PAD treats all variables as global → Blueprint prefixes to avoid collisions (MSFT now supports in more recent SDKs, but requires customers to be up to date on PAD)
- PAD requires XML parent nodes, unlike A360
- PAD requires browser scope when launching Chrome as application
- PAD enforces mostly linear workflows vs. non-linear source platforms

### 2. Source Code Differences (Customer-Originated)
**Definition:** Inefficiencies in original bot that get faithfully preserved in migration

**Customer Positioning:** "What you're seeing is exactly what was in your source bot. Blueprint migrates 1:1 so you don't lose functionality. If the source had inefficiencies, those carry over intentionally."

**Examples:**
- All arguments marked as input/output, doubling variables in PAD
- Browser launched as program instead of browser, causing selector mismatches
- Poor scoping or hard-coded assumptions in source logic

**Key Analogies:**
- "Blueprint is like Google Translate for bots. If a sentence had typos in the original, it carries those traits in translation."
- "Blueprint is a mover that moves everything. If a container had extra junk, it all gets shipped. We don't sort or clean."

### 3. Blueprint Enhancement (Our Ongoing Improvements)
**Definition:** Areas where Blueprint could improve handling, requires investigation

**Customer Positioning:** "Some things are in our control, and we're actively optimizing. We'll log this and update you as we improve."

**Examples:**
- Improving detection of Chrome launches for browser scope
- Reducing redundant wrapper subflows in certain conditions
- Known bugs being actively worked (e.g., SAP element migration)

### 4. SI Ineptitude (Human Error/Process Issues)
**Definition:** Issues from Service Integrator technical skill gaps or lack of motivation

**Two Sub-Categories:**

**4a. SI Technical Skill Gaps**
- Don't know PAD capabilities/syntax
- Don't understand source platform (UiPath/Blue Prism/A360)
- Assume generated code won't work because "it's not how I would write it"
- Raise issues about things that actually work fine

**4b. SI Motivation/Process Issues**
- No desire to test tool before raising concerns
- Refuse to try product despite having purchased it
- Want Blueprint to pre-validate every scenario
- Elongate cycles by avoiding hands-on evaluation

**Customer Positioning:**
- "Generated code won't look like hand-written code because it needs to work for many different organizations"
- "Have you tried it? You have the product and paid for it."
- Walk through that product works as designed
- Explain why Blueprint's approach differs from manual coding

**Common Patterns:**
- Show sample bot, ask "how would you migrate?" without attempting
- Assume failure based on code appearance without functional testing
- Object to working functionality because it doesn't match preferred style
- Request pre-sales validation on already-purchased tools

**Mitigation:**
- Direct to existing enablement resources first
- Pattern: Unmotivated SIs rarely become repeat customers
- Acceptance: Some mandated users reluctantly improve over time
- Focus energy on motivated partners

## Application Notes
- Most customer escalations are Bucket 2 (Source Code) or Bucket 4 (SI Issues)
- Bucket 1 issues require Microsoft partnership to resolve
- Bucket 3 requires investigation before committing to fixes
- Bucket 4 issues not solvable through product improvements alone
