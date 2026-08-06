---
name: research
description: Research a content topic and produce a structured research brief. Use at the start of every content job, before any writing or image work. Prefer the cheapest capable model for this skill.
---

# Research

## Model routing

This is broad, mechanical research work — use the **cheapest capable
model** available. Do not use a premium/reasoning model for this step.
Reserve stronger models for [[brand-voice]], [[linkedin-writing]], and
[[content-package-review]].

## Input

- Topic
- Client slug (to load pillar/audience context from [[client-profile]])
- Any specific requirements the human gave (required examples, a date
  window, a particular angle to include or avoid)

## Output

Save as `clients/[client-slug]/posts/[NNN-topic-slug]/research.md`:

1. **Executive summary** — 2-4 sentences.
2. **Key points** — the load-bearing facts and arguments.
3. **Notable statistics** — each with its source and date.
4. **Specific examples** — concrete, recent, real cases (not invented
   composites).
5. **Risks, counterarguments, or limitations** — every topic with real
   drawbacks must include them here; do not produce one-sided research on
   a topic where balance matters (this client's AI-automation pillar
   especially needs honest limitations, not hype).
6. **Possible content angles** — 3-5 distinct angles a writer could take.
7. **Source list** — direct link, publisher, title, date for every
   source used.
8. **Research notes** — explicitly separate sourced facts from your own
   inference or synthesis. If evidence for a claim is weak, say so.

Also save `clients/[client-slug]/posts/[NNN-topic-slug]/sources.md` as a
clean, standalone source list (subset of the above) for quick fact-checks
during review.

## Hard rules

- Never invent a source, quotation, statistic, or example. If you can't
  verify something, label it as unverified or leave it out.
- Prefer primary and authoritative sources over aggregators.
- Verify that time-sensitive claims (stats, "recent" examples) are
  actually current — check publish dates.
- If specialized domain data is genuinely needed (e.g., art market data,
  SMB automation adoption stats) and a general web search can't get it,
  say so explicitly rather than silently producing thin research — do not
  add API complexity that wasn't requested.
