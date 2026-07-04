---
name: agentic-stack-research
description: Use when the user asks how to evaluate languages, frameworks, runtimes, SDKs, orchestration systems, memory systems, tool-calling stacks, or deployment choices specifically for agentic AI products and systems. Also use for agent framework ecosystem analysis, AI application stack research, and language/runtime selection research for agentic systems, especially when comparing Python, Go, Java, C#, TypeScript, or emerging AI-native runtimes.
version: 1.0.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [research, agents, ai, agentic, frameworks, runtimes, strategy, enterprise]
    related_skills: [deep-research, strategic-research-briefs, technology-adoption-research]
---

# Agentic Stack Research

## Overview

Use this skill to evaluate technology choices for agentic systems: languages, frameworks, runtimes, provider SDKs, memory layers, tool-calling stacks, orchestration approaches, and enterprise deployment patterns. The aim is not just to say which option is "best." The aim is to determine which stack is best for a specific agentic product, buyer environment, and operating model.

This skill is especially useful when the user asks questions like:
- "Are people moving from Python/Go to Java/C# for agentic development?"
- "Will buyers reject our current stack?"
- "Which language should we use for agents versus infra?"
- "How should we compare agent frameworks and runtimes?"
- "Is a new AI-native language actually relevant to agent apps?"

## When to Use

Use this skill when the decision is specifically about agentic AI systems, including:
- agent frameworks and orchestration systems
- multi-agent versus single-agent architecture choices
- provider SDK support across languages
- tool-calling ecosystems
- memory, retrieval, evaluation, and observability layers for agents
- language/runtime selection for AI applications and agent backends
- enterprise fit of an AI/agent product stack
- risk that a current AI stack looks weak to buyers

Do not use this skill for broad non-AI tech trend questions; use `technology-adoption-research` for those.

## Core Principles

1. **Agentic systems are multi-layer stacks.** Do not reduce the decision to a single language.
2. **Python often leads ecosystem velocity.** That does not automatically make it the best production choice for every layer.
3. **Go, Java, and C# can be highly credible in agentic systems.** Their role depends on whether the problem is experimentation, orchestration, enterprise integration, or operational reliability.
4. **Provider SDK support is necessary but not sufficient.** Official SDKs prove support, not framework leadership.
5. **Buyer perception depends on enterprise readiness, not only language choice.** Security, observability, deployment, integration, and governance often dominate buyer judgment.
6. **Always analyze what happens if the user keeps the current stack.** The user values decision pressure, not vague neutrality.

## Stack Decomposition

Always split the agentic stack into layers before judging it:

### 1. Model and provider layer
- which providers matter?
- official SDK support by language
- model access parity across ecosystems
- streaming / tool-calling / multimodal support

### 2. Agent framework layer
- orchestration libraries
- workflow/state handling
- memory abstractions
- human-in-the-loop support
- tracing, eval, guardrails

### 3. Application layer
- business logic
- APIs
- webhooks
- auth
- product integration

### 4. Runtime and infra layer
- workers
- concurrency model
- deployment
- queues
- scaling
- latency/cost controls

### 5. Enterprise readiness layer
- observability
- compliance hooks
- policy control
- testing/eval maturity
- integration with existing enterprise stack

Many false conclusions happen because people compare one language across all five layers as if the answer must be uniform.

## Research Workflow

### 1. Frame the real user concern
Usually the actual concern is one of these:
- ecosystem leadership
- buyer rejection risk
- hiring/integration risk
- performance/runtime concerns
- whether to migrate or stay put

Name the real concern first.

### 2. Identify the relevant comparison class
Choose the right comparison set:
- Python vs Go
- Python vs Java/C#
- framework A vs framework B
- agent framework vs raw SDK approach
- existing stack vs emerging runtime/language

Do not broaden the field unnecessarily.

