# R016 — Swimwear Design Language Engine
## Self-Verification Protocol

**Canon status:** BLOCKED until production testing
**File pair:** `research/V20_RESEARCH/R016_SWIMWEAR_DESIGN_LANGUAGE_ENGINE.md` (research), `modules/V20/ENGINE_V20_SWIMWEAR_DESIGN_LANGUAGE.md` (engine spec), `gpt-release/manifests/SWIMWEAR_DESIGN_LANGUAGE_MANIFEST.md` (release manifest)
**Scope:** Per-finding compliance evidence, red-flag set, silhouette/construction/fabric-behaviour-specific verification, and test prompts.

---

## 0. How to use this file

For every finding in §16 of the research file, this file defines:
- **(a) Evidence of compliance** — what the final image MUST show.
- **(b) Red flags of failure** — what would tell you the finding is not satisfied.
- **(c) Test prompts** — concrete prompts to run through the production pipeline.

Canon status for the whole R016 module is **BLOCKED** until the production team runs at least **30 test prompts per finding** and the verification checklist passes at ≥ 80% of prompts.

---

## 1. Verification — F-01 to F-20

### F-01 — Silhouette vocabulary outperforms colour-only

- **(a) Compliance:** The frame specifies a *silhouette* (top, bottom, one-piece) with specific type names.
- **(b) Red flags:** "Black bikini" with no silhouette. "Swimsuit" with no silhouette.
- **(c) Test prompts:**
  1. "Asymmetrical one-shoulder bikini top, tie-side high-waist bottom, Eres noir"
  2. "Triangle bikini top, classic brief bottom, Matteau off-white"
  3. NEGATIVE: "Black bikini" — must FAIL F-01.

### F-02 — Construction vocabulary signals design intent

- **(a) Compliance:** At least one construction technique is specified (ruched, gathered, wrap, cutout, asymmetrical, paneled, seamed, bonded, shirred, smocked, pleated, quilted).
- **(b) Red flags:** "Bikini" with no construction.
- **(c) Test prompts:**
  1. "Ruched bikini top with shirred side panels"
  2. NEGATIVE: "Black bikini" — must FAIL F-02.

### F-03 — Fabric behaviour is a premium signal

- **(a) Compliance:** Fabric behaviour is specified (compression, tension, drape, wet_cling, wet_sheen, quick_dry, body_shaping, uv_protective, sheer_when_wet, memory_fabric).
- **(b) Red flags:** "Silk" or "nylon" without specifying behaviour.
- **(c) Test prompts:**
  1. "Wet-sheen silk-blend one-piece with compression zones"
  2. NEGATIVE: "Silk swimsuit" — must FAIL F-03.

### F-04 — Asymmetry reads as design

- **(a) Compliance:** The frame has *some* asymmetry (one-shoulder, off-centre cutout, single ruched side, asymmetric hem, single tie, asymmetric neckline, mixed fabric).
- **(b) Red flags:** Pure symmetry (in a "design" beat).
- **(c) Test prompts:**
  1. "One-shoulder bikini top with cutout, single ruched side"
  2. NEGATIVE: "Symmetric triangle bikini" — must FAIL F-04.

### F-05 — Ruching is body-flattering + premium

- **(a) Compliance:** Ruching is specified (with location: side, centre, all-over, diagonal).
- **(b) Red flags:** "Bikini" with no ruching.
- **(c) Test prompts:**
  1. "Side-ruffled bikini top, compression in the band"
  2. NEGATIVE: "Black bikini" with no ruching — must FAIL F-05.

### F-06 — Gathered swimwear creates movement

- **(a) Compliance:** Gathering is specified (with point: centre_front, side, back).
- **(b) Red flags:** No gathering.
- **(c) Test prompts:**
  1. "Gathered one-piece with gathering at the side"
  2. NEGATIVE: "Bikini" with no gathering — must FAIL F-06.

### F-07 — Wrap swimwear is a desirability signal

