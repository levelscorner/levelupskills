---
name: devops-and-reliability-planning
description: "Use when the user asks how to run deployment, uptime, monitoring, incident readiness, backup strategy, environments, CI/CD, cost-aware infrastructure, or operational maturity for a product. Also use for SRE-style planning, operational readiness reviews, release safety planning, and reliability roadmaps for startups. Do not use this as the main skill for pure architecture direction or pure security review when operational reliability is not the central issue."
version: 1.1.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [devops, reliability, sre, operations, deployment, observability]
    related_skills: [technical-architecture-and-platform-decisions, security-privacy-and-risk-review]
---

# DevOps and Reliability Planning

## Overview
Use this skill to turn a product from “it runs on my machine” into something that can be deployed, observed, recovered, and trusted. The goal is not enterprise ceremony. The goal is operational confidence sized to stage.

## When to Use
Use this skill when the main problem is **operating and recovering production systems reliably**.

Typical triggers:
- deployment process is fragile
- rollback is unclear
- monitoring and alerts are weak
- backup or restore confidence is low
- incidents are handled ad hoc
- reliability work is lagging behind product growth

Do **not** use this as the main skill when:
- the main issue is architecture shape → use `technical-architecture-and-platform-decisions`
- the main issue is security/privacy posture → use `security-privacy-and-risk-review`
- the task is only coding a CI pipeline snippet with no reliability-planning question

## Core Principle
Reliability is not only uptime. Reliability is the ability to detect, understand, and recover from failure without panic.

## Always cover
- deployment workflow
- rollback path
- backups / restore confidence
- monitoring and logs
- incident response basics
- secrets handling
- cost discipline

## Workflow
1. Identify the service model and critical user flows.
2. Define environments, deployment path, and rollback model.
3. Define monitoring, logging, alerting, and backup expectations.
4. Identify single points of failure and operational blind spots.
5. Recommend the next maturity step, not an enterprise fantasy stack.

## Stage guidance
### Early stage
- prefer simple deploys with real rollback
- add core monitoring before elaborate automation
- verify backups can actually restore

### Growing stage
- improve alert quality, incident handling, and environment consistency
- reduce deployment fear and hidden operational debt
- track cost alongside reliability

## Output format
Return:
1. operational maturity assessment
2. critical gaps
3. must-have controls now
4. next-level improvements later
5. recovery and incident priorities

## Common pitfalls
1. **No rollback story.** Deploying without retreat is not a process.
2. **No restore-tested backups.** Backup claims without restore proof are fiction.
3. **Alerts without useful observability.** Noise is not awareness.
4. **Copying big-company SRE patterns too early.** Complexity can outrun team capacity.
5. **Ignoring cost while improving reliability.** Overbuilt ops can become its own failure mode.

## Verification checklist
- [ ] I covered deploy, observe, and recover.
- [ ] I prioritized high-leverage reliability controls.
- [ ] I adapted recommendations to startup stage and team capacity.
- [ ] I included backup, rollback, or incident-readiness logic.

## Examples
### Example: first production hardening
Return:
1. Main gap is not scale; it is lack of safe deployment and recovery discipline.
2. Add one predictable deployment path, one rollback path, and baseline monitoring.
3. Verify backups by restore test, not by assumption.
4. Route alerts to owners with simple severity expectations.
5. Delay advanced platform work until the basics are stable.

### Example: alert fatigue
Return:
1. The issue is low signal quality, not lack of more alerts.
2. Reduce noise and tighten alerts around user-impacting failures.
3. Improve dashboards and logs so incidents can be diagnosed fast.
4. Clarify incident ownership and escalation.
5. Review cost and toil before adding more tools.
