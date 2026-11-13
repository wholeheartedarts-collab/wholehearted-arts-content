# Image — 052 "After the Rain, the Windows Kept Glowing"

## Source

Real photo of the actual painting (not AI-generated), per the
established, human-directed convention for this client (real product
photos of Agata's own paintings, consistent with post 002 onward).

- **No `chosen_images` mockup exists** for this catalog entry — the
  mockup-curation pass only covered Atelier's unused list as of
  2026-09-01; Studio's unused list (including this entry) hasn't been
  reached yet. Per the run's rules, falling back to `primary_image_url`
  (a flat photo of the painting) rather than guessing whether either of
  the 2 listed images is a styled room shot. **Flagging for a human to
  curate `chosen_images` for this entry in a future catalog refresh** —
  noted in the Step 13 email.
- Chosen image URL (same URL for both platforms, since no mockup/flat
  distinction exists — this is simply the one primary product photo):
  `https://images.squarespace-cdn.com/content/v1/5b412dba5ffd201a3f9205e4/1783036852821-WCQ53BEAHO759Z0KQ3BC/02567E0C-0C60-4746-94ED-A839E314B133.jpeg`

## Egress / download attempt

One test download via `curl` to `images.squarespace-cdn.com` was
attempted and failed: the sandbox's egress proxy rejected the
connection (`connect_rejected` — host not allowed for this session).
Per CLAUDE.md's egress note, this was not retried.

**Result: no local crop was produced.** The chosen image URL is passed
straight through to Buffer at `create_post` time (per the routine's
Step 7-9 instructions) — Buffer's own servers fetch the image
independently of this sandbox, so this does not block staging the
drafts. No LinkedIn 1200x627 / Instagram 1080x1350 crop exists locally;
both platform posts will use the original image as Squarespace serves
it. This is noted here, in the package-review, and in the Step 13 email
so a human knows to check the crop looks right once the draft is live
in Buffer, and can add a locally-cropped version later if needed.

## Alt text basis

Because the image could not be downloaded/viewed in this sandbox, alt
text (see `../alt-text/linkedin.md` and `../alt-text/instagram.md`) is
based on the catalog's own product description and is explicitly
flagged as not visually verified, per [[accessibility-alt-text]] and
this run's Step 7-9 instructions.
