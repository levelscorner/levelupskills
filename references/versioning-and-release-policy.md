# Skill Library Versioning and Release Policy

This document defines how `levelupskills` should evolve without turning the library into an unstable moving target.

The goal is simple:
- improve skills aggressively
- preserve contributor clarity
- make releases understandable
- avoid meaningless version bumps

## What gets versioned

There are two useful version layers in this repo:

1. **Per-skill version** inside each `SKILL.md`
2. **Repository release version** for the library as a whole

Both matter, but for different reasons.

## 1. Per-skill versioning

Each skill should keep a semantic-style version in frontmatter:

```yaml
version: 1.1.0
```

### How to bump a skill version

#### Patch bump (`1.1.0` → `1.1.1`)
Use when:
- fixing wording mistakes
- improving clarity without changing the core workflow materially
- tightening examples, checklists, or phrasing
- correcting broken references or minor authoring defects

#### Minor bump (`1.1.0` → `1.2.0`)
Use when:
- adding meaningful new sections
- improving boundaries with adjacent skills
- expanding workflow depth
- adding substantial examples or verification logic
- changing how the skill should usually behave without redefining its whole purpose

#### Major bump (`1.1.0` → `2.0.0`)
Use when:
- changing the core task class the skill covers
- splitting or merging the skill in a way that changes how contributors should route work
- rewriting the skill so heavily that old expectations are no longer reliable

## 2. Repository release versioning

The library as a whole should also use semantic-style releases:

- `v1.0.0`
- `v1.1.0`
- `v1.2.0`
- `v2.0.0`

### How to bump the repository release

#### Patch release
Use when the repo change is mostly:
- documentation cleanup
- template fixes
- contributor guide improvements
- typo or formatting cleanup
- no major shift in library capability

#### Minor release
Use when the repo adds or materially improves library capability, for example:
- new reference guides
- new contributor tooling
- broad skill-quality improvements
- multiple strengthened skills across categories
- new issue / PR / submission workflows

#### Major release
Use when the library changes in a way that affects user expectations broadly, for example:
- major category reshaping
- broad renaming or relocation of skills
- large-scale routing changes
- substantial redefinition of the repo standard

## Recommended release rhythm

This repo does **not** need high-frequency release theater.

Use a practical rhythm:
- merge useful improvements continuously
- cut a release when the change set becomes meaningfully legible to users
- prefer fewer clear releases over many tiny cosmetic tags

A good default:
- patch releases for cleanup bundles
- minor releases for meaningful library upgrades
- major releases only when the library contract really changes

## Changelog policy

Every release should summarize:
- what improved
- which skills changed materially
- whether contributor behavior should change
- whether any renamed, split, or merged skills need special attention

Prefer human-readable changelog entries over exhaustive diff spam.

## Skill-change expectations

When editing an existing skill:
1. decide whether the change is patch, minor, or major
2. update the skill's `version:` field if the change is meaningful
3. include the rationale in the PR or commit message when helpful

Do **not** bump skill versions for no-op formatting churn.

## When not to bump a skill version

Usually do **not** bump for:
- whitespace-only cleanup
- line wrapping only
- purely mechanical formatting normalization
- unrelated repo-doc updates that do not change the skill

## New skill policy

When adding a new skill:
- start at `1.0.0` if it is a real merge-ready skill
- do not start at `0.x` unless the repo explicitly adopts a preview convention later

The default assumption in this repo should be:
- if a skill is committed, it is intended to be usable

## Renames, splits, and merges

When a skill is renamed, split, or merged:
- note it explicitly in the changelog
- update related references in README / SETUP / templates / docs
- update adjacent-skill references where needed
- treat it as at least a **minor** repo release
- consider a **major** skill bump or repo bump if routing expectations changed materially

## Release checklist

Before cutting a release:
- [ ] changed skills still validate structurally
- [ ] new references/templates are linked or discoverable
- [ ] README / SETUP reflect important repo-shape changes
- [ ] changelog entry summarizes the meaningful deltas
- [ ] skill versions were bumped where behavior changed materially
- [ ] no meaningless version churn was introduced

## Practical examples

### Example: doc-only polish
Changes:
- contributor guide added
- issue templates added
- no skill behavior changed

Suggested release:
- repo: patch or minor, depending on contributor impact
- skills: no version bump required

### Example: broad skill quality pass
Changes:
- many skills gain `When to Use`, pitfalls, verification, and examples
- routing quality improves substantially

Suggested release:
- repo: minor
- each materially improved skill: minor bump

### Example: category reshaping
Changes:
- one broad skill becomes three new skills
- routing expectations change across the repo

Suggested release:
- repo: major
- affected skills: major or fresh `1.0.0` if replaced cleanly

## Contributor default

If unsure:
- bump the **skill minor version** when the skill became meaningfully better
- leave the version alone when the change is purely cosmetic
- use **repo minor releases** for meaningful visible improvements to the library

The rule is not “version everything.”
The rule is “version the changes people can feel.”
