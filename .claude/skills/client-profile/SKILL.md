---
name: client-profile
description: Load, validate, and update a client's profile before running any other content skill. Use at the start of any content job, when a new client is onboarded, or when profile details change.
---

# Client Profile

Every content job operates against exactly one client. Before doing
anything else (research, writing, images, review), load that client's
profile from:

```
clients/[client-slug]/profile/profile.md
```

## On job start

1. Confirm the client slug. If ambiguous, ask.
2. Read the profile file in full. Note anything marked **PROVISIONAL** —
   treat those fields as best-guess defaults, not confirmed facts, and
   flag content decisions that lean heavily on a provisional field.
3. Check the "Open items to fill in later" section. If a missing item is
   required for the current job (e.g., no CTA defined and the post needs
   one), ask the human rather than inventing one silently.

## Required fields a complete profile must have

- Client slug, industry
- Account type per active platform (e.g. LinkedIn personal profile,
  Instagram Business/Creator account, Facebook Page) — only require the
  platforms actually active for this client, don't invent accounts for
  platforms not in use
- Audience(s) and business goal(s)
- Content pillars
- Voice description (and whether it's provisional or sample-derived)
- Avoid list
- Approved CTAs (or explicit "not yet defined — use soft CTA default")
- Publishing cadence

## Creating a new client

```
clients/[new-client-slug]/
  profile/profile.md
  brand-assets/
  visual-style/
  posts/
```

Ask for the same intake fields listed above. If the human can only give
partial answers, build the profile anyway, mark unanswered fields
provisional, and proceed — do not block setup on incomplete branding
details unless a field is required for the immediate job.

## Updating a profile

- Voice: after [[brand-voice]] analyzes real writing samples, replace the
  provisional voice section and remove the PROVISIONAL flag.
- Cadence, CTAs, compliance constraints: update whenever the human gives
  new direction. Keep the "Open items" list current — remove items once
  resolved, add new ones as they surface.
- Never delete history silently; if a major rewrite is needed, note what
  changed and why at the top of the file.
