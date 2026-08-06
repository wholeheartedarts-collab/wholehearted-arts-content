---
name: performance-learning
description: Log post performance and periodically propose evidence-based improvements to hooks, angles, formats, and cadence. Use when the human reports metrics for a published post, or periodically once enough posts have data.
---

# Performance Learning

## Logging

When the human reports metrics for a published post, append to
`clients/[client-slug]/performance-log.md` (create if missing). Use the
metric fields for the platform that post was actually published on —
don't force one platform's terminology onto another.

```
## [NNN-topic-slug] - [platform] - [date published]
- Impressions/Reach:
- [platform-specific engagement fields, see below]
- Clicks:
- Leads/DMs:
- Notes: [audience/pillar it targeted, anything unusual]
```

Platform-specific engagement fields:

- **LinkedIn:** Reactions, Comments, Shares, Saves
- **Instagram:** Likes, Comments, Saves, Shares, Follows gained
- **Facebook:** Reactions, Comments, Shares

If the same topic was posted to multiple platforms, log a separate entry
per platform (same topic slug, different platform label) rather than one
merged entry — performance varies by platform and merging hides that.

Only log approved metrics the human actually provides — never estimate or
invent numbers.

## Analysis

Once there's a **meaningful sample** (roughly 8-10 posts minimum — do not
draw conclusions from 1-2 data points), look for patterns across:

- Hook types (contrarian / stat-led / question / etc.)
- Content pillar (art / books / AI venture) and which audience it served
- Format (short vs. long, image style)
- Posting day/time, if cadence data exists
- Platform (LinkedIn vs. Instagram vs. Facebook) — a hook or format that
  wins on one platform may not transfer to another; don't average across
  platforms when proposing changes to a specific platform's writing
  skill

## Output

Propose specific, evidence-linked changes to the relevant platform's
writing skill ([[linkedin-writing]], [[instagram-writing]], or
[[facebook-writing]]) or to [[visual-style]] — e.g., "LinkedIn posts
opening with a specific number outperformed question-hooks 3:1 across
the last 9 LinkedIn posts; consider favoring that pattern for the
AI-venture pillar on LinkedIn." Cite the posts behind the claim, and keep
the recommendation scoped to the platform the data came from unless the
same pattern is independently confirmed on another platform too.

## Hard rules

- Optimize for outcomes tied to the client's actual business goal
  (credibility, new clients) — not vanity engagement alone. A
  high-reaction post that doesn't serve the goal is not automatically a
  win.
- Never silently rewrite the core brand voice based on one post's
  performance. Voice changes go through [[brand-voice]] deliberately, with
  the human's sign-off, not as an automatic side effect of this skill.
