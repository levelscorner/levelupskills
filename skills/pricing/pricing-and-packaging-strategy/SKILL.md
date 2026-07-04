---
name: pricing-and-packaging-strategy
description: "Use when the user asks how to price a software, SaaS, AI, or digital product; how to structure tiers, plans, credits, usage limits, free trials, freemium boundaries, enterprise packaging, or monetization experiments; or how to decide what to charge before strong market certainty exists. Also use when the user needs a practical operator-level lens on pricing and packaging trade-offs rather than generic pricing slogans. Do not use this as the main skill for pure billing implementation or generic finance modeling without a real pricing-strategy question."
version: 1.1.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [pricing, packaging, monetization, SaaS, strategy]
    related_skills: [startup-finance-and-unit-economics, product-discovery-and-prioritization, payment-gateway-selection-for-software]
---

# Pricing and Packaging Strategy

## Overview
Use this skill to design pricing and packaging in a way that reflects customer value, operating costs, buying behavior, and product maturity. The goal is not to pick a clever number. The goal is to create a monetization system that customers understand and the company can operate.

## When to Use
Use this skill when the main problem is **what to charge, how to structure plans, and what behavior the pricing model should encourage**.

Typical triggers:
- deciding price points or packaging tiers
- choosing seat-based, usage-based, flat-rate, or hybrid logic
- designing trials, freemium limits, or plan boundaries
- packaging AI or infrastructure-heavy products
- evaluating willingness-to-pay before strong certainty exists
- fixing pricing that feels confusing, underpriced, or misaligned with value

Do **not** use this as the main skill when:
- the task is billing-system implementation rather than pricing strategy
- the task is detailed financial modeling with no packaging decision → use `startup-finance-and-unit-economics`
- the question is payment provider setup rather than pricing design → use `payment-gateway-selection-for-software`

## Core Principle
Pricing is not just a number. It is a product decision, a market-positioning signal, and a filter on which customers the company is trying to attract.

## Always cover
- customer and use-case segmentation
- value metric vs seat vs usage vs flat-rate logic
- free / trial / freemium boundaries
- margin and cost sensitivity
- packaging clarity and plan ladder
- experiment and revision triggers
- what should be kept simple now

## Workflow
1. Identify the product type, value moment, customer type, and current stage.
2. Separate pricing questions from packaging questions.
3. Evaluate willingness-to-pay signals, usage patterns, value metrics, and cost drivers.
4. Recommend a simple structure that can learn quickly without creating billing chaos.
5. State what should be tested later versus what should be locked now.

## Decision lenses
### Customer value
What benefit are customers actually buying, and when do they feel that value?

### Buyer behavior
Who decides, who pays, and what buying friction matters?

### Cost structure
What usage patterns or support burdens could silently destroy margin?

### Simplicity
Can the pricing model be explained in one short conversation?

## Output format
Return:
1. pricing context diagnosis
2. recommended packaging structure
3. pricing logic and rationale
4. risks and failure modes
5. what to test next

## Common pitfalls
1. **Choosing a price before understanding value delivery.** Price signals work only when tied to perceived value.
2. **Too many plans too early.** Complexity creates confusion and internal overhead.
3. **Copying competitors without understanding their context.** Their model may reflect a different product or customer base.
4. **Ignoring cost-to-serve and support burden.** Revenue without margin discipline can still hurt the company.
5. **Overfitting to one loud customer segment.** Packaging should reflect the target market, not the most demanding anecdote.
6. **Treating trials and freemium as free defaults.** They are strategic tools, not automatic best practices.

## Verification checklist
- [ ] I separated pricing from packaging clearly.
- [ ] I tied the recommendation to customer value and company stage.
- [ ] I considered cost, margin, or support implications.
- [ ] I kept the structure as simple as the situation allows.
- [ ] I stated what still needs testing.

## Examples
### Example: early B2B SaaS
Return:
1. Start with a simple tiered model before advanced usage pricing.
2. Anchor plans around team size or workflow scope if that matches buying behavior.
3. Avoid too many feature gates until value segmentation is clearer.
4. Offer a trial if setup friction is low enough to support self-serve learning.
5. Reassess pricing only after observing activation, conversion, and support load.

### Example: AI-heavy product
Return:
1. Cost variability means pure unlimited pricing may be dangerous.
2. Use packaging that gives customers clarity while protecting margin.
3. Consider credits or sensible usage bands if value and cost both scale with usage.
4. Reserve custom pricing for enterprise patterns that genuinely differ.
5. Track gross margin by customer behavior, not just top-line conversions.
