# Skill Example Prompts and Eval Cases

This reference gives contributor-grade example prompts and lightweight evaluation cases for **all 33 skills** in `levelupskills`.

Use it for:
- smoke-testing whether a skill routes to the right type of answer
- reviewing whether a rewritten skill still behaves correctly
- creating demos, examples, or future automated eval harnesses

## How to use this file

For each skill:
1. Try one or both example prompts.
2. Score the answer against the listed eval cases.
3. Treat a skill as weak if it misses adjacent-skill boundaries, omits its core workflow, or produces generic advice.

## Catalog

### `ai-product-evaluation-and-model-ops`
**Category:** `ai`

**Example prompts**
1. Evaluate an AI support copilot for cost, latency, failure modes, fallback design, and eval strategy before production rollout.
2. Recommend a model-ops plan for an AI summarization feature that works in demos but shows inconsistent real-user quality.

**Eval cases**
- **Core case:** The answer should define task quality, discuss cost/latency/risk trade-offs, propose offline + online evals, and specify fallback or escalation behavior.
- **Edge case:** The answer should avoid benchmark theater, avoid treating prompt tweaks as the whole system, and separate immediate reliability work from later sophistication.

### `analytics-and-metrics-system`
**Category:** `analytics`

**Example prompts**
1. Design an analytics and metrics system for an early SaaS product that needs activation, retention, and revenue visibility.
2. Help me fix a startup dashboard that has too many vanity metrics and not enough decision-useful signals.

**Eval cases**
- **Core case:** The answer should define stage-relevant metrics, event/ownership logic, and decision use rather than listing random dashboard ideas.
- **Edge case:** The answer should distinguish leading vs lagging indicators and avoid recommending heavy BI complexity too early.

### `brand-positioning-and-messaging`
**Category:** `brand`

**Example prompts**
1. Help position a workflow product so buyers immediately understand who it is for, why it matters, and why it is different.
2. Rewrite our messaging stack so it is sharper for homepage, sales deck, and founder pitch use.

**Eval cases**
- **Core case:** The answer should define audience, problem, differentiated claim, and message hierarchy rather than generic slogans.
- **Edge case:** The answer should avoid vague brand poetry and should preserve consistency across channels.

### `concise-structured-communication`
**Category:** `communication`

**Example prompts**
1. Answer a complex founder question in a concise, structured format that is easy to scan on mobile.
2. Turn a messy explanation into a short response with clear headings, bullets, and no wasted prose.

**Eval cases**
- **Core case:** The answer should reduce verbosity, improve scannability, and preserve the real substance.
- **Edge case:** The answer should not become cryptic, omit key constraints, or bury the decision in prose.

### `response-articulation-pattern`
**Category:** `communication`

**Example prompts**
1. Choose the best response shape for a mixed strategy-plus-execution question so the answer lands clearly.
2. Restructure this answer so it uses the right articulation pattern for comparison, diagnosis, and next steps.

**Eval cases**
- **Core case:** The answer should choose a fitting structure, order points well, and make the reasoning easy to follow.
- **Edge case:** The answer should not default to one rigid template when the task calls for a different pattern.

### `verdict-first-writing`
**Category:** `communication`

**Example prompts**
1. Give me a verdict-first response on whether we should expand pricing tiers this quarter.
2. Rewrite this long analysis so the final judgment appears immediately and the support comes after.

**Eval cases**
- **Core case:** The answer should lead with a clear judgment and then support it with reasons and trade-offs.
- **Edge case:** The answer should not hedge endlessly or hide the recommendation at the end.

### `community-led-growth`
**Category:** `community`

**Example prompts**
1. Design a community-led growth motion for a product whose users want peer learning and identity, not just transactions.
2. Help decide whether community should be a growth engine or just a support surface for this product.

**Eval cases**
- **Core case:** The answer should distinguish community value from audience accumulation and describe participation loops or trust mechanics.
- **Edge case:** The answer should avoid recommending a community when the product has no real interaction or identity wedge.

### `customer-success-for-b2b`
**Category:** `customer-success`

