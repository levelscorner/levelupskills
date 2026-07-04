---
name: technology-adoption-research
description: Use when the user asks whether a programming language, framework, platform, protocol, database, toolchain, or engineering approach is gaining or losing adoption, whether enterprise adoption is credible, whether something is hype or durable, or how to compare technology trajectories. Also use when the user needs a research-driven adoption verdict rather than anecdotal hot takes.
version: 1.1.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [research, technology-adoption, ecosystem-analysis, trend-analysis, enterprise-software]
    related_skills: [agentic-stack-research, strategic-research-briefs, deep-research]
---

# Technology Adoption Research

## Overview
Use this skill when the user wants a grounded judgment about whether a technology is actually gaining adoption, losing momentum, or merely being discussed loudly online.

This skill is for **technology adoption reality-testing**, not fandom, not hype amplification, and not one-source takes.

## When to Use
Use this skill when the user's core question is about **trajectory**:
- Is this language / framework / platform really growing?
- Are companies actually adopting it?
- Is this just hype or a real shift?
- Will this likely matter in 1 to 3 years?
- Is it risky to ignore this trend?
- Is this ecosystem durable enough to bet on?

Typical trigger classes:
- programming languages
- web / backend / infra frameworks
- AI / ML tools and platforms
- developer toolchains
- cloud / data / database systems
- enterprise engineering patterns

Do **not** use this skill when:
- the task is about choosing an agent stack specifically → use `agentic-stack-research`
- the task is general business strategy without technology-adoption analysis
- the user only wants a shallow opinion with no evidence

## Core Principles
1. **Adoption is not attention.** Talk, stars, and social chatter are weak evidence by themselves.
2. **Enterprise credibility is different from developer excitement.** Separate experimentation from production standardization.
3. **Trajectory matters more than isolated datapoints.** Look for sustained movement, not a viral month.
4. **Negative analysis is required.** Always ask what happens if the user ignores or delays the shift.
5. **A verdict is required.** End with a clear judgment, not only a pile of observations.

## Always cover
- what the technology is and where it fits
- evidence of real adoption versus surface attention
- ecosystem maturity
- enterprise credibility
- talent / hiring / learning curve implications
- operational / migration risk
- downside of ignoring it

## Workflow
1. Define the technology precisely and identify what adjacent alternatives it competes with.
2. Gather signals across multiple evidence classes: official docs, vendor/user adoption, ecosystem depth, community activity, jobs, tooling maturity, and migration stories.
3. Separate hype signals from production signals.
4. Evaluate the adoption curve: emerging, rising, plateauing, fragmenting, or declining.
5. Assess enterprise viability, talent availability, and operational risk.
6. State the downside of omission: what happens if the user does nothing.
7. End with a direct verdict and recommendation.

## Output format
Return the answer in this structure:
1. **What it is**
2. **Adoption signals**
3. **What looks real vs what looks hype-driven**
4. **Enterprise / production credibility**
5. **Risks, limits, and downside of ignoring it**
6. **Verdict**

## Required Questions to Answer Internally
Before finalizing, answer these internally:
- Am I mistaking discussion for deployment?
- Do I have official-source or implementation-source evidence?
- Did I separate individual developer enthusiasm from company adoption?
- Did I include the cost of ignoring the shift?
- Did I end with a clear call?

## Common Pitfalls
1. **Using GitHub stars as primary proof.** Stars are interest, not necessarily adoption.
2. **Mistaking strong advocates for broad consensus.** Loud communities can distort perceived reality.
3. **Ignoring migration friction.** Good technologies still fail in adoption if the switch cost is too high.
4. **Over-rotating on one vendor's marketing.** Vendor content is useful, but not sufficient.
5. **Ending with ambiguity when the user needs a recommendation.** The skill should resolve, not hedge forever.

## Verification Checklist
- [ ] I used more than one evidence class.
- [ ] I separated hype from durable adoption.
- [ ] I assessed enterprise credibility separately from community excitement.
- [ ] I named the downside of ignoring the trend.
- [ ] I gave a clear final verdict.

## Examples
### Example: programming language trend
Question: Is language X real, or just hype?

Return:
1. What category it competes in.
2. Whether growth is mostly experimentation or real deployment.
3. Ecosystem/tooling maturity.
4. Talent and hiring implications.
5. What happens if the team ignores it for 2 years.
6. Clear verdict: watch, pilot, adopt, or avoid for now.

### Example: framework adoption
Question: Are enterprises really adopting framework Y?

Return:
1. Official and implementation signals.
2. Whether the framework is seeing greenfield-only or broader adoption.
3. Operational trade-offs.
4. Vendor / community concentration risk.
5. Recommendation by company stage and risk tolerance.

## Evidence hierarchy
Prefer evidence in roughly this order:
1. official docs, release notes, vendor architecture docs
2. production case studies / user engineering posts
3. ecosystem depth: tooling, adapters, integrations, books, references
4. job market / hiring demand
5. community momentum and discussion

Community energy matters — just not by itself.
