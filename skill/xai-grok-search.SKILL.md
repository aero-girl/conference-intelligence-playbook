---
name: xai-grok-search
description: Use xAI Grok Responses API for live web and X search with citations, especially to pull current posts/opinions/comments around conference topics before synthesis.
version: 1.0.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [xai, grok, x-search, web-search, social-listening, citations]
    related_skills: [conference-intelligence-synthesis, xurl, last30days-research]
---

# xAI Grok Search

Use this skill when Gavi wants live web/X signal from xAI/Grok: top public posts, opinions, objections, comments/replies where available, citations, and quick synthesis for internal teams and customers.

## What this is

xAI has a Responses API at `https://api.x.ai/v1/responses` that supports tools including:

- `web_search` — current web/news/docs search with citations.
- `x_search` — current X/Twitter search with citations.

This is different from `xurl`:

- `xai-grok-search` asks Grok to search and synthesise with citations.
- `xurl` directly calls the official X API and is better when we need raw post objects, IDs, replies, metrics, timelines, or write actions.

Default preference for Gavi’s conference intelligence:

1. Use `xai-grok-search` first for fast X/web synthesis with citations.
2. Use `xurl` when configured for deeper raw X retrieval, reply/thread inspection, or exact post metadata.
3. Preserve source links; do not treat Grok’s synthesis as evidence by itself.

## Safety / secrets

- Never ask Gavi to paste API keys into chat.
- Never print `.env` or token files.
- Check only whether `XAI_API_KEY` is set, not its value.
- If missing, tell Gavi to add it to `/root/.hermes/.env` and restart Hermes/gateway.
- Never perform X write actions from this skill. This is read/synthesis only.

## Prerequisite check

```bash
python3 - <<'PY'
import os
print('XAI_API_KEY set:', bool(os.environ.get('XAI_API_KEY')))
PY
```

If Hermes has not loaded the env after adding the key, restart the gateway/session.

## Basic usage via helper script

Use the bundled helper script so the API key stays in the environment and is never printed:

```bash
python /root/.hermes/skills/research/xai-grok-search/scripts/grok_search.py x "Search X for current posts about <topic>. Return top opinions, notable posts with source links, useful replies/comments if visible, and what a sceptical CAIO should challenge."
```

For web search:

```bash
python /root/.hermes/skills/research/xai-grok-search/scripts/grok_search.py web "Search the web for current analysis of <topic>. Return cited sources, strongest arguments, counterarguments, and implications for FSI and retail/CPG customers."
```

## Direct API shape

If writing a custom request, use xAI Responses API with `tools: [{"type":"x_search"}]` or `tools: [{"type":"web_search"}]`; keep the key in `XAI_API_KEY` and never inline it in prompts or chat.

Useful `x_search` parameters:

- `allowed_x_handles`: only consider posts from specified handles, max 20.
- `excluded_x_handles`: exclude specified handles, max 20.
- `from_date`: ISO8601 start date.
- `to_date`: ISO8601 end date.
- `enable_image_understanding`: analyse images in posts.
- `enable_video_understanding`: analyse videos in posts.

Example constrained search:

```json
{
  "type": "x_search",
  "from_date": "2026-06-01T00:00:00Z",
  "to_date": "2026-06-15T23:59:59Z",
  "enable_image_understanding": true
}
```

## Basic web search call

Use the helper script shown above with `web` mode, or call the Responses API with `tools: [{"type":"web_search"}]`.

Useful `web_search` parameters:

- `allowed_domains`: search only specific domains, max 5.
- `excluded_domains`: exclude specific domains, max 5.
- `enable_image_understanding`: analyse images on pages where available.

## Prompt pattern for conference intelligence

Ask Grok for structured output so it does not return mush:

```text
You are supporting a Chief AI Officer preparing post-conference intelligence.
Search X and/or the web for current public discussion of: <topic/conference/theme>.

Return:
1. Top posts or sources worth reading, with links and dates where available.
2. The strongest opinions people are expressing.
3. The best objections, comments, or questions.
4. What is hype vs what seems substantive.
5. Devil's advocate: what a CISO, procurement lead, model-risk owner, or sceptical CAIO would challenge.
6. What Gavi can say to highly skilled AI consultants.
7. What Gavi can say to sales/growth without technical detail.
8. FSI customer angles.
9. Retail/CPG customer angles.
10. Claims that need verification before public use.

Preserve citations/source links. Do not invent metrics. If a reply/comment is not visible, say so.
```

## Output contract

Always reduce the result into this shape for Gavi:

```markdown
## xAI/Grok signal: <topic>

### Sources worth opening
- <source/link/date> — why it matters

### Top opinions
- ...

### Best comments / objections
- ...

### Devil’s advocate
- ...

### What Gavi can say quickly
- Technical AI consultants: ...
- Sales/growth: ...
- FSI customers: ...
- Retail/CPG customers: ...

### Source quality / verification
- Strong: ...
- Weak/hype: ...
- Verify before posting: ...
```

## Common pitfalls

1. **Confusing xAI search with raw X API.** Grok can search and cite, but if we need exact metrics/replies/thread structure, use `xurl` too.
2. **Letting Grok paraphrase without links.** Ask for citations/source links explicitly and preserve them in the final answer.
3. **Treating social consensus as truth.** Social posts are signal, not evidence. Validate claims before public use.
4. **Over-serving the sales team.** Sales needs triggers and talk tracks, not architecture dumps.
5. **Under-serving consultants.** Consultants need implementation implications, risks, and assets to build.
