# levelupskills

A public library of **general-purpose, profession-shaped startup and product skills** for Hermes and other agent systems.

These skills are written to be:
- reusable across companies, founders, and products
- portable across agent environments
- structured for real operational judgment, not one-off prompt tricks
- strong on boundaries, pitfalls, examples, and verification

This repo is **not** for company-specific or project-specific instructions.
Project-specific context belongs in project docs, not in the skill bodies.

## What this repo is trying to be

`levelupskills` maps startup building into reusable expert functions:
- research
- company design
- product
- engineering
- security
- finance
- pricing
- legal / compliance
- payments
- growth
- sales
- support
- customer success
- analytics
- AI product ops
- brand
- communication
- operations
- strategy
- people

Think of each skill as: **"load a sharp operator for this category."**

## Library standard

The repo now follows a stronger 2026-2027-style skill standard.

A strong skill in this library should usually include:
- trigger-rich description
- `## Overview`
- `## When to Use`
- counter-triggers / adjacent-skill boundaries
- domain-specific workflow and coverage
- `## Common Pitfalls`
- `## Verification Checklist`
- `## Examples`

See:
- [`references/2026-2027-skill-authoring-standards.md`](./references/2026-2027-skill-authoring-standards.md)
- [`references/brutal-skill-audit.md`](./references/brutal-skill-audit.md)

## Install and setup

See [`SETUP.md`](./SETUP.md) for cross-agent installation and setup.

See [`references/using-levelupskills-across-agents.md`](./references/using-levelupskills-across-agents.md) for portable usage patterns.

## How to use these skills in Hermes

### Option 1: Add this repo as a skill tap

```bash
hermes skills tap add levelscorner/levelupskills
```

Verify:

```bash
hermes skills tap list
```

### Option 2: Install one skill directly from a raw GitHub URL

```bash
hermes skills install https://raw.githubusercontent.com/levelscorner/levelupskills/main/skills/management/startup-company-design/SKILL.md --yes
```

### Option 3: Start Hermes with skills preloaded

```bash
hermes -s startup-company-design,founder-operating-system,product-discovery-and-prioritization
```

### Option 4: Load a skill inside a live Hermes session

```text
/skill startup-company-design
```

### Important Hermes behavior note
- installing a skill and loading a skill are different steps
- `hermes skills install ...` puts the skill on disk
- `hermes -s ...` or `/skill ...` activates the skill in a session
- if a session does not pick up a new skill immediately, start a fresh session or reset session context

## Portable use outside Hermes

These skills are written as portable instruction files.
You can also adapt them into:
- Claude
- Cursor
- Gemini
- terminal/CLI agents
- other chat-based or project-rule agent systems

For non-Hermes systems, copy the relevant `SKILL.md` body into that system's instruction surface.

## Suggested starter bundles

### Pre-idea / idea founder
- `startup-company-design`
- `product-discovery-and-prioritization`
- `customer-research-and-user-interviews`
- `startup-risk-register-and-decision-making`

### Pre-beta founder
- `founder-operating-system`
- `technical-architecture-and-platform-decisions`
- `india-tech-company-legal-compliance`
- `startup-finance-and-unit-economics`
- `pricing-and-packaging-strategy`

### Beta / first users
- `devops-and-reliability-planning`
- `security-privacy-and-risk-review`
- `payment-gateway-selection-for-software`
- `customer-support-and-feedback-ops`
- `analytics-and-metrics-system`

### First revenue
- `gtm-and-growth-experiments`
- `founder-sales-for-b2b`
- `customer-success-for-b2b`
- `brand-positioning-and-messaging`

### Repeatability / expansion
- `hiring-and-people-ops-for-startups`
- `org-design-after-first-hires`
- `vendor-selection-and-procurement`
- `partnerships-and-business-development`
- `community-led-growth`
- `marketplace-and-network-effects-strategy`

## Current skill library

### Research
- `technology-adoption-research`
- `agentic-stack-research`

### Management / company design
- `startup-company-design`
- `founder-operating-system`
- `startup-risk-register-and-decision-making`
- `founder-communication-and-updates`

### Product
- `product-discovery-and-prioritization`
- `customer-research-and-user-interviews`

### Engineering
- `technical-architecture-and-platform-decisions`
- `devops-and-reliability-planning`

### Security
- `security-privacy-and-risk-review`

### Finance
- `startup-finance-and-unit-economics`

### Pricing
- `pricing-and-packaging-strategy`

### Legal / compliance
- `india-tech-company-legal-compliance`

### Payments
- `payment-gateway-selection-for-software`

### Growth / GTM
- `gtm-and-growth-experiments`
- `b2c-growth-and-content-loops`
- `community-led-growth`

### Sales
- `b2b-sales-discovery-and-pipeline`
- `founder-sales-for-b2b`

### Partnerships
- `partnerships-and-business-development`

### Support
- `customer-support-and-feedback-ops`

### Customer Success
- `customer-success-for-b2b`

### Analytics
- `analytics-and-metrics-system`

### AI product ops
- `ai-product-evaluation-and-model-ops`

### Brand
- `brand-positioning-and-messaging`

### Communication
- `concise-structured-communication`
- `verdict-first-writing`
- `response-articulation-pattern`

### Operations
- `vendor-selection-and-procurement`

### Strategy
- `marketplace-and-network-effects-strategy`

### People
- `hiring-and-people-ops-for-startups`
- `org-design-after-first-hires`

## Founder stage navigation

### Pre-idea / idea
- `startup-company-design`
- `product-discovery-and-prioritization`
- `customer-research-and-user-interviews`
- `startup-risk-register-and-decision-making`

### Pre-beta
- `founder-operating-system`
- `technical-architecture-and-platform-decisions`
- `india-tech-company-legal-compliance`
- `startup-finance-and-unit-economics`
- `pricing-and-packaging-strategy`

### Beta / first users
- `devops-and-reliability-planning`
- `security-privacy-and-risk-review`
- `payment-gateway-selection-for-software`
- `customer-support-and-feedback-ops`
- `analytics-and-metrics-system`

### First revenue
- `gtm-and-growth-experiments`
- `founder-sales-for-b2b`
- `customer-success-for-b2b`
- `brand-positioning-and-messaging`
- `verdict-first-writing`
- `response-articulation-pattern`

### Repeatability / expansion
- `hiring-and-people-ops-for-startups`
- `org-design-after-first-hires`
- `vendor-selection-and-procurement`
- `partnerships-and-business-development`
- `community-led-growth`
- `marketplace-and-network-effects-strategy`

## Recommended way to use this repo

1. Use `references/solo-founder-company-function-map.md` to understand the full function map.
2. Load only the few skills relevant to the current problem or stage.
3. Use function skills for **general expert guidance**.
4. Save project-specific decisions in product/company repos, not inside these skills.
5. Add new skills only when they are reusable across many products or teams.
6. Prefer fewer strong skills over many thin ones.

## Repository structure

```text
skills/
  research/
  management/
  product/
  engineering/
  security/
  finance/
  pricing/
  legal/
  payments/
  growth/
  community/
  sales/
  partnerships/
  support/
  customer-success/
  analytics/
  ai/
  brand/
  communication/
  operations/
  strategy/
  people/
references/
  2026-2027-skill-authoring-standards.md
  brutal-skill-audit.md
  research-taxonomy.md
  solo-founder-company-function-map.md
  using-levelupskills-across-agents.md
README.md
SETUP.md
```

## Notes

This repository is building toward a reusable startup-function skill library: skills that map to real professional roles, not one-off project notes.
