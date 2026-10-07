# Research Brief: "Heaven Declares" (Atelier Collection)

## Source painting (from painting-catalog.json, Atelier Collection, unused list)

- **Title:** Heaven Declares
- **Artist:** Agata May'kowska
- **Collection:** Atelier Collection
- **Size:** 40" x 30", presented in a silver frame
- **Price:** $2,800.00 USD — no `price_note` flag on this entry.
- **Availability:** No `availability_note` flag — appears purchasable as of the catalog snapshot; verify before implying it's in stock if this post runs long after the snapshot date.
- **Materials:** Mixed media — fabric, paper, and acrylic on canvas.
- **Caution note (from catalog):** "Also based on Psalm 19, same as topic 004 (Psalm of the Birch Forest). Angle is different (Scripture-fragment figure vs. birch trunks), so still usable, but a writer should differentiate the framing clearly from 004 rather than repeating the same scripture-quote-and-angle." This is a usability note, not a "NEEDS HUMAN DECISION" flag per `skip_rules`, so the entry is eligible — see "Differentiation from post 004" below for how this draft honors it.
- **Selected image:** This entry HAS `chosen_images` (verified by Claude Code, 2026-09-01 — every image in the listing was actually viewed, not inferred). `mockup_index: 2` ("white brick, bright daylight — carries the blues best"), `mockup_url` set, `flat_index: 0`/`flat_url` also set. No seasonal warning on this entry. Per run instructions, using `mockup_url` for both platforms.
- **Product URL:** https://www.wholeheartedarts.com/atelier-collection-christian-abstract-art/p/110serjwdear3vzksh25lftl8um5xc

## Selection rule reasoning

Per `_selection_rule`: pick from the collection with fewer entries in its `used` list; if tied, pick from whichever collection was NOT used for the most recent post number.

Reconciling actual usage across post folders (catalog's own `used_count` fields are stale — Atelier 7, Studio 7 — and stopped being updated after post 015, consistent with prior runs' notes):

- Through post 034: **Atelier 17 used** (002, 003, 004, 007, 009, 011, 014, 016, 018, 020, 022, 024, 026, 028, 032, 033, 034), **Studio 16 used**.
- Post 035 (most recent prior run) used **Studio** ("Where Grace Settles") — bringing Studio to **17**.
- That makes Atelier (17) and Studio (17) **tied**. Tiebreak: the most recent post (035) used Studio, so this run picks the collection **not** used most recently — **Atelier**.

Within Atelier's genuinely-unused, non-flagged candidates (cross-checking the catalog's stale `unused` list against actual post history — most of that list's 11 titles are already used in practice, e.g. Awakened Fields=026, Gathered Light=024, Guardian of Innocence=016, Love Eternal Rhapsody=022, Messenger=028, Never Stop Wonder=034, Patience=018, The Strength of Three Strands=020, Whimsical Gdansk=032), only **two titles remain genuinely untouched**:

1. **"Let Our Light Continue to Shine"** — excluded this run. Its own description states it is explicitly "my heartfelt prayer for peace in #Israel and for all Jewish people worldwide," built around Hanukkah blessings (Hebrew text/transliteration for three blessings). This borders the client's explicit no-politics avoid-list item (a stated prayer regarding Israel) and is non-Christian-holiday subject matter that doesn't fit the confirmed content pillars (faith/prayer/healing in the Christian register this client has defined). It also carries an `availability_note` ("zero stock — likely already sold") and a `price_note` ("ON SALE at time of snapshot"), reinforcing it's not a clean pick. Consistent with how post 034's run set this same title aside.
2. **"Heaven Declares"** — chosen. No caution about politics/sensitivity, no stock/price flags, rich verified description, and a `chosen_images` mockup already confirmed by a human/Claude viewing session.

## Differentiation from post 004 ("Psalm of the Birch Forest")

Both paintings cite Psalm 19, so this draft deliberately takes the *other half* of the psalm and a different visual/theological hook than 004 used:

