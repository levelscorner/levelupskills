# 2026-2027 skill authoring standards

This document captures the **practical standard** that is emerging across modern agent systems in 2026 and likely to remain stable into 2027.

It is based on the patterns visible in:
- Hermes Agent docs and bundled skill catalog
- Claude Code docs around instructions, memories, skills, hooks, and context
- OpenAI Agents SDK docs around tools, guardrails, handoffs, sessions, and structured orchestration
- Google Gemini prompt-design guidance

This is not a formal standards body spec. It is a **best-practice convergence map** for building reusable skills that survive across agent runtimes.

## Core 2026-2027 standard

A strong skill now has to do **five jobs at once**:
1. trigger correctly
2. shape the agent's reasoning reliably
3. reduce repeated mistakes
4. stay portable across platforms
5. avoid overfitting to one founder, one repo, or one lucky prompt

That means the old style of "short smart note with a few bullets" is no longer enough.

## Cross-platform principles that now look standard

### 1. Trigger-rich frontmatter
The description is not decoration.
It is the **primary routing layer**.

Good modern descriptions:
- start with `Use when ...`
- include concrete trigger classes
- include synonyms users actually say
- distinguish the skill from adjacent skills
- avoid vague words like "helps with strategy"

Bad:
- too short
- too abstract
- no counter-trigger boundaries
- duplicates another skill's trigger territory

### 2. Clear body structure
A reusable skill should usually have this shape:
- `## Overview`
- `## When to Use`
- `## Core Principle` or `## Core Principles`
- `## Always cover` and/or `## Workflow`
- `## Output format`
- `## Common pitfalls`
- `## Verification checklist`
- optional `## Examples` or `## Reference files`

This is not bureaucracy.
It helps the agent find the right instruction at the right time.

### 3. Counter-triggers are now mandatory
A skill that says only when to use it will overtrigger.
A skill that never says what it is **not** for becomes a routing collision.

Modern skills need at least one of:
- `Do not use when ...`
- `Use another skill when ...`
- explicit neighboring-skill boundary language

### 4. Completion criteria beat motivational prose
Good skills do not say:
- be thoughtful
- be strategic
- be comprehensive

Good skills say:
- separate reversible from irreversible decisions
- distinguish current bottleneck from future maturity work
- state the downside of inaction
- end with a direct recommendation

The best 2026 skills change agent behavior through **checkable moves**, not vibes.

### 5. Progressive disclosure
The body should contain the rules needed almost every time.
Bulky references should live in linked files.

Strong pattern:
- small routing description
- medium-size core skill body
- references for long domain material, templates, official-source maps, or category playbooks

### 6. Tool/runtime agnostic core
The core professional reasoning should survive outside Hermes.
Platform-specific instructions should stay in:
- README
- SETUP docs
- linked references
- optional scripts/templates

A good cross-agent skill still makes sense if copied into Claude, Cursor, Gemini, or another instruction surface.

### 7. Evidence and guardrails by domain
By 2026, the best skills do not just tell the model what answer shape to produce.
They also define:
- what evidence counts
- what assumptions must be separated from facts
- what risks must be surfaced
- what must be escalated to humans or professionals

### 8. Stage-aware reasoning
Most business/operator skills fail because they ignore stage.
A modern reusable skill should adapt for:
- idea
- pre-beta
- beta
- early revenue
- scaling

Without stage logic, advice collapses into generic blog sludge.

### 9. Examples and evalability
Examples are no longer optional fluff.
They help:
- trigger quality
- portability
- evaluation
- future iteration

Not every skill needs a long example bank, but the library should have enough examples somewhere to test skill boundaries.

### 10. Verification language inside the skill
A strong skill now includes some form of self-check:
- did the agent name the main risks?
- did it adapt to stage?
- did it separate now vs later?
- did it provide an action-oriented recommendation?

This sharply reduces premature completion and generic outputs.

## Category-specific standards

## Research skills
Use when the task is about truth-finding, evidence synthesis, or market/technology interpretation.

Required patterns:
- source hierarchy
- recency awareness
- distinction between hype and adoption
- distinction between fact and inference
- negative case: what happens if nothing changes
- direct verdict at the end

Best practice extras:
- official-source-first where possible
- evidence tier labels
- required internal questions before final answer
- tables for option comparison

## Communication skills
Use when the skill's job is answer shape, brevity, articulation, or decision readability.

Required patterns:
- clear trigger separation between brevity vs answer-first vs structure-selection
- audience/readership awareness
- over-compression guardrails
- examples because communication skills are easy to misunderstand

Best practice extras:
- explicit conflict rule: clarity beats style gimmicks
- short vs expanded mode rule
- sections for when not to compress

## Management / founder / operations skills
Use when the task is operating cadence, prioritization, company design, or decision hygiene.

Required patterns:
- stage awareness
- bottleneck diagnosis
- now vs later separation
- priority order instead of unordered advice
- concrete review rhythms or decision rules

Best practice extras:
- escalation triggers
- decision log logic
- risk-register tie-in

## Product / growth / sales / customer-success / community / partnerships
Use when the task involves user learning, demand creation, deal motion, retention, or ecosystem growth.

Required patterns:
- actor map: who matters here
- incentive map
- lifecycle stage or funnel stage
- feedback/learning loop
- metrics that matter now
- warning against vanity motion

Best practice extras:
- experiment sequencing
- failure-mode language
- distinction between acquisition, activation, retention, expansion, and advocacy

## Engineering / AI / analytics / security / payments / legal / vendor selection
Use when the task touches systems, operational risk, regulated decisions, or architecture.

Required patterns:
- evidence and risk hierarchy
- explicit tradeoffs
- reversibility vs irreversibility
- operational burden
- safety/compliance boundary
- what must be verified with official docs, counsel, or real measurements

Best practice extras:
- default assumptions section
- official-source-first note
- implementation boundary note: strategy vs coding work

## Finance / pricing
Use when the task involves economic logic, monetization, margin, runway, or packaging decisions.

Required patterns:
- value logic, not slogan logic
- margin/cost awareness
- stage-appropriate sophistication
- what to test later vs lock now
- downside/failure modes

Best practice extras:
- scenario thinking
- sensitivity to support burden and operational complexity

## What the current repo was missing before remediation

The common failure pattern in this repo was not bad taste.
It was **under-specification**.

Typical weaknesses:
- many skills were too short to be robust
- many had no `## When to Use` body section
- many had no counter-triggers
- many had no pitfalls/checklist
- some had overlapping trigger areas without boundary language
- most had no explicit examples or eval hooks

That is enough to make a library look smart while still underperforming in real routing.

## Practical authoring rule for this repo

Every new skill should pass this test:

> If another agent loads only this file with no extra context, will it know when to use it, when not to use it, what to cover, how to finish, and how to avoid sounding generic?

If the answer is no, the skill is not ready.
