---
name: technical-architecture-and-platform-decisions
description: Use when the user asks how to choose a stack, architecture, platform, runtime, service boundaries, persistence model, or long-term technical direction for a product. Also use when the user needs architecture trade-off analysis, platform decision frameworks, build-versus-buy guidance, or a strong staff-engineer-style recommendation for an early-stage tech company.
version: 1.0.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [engineering, architecture, platform, systems-design, trade-offs]
    related_skills: [technology-adoption-research, product-discovery-and-prioritization, devops-and-reliability-planning]
---

# Technical Architecture and Platform Decisions

## Overview

Use this skill to make architecture decisions that are grounded in product needs, team constraints, and operational reality rather than fashion.

## Core Principle

Good architecture is not the most sophisticated design. It is the design that preserves learning speed while keeping future failure modes manageable.

## Workflow

1. Clarify scale, latency, reliability, and complexity requirements.
2. Identify the irreversible versus reversible decisions.
3. Compare options by simplicity, operability, cost, talent fit, and migration risk.
4. Recommend the narrowest architecture that fits likely reality.
5. State explicit triggers for revisiting the decision later.

## Always cover

- delivery speed
- complexity cost
- reliability implications
- observability and debugging
- hiring / maintainability
- vendor lock-in
- migration difficulty

## Output format

Return:
1. current requirements model
2. options compared
3. recommended architecture
4. what not to overbuild
5. future revisit triggers

## Common pitfalls

- architecture driven by imagined scale
- too many services too early
- ignoring debugging and ops burden
- mistaking technical novelty for leverage

## Verification checklist

- [ ] I tied the architecture to real requirements.
- [ ] I separated reversible from irreversible decisions.
- [ ] I recommended the simplest viable architecture.
- [ ] I identified revisit triggers.
