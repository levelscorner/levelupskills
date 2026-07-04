---
name: analytics-and-metrics-system
description: "Use when the user asks how to design startup analytics, KPI systems, dashboards, event tracking, reporting cadence, activation or retention measurement, experiment measurement, or founder-level metrics discipline. Also use when the user needs help deciding what to measure now versus later, how to avoid vanity metrics, or how to turn product and business questions into a practical measurement system. Do not use this as the main skill for pure data science analysis or generic dashboard design when the real issue is measurement strategy."
version: 1.1.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [analytics, metrics, KPI, dashboards, measurement, startup]
    related_skills: [founder-operating-system, product-discovery-and-prioritization, startup-finance-and-unit-economics]
---

# Analytics and Metrics System

## Overview
Use this skill to build a measurement system that helps a startup make better decisions rather than merely collect more numbers. The goal is not reporting theater. The goal is to reduce uncertainty early enough to act.

## When to Use
Use this skill when the main problem is **what to measure, how to define it, and how to use it in decisions**.

Typical triggers:
- designing a KPI system or company scorecard
- defining activation, retention, or revenue metrics
- planning event tracking and instrumentation priorities
- choosing dashboard and reporting cadence
- fixing a company that has too many numbers and too little clarity
- deciding what not to measure yet

Do **not** use this as the main skill when:
- the task is mostly a one-off data analysis question rather than a measurement system
- the task is pure visualization polish with no KPI or instrumentation decision
- the user mainly needs finance modeling rather than broader measurement design → use `startup-finance-and-unit-economics`

## Core Principle
Metrics are useful only when they reduce uncertainty, improve decisions, or expose risk early enough to act.

## Always cover
- company stage and current bottleneck
- decisions the metrics should enable
- leading vs lagging indicators
- event / entity model basics
- dashboard and review cadence
- data definition hygiene and ownership
- metrics that should **not** be tracked yet

## Workflow
1. Identify the stage and the decisions the company is struggling to make.
2. Separate business questions from instrumentation details.
3. Define a small metric set tied to acquisition, activation, retention, revenue, reliability, or cost as relevant.
4. Recommend event tracking, metric definitions, dashboards, and review cadence.
5. Explicitly reject vanity metrics that do not change decisions.
6. Distinguish must-have instrumentation now from deeper analytics later.

## Stage guidance
### Pre-product or very early stage
- optimize for learning, not dashboard abundance
- track a few core signals around usage, activation, and feedback quality
- avoid overbuilding attribution and BI complexity

### Early traction stage
- improve retention and funnel visibility
- tighten event definitions and owner discipline
- add revenue and unit-economics linkage if monetization is live

### Scaling stage
- increase segmentation, cohort analysis, and team accountability
- improve data quality controls and definitions
- separate executive scorecards from deep operator dashboards

## Output format
Return:
1. decision context
2. recommended metric system
3. key definitions and instrumentation needs
4. reporting cadence and ownership
5. risks / vanity metrics to avoid

## Common pitfalls
1. **Tracking everything and learning nothing.** Metric sprawl kills signal.
2. **Mixing product, finance, and GTM metrics without definitions.** Shared words with different meanings create chaos.
3. **No owner for instrumentation quality.** Bad events quietly poison decisions.
4. **Dashboards without review rituals.** A metric nobody reviews is decorative.
5. **Choosing KPIs because competitors mention them.** Metric fit is stage- and model-dependent.
6. **Measuring downstream outcomes before upstream behavior is even defined.** Start where the decisions are.

## Verification checklist
- [ ] I tied metrics to decisions, not curiosity alone.
- [ ] I selected a stage-appropriate metric set.
- [ ] I separated must-have instrumentation from later depth.
- [ ] I named metric owners, definitions, or cadence where relevant.
- [ ] I explicitly identified vanity metrics to avoid.

## Examples
### Example: early SaaS analytics
Return:
1. Main decision problem is whether activation is real, not whether traffic charts look good.
2. Track signup completion, first-value event, weekly retained actives, and top failure reason.
3. Define activation precisely instead of using generic “active user” language.
4. Review weekly with product + founder, monthly at company level.
5. Ignore advanced attribution until retention and activation are credible.

### Example: overloaded dashboard system
Return:
1. Current issue is too many metrics with no operating hierarchy.
2. Collapse to one company scorecard plus role-specific supporting views.
3. Remove vanity traffic and social metrics unless they change decisions.
4. Create a metric dictionary and owner list.
5. Rebuild trust in data definitions before adding new dashboards.