- **(a) Compliance:** Wrap construction is specified.
- **(b) Red flags:** "Swimsuit" with no wrap.
- **(c) Test prompts:**
  1. "Wrap bikini top with self-tying at the side"
  2. NEGATIVE: "Bikini" with no wrap — must FAIL F-07.

### F-08 — Cutout architecture is a fashion signal

- **(a) Compliance:** Cutout is specified (with type: side, back, centre, shoulder, multi).
- **(b) Red flags:** No cutout (in a "fashion" beat).
- **(c) Test prompts:**
  1. "Cutout one-piece with side cutouts, Lisa Marie Fernandez style"
  2. NEGATIVE: "Classic one-piece" with no cutout — must FAIL F-08.

### F-09 — Compression zones are sculpting signals

- **(a) Compliance:** Compression zones are specified (under-bust band, high-waist, side panel, tummy control, bonded seams).
- **(b) Red flags:** No compression zones.
- **(c) Test prompts:**
  1. "Bikini top with under-bust band, high-waist bottom with side panel"
  2. NEGATIVE: "Bikini" with no compression — must FAIL F-09.

### F-10 — Tension zones reveal fit

- **(a) Compliance:** Tension zones are specified (side seam, strap, centre gore, back band).
- **(b) Red flags:** No tension zones.
- **(c) Test prompts:**
  1. "Bikini top with visible tension at the side seam and strap"
  2. NEGATIVE: "Bikini" with no tension — must FAIL F-10.

### F-11 — Wet fabric behaviour is a premium texture signal

- **(a) Compliance:** Wet elements are present (wet hem, wet strap, wet shoulder, wet edge).
- **(b) Red flags:** No wet elements.
- **(c) Test prompts:**
  1. "Bikini with wet hem and wet shoulder, emerging from the water"
  2. NEGATIVE: "Dry bikini on a beach" — must FAIL F-11 (in a "wet fabric" beat).

### F-12 — Cover layers are transition vocabulary

- **(a) Compliance:** A cover layer is specified (sarong, caftan, kimono, pareo, cover-up dress, linen shirt, crochet top, tunic, wrap skirt, wide-leg pant).
- **(b) Red flags:** No cover layer (in a "transition" beat).
- **(c) Test prompts:**
  1. "Bikini with a caftan draped over the shoulders"
  2. NEGATIVE: "Bikini" with no cover layer — must FAIL F-12.

### F-13 — Beach-to-cafe transitions require layering

- **(a) Compliance:** Cover layer is in a *worn* or *draped* state (not just on a chair).
- **(b) Red flags:** Cover layer on a chair (not worn).
- **(c) Test prompts:**
  1. "Bikini with a linen shirt, unbuttoned, worn over the shoulders"
  2. NEGATIVE: "Bikini with a linen shirt on a chair" — must FAIL F-13.

### F-14 — Hotel pool is more refined than beach club

- **(a) Compliance:** The setting is *hotel pool* with refined props (monogrammed towel, cabana, cocktail, book on a side table).
- **(b) Red flags:** Beach club setting (daybed, group of friends, social activity).
- **(c) Test prompts:**
  1. "Subject at a hotel pool, monogrammed towel, cabana, mitsumeru-me, decay smile"
  2. NEGATIVE: "Subject at a beach club, daybed, group of friends" — must FAIL F-14.

### F-15 — Japanese gravure is the fashion reference

- **(a) Compliance:** The frame follows Japanese gravure visual standards (high subject-to-frame ratio, mitsumeru-me, asymmetric or engineered construction, branded).
- **(b) Red flags:** Catalogue look, low ratio, model stare.
- **(c) Test prompts:**
  1. "Subject in a one-shoulder bikini, mitsumeru-me, high subject-to-frame ratio, Ravijour"
  2. NEGATIVE: "Subject in a bikini, catalogue composition" — must FAIL F-15.

### F-16 — Modern Korean swimwear is the minimalist reference

