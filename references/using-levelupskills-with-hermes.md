# Using levelupskills with Hermes

This guide explains how to consume the `levelscorner/levelupskills` repository as a reusable Hermes skill library.

## What this repo is for

`levelupskills` is a library of **profession-based startup skills**.

Use it when you want Hermes to reason more like:
- a founder operator
- a product lead
- a technical architect
- a DevOps / reliability lead
- a startup finance operator
- a startup lawyer / CA / CS-informed operator
- a growth, sales, support, or customer success lead

Do **not** use this repo as a place for project-specific decisions. Those belong in your product/company repo docs.

## 1. Add the repo as a Hermes skill tap

```bash
hermes skills tap add levelscorner/levelupskills
```

Verified behavior:
- Hermes accepts the repo as a tap source.
- `hermes skills tap list` shows it as:
  - repo: `levelscorner/levelupskills`
  - path: `skills/`

Check it:

```bash
hermes skills tap list
```

## 2. Install an individual skill directly from GitHub

If you want only one skill, install from the raw `SKILL.md` URL.

Example:

```bash
hermes skills install https://raw.githubusercontent.com/levelscorner/levelupskills/main/skills/management/startup-company-design/SKILL.md --yes
```

Verified behavior:
- the raw `SKILL.md` URL resolves successfully from GitHub
- `hermes skills install` accepts direct HTTP(S) identifiers

## 3. Load installed skills into Hermes sessions

Install only puts the skill on disk. To actively use it, load it into a session.

### Start a new session with skills preloaded

```bash
hermes -s startup-company-design
```

Multiple skills:

```bash
hermes -s startup-company-design,founder-operating-system,product-discovery-and-prioritization
```

### Load a skill inside a live session

```text
/skill startup-company-design
```

### If the skill does not appear immediately

Start a fresh session or reset:

```text
/reset
```

## 4. Recommended usage pattern

Do not load everything.

Instead, pick a small set of skills based on the current company stage.

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

## 5. Good operating rule

Use `levelupskills` like a library of reusable expert brains:

- skills = reusable professional thinking
- repo docs = project-specific application
- decision memos = company-specific calls
- product repo docs = implementation details

## 6. Example workflows

### Example: founder planning session

```bash
hermes -s startup-company-design,founder-operating-system
```

Then ask:
- "Map the missing functions in my startup."
- "Design my weekly operating cadence."
- "What should I build first versus later?"

### Example: pre-beta stack and legal setup

```bash
hermes -s technical-architecture-and-platform-decisions,india-tech-company-legal-compliance,startup-finance-and-unit-economics
```

Then ask:
- "What is the simplest architecture for this product?"
- "What legal and document stack do I need as an India-based SaaS founder?"
- "How should I think about runway and pricing at this stage?"

### Example: first-revenue GTM work

```bash
hermes -s founder-sales-for-b2b,gtm-and-growth-experiments,brand-positioning-and-messaging
```

Then ask:
- "Help me diagnose this sales pipeline."
- "What GTM experiments should I run first?"
- "Tighten this positioning for B2B buyers."

## 7. Repo maintenance guidance

When adding new skills to this repo:

- make them profession-based
- keep them reusable across many startups
- avoid founder-specific or repo-specific instructions in `SKILL.md`
- put specifics into references or separate repo docs
- prefer a small number of strong umbrella skills over many narrow one-offs
