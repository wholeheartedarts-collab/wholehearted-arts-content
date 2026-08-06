---
name: facebook-review
description: Review a drafted Facebook post specifically for platform fit — tone, length, link handling, hashtag use — before it goes into the full content-package-review gate. Use right after facebook-writing produces a draft.
---

# Facebook Review

This is a platform-fit check, narrower than [[content-package-review]]
(which covers the whole package: facts, image, alt text, compliance).
Run this first, on the post alone.

## Checklist

- **Hook**: clear, grounded opening line — not clickbait, not buried.
- **Tone**: conversational/story-driven, community-feeling rather than
  professional-insight (LinkedIn) or fast-scroll-visual (Instagram).
  Check against `brand-voice.md`.
- **Formatting**: readable paragraph lengths for Facebook's audience —
  less strict than Instagram, but still not a dense wall of text.
- **Audience clarity**: written for one of the two audiences (art
  collectors vs. automation businesses), or a topic that genuinely
  bridges both — not muddled.
- **Length**: proportionate to the topic's substance.
- **Links**: if a link is included, confirm it's a real clickable link
  used appropriately (Facebook supports this, unlike Instagram).
- **Hashtags**: 0-2 only. Flag anything with more as copied from another
  platform's convention.
- **CTA**: present, natural, matches approved CTAs or the soft-CTA
  default.
- **No politics** and no other avoid-list violations.
- **No AI-slop phrasing**.

## Output

Add a **Facebook platform review** section to
`clients/[client-slug]/posts/[NNN-topic-slug]/facebook-review.md` with a
PASS/NEEDS REVISION verdict per checklist item, and specific edits if
anything needs revision. If it needs revision, revise and re-check before
moving on — don't pass a draft with open issues into
[[content-package-review]].
