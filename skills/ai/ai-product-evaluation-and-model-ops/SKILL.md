---
name: ai-product-evaluation-and-model-ops
description: "Use when the user asks how to evaluate AI product quality, choose models, design prompts or system behavior, manage cost-quality-latency trade-offs, implement routing or fallback strategy, build evals, or run operational practices for AI features in a product. Also use when the user needs a reusable professional lens on AI product operations rather than one-off prompt tinkering. Do not use this as the main skill for pure model ecosystem research or pure software architecture work when no AI operating question is central."
version: 1.1.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [AI, evaluation, model-ops, prompts, routing, product-ops]
    related_skills: [agentic-stack-research, analytics-and-metrics-system, technical-architecture-and-platform-decisions]
---

# AI Product Evaluation and Model Ops

## Overview
Use this skill to evaluate and operate AI features as product systems, not just prompts or model calls. The point is to make an AI feature reliable enough to earn trust under real usage, not just to make a demo look impressive.

## When to Use
Use this skill when the main problem is **operating an AI feature in production or near-production conditions**.

Typical triggers:
- choosing a model for a real product workflow
- deciding how to evaluate AI quality beyond vibes
- designing fallback, routing, guardrails, or escalation logic
- balancing latency, cost, and quality
- planning monitoring, failure review, and iteration loops
- diagnosing why an AI feature works in demos but not reliably for users

Do **not** use this as the main skill when:
- the task is mainly technology-market research about model vendors or frameworks → use `agentic-stack-research`
- the task is mostly general architecture shape without AI-quality operations as the focus → use `technical-architecture-and-platform-decisions`
- the task is simple prompt editing with no product-ops or evaluation question

## Core Principle
An AI product becomes trustworthy when quality, latency, cost, fallback behavior, and failure review are managed as one operating system rather than as isolated experiments.

## Always cover
- task definition and user expectation
- error tolerance and risk level
- quality / latency / cost trade-offs
- eval design: offline, online, and human review
- routing, fallback, and escalation behavior
- monitoring and failure taxonomy
- what should be optimized now versus later

## Workflow
1. Identify the user job, desired output quality, and what failure actually means.
2. Separate offline evaluation, online behavior, and operator controls.
3. Review model choice, prompt/system design, context design, routing, guardrails, fallback paths, and human escalation if needed.
4. Recommend an evaluation system tied to product outcomes rather than benchmark theater.
5. Define monitoring and review loops for cost, quality, latency, and failure clusters.
6. Distinguish immediate reliability work from later sophistication.

## Evaluation lenses
### 1. Task quality
Ask:
- what does a good output look like?
- what failures are acceptable, annoying, or dangerous?
- does the task need deterministic accuracy, helpful approximation, or creative usefulness?

### 2. Operational behavior
Review:
- latency tolerance
- context-window fit
- cost per successful outcome
- fallback behavior under rate limits or degraded quality
- user-visible failure handling

### 3. Feedback and iteration loop
Require:
- representative eval set
- failure categories
- review rhythm
- owner for quality and cost changes

## Output format
Return:
1. AI system diagnosis
2. current trade-off view: quality / cost / latency / risk
3. recommended model-ops design
4. evaluation and monitoring plan
5. immediate fixes vs later optimizations

## Stage guidance
### Early stage
- optimize for baseline usefulness and visible failure handling
- prefer simpler routing and fewer moving parts
- build the first eval set before complex orchestration

### Growing product
- add clearer segmentation by task type or user tier
- monitor failure clusters and fallback performance
- introduce more deliberate cost controls and alerting

### Mature / sensitive workflows
- require tighter risk controls
- add human review or escalation where appropriate
- use stricter eval governance and rollback rules

## Common pitfalls
1. **Optimizing prompts without defining task quality.** You cannot improve what nobody has defined.
2. **No eval set or failure taxonomy.** Teams then confuse anecdotes with evidence.
3. **Routing complexity before baseline reliability exists.** Fancy orchestration often hides weak fundamentals.
4. **Judging success only by output vibes.** Product quality needs repeatable evaluation.
5. **Treating fallback as an edge case.** Real systems degrade; good ones degrade intentionally.
6. **Ignoring user trust mechanics.** If users cannot understand or recover from failure, the feature feels broken even when average quality is decent.

## Verification checklist
- [ ] I treated the AI feature as a product system, not a single prompt.
- [ ] I covered quality, latency, cost, and risk together.
- [ ] I recommended explicit offline and online evaluation loops.
- [ ] I addressed fallback, escalation, or degraded-mode behavior where relevant.
- [ ] I separated immediate reliability work from later sophistication.

## Examples
### Example: support copilot
Return:
1. Quality target is helpful draft generation, not autonomous customer commitment.
2. Main risk is confident policy hallucination, not creativity failure.
3. Start with one model, limited routing, and clear human approval.
4. Build evals around policy accuracy, tone, latency, and escalation correctness.
5. Add fallback to safe template responses when retrieval or model confidence is weak.

### Example: AI feature cost spike
Return:
1. Product quality is acceptable, but cost per successful action is unstable.
2. Diagnose long-context overuse and weak task segmentation.
3. Route simple tasks to cheaper paths and reserve premium models for high-value cases.
4. Track cost per accepted output, not just cost per request.
5. Reassess prompt and context design before adding more providers.
