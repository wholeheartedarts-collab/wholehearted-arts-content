# Social Media Content System — Orchestrator

## Mission

Produce research-backed, brand-consistent social content packages for
each client — across whichever platforms are active for them (LinkedIn,
Instagram, Facebook) — and stop for human approval before anything is
scheduled or published. This is a repeatable process, not a one-off
"perfect prompt" — persist everything in files so any session can pick up
where the last one left off.

## Current scope

**LinkedIn, Instagram, and Facebook**, as of 2026-08-06. Each platform
has its own writing and review skills with platform-correct rules (hook
length, hashtag density, link handling, tone) — LinkedIn's rules are
never silently reused for Instagram or Facebook, and vice versa. If
another platform is added later, it gets the same treatment: its own
platform-specific skills, not a generalization of an existing one.

Not every topic has to target all three platforms — default to mirroring
a topic across all three unless a topic is genuinely platform-exclusive
(e.g. an Instagram-only Reel idea with no LinkedIn equivalent), in which
case say so explicitly rather than forcing a weak version onto a platform
it doesn't fit.

## Active client

`clients/wholehearted-arts/` — see `clients/wholehearted-arts/profile/profile.md`
for full details (industry, audience, voice, goals, avoid-list). Currently
**provisional** on voice and visual style — no writing samples or
reference images yet.

## Workflow (run in this order for every new topic)

Steps 1-3 and 7 run **once per topic**, shared across whichever platforms
that topic targets. Steps 4-6 and 8-9 run **once per target platform**,
using that platform's own writing/review skills.

1. **[[client-profile]]** — load the client profile first, always.
2. **[[research]]** — research the topic (cheapest capable model).
3. **[[brand-voice]]** — load/confirm the voice guide (build provisionally
   if no samples yet).
4. **Write the post, per platform** — [[linkedin-writing]],
   [[instagram-writing]], and/or [[facebook-writing]] for each targeted
   platform, from the same research + voice.
5. **Platform-fit review, per platform** — [[linkedin-review]],
   [[instagram-review]], and/or [[facebook-review]] on each draft; revise
   and re-check until each passes.
6. **[[factual-verification]]** — verify every claim against sources
   (shared across platform variants, since the underlying facts are the
   same topic).
7. **[[visual-style]]** — load the client's style guide (placeholder is
   fine until reference images exist), including its per-platform
   dimensions.
8. **[[image-generation]], per platform** — generate (or source, if the
   human wants a real photo instead) one image per targeted platform,
   sized to that platform's dimensions, *only after* that platform's post
   is finalized. Never generate an image from the topic alone.
9. **[[accessibility-alt-text]], per platform** — write alt text for each
   platform's final image.
10. **[[content-package-review]]** — full package review gate, covering
    every platform variant produced for this topic together. Fix any FAIL
    before presenting; surface every NEEDS HUMAN DECISION explicitly.
11. Present the complete package (all platform variants) and **stop**. Do
    not move to [[publishing-handoff]] without explicit human approval
    naming the exact package — and for scheduling via Buffer, an explicit
    date/time per platform.

[[performance-learning]] runs separately, whenever the human reports
metrics on a published post, or periodically once enough posts have data.

## Model routing

- Cheapest capable model: [[research]], mechanical extraction/formatting.
- Stronger model: [[brand-voice]] synthesis, [[linkedin-writing]],
  [[instagram-writing]], [[facebook-writing]], [[content-package-review]]
  judgment calls.
- Don't default to the largest model for simple, repetitive work.

## Folder conventions

```
clients/[client-slug]/
  profile/profile.md            client config + brand-voice.md
  brand-assets/                 logos, existing photos, etc.
  visual-style/style-guide.json
  performance-log.md
  posts/
    [NNN-topic-slug]/
      brief.md
      research.md                 shared across platforms
      sources.md                  shared across platforms
      fact-check.md                shared across platforms
      linkedin-post.md
      linkedin-review.md
      instagram-post.md
      instagram-review.md
      facebook-post.md
      facebook-review.md
      package-review.md            final gate, covers every platform variant
      status.json                  per-platform status map (see below)
      images/
        linkedin-v1.png, instagram-v1.png, facebook-v1.png, ...
        never overwrite — new version per regen, per platform
      alt-text/
        linkedin.md, instagram.md, facebook.md
```

Number topic folders sequentially (`001-`, `002-`, ...) in creation order.
Never overwrite an approved package — create a new version with traceable
history instead.

**Single-platform topics** (still common — not every topic needs all
three) may skip files for platforms not targeted; don't create empty
`facebook-post.md` etc. just to match the template.

**Legacy note:** posts `001` and `002` predate this multi-platform
convention and use the older flat, LinkedIn-only layout (`linkedin-post.md`,
a single `review.md` covering platform review + fact-check + package
review, unprefixed `images/v1.png`). They are not being migrated — this
convention applies to new topics going forward.

`status.json` for a multi-platform topic carries a `platforms` object so
each platform can be at a different stage:

```json
{
  "platforms": {
    "linkedin": {"status": "approved", "scheduled_via": "buffer", "scheduled_for": "..."},
    "instagram": {"status": "review-ready"},
    "facebook": {"status": "review-ready"}
  },
  "history": [...]
}
```

## Safety rules (non-negotiable)

- **No fabrication.** Never invent a source, statistic, quote, example, or
  personal story. See [[factual-verification]].
- **No secrets in the repo.** API keys live in environment variables only
  (see `.env.example`). Never ask the human to paste a key into chat,
  never write one into any file here.
- **No auto-publishing by default, and never via browser bots or
  scraping, ever.** Default to a human-led manual publish for every
  platform. The one sanctioned exception: an explicitly authorized,
  officially supported API integration — currently **Buffer**, connected
  via its official MCP server with Agata's own OAuth login, covering
  LinkedIn, Instagram Business, and the Facebook Page. Even through
  Buffer, nothing is scheduled without an explicit human instruction
  naming the exact package and platform. See [[publishing-handoff]].
- **No status skipping.** draft → review-ready → approved → scheduled →
  published are distinct; only a human moves a package past
  review-ready.
- **No politics** in content (client's explicit avoid-list item).
- **Stay in scope.** Don't add API integrations, platforms, or complexity
  the current job doesn't need.

## Adding a new client

Follow [[client-profile]]'s onboarding steps. Update this file's "Active
client" section if the new client becomes the default, or note multiple
active clients if running several in parallel.

## When adding or changing a skill

Update this file's workflow/routing list so it stays accurate — an
orchestrator that points to stale skills is worse than no orchestrator.
