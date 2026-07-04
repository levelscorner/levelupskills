---
name: technology-adoption-research
description: Use when the user asks whether a programming language, framework, platform, protocol, database, toolchain, or engineering approach is gaining or losing adoption, whether enterprises are likely to accept it, why the market is shifting, what the real decision criteria are, or what happens if a team adopts or ignores a technology trend. Also use for developer ecosystem research, programming language adoption analysis, platform/tooling trend analysis, and enterprise technology strategy research.
version: 1.0.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [research, strategy, technology-adoption, enterprise, ecosystems, languages, frameworks]
    related_skills: [deep-research, strategic-research-briefs]
---

# Technology Adoption Research

## Overview

Use this skill to analyze whether a technology is actually gaining traction, who is adopting it, why adoption is happening, what the constraints are, and whether the change is relevant to the user's business or product. The goal is not to repeat hype. The goal is to separate narrative from real adoption signals and convert that into an actionable recommendation.

This skill is for questions such as:
- "Are companies moving from X to Y?"
- "Will enterprises reject our stack?"
- "Is this technology becoming standard or is it still niche?"
- "Why are developers switching to this tool/framework/language?"
- "What happens if we do not adopt this?"

## When to Use

Use this skill when the user asks about:
- adoption of programming languages, frameworks, databases, protocols, platforms, cloud tooling, or developer tools
- market perception of a technology choice
- whether a stack will create enterprise-sales friction
- long-term viability of an engineering choice
- ecosystem momentum, talent pool, support, standardization, or buyer acceptance
- broad technology strategy questions that are not only about AI agents

Do not use this skill when the task is mostly about implementing code or debugging a technical issue. This is a strategy-and-research skill.

## Core Principles

1. **Adoption is multi-layered.** Distinguish between hobbyist excitement, open-source mindshare, startup usage, enterprise pilots, and production standardization.
2. **Vendor support matters.** Official SDKs, docs, integrations, and first-party support are stronger signals than social-media hype.
3. **Enterprise acceptance is not just language preference.** Integration, security, observability, deployment model, procurement comfort, and team familiarity often matter more than syntax.
4. **Do not confuse usage with suitability.** A popular tool may still be wrong for the user's context.
5. **Always analyze the downside of inaction.** Explain what happens if the proposed adoption does not occur or if the current approach is retained.


## Always cover

- adoption signals versus hype
- enterprise fit and buyer interpretation
- ecosystem and vendor support
- migration cost and downside of inaction
- what matters now versus later

## Workflow

### 1. Frame the exact decision
Identify what is actually being decided:
- language choice?
- framework choice?
- enterprise positioning risk?
- ecosystem timing?
- migration necessity versus optionality?

Restate the decision in one sentence internally before researching.

### 2. Separate the stack layers
Do not treat an entire stack as one blob. Break it into layers such as:
- language/runtime
- framework/orchestration
- SDK/vendor support
- deployment/runtime infra
- governance/observability/security
- buyer/integration expectations

Many arguments that look like "language adoption" are actually about a different layer.

### 3. Gather evidence from multiple signal types
Prefer a mix of:
- official docs
- official SDK repos
- vendor release notes
- GitHub repos and activity
- major framework docs
- Stack Overflow / industry surveys for broad language usage
- engineering blogs or architecture posts from real companies
- cloud/platform integrations

Do not rely on one viral claim.

### 4. Evaluate using these dimensions
For each technology or option, score qualitatively:
- current adoption
- momentum
- enterprise fit
- ecosystem depth
- hiring/talent availability
- vendor support
- operational maturity
- portability / lock-in risk
- migration cost
- consequences of not choosing it

### 5. Distinguish these outcomes explicitly
Use one of these labels for each candidate:
- **Leading default**
- **Rising strongly**
- **Solid but niche**
- **Important in specific environments**
- **Overhyped relative to real adoption**
- **Too early to matter for most teams**

### 6. Translate to the user's business reality
Always answer:
- Does this create enterprise-sales friction?
- Does this slow hiring or integration?
- Does this create strategic risk?
- Is the current stack still defendable?
- Under what conditions should the user revisit the decision?

## Output format

Start with a short verdict section:
- what is true now
- what is overblown
- what matters to the user's decision

Then provide:
1. **Current state**
2. **Why adoption is or is not happening**
3. **Enterprise/buyer interpretation**
4. **Risk if the user does nothing**
5. **Final recommendation**

When useful, include a compact table:

| Option | Adoption | Enterprise fit | Main strength | Main risk |
|---|---|---|---|---|

End with a direct recommendation, not just analysis.

## Required Questions to Answer Internally

Before finalizing, make sure you can answer:
- Is this a real adoption trend or mostly narrative?
- Which layer is actually changing?
- Who is adopting it: hobbyists, startups, or enterprises?
- What would a buyer actually care about here?
- What happens if the user keeps the current stack?
- What proof would force a recommendation change in 6-12 months?

## Common Pitfalls

1. **Equating GitHub hype with enterprise adoption.** Stars are signals, not proof.
2. **Missing layer confusion.** A framework shift can be mistaken for a language shift.
3. **Ignoring official support.** Vendor SDKs and docs are concrete evidence.
4. **Forgetting the negative case.** Always explain the cost of not adopting.
5. **Answering like a trend reporter instead of a strategist.** Tie conclusions back to the user's decision.
6. **Over-penalizing non-enterprise languages.** Enterprises buy outcomes, integration, and risk management, not just Java/C# comfort.

## Verification Checklist

- [ ] I separated hype from real adoption signals.
- [ ] I distinguished stack layers instead of flattening them.
- [ ] I considered enterprise acceptance separately from developer excitement.
- [ ] I included downside analysis if the user does not adopt the trend.
- [ ] I gave a final recommendation with a clear verdict.