- **Post 004's angle:** Psalm 19:1-4 — creation's *wordless* testimony (literal words inscribed into birch bark; "they have no speech... yet their voice goes out").
- **This post's angle:** Psalm 19:7-11 and 19:14 — the *second half* of the psalm, about the perfection and sweetness of God's own *spoken/written Word*, paired with the painting's own description of a worship scene: a human figure built from fragments of Scripture, raised in surrender, with intentionally rough/torn paper and fabric standing in for human imperfection — "perfectly imperfect," offered and made whole in worship. The throughline here is personal and interior (a person's brokenness lifted in worship), not 004's exterior/nature register (trees silently witnessing). Different verses, different visual subject (a figure vs. tree trunks), different theological beat (God's Word refining the heart vs. creation's silent praise).

## Executive summary

"Heaven Declares" is a 40"x30" mixed-media Atelier piece — fabric, paper, and acrylic layered into a lifted human figure built from fragments of Scripture, inspired by Psalm 19. Agata's own listing copy frames the piece around worship as the place where fragmentation is offered and made whole: "what is fragmented is offered, what is unfinished is lifted, and in the presence of God, the heart is made whole." The content angle is "worship as the place brokenness is offered, not hidden" — grounded in the artist's own words, Psalm 19's second half (the sweetness and refining power of God's Word), and 2 Corinthians 4:7's "treasure in jars of clay," rather than any invented personal story.

## Key points

