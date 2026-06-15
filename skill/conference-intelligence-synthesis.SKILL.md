---
name: conference-intelligence-synthesis
description: Use when Gavi uploads conference transcripts, Otter.ai notes, session notes, speaker slides/photos, screenshots, or voice notes and wants useful outputs for teams, learning, client insight, LinkedIn/X posts, follow-ups, and CAIO thought leadership.
version: 1.0.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [conference, otter, transcripts, thought-leadership, linkedin, x, learning, team-briefs, social-listening, excalidraw]
    related_skills: [last30days-research, dais-ai-strategy-translator, humanizer, ocr-and-documents, xurl, excalidraw]
---

# Conference Intelligence Synthesis

## Overview

Use this skill when Gavi is sitting in a conference, recording sessions with Otter.ai, taking notes, and capturing photos/screenshots of slides, booths, demos, or speaker details. The goal is not to make passive summaries. The goal is to turn raw conference exhaust into a live intelligence engine for Gavi’s role as a Chief AI Officer: what happened, what matters, what her teams should understand, what clients will ask next, what she should learn, who she should follow up with, and what public thought leadership she can publish.

Default posture: **capture → interpret → convert into useful artefacts**. A transcript alone is not the deliverable.

## When to Use

Use when the user provides or mentions:

- Otter.ai transcripts from conference sessions
- speaker notes, agenda items, or session titles
- photos of slides, booths, demos, badges, posters, or whiteboards
- voice notes after a session
- “what should I do with this data?”
- “summarise this for my team”
- “turn this into LinkedIn/X posts”
- “help me learn this topic”
- “what should I tell Advancing Analytics / DAIS / client teams?”
- “what are people saying online about this?”
- “pull top posts / comments / opinions”
- “use X / xAI / Grok signal”
- “play devil’s advocate”
- “map this visually”
- “what did the conference really say?”

Do **not** use for private/client-confidential sessions where recording/sharing is not permitted. If content includes private client, employee, or commercially sensitive data, keep outputs internal and flag privacy risk.

## Inputs to Ask For or Extract

When Gavi uploads material, extract these fields where possible:

- conference name and date
- session title
- speaker names and companies
- transcript source and quality
- Gavi’s own notes / reactions
- photos or screenshots of slides
- quoted claims and statistics
- tools, vendors, products, frameworks mentioned
- audience questions and objections
- live demos or announcements
- follow-up people / companies
- relevance to: financial services, retail, CPG, Databricks, AI strategy, model risk, red-teaming, AI shelf, CAIO operating model

If photos are provided, use vision/OCR where available. Describe visible slide content and extract exact text if legible. Do not invent slide text.

## Processing Workflow

### 1. Clean and segment the transcript

- Identify speaker names if possible.
- Remove Otter noise, repeated filler, transcription artefacts, timestamps unless useful.
- Segment into: opening claim, core sections, examples, Q&A, final takeaways.
- Mark uncertainty where transcript quality is poor.

### 2. Separate facts from interpretation

For every session, split into:

- **What was said** — direct claims, examples, statistics, announcements.
- **What it means** — implication for Gavi, teams, clients, CAIO agenda.
- **What to verify** — claims needing source-checking before external use.
- **What to do next** — actions, follow-ups, reading, demos, experiments.

### 3. Map to Gavi’s mission

Always ask: how does this compound Gavi’s public CAIO positioning?

Classify insights into:

- CAIO operating model
- Databricks / data + AI strategy
- enterprise AI governance
- red-teaming / model risk / assurance
- AI agents and automation
- financial services AI
- retail / CPG / AI shelf
- organisational change and adoption
- talent / ways of working
- vendor landscape and procurement risk

### 4. Pull the online conversation

When Gavi asks for external signal, use the `xurl` / X workflow where configured, plus web/news/blog search where useful. The goal is not vanity social listening. The goal is to understand what smart people, sceptics, practitioners, vendors, and customers are saying around the conference themes.

