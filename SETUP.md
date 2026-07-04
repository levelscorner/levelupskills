# levelupskills setup

This file explains how to install and use `levelupskills` across Hermes and other agent systems.

## What this repo contains

`levelupskills` is a library of reusable `SKILL.md` files.

Each skill is meant to be:
- profession-based
- reusable across many founders, teams, and products
- portable across agent systems

## Quick setup by platform

| Platform | Install method | Runtime verified in this repo work | Notes |
|---|---|---:|---|
| Hermes | native tap / install commands | Yes | Best experience |
| Claude | copy `SKILL.md` into project instructions or reusable prompt | No | Manual setup; documented approach only |
| Cursor | copy `SKILL.md` into rules / project instructions | No | Manual setup; documented approach only |
| Gemini | copy `SKILL.md` into saved instructions or chat context | No | Manual setup; documented approach only |
| CLI / terminal agents | load `SKILL.md` into prompt file or instruction file | No | Manual setup; documented approach only |

## 1. Hermes setup

These commands were already tested during repo setup work.

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

### Start Hermes with a skill preloaded

```bash
hermes -s startup-company-design
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

These systems usually do not have a shared native skill installer.
So the portable setup is instruction-based.

### General steps

1. choose the skill you want from `skills/<category>/<skill-name>/SKILL.md`
2. open the file
3. copy the instruction body
4. paste it into the target system's instruction slot
5. reuse it whenever that kind of task appears

### Where to paste it

| System | Good place to put the skill |
|---|---|
| Claude | project instructions, reusable prompt, or top of chat |
| Cursor | project rules, workspace instructions, or reusable prompt snippet |
| Gemini | saved instructions, project context, or top of chat |
| Other CLI agents | prompt file, rules file, agent preset, or startup instruction block |

## 3. Raw GitHub path pattern

Every skill can be addressed with this pattern:

```text
https://raw.githubusercontent.com/levelscorner/levelupskills/main/skills/<category>/<skill-name>/SKILL.md
```

Example:

```text
https://raw.githubusercontent.com/levelscorner/levelupskills/main/skills/communication/concise-structured-communication/SKILL.md
```

This is useful when you want to:
- install directly in Hermes
- open the raw file quickly
- copy the skill into another agent system

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

### Engineering / platform starter pack
- `technical-architecture-and-platform-decisions`
- `devops-and-reliability-planning`
- `security-privacy-and-risk-review`
- `payment-gateway-selection-for-software`

## 5. Why there is no one universal install script

A universal script would only really help Hermes.
Most other agent systems use different instruction surfaces instead of a common install command.

So the right setup is:
- **Hermes:** native install commands
- **everything else:** portable `SKILL.md` copy/load workflow

## 6. Best practice for repo growth

When adding new skills:
- keep the skill body agent-agnostic
- keep tool-specific setup notes in README, `SETUP.md`, or references
- avoid project-specific instructions in the main skill body
- prefer fewer strong skills over many narrow ones