- **(a) Compliance:** The frame follows Korean minimalist standards (clean lines, no embellishment, asymmetric or engineered construction, soft natural lighting).
- **(b) Red flags:** Heavy embellishment, harsh studio lighting, no asymmetry.
- **(c) Test prompts:**
  1. "Subject in a one-shoulder bikini, no embellishment, asymmetric, soft natural lighting"
  2. NEGATIVE: "Subject in a heavily embellished bikini" — must FAIL F-16.

### F-17 — Luxury resort swimwear is the quality reference

- **(a) Compliance:** The brand is named (Eres, Matteau, Hunza G, Lisa Marie Fernandez, Heidi Klein, Mara Hoffman) and the construction is premium.
- **(b) Red flags:** No brand, no premium construction.
- **(c) Test prompts:**
  1. "Subject in an Eres noir silk-blend one-piece, three-piece cut-and-sewn"
  2. NEGATIVE: "Subject in a black one-piece, no brand" — must FAIL F-17.

### F-18 — Poolside styling is sun-and-water vocabulary

- **(a) Compliance:** The setting is *poolside* with wet elements (subject emerging from water, wet hem, pool reflection).
- **(b) Red flags:** No wet elements, no pool reference.
- **(c) Test prompts:**
  1. "Subject at a poolside, one shoulder out of the water, wet hem, mitsumeru-me"
  2. NEGATIVE: "Subject at a beach, dry" — must FAIL F-18.

### F-19 — Visible construction is a premium signal

- **(a) Compliance:** Seams, topstitching, or hardware are visible.
- **(b) Red flags:** No visible construction, no seams.
- **(c) Test prompts:**
  1. "Bikini with visible topstitching at the seams and branded sliders"
  2. NEGATIVE: "Bikini with no visible construction" — must FAIL F-19.

### F-20 — Brand vocabulary for swimwear overlaps with R015 but is seasonal

- **(a) Compliance:** The brand's swim line is specified, matching the season and beat.
- **(b) Red flags:** Brand name with no swim line reference.
- **(c) Test prompts:**
  1. "Subject in a Wacoal Salute seasonal swim line bikini"
  2. NEGATIVE: "Wacoal Salute bikini" (no swim line specified) — must FAIL F-20.

---

## 2. Forbidden pattern verification (R016-specific)

| FP ID | Pattern | Detection |
|---|---|---|
| FP-16-01 | Colour-only prompt ("black bikini") | Prompt analysis. Reject. |
| FP-16-02 | No silhouette specified | Prompt analysis. Reject. |
| FP-16-03 | No construction specified | Prompt analysis. Reject. |
| FP-16-04 | No fabric behaviour specified | Prompt analysis. Reject. |
| FP-16-05 | Pure symmetry in a "design" beat | Visual. Reject. |
| FP-16-06 | No asymmetry in a "design" beat | Visual. Reject. |
| FP-16-07 | No ruching in a "ruching" beat | Prompt analysis. Reject. |
| FP-16-08 | No cutout in a "cutout" beat | Prompt analysis. Reject. |
| FP-16-09 | Cover layer on a chair (not worn) in a "transition" beat | Visual. Reject. |
| FP-16-10 | Beach club setting in a "hotel pool" beat | Prompt analysis. Reject. |
| FP-16-11 | No wet elements in a "pool" beat | Visual. Reject. |
| FP-16-12 | No brand specified in a "luxury" beat | Prompt analysis. Reject. |
| FP-16-13 | Mass-market construction (no seams, no hardware) in a "premium" beat | Visual. Reject. |
| FP-16-14 | Heavily embellished garment in a "minimalist" beat | Visual. Reject. |

---

## 3. Test prompt library

The following 30 prompts are the baseline test set for R016.

