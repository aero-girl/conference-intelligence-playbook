# Tomorrow Conference Intelligence Test Run — 2026-06-16

Generated: 2026-06-15 23:34 UTC

## Status

**Core synthesis workflow:** ready.

**Live X/web signal via xAI/Grok:** blocked until `XAI_API_KEY` is loaded into the Hermes runtime.

**Raw X API via xurl:** blocked until an X app is registered in `xurl`.

This means tomorrow's workflow can still process transcripts, notes, photos, session titles, and Gavi's reactions immediately. It cannot yet pull live X/Grok signal from Hermes until credentials are loaded/restarted.

## Smoke test results

### Environment checks

- `XAI_API_KEY set`: false
- xAI helper script exists: true
- `xurl` command present: true
- `xurl auth status`: `No apps registered. Use 'xurl auth apps add' to register one.`
- GitHub Pages repo HEAD: `ae7d733`

### xAI helper behaviour

Command tested:

```bash
python /root/.hermes/skills/research/xai-grok-search/scripts/grok_search.py web "Smoke test: return one cited source about enterprise AI governance"
```

Observed result:

```text
XAI_API_KEY is not set in this Hermes environment.
```

This is the correct safe failure mode: it does not print secrets and it stops cleanly.

## Tomorrow operating mode

### If xAI is fixed before the conference

Use this exact prompt:

```text
Use conference-intelligence-synthesis and xai-grok-search.

Search X and the web for current public discussion of: <conference/session/theme>.

Return:
1. Sources worth opening, with links and dates where available.
2. Top opinions people are expressing.
3. Best objections, comments, or questions.
4. What is hype vs substantive.
5. Devil's advocate: what a CISO, procurement lead, model-risk owner, or sceptical CAIO would challenge.
6. What Gavi can say to technical AI consultants.
7. What Gavi can say to sales/growth.
8. FSI customer angles.
9. Retail/CPG customer angles.
10. Claims that need verification before public use.

Preserve citations/source links. Do not invent metrics. If replies/comments are not visible, say so.
```

Expected command shape:

```bash
python /root/.hermes/skills/research/xai-grok-search/scripts/grok_search.py x "<prompt above>"
python /root/.hermes/skills/research/xai-grok-search/scripts/grok_search.py web "<prompt above>"
```

### If xAI is still not fixed

Run the conference workflow without live social signal:

```text
Use conference-intelligence-synthesis.

I am uploading conference material from <session/theme>.
Turn it into:
1. 60-second executive summary
2. technical AI consultant briefing
3. sales/growth talk track
4. Gavi learning brief with beginner analogy and Socratic why-chain
5. FSI customer angle
6. retail/CPG customer angle
7. LinkedIn/X draft ideas in my voice
8. devil's advocate challenge
9. claims to verify before external use
10. follow-up/action tracker
```

## Live capture checklist for Gavi

For each session, capture these if possible:

- Session title
- Speaker name/company
- One photo of agenda/title slide
- 2–3 photos of key slides/frameworks, only if allowed
- Otter transcript or rough notes
- Your own 3 reactions:
  - what landed?
  - what felt like vendor theatre?
  - what would a client ask us after hearing this?
- Any named tools/vendors/frameworks
- Any claims/statistics that need verification
- Any people to follow up with

## Output stack tomorrow

Default deliverable per session:

1. Bottom line
2. What was said vs what it means
3. Consultant implications
4. Sales/growth talk track
5. FSI angle
6. Retail/CPG angle
7. Gavi learning brief
8. Public-safe content ideas
9. Devil's advocate
10. Verify-before-posting list
11. Follow-up tracker

End-of-day deliverable:

1. The five themes everyone is circling
2. What's actually new vs recycled vendor theatre
3. What people are overhyping
4. What people are underestimating
5. What a CAIO should do next
6. Implications for DAIS / Advancing Analytics positioning
7. Client conversation starters
8. People/companies to follow up with
9. Content calendar
10. Learning plan

## Credential fix needed before live social listening

Do not paste keys into Telegram.

On the VPS, add:

```bash
XAI_API_KEY=<key>
```

to:

```text
/root/.hermes/.env
```

Then restart Hermes/gateway so the environment is loaded.

Optional X API route:

```bash
xurl auth apps add
xurl auth status
```

Only needed if we need raw post/reply/thread data rather than Grok-cited synthesis.

## Public safety rules

- No private/client details in public posts.
- Do not quote private/off-record sessions externally.
- Do not publish slide photos unless sharing is clearly allowed.
- Treat vendor claims as claims until verified.
- Use “speaker argued/claimed” for unverified stats.
- Keep the opinion spine in Gavi’s voice: concise, specific, warm, not LinkedIn mush.
