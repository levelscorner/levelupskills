---
name: concise-structured-communication
description: Use when the user wants a short, clear, low-wording response with simple English, few lines, direct conclusions, compact summaries, concise comparisons, short decision notes, or minimal explanation. Also use when the user says be brief, concise, to the point, simple English, no fluff, few lines, or answer like a busy human would want to read. Do not use this as the main skill when the real need is verdict ordering or response-pattern selection; pair or defer to those adjacent skills when that distinction matters.
version: 1.2.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [communication, concise, writing, summaries, brevity, clarity]
    related_skills: [verdict-first-writing, response-articulation-pattern, founder-communication-and-updates]
---

# Concise Structured Communication

## Overview
Use this skill to compress an answer without making it useless. The job is not to sound clipped for style points. The job is to remove drag, keep the necessary facts, and leave the reader with a clean answer they can absorb fast.

## When to Use
Use this skill when the main problem is **too many words**.

Typical triggers:
- the user wants brevity, plain English, or low word count
- a long answer needs to be compressed into a usable summary
- a comparison, diagnosis, or recommendation should be shorter
- the reader is busy and only needs essentials
- the output is becoming bloated with warm-up, restatement, or filler

Do **not** use this as the primary skill when:
- the main issue is **answer ordering** rather than length → use `verdict-first-writing`
- the main issue is **choosing the right structure** for a messy answer → use `response-articulation-pattern`
- high-risk context requires detail that cannot safely be compressed

## Core Principle
Concise writing is not small writing. It is writing with a high signal-to-noise ratio.

## Always cover
- what the question is really about
- only the facts needed for a correct answer
- the direct answer or recommendation
- plain language where possible
- any warning that materially changes the decision

## Workflow
1. Identify the user's actual question, decision, or requested output.
2. Remove filler, repetition, hedging, throat-clearing, and obvious restatements.
3. Keep only the minimum facts required for correctness.
4. Prefer short sentences, plain words, and direct recommendations.
5. Use a compact structure that still preserves clarity.
6. Expand only when detail is needed for safety, correctness, or avoiding confusion.

## Output format
Default to this structure when it fits:

Topic: one line saying what this is about.

Body:
- 1 to 3 short bullets or short lines
- only the key facts, actions, or differences
- no long background unless required

Verdict: one line with the answer, recommendation, or conclusion.

## Compression rules
- Lead with substance, not warm-up.
- Prefer one clear sentence over three soft ones.
- Replace complex words with simpler ones when meaning stays intact.
- Cut phrases like "to clarify," "it is important to note," or "here's the thing" unless they add meaning.
- Do not list every edge case unless the user asked for depth.
- If risk is high, stay concise but do not omit the warning.
- If the user wants a verdict, give the verdict plainly.

## When to expand
Expand beyond the default short format only when:
- safety or irreversible action needs explanation
- the user explicitly asks for detail
- the task needs steps, evidence, or comparison to avoid confusion
- over-compression would make the answer misleading

## Common pitfalls
1. **Compressing away the real answer.** Shorter is not better if the decision becomes unclear.
2. **Cutting the warning but keeping the recommendation.** Dangerous in legal, security, or financial contexts.
3. **Using telegraphic fragments that feel lazy.** The output should still read like intentional writing.
4. **Confusing brevity with verdict-first.** Sometimes the answer should be short but not necessarily front-loaded the same way.
5. **Flattening nuance that actually matters.** If one caveat changes the call, keep it.

## Verification checklist
- [ ] I reduced words without removing the core answer.
- [ ] I kept the language simple and direct.
- [ ] I preserved any warning that changes the decision.
- [ ] I chose brevity because the main need was compression, not because another communication skill should have handled it.

## Examples
### Example: summary
Topic: Meeting summary

Body:
- Team agreed to ship beta next week.
- Login bug is still open.
- Founder owns pricing page update.

Verdict: Launch is on, but the login bug must close first.

### Example: comparison
Topic: Stripe vs Paddle

Body:
- Stripe gives more control.
- Paddle is easier for tax and merchant-of-record setup.
- Paddle usually fits a faster early-stage launch.

Verdict: Pick Paddle if speed and compliance matter more than control.

### Example: technical diagnosis
Topic: Why app is slow

Body:
- Database query is the bottleneck.
- No index exists on the filtered column.
- CPU is not the main issue.

Verdict: Add the missing index first.
