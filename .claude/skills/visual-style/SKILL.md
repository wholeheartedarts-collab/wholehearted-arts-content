---
name: visual-style
description: Build or apply a compact JSON visual-style guide that keeps generated post images consistent with the client's brand. Use once to build the guide from reference images, and every time before image-generation to apply it.
---

# Visual Style

## Building the guide (one-time, or when references change)

Input: 3-6 approved reference images (Agata will provide these) plus any
existing brand assets in `clients/[client-slug]/brand-assets/`.

Convert them into a compact JSON style guide capturing:

- Composition and visual hierarchy
- Typography characteristics (if references include text/graphics)
- Color palette and contrast
- Subject placement and cropping
- Illustration/photography treatment
- Whitespace and density
- Recurring brand devices/motifs
- Prohibited visual elements
- Per-platform dimensions and safe areas (see [[image-generation]]) —
  keep a `dimensions` map with one entry per active platform (LinkedIn,
  Instagram, Facebook), not a single LinkedIn-only value

Keep the JSON concise enough for reliable use in an image-generation API
call — if a first pass is too long/detailed, compress it while preserving
the essential identity and hierarchy.

Save as `clients/[client-slug]/visual-style/style-guide.json`.

## Current status for wholehearted-arts

**No reference images yet.** Until they're provided, use this minimal
placeholder so [[image-generation]] has something concrete to work from
rather than nothing:

```json
{
  "status": "placeholder - awaiting reference images",
  "palette": "warm, natural tones; avoid cold corporate blue/gray defaults",
  "mood": "creative, energetic, personal - not stock-photo corporate",
  "composition": "clear single focal point, generous negative space",
  "typography": "minimal to none - prefer imagery over text-heavy graphics",
  "prohibited": ["generic AI-art clichés (extra fingers, warped text)", "stock-photo handshake/boardroom imagery", "overtly religious iconography unless explicitly requested"],
  "dimensions": {
    "linkedin": {"single_image": "1200x627", "square": "1200x1200"},
    "instagram_feed": "1080x1350",
    "facebook": "1200x630"
  }
}
```

Replace this entirely once real references are analyzed — do not treat
the placeholder as a real brand system, and flag its use in
`review.md` whenever an image is generated against it.

Live copy of this placeholder lives at
`clients/[client-slug]/visual-style/style-guide.json` — update both if
either changes (SKILL.md is the documented default, the JSON file is
what [[image-generation]] actually reads).

## Applying the guide

Before calling [[image-generation]], load
`clients/[client-slug]/visual-style/style-guide.json` and pass it as the
guiding style reference. It guides new, original, content-relevant
images — never instructs copying a reference image directly.

## Testing rule

When the guide changes, regenerate a test image rather than editing an
old one in place — save as a new numbered version so results are
comparable. Never silently overwrite a prior version.
