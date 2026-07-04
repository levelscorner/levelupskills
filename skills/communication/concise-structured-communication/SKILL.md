---
name: concise-structured-communication
description: Use when the user wants a short, clear, low-wording response with simple English, few lines, direct conclusions, verdict-first communication, compact summaries, or minimal explanation. Also use when the user says be brief, concise, to the point, verdict first, simple format, topic-body-verdict, or does not want long prose.
version: 1.0.0
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

## Core Principle
Most people do not want a wall of text. Good concise communication gives the answer fast, keeps only the useful facts, and ends with a clear verdict.

## Workflow
1. Identify the user's actual question, decision, or requested output.
2. Remove filler, repetition, hedging, long setup, and obvious restatements.
3. Keep only the minimum facts needed to answer correctly.
4. Prefer short sentences, plain words, and direct recommendations.
5. Use the Topic / Body / Verdict structure unless the user requests a different format.

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

## When to expand
Expand beyond the default short format only when:
- safety or irreversible action needs explanation
- the user explicitly asks for detail
- the task needs steps, evidence, or comparison to avoid confusion
- the output would become misleading if over-compressed

## Example
Topic: Why app is slow

Body:
- Database query takes too long.
- No index on the filtered column.
- CPU is fine. Bottleneck is database.

Verdict: Add the missing index first.
