---
name: verdict-first-writing
description: Use when the user wants the answer first, recommendation first, bottom line first, executive-summary-first writing, or no warm-up before the conclusion. Also use for recommendations, tradeoff calls, summaries for busy readers, founder updates, status notes, or replies where the main need is the conclusion before the reasoning. Do not use this as the main skill when the bigger problem is overall brevity or response-structure selection rather than answer ordering.
version: 1.1.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [communication, writing, verdict, recommendation, decision-making]
    related_skills: [concise-structured-communication, response-articulation-pattern, founder-communication-and-updates]
---

# Verdict First Writing

## Overview
Use this skill when the answer should come before the explanation. It is for moments when the reader mainly needs the call, not a long ramp into the call.

## When to Use
Use this skill when the main problem is **buried conclusion**.

Typical triggers:
- the user says verdict first, answer first, recommendation first, or bottom line first
- a busy reader needs the call before the supporting logic
- the output is a decision note, tradeoff call, or executive summary
- the answer must quickly resolve yes/no, choose A vs B, or recommend a next move

Do **not** use this as the main skill when:
- the real need is **overall compression** → use `concise-structured-communication`
- the real need is **choosing the right response shape** → use `response-articulation-pattern`
- the conclusion would be misleading without substantial setup, and the setup is part of the decision itself

## Core Principle
Do not make the reader hunt for the point.

## Default format
Use this structure unless the task clearly needs another format:

Verdict: one direct line with the answer, recommendation, or decision.

Why:
- 1 to 3 short bullets with the main reasons
- facts, tradeoffs, or signals only
- no long history section first

Next step: one short line saying what to do now.

## Workflow
1. Identify the real question or decision.
2. Write the answer in one plain line.
3. Add only the strongest supporting reasons.
4. Add one next action if action is needed.
5. Add caveats only if they materially change the decision.

## Writing rules
- Put the conclusion in the first line, not the last paragraph.
- Do not open with scene-setting unless it changes the decision.
- Prefer direct language over soft framing.
- If the answer is uncertain, say the uncertainty inside the verdict line.
- If there is a tradeoff, still give a recommendation.
- If the user asks for a yes or no, say yes or no clearly.

## When to expand
Expand only when the reader would otherwise misunderstand the decision:
- high-risk choice
- expensive or irreversible action
- close tradeoff where one caveat changes the call
- user explicitly asks for more evidence

## Common pitfalls
1. **Mistaking bluntness for clarity.** The verdict should be direct, not careless.
2. **Hiding uncertainty after an overconfident first line.** If uncertainty matters, it belongs in the verdict.
3. **Giving no action after the verdict.** Many verdicts are more useful with one clear next step.
4. **Using verdict-first when the task really needs a structured plan.** Do not force everything into one pattern.
5. **Front-loading a recommendation without enough support to trust it.** Keep the reasons short, but keep them real.

## Verification checklist
- [ ] I put the real answer in the first line.
- [ ] I kept only the strongest supporting reasons.
- [ ] I included uncertainty in the verdict when it materially changes the call.
- [ ] I used verdict-first because ordering was the main need, not because another communication skill should have led.

## Examples
### Example: vendor decision
Verdict: Pick Paddle.

Why:
- Faster to launch with tax and merchant-of-record handled.
- Lower operations burden for an early team.
- Good enough flexibility for the current stage.

Next step: Start integration with Paddle and revisit only if custom billing needs grow.

### Example: hiring decision
Verdict: Do not hire yet.

Why:
- Product scope is still moving.
- Process is not stable enough to onboard well.
- A new hire will likely increase coordination cost now.

Next step: Stabilize product direction first, then hire for the most constrained role.

### Example: technical choice
Verdict: Use Postgres, not a custom event store.

Why:
- Faster to ship.
- Easier to hire for and operate.
- Current scale does not justify extra complexity.

Next step: Keep architecture boring until scale creates a real problem.
