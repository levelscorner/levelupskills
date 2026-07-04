---
name: response-articulation-pattern
description: "Use when the user wants a response articulated clearly, structured well, easy to scan, and shaped to the task instead of dumped as loose prose. Also use when the answer needs the right response pattern for the situation: verdict, steps, comparison, summary, diagnosis, recommendation, or action plan. Helpful across Hermes, Claude, Cursor, Gemini, CLI agents, and chat apps. Do not use this as the main skill when the issue is primarily brevity or verdict ordering rather than structure selection."
version: 1.1.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [communication, writing, structure, articulation, clarity, formatting]
    related_skills: [concise-structured-communication, verdict-first-writing, founder-communication-and-updates]
---

# Response Articulation Pattern

## Overview
Use this skill to choose the right response shape for the task. The goal is not just to be correct. The goal is to make the answer easy to read, easy to trust, and easy to act on.

## When to Use
Use this skill when the main problem is **shape mismatch**.

Typical triggers:
- the answer feels messy, blob-like, or hard to scan
- the user wants something structured, articulated, or reformatted
- the task could be answered as steps, comparison, diagnosis, summary, or plan
- the agent is mixing several answer modes into one confusing block

Do **not** use this as the main skill when:
- the user mainly wants **fewer words** → use `concise-structured-communication`
- the user mainly wants the **answer first** → use `verdict-first-writing`
- a domain skill already defines a strict output format that should take priority

## Core Principle
Different tasks need different response shapes. A good response is not one long generic paragraph. It is a structure that matches what the reader needs.

## Workflow
1. Identify the user's real need: answer, steps, comparison, summary, diagnosis, recommendation, or plan.
2. Choose the lightest structure that fits that need.
3. Put the most important information first.
4. Group related points together.
5. Remove anything that does not help understanding or action.
6. End with a clear takeaway, recommendation, or next step when useful.

## Choose the right pattern
### 1. Direct answer
Use when the user wants a clear answer or call.

Format:
- Answer
- 1 to 3 supporting points
- next step if needed

### 2. Steps
Use when the user needs execution.

Format:
- Goal
- Step 1
- Step 2
- Step 3
- watch-out or verification note

### 3. Comparison
Use when the user is choosing between options.

Format:
- Goal
- Option A strengths
- Option B strengths
- key difference
- recommendation

### 4. Summary
Use when the user wants compression.

Format:
- Topic
- key points
- takeaway

### 5. Diagnosis
Use when something is wrong and the user needs cause and next check.

Format:
- Problem
- strongest signals
- likely cause
- next check or fix

### 6. Plan
Use when the user needs a sequence of work.

Format:
- objective
- workstreams or phases
- first move
- risks or blockers

## Writing rules
- Use headings, bullets, or short blocks when they improve scanning.
- Keep one idea per bullet when possible.
- Use simple English unless technical language is necessary.
- Do not mix summary, comparison, diagnosis, and action plan into one messy blob.
- If the user asks for a format, honor it.
- If no format is requested, choose the one that best helps the reader act.

## When to stay short
Stay compact when:
- the user asked for brevity
- the task is simple
- one structure can answer it cleanly

## When to expand
Expand when:
- the user needs steps
- the reasoning matters to trust the answer
- there are real tradeoffs
- risk or ambiguity must be surfaced

## Common pitfalls
1. **Choosing a fancy structure when a simple answer would do.** Structure should clarify, not decorate.
2. **Mixing multiple response patterns at once.** This is how answers turn muddy.
3. **Over-formatting trivial answers.** Not every reply needs sections and sub-sections.
4. **Ignoring domain constraints.** If a technical or legal skill requires a specific output shape, follow that.
5. **Solving shape but not substance.** Good articulation cannot rescue a weak answer.

## Verification checklist
- [ ] I identified the actual answer mode the task needed.
- [ ] I chose the lightest useful structure.
- [ ] I did not mix several incompatible response patterns into one blob.
- [ ] I used structure because shape selection was the main need, not because another communication skill should have led.

## Examples
### Example: comparison
Goal: Choose a payment stack

Option A strengths:
- Stripe gives more flexibility.
- Strong ecosystem and developer familiarity.

Option B strengths:
- Paddle reduces compliance and tax burden.
- Faster for a small team to operate.

Key difference: Stripe optimizes for control; Paddle optimizes for simplicity.

Recommendation: Pick Paddle now if speed and lower operations matter most.

### Example: diagnosis
Problem: Signups are dropping.

Strongest signals:
- Landing page traffic is flat.
- Signup completion rate fell after the new form change.
- Error logs show more validation failures.

Likely cause: The new signup form added friction and validation breakage.

Next check or fix: Roll back the form change and inspect validation errors first.

### Example: steps
Goal: Launch the repo skills in Hermes fast.

Step 1: Add the repo as a skill tap.
Step 2: Install the specific skill you need.
Step 3: Start Hermes with that skill or load it into the live session.

Watch-out: Installing a skill is not the same as loading it into the session.