For each conference theme, collect:

- **Top posts:** high-engagement X/LinkedIn/public posts where accessible.
- **Top opinions:** recurring claims, disagreements, excitement, scepticism, and hot takes.
- **Top comments/replies:** what people push back on, ask for, or misunderstand.
- **Source links:** preserve URLs, handles/names where public, dates, and visible engagement metrics.
- **Signal quality:** mark whether the source is practitioner, vendor, analyst, customer, journalist, academic, or hype account.
- **Devil’s advocate:** what a sceptical CAIO, CISO, procurement lead, or model-risk owner would challenge.

X-specific workflow:

- First verify access with `xurl auth status` and a cheap read/search. Never read or expose `~/.xurl` or tokens.
- Use `xurl search "<conference/theme query>" -n <N>` for public posts.
- For a specific post, use its URL/ID with `xurl read <post>` where possible.
- To inspect replies/comments around a post, search by conversation/thread where API access permits; rank replies by visible engagement and usefulness, not just likes.
- Do not post, like, reply, repost, follow, or DM unless Gavi explicitly asks and approves the exact action.
- If X API access is missing, say so plainly and fall back to public web search rather than pretending.

If xAI/Grok access is configured for the Hermes environment, use it as an additional synthesis lens for clustering public posts/opinions, but still preserve source links and do not treat model synthesis as evidence.

### 5. Produce layered outputs

Do not dump one giant summary. Produce a stack of artefacts for different audiences.

## Default Deliverables

When Gavi uploads one session, produce:

### A. 60-second executive summary

- 3–5 bullets
- plain English
- why it matters
- strongest quote or claim
- one “so what”

### B. Team briefing

Make it useful for two internal audiences, not one blob:

#### Technical AI consultants

- **What happened:** concise factual summary
- **Why it matters technically:** architecture, data, governance, evaluation, integration, deployment, risk
- **What we should change:** delivery patterns, reusable assets, accelerators, experiments, demos, reference architectures
- **Client relevance:** how this shows up in financial services, retail, CPG, or Databricks conversations
- **Questions for the team:** sharp discussion prompts
- **Suggested owner / next action:** if obvious

#### Sales / growth team

- **Plain-English version:** no unnecessary technical detail
- **Client trigger:** what problem this helps them spot in a meeting
- **Talk track:** 3–5 lines they can say confidently
- **Objections to expect:** budget, risk, procurement, security, unclear ROI
- **Proof/examples:** public examples or anonymised patterns only
- **Next-best question:** what to ask the client next

Always separate these audiences. Highly skilled consultants need depth; sales need usable signal without drowning in implementation detail.

### C. Gavi learning brief

Help Gavi learn, not just remember:

- beginner explanation of the topic
- glossary of terms used
- “explain it like I’m new to this” analogy
- 3 Socratic why-chain questions
- what to read/watch next
- what she should be able to explain after this

### D. Thought-leadership angles

Generate:

- 3 LinkedIn hooks in Gavi’s voice
- 1 polished LinkedIn post draft
- 3 X posts / short takes
- 1 contrarian take
- 1 “question to the community”
- 1 short anecdotal reflection if she gave personal notes

Keep public posts punchy, warm, specific, and non-corporate. Avoid over-polished LinkedIn consultant mush.

### E. Follow-up/action tracker

Extract:

- people to message
- companies to research
- tools to try
- demos to build
- claims to verify
- internal actions
- client opportunities
- possible content pieces

### G. Social signal digest

When online signal is requested, add a digest that lets Gavi understand the market quickly:

```markdown
## Online signal digest: <theme/conference>

### Top posts worth reading
1. <source/link/date/engagement if visible> — <why it matters>
2. ...

### What people seem to believe
- ...

### What people are arguing about
- ...

### Best comments / replies
- <source/link> — <useful objection, question, or nuance>

### Devil’s advocate
- strongest sceptical challenge
- procurement/security/model-risk objection
- what would make this claim weak

### What Gavi can say
- internal technical team: ...
- sales team: ...
- FSI customer: ...
- retail/CPG customer: ...

### Source reliability
- strong sources: ...
- hype/noise: ...
- needs verification: ...
```

