---
name: verdict-first-writing
description: Use when the user wants the answer first, recommendation first, bottom line first, executive-summary-first writing, decision-ready output, or no warm-up before the conclusion. Also use for recommendations, tradeoff calls, summaries for busy readers, founder updates, status notes, or any reply where the user mainly needs the conclusion before the reasoning.
version: 1.0.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [communication, writing, verdict, recommendation, summaries, decision-making]
    related_skills: [concise-structured-communication, response-articulation-pattern, founder-communication-and-updates]
---

# Verdict First Writing

## Overview
Use this skill when the answer should come before the explanation.

It is for moments when the reader is busy and wants the conclusion fast.

## Core Principle
Do not make the reader hunt for the point.

State the answer, recommendation, or decision first. Then give only the support needed to trust that answer.

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
- Do not open with context, thanks, or scene-setting.
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

## Cross-platform usage note
This pattern works across:
- Hermes
- Claude
- Cursor
- Gemini
- terminal or CLI agents
- chat apps and internal team messages

The platform does not matter. The reader's attention does.

## Trigger phrases and situations
Use this skill when the user says or clearly implies things like:
- just give me the answer
- verdict first
- bottom line first
- recommendation first
- what should I do
- don't bury the lead
- executive summary
- short decision note
- give me the call
- answer first, reasons after

Also use it when the response is mainly for:
- a founder
- an executive
- a busy operator
- a decision maker
- a summary sent to a team or stakeholder

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
