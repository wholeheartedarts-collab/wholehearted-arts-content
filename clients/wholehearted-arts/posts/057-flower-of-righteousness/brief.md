# Brief: "Flower of Righteousness" (Studio Collection)

## Run context

Automated scheduled run of the content pipeline, 2026-11-25. Platforms:
LinkedIn + Instagram only (per CLAUDE.md's current scope and this run's
explicit instructions). No Facebook post produced or staged.

## Painting selection & collection reasoning (for the record)

Per `_selection_rule` in `painting-catalog.json`: pick from the collection
with fewer entries in its `used` list; if tied, pick from whichever
collection was NOT used for the most recent post number.

- Catalog's raw `used_count` is tied (Atelier 7 / Studio 7) — stale, as
  established across posts 039-056.
- Reconciled Atelier's `unused` list (11 nominal entries) against actual
  post folders directly: **every title except "Let Our Light Continue to
  Shine" already has a post folder** (008, 016, 018, 020, 022, 024, 026,
  028, 032, 034, 036). The one remaining title is an explicit prayer for
  peace in Israel/the Jewish people, judged politically-adjacent and
  excluded by posts 039-056 under the client's no-politics avoid-list.
- This makes Atelier **genuinely exhausted of non-flagged candidates for
  the 20th consecutive run (039-057)**. Per `skip_rules`, the hard-stop
  ("both collections exhausted — stop and report") does not apply, since
  Studio still has real unused inventory. Falling back to **Studio
  Collection** again, consistent with posts 039-056.
- **This pattern is escalated as a standing NEEDS HUMAN DECISION** — see
  package-review.md and the Step 13 email. A human should either confirm
  "Let Our Light Continue to Shine" is permanently excluded (and have the
  catalog's `_selection_rule`/`skip_rules` updated to reflect that Atelier
  is a closed collection until new art is added), or make the call to
  include it with a political-sensitivity-aware treatment.

## Reconciling Studio's "unused" list

Catalog's Studio `unused` list is also stale (same pattern as Atelier).
Cross-checked against existing post folders 002-056: most of Studio's
nominal "unused" list is already used. Genuinely unused, non-flagged,
non-product-listing candidates found: All the Love We Need, Can You See
Me?, Deep Blue Love, Disassembled Grace, Floral Symphony, **Flower of
Righteousness**, Heart Filled with Sunrise, I Am Still Standing, Imagine,
Inner Wisdom, Life, Modern Man #1, Moonlight Delight, Moonlight Serenade,
Mother, Peace is Her Power, Prayerful Rose or Jeremiah, Quiet Abundance,
Quiet Company, Red, Snowy Bond, Tell Me Your Story, The Color of Waiting,
The Language Beneath the Noise, Village, What the Body Remembers, Woman.

Excluded from consideration:
- **Eyes of Fear - War**, **President Trump Portrait - customized!** —
  political/war-adjacent, excluded under the no-politics avoid-list even
  without an explicit `caution_note`.
- **Leaving the Matrix**, **Gaslighted**, **Reckoning** — thematically
  heavy/ambiguous titles with no catalog description context available in
  the unused-list query; left for a future run with fuller review rather
  than guessing a safe treatment blind.
- **Where the Walls Remember** — explicit `caution_note`: NEEDS HUMAN
  DECISION, Holocaust/Auschwitz memorial piece — skipped per skip_rules.
- **The Key Within** — `caution_note` flags it as thematically paired
  with the above; left alone this run since a genuinely clean candidate
  was available.
- **Sisters** — `caution_note`: Agata already posted about this piece
  organically; skippable since better options exist.
- **Tell Me Your Story**, **The Language Beneath the Noise** —
  `is_visible: False` in the catalog (not a live/published listing on the
  site) — excluded to avoid promoting content that isn't actually public.
- Non-painting product listings (Christmas Cards, Happy Hanukkah,
  International Shipping Deposit, Roses Blooms - Tissue Box Holder) —
  not actual artworks, excluded.

## Selected: "Flower of Righteousness" (Studio Collection)

- SKU: SQ0507999
- Price: $125.00 USD — **SOLD OUT / 0 in stock** (`availability_note`:
  "Shows zero stock — likely already sold. Do not imply it is purchasable
  without checking.") — post will not claim it's for sale.
- Scripture tie-in: Philippians 1:9-11, written as a prayer (per catalog
  description).
- Catalog description includes Agata's own first-person reflection on how
  she perceives the world (small particles/fragments moving and holding
  together in a dance) — this is a real, sourced piece of personal
  narrative from the catalog itself, not invented. The post may draw on
  it directly but must not extend or embellish beyond what's written.
- `chosen_images`: **not set** for this entry (no human has reviewed its
  photos to pick a room mockup). Per the run instructions, will use
  `primary_image_url` for both platforms and flag plainly that no mockup
  was selected — this is NOT being asserted as a room scene.
- Fits content pillar: faith / emotion / "how I see the world" process
  reflection — genuinely bridges the art-collector audience with a
  faith-forward angle. No automation/business pillar relevance; this
  topic targets the **art collectors** audience only.

## Platforms

LinkedIn + Instagram. No Facebook (Instagram cross-posts automatically).
