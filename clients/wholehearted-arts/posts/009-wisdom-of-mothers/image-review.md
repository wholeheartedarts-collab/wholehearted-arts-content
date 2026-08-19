# Image sourcing — 009-wisdom-of-mothers

## Source

Real product photo of the painting "Wisdom of Mothers" (Atelier
Collection) — NOT an AI-generated image. Sourced per CLAUDE.md's option
to use a real photo of the client's own artwork instead of generating
one (same as post 002's "Fear Not," per [[image-generation]] skill
guidance).

**Image URL (from `painting-catalog.json`):**
`http://static1.squarespace.com/static/5b412dba5ffd201a3f9205e4/69da327c2622e42cafbe8437/64025abb16b07c295c606e65/1716639367991/3F36E489-3B49-421E-8347-AAA6614A068D?format=1500w`

## Download attempt — FAILED (egress blocked)

Attempted `curl` download this run:

```
curl -sS -o images/source-original.jpg "http://static1.squarespace.com/..."
```

Result: HTTP 403, response body: `Host not in allowlist:
static1.squarespace.com. Add this host to your network egress settings
to allow access.` A follow-up attempt over HTTPS also failed at the
CONNECT tunnel stage (403).

This confirms the image CDN host (`static1.squarespace.com`) is blocked
by the same sandbox egress policy as `www.wholeheartedarts.com` itself —
this was previously untested/unknown per the runbook, now confirmed
blocked as of 2026-08-19.

## Fallback used

Per CLAUDE.md Step 7-9 fallback instructions: since local download and
Pillow-based cropping/letterboxing is not possible this run, **no local
per-platform image files were produced** (no `linkedin-v1`,
`instagram-v1`, or `facebook-v1` PNG/JPG in `images/`). Instead, the raw
`image_url` above will be passed directly wherever a public image URL is
needed:

- **Buffer (Instagram draft, Step 11):** the raw URL is attached directly
  to the `create_post` call — this is explicitly fine per the runbook,
  since Buffer's own servers fetch the image independently of this
  sandbox's egress restrictions.
- **LinkedIn / Facebook:** not pushed to Buffer this run at all (see
  `status.json` and the final summary) — no image file is needed for
  those platforms this run since they're left at `review-ready` for
  Agata to handle manually. If/when Agata publishes those manually, she
  can pull the same real photo directly from the live product page
  herself.

## Consequence for platform-specific sizing

No platform-specific crop/letterbox was applied (LinkedIn 1200x627,
Instagram 1080x1350 portrait, Facebook 1200x630, per
`visual-style/style-guide.json`). The same single raw source image is
used everywhere this run rather than three distinct optimized crops.
This is a known deviation from the normal pipeline (see posts 003/004
for the normal cropped-per-platform pattern) — flagged here and in the
final run summary. Not a blocker for the Instagram Buffer draft (Buffer
will scale/display the image as uploaded), but a human should apply
proper per-platform cropping before final publish if image quality/crop
matters for the LinkedIn and Facebook posts.

## No caution flags on this catalog entry

Unlike some other catalog entries, "Wisdom of Mothers" carries no
`availability_note` or `price_note` — no additional flag needed for
Agata beyond the general catalog-staleness caveat already noted in
research.md.
