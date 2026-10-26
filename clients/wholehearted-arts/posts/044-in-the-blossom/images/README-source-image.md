No local image file for this post.

No `chosen_images` mockup exists yet for "In the Blossom" (Studio Collection), and this sandbox's egress to the Squarespace image CDN is blocked (confirmed via a direct `curl` test — 403 at the proxy), so the image could not be downloaded or cropped per-platform with Pillow.

Both platforms use the catalog's `primary_image_url` (flat product photo) passed through to Buffer as a raw external URL — Buffer's own servers fetch it independently of this sandbox:

https://images.squarespace-cdn.com/content/v1/5b412dba5ffd201a3f9205e4/1677272410974-3G258RL7WMIPHEB01KB3/B10AE65C-A461-4E9F-BDA4-322C22BC4278

See `package-review.md` for the NEEDS HUMAN DECISION note on image sizing/mockup selection.