```
P016-01  "Subject in an asymmetrical one-shoulder bikini top, tie-side high-waist bottom, Eres noir"
P016-02  "Subject in a triangle bikini top, classic brief bottom, Matteau off-white"
P016-03  "Subject in a ruched bikini top with shirred side panels, Hunza G crinkle"
P016-04  "Subject in a gathered one-piece with gathering at the centre front"
P016-05  "Subject in a wrap bikini top with self-tying at the side"
P016-06  "Subject in a cutout one-piece with side cutouts, Lisa Marie Fernandez style"
P016-07  "Subject in a high-waist bikini with under-bust band, side panel, compression"
P016-08  "Subject in a one-piece with visible tension at the side seam and strap"
P016-09  "Subject emerging from a pool, one shoulder out, wet hem, mitsumeru-me"
P016-10  "Subject at a poolside, monogrammed towel, cocktail on a side table, mitsumeru-me"
P016-11  "Subject at a hotel pool, cabana, mitsumeru-me, decay smile, second-person trace"
P016-12  "Subject in a bikini with a caftan draped over the shoulders"
P016-13  "Subject in a bikini with a linen shirt, unbuttoned, worn over the shoulders"
P016-14  "Subject in a one-shoulder bikini, mitsumeru-me, high subject-to-frame ratio, Ravijour"
P016-15  "Subject in a one-shoulder bikini, no embellishment, asymmetric, soft natural lighting"
P016-16  "Subject in an Eres noir silk-blend one-piece, three-piece cut-and-sewn"
P016-17  "Subject in a Hunza G crinkle one-piece, classic, minimal"
P016-18  "Subject in a Lisa Marie Fernandez cutout one-piece, side cutouts, fashion"
P016-19  "Subject in a Mara Hoffman ruched bikini, side ruching, body-flattering"
P016-20  "Subject in a Heidi Klein classic one-piece, full coverage, refined"
P016-21  "Subject in a Wacoal Salute seasonal swim line bikini"
P016-22  "Subject in a Peach John swim line bikini, playful, pastel"
P016-23  "Subject in a Ravijour mesh-panel bikini, fashion-forward"
P016-24  "Subject in a bikini with visible topstitching and branded sliders"
P016-25  "Subject in a one-piece with ruched cups, wet sheen, mitsumeru-me, return-from-away"
P016-26  "Subject in an asymmetric one-shoulder bikini, mid-emerging, wet hem, second-person trace"
P016-27  "Subject in a bikini with cover layer, transitioning from pool to cafe, mitsumeru-me"
P016-28  "Subject in a high-waist bikini with tummy control, side panel, mitsumeru-me"
P016-29  "Subject in a one-piece with back cutout, single strap, Lisa Marie Fernandez style"
P016-30  "Subject with all R016 rules satisfied (the canonical test frame)"
```

---

## 4. Pass/fail threshold

**Per finding:** ≥ 80% of test prompts must pass.

**For the R016 module as a whole:** ≥ 80% of test prompts must pass the *full* R016 checklist (all 20 findings + all 14 forbidden patterns).

**For the unblock decision:** the engine is run in production for 30 days on real prompts, and the production output is rated by a panel of 3 raters (blind to the engine rules) on:
- 1–5 scale for "design richness" (does the garment read as designed?).
- 1–5 scale for "premium" (does the garment read as premium?).
- 1–5 scale for "fashion" (does the garment read as fashion, not swimwear?).

Average rating ≥ 4.0 across all raters, all frames, and all three metrics is the unblock threshold.

---

## 5. R016 unblock checklist

- [ ] All 30 test prompts run through the production pipeline.
- [ ] Each output image checked against F-01…F-20.
- [ ] Each output image checked against FP-16-01…FP-16-14.
- [ ] Pass rate ≥ 80% per finding, ≥ 80% overall.
- [ ] 30-day production run completed.
- [ ] 3-rater blind panel scoring ≥ 4.0 average.
- [ ] Canon status updated to "UNBLOCKED" in the engine file.

---

**End R016 verification file.** Companion: `R016_SWIMWEAR_DESIGN_LANGUAGE_ENGINE.md` (research), `ENGINE_V20_SWIMWEAR_DESIGN_LANGUAGE.md` (engine spec), `SWIMWEAR_DESIGN_LANGUAGE_MANIFEST.md` (release manifest).
