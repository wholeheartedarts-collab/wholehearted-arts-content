# Source image — 028 "Messenger"

**Chosen image:** `chosen_images.mockup_url` (index 1) from the catalog
entry — a human/Claude-verified room mockup, per the entry's own note:
"idx 1 (teal wall, plant, warm light) is the cleanest. No pure flat shot
exists in the set. AVOID idx 6/7 — split/duplicated framing."

URL:
https://images.squarespace-cdn.com/content/v1/5b412dba5ffd201a3f9205e4/1679062008337-XALQPJ8H7BFCDR80ONQD/6DBA1855-96FE-49A6-A0B1-16146AF8AC44

Same image used for all three platforms (LinkedIn, Instagram, Facebook)
— no seasonal warning on this entry's `chosen_images.note`, and no
`avoid_indexes` conflict with index 1.

## Download attempt

One Python `urllib` download attempt this run:
`Tunnel connection failed: 403 Forbidden` — egress to
`images.squarespace-cdn.com` is blocked by this sandbox, consistent with
prior runs (posts 026/027). Per run instructions, this was **not**
retried.

## Fallback (per run instructions — not a run failure)

- No local crop/letterbox was produced for any platform this run.
- The raw `mockup_url` above was passed straight through to Buffer
  (create_post for Instagram, create_idea for LinkedIn/Facebook) — see
  `status.json`. Buffer's own servers fetch the image independently of
  this sandbox.
- A human should confirm the image renders correctly in Buffer's
  composer per platform (uncropped — native aspect ratio, not resized to
  LinkedIn 1200x627 / Instagram 1080x1350 / Facebook 1200x630) before
  approving/scheduling, or crop it locally first.
