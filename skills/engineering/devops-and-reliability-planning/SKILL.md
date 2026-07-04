---
name: devops-and-reliability-planning
description: Use when the user asks how to run deployment, uptime, monitoring, incident readiness, backup strategy, environments, CI/CD, cost-aware infrastructure, or operational maturity for a product. Also use for SRE-style planning, operational readiness reviews, release safety planning, and reliability roadmaps for startups.
version: 1.0.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [devops, reliability, sre, operations, deployment, observability]
    related_skills: [technical-architecture-and-platform-decisions, security-privacy-and-risk-review]
---

# DevOps and Reliability Planning

## Overview

Use this skill to turn a product from "it runs on my machine" into something that can be deployed, observed, recovered, and trusted.

## Core Principle

Reliability is not only uptime. Reliability is the ability to detect, understand, and recover from failure without panic.

## Workflow

1. Identify the service model and critical user flows.
2. Define environments, deployment path, and rollback model.
3. Define monitoring, logging, alerting, and backup expectations.
4. Identify single points of failure and operational blind spots.
5. Recommend the next maturity step, not an enterprise fantasy stack.

## Always cover

- deployment workflow
- rollback path
- backups / restore confidence
- monitoring and logs
- incident response basics
- secrets handling
- cost discipline

## Output format

Return:
1. operational maturity assessment
2. critical gaps
3. must-have controls now
4. next-level improvements later

## Common pitfalls

- no rollback story
- no restore-tested backups
- alerts without useful observability
- copying big-company SRE patterns too early

## Verification checklist

- [ ] I covered deploy, observe, recover.
- [ ] I prioritized high-leverage reliability controls.
- [ ] I adapted recommendations to startup stage.
