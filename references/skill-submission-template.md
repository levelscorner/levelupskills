---
name: skill-submission-template
description: Use when proposing, drafting, or reviewing a new reusable skill for the levelupskills library, especially when contributors need a consistent structure before writing the final SKILL.md.
version: 1.0.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [skills, template, contribution, library, authoring]
    related_skills: [startup-company-design, product-discovery-and-prioritization]
---

# Skill Submission Template

## Overview
Use this template when drafting a **new** skill for `levelupskills` before the final version is polished.

This is not the final style target.
It is a contributor aid that helps prevent thin, vague, or misrouted submissions.

## When to Use
Use this template when:
- proposing a new skill in a PR
- testing whether a potential skill is broad enough to belong in the repo
- drafting a first pass before turning it into a stronger final `SKILL.md`

Do **not** use this template as a substitute for the repo's quality bar.
A submitted skill should still be reviewed against:
- `references/skill-quality-rubric.md`
- `references/2026-2027-skill-authoring-standards.md`

## Template

```yaml
---
name: your-skill-name
description: Use when the user asks about <clear recurring task class>. Also use when <adjacent trigger>. Do not use this as the main skill for <adjacent class>. 
version: 1.0.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [tag1, tag2, tag3]
    related_skills: [related-skill-1, related-skill-2]
---

# Your Skill Title

## Overview
What class of work this skill handles, and why it exists.

## When to Use
Use this skill when the main problem is **...**.

Typical triggers:
- ...
- ...
- ...

Do **not** use this as the main skill when:
- ...
- ...
- ...

## Core Principle
State the category truth this skill should keep the agent anchored on.

## Always cover
- ...
- ...
- ...

## Workflow
1. ...
2. ...
3. ...
4. ...
5. ...

## Output format
Return:
1. ...
2. ...
3. ...
4. ...
5. ...

## Common pitfalls
1. ...
2. ...
3. ...

## Verification checklist
- [ ] ...
- [ ] ...
- [ ] ...

## Examples
### Example: ...
Return:
1. ...
2. ...
3. ...
4. ...
5. ...
```

## Submission checklist
- [ ] the skill is reusable across many users or companies
- [ ] the description clearly starts with `Use when ...`
- [ ] adjacent-skill boundaries are explicit
- [ ] workflow is real, not generic prose
- [ ] examples show how the skill should think
- [ ] verification can catch shallow output

## Notes
If the draft cannot score reasonably against the quality rubric, it probably should not become a standalone skill yet.
