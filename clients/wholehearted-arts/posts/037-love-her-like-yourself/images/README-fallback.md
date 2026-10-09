# Image fallback note — 037 "Love Her Like Yourself"

No `chosen_images` entry exists for this painting in painting-catalog.json,
so per the run instructions, `primary_image_url` was used (the catalog's
index-0 photo, 780x780, square) rather than a human-selected room mockup:

https://images.squarespace-cdn.com/content/v1/5b412dba5ffd201a3f9205e4/1669042148091-7NBNHPSQN67RZ1AU85KQ/77EF05C5-409B-4414-AB9B-40773F229D73

**No mockup was selected for this painting — flagging for a human to add
one** (view the product's photos and set `chosen_images.mockup_url` in the
catalog, the way earlier posts' entries were annotated) if a styled room
shot is preferred for a future repost.

This sandbox's egress to images.squarespace-cdn.com is blocked (tested once
via curl: `CONNECT tunnel failed, response 403`; not retried per run
instructions). The image was NOT downloaded or cropped to platform
dimensions (LinkedIn 1200x627 / Instagram 1080x1350) with Pillow. The
uncropped source URL above was passed directly to Buffer for both
platforms — Buffer's own servers fetch the image independently of this
sandbox, so this is not expected to block staging, but the image will be
Squarespace's native (square, 780x780) crop rather than a platform-correct
crop until a human re-exports it.
