---
name: security-privacy-and-risk-review
description: Use when the user asks how to review a product, workflow, vendor, feature, or architecture for security, privacy, data-risk, abuse-risk, or compliance-sensitive design weaknesses. Also use for startup security posture reviews, privacy-by-design reviews, vendor-risk thinking, and practical risk reduction planning before overcomplicated compliance theater sets in.
version: 1.0.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [security, privacy, risk, compliance, data-protection]
    related_skills: [devops-and-reliability-planning, india-tech-company-legal-compliance]
---

# Security, Privacy, and Risk Review

## Overview

Use this skill to review product and operational choices through a practical security and privacy lens.

## Core Principle

Early-stage security is about **risk concentration**: identify where a small mistake could create outsized damage, then reduce that exposure first.

## Workflow

1. Identify sensitive assets, data, and trust boundaries.
2. Review who can access what and how.
3. Identify top abuse, breach, fraud, or privacy failure modes.
4. Separate immediate controls from later maturity items.
5. Recommend mitigations by severity and effort.

## Always evaluate

- auth and access control
- secrets and credentials
- user data collection and retention
- logging/privacy trade-offs
- vendor / third-party exposure
- incident handling readiness

## Output format

Return:
1. risk overview
2. highest-risk failure modes
3. controls needed now
4. later maturity roadmap

## Common pitfalls

- collecting more data than needed
- unclear access boundaries
- no incident owner or process
- compliance theater without real risk reduction

## Verification checklist

- [ ] I identified assets and trust boundaries.
- [ ] I prioritized by severity, not fear.
- [ ] I recommended concrete mitigations.
- [ ] I distinguished now from later.
