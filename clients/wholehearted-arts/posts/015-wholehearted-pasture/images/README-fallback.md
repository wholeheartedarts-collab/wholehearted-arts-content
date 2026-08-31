# Image fallback note — "Wholehearted Pasture"

The source image could not be downloaded this run:

```
curl https://images.squarespace-cdn.com/content/v1/5b412dba5ffd201a3f9205e4/1680747884654-50WSR14DD9XC90CEFO5X/86452606-61A1-470A-88AD-233F2BB32783
→ curl: (56) CONNECT tunnel failed, response 403
```

Per the run instructions, this is not treated as a run failure. The raw
public `image_url` was passed directly wherever an image URL was needed
(Buffer's Instagram draft and the LinkedIn/Facebook ideas) — Buffer's own
servers fetch the image independently of this sandbox, so it should attach
correctly there even though this run couldn't fetch/crop it locally.

**Consequence:** no platform-sized crops exist in this folder
(LinkedIn 1200x627 / Instagram 1080x1350 / Facebook 1200x630) — all three
platforms reference the same uncropped source image via its public URL.
This is a NEEDS HUMAN DECISION item — see package-review.md.

Image URL used for all three platforms:
https://images.squarespace-cdn.com/content/v1/5b412dba5ffd201a3f9205e4/1680747884654-50WSR14DD9XC90CEFO5X/86452606-61A1-470A-88AD-233F2BB32783
