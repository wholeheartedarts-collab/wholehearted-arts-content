# Source image — 026 Awakened Fields

Per CLAUDE.md run instructions: this catalog entry HAS a `chosen_images`
block (verified 2026-09-01 by a human/Claude actually viewing every photo
in the listing), so the mockup photo is used for all three platforms
rather than generating a new image.

- **mockup_index:** 0
- **mockup_url:** https://images.squarespace-cdn.com/content/v1/5b412dba5ffd201a3f9205e4/1677295694660-LC8AN3FV2TZ7TCEU25P8/6F637985-B34A-499B-B732-D353A278A46A
- **catalog note:** "idx 0 is already a warm living-room mockup; idx 1 is
  the flat framed shot. idx 4 is a close-up of the paint surface."
- **avoid_indexes:** none listed for this entry.
- **seasonal warning:** none — no seasonal styling flagged in the note.

## Download/crop attempt

Attempted to download the mockup image with Python (`urllib`) to crop it
to each platform's dimensions with Pillow (LinkedIn 1200x627, Instagram
1080x1350, Facebook 1200x630). The request failed:

```
URLError: <urlopen error Tunnel connection failed: 403 Forbidden>
```

Per run instructions, this was **not retried** — the sandbox's egress
policy blocks `images.squarespace-cdn.com`, and this is documented as an
expected, non-fatal outcome, not a run failure.

## Fallback used

The raw, uncropped `mockup_url` above was passed directly to Buffer for
all three platforms (LinkedIn idea, Instagram draft, Facebook idea).
Buffer's own servers fetch the image independently of this sandbox, so
this does not block staging. **No cropping to platform-specific
dimensions was performed this run** — a human should confirm the image
displays acceptably in Buffer's composer per platform, or fetch/crop it
locally before scheduling, per the run's Step 13 email.

Alt text (see `../alt-text/`) was written from the catalog's
`description`, `chosen_images.note` (confirms this is a genuine
living-room mockup, not a flat product shot), and the listing's own
`alt_from_site` if present — not from direct visual inspection, since the
image could not be downloaded this run.
