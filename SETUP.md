# levelupskills setup

This file explains how to install and use `levelupskills` across Hermes and other agent systems.

## What this repo contains

`levelupskills` is a library of reusable `SKILL.md` files.

Each skill is intended to be:
- profession-shaped
- reusable across many founders, teams, and products
- portable across agent systems
- general-purpose rather than person-specific

## Current repo standard

The repo now expects skills to be stronger than lightweight notes.
A mature skill in this library should usually contain:
- trigger-rich frontmatter
- `## Overview`
- `## When to Use`
- counter-triggers
- category-specific workflow
- `## Common Pitfalls`
- `## Verification Checklist`
- `## Examples`

For the authoring standard, see:
- [`references/2026-2027-skill-authoring-standards.md`](./references/2026-2027-skill-authoring-standards.md)
- [`references/brutal-skill-audit.md`](./references/brutal-skill-audit.md)

## Quick setup by platform

| Platform | Install method | Runtime verified in this repo work | Notes |
|---|---|---:|---|
| Hermes | native tap / install commands | Yes | Best experience |
| Claude | copy `SKILL.md` into project instructions or reusable prompt | No | Manual setup; documented approach only |
| Cursor | copy `SKILL.md` into rules / project instructions | No | Manual setup; documented approach only |
| Gemini | copy `SKILL.md` into saved instructions or chat context | No | Manual setup; documented approach only |
| CLI / terminal agents | load `SKILL.md` into prompt file or instruction file | No | Manual setup; documented approach only |

## 1. Hermes setup

### Add the whole repo as a skill tap

```bash
hermes skills tap add levelscorner/levelupskills
```

Verify:

```bash
hermes skills tap list
```

### Install one skill directly

```bash
hermes skills install https://raw.githubusercontent.com/levelscorner/levelupskills/main/skills/management/startup-company-design/SKILL.md --yes
```

### Start Hermes with skills preloaded

```bash
hermes -s startup-company-design,founder-operating-system
```

### Load a skill inside a live Hermes session

```text
/skill startup-company-design
```

### Important Hermes note
Installing and loading are different:
- install puts the skill on disk
- load makes Hermes use it in the session

## 2. Portable setup for Claude, Cursor, Gemini, and similar agents

These systems usually do not share Hermes-style install semantics.
So the portable setup is instruction-based.

### General steps
1. choose the skill you want from `skills/<category>/<skill-name>/SKILL.md`
2. open the file
3. copy the instruction body
4. paste it into the target system's instruction surface
5. reuse it whenever that task class appears

### Where to paste it

| System | Good place to put the skill |
|---|---|
| Claude | project instructions, reusable prompt, or top of chat |
| Cursor | project rules, workspace instructions, or reusable prompt snippet |
| Gemini | saved instructions, project context, or top of chat |
| Other CLI agents | prompt file, rules file, preset, or startup instruction block |

## 3. Raw GitHub path pattern

Every skill can be addressed with this pattern:

```text
https://raw.githubusercontent.com/levelscorner/levelupskills/main/skills/<category>/<skill-name>/SKILL.md
```

Example:

```text
https://raw.githubusercontent.com/levelscorner/levelupskills/main/skills/communication/response-articulation-pattern/SKILL.md
```

Useful for:
- Hermes direct install
- quick raw-file access
- copying a skill into another system

## 4. Recommended starter setup

Do not load everything.
Start with a small pack.

### Founder / strategy starter pack
- `startup-company-design`
- `founder-operating-system`
- `startup-risk-register-and-decision-making`

### Product / research starter pack
- `product-discovery-and-prioritization`
- `customer-research-and-user-interviews`
- `brand-positioning-and-messaging`

### GTM / revenue starter pack
- `gtm-and-growth-experiments`
- `founder-sales-for-b2b`
- `customer-success-for-b2b`
- `concise-structured-communication`
- `verdict-first-writing`
- `response-articulation-pattern`

### Engineering / platform starter pack
- `technical-architecture-and-platform-decisions`
- `devops-and-reliability-planning`
- `security-privacy-and-risk-review`
- `payment-gateway-selection-for-software`

## 5. How to keep the repo clean

When adding or editing skills:
- keep the skill body agent-agnostic
- keep tool-specific setup notes in README, `SETUP.md`, or references
- avoid project-specific instructions in the main skill body
- prefer fewer strong skills over many thin ones
- add counter-triggers where skill overlap is likely
- include examples when a category is easy to misuse

## 6. Why there is no one universal install script

A universal script would mainly help Hermes.
Most other agent systems use different instruction surfaces instead of a common install command.

So the practical setup split is:
- **Hermes:** native commands
- **everything else:** portable `SKILL.md` copy/load workflow
