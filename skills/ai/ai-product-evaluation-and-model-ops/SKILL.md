---
name: ai-product-evaluation-and-model-ops
description: Use when the user asks how to evaluate AI product quality, model choice, prompt/system performance, cost-quality trade-offs, routing, fallback strategy, eval design, or operational practices for AI features in a product. Also use when the user needs a reusable professional lens on AI product operations rather than one-off prompt tinkering.
version: 1.0.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [AI, evaluation, model-ops, prompts, routing, product-ops]
    related_skills: [agentic-stack-research, analytics-and-metrics-system, technical-architecture-and-platform-decisions]
---

# AI Product Evaluation and Model Ops

## Overview

Use this skill to evaluate and operate AI features as product systems, not just as prompts or model calls.

## Core Principle

An AI product becomes trustworthy when quality, latency, cost, fallback behavior, and failure review are managed as an operating system rather than as isolated experiments.

## Workflow

1. Identify the AI use case, risk level, and user expectation.
2. Separate offline evaluation, online behavior, and operator controls.
3. Review model choice, prompt/system design, routing, guardrails, and fallback paths.
4. Recommend evals, monitoring, and review loops tied to product outcomes.
5. Define what should be optimized now versus later.

## Always cover

- task definition and user expectation
- quality / latency / cost trade-offs
- routing and fallback design
- eval methodology
- monitoring and failure review
- product-risk and trust implications

## Output format

Return:
1. AI system diagnosis
2. current risk / quality trade-off view
3. model-ops recommendation
4. evaluation and monitoring plan
5. next optimization priorities

## Common pitfalls

- optimizing prompts without defining task quality
- no eval set or failure taxonomy
- routing complexity before baseline reliability exists
- judging success only by model output vibes

## Verification checklist

- [ ] I treated the AI feature as a product system.
- [ ] I covered quality, cost, latency, and risk together.
- [ ] I recommended explicit eval and monitoring loops.
- [ ] I separated immediate controls from later sophistication.
