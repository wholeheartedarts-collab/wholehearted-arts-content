# Content package review — 041-protect-my-heart (LinkedIn + Instagram)

## NEEDS HUMAN DECISION (read first)

1. **Atelier collection selection rule could not be followed as written
   this run.** Reconciling the catalog against actual post folders
   (001-040): Atelier has 17 of its 18 catalog entries already used;
   Studio has 21 of 74 used. By raw used-count, the deterministic rule
   points to **Atelier** (fewer used) this run. But Atelier's only
   remaining unused entry, **"Let Our Light Continue to Shine,"** is a
   Hanukkah/menorah piece whose own catalog description explicitly
   states it is "my heartfelt prayer for peace in #Israel and for all
   Jewish people worldwide," with Hebrew blessing text. That combination
   (an explicitly Israel-linked statement, in the current geopolitical
   climate, from a Christian-voice brand account, with no caution_note
   flag in the catalog to catch it mechanically) is exactly the kind of
   call this pipeline is not supposed to make unattended, given the
   client's non-negotiable "no politics, even tangentially" rule. I
   treated it as needing human judgment and did not select it, which
   left Atelier's unused pool empty of viable candidates this run, so I
   drew from **Studio** instead (painting below). **Please decide:** (a)
   whether "Let Our Light Continue to Shine" should ever run through this
   automated pipeline, or only if Agata writes/directs it herself, and
   (b) whether the catalog's `skip_rules`/`caution_note` logic should be
   updated to flag it explicitly so future runs don't have to re-litigate
   this. Also worth knowing: Atelier is now functionally exhausted for
   automated selection (0 of 18 entries both unused and unflagged) - a
   catalog regen from the live Squarespace data may surface new Atelier
   pieces, or Agata may need to decide Atelier simply won't contribute
   new unattended picks until then.
2. **No pre-selected room-mockup photo exists for "Protect My Heart."**
   The catalog has no `chosen_images` entry for this painting (it hasn't
   been through a human/Claude visual review of its 11 product photos
   yet). Per the rule against guessing which photo is a mockup, this
   package uses `primary_image_url` (the listing's main/flat image) for
   both platforms instead. If Agata would prefer a room-mockup shot (she
   has stated she generally does), someone should view the listing's
   other 10 photos and either add a `chosen_images.mockup_url` to the
   catalog or swap the image directly in Buffer before this draft is
   queued.
3. **Image could not be downloaded, cropped, or visually verified in
   this sandbox** - egress to `images.squarespace-cdn.com` returned 403
   (expected, per this routine's own egress note; not retried). The
   image was not resized for LinkedIn (1200x627) or Instagram (1080x1350)
   and alt text is written from the catalog's text description only, not
   from actually viewing the photo. Buffer will fetch the raw URL
   directly from its own servers, but a human should open both drafts in
   Buffer and visually confirm the image looks right before queuing.
4. **Price/availability note:** catalog snapshot (2026-09-01, ~7 weeks
   stale) shows "Protect My Heart" as 0 in stock / sold out. Neither
   draft states or implies it's purchasable, but if Agata wants to
   mention availability/price at all, that needs a fresh check against
   her live Squarespace listing first.
5. **Buffer's Instagram channel shows as disconnected.** Both
   `list_channels` and `get_channel` returned `isDisconnected: true` for
   the Instagram channel (id `6a74f44c99afb44349156296`) before the
   Instagram draft was created. The `create_post` call still succeeded
   and `get_post` confirmed a clean, inert draft (status draft, dueAt
   null, sentAt null, sharedNow false, schedulingType automatic) - so the
   draft itself staged fine - but Agata should reconnect the Instagram
   account in Buffer (OAuth login, Buffer settings) before counting on
   being able to queue or share it from the Drafts tab. If the
   disconnection is real, the draft may need to be recreated after
   reconnecting.

## Checklist

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal match the brief | PASS | Art pillar, collector audience, faith/emotion/healing themes per profile.md. |
| Every claim supported (pull from fact-check.md) | PASS | fact-check.md: all claims SOURCED or clearly framed as interpretation; no UNSUPPORTED items. |
| Balanced treatment of real risks/drawbacks | PASS | research.md's framing-risk note (avoid one-sided "protect yourself" read) was carried into both drafts via the "shield and open, both not either" framing. |
| No fabricated facts/quotes/experiences/results | PASS | No invented backstory; weak psychology research explicitly excluded per research.md. |
| Client voice and avoid-list followed | PASS | No politics; voice checked against brand-voice.md in both platform reviews. |
| Platform-native structure (LinkedIn) | PASS | See linkedin-review.md - PASS on all items. |
| Platform-native structure (Instagram) | PASS | See instagram-review.md - PASS on all items, hashtags at the 5-tag cap. |
| Hook strength and readability | PASS | Both hooks are specific to this painting/verse, not generic. |
| Image relevant, original, on-style-guide, correctly sized | NEEDS HUMAN DECISION | See item 2 and 3 above - no mockup selection exists, and sizing/cropping could not be done due to egress block. Image is a real client product photo (not Gemini-generated), a valid deviation per image-generation's "real photo" path, consistent with Agata's stated preference to use her own art photography over generated imagery. |
| Alt text accurate and matches final image/post | NEEDS HUMAN DECISION | Written from catalog text only, not visual inspection - see item 3. |
| Tags/mentions appropriate, minimal, no unwanted third-party tagging | PASS | No third parties tagged; hashtags are topic-specific. |
| Compliance constraints from profile respected | PASS | No professional/medical/legal claims made. |
| No secrets/API keys/private info in output | PASS | Confirmed by inspection of every file in this topic folder. |

## Overall verdict

**review-ready**, with three NEEDS HUMAN DECISION items above that must
be read before either draft is approved, scheduled, or published. No
FAIL items - nothing required a loop-back to writing/research.