- **Painting narrative (verified, Agata's own site copy, from painting-catalog.json):**
  > "Heaven Declares is an original mixed media painting inspired by Psalm 19 and the deeply personal way God's truth brings salvation to the heart. Built in layers of fabric, paper, and acrylic on canvas, the piece carries both movement and reverence—like praise rising, like heaven still speaking.
  > At the center is a lifted figure formed from fragments of Scripture, surrounded by color, light, and texture that suggest both surrender and joy. The paper and fabric layers are intentionally left somewhat rough in places. That rawness matters. It speaks to the truth that we are created beautifully, yet we move through this life marked by weakness, process, and imperfection. We are, in many ways, perfectly imperfect. And yet in worship, something holy happens—what is fragmented is offered, what is unfinished is lifted, and in the presence of God, the heart is made whole.
  > The composition holds that beautiful tension Psalm 19 carries so well: the vast glory of God revealed in creation, and the intimate mercy of God revealed in His Word.
  > Measuring 40" x 30" and presented in a silver frame, Heaven Declares is a statement piece with spiritual depth—created for a home that makes room for beauty, meaning, and the presence of what is eternal."
- **Scripture — Psalm 19:7-11 (NIV, verified via web search of authoritative Bible reference sites, since direct fetches to biblegateway.com/biblehub.com/esv.org are blocked in this sandbox):**
  > "The law of the LORD is perfect, refreshing the soul. The statutes of the LORD are trustworthy, making wise the simple. The precepts of the LORD are right, giving joy to the heart. The commands of the LORD are radiant, giving light to the eyes. The fear of the LORD is pure, enduring forever. The decrees of the LORD are firm, and all of them are righteous. They are more precious than gold, than much pure gold; they are sweeter than honey, than honey from the honeycomb. By them your servant is warned; in keeping them there is great reward." — Psalm 19:7-11, NIV
- **Scripture — Psalm 19:14 (NIV, same verification method):**
  > "May these words of my mouth and this meditation of my heart be pleasing in your sight, LORD, my Rock and my Redeemer." — Psalm 19:14, NIV
- **Scripture — 2 Corinthians 4:7 (ESV, same verification method), supporting the "fragments/rawness" visual motif:**
  > "But we have this treasure in jars of clay, to show that the surpassing power belongs to God and not to us." — 2 Corinthians 4:7, ESV
- **Scripture — Psalm 51:17 (ESV, same verification method), supporting the "offered in worship" motif — used only as a secondary/optional reference, not required in every draft:**
  > "The sacrifices of God are a broken spirit; a broken and contrite heart, O God, you will not despise." — Psalm 51:17, ESV
- The client's confirmed content pillars include "faith, emotion, healing... and overcoming struggles by staying faithful to God" — this painting's "rawness offered in worship, made whole" framing fits squarely within that lane, with no politics risk (purely a faith/art reflection topic).
- Audience: this topic serves the **art collectors** pillar (personal art practice/process/faith), not the AI-automation pillar — no attempt to bridge both.

## Notable statistics

None applicable — this is an art/faith reflection topic, not a data-driven topic. No statistics are fabricated or needed.

## Specific examples

- The painting itself (described above, from the current, real product listing) is the only "example" in play. No third-party testimonials, customer stories, or composites are used or invented.

## Risks, counterarguments, or limitations

- **Overlap risk with post 004** (both cite Psalm 19) — mitigated as described in "Differentiation from post 004" above; writers for linkedin-post.md/instagram-post.md must keep to the second-half-of-Psalm-19 + "fragments made whole" framing, not reuse 004's "silent witness of creation" framing.
- **No personal backstory beyond the site copy** — per skip_rules guidance and this client's no-fabrication rule, no invented anecdote about Agata's own process is added; the post stays with what the painting's own description already supports, which is substantial enough here that the post need not be unusually short/image-led.
- **Availability drifts over time** — the catalog snapshot shows this piece as available with no flags, but stock should be verified by a human before any post implies it's currently purchasable, since Squarespace inventory can change between the snapshot and publish.

## Possible content angles

1. **"Worship is where the fragments get offered"** (chosen) — the painting's own framing: rawness and incompleteness aren't hidden from God, they're what's lifted in worship, and that's where the heart is made whole. Psalm 19:7-11/14 + 2 Corinthians 4:7.
2. God's Word as something that refines rather than restricts — Psalm 19:7-11's "sweeter than honey" language, paired with the painting's literal use of Scripture-fragments forming the central figure.
3. "Perfectly imperfect" as a theological claim, not a self-help platitude — contrasting secular "self-acceptance" framing with the specifically Christian claim that the rough edges are offered *to someone*, not just accepted in isolation.
4. A making-of/process angle on the literal technique (fabric + paper + acrylic, intentionally rough layers) as a metaphor for lived faith — more craft-forward, useful if Instagram wants a more visual/textural hook.
5. (Not used, flagged as overlapping 004 — avoid) Creation's wordless testimony (Psalm 19:1-4) — already 004's angle.

## Source list

- WholeheartedArts product listing for "Heaven Declares" (via `painting-catalog.json`, sourced live from Squarespace Commerce API): https://www.wholeheartedarts.com/atelier-collection-christian-abstract-art/p/110serjwdear3vzksh25lftl8um5xc
- Psalm 19:7-11, NIV — verified via web search against Bible reference aggregators (biblia.com, bible.com) summarizing the NIV text; direct biblegateway.com/biblehub.com/esv.org fetches are blocked in this sandbox. Full citation: Psalm 19:7-11, New International Version.
- Psalm 19:14, NIV — verified the same way. Full citation: Psalm 19:14, New International Version.
- 2 Corinthians 4:7, ESV — verified the same way. Full citation: 2 Corinthians 4:7, English Standard Version.
- Psalm 51:17, ESV — verified the same way. Full citation: Psalm 51:17, English Standard Version.
- Prior post 004 research brief (`clients/wholehearted-arts/posts/004-psalm-of-the-birch-forest/research.md`) — internal source, used only to confirm differentiation, not as an external claim.

## Research notes

- All painting details (title, size, price, materials, description) are sourced facts from `painting-catalog.json`, itself generated from the live Squarespace Commerce API — not inference.
- All scripture text above is sourced (verified via web search snippets, not fetched directly) — none is paraphrased from memory without that check.
- The "two remaining Atelier candidates" reconciliation (this painting vs. "Let Our Light Continue to Shine") is this run's own synthesis from cross-referencing the catalog's stale lists against actual post folder history — flagged clearly as synthesis, not a sourced fact, in the "Selection rule reasoning" section above.
- No claim in this brief asserts a specific personal story from Agata beyond what her own published listing copy says.
