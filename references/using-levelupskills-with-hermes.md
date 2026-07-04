# Using levelupskills across Hermes and other agent systems

This guide explains how to use the `levelscorner/levelupskills` repository both inside Hermes and outside Hermes.

For installation and setup, start with [`SETUP.md`](../SETUP.md).

## Core idea

`levelupskills` is a library of **profession-based reusable skill files**.

Each `SKILL.md` is meant to improve how an agent thinks, structures work, or communicates.

That means the library should work in:
- Hermes
- Claude
- Cursor
- Gemini
- Codex-style terminal agents
- other chat or CLI agent systems

## 1. Best experience: Hermes

Hermes supports native skill install and loading.

### Add the repo as a Hermes skill tap

```bash
hermes skills tap add levelscorner/levelupskills
```

Check it:

```bash
hermes skills tap list
```

### Install one skill directly

```bash
hermes skills install https://raw.githubusercontent.com/levelscorner/levelupskills/main/skills/management/startup-company-design/SKILL.md --yes
```

### Load skills into a Hermes session

New session:

```bash
hermes -s startup-company-design
```

Live session:

```text
/skill startup-company-design
```

If needed, start fresh with:

```text
/reset
```

## 2. Use outside Hermes

Other systems may not have native skill install.
That is fine.
The skills are still usable.

### General rule

For Claude, Cursor, Gemini, or similar systems:
1. open the relevant `SKILL.md`
2. copy the instructions
3. paste them into the system prompt, project instructions, agent preset, memory/rules file, or reusable template the tool supports
4. use that skill when working on the matching task

## 3. Example ways to use the same skill outside Hermes

### Claude
- paste a skill into a project instruction or a reusable prompt
- or paste the relevant sections at the start of the conversation

### Cursor
- place the skill logic in project rules, workspace instructions, or a reusable prompt snippet
- especially useful for writing, product, architecture, and founder-workflow skills

### Gemini
- paste the skill into the chat context or saved instruction set
- use it as a reusable response pattern or expert role file

### Terminal / CLI agents
- store the `SKILL.md` beside the repo
- load it into the prompt or instruction file used by that agent
- reuse it as a standard operating prompt

## 4. Good portable usage rule

Do not think of these as Hermes-only features.
Think of them as **high-quality instruction files**.

Hermes can load them natively.
Other agents can still use them by copy/paste or by attaching them to their own instruction systems.

## 5. Communication skill example

The communication skill `concise-structured-communication` is a good example of portability.

It works in any system because it only defines:
- when to be concise
- how to structure the answer
- how to end with a verdict
- when to expand for safety or clarity

That pattern works almost everywhere.

## 6. Recommended usage pattern

Do not load everything.
Pick a small set based on the current company stage or task.

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
- `concise-structured-communication`

## 7. Repo maintenance rule

When adding new skills:
- make them profession-based
- keep them reusable across many startups
- avoid founder-specific or repo-specific instructions in `SKILL.md`
- write them so they still make sense outside Hermes
- put tool-specific usage notes in README or references, not in the core skill logic