### 3. Collect evidence from the right source types
Prefer:
- official provider SDK repos and docs
- official framework docs
- GitHub repo maturity and activity
- vendor statements about supported languages
- enterprise-oriented docs emphasizing observability, security, deployment
- industry surveys for general language prevalence
- case studies / engineering posts when available

### 4. Evaluate each option along these dimensions
For every candidate, examine:
- ecosystem depth for agent development
- official provider coverage
- framework maturity
- iteration speed
- production operability
- enterprise fit
- interoperability with existing systems
- performance/runtime suitability
- migration cost
- what happens if the user stays with the current stack

### 5. Separate these judgments explicitly
Label each candidate by role:
- **Best for experimentation**
- **Best for enterprise integration**
- **Best for infra/runtime layer**
- **Best for compliance-heavy deployments**
- **Promising but early**
- **Useful for lower-level acceleration, not app-layer replacement**

### 6. Translate into product and buyer language
Always state:
- whether the current stack is defensible
- whether buyers would likely reject it
- what objections buyers may raise
- how to answer those objections
- what technical gaps matter more than language choice

## Special Guidance for Python + Go Stacks

When the user's stack is Python + Go, do not lazily frame it as inferior to Java/C#.

Instead evaluate it as:
- **Python** for AI ecosystem velocity, agent logic, model integrations, experimentation
- **Go** for APIs, workers, gateways, concurrency-heavy services, infra, and operational robustness

Ask whether any perceived weakness is actually due to:
- missing enterprise controls
- missing observability
- weak deployment story
- weak connectors/integration
- lack of governance narrative

Often the real issue is packaging, not language.

## Special Guidance for New AI-Native Languages

When the user asks about a new AI-native language or runtime:
- determine whether it is relevant to the app layer, infra layer, or compute/kernel layer
- check whether it is actually open source or only partially open
- check whether it has Python interop or migration pathways
- distinguish performance-language promise from agent-framework relevance
- avoid assuming that a new AI-native language replaces Python/Go for full product stacks

Use labels like:
- **important to watch**
- **promising for performance-critical subsystems**
- **not yet a default for agentic app development**

## Output Format

Start with:
- **Verdict**
- **What matters for the user's stack**
- **Whether buyers are likely to say no**

Then structure the answer as:
1. **Current ecosystem state**
2. **Why these shifts are happening**
3. **Layer-by-layer interpretation**
4. **Buyer / enterprise interpretation**
5. **Negative analysis: what if the user does not migrate?**
6. **Final recommendation**

Use tables when useful, such as:

| Stack/Language | Best use in agentic systems | Main strength | Main weakness | Buyer interpretation |
|---|---|---|---|---|

## Required Questions to Answer Internally

Before finalizing, confirm:
- Which layer is the user actually worried about?
- Is the market moving languages, frameworks, or just enterprise packaging?
- Does official SDK support exist across the compared languages?
- Is the current stack defendable with a good enterprise story?
- What would actually make a buyer reject the stack?
- What would force a migration recommendation later?

## Common Pitfalls

1. **Treating provider SDK support as proof of ecosystem leadership.** It proves legitimacy, not dominance.
2. **Flattening all stack layers into one verdict.** Agentic systems are layered.
3. **Confusing enterprise preference with technical necessity.** Buyers often care more about integration and controls.
4. **Overreacting to emerging AI-native languages.** Many are more relevant to performance or inference infrastructure than app-layer agent development.
5. **Ignoring the user's current strategic position.** The recommendation must answer whether their current stack is still commercially defendable.
6. **Missing the negative case.** Always say what happens if the user keeps the current architecture.

## Verification Checklist

- [ ] I decomposed the stack into layers before judging it.
- [ ] I checked official SDK/framework support rather than relying on vibes.
- [ ] I distinguished ecosystem velocity from enterprise acceptance.
- [ ] I evaluated buyer rejection risk directly.
- [ ] I included what happens if the user does not migrate.
- [ ] I gave a decisive recommendation tied to the user's real stack.
