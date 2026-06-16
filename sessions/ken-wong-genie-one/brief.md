# Ken Wong / Genie One — DAIS Keynote 2 Intelligence Pack

## Executive readout

Ken Wong’s keynote makes Genie One the practical answer to Ali Ghodsi’s “context problem”. The thesis is simple: generic agents are weak with enterprise data because they hallucinate, use stale documents, or burn tokens crawling systems without enough business context. Genie One is Databricks’ attempt to turn enterprise context into a governed, always-on coworker.

The important phrase for Gavi: **the future agent stack needs an enterprise ontology, not just a chat interface.**

## 60-second summary

- Genie One is positioned as a **data-smart AI coworker** that connects to data and apps so employees can get insights and automate action.
- Ken’s contrast: generic AI assistants either hallucinated, used stale documents, or spent 30 minutes/token-heavy loops producing partial results.
- The core differentiator is **Genie Ontology**: an automatic learned context layer built from dashboards, queries, pipelines, docs, permissions and expertise.
- Genie can compute live results, cite tables/docs/tickets/glossary snippets, enforce Unity Catalog permissions, and create reusable domain agents.
- It is now integrated with Teams, Slack, iOS and Android, and available through a Genie MCP app for other agents/tools.

## What was said vs what it means

### What was said
- Generic agents struggled on a real Databricks account-profile task: one invented a number, another used stale docs, and coding agents took too long.
- Databricks Research benchmarked coding agents on real employee data questions; the best solved only a little over half and took minutes.
- Semantic layers and skills help, but cannot cover the full messy breadth of how businesses define things.
- Genie Ontology extracts expressions, relationships, expertise and permissioned snippets from enterprise systems, then ranks authority with OntoRank.
- Genie One can draft docs, comment on Jira tickets through MCP, run SQL across Databricks and BigQuery, add forecasts, schedule recurring work, create domain agents and push proactive mobile notifications.

### What it means
- Databricks is arguing that generic agents are not enterprise-ready until they understand the business context and permission model.
- The product battle is moving from “who has the best chatbot?” to “who owns the trusted context layer?”
- The killer enterprise feature is not just answering; it is **computing, citing, acting and staying governed**.

## xAI/Grok market signal

### Query used
`Databricks Genie One Ken Wong DAIS Summit 2026 ontology Unity AI Gateway Teams Slack mobile Genie MCP app`

### Sources worth opening
- https://x.com/Data_AI_Summit/status/2066917869225640100 — official Data + AI Summit signal on Ken Wong / Genie One session.
- https://x.com/i/status/2066911087971201501 — official/video signal positioning Genie One as a data-smart AI coworker.
- https://x.com/LeoneDataAI/status/2066923112978141322 — analyst/practitioner signal on GA and adoption model.
- https://x.com/Data_AI_Summit/status/2066919347378167844 — signal around Genie Ontology and enterprise context.
- https://x.com/mikeni/status/2066924564987465842 — analyst signal on why owning fresh enterprise ontology matters.
- https://x.com/leta14_l3ta14/status/2066926839017411046 — public signal on Unity governance extending to models, agents, files, skills and MCP.
- https://x.com/iedaily_/status/2066924881489646022 — signal on Unity AI Gateway cost/routing/runtime controls.
- https://x.com/DatabricksJP/status/2066921817353355766 — signal on mobile availability.
- https://x.com/RealStrech/status/2066922053467590982 — signal around MCP apps / agent interoperability.

### Market read
Public DAIS signal is converging on the same story as the transcript: Genie One is not being pitched as “another assistant”. It is being pitched as an enterprise context, governance and action layer for agents.

### Devil’s advocate from the market signal
The obvious sceptical challenge: if Genie One becomes the way employees ask questions, create agents, automate tasks and access operational data, Databricks is moving much closer to the enterprise workflow layer. Buyers will ask whether this is openness or a new control-plane dependency.

## Technical AI consultant brief