**Example prompts**
1. Design a customer-success motion for B2B onboarding, adoption, renewal risk, and expansion readiness.
2. Diagnose why accounts are staying polite but not reaching time-to-value after purchase.

**Eval cases**
- **Core case:** The answer should define post-sale lifecycle logic, health signals, time-to-value, and renewal-risk handling.
- **Edge case:** The answer should not collapse success into support queue management or premature upsell pressure.

### `devops-and-reliability-planning`
**Category:** `engineering`

**Example prompts**
1. Review our product for deployment safety, observability, rollback readiness, and backup confidence.
2. Recommend a reliability roadmap for a startup that has production traffic but weak incident discipline.

**Eval cases**
- **Core case:** The answer should cover deploy, observe, recover, and prioritize practical controls over platform fantasy.
- **Edge case:** The answer should mention restore-tested backups, rollback logic, and alert quality rather than only uptime aspirations.

### `technical-architecture-and-platform-decisions`
**Category:** `engineering`

**Example prompts**
1. Help choose a technical architecture for a product expected to grow from MVP to repeatable scale.
2. Evaluate whether our current platform decisions are creating avoidable complexity or future bottlenecks.

**Eval cases**
- **Core case:** The answer should discuss system shape, interfaces, constraints, stage fit, and trade-offs.
- **Edge case:** The answer should avoid over-architecting and should separate real bottlenecks from speculative ones.

### `startup-finance-and-unit-economics`
**Category:** `finance`

**Example prompts**
1. Review our startup finances for burn, runway, margin, scenario planning, and unit-economics health.
2. Help me understand whether growth is actually creating value or just increasing expense.

**Eval cases**
- **Core case:** The answer should separate cash, revenue, margin, and cost-driver logic and provide operator actions.
- **Edge case:** The answer should avoid top-line obsession and include scenario thinking where uncertainty matters.

### `b2c-growth-and-content-loops`
**Category:** `growth`

**Example prompts**
1. Design a B2C growth loop that ties content, activation, sharing, and retention together.
2. Diagnose why our consumer product gets bursts of attention but no compounding growth behavior.

**Eval cases**
- **Core case:** The answer should map loop mechanics across acquisition, activation, retention, and sharing.
- **Edge case:** The answer should not mistake views or impressions for durable product growth.

### `gtm-and-growth-experiments`
**Category:** `growth`

**Example prompts**
1. Create a small GTM experiment stack to test audience, message, and channel for an early-stage product.
2. Help me stop random growth activity and replace it with hypothesis-driven GTM learning.

**Eval cases**
- **Core case:** The answer should identify the biggest GTM uncertainty and propose learning-oriented experiments with success signals.
- **Edge case:** The answer should avoid channel thrash, weak sample-size overconfidence, and scaling before repeatability.

### `india-tech-company-legal-compliance`
**Category:** `legal`

**Example prompts**
1. What legal and compliance groundwork should an Indian SaaS startup prioritize now versus later?
2. Help stage our India-specific company, contract, privacy, and hiring legal hygiene without pretending this is formal counsel.

**Eval cases**
- **Core case:** The answer should stay India-specific, separate guidance from legal advice, and prioritize immediate vs later needs.
- **Edge case:** The answer should not overclaim legal certainty or ignore escalation to qualified counsel when needed.

### `founder-communication-and-updates`
**Category:** `management`

**Example prompts**
1. Draft a founder update that is clear on progress, risks, asks, and decisions without sounding inflated.
2. Help me create a repeatable investor/stakeholder update format that improves trust and speed.

**Eval cases**
- **Core case:** The answer should balance clarity, candor, and actionability, with explicit risks and asks.
- **Edge case:** The answer should avoid spin, vagueness, or updates that report activity without meaning.

### `founder-operating-system`
**Category:** `management`

**Example prompts**
1. Design a founder operating system for weekly priorities, metrics, reviews, and decision hygiene.
2. Help fix a startup where the founder is constantly context-switching and priorities reset every week.

