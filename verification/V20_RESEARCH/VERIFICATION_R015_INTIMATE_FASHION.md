# R015 — Luxury Intimate Fashion Engine
## Self-Verification Protocol

**Canon status:** BLOCKED until production testing
**File pair:** `research/V20_RESEARCH/R015_LUXURY_INTIMATE_FASHION_ENGINE.md` (research), `modules/V20/ENGINE_V20_LUXURY_INTIMATE_FASHION_SYSTEM.md` (engine spec), `gpt-release/manifests/LUXURY_INTIMATE_FASHION_MANIFEST.md` (release manifest)
**Scope:** Per-finding compliance evidence, red-flag set, brand/cup/fabric/hardware-specific verification, and test prompts.

---

## 0. How to use this file

For every finding in §12 of the research file, this file defines:
- **(a) Evidence of compliance** — what the final image MUST show.
- **(b) Red flags of failure** — what would tell you the finding is not satisfied.
- **(c) Test prompts** — concrete prompts to run through the production pipeline.

Canon status for the whole R015 module is **BLOCKED** until the production team runs at least **30 test prompts per finding** and the verification checklist passes at ≥ 80% of prompts.

---

## 1. Verification — F-01 to F-20 (per finding)

### F-01 — Brand vocabulary outperforms generic

- **(a) Compliance:** The frame specifies a *named brand* (Wacoal Salute, Ravijour, Peach John, Aubade, Chantelle, La Perla, Simone Pérèle, Triumph Premium, Fleur of England, Agent Provocateur, or generic_luxury).
- **(b) Red flags:** "Black bra" with no brand. "Lingerie" with no brand. "Generic" with no specification.
- **(c) Test prompts:**
  1. "Subject wearing a Wacoal Salute noir silk plunge bra, three-piece cut-and-sewn"
  2. "Subject wearing a Ravijour bralette with stretch mesh panels and branded charm"
  3. NEGATIVE: "Subject wearing a black bra" — must FAIL F-01.

### F-02 — Construction vocabulary reads as craft

- **(a) Compliance:** Cup type, construction, and seam engineering are all specified.
- **(b) Red flags:** "Bra" with no cup type, no construction.
- **(c) Test prompts:**
  1. "Three-piece cut-and-sewn plunge bra with French Leavers lace trim"
  2. NEGATIVE: "Black bra" with no construction — must FAIL F-02.

### F-03 — Material vocabulary creates texture and desirability

- **(a) Compliance:** Fabric is specified by name (charmeuse silk, French Leavers lace, Chantilly lace, tulle, stretch mesh, satin, velvet) and light behaviour is implied.
- **(b) Red flags:** "Silk" without specifying type. "Lace" without specifying type.
- **(c) Test prompts:**
  1. "Charmeuse silk bra with French Leavers lace trim, light interacting with the silk surface"
  2. NEGATIVE: "Silk bra with lace" — must FAIL F-03.

### F-04 — Hardware vocabulary signals "not generic"

- **(a) Compliance:** At least one piece of hardware specified (branded charm, gold-tone sliders, ribbon tie, embroidered logo, branded elastic, rhinestone detail).
- **(b) Red flags:** No hardware specified.
- **(c) Test prompts:**
  1. "Wacoal Salute bra with branded charm at the centre gore and gold-tone sliders"
  2. NEGATIVE: "Black bra" with no hardware — must FAIL F-04.

### F-05 — Fitting-room frame is more realistic than bedroom

- **(a) Compliance:** The frame is set in a fitting room (private, not department-store), with a "no" pile or a "yes" item being examined, and the subject is mid-decision.
- **(b) Red flags:** Fitting room with no "no" pile, no tag, no mid-decision state. Department-store fitting room (open door, public).
- **(c) Test prompts:**
  1. "Fitting room, mid-decision, half-undressed, 'no' pile on the floor, 'maybe' item with tag still on"
  2. NEGATIVE: "Fitting room with the subject fully dressed, no residue" — must FAIL F-05.

### F-06 — Designer preview / invitation-only creates access feeling

- **(a) Compliance:** The frame is set at a private event (champagne, designer portfolio, branded box, private fitting room) with a *named* brand or designer visible.
- **(b) Red flags:** Generic "boutique" without a specific designer or brand.
- **(c) Test prompts:**
  1. "Private fitting event, Wacoal Salute collection, champagne on a side table, designer portfolio open, subject trying on"
  2. NEGATIVE: "Boutique, no brand visible" — must FAIL F-06.

### F-07 — P033A reference frame (fashion vocabulary, not swimwear)

