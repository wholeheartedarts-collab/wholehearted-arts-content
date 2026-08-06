---
name: linkedin-writing
description: Write a LinkedIn post from a completed research brief and the client's brand-voice guide. Use only after research.md exists for the topic; do not use for other platforms.
---

# LinkedIn Writing

## Prerequisites

- `research.md` for the topic must exist (see [[research]]).
- `clients/[client-slug]/profile/brand-voice.md` must exist (see
  [[brand-voice]]) — provisional is acceptable, missing is not.

## LinkedIn-specific requirements

- **Opening**: the first ~210 characters / first two visible lines must
  work as a standalone hook, since LinkedIn truncates and shows a "see
  more" link after that point. Use a contrarian idea, a specific number,
  a surprising fact, a genuine question, or a "most people think X, but
  actually Y" structure — grounded in the actual research, not invented.
- **Structure**: short paragraphs (1-3 lines), generous white space,
  scannable. Long unbroken blocks of text underperform on LinkedIn.
- **Body**: professional insight backed by concrete evidence from
  research.md. Show, don't tell.
- **Length**: favor a length that earns the "see more" click and rewards
  it — neither a stub nor a wall of text. Let the topic's substance set
  the length rather than a fixed target.
- **CTA**: natural, matched to the client's approved CTAs (see profile).
  If none are approved yet, default to a soft CTA (invite comments/DMs,
  point to relevant work) rather than a hard sell.
- **Hashtags/mentions**: only when they add real discoverability or
  credit — never forced, never more than a small handful.
- **Account type**: this client posts from a **personal profile**, so
  first-person, personal voice is correct — avoid switching to
  brand/company phrasing.

## Two-audience awareness

Wholehearted Arts content pillars split across two audiences (art
collectors vs. automation-buying businesses). Before writing, identify
which pillar/audience this topic serves and write for that audience
specifically — don't try to serve both in one post unless the topic
genuinely bridges them (e.g., "how I use AI in my own art practice" can
legitimately speak to both).

## Output

Save `clients/[client-slug]/posts/[NNN-topic-slug]/linkedin-post.md`:

```
## Hook
[opening lines]

## Body
[full post]

## CTA
[final line(s)]

## Hashtags/Tags
[if any, with rationale]

## Angle used
[which research angle this draft took, and which audience/pillar it serves]
```

## Hard rules

- Every factual claim must trace to `research.md` — no invented stats,
  quotes, or stories. See [[factual-verification]].
- No politics (client's explicit avoid-list item).
- Avoid AI-slop phrasing — see [[brand-voice]] quality rules.
- Do not generate or reference an image here — imagery happens after the
  post is finalized, in [[image-generation]].
