---
name: payment-gateway-selection-for-software
description: "Use when the user asks how to choose payment infrastructure for a software, SaaS, AI, app, or digital-product business, including merchant-of-record versus direct gateway decisions, subscriptions, one-time payments, invoicing, international collection, tax/compliance implications, or operational payment trade-offs. Also use when the user needs a product-and-operations lens on payments rather than a generic feature checklist. Do not use this as the main skill for product pricing design or broad procurement work when the core question is not payment infrastructure choice."
version: 1.1.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [payments, gateway, SaaS, subscriptions, merchant-of-record, billing]
    related_skills: [pricing-and-packaging-strategy, vendor-selection-and-procurement, startup-finance-and-unit-economics]
---

# Payment Gateway Selection for Software

## Overview
Use this skill to choose payment infrastructure in a way that reflects business model, geography, compliance load, and operational reality. The goal is not to compare gateways as abstract tools. The goal is to choose a payment system the company can actually run.

## When to Use
Use this skill when the main problem is **how to collect money operationally**.

Typical triggers:
- choosing between merchant-of-record and direct gateway models
- subscriptions vs invoices vs one-time payment flows
- international payments or tax/compliance burden
- failed-payment recovery and billing operations
- payment stack changes driven by product or geography expansion

Do **not** use this as the main skill when:
- the issue is pricing/packaging strategy → use `pricing-and-packaging-strategy`
- the issue is generic vendor scoring without payment-specific logic → use `vendor-selection-and-procurement`
- the task is accounting, tax filing, or legal advice beyond payment-ops framing

## Core Principle
Payment infrastructure is not only a checkout choice. It is an operating-system decision about who handles compliance, risk, billing complexity, and cash movement.

## Key decision split
The first major question is usually not “which gateway has the best API?” It is “should this company own the merchant/compliance burden directly or outsource part of it through a merchant-of-record model?”

## Always cover
- merchant-of-record vs direct model
- billing model fit
- geography and currency support
- tax / invoicing / compliance burden
- payment failure handling
- operational complexity and margin impact

## Workflow
1. Identify product model, customer type, geography, and billing pattern.
2. Separate pricing design from payment collection design.
3. Evaluate merchant-of-record vs direct ownership trade-offs.
4. Compare operational burden, margin effect, flexibility, and risk.
5. Recommend the simplest payment setup that supports the current stage.

## Output format
Return:
1. payment-infrastructure diagnosis
2. recommended collection model
3. operational and compliance trade-offs
4. risks and failure modes
5. next implementation or review priorities

## Common pitfalls
1. **Choosing by API aesthetics alone.** Payments are operations, not just SDKs.
2. **Ignoring failed-payment workflows.** Collection quality matters after checkout too.
3. **Underestimating tax and merchant burden.** Those costs are real work.
4. **Over-optimizing margin too early while creating huge operational load.** Simplicity often wins early.
5. **Mixing pricing questions with collection questions.** They interact, but they are not identical.

## Verification checklist
- [ ] I separated pricing from payment-collection design.
- [ ] I evaluated merchant-of-record versus direct ownership clearly.
- [ ] I considered geography, compliance, and operational burden.
- [ ] I recommended a stage-appropriate payment setup.

## Examples
### Example: early global SaaS
Return:
1. Main trade-off is margin versus outsourced complexity.
2. Merchant-of-record may fit if tax/compliance simplicity matters more than payment flexibility.
3. Prioritize reliable subscriptions, invoicing clarity, and dunning over exotic payment features.
4. Revisit only if enterprise billing or margin pressure becomes meaningful.
5. Keep the payment stack boring until the business model demands more.

### Example: direct gateway reconsideration
Return:
1. The current direct model gives control but is creating operational drag.
2. Compare margin leakage against internal time, support, and compliance burden.
3. Do not switch just for novelty; switch if the total system improves.
4. Review failure recovery and geographic expansion needs.
5. Coordinate with finance and legal before committing to migration.