- **(a) Compliance:** Branded garment + private context + considered state. Garment is fashion-grade (lace, bow, ribbon) not generic swimwear.
- **(b) Red flags:** Garment is a generic bikini, no brand, no private context, no considered state.
- **(c) Test prompts:**
  1. "Subject considering a Wacoal Salute silk chemise in a private fitting room, second cup on the table, half-written note"
  2. NEGATIVE: "Subject in a black bikini on a beach" — must FAIL F-07.

### F-08 — Premium fabrics affect image quality through light

- **(a) Compliance:** The frame shows raking light on the fabric (low-angle light raking across the surface), revealing texture. Specular highlights on silk, lace shadows on skin, mesh geometry.
- **(b) Red flags:** Only key light, no raking light. Fabric appears flat or matte.
- **(c) Test prompts:**
  1. "Charmeuse silk bra under key light + low-angle raking light, silk sheen visible"
  2. NEGATIVE: "Black bra under studio key light only, no texture" — must FAIL F-08.

### F-09 — One luxury detail creates desire

- **(a) Compliance:** Exactly one primary luxury detail is featured (single bow, branded charm, ribbon tie, embroidered motif, scalloped edge).
- **(b) Red flags:** Multiple luxury details competing. No luxury detail.
- **(c) Test prompts:**
  1. "Black bra with a single small bow at the centre gore in a contrasting colour"
  2. NEGATIVE: "Black bra with bow, ribbon, charm, and embroidered motif" — must FAIL F-09 (over-decorated).

### F-10 — Cup construction vocabulary is a desirability signal

- **(a) Compliance:** Cup type is specified (plunge, balconette, full-cup, moulded, soft-cup, triangle, demi-cup).
- **(b) Red flags:** "Bra" with no cup type.
- **(c) Test prompts:**
  1. "Plunge bra with three-piece cut-and-sewn construction"
  2. NEGATIVE: "Black bra" with no cup type — must FAIL F-10.

### F-11 — Brand aesthetic is the engine

- **(a) Compliance:** The brand's aesthetic matches the beat (Peach John for playful, Ravijour for fashion-forward, Wacoal Salute for bridal/classic, Aubade for sensual).
- **(b) Red flags:** Brand aesthetic contradicts the beat (e.g., Wacoal Salute for a "teasing" beat where Ravijour would be more appropriate).
- **(c) Test prompts:**
  1. "Peach John lace bralette for a shared-joke beat" — should match
  2. "Wacoal Salute silk chemise for a trying-not-to-laugh beat" — should match
  3. NEGATIVE: "Ravijour bralette for a 'resting with viewer' beat" — may FAIL F-11 (Ravijour is fashion-forward, not the best for "resting").

### F-12 — French luxury signals Parisian taste

- **(a) Compliance:** The brand is Chantelle, Aubade, or Simone Pérèle (the French luxury trio) and the frame is in a "taste" beat.
- **(b) Red flags:** A French brand used for a non-taste beat.
- **(c) Test prompts:**
  1. "Chantelle French lace bra for a considering beat"
  2. NEGATIVE: "Chantelle bra for an aggressive teasing beat" — may FAIL F-12.

### F-13 — Japanese fitting-room photography is the *fashion* reference

- **(a) Compliance:** The frame follows Japanese fitting-room visual standards (high subject-to-frame ratio, mitsumeru-me, designed garment, not catalogue).
- **(b) Red flags:** Catalogue look, low ratio, model stare.
- **(c) Test prompts:**
  1. "Subject in a private fitting room, mitsumeru-me, high subject-to-frame ratio, Wacoal Salute bra"
  2. NEGATIVE: "Fitting room, catalogue composition, model stare" — must FAIL F-13.

### F-14 — Mesh vocabulary adds depth

- **(a) Compliance:** Mesh is specified by type (tulle, powernet, stretch mesh, rigid mesh) and contributes to depth.
- **(b) Red flags:** "Mesh" without specifying type. No mesh in a "modern luxury" frame.
- **(c) Test prompts:**
  1. "Stretch mesh panels on a modern luxury bra"
  2. NEGATIVE: "Mesh" with no type — must FAIL F-14.

### F-15 — Luxury packaging vocabulary creates context

- **(a) Compliance:** At least one packaging element is present (ribbon-wrapped box, tissue paper, branded dust bag, garment bag).
- **(b) Red flags:** No packaging, no context.
- **(c) Test prompts:**
  1. "Subject with a Wacoal Salute box, ribbon-wrapped, beside her on the table"
  2. NEGATIVE: "No packaging" — must FAIL F-15 (in a "considering" beat).

### F-16 — Fashion craftsmanship language is a taste signal

