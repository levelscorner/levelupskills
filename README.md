# levelupskills

Custom Hermes skills for **expert, profession-based, reusable thinking** across startup building, research, company design, product, engineering, finance, legal, payments, growth, sales, support, communication, and operations.

## Philosophy

These skills are meant to feel like bringing in a strong professional from a real function:

- strategy / founder advisor
- product lead
- architect / engineering lead
- DevOps / reliability lead
- security / privacy reviewer
- startup finance operator
- startup lawyer / CA / CS-informed operator
- payments operator
- growth lead
- sales lead
- customer success / support lead
- communication coach / editor
- operations lead

They are **not** intended to be specific to one founder, company, or project. Project-specific application should live in repo docs, decision memos, or research notes.

## Install and setup

See [`SETUP.md`](./SETUP.md) for cross-agent installation and setup.

See [`references/using-levelupskills-across-agents.md`](./references/using-levelupskills-across-agents.md) for cross-agent usage patterns.

## How to use these skills in Hermes

### Option 1: Add this repo as a skill tap

This is the best way to make the repo available as a reusable skill source.

```bash
hermes skills tap add levelscorner/levelupskills
```

What this does:
- registers `levelscorner/levelupskills` as a GitHub skill source
- tells Hermes to look under the repo's `skills/` directory
- lets you manage the repo as a reusable skill library across sessions and machines

You can verify the tap exists with:

```bash
hermes skills tap list
```

### Option 2: Install a skill directly from a raw GitHub URL

Use this when you only want one skill.

Example:

```bash
hermes skills install https://raw.githubusercontent.com/levelscorner/levelupskills/main/skills/management/startup-company-design/SKILL.md --yes
```

Notes:
- `--yes` skips the install confirmation prompt
- use `--name <skill-name>` only if the remote `SKILL.md` has no `name:` frontmatter
- raw GitHub URLs are useful for pin-point installs, but less convenient than tapping the repo if you want many skills

### Option 3: Start Hermes with a skill preloaded

Once a skill is installed locally, preload it into a new session:

```bash
hermes -s startup-company-design
```

You can preload multiple skills:

```bash
hermes -s startup-company-design,founder-operating-system,product-discovery-and-prioritization
```

### Option 4: Load a skill inside an existing Hermes session

Inside Hermes, run:

```text
/skill startup-company-design
```

Use this when you already have a live conversation and want the skill added to that Hermes session.

### Use the same skills outside Hermes too

These skills are written as portable instruction files, not Hermes-only logic.

You can also paste or adapt them into:
- Claude
- Cursor
- Gemini
- Codex-style terminal agents
- other chat or CLI agent systems

For non-Hermes systems, copy the relevant `SKILL.md` content into that system's prompt, instruction file, project rules, or reusable agent preset.

### Important behavior notes

- Installing a skill and loading a skill are **different** steps.
- `hermes skills install ...` puts the skill on disk.
- `hermes -s ...` or `/skill ...` makes Hermes actively use it in a session.
- Tool/skill changes may require a fresh session or `/reset` if the current session does not pick them up immediately.

## Suggested starter bundles

### Pre-idea / idea founder
Start with:
- `startup-company-design`
- `product-discovery-and-prioritization`
- `customer-research-and-user-interviews`
- `startup-risk-register-and-decision-making`

### Pre-beta founder
Start with:
- `founder-operating-system`
- `technical-architecture-and-platform-decisions`
- `india-tech-company-legal-compliance`
- `startup-finance-and-unit-economics`
- `pricing-and-packaging-strategy`

### Beta / first users
Start with:
- `devops-and-reliability-planning`
- `security-privacy-and-risk-review`
- `payment-gateway-selection-for-software`
- `customer-support-and-feedback-ops`
- `analytics-and-metrics-system`

### First revenue
Start with:
- `gtm-and-growth-experiments`
- `founder-sales-for-b2b`
- `customer-success-for-b2b`
- `brand-positioning-and-messaging`

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
  - short answers, simple English, Topic / Body / Verdict, works across Hermes and other agent/chat systems
- `verdict-first-writing`
  - answer first, reasons after, strong for recommendations and decision notes
- `response-articulation-pattern`
  - pick the right structure for answers, steps, comparisons, diagnoses, and plans

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

1. Use `references/solo-founder-company-function-map.md` to understand the full company function map.
2. Use function skills for **general expert guidance**.
3. Use `references/using-levelupskills-across-agents.md` when you want portable usage patterns outside Hermes too.
4. Save project-specific decisions in your product/company repos, not inside these skills.
5. Add new skills only when they are reusable across many startups or products.
6. Prefer loading a small set of relevant skills for the current startup stage instead of loading everything at once.

## Repository structure

```text
skills/
  research/
    technology-adoption-research/
      SKILL.md
    agentic-stack-research/
      SKILL.md
  management/
    startup-company-design/
      SKILL.md
    founder-operating-system/
      SKILL.md
    startup-risk-register-and-decision-making/
      SKILL.md
    founder-communication-and-updates/
      SKILL.md
  product/
    product-discovery-and-prioritization/
      SKILL.md
    customer-research-and-user-interviews/
      SKILL.md
  engineering/
    technical-architecture-and-platform-decisions/
      SKILL.md
    devops-and-reliability-planning/
      SKILL.md
  security/
    security-privacy-and-risk-review/
      SKILL.md
  finance/
    startup-finance-and-unit-economics/
      SKILL.md
  pricing/
    pricing-and-packaging-strategy/
      SKILL.md
  legal/
    india-tech-company-legal-compliance/
      SKILL.md
  payments/
    payment-gateway-selection-for-software/
      SKILL.md
  growth/
    gtm-and-growth-experiments/
      SKILL.md
    b2c-growth-and-content-loops/
      SKILL.md
  community/
    community-led-growth/
      SKILL.md
  sales/
    b2b-sales-discovery-and-pipeline/
      SKILL.md
    founder-sales-for-b2b/
      SKILL.md
  partnerships/
    partnerships-and-business-development/
      SKILL.md
  support/
    customer-support-and-feedback-ops/
      SKILL.md
  customer-success/
    customer-success-for-b2b/
      SKILL.md
  analytics/
    analytics-and-metrics-system/
      SKILL.md
  ai/
    ai-product-evaluation-and-model-ops/
      SKILL.md
  brand/
    brand-positioning-and-messaging/
      SKILL.md
  communication/
    concise-structured-communication/
      SKILL.md
    verdict-first-writing/
      SKILL.md
    response-articulation-pattern/
      SKILL.md
  operations/
    vendor-selection-and-procurement/
      SKILL.md
  strategy/
    marketplace-and-network-effects-strategy/
      SKILL.md
  people/
    hiring-and-people-ops-for-startups/
      SKILL.md
    org-design-after-first-hires/
      SKILL.md
references/
  research-taxonomy.md
  solo-founder-company-function-map.md
  using-levelupskills-across-agents.md
README.md
```

## Notes

This repository is building toward a reusable startup-function skill library: skills that map to real professional roles, not one-off project notes.
