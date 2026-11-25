# Image note — "Flower of Righteousness"

No `chosen_images` field exists on this catalog entry (no human has
reviewed its photos to pick a room mockup). Per the run instructions,
using `primary_image_url` for both LinkedIn and Instagram — this is a
flat/square product photo of the painting itself, **not** a room scene.
Do not describe it as one anywhere in the package.

Image URL used for both platforms:
https://images.squarespace-cdn.com/content/v1/5b412dba5ffd201a3f9205e4/1677687587084-GMQ4T1IK2D36BYQ56GUL/674D40D2-9150-4188-9B49-C9A15C080468
(2411x2500, square-ish/portrait-leaning, SKU SQ0507999)

Download attempted once (`curl` to images.squarespace-cdn.com) — failed
with a proxy CONNECT tunnel 403, consistent with the egress policy
described in the run instructions. Not retried. No local crop was
produced; the raw URL is passed directly to Buffer's `create_post` for
both platforms (Buffer's own servers fetch the image independently of
this sandbox). Both platforms therefore use the **uncropped** native
image rather than a LinkedIn 1200x627 / Instagram 1080x1350 letterboxed
crop.

**NEEDS HUMAN DECISION:** no mockup selected for this painting — a human
reviewing its actual photos could add a `chosen_images` entry to the
catalog (flat vs. mockup, which index) for future runs.