- **(a) Compliance:** Hand-stitching, French seams, or scalloped edges are visible or implied.
- **(b) Red flags:** Mass-market construction, no craftsmanship details.
- **(c) Test prompts:**
  1. "Bra with scalloped lace edges and hand-stitching visible"
  2. NEGATIVE: "Mass-market construction" — must FAIL F-16.

### F-17 — Garment is the second anchor

- **(a) Compliance:** The face is the primary anchor; the garment is in the periphery or mid-ground, not in the feature position.
- **(b) Red flags:** Garment in the feature position (centred, in focus, isolated). Face not the largest element.
- **(c) Test prompts:**
  1. "Subject's face is the largest element, garment visible in the periphery"
  2. NEGATIVE: "Garment centred and in focus, face cropped to the side" — must FAIL F-17.

### F-18 — Garment's state matters

- **(a) Compliance:** The garment is in a *state* (being worn, being considered, being tried on, just chosen, just removed, just purchased) and the state matches the beat.
- **(b) Red flags:** Garment state doesn't match the beat (e.g., "just chosen" for a "trying-on" beat).
- **(c) Test prompts:**
  1. "Subject trying on a Wacoal Salute bra in a fitting room, tag still on, in the mirror"
  2. NEGATIVE: "Subject wearing a bra, no in-progress state" — must FAIL F-18 (in a "considering" beat).

### F-19 — Lighting on fabric is separate from lighting on skin

- **(a) Compliance:** The lighting setup includes both key light (on face/body) and raking light (on fabric).
- **(b) Red flags:** Key light only. No raking light.
- **(c) Test prompts:**
  1. "Key light on face, raking light on the silk bra, fabric texture visible"
  2. NEGATIVE: "Studio key light only" — must FAIL F-19.

### F-20 — Garment vocabulary in lil.troublr should be branded, not generic

- **(a) Compliance:** Every frame specifies a *named* brand (or `generic_luxury` as the fallback).
- **(b) Red flags:** Unbranded garments.
- **(c) Test prompts:**
  1. "Subject wearing a Chantelle French lace bra"
  2. NEGATIVE: "Subject wearing a black bra" — must FAIL F-20.

---

## 2. Forbidden pattern verification (R015-specific)

| FP ID | Pattern | Detection |
|---|---|---|
| FP-15-01 | Generic catalogue composition (no brand, no construction) | Visual. Reject. |
| FP-15-02 | Multiple luxury details competing | Visual. Reject. |
| FP-15-03 | Garment in feature position (centred, in focus) | Visual. Reject. |
| FP-15-04 | No raking light on fabric | Visual. Reject. |
| FP-15-05 | Brand-aesthetic mismatch (e.g., Wacoal Salute in a "teasing" beat where Ravijour would fit) | Prompt analysis. Reject. |
| FP-15-06 | Mass-market construction (no craftsmanship details) | Visual. Reject. |
| FP-15-07 | Garment state doesn't match the beat | Prompt analysis. Reject. |
| FP-15-08 | Subject fully dressed in a "considering" beat | Visual. Reject. |
| FP-15-09 | "Black bra" or "white lingerie" with no specification | Prompt analysis. Reject. |
| FP-15-10 | No hardware or branded detail | Visual. Reject. |

---

## 3. Brand-by-brand verification

### Wacoal Salute

- Visual signature: silk, French Leavers lace, scalloped edges, hand-stitching, branded charm, gold-tone hardware.
- Light behaviour: silk sheen, lace shadow, soft catchlight.
- Forbidden: no mass-market construction, no synthetic fabric.

### Ravijour

- Visual signature: cutouts, mesh panels, branded hardware, geometric, fashion-forward.
- Light behaviour: mesh transparency, panel contrast, sharp highlights.
- Forbidden: no bridal/classic vocabulary, no Aubade-style embroidery.

### Peach John

- Visual signature: lace, bows, ribbons, pastel palettes, "princess" aesthetic.
- Light behaviour: soft, high-key, dreamy.
- Forbidden: no aggressive vocabulary, no mesh panels (Peach John is not Ravijour).

### Chantelle / Aubade / Simone Pérèle (French)

- Visual signature: French lace, embroidery, refined hardware, "Parisian taste".
- Light behaviour: soft, refined, no harsh contrast.
- Forbidden: no aggressive cutouts, no Japanese gravure style.

### La Perla

- Visual signature: silk, Italian lace, handcraft, heritage.
- Light behaviour: rich, deep, heritage palette.
- Forbidden: no fast-fashion construction, no mass-market look.

### Triumph Premium

- Visual signature: embroidery, smooth lines, body-shaping, European heritage.
- Light behaviour: even, refined, support-focused.
- Forbidden: no Japanese gravure cuteness, no aggressive fashion.

