---
name: linkedin-review
description: Review a drafted LinkedIn post specifically for platform fit — hook strength, formatting, length, tags — before it goes into the full content-package-review gate. Use right after linkedin-writing produces a draft.
---

# LinkedIn Review

This is a platform-fit check, narrower than [[content-package-review]]
(which covers the whole package: facts, image, alt text, compliance).
Run this first, on the post alone.

## Checklist

- **Hook**: does the first ~210 characters stand alone and earn a "see
  more" click? Is it grounded in the actual research (not a generic or
  clickbait-y line unsupported by the body)?
- **Formatting**: short paragraphs, scannable, no dense walls of text.
- **Voice**: does it sound like the client (energetic, creative, warm,
  personal) rather than generic corporate LinkedIn voice? Check against
  `brand-voice.md`.
- **Audience clarity**: is it clearly written for one of the two
  audiences (art collectors vs. automation businesses), or a topic that
  genuinely bridges both — not a muddled in-between?
- **Length**: proportionate to the topic's substance, not padded or
  stubby.
- **CTA**: present, natural, matches approved CTAs or the soft-CTA
  default.
- **Hashtags/mentions**: minimal, relevant, not forced.
- **No politics** and no other avoid-list violations.
- **No AI-slop phrasing** — generic hype words, fake intimacy,
  unsupported superlatives.

## Output

Add a **LinkedIn platform review** section to
`clients/[client-slug]/posts/[NNN-topic-slug]/review.md` with a
PASS/NEEDS REVISION verdict per checklist item, and a short list of
specific edits if anything needs revision. If it needs revision, revise
and re-check before moving on — don't pass a draft with open issues into
[[content-package-review]].