### H. Visual map

When the material is complex, produce or offer an Excalidraw map that shows:

- inputs: transcripts, notes, photos, online posts/comments
- processing: clean, interpret, verify, devil’s advocate, sector translation
- outputs: consultant brief, sales talk track, customer angles, livestream, posts
- feedback loop: what gets verified, learned, reused, or discarded

Save diagrams as `.excalidraw` files and link or attach them when useful.

## Multi-Session / End-of-Day Synthesis

When Gavi uploads multiple sessions from a day, produce a **Conference Intelligence Brief**:

1. **The 5 big themes everyone is circling**
2. **What’s actually new** versus recycled vendor theatre
3. **What people are overhyping**
4. **What people are underestimating**
5. **What a CAIO should do next**
6. **Implications for Advancing Analytics / DAIS positioning**
7. **Client conversation starters**
8. **People and companies to follow up with**
9. **Content calendar:** 5–10 post ideas
10. **Learning plan:** what Gavi should study next

## Output Templates

### Session Intelligence Card

```markdown
## Session: <title>
Speaker: <name/company>
Source: Otter transcript + notes/photos
Confidence: High / Medium / Low

### Bottom line
<one punchy paragraph>

### What was said
- ...

### Why it matters
- ...

### For the team
- ...

### For clients
- ...

### For Gavi to learn
- ...

### Post ideas
- LinkedIn: ...
- X: ...

### Follow-ups
- ...

### Verify before external use
- ...
```

### Team Brief Format

```markdown
## Conference note for the team: <topic>

### What changed / what I heard
- ...

### Why we should care
- ...

### For technical AI consultants
- Delivery implication: ...
- Architecture / data / governance implication: ...
- Reusable asset or demo idea: ...
- Technical questions to debate: ...

### For sales / growth
- Plain-English talk track: ...
- Client trigger to listen for: ...
- Best next question to ask: ...
- Objections likely to come up: ...

### What this means for our work
- Delivery: ...
- Sales: ...
- Partnerships: ...
- Demos/assets: ...

### Questions for us
1. ...
2. ...
3. ...

### Suggested next actions
- ...
```

### LinkedIn Draft Format

```markdown
Hook: <short direct opening>

Post:
<draft in Gavi’s voice>

Why this works:
- ...

Risk check:
- Public-safe? yes/no
- Needs source? yes/no
- Any client/private detail? yes/no
```

## Public Posting Rules

Before drafting public content:

- Remove private/client-sensitive details.
- Do not quote speakers if the session was off-record, Chatham House, private, or unclear.
- Do not use photos of slides publicly unless allowed.
- Treat vendor claims as claims, not facts, unless verified.
- If using a statistic, include source or mark “speaker claimed”.
- Avoid “at conference X everyone agreed…” unless genuinely supported.
- Keep Gavi’s voice: concise, punchy, warm, personal, rough-edged, not consultant-polished.

## Learning Mode

When Gavi wants to learn from the content, produce:

- **Beginner version:** no jargon, analogies first.
- **Technical version:** architecture, tools, dependencies, risks.
- **CAIO version:** decisions, governance, investment, operating model.
- **Teach-back questions:** ask Gavi 3–5 questions she can answer to prove she gets it.
- **Flashcards:** term → plain English → why it matters.
- **One whiteboard analogy:** something she can explain in a meeting.

## Team Use Cases

Convert conference material into:

- weekly internal digest
- client trend memo
- DAIS/Databricks opportunity radar
- sales enablement notes
- demo ideas backlog
- objection-handling bank
- “what clients will ask next” brief
- competitor/vendor watchlist
- training materials for juniors
- board/executive briefing
- podcast/talk/deck outline