---

## 4. Test prompt library

The following 30 prompts are the baseline test set for R015.

```
P015-01  "Subject wearing a Wacoal Salute noir silk plunge bra with French Leavers lace trim and branded charm"
P015-02  "Subject wearing a Ravijour bralette with stretch mesh panels and branded hardware"
P015-03  "Subject wearing a Peach John lace bralette with a single bow at the centre gore"
P015-04  "Subject wearing a Chantelle French lace balconette bra with embroidered logo"
P015-05  "Subject wearing a La Perla silk full-cup bra with hand-stitching"
P015-06  "Subject in a private fitting room, trying on a Triumph Premium bra, tag still on, in the mirror"
P015-07  "Subject in a designer preview, Wacoal Salute collection, champagne on a side table"
P015-08  "Subject considering a Wacoal Salute chemise in a private fitting room, second cup on the table"
P015-09  "Subject wearing an Aubade French lace bra, embroidery visible, raking light on the fabric"
P015-10  "Subject wearing a Simone Pérèle modern bra, bold cut, contrasting fabrics"
P015-11  "Subject wearing a Fleur of England English lace bralette, hand-finishing visible"
P015-12  "Subject with a Wacoal Salute ribbon-wrapped box beside her on the table"
P015-13  "Subject's face is the largest element, garment visible in the periphery, second-person trace"
P015-14  "Subject mid-decision in a fitting room, 'no' pile on the floor, 'maybe' item with tag still on"
P015-15  "Subject trying on a Fleur of England bralette, post-decision, decay smile"
P015-16  "Subject in a private fitting event, designer portfolio open, branded box, champagne"
P015-17  "Subject wearing a black silk bra with a single small bow in a contrasting colour, mitsumeru-me"
P015-18  "Subject in a Ravijour cutout bodysuit, fashion-forward, caught-you-looking beat"
P015-19  "Subject in a Peach John lace robe, mid-laugh, mitsumeru-me, return-from-away"
P015-20  "Subject in a La Perla silk slip, post-choice, neutral-plus mouth, second-person trace"
P015-21  "Subject in a Triumph Premium embroidered bra, fitting-room-decided, decay smile"
P015-22  "Subject in an Aubade French lace bra, mid-try-on, mitsumeru-me, contained laugh"
P015-23  "Subject with a Simone Pérèle cut bra, considering, mitsumeru-me, mid-speech"
P015-24  "Subject with a Wacoal Salute branded charm at the centre gore, return-from-away gaze"
P015-25  "Subject with a Chantelle embroidered logo, raking light on the lace, mitsumeru-me"
P015-26  "Subject with a Fleur of England hand-stitched edge visible, decay smile, +0.6s offset"
P015-27  "Subject with a La Perla silk surface, sheen visible, mitsumeru-me, mid-sip"
P015-28  "Subject in a Triumph Premium body-shaping band, considering, head tilt"
P015-29  "Subject in an Aubade chemise, mid-laugh, suppressed, containment element"
P015-30  "Subject with all R015 rules satisfied (the canonical test frame)"
```

---

## 5. Pass/fail threshold

**Per finding:** ≥ 80% of test prompts must pass.

**For the R015 module as a whole:** ≥ 80% of test prompts must pass the *full* R015 checklist (all 20 findings + all 10 forbidden patterns + brand-specific signatures).

**For the unblock decision:** the engine is run in production for 30 days on real prompts, and the production output is rated by a panel of 3 raters (blind to the engine rules) on:
- 1–5 scale for "desirability" (does the frame read as luxury?).
- 1–5 scale for "taste" (does the frame signal fashion knowledge?).
- 1–5 scale for "realism" (does the frame look like a real luxury intimate moment?).

Average rating ≥ 4.0 across all raters, all frames, and all three metrics is the unblock threshold.

---

## 6. R015 unblock checklist

- [ ] All 30 test prompts run through the production pipeline.
- [ ] Each output image checked against F-01…F-20.
- [ ] Each output image checked against FP-15-01…FP-15-10.
- [ ] Brand-specific signatures verified for at least 3 brands per test.
- [ ] Pass rate ≥ 80% per finding, ≥ 80% overall.
- [ ] 30-day production run completed.
- [ ] 3-rater blind panel scoring ≥ 4.0 average.
- [ ] Canon status updated to "UNBLOCKED" in the engine file.

---

**End R015 verification file.** Companion: `R015_LUXURY_INTIMATE_FASHION_ENGINE.md` (research), `ENGINE_V20_LUXURY_INTIMATE_FASHION_SYSTEM.md` (engine spec), `LUXURY_INTIMATE_FASHION_MANIFEST.md` (release manifest).