### Architecture implications
- Treat ontology as agent infrastructure: definitions, relationships, authority, permissions and expertise must be discoverable at runtime.
- Design agents that compute from source systems, not agents that merely summarise stale documents.
- Use citations as audit evidence: tables, dashboards, tickets, docs, glossary terms and ontology snippets.
- Build governed action flows through Unity Catalog and Unity AI Gateway, especially for MCP tools.
- Expect clients to ask how this compares with Copilot, ChatGPT Enterprise, custom LangGraph/CrewAI agents and existing semantic layers.

### Reusable AA assets to build
- “Enterprise Agent Context Readiness” assessment.
- Genie Ontology explainer diagram for executives.
- Pattern: governed domain agent for finance/HR/sales operations.
- Pattern: proactive mobile insight → human review → automated workflow.
- Evaluation harness: generic agent vs ontology-grounded agent for enterprise data questions.

### Technical questions to debate
1. How much of a client’s context can be learned automatically vs curated?
2. What is the failure mode when OntoRank ranks the wrong snippet as authoritative?
3. How do we test permission enforcement across federated apps and MCP tools?
4. How do clients avoid silent automation drift as domain agents evolve?

## Sales and growth talk track

### Plain-English version
Most AI agents are clever but not business-aware. Genie One is Databricks saying: give the AI your trusted business context, permissions and live data, then it can answer and act more reliably.

### Client trigger
Listen for:
- “Our AI assistant gives plausible but wrong answers.”
- “Teams don’t trust the data behind AI answers.”
- “The AI summarises documents, but cannot compute the latest numbers.”
- “We have too many definitions for the same metric.”
- “Security worries about agents connecting to Slack, email, Jira and data warehouses.”

### Talk track
The problem is not whether an AI can write text. The problem is whether it knows your business definitions, can access live data safely, cites where answers came from, and acts inside governance. That is the gap Genie One is trying to close.

### Best next question
“Which business questions do your teams still answer manually because nobody trusts the automated answer?”

## FSI customer angle

For financial services, Genie One is about **trusted decision support**, not productivity theatre.

Useful hooks:
- citations and lineage for answers
- permission enforcement through existing governance
- controlled MCP actions and tool access
- auditable definitions for metrics and KPIs
- scheduled/proactive insights with human review
- domain agents for risk, ops, finance, customer service and compliance teams

Line Gavi can use:
> “In FSI, the question is not whether an AI coworker can produce an answer. It is whether the firm can prove why that answer was trusted, which data it used, and what action it took.”

## Retail and CPG customer angle

For retail and CPG, the Genie One story connects directly to customer/product context and the AI shelf.

Useful hooks:
- sales, supply chain, marketing and product teams asking questions in natural language
- campaign definitions and customer metrics that vary by team
- proactive alerts when engagement, demand or stock patterns change
- domain agents for merchandising, store ops, category management and marketing
- trusted product/customer context becoming the raw material for better AI recommendations

Line Gavi can use:
> “Retail and CPG firms do not just need AI agents. They need agents that understand the difference between this week’s campaign logic, product hierarchy, customer definition and channel reality.”

## Gavi learning brief

### Beginner analogy
A generic agent is like a clever temp who has never worked in your company. It can write well, but it does not know which dashboard is trusted, which Jira field means “blocked”, who owns a metric, or whether yesterday’s document is stale.

Genie One is Databricks trying to give that temp a company map, permissions badge, glossary, expert directory, calculator and workflow tools.

### Key terms
- **Ontology**: a map of business concepts, relationships and trusted definitions.
- **OntoRank**: Databricks’ authority-ranking approach for ontology snippets, roughly like PageRank for business context.
- **Semantic layer**: curated business definitions for metrics/data.
- **MCP**: Model Context Protocol; a standard way for agents to use tools/systems.
- **Unity Catalog**: Databricks governance layer for permissions, lineage and assets.
- **Unity AI Gateway**: control plane for AI/model/tool usage, cost and policy.

### Teach-back questions
1. Why did the generic assistants fail Ken’s customer-profile task?
2. Why is “summarising existing docs” weaker than “computing live results”?
3. What does Genie Ontology add beyond a normal semantic layer?
4. Where could this go wrong in a regulated organisation?