## YouTube Livestream Prep

When Gavi says she is hosting a YouTube livestream/playback after the conference, turn the conference intelligence into a show pack, not a transcript recap.

Produce:

- **Show title options:** sharp, beginner-friendly, non-boring.
- **Core thesis:** the opinionated thing Gavi believes after attending.
- **3-act running order:** what happened → what it means → what customers should do.
- **Opening monologue:** 60–90 seconds in Gavi’s voice.
- **Segment cards:** 5–7 sections with hooks, examples, and transitions.
- **FSI lens:** bank/insurance/wealth examples, risk, governance, regulation, model assurance, customer trust.
- **Retail/CPG lens:** AI shelf, recommendation engines, product content, agents, supply chain, customer experience.
- **Real-world examples:** only use sourced/public-safe examples or clearly label as hypothetical.
- **Opinion spine:** what Gavi agrees with, disagrees with, thinks is overhyped, and thinks people are missing.
- **Audience interaction:** polls, chat prompts, questions to ask viewers, “tell me if you’re seeing this too”.
- **Clips bank:** 5 short punchy moments that can become LinkedIn/X clips afterwards.
- **Customer CTA:** what FSI/retail leaders should do next week.

Default structure:

1. **Cold open:** “Here’s the thing nobody said plainly at the conference…”
2. **The three signals:** the most important patterns across sessions.
3. **What this means for customers:** split FSI and retail/CPG.
4. **Where I disagree:** one provocative but defensible take.
5. **Real examples:** public examples, not private conference gossip.
6. **What to do now:** 3 practical actions.
7. **Audience Q&A:** questions seeded from transcript themes.
8. **Close:** memorable CAIO takeaway and follow-up CTA.

Public safety rules for livestream:

- Do not replay private/off-record material.
- Do not show slide photos unless sharing is clearly permitted.
- Use “speaker argued/claimed” for unverified claims.
- Prefer public real-world examples over private anecdotes.
- Keep client names out unless already public and safe.
- Make Gavi’s opinion explicit: the audience is there for her judgement, not a neutral transcript readout.

## Image / Photo Handling

When photos are uploaded:

1. Inspect with vision/OCR.
2. Extract visible text, logos, diagrams, frameworks, and speaker names.
3. Tie each photo to transcript timing if possible.
4. Flag if image quality is too poor to trust.
5. Do not infer hidden slide content.
6. For public posts, ask whether the photo is safe/allowed to share if not obvious.

## Common Pitfalls

1. **Only summarising.** Summaries are table stakes. The value is team action, learning, content, and commercial relevance.

2. **Confusing transcript confidence with truth.** Otter can mishear names, products, numbers, and acronyms. Mark uncertain claims and verify before external use.

3. **Publishing private conference material.** Some sessions are under Chatham House or no-recording norms. Keep public drafts safe.

4. **Writing generic LinkedIn slop.** Avoid “In today’s rapidly evolving landscape...” and other dead phrases. Use concrete moments, sharp takes, and Gavi’s voice.

5. **Missing the team angle.** Always ask: who needs to know this, what should they do differently, and what artefact helps them act?

6. **Letting photos rot.** Photos often contain the best frameworks and diagrams. Extract them quickly while Gavi remembers context.

7. **Not creating a follow-up list.** Conferences are opportunity engines. Always extract people, companies, tools, and next steps.

## Verification Checklist

Before finalising any output:

- [ ] Transcript/notes/photos were separated from interpretation.
- [ ] Speaker names, companies, and claims are marked uncertain if needed.
- [ ] Team relevance is explicit.
- [ ] Gavi learning angle is included.
- [ ] LinkedIn/X drafts are public-safe and in Gavi’s voice.
- [ ] Follow-ups and actions are extracted.
- [ ] Claims needing external sources are flagged.
- [ ] Confidential/client-sensitive details are excluded from public content.
