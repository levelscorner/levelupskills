---
name: startup-risk-register-and-decision-making
description: "Use when the user asks how a startup should think about risk, uncertainty, decision hygiene, trade-off framing, founder decision logs, escalation triggers, or how to avoid drifting into avoidable mistakes. Also use when the user needs a structured operating lens on risk and decision quality rather than vibes or post-hoc rationalization. Do not use this as the main skill for legal/compliance detail or weekly operating cadence when the core issue is not decision-risk discipline."
version: 1.1.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [risk, decision-making, founder, uncertainty, trade-offs]
    related_skills: [founder-operating-system, startup-company-design, security-privacy-and-risk-review]
---

# Startup Risk Register and Decision Making

## Overview
Use this skill to help a startup make better decisions under uncertainty and keep important risks visible before they become expensive surprises. The goal is not paranoia. The goal is disciplined awareness and cleaner trade-offs.

## When to Use
Use this skill when the main problem is **decision hygiene under uncertainty**.

Typical triggers:
- recurring avoidable surprises
- no clear view of top risks
- big trade-offs being made informally
- founder decisions are being forgotten or re-litigated
- the team needs escalation triggers or better decision logging
- risk is being discussed vaguely instead of operationally

Do **not** use this as the main skill when:
- the issue is company cadence → use `founder-operating-system`
- the issue is deep security/privacy risk → use `security-privacy-and-risk-review`
- the issue is legal advice or compliance interpretation

## Core Principle
Good decision-making under uncertainty comes from making risk visible, separating reversible from irreversible calls, and defining what would force a change in view.

## Always cover
- top risks and assumptions
- reversible vs irreversible decisions
- leading indicators or warning signals
- escalation triggers
- decision log hygiene
- now-vs-later mitigation logic

## Workflow
1. Identify the decision surface and current uncertainty.
2. Map the major assumptions and concentrated risks.
3. Separate reversible calls from high-cost irreversible ones.
4. Recommend a lightweight risk register and decision-recording approach.
5. Define triggers that should force review, escalation, or reversal.

## Output format
Return:
1. decision-risk diagnosis
2. top risks and assumptions
3. recommended register / logging approach
4. escalation and review triggers
5. mitigation and next actions

## Common pitfalls
1. **Treating risk as a one-time brainstorm.** Risks need review, not just naming.
2. **Logging decisions without triggers.** History alone does not improve judgment.
3. **Acting as if reversible and irreversible decisions are the same.** They are not.
4. **Using vague fear language instead of specific failure modes.** Specificity makes action possible.
5. **Overbuilding risk process too early.** The register should help decisions, not bury them.

## Verification checklist
- [ ] I identified concentrated risks and assumptions.
- [ ] I separated reversible from irreversible decisions.
- [ ] I defined escalation or review triggers.
- [ ] I recommended lightweight but durable risk/decision hygiene.

## Examples
### Example: founder uncertainty
Return:
1. The problem is not lack of ideas; it is unclear trade-off discipline.
2. Create a simple risk register around product, GTM, finance, and execution assumptions.
3. Add one decision log with owner, date, rationale, and revisit trigger.
4. Focus review on risks that could break the company, not every annoyance.
5. Revisit monthly or on explicit trigger events.

### Example: risky product bet
Return:
1. The proposed bet is not inherently wrong, but the downside is under-specified.
2. Define the assumption being tested and what evidence would falsify it.
3. Treat spend and time exposure explicitly.
4. Add an escalation checkpoint before deeper commitment.
5. Do not let momentum substitute for decision quality.
