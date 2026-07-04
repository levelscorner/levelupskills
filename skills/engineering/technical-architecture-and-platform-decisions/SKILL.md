---
name: technical-architecture-and-platform-decisions
description: "Use when the user asks how to choose a stack, architecture, platform, runtime, service boundaries, persistence model, or long-term technical direction for a product. Also use when the user needs architecture trade-off analysis, platform decision frameworks, build-versus-buy guidance, or a strong staff-engineer-style recommendation for an early-stage tech company. Do not use this as the main skill for pure technology adoption research or vendor procurement when architecture is not the central question."
version: 1.1.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [engineering, architecture, platform, systems-design, trade-offs]
    related_skills: [technology-adoption-research, product-discovery-and-prioritization, devops-and-reliability-planning]
---

# Technical Architecture and Platform Decisions

## Overview
Use this skill to make architecture decisions that are grounded in product needs, team constraints, and operational reality rather than fashion. The point is not to design the most impressive system. It is to preserve delivery speed while keeping failure modes and migration pain manageable.

## When to Use
Use this skill when the main problem is **technical shape and platform direction**.

Typical triggers:
- choosing a stack or runtime
- deciding monolith vs services vs modular boundaries
- evaluating persistence models or platform choices
- build-vs-buy trade-offs with architectural implications
- designing for reliability, scale, or future change without overbuilding
- deciding when current architecture is “good enough” versus when it must evolve

Do **not** use this as the main skill when:
- the task is mainly ecosystem or language adoption research → use `technology-adoption-research`
- the task is mainly vendor selection or procurement process → use `vendor-selection-and-procurement`
- the task is detailed reliability operations planning more than architecture direction → use `devops-and-reliability-planning`

## Core Principle
Good architecture is not the most sophisticated design. It is the design that preserves learning speed while keeping future failure modes manageable.

## Always cover
- product and delivery constraints
- reversible vs irreversible decisions
- complexity cost
- reliability and observability implications
- hiring / maintainability fit
- vendor lock-in and migration difficulty
- what not to overbuild

## Workflow
1. Clarify scale, latency, reliability, delivery, and complexity requirements.
2. Identify reversible versus irreversible decisions.
3. Compare options by simplicity, operability, cost, talent fit, observability, and migration risk.
4. Recommend the narrowest architecture that fits likely reality.
5. State explicit triggers for revisiting the decision later.

## Decision lenses
### Simplicity
Will the team understand and debug this under pressure?

### Operability
Can the team observe, deploy, and recover the system without heroics?

### Team fit
Does the architecture match the team's actual skills and likely hiring pool?

### Future change
What is expensive to reverse later, and what can safely wait?

## Output format
Return:
1. current requirements model
2. options compared
3. recommended architecture
4. overbuild risks and what to keep simple
5. future revisit triggers

## Common pitfalls
1. **Architecture driven by imagined scale.** Most early systems fail from unnecessary complexity sooner than from traffic.
2. **Too many services too early.** Distributed systems multiply coordination, debugging, and deployment cost.
3. **Ignoring observability and ops burden.** Fancy design without practical diagnosis is fragile.
4. **Mistaking novelty for leverage.** New technology is not strategy by itself.
5. **Forgetting migration paths.** A good decision includes a believable future change path.
6. **Choosing architecture that the team cannot operate.** Elegance on paper does not ship products.

## Verification checklist
- [ ] I tied the architecture to real product and team requirements.
- [ ] I separated reversible from irreversible decisions.
- [ ] I recommended the simplest viable architecture.
- [ ] I named overbuild risks explicitly.
- [ ] I identified concrete revisit triggers.

## Examples
### Example: early SaaS backend
Return:
1. Delivery speed and debugging simplicity matter more than speculative scale.
2. Start with a modular monolith and a boring relational database.
3. Delay service decomposition until operational boundaries become real.
4. Invest early in logging, migrations, and observability hygiene.
5. Revisit architecture only when team size, load, or reliability needs justify it.

### Example: choosing a managed platform
Return:
1. The main trade-off is speed vs control, not prestige.
2. Prefer the managed option if it removes meaningful ops burden without blocking core product needs.
3. Name lock-in and migration cost clearly.
4. Avoid self-hosting unless it solves a real risk or cost problem.
5. Set revisit triggers based on scale, compliance, or cost thresholds.
