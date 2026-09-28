# Image sourcing note — 027 His Steadfast Love Embraces

This catalog entry ("His Steadfast Love Embraces", Studio Collection) has
**no `chosen_images` block** — no human or prior Claude session has
visually reviewed its 3 product photos to identify a styled room mockup.
Per this run's instructions, that means:

- **Do not guess** which of the 3 photos (if any) is a room mockup.
- Use **`primary_image_url`** (catalog image index 0, portrait
  orientation, 2120x2500) for all three platforms instead.
- This is flagged as a **NEEDS HUMAN DECISION** item: a human should
  review the entry's 3 photos and set `chosen_images` (mockup_url /
  flat_url / avoid_indexes / note) if a genuine room mockup exists among
  them, so future runs on this entry don't have to fall back this way.

Source image URL used for all three platforms:
```
https://images.squarespace-cdn.com/content/v1/5b412dba5ffd201a3f9205e4/1716645308083-1O7E3LLU1J6K2HUTMH0W/E0BDB703-E2B0-4CB5-A936-FA32BC45E570.jpeg
```

**Download/crop attempt this run:** one Python `urllib.request` attempt
to fetch the above URL failed (`Tunnel connection failed: 403 Forbidden`),
consistent with every prior run's image-CDN egress block since 2026-08-09.
Not retried, per run instructions. No local download, no Pillow crop, no
letterboxing was possible — the raw uncropped source URL is passed
straight through to Buffer for LinkedIn (Idea), Instagram (draft), and
Facebook (Idea) alike. Buffer's own servers fetch the URL independently of
this sandbox, so this is not expected to block staging, but the image is
**not resized to platform dimensions** (LinkedIn 1200x627, Instagram
1080x1350, Facebook 1200x630) and has **not been visually verified** by
this run. A human should confirm the image renders correctly in Buffer's
composer for each platform, and ideally crop it locally to spec before
scheduling.
