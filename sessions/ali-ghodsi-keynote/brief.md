# Ali Ghodsi — DAIS Keynote 1 Intelligence Pack

## Executive readout

Ali Ghodsi’s keynote sets up the whole DAIS 2026 story: AI is now capable enough; the bottleneck is enterprise context, control, cost and choice. Databricks is positioning itself as the governed platform where agents can access business context, operational memory, model/tool choice and policy controls without turning the enterprise into a security and cost bonfire.

The clean CAIO thesis: **the future of enterprise AI is not model-picking — it is building the operating system around agents.**

## 60-second summary

- Ali argued that by older definitions, AGI-level capability is already here; the bigger enterprise problem is that AI has not permeated organisations safely.
- The keynote framework was **choice, control, cost and context**.
- Databricks’ answer spans Lakeflow, Lakehouse/Lakebase, Unity Catalog, Unity AI Gateway, Genie Ontology, Genie One, Agent Bricks, Lakewatch and Customer Lake.
- The strongest line for Gavi: **AI does not have an intelligence problem. It has a context problem.**
- For clients, the practical question is not “which model?” but “what context can agents use, what can they touch, what will it cost, and how do we audit it?”

## What was said vs what it means

### What was said
- DAIS had over 100,000 sign-ups and more than 31,000 in-person attendees, according to the transcript.
- Databricks framed itself around open source roots: Spark, Delta Lake, Iceberg, MLflow, Unity Catalog and Postgres.
- Ali used benchmark-style AGI examples to argue that intelligence is no longer the real blocker.
- The enterprise challenge is getting the right data and context to agents while preserving security, control, cost visibility and model choice.
- Lakebase brings Postgres into the Databricks lakehouse story, including branching for agent experimentation and lower TCO.
- Unity AI Gateway becomes the control plane for agents, model usage, MCPs, costs, identities and policies.
- Genie Ontology/Genie One provide context and a business-facing agent layer.

### What it means
- Databricks wants to own the enterprise agent substrate: data, context, governance, operational state, apps and security.
- The CAIO agenda becomes: context readiness, governance architecture, cost controls, agent auditability and operating model.
- The platform story is bigger than analytics; it is moving toward the daily workflow layer.

## xAI/Grok market signal

### Query used
`Databricks DAIS 2026 Ali Ghodsi keynote Lakebase Agent Bricks Unity AI Gateway Genie One context control cost choice`

### Sources worth opening
- https://x.com/databricks/status/2066912732495139142 — official Databricks signal around Ali’s agentic enterprise framing.
- https://x.com/Infometryinc/status/2066917881682747495 — partner/market recap clustering the announcements around One, Context, Control, Cost and Choice.
- https://x.com/clawdb0t/status/2066574937754628112 — practitioner signal on Lakebase, LTAP and agent state/memory.
- https://x.com/i/status/2066911087971201501 — official/video signal around Genie One as a data-smart AI coworker.
- https://x.com/i/status/2066912732495139142 — signal on Genie Ontology / enterprise context.
- https://x.com/i/status/2066910274049994992 — signal on Unity AI Gateway and whole-company AI governance.
- https://x.com/databricks/status/2066909782619897929 — official signal on Unity AI Gateway cost/routing/control.

### Market read
The online signal matches the transcript: Databricks is not just announcing features. It is stitching together a production-agent stack: Lakebase for state/memory, Genie Ontology for context, Unity AI Gateway for governance and cost, and Agent Bricks/apps for implementation.

### Devil’s advocate from the market signal
The bold claim is openness and choice. The procurement/security challenge is whether Databricks is giving enterprises a portable open control plane — or becoming a deeper dependency across data, AI, agents, apps and operational workflows.

## Technical AI consultant brief

### Architecture implications
- Design around **context → control → cost → choice**, not just model APIs.
- Treat agent state/memory as a data-platform concern, not an app-team afterthought.
- Use branching/sandboxing patterns before letting agents mutate operational data.
- Put model usage, MCP tools, identities, rate limits, guardrails and audit through a governed gateway.
- Treat business ontology and semantic context as production infrastructure.

### Assets AA should build
- Agent governance reference architecture for Databricks clients.
- Lakebase agent memory/state design pattern.
- Unity AI Gateway cost-control and audit dashboard.
- Genie Ontology plain-English explainer.
- Zero Ops-style data pipeline repair demo flow.
- Client workshop: “Are you context-ready for enterprise agents?”

### Questions for consultants
1. What context layer is required before agents can safely act?
2. How do we evaluate an agent across data, tools, model calls and actions?
3. What is the audit evidence a bank or insurer will require?
4. Where does Databricks end and the client’s operating model begin?

## Sales and growth talk track

### Plain-English version
AI models are clever enough for many tasks now. The problem is that companies have not made their data, permissions, context and costs ready for agents to work safely.

### Client trigger
Listen for clients saying:
- “We have AI pilots but nothing scaled.”
- “Security won’t approve agents touching systems.”
- “We don’t know what our AI usage is costing.”
- “Our data is everywhere.”
- “Every team is trying a different tool/model.”

### Talk track
The next stage is not just picking a model. It is giving agents the right business context, controlling what they can access, tracking what they did, and managing cost. That is where Databricks — and AA delivery around Databricks — becomes relevant.

### Best next question
“If 100 agents went live in your business next month, what would you not trust them to access or do yet?”

## FSI customer angle

For financial services, this is about **controlled autonomy**.

