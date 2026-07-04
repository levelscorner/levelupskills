---
name: vendor-selection-and-procurement
description: Use when the user asks how to evaluate vendors, tools, infrastructure providers, AI providers, software subscriptions, outsourcing partners, procurement choices, or buy-vs-build trade-offs. Also use when the user needs a professional operator lens on vendor selection, contract trade-offs, reliability, switching costs, and approval criteria. Do not use this as the main skill for pure architecture design or pure security review when procurement is not the central question.
version: 1.1.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [vendors, procurement, buy-vs-build, operations, sourcing]
    related_skills: [startup-finance-and-unit-economics, security-privacy-and-risk-review, technical-architecture-and-platform-decisions]
---

# Vendor Selection and Procurement

## Overview
Use this skill to evaluate external tools and vendors in a disciplined, repeatable way. The point is not to compare feature checklists forever. The point is to make a decision that survives cost, risk, contract, and operational reality.

## When to Use
Use this skill when the main problem is **external provider choice**.

Typical triggers:
- choosing between vendors, SaaS tools, infra providers, or AI providers
- evaluating outsourcing or service partners
- build vs buy vs hybrid tradeoff with procurement implications
- negotiating contract risk, lock-in, or approval criteria

Do **not** use this as the main skill when:
- the main question is architecture shape without procurement focus → use `technical-architecture-and-platform-decisions`
- the main question is security/privacy posture without a vendor decision at stake → use `security-privacy-and-risk-review`
- the task is pricing a product sold to customers rather than a tool bought by the company

## Core Principle
A vendor choice is never just a feature comparison. It is a long-tail decision about reliability, economics, lock-in, risk, and operating burden.

## Always cover
- decision scope
- build vs buy trade-off
- total cost and operational load
- security / reliability / contract risk
- lock-in and migration risk
- exit criteria

## Workflow
1. Clarify the job to be done and why outside procurement is being considered.
2. Compare build, buy, and hybrid options.
3. Evaluate economics, risk, integration cost, switching cost, and vendor reliability.
4. Recommend a decision framework sized to stage.
5. Define review triggers and exit criteria.

## Output format
Return:
1. procurement context
2. recommended evaluation framework
3. preferred option and rationale
4. risks and negotiation concerns
5. review triggers and next steps

## Common pitfalls
1. **Choosing by demo quality alone.** Sales polish is not delivery quality.
2. **Ignoring switching cost.** Lock-in often matters more later than sticker price now.
3. **Treating build-vs-buy like a philosophical debate.** It is a stage and capability question.
4. **Missing hidden operator burden.** A cheap tool can still be expensive to run.
5. **Signing without exit criteria.** Good procurement includes a way out.

## Verification checklist
- [ ] I compared build, buy, and hybrid where relevant.
- [ ] I considered total cost, risk, and operational burden.
- [ ] I named contract, lock-in, or migration concerns.
- [ ] I defined review triggers or exit criteria.

## Examples
### Example: AI provider selection
Return:
1. Job is product inference, not research experimentation.
2. Reliability and cost predictability matter more than top benchmark score.
3. Prefer the provider with clearer fallback and pricing control.
4. Negotiate data use, SLA, and rate-limit terms early.
5. Revisit only if quality gap becomes commercially meaningful.
