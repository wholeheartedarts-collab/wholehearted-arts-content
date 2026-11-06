# Image — "The Center Holds"

No local image file in this folder. Egress to the Squarespace image CDN
(`images.squarespace-cdn.com`) is blocked in this sandbox — confirmed
with a single attempt per the run's egress-note instruction (curl
returned `CONNECT tunnel failed, response 403`); not retried.

**Chosen image (passed straight through to Buffer as a public URL):**
`primary_image_url` —
https://images.squarespace-cdn.com/content/v1/5b412dba5ffd201a3f9205e4/1782834496512-34VULQENUQHBNY89FIJR/BD8F4DA8-37B6-4090-A28A-FAF3D8247AD6.jpeg

This entry has **no `chosen_images` field** in painting-catalog.json — no
human has viewed its 4 listing photos to identify a styled room mockup.
Per the run instructions, `primary_image_url` (a flat product shot of the
painting) was used instead of guessing which photo might be a mockup, and
this is flagged as a NEEDS HUMAN DECISION item: a human (or a future run
that can actually view the photos) should check the listing's other 3
images for a room mockup and add a `chosen_images` entry for this
painting in the catalog.

No local crop was produced (LinkedIn 1200x627 / Instagram 1080x1350 with
sampled-background letterboxing, per the run's Pillow step) because the
file could not be downloaded in this sandbox. Buffer's own servers fetch
the image independently from this sandbox's egress restrictions, so the
same public URL was attached directly to both Buffer drafts, uncropped.