**Eval cases**
- **Core case:** The answer should define an operating cadence, a small metric set, and reprioritization or escalation triggers.
- **Edge case:** The answer should stay stage-appropriate and avoid turning the company into process theater.

### `startup-company-design`
**Category:** `management`

**Example prompts**
1. Map what functions this startup actually needs even though the team is tiny and titles are fuzzy.
2. Help me see which company functions are under-covered before I hire or scale further.

**Eval cases**
- **Core case:** The answer should map company functions, expose hidden weak spots, and distinguish now-vs-later function depth.
- **Edge case:** The answer should not confuse an org chart with real function coverage.

### `startup-risk-register-and-decision-making`
**Category:** `management`

**Example prompts**
1. Create a lightweight risk register and decision-making system for a startup making high-uncertainty bets.
2. Help us stop forgetting why big decisions were made and when they should be revisited.

**Eval cases**
- **Core case:** The answer should separate reversible vs irreversible decisions, define triggers, and make risk concrete.
- **Edge case:** The answer should avoid vague fear language and overbuilt risk bureaucracy.

### `vendor-selection-and-procurement`
**Category:** `operations`

**Example prompts**
1. Compare vendors for a critical software capability, including cost, lock-in, reliability, and exit criteria.
2. Help me decide between build, buy, and hybrid for a tool the company may depend on for years.

**Eval cases**
- **Core case:** The answer should evaluate total cost, operator burden, risk, and migration/lock-in dynamics.
- **Edge case:** The answer should not pick a winner based only on demo quality or sticker price.

### `partnerships-and-business-development`
**Category:** `partnerships`

**Example prompts**
1. Assess whether a partnership opportunity is strategically meaningful or just flattering noise.
2. Design a business-development approach for channel, distribution, or ecosystem partnerships.

**Eval cases**
- **Core case:** The answer should define partnership logic, mutual value, operating burden, and success criteria.
- **Edge case:** The answer should avoid partnership theater and should question opportunities that lack real leverage.

### `payment-gateway-selection-for-software`
**Category:** `payments`

**Example prompts**
1. Help choose payment infrastructure for subscriptions, invoicing, and international collection in a software business.
2. Compare merchant-of-record versus direct gateway models for a SaaS company selling across regions.

**Eval cases**
- **Core case:** The answer should separate pricing from collection design and evaluate operational, compliance, and margin trade-offs.
- **Edge case:** The answer should not fixate on APIs while ignoring merchant burden, dunning, or tax/compliance load.

### `hiring-and-people-ops-for-startups`
**Category:** `people`

**Example prompts**
1. Advise on who to hire next, whether to use a contractor, and what people-ops basics need to exist.
2. Help us stop hiring from anxiety and instead hire around real bottlenecks.

**Eval cases**
- **Core case:** The answer should identify the real bottleneck, define the work before the title, and compare contractor vs employee paths.
- **Edge case:** The answer should avoid aspirational org-chart hiring and should include onboarding basics.

### `org-design-after-first-hires`
**Category:** `people`

**Example prompts**
1. Redesign our startup org now that the first hires are creating coordination and ownership confusion.
2. Help decide how responsibilities and reporting should change after a tiny founding team becomes a real org.

**Eval cases**
- **Core case:** The answer should address ownership, coordination, managerial load, and structural clarity after first hires.
- **Edge case:** The answer should not recommend heavyweight layers or vague role reshuffles without clear ownership outcomes.

### `pricing-and-packaging-strategy`
**Category:** `pricing`

**Example prompts**
1. Design pricing and packaging for a product that has early users but unclear willingness-to-pay signals.
2. Help decide whether our monetization issue is price level, packaging, segmentation, or value communication.

**Eval cases**
- **Core case:** The answer should distinguish willingness to pay, segmentation, plan structure, and monetization trade-offs.
- **Edge case:** The answer should not default to discounting or random tier proliferation without logic.

### `customer-research-and-user-interviews`
**Category:** `product`

**Example prompts**
1. Create a user-interview plan to validate a product pain point without leading participants.
2. Help synthesize qualitative customer conversations into product learning instead of anecdote piles.

