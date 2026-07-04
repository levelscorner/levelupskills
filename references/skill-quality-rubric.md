# Skill Quality Rubric

This rubric is for contributors reviewing or authoring `levelupskills` entries.

Use it before opening a PR, when reviewing a change, or when deciding whether a thin skill is ready to merge.

## Scoring model

Score each dimension from **0 to 3**.

- **0 = missing or wrong**
- **1 = weak / partial**
- **2 = solid**
- **3 = excellent**

A strong merge-ready skill should usually:
- score **at least 2** on every core dimension
- score **18+ / 24** overall on the six core dimensions below
- have **no 0s** in trigger clarity, workflow quality, or boundary clarity

## The six core dimensions

### 1. Trigger clarity
**Question:** Does the skill clearly tell the agent when it should load?

Score guide:
- **0:** Trigger is vague, generic, or missing.
- **1:** Trigger exists but could match too many unrelated tasks.
- **2:** Trigger is clear and practically useful.
- **3:** Trigger is sharp, rich in examples, and hard to misroute.

What good looks like:
- description starts with `Use when ...`
- concrete trigger examples are included
- the task class is obvious within a few lines

### 2. Boundary clarity
**Question:** Does the skill say what it is *not* for?

Score guide:
- **0:** No adjacent-skill boundaries.
- **1:** Boundaries exist but are too weak or generic.
- **2:** Main overlap areas are handled well.
- **3:** Boundaries are explicit, realistic, and prevent routing confusion.

What good looks like:
- `Do not use this as the main skill when ...`
- references to adjacent skills where appropriate
- clear separation from neighboring categories

### 3. Workflow quality
**Question:** Does the skill provide a usable operating sequence, not just advice fragments?

Score guide:
- **0:** No real workflow.
- **1:** Steps exist but are shallow, unordered, or generic.
- **2:** Steps form a practical sequence.
- **3:** Steps are stage-aware, decision-useful, and reduce agent drift.

What good looks like:
- a clear `## Workflow`
- order of operations is explicit
- the workflow changes how the agent approaches the task

### 4. Domain depth
**Question:** Does the skill reflect real operator judgment in its category?

Score guide:
- **0:** Mostly generic business or writing advice.
- **1:** Some domain language exists but feels thin.
- **2:** Domain-specific concepts and trade-offs are present.
- **3:** The skill feels like a sharp specialist, not a generic assistant.

What good looks like:
- category-specific lenses and trade-offs
- real failure modes
- stage-sensitive or context-sensitive guidance

### 5. Verification strength
**Question:** Does the skill define how to tell whether a good answer was produced?

Score guide:
- **0:** No verification section.
- **1:** Verification exists but is generic.
- **2:** Verification is relevant and checkable.
- **3:** Verification strongly guards against the most likely failure modes.

What good looks like:
- `## Verification Checklist`
- checks tied to the category, not generic “be thorough” language
- enough specificity to catch weak answers

### 6. Example usefulness
**Question:** Do the examples make the skill easier to use and harder to misuse?

Score guide:
- **0:** No examples.
- **1:** Examples exist but are generic or repetitive.
- **2:** Examples clarify expected output well.
- **3:** Examples teach routing, answer shape, and failure avoidance.

What good looks like:
- realistic prompts or scenarios
- examples reveal how the skill thinks
- examples reduce ambiguity for future contributors

## Fast fail conditions

A skill should usually be revised before merge if any of these are true:
- description does not clearly start with `Use when ...`
- no `## When to Use`
- no boundary / counter-trigger guidance
- no `## Common Pitfalls`
- no `## Verification Checklist`
- no `## Examples`
- mostly generic advice that could fit many categories equally well
- obvious overlap with another repo skill and no boundary clarification

## Merge guidance by score

| Total | Meaning | Suggested action |
|---|---|---|
| 0-9 | weak | rewrite before merge |
| 10-13 | underpowered | patch substantially |
| 14-17 | usable but uneven | improve before calling it a flagship skill |
| 18-21 | strong | mergeable |
| 22-24 | excellent | reference-quality skill |

## Reviewer prompts

When reviewing a skill, ask:
1. Would a new contributor know when to load this skill?
2. Would the agent confuse this with a neighboring skill?
3. Does the workflow change behavior, or is it mostly stylistic prose?
4. Does the skill contain real category judgment?
5. Would the verification checklist catch a shallow answer?
6. Do the examples make the intended output more concrete?

## Recommended review comment format

Use this simple structure in PR review or issue comments:

```text
Skill reviewed: <skill-name>

Scores:
- Trigger clarity: X/3
- Boundary clarity: X/3
- Workflow quality: X/3
- Domain depth: X/3
- Verification strength: X/3
- Example usefulness: X/3
- Total: X/24

Top strengths:
- ...
- ...

Top weaknesses:
- ...
- ...

Required before merge:
- ...

Nice-to-have later:
- ...
```

## Notes for contributors

Prefer:
- fewer strong skills over many thin ones
- portable task-class guidance over company-specific instructions
- examples that teach judgment, not just formatting
- checklists that catch failure, not generic confidence theater

Avoid:
- writing one-off incident notes as if they were reusable skills
- duplicating another skill with slightly different wording
- inflating a skill with long generic prose
- hiding missing rigor behind polished writing
