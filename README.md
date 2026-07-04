# levelupskills

Custom Hermes skills for research-driven technology strategy and agentic stack analysis.

## Included skills

### 1. `technology-adoption-research`
Use when evaluating whether a language, framework, platform, database, protocol, or engineering tool is gaining or losing adoption, whether enterprises are likely to accept it, and what happens if a team does or does not adopt it.

### 2. `agentic-stack-research`
Use when evaluating languages, frameworks, SDKs, orchestration systems, memory/runtime choices, and platform trade-offs specifically for agentic AI products and systems.

## Why these exist

These skills are designed for questions like:
- Are people moving from Python/Go to Java/C# for agentic development?
- Will enterprise buyers reject a Python + Go stack?
- How should we compare AI application stacks by adoption, enterprise fit, and ecosystem maturity?
- What is the right language/runtime/framework choice for agentic systems?

## Repository structure

```text
skills/
  research/
    technology-adoption-research/
      SKILL.md
    agentic-stack-research/
      SKILL.md
references/
  research-taxonomy.md
README.md
```

## Skill inventory used while creating this repo

These are the Hermes skills used in the originating conversation:
- using-superpowers
- strategic-research-briefs
- deep-research
- verification-before-completion
- skill-creator
- github-auth
- github-repo-management
- hermes-agent
- hermes-agent-skill-authoring

## Notes

This repository currently contains original custom skills intended for general reuse. The upstream skills listed above are referenced for provenance and workflow context, but are not copied into this repo.
