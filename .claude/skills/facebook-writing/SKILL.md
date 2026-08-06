---
name: facebook-writing
description: Write a Facebook Page post from a completed research brief and the client's brand-voice guide. Use only after research.md exists for the topic; do not use for other platforms.
---

# Facebook Writing

## Prerequisites

- `research.md` for the topic must exist (see [[research]]).
- `clients/[client-slug]/profile/brand-voice.md` must exist (see
  [[brand-voice]]) — provisional is acceptable, missing is not.

## Facebook-specific requirements

- **Opening**: Facebook truncates later than Instagram and shows more
  text before "See more" than either LinkedIn or Instagram in-feed on
  most devices, but don't rely on that — still lead with a clear,
  grounded opening line rather than burying the point.
- **Tone**: conversational and story-driven performs well on Facebook —
  closer to talking to a community than presenting professional insight
  (LinkedIn) or a fast visual scroll (Instagram). Still first-person,
  still Agata's actual voice per brand-voice.md.
- **Length**: shorter, punchier posts generally outperform long ones on
  Facebook, but it's less strict than Instagram — let the topic's
  substance set the length, same principle as [[linkedin-writing]].
- **Links**: unlike Instagram, Facebook posts support real clickable
  links inline — fine to link directly to wholeheartedarts.com or a
  specific piece's page when relevant.
- **Hashtags**: use sparingly — 1-2 at most, if any. Facebook is not a
  hashtag-discovery platform the way Instagram is; more than 1-2 reads as
  copy-pasted from another platform.
- **Audience**: broader and more general than LinkedIn's professional
  context — can include local community, family, and general art-lovers
  audiences, not just serious collectors or business buyers. Same
  avoid-list (no politics) and same brand-voice.md still apply.
- **Account type**: this client posts from a **Facebook Page** for
  WholeheartedArts (confirmed by Agata), not a personal profile — voice
  should still read as Agata herself, not a corporate brand voice.

## Two-audience awareness

Same split as [[linkedin-writing]]: art collectors vs. automation-buying
businesses. Facebook's broader/community audience can suit either pillar
reasonably well — pick the audience the specific topic actually serves,
same rule as the other platforms; don't force both into one post unless
the topic genuinely bridges them.

## Output

Save `clients/[client-slug]/posts/[NNN-topic-slug]/facebook-post.md`:

```
## Hook
[opening line(s)]

## Body
[full post]

## CTA
[final line(s)]

## Hashtags
[0-2 tags, if any, with rationale]

## Angle used
[which research angle this draft took, and which audience/pillar it serves]
```

## Hard rules

- Every factual claim must trace to `research.md` — no invented stats,
  quotes, or stories. See [[factual-verification]].
- No politics (client's explicit avoid-list item).
- Avoid AI-slop phrasing — see [[brand-voice]] quality rules.
- Do not generate or reference image content here — imagery happens in
  [[image-generation]], sized for Facebook per [[visual-style]].
- Do not pad the post with hashtags just because Instagram uses more —
  Facebook's norm is different, keep it that way.
