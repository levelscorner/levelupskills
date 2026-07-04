# Contributing to levelupskills

Thanks for contributing to `levelupskills`.

This repo is for **portable, profession-shaped skills** that help agents reason better across recurring startup, product, and operating tasks.

It is **not** for:
- company-specific playbooks
- one-off incident notes
- personal context that only makes sense for one founder or one repo
- thin prompt snippets pretending to be reusable skills

## What a good contribution looks like

A strong contribution usually does one of these:
- strengthens an existing skill
- adds a missing reference file that improves contributor quality
- introduces a genuinely reusable new skill with clear boundaries
- improves contributor workflows, review quality, or release clarity

Before adding a new skill, ask:
1. does an existing skill already cover this class of task?
2. would a patch to an umbrella skill be better than a new sibling?
3. is this reusable across many users, products, or companies?

## Skill standards

Read these first:
- [`references/2026-2027-skill-authoring-standards.md`](./references/2026-2027-skill-authoring-standards.md)
- [`references/skill-quality-rubric.md`](./references/skill-quality-rubric.md)
- [`references/versioning-and-release-policy.md`](./references/versioning-and-release-policy.md)
- [`references/skill-example-prompts-and-eval-cases.md`](./references/skill-example-prompts-and-eval-cases.md)
- [`references/skill-submission-template.md`](./references/skill-submission-template.md)

A merge-ready skill should usually include:
- trigger-rich description starting with `Use when ...`
- `## Overview`
- `## When to Use`
- adjacent-skill boundaries / counter-triggers
- a real `## Workflow`
- `## Common Pitfalls`
- `## Verification Checklist`
- `## Examples`

## Repo structure

```text
skills/<category>/<skill-name>/SKILL.md
references/*.md
README.md
SETUP.md
```

Use `references/` for:
- eval cases
- standards
- contributor guidance
- category maps
- detailed support docs that do not belong inside one skill body

## Contribution workflow

1. pick an existing skill or identify a real gap
2. make the smallest durable improvement that solves the problem
3. verify the skill still has strong triggers, boundaries, workflow, pitfalls, verification, and examples
4. if you add a new skill, make sure it is class-level and portable
5. update docs or references if contributor behavior should change
6. verify before opening the PR

## Review expectations

Contributors and reviewers should score changed skills with:
- [`references/skill-quality-rubric.md`](./references/skill-quality-rubric.md)

Reviewers should reject changes that are:
- too generic
- too company-specific
- overlapping with an existing skill without boundary fixes
- missing real workflow logic
- missing verification or examples

## New skill checklist

Before opening a PR for a new skill:
- [ ] checked whether an existing umbrella skill can absorb it instead
- [ ] chose a class-level, portable skill name
- [ ] wrote a trigger-rich description starting with `Use when ...`
- [ ] added boundaries against adjacent skills
- [ ] included pitfalls, verification, and examples
- [ ] added related references if needed
- [ ] reviewed against the quality rubric

## Validation expectations

At minimum, verify:
- the changed markdown is structurally sound
- the changed skill still validates against repo conventions
- any new reference doc is internally complete
- README / SETUP / templates stay in sync if repo usage changed

## Pull request guidance

Use the PR template and include:
- what changed
- why it changed
- whether any skills were added, split, merged, or materially rerouted
- what verification you ran

## Contributor philosophy

Prefer:
- fewer strong skills over many thin ones
- real operator judgment over generic advice
- explicit routing clarity over broad vague prompts
- human-readable docs over ritual complexity

If a contribution makes the library sharper, more portable, and easier to route correctly, it probably fits.