## Devil’s advocate

- **Authority risk:** if OntoRank picks the wrong “trusted” snippet, the agent may confidently compute from the wrong business logic.
- **Governance risk:** connecting email, Slack, Jira, BigQuery, Databricks and docs raises permission-boundary complexity.
- **Vendor dependency:** if Genie becomes the front door for enterprise work, Databricks becomes more than a data platform.
- **Change-management risk:** domain agents sound easy to create, but ownership, certification, expiry and monitoring will matter.
- **Evaluation gap:** “30 percentage point accuracy improvement” is useful, but clients will need their own benchmarks, not just vendor tests.

## Thought leadership angles

### LinkedIn hooks
1. The DAIS Genie One keynote made something obvious: the next AI battleground is not the chatbot. It is the business context layer.
2. A clever AI assistant that does not know your company is just a confident intern with keyboard access.
3. Enterprise AI will not scale on prompts. It needs trusted definitions, permissions, citations and live data.

### Draft LinkedIn post
The Genie One keynote at DAIS landed for me because it named a problem most teams are already feeling.

Generic AI assistants are clever.  
But they are not necessarily business-aware.

They can summarise stale docs.  
They can make up numbers.  
They can spend ages crawling systems and still come back half-right.

The real enterprise gap is context.

Which dashboard is trusted?  
How is “engagement” defined this month?  
Who owns that metric?  
What data am I allowed to see?  
Can the answer be traced back to source?  
Can the agent take action without creating a governance mess?

That is why ontology, permissions, citations and live computation matter.

The next phase of enterprise AI is not “another assistant”.
It is giving agents enough business context to be useful — and enough control to be safe.

### Short takes
- The best AI coworker is not the one that talks most fluently. It is the one that knows which data to trust.
- “Can it answer?” is table stakes. “Can it cite, compute, act and stay governed?” is the enterprise test.
- Ontology is not a data nerd side quest. It is becoming agent infrastructure.

## YouTube playback pack

### Show title options
- Why enterprise AI agents keep failing: they don’t know your business
- Genie One and the real AI bottleneck: context
- The next AI battleground is the ontology layer

### 3-act running order
1. **The demo problem:** generic agents hallucinate, use stale docs or burn tokens.
2. **The Databricks answer:** Genie Ontology + Unity governance + live computation.
3. **What clients should do:** assess context readiness before scaling agents.

### Opening monologue
“Ken Wong’s Genie One keynote was basically a warning: the AI assistant you already use might be fluent, fast and still completely wrong for enterprise work. The issue is not writing ability. It is whether the AI knows your business definitions, has permission to use the right data, can compute live results, and can show you where the answer came from.”

### Clip-worthy line
“A clever agent without enterprise context is just a confident intern with production access.”

## Claims to verify before public use

- Exact speaker title: Ken Wong’s Databricks role.
- Exact spelling/name of Elise/Elise Joris/Georis from demo segment.
- “30 percentage point accuracy improvement” and “roughly half runtime” — cite official deck/session before posting.
- “Best coding agent solved above half the time” — verify benchmark wording.
- General availability date for Genie One.
- $10 token credit per user per month.
- Teams, Slack, iOS, Android availability “today”.
- Genie MCP app availability “today”.
- Customer examples: Warner Music Group, General Motors, Foot Locker — use only if public/official.

## Follow-up tracker

### Internal AA actions
- Create a “Genie One in plain English” briefing for consultants and sales.
- Build a client workshop: “Are you context-ready for enterprise agents?”
- Draft a Databricks architecture slide: Genie Ontology + Unity Catalog + Unity AI Gateway + MCP.
- Prepare FSI angle: auditable AI coworkers and governed action.
- Prepare retail/CPG angle: product/customer context and proactive decision agents.

### Demo ideas
- Stale-doc assistant vs live-compute assistant.
- Metric-definition conflict resolved through ontology/citations.
- Domain agent for retail category manager or FSI operations analyst.
- Proactive alert → mobile follow-up → scheduled recurring update.

