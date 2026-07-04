---
name: agentic-stack-research
description: Use when the user asks how to evaluate languages, frameworks, runtimes, SDKs, orchestration systems, memory systems, tool-calling stacks, or deployment choices specifically for agentic / AI-product systems. Also use when the user wants a research-driven recommendation about Python vs Go vs Java vs C# vs newer AI-native languages for agent building, or about whether a given agent framework is strategically credible. This skill is specifically for agentic-system stack selection, not general software trend commentary.
version: 1.1.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [research, agentic-systems, ai-engineering, stack-selection, framework-analysis]
    related_skills: [technology-adoption-research, strategic-research-briefs, deep-research]
---

# Agentic Stack Research

## Overview
Use this skill when the user wants to understand which technologies are actually credible for building agentic systems, AI products, or tool-using software — and which ones are mostly fashion, demos, or local maxima.

This is not generic tech-trend research. It is specifically for **agentic-system stack selection**.

## When to Use
Use this skill when the user's question is like:
- What language should we use for agentic systems?
- Is Python enough, or should we use Go / Java / C# too?
- Is framework X real or overhyped?
- What is the best stack for a production AI product?
- What happens if we do *not* adopt a more agent-native stack?
- Is a new AI-native language credible yet?

Typical trigger categories:
- agent frameworks
- tool-calling / orchestration stacks
- inference / routing layers
- memory / workflow systems
- evaluation / observability systems for agents
- AI-product runtime / language choices

Do **not** use this skill when:
- the question is about broad technology adoption outside agentic systems → use `technology-adoption-research`
- the user only wants implementation help for a chosen stack
- the task is product strategy with no stack-selection question

## Core Principles
1. **Production credibility beats demo fluency.** Do not confuse cool examples with durable operating value.
2. **Language choice is ecosystem choice.** Compare tools, libraries, hiring, and operational ergonomics — not syntax taste.
3. **Agent frameworks are not equal.** Many reduce prompt plumbing; fewer reduce production pain.
4. **The cost of omission matters.** Always analyze what the user loses by *not* upgrading the stack.
5. **A verdict is mandatory.** The user needs a recommendation, not a shrug.

## Stack Decomposition
Always separate the stack into layers:
- application language / runtime
- model provider / inference layer
- orchestration / agent framework
- tool execution model
- memory / state model
- eval / observability / monitoring layer
- deployment / ops model

Do not compare stacks as undifferentiated blobs.

## Always cover
- current stack fit for the target agentic workload
- ecosystem and maturity by layer
- operational and debugging burden
- hiring / talent realism
- speed of iteration vs long-term maintainability
- omission cost: what happens if the stack stays as-is

## Workflow
1. Define the agentic system class: internal automation, coding agent, AI feature, support agent, workflow orchestrator, multi-agent system, etc.
2. Break the stack into layers and identify which layer is actually under question.
3. Collect evidence across official sources, ecosystem depth, implementation stories, jobs, tooling, and operational maturity.
4. Separate demo attractiveness from production credibility.
5. Evaluate the adoption and omission risk of each serious option.
6. Recommend a stack by company stage, team composition, and product risk.
7. End with a direct ranking or final call.

## Special Guidance for Python + Go Stacks
When comparing Python + Go against Java / C# / new AI-native languages:
- treat Python as the default innovation layer unless evidence clearly says otherwise
- treat Go as credible for performance, infra, SDK, and operational systems even when ecosystem mindshare is lower
- distinguish enterprise procurement optics from actual technical fitness
- do not assume broader language popularity means better agentic fit

## Special Guidance for New AI-Native Languages
When evaluating new languages or runtimes marketed as AI-native:
- require stronger evidence than for established ecosystems
- check whether the value is runtime-level, tooling-level, or mostly branding
- assess whether the language changes real product outcomes or only developer aesthetics
- explicitly state whether it is “watch”, “pilot”, or “production-ready for this use case”

## Output format
Return the answer in this structure:
1. **System context**
2. **Layer-by-layer assessment**
3. **What looks production-credible vs hype-heavy**
4. **What happens if the current stack is kept**
5. **Recommended stack / ranking**
6. **Why this verdict wins**

## Required Questions to Answer Internally
Before finalizing, answer these internally:
- Which stack layer is the actual bottleneck?
- Am I over-crediting demo ecosystems?
- Did I assess omission cost, not only adoption benefit?
- Did I separate language choice from framework choice?
- Did I provide a real verdict and ranking?

## Common Pitfalls
1. **Comparing languages without comparing ecosystems.** Syntax is not the real decision.
2. **Treating framework abundance as framework quality.** Many wrappers do not equal operational maturity.
3. **Ignoring observability and evaluation layers.** Agent stacks fail there more often than in prompt syntax.
4. **Assuming new AI-native tech must replace Python immediately.** Watch the actual leverage.
5. **Stopping at analysis without a call.** The user needs a recommendation.

## Verification Checklist
- [ ] I broke the stack into layers.
- [ ] I separated hype from production credibility.
- [ ] I assessed omission cost explicitly.
- [ ] I accounted for team, hiring, and operability.
- [ ] I gave a final ranking or clear recommendation.

## Examples
### Example: language choice for agents
Question: Should we stay Python + Go, or move to Java / C# / AI-native runtimes?

Return:
1. Which layer each language is best suited for.
2. Ecosystem maturity and operational fit.
3. What the team loses by staying put.
4. What the team risks by switching early.
5. Final verdict by near-term and medium-term horizon.

### Example: evaluating a new agent framework
Question: Is framework Z real, or just demo bait?

Return:
1. What layer it occupies.
2. What pain it actually removes.
3. What it adds in complexity.
4. Ecosystem maturity and production signals.
5. Verdict: ignore, watch, pilot, or adopt.

## Evidence hierarchy
Prefer evidence in roughly this order:
1. official docs and architecture docs
2. real implementation writeups and engineering posts
3. ecosystem depth and integration coverage
4. ops / evaluation / observability maturity
5. hiring signals and community momentum

Community momentum matters — but only after the stack proves it can survive production reality.