**Eval cases**
- **Core case:** The answer should define the decision being informed, participant logic, question design, and synthesis method.
- **Edge case:** The answer should avoid feature-request harvesting as a substitute for real research.

### `product-discovery-and-prioritization`
**Category:** `product`

**Example prompts**
1. Help decide what to build first and what to defer for an MVP under tight resource constraints.
2. Clean up our roadmap so it reflects product bottlenecks and learning value instead of noise.

**Eval cases**
- **Core case:** The answer should identify the current bottleneck, recommend sequence not just ranking, and state what to defer.
- **Edge case:** The answer should avoid treating every request as equal demand or expanding scope to dodge trade-offs.

### `agentic-stack-research`
**Category:** `research`

**Example prompts**
1. Compare Python+Go versus Java or AI-native runtimes for a production agentic system and give a ranked verdict.
2. Evaluate whether an agent framework is production-credible or mostly demo bait.

**Eval cases**
- **Core case:** The answer should decompose the stack into layers, assess production credibility, and include omission cost.
- **Edge case:** The answer should not confuse ecosystem noise with operational maturity and must end with a clear ranking or call.

### `technology-adoption-research`
**Category:** `research`

**Example prompts**
1. Assess whether a database technology is truly gaining enterprise adoption or just benefiting from hype cycles.
2. Tell me whether ignoring a rising framework trend is strategically safe over the next two years.

**Eval cases**
- **Core case:** The answer should separate attention from adoption, weigh enterprise credibility, and include downside-of-ignoring analysis.
- **Edge case:** The answer should not rely on stars or social buzz as primary proof and must end with a direct verdict.

### `b2b-sales-discovery-and-pipeline`
**Category:** `sales`

**Example prompts**
1. Improve our B2B discovery calls, qualification logic, and pipeline stage discipline.
2. Diagnose why our pipeline looks full but deals keep stalling after meetings.

**Eval cases**
- **Core case:** The answer should cover qualification, discovery structure, next-step discipline, and stage-exit logic.
- **Edge case:** The answer should not confuse interest with real pipeline quality or recommend empty activity metrics.

### `founder-sales-for-b2b`
**Category:** `sales`

**Example prompts**
1. Help a founder run early B2B sales personally while turning calls into both revenue and market learning.
2. Improve founder-led discovery, demo, objection handling, and follow-up before a formal sales team exists.

**Eval cases**
- **Core case:** The answer should be founder-specific, connect sales to learning, and define transition triggers for a more repeatable motion.
- **Edge case:** The answer should avoid generic enterprise-sales theater that ignores founder-stage constraints.

### `security-privacy-and-risk-review`
**Category:** `security`

**Example prompts**
1. Review a new product feature for security, privacy, abuse, and sensitive-data risk before launch.
2. Help prioritize the top risk-reduction controls for a startup that cannot do full compliance theater yet.

**Eval cases**
- **Core case:** The answer should identify assets, trust boundaries, concentrated risks, and immediate mitigations.
- **Edge case:** The answer should not devolve into vague fear, legal overclaiming, or checklist-only compliance language.

### `marketplace-and-network-effects-strategy`
**Category:** `strategy`

**Example prompts**
1. Evaluate whether our marketplace idea has real network effects or just superficial two-sided activity.
2. Design a strategy for seeding and defending a network-effects business without assuming the flywheel will appear automatically.

**Eval cases**
- **Core case:** The answer should assess liquidity, side dependence, sequencing, defensibility, and failure modes of network effects.
- **Edge case:** The answer should avoid magical flywheel assumptions or confusing scale with genuine network advantage.

### `customer-support-and-feedback-ops`
**Category:** `support`

**Example prompts**
1. Design a support workflow for issue triage, customer communication, and product-feedback capture.
2. Help me turn a messy support inbox into an operational system that protects trust and retention.

**Eval cases**
- **Core case:** The answer should include triage, severity, ownership, communication norms, and the loop into product learning.
- **Edge case:** The answer should not treat support as inbox cleanup only or ignore trust-sensitive escalation paths.

