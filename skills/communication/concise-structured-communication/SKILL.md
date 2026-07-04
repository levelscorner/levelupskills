---
name: concise-structured-communication
description: Use when the user wants a short, clear, low-wording response with simple English, few lines, direct conclusions, verdict-first communication, compact summaries, minimal explanation, concise comparisons, short decision notes, or stripped-down summaries. Also use when the user says be brief, concise, to the point, simple English, verdict first, topic-body-verdict, no long explanation, few lines, or answer like a busy human would want to read.
version: 1.1.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [communication, concise, writing, summaries, verdict, brevity]
    related_skills: [founder-communication-and-updates, brand-positioning-and-messaging]
---

# Concise Structured Communication

## Overview
Use this skill to turn answers into short, readable communication with low word count, simple English, and a direct conclusion.

This skill is not tied to one agent platform. It should work well in chat apps, IDE assistants, terminal agents, and general-purpose LLM conversations.

## Core Principle
Most people do not want a wall of text. Good concise communication gives the answer fast, keeps only the useful facts, and ends with a clear verdict.

## Workflow
1. Identify the user's real question, decision, or requested output.
2. Remove filler, repetition, hedging, long setup, and obvious restatements.
3. Keep only the minimum facts needed to answer correctly.
4. Prefer short sentences, plain words, and direct recommendations.
5. Use the Topic / Body / Verdict structure unless the user requests a different format.
6. Expand only when detail is needed for safety, correctness, or avoiding confusion.

## Always cover
- what this is about
- essential facts only
- direct answer or recommendation
- simple English
- no padding
- no explanation unless needed for correctness or safety

## Output format
Default to this exact structure when it fits:

Topic: one line saying what this is about.

Body:
- 1 to 3 short bullets or short lines
- only the key facts, actions, or differences
- no long background unless required

Verdict: one line with the answer, recommendation, or conclusion.

## Compression rules
- Lead with the answer, not the warm-up.
- Prefer one clear sentence over three soft sentences.
- Replace complex words with simpler ones when meaning stays intact.
- Cut throat-clearing like "here's the thing," "to clarify," or "it is important to note."
- Do not list every edge case unless the user asked for depth.
- If risk is high, still be concise, but do not omit the warning.
- If the user asks for a verdict, give the verdict plainly.
- If the user asks for comparison, keep only the main differences.

## When to expand
Expand beyond the default short format only when:
- safety or irreversible action needs explanation
- the user explicitly asks for detail
- the task needs steps, evidence, or comparison to avoid confusion
- the output would become misleading if over-compressed

## Cross-platform usage note
Use the same communication pattern whether the answer is going into:
- Hermes
- Claude
- Cursor
- Gemini
- Codex-style or terminal agents
- chat apps like Telegram, Slack, Discord, WhatsApp, or similar

The point is not the tool. The point is readable human communication.

## Trigger phrases and situations
Apply this skill when the user says or clearly implies things like:
- be brief
- keep it short
- concise answer
- simple English
- just tell me the answer
- verdict first
- no long explanation
- few lines only
- topic body verdict
- summarize this quickly
- compare in short
- give me the conclusion
- answer like a human with no fluff

Also apply it when the context suggests the reader is busy and mainly needs:
- a quick answer
- a short summary
- a short comparison
- a direct recommendation
- a decision-ready note

## Examples
### Example: Q and A
Topic: Best next step

Body:
- Traffic is low.
- Product feedback is still weak.
- Paid ads now will waste money.

Verdict: Fix feedback and activation before spending on ads.

### Example: Summary
Topic: Meeting summary

Body:
- Team agreed to ship beta next week.
- Login bug is still open.
- Founder owns pricing page update.

Verdict: Launch is on, but login bug must close first.

### Example: Comparison
Topic: Stripe vs Paddle

Body:
- Stripe gives more control.
- Paddle is easier for tax and merchant-of-record setup.
- Paddle usually fits faster early-stage launch.

Verdict: Pick Paddle if speed and compliance matter more than control.

### Example: Decision note
Topic: Should we hire now

Body:
- Core product is still changing.
- Process is not stable yet.
- New hire may amplify chaos.

Verdict: Do not hire yet. Stabilize first.

### Example: Technical diagnosis
Topic: Why app is slow

Body:
- Database query takes too long.
- No index on the filtered column.
- CPU is fine. Bottleneck is database.

Verdict: Add the missing index first.