Relevant hooks:
- agent identity and access control
- audit trails for model/tool/data usage
- policy-based access through Unity Catalog
- centralised spend/rate limits through Unity AI Gateway
- human approval for high-risk workflows
- evidence for model-risk, compliance and security reviews

Line Gavi can use:
> “For banks, the question is moving from ‘can we build AI?’ to ‘can we prove how it behaved under pressure?’”

## Retail and CPG customer angle

For retail and CPG, this connects to customer/product context and the AI shelf.

Relevant hooks:
- product, campaign and customer data becoming agent-readable
- Customer Lake / CDP positioning
- campaign agents and continuous personalisation
- AI shelf: products need structured, retrievable, governed context
- agents that can reason over availability, reviews, content, customer segments and marketing rules

Line Gavi can use:
> “Retailers will not just compete for shelf space. They will compete for recommendation space inside AI assistants.”

## Gavi learning brief

### Beginner analogy
Think of an AI model as a brilliant new employee. It is smart, but it does not know your company. It needs a map of the business, a permissions badge, a budget limit, a memory notebook, and a manager who can audit what it did.

That is what Databricks is pitching: the office infrastructure around the brilliant employee.

### Key terms
- **Context:** the business knowledge the AI needs to work well.
- **Ontology:** map of concepts, relationships and trusted definitions.
- **Unity Catalog:** governance layer for data and AI assets.
- **Unity AI Gateway:** controlled front door for models, agents and tools.
- **Lakebase:** serverless Postgres on the lakehouse, useful for operational apps and agent state.
- **Agent Bricks:** building blocks for production agents.
- **MCP:** Model Context Protocol, a standard way for agents to use tools.

### Teach-back questions
1. Why does Ali say intelligence is not the main problem anymore?
2. What are choice, control, cost and context?
3. Why does Lakebase branching matter for agents?
4. Why would Unity AI Gateway matter to a CISO or procurement lead?

## Devil’s advocate

- **Lock-in risk:** one platform for data, agents, gateways, context, apps, security and customer data is powerful — and potentially sticky.
- **Ontology risk:** learned context can be wrong, stale or politically contested inside large firms.
- **Cost risk:** central visibility helps, but widespread agents can still create new demand faster than governance can mature.
- **Security risk:** MCP/tool access expands the blast radius if identity and permissions are not designed properly.
- **Proof gap:** vendor keynote claims need client-specific evaluation before being used as evidence.

## Thought leadership angles

### LinkedIn hooks
1. The line that stuck with me from Ali Ghodsi’s DAIS keynote: AI does not have an intelligence problem. It has a context problem.
2. We keep asking “which model is best?” DAIS made me think that is becoming the wrong question.
3. Enterprise AI is moving from model choice to operating model.

### Draft LinkedIn post
The line that stuck with me from Ali Ghodsi’s DAIS keynote:

AI does not have an intelligence problem.  
It has a context problem.

That feels right.

Most organisations are not blocked because the model is not clever enough. They are blocked because the AI does not know enough about the business, cannot safely access the right systems, has unclear permissions, and can quietly burn through cost while trying to help.

The more interesting questions now are:

- what context does the AI need?
- what can it touch?
- who is it acting on behalf of?
- how do we audit it?
- how do we stop costs running away?
- how do we avoid locking ourselves into one vendor?

That is the real CAIO work now.

Not another AI pilot. The operating model around the agents.

## YouTube playback pack

### Show title options
- AI is smart enough. Your company context isn’t.
- The DAIS keynote explained the real AI bottleneck.
- From models to operating models: what DAIS really said.

### 3-act running order
1. What Ali said: intelligence is no longer the main blocker.
2. What it means: context, control, cost and choice are the enterprise bottlenecks.
3. What customers should do: build the governed context layer before unleashing agents.

### Opening monologue
“Here’s the thing that landed for me from Ali Ghodsi’s DAIS keynote. We keep talking about whether AI is smart enough. His argument was basically: yes, it is. The problem is not intelligence anymore. The problem is context. Does the AI know the business? Can it access the right data safely? Can we audit what it did? Can we stop costs running away? That’s where the real enterprise work is now.”

### Clip-worthy line
Agents do not just need better prompts. They need an operating model.

## Claims to verify before public use

- 100,000+ people signed up for DAIS.
- 31,309 in-person attendees.
- 174 countries represented.
- Spark has 3B downloads per year.
- Exact Postgres governance/committer statistic.
- Exact project name/spelling: Omnigen/OmniGen/Omnigent.
- Exact new engine/product names mangled by Otter.
- “10% of OpenClaw skills were malicious” — high-risk claim; verify before repeating.
- Uber CEO annual AI budget quote.
- Exact GA/preview status for Lakeflow, ZeroBus, Spark RTM, Lakebase, Unity AI Gateway, Genie One, Genie Ontology, Lakewatch and Customer Lake.

## Follow-up tracker

### Internal AA actions
- Build the “context/control/cost/choice” DAIS briefing.
- Create Databricks agent governance workshop outline.
- Turn this into a CAIO LinkedIn post while the keynote is fresh.
- Prepare FSI one-pager: governed agents and audit evidence.
- Prepare retail/CPG one-pager: Customer Lake, AI shelf and product context.

### Demos/assets
- Unity AI Gateway governance dashboard concept.
- Lakebase agent memory/state demo.
- Genie Ontology visual explainer.
- Zero Ops pipeline-fix demo flow.

