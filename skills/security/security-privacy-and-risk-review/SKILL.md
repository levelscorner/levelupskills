---
name: security-privacy-and-risk-review
description: "Use when the user asks how to review a product, workflow, vendor, feature, or architecture for security, privacy, data risk, abuse risk, or compliance-sensitive design weaknesses. Also use for startup security posture reviews, privacy-by-design reviews, vendor-risk thinking, and practical risk reduction planning before compliance theater sets in. Do not use this as the main skill for narrow legal interpretation or pure reliability design when security and privacy risk are not central."
version: 1.1.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [security, privacy, risk, compliance, data-protection]
    related_skills: [devops-and-reliability-planning, india-tech-company-legal-compliance]
---

# Security, Privacy, and Risk Review

## Overview
Use this skill to review product and operational choices through a practical security and privacy lens. The goal is not maximum ceremony. The goal is to identify where a small mistake could create outsized harm and reduce that exposure first.

## When to Use
Use this skill when the main problem is **security, privacy, or abuse-risk posture**.

Typical triggers:
- reviewing a feature or workflow for sensitive-data risk
- assessing startup security posture
- checking privacy-by-design decisions
- evaluating vendor or third-party exposure
- prioritizing risk reduction before formal compliance programs mature
- identifying top breach, fraud, abuse, or misuse failure modes

Do **not** use this as the main skill when:
- the question is narrow legal interpretation or jurisdiction-specific legal advice → use relevant legal skills or real counsel
- the question is mostly reliability/availability with little security or privacy exposure → use `devops-and-reliability-planning`
- the task is procurement-first rather than risk-first → use `vendor-selection-and-procurement`

## Core Principle
Early-stage security is about **risk concentration**: identify where a small mistake could create outsized damage, then reduce that exposure first.

## Always cover
- sensitive assets and trust boundaries
- auth and access control
- secrets and credentials
- user data collection, storage, and retention
- logging and privacy trade-offs
- vendor / third-party exposure
- incident handling readiness
- immediate controls vs later maturity work

## Workflow
1. Identify sensitive assets, data flows, and trust boundaries.
2. Review who can access what, under which controls.
3. Identify top abuse, breach, fraud, or privacy failure modes.
4. Prioritize mitigations by severity, likelihood, and effort.
5. Separate immediate controls from later maturity items.
6. Note where legal, compliance, or specialist review is required.

## Severity framing
### Critical
A failure could cause major customer harm, major data exposure, or material company damage.

### High
A failure is serious and likely needs early mitigation before broader rollout.

### Medium
A real weakness exists, but it may be acceptable temporarily with explicit awareness and a plan.

### Low
The issue is worth improving but not the current primary risk.

## Output format
Return:
1. risk overview and trust-boundary map
2. highest-risk failure modes
3. controls needed now
4. later maturity roadmap
5. escalation areas needing legal or specialist review

## Common pitfalls
1. **Collecting more data than needed.** Unnecessary data multiplies breach and privacy risk.
2. **Unclear access boundaries.** If nobody knows who should access what, mistakes are inevitable.
3. **No incident owner or process.** Many teams discover this only when something breaks badly.
4. **Compliance theater without real risk reduction.** Checklists are not protection.
5. **Logging sensitive data casually.** Debug convenience can become a privacy leak.
6. **Treating vendors as trusted by default.** Third-party risk still counts as your risk.

## Verification checklist
- [ ] I identified assets, data flows, and trust boundaries.
- [ ] I prioritized by severity and likely harm, not fear alone.
- [ ] I recommended concrete mitigations for the top risks.
- [ ] I distinguished immediate controls from later maturity work.
- [ ] I called out where legal or specialist review is necessary.

## Examples
### Example: early B2B SaaS review
Return:
1. Main concentrated risk is broad internal access to customer workspace data.
2. Highest-priority controls are tighter role boundaries, audit logging, and secrets handling.
3. Logging policy needs review because debug output may expose customer content.
4. Formal compliance can wait, but retention and access boundaries cannot.
5. Seek legal/privacy input if customer data categories expand.

### Example: AI feature privacy review
Return:
1. Primary issue is whether prompts or outputs contain sensitive user data.
2. Review provider retention terms, logging policy, and staff access.
3. Add redaction or segmentation if full-context forwarding is not necessary.
4. Define incident response for model or provider-side leakage scenarios.
5. Do not ship based only on “provider says they are secure.”
