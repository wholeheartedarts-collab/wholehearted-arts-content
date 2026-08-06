# Review: 002-art-that-moves-people-to-tears-or-joy

## LinkedIn platform review

| Checklist item | Verdict | Notes |
|---|---|---|
| Hook (~210 char standalone) | PASS | ~145 characters across two short lines ("There's a moment... face changes." / "That's the moment I make art for."). Stands alone, earns curiosity, grounded in the post's actual content — not clickbait. |
| Formatting | PASS | Short paragraphs (2-4 lines), generous white space, scannable. |
| Voice | PASS | Checked against `brand-voice.md` — warm, personal, sensory ("mirror, fabric," "shifts as the light... shifts"), first person. No AI-slop phrases found (no "game-changing," "unlock," "thrilled to announce," etc.). |
| Audience clarity | PASS | Clearly Art-pillar / art-collector audience. Does not attempt to bridge to the AI-automation pillar — correct per brief.md. |
| Length | PASS | Proportionate to the topic; earns the "see more" click without padding. |
| CTA | PASS | Soft CTA (invite comments, point to the collection page) — matches the client's default soft-CTA policy since no specific CTAs are approved yet. |
| Hashtags/mentions | PASS | 3 minimal, directly relevant tags (#ChristianArt #MixedMediaArt #OriginalArtwork). No forced or unrelated tags. |
| No politics / avoid-list | PASS | No political content. No generic AI-hype language. |
| No AI-slop phrasing | PASS | Confirmed against brand-voice.md "Avoid" list. |

**Overall: PASS — no revision needed.**

## Fact-check

Claims checked against `research.md` / `sources.md`:

| Claim in draft | Status | Note |
|---|---|---|
| "Fear Not" is a 36×36 inch mixed media painting (mirror, fabric, acrylic, paper) | SOURCED | Matches Agata's own product page verbatim on materials/size. |
| Isaiah 54 words are woven into the painting, in small shapes across the background | SOURCED | Matches product page description directly. |
| Mirror fragments make the piece shift as light changes in the room | SOURCED | Paraphrase of Agata's own description ("shifts as light moves across it... full of reflection, depth, and holy interruption"). |
| "Built to feel less like decoration and more like an interruption — the kind that's holy, not startling" | SOURCED | Direct paraphrase of Agata's own stated intent for the piece, from her product page — not an invented claim about her intent. |
| Researchers describe being "moved" (to tears/joy) as involving low personal causation/control and a "witness" stance | SOURCED | Menninghaus et al. 2015, PLoS ONE — matches the study's appraisal-pattern findings. |
| That witness stance is "part of what seems to make it feel safe enough to let happen at all" | SOURCED (softened) | Traces to the study's link between witness stance/control and emotional safety in art contexts. Phrased with "seems to" — not stated as settled clinical fact, per research.md's risk note against overclaiming therapeutic effect. |
| Sadness and joy showing up "tangled together" | SOURCED | Matches the study's "mixed affect" finding for episodes of being moved. |
| Artist's own hope/feeling while making the piece ("I think about that possible moment the whole time I'm layering") | GENERAL STATEMENT — APPROVED FRAMING | Not a specific incident or third-party story. This is exactly the "speak generally, no fabricated specific incident" framing Agata approved (see brief.md) — an artist's own stated general intent, not a verifiable external fact requiring a source. |
| No claim that any specific person cried or reacted to this or any piece | CONFIRMED ABSENT | Per Agata's explicit instruction — checked and confirmed the draft contains no invented incident, quote, or third-party reaction. |

**No UNSUPPORTED claims found.** Nothing requires removal or human
confirmation beyond what's already flagged as human-approved framing
above.

### Correction (post-review, human-flagged)

The original draft called "Fear Not" Agata's "newest work" — this was an
**unverified claim I introduced without checking**, not something from
research.md or the product page. Agata corrected it on 2026-08-05: the
painting was made a few years ago, not recently. Fixed in
`linkedin-post.md`: "My newest work" → "One piece... a painting I made a
few years ago," and the closing "the whole time I'm layering" (implying
present-tense creation of this specific piece) was generalized to "I
think about... whenever I'm layering a new piece" (a general statement
about her ongoing practice, not this specific painting). This is a
process gap worth noting: [[factual-verification]] should treat
unqualified recency/timing claims ("newest," "latest," "just finished")
about a specific named work as needing explicit confirmation, the same
as any other specific factual claim, before they're written into a
draft.

## Content package review (final gate)

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal match brief | PASS | Matches brief.md exactly — Art pillar, art-collector audience, general (non-incident) framing as Agata specified. |
| Every factual claim supported | PASS | Pulled directly from the Fact-check table above; no unsupported claims. |
| Balanced treatment of real risks/limitations | PASS | Post avoids implying guaranteed emotional reaction or clinical/therapeutic claims, per research.md's risk notes — uses "seems to," "the hope that," not certainty language. |
| No fabricated facts, quotes, personal experiences, results | PASS | Confirmed in fact-check — no invented incident or third-party story. |
| Client voice / avoid-list (no politics, no AI-slop) | PASS | Confirmed against brand-voice.md and linkedin-review above. |
| Platform-native structure met | PASS | Pulled from LinkedIn platform review above — PASS. |
| Hook strength/readability | PASS | See platform review. |
| Image relevant, consistent, correctly sized | PASS — see note | Image is a **real photograph of Agata's own painting** ("Fear Not"), not an AI-generated image — a deliberate, explicit deviation from the default [[image-generation]] skill per Agata's direct request to use one of her actual paintings. Not evaluated against `style-guide.json` for that reason (style guide governs generated images; not applicable to a real product photo the client chose herself). It's a staged room-mockup photo (brick-loft living room) from Agata's own site, chosen by her from a set of options. Dimensions: 1500×1068 — close to but not an exact match for LinkedIn's suggested 1200×627 crop; LinkedIn auto-fits on upload, so this is not a blocker, just noted for awareness. |
| Alt text accurate | PASS | Matches the actual final image (verified against the same photo before writing alt-text.md). |
| Tags/mentions appropriate | PASS | 3 minimal relevant hashtags, no @mentions, no third-party tagging. |
| Compliance constraints respected | PASS | No professional/medical/legal claims; no AI-automation claims (not applicable to this post). |
| No secrets/API keys/private info in package | PASS | Checked all files in this folder — none present. |

**Overall verdict: PASS.** No FAIL items. No items require a human
decision beyond what Agata has already decided (painting choice, image
choice, general-framing choice) — flagging the image-sourcing deviation
above for transparency, not because it needs a further decision.

### Known provisional elements (informational, not blockers)

- `brand-voice.md` is still provisional (no real writing samples yet) —
  standard known state per [[brand-voice]], scheduled to be replaced
  after the first 3 published posts.
- `visual-style/style-guide.json` remains an unused placeholder for this
  post specifically, since no AI image was generated.
