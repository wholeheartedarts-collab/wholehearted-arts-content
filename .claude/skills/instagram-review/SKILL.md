---
name: instagram-review
description: Review a drafted Instagram caption specifically for platform fit — hook length, hashtag mix, link handling — before it goes into the full content-package-review gate. Use right after instagram-writing produces a draft.
---

# Instagram Review

This is a platform-fit check, narrower than [[content-package-review]]
(which covers the whole package: facts, image, alt text, compliance).
Run this first, on the caption alone.

## Checklist

- **Hook**: does the first ~125 characters stand alone and earn a "...
  more" tap? Grounded in the actual research/image, not generic or
  clickbait-y.
- **Image-caption fit**: does the caption make sense as support for the
  actual final image, not just the topic in the abstract? (Instagram is
  image-first — a caption that would work with any image is a problem.)
- **Formatting**: short lines, native use of line breaks. Emoji only if
  they match brand-voice.md, not decorative overuse.
- **Voice**: sounds like Agata (energetic, creative, warm, personal), not
  generic influencer-hype voice. Check against `brand-voice.md`.
- **Links**: confirm no raw clickable-link expectation in the caption
  text (Instagram captions aren't clickable) — "link in bio" or nothing.
- **Length**: proportionate — Instagram audiences scan fast; not padded.
- **CTA**: present, natural, matches approved CTAs or the soft-CTA
  default.
- **Hashtags**: maximum 5 (Agata's explicit rule — see
  instagram-writing's Hashtags section), relevant, a real mix (not 5
  near-duplicates or 5 generic art tags unrelated to this specific
  piece). Flag as NEEDS REVISION if the draft has more than 5.
- **No politics** and no other avoid-list violations.
- **No AI-slop / generic IG-hype phrasing**.

## Output

Add an **Instagram platform review** section to
`clients/[client-slug]/posts/[NNN-topic-slug]/instagram-review.md` with a
PASS/NEEDS REVISION verdict per checklist item, and specific edits if
anything needs revision. If it needs revision, revise and re-check before
moving on — don't pass a draft with open issues into
[[content-package-review]].
