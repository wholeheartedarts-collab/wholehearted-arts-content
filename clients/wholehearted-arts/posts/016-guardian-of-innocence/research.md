# Research Brief: "Guardian of Innocence" (Atelier Collection)

**Run type:** Automated scheduled pipeline run, 2026-09-02.
**Selection rule applied:** Per `painting-catalog.json`'s `_selection_rule`, pick
from the collection with fewer entries in `used`; if tied, pick from whichever
collection was NOT used for the most recent post number. Catalog snapshot shows
Atelier=7 used, Studio=7 used — a tie. Post 015 ("Wholehearted Pasture") used
Studio, so the tiebreaker points to Atelier this run.
**Painting/product details source:** `clients/wholehearted-arts/painting-catalog.json`,
live Squarespace Commerce API data (entry `modified_on` 2026-08-30). No
`caution_note`, `price_note`, or `availability_note` on this entry — price
($1,200) and availability (1 in stock) are clean.
**Egress note:** Not re-tested this run — post 015's run confirmed
`www.wholeheartedarts.com` and the image CDN are both blocked, and instructions
say don't retry. All painting facts below come from the catalog.

## Executive summary

"Guardian of Innocence" is a 20x20" original mixed-media (textile/acrylic on
canvas) piece from Agata May'kowska's Atelier Collection, priced at $1,200,
one in stock. The catalog's own site description depicts a mother resting
with her child, eyes closed "not in weariness, but in trust," built from
"fragments of color and texture" that come together "like a life shaped
through both breaking and beauty." The piece's own language centers on
protective, non-controlling love — "guardianship without fear" — which maps
directly onto WholeheartedArts' faith/family/healing content pillars without
needing an invented backstory.

## Key points

- Medium and size, per the catalog: original mixed media on canvas, 20 x 20
  inches.
- The site's own description (used verbatim as the primary source for any
  claim about the piece's meaning) frames the subject as a mother and child,
  emphasizes trust over vigilance, and describes the surrounding abstract
  texture as "a life shaped through both breaking and beauty — nothing
  wasted, everything held."
- The description explicitly distinguishes this piece's idea of guardianship
  from controlling or fearful protection: "protection without fear, of love
  that does not control, but covers."
- No scripture citation is embedded in this piece's own product description
  (unlike, e.g., "Love Eternal Rhapsody," which explicitly names Colossians
  3). Any scripture referenced in the social copy must be framed as a
  resonance a writer/viewer might draw, not as a quotation Agata herself
  built into the work — do not claim the painting "is based on" or
  "references" a specific verse.

## Notable statistics

None applicable — this is a product/art topic, not a stats-driven topic.

## Specific examples

- The painting itself is the example; no external case studies apply.

## Risks, counterarguments, or limitations

- Thin narrative risk: beyond the site's own description, there is no
  additional artist statement, backstory, or process note available for this
  piece. Per the orchestrator's and skip_rules' guidance for thin-narrative
  pieces, keep post copy shorter and more image-led rather than inventing
  personal story, studio process, or a "why I painted this" narrative that
  isn't in the source description.
- Do not claim a specific scripture is depicted in or inspired the painting,
  since the source description does not name one. It is safe to draw a
  resonant connection (e.g., "the kind of care Isaiah 40:11 describes") as
  the writer's own reflection, clearly framed as such, not as fact about the
  artwork's origin.
- Price ($1,200) and one-in-stock status should be treated as a live
  commercial fact, current as of the catalog's 2026-08-30 snapshot — normal
  caveat that stock can change between snapshot and publish.

## Possible content angles

1. **Protective, non-anxious love** — the piece's own line "protection
   without fear... love that does not control, but covers" as the entire
   angle; invites reflection on parents, caregivers, or anyone holding
   something fragile.
2. **Rest as trust, not exhaustion** — the mother's closed eyes "not in
   weariness, but in trust" as a short meditation on faith-postured rest.
3. **Wholeness made of fragments** — "a life shaped through both breaking
   and beauty — nothing wasted, everything held" as a broader healing/
   overcoming-struggle angle, less tied to the mother-child image
   specifically, useful if a platform wants a wider audience than parents.
4. **Being held, being covered** — a shorter, more devotional angle
   resonant with (not claiming direct inspiration from) Isaiah 40:11 ("he
   gathers the lambs in his arms and carries them close to his heart") or
   Psalm 91:4 (being covered/sheltered), framed explicitly as the writer's
   own connection, not the artwork's stated source.

Recommended: angle 1 or 4 for LinkedIn/Facebook (broader, reflective);
angle 2 or 3 for Instagram (shorter, image-forward).

## Scripture verification (for optional resonance framing only — not claimed
as the painting's source)

- **Isaiah 40:11 (NIV):** "He tends his flock like a shepherd: He gathers the
  lambs in his arms and carries them close to his heart; he gently leads
  those that have young." Verified via WebSearch against BibleHub, Biblia,
  and Bible.com/NIV listings (direct fetch to biblegateway.com/biblehub.com/
  esv.org is blocked by the egress proxy; search-result snippets from those
  same indexed pages confirm the wording). See sources.md.
- **Psalm 91:4 (ESV):** "He will cover you with his pinions, and under his
  wings you will find refuge; his faithfulness is a shield and buckler."
  (NIV renders "pinions" as "feathers" — same meaning, different word
  choice; use whichever translation is quoted consistently if used at all.)
  Verified via WebSearch against Biblia (ESV) and BibleHub/NIV listings. See
  sources.md.

## Research notes

- Everything under "Key points" is sourced directly from the catalog's own
  `description` field (itself pulled live from the Squarespace product
  listing) — not inference.
- The content angles are the writer's synthesis of that description against
  the client's stated content pillars (faith, emotion, healing, family,
  overcoming struggles) — clearly separated here from the sourced facts
  above.
- No claim in this brief asserts a real quote, statistic, or personal story
  beyond what the product description states. If either scripture verse is
  used in copy, it must be attributed as a translator's-text quotation
  (with version named) and framed as the writer's own resonance, not as fact
  about the painting.
