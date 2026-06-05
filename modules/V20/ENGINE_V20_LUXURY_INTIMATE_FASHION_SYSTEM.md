# ENGINE_V20_LUXURY_INTIMATE_FASHION_SYSTEM

**Engine ID:** V20-ENG-015
**Engine name:** Luxury Intimate Fashion Engine (R015)
**Canon status:** BLOCKED — awaiting production testing per VERIFICATION_R015
**Version:** 0.1.0
**Last updated:** 2026-06-05
**Owner:** V20 production track (lil.troublr)
**Research file:** `research/V20_RESEARCH/R015_LUXURY_INTIMATE_FASHION_ENGINE.md`
**Verification file:** `verification/V20_RESEARCH/VERIFICATION_R015_INTIMATE_FASHION.md`
**Release manifest:** `gpt-release/manifests/LUXURY_INTIMATE_FASHION_MANIFEST.md`
**Companion engines:** R012 (Conversation Illusion), R014 (Viewer Gaze), R016 (Swimwear Design Language), R017 (Female Teasing Behaviour)

---

## 1. Mission

Give every generated intimate-garment frame in the lil.troublr pipeline a **fashion-grade vocabulary** of brand, cup, fabric, hardware, and design. The engine exists to convert *generic* intimate frames ("black bra", "white lingerie") into *designed* intimate frames (Wacoal Salute noir silk plunge with French Leavers lace trim and branded charm) that signal taste, craftsmanship, and access.

The engine does NOT decide:
- Who the persona is (R015 / Persona Visual Anchor — same engine ID, different module — see note below)
- Where she is (R017 / Environment Engine)
- What expression she has (R012 / Conversation Illusion)
- What her gaze anchors are (R014 / Viewer Gaze)
- What her teasing beat is (R017 / Female Teasing Behaviour)

*Note: the engine ID V20-ENG-015 is shared between this engine (R015 Luxury Intimate Fashion) and the Persona Visual Anchor (referenced as R015 in earlier modules). In production, these are separate modules that share a numerical ID. The Persona Visual Anchor module is responsible for `persona_id` and `persona_signature`; this engine (R015 Luxury Intimate Fashion) is responsible for the garment vocabulary.*

The engine DOES decide, given the above inputs:
- The garment (brand, category, color, fabric, cup type, construction, hardware).
- The primary luxury detail.
- The context (location, event type, lighting setup).
- The state (garment state, tag state, body state).
- The subject state (expression intent, posture, mirror state).

---

## 2. Inputs

| Input | Type | Source | Required? |
|---|---|---|---|
| `persona_id` | string | Persona Visual Anchor | required |
| `persona_garment_signature` | object (preferred brands, beat fit, default state) | Persona Visual Anchor | required |
| `scene_id` | string | R011 | required |
| `scene_conversation_beat` | enum { pre_speech, mid_speech, post_speech, ... playful_embarrassment, resting_with_viewer } | R011 or R012 | required |
| `garment_category` | enum { bra, bralette, bodysuit, corset, chemise, slip, robe, bikini, swimwear_one_piece, brief, high_waist, thong, garter, stockings } | this engine or R016 | required |
| `garment_state` | enum { being_worn, being_considered, being_tried_on, just_chosen, just_removed, just_purchased } | this engine | required |
| `location_type` | enum { fitting_room, bedroom, private_event, bathroom, walk_in_wardrobe, hotel_room, studio } | R017 | required |
| `event_type` | enum { trying_on, being_fitted, considering, post_choosing, arriving, leaving, private_fitting_event } | R017 | required |
| `lighting_setup` | object { key_light, raking_light, fill } | this engine | required |
| `cover_layer_ref` | object (type, state) | R016 (if applicable) | optional |
| `platform_target` | enum { instagram, xiaohongshu, twitter, douyin, generic } | R018 | required |

---

## 3. Output contract

The engine emits a JSON object specifying the garment, the context, the state, and the lighting.

```json
{
  "garment": {
    "brand": "Wacoal Salute | Ravijour | Peach John | Aubade | Chantelle | La Perla | Simone Pérèle | Triumph Premium | Fleur of England | Agent Provocateur | generic_luxury",
    "category": "bra | bralette | bodysuit | corset | chemise | slip | robe | bikini | swimwear_one_piece | brief | high_waist | thong | garter | stockings",
    "color": "noir | ivory | nude | rouge | champagne | powder | midnight | blush | specific_hex",
    "fabric": ["charmeuse_silk", "french_leavers_lace", "chantilly_lace", "tulle", "stretch_mesh", "satin", "velvet"],
    "cup_type": "moulded | soft_cup | plunge | balconette | full_cup | triangle | demi_cup",
    "construction": "three_piece_cut_and_sewn | two_piece | single_piece_moulded | lace_over_moulded | lace_only",
    "hardware": ["branded_charm", "gold_tone_sliders", "ribbon_tie", "embroidered_logo", "branded_elastic", "rhinestone_detail"],
    "primary_luxury_detail": "single_bow_at_centre_gore | branded_charm_at_centre_gore | ribbon_tie_at_back | scalloped_lace_edge | embroidered_motif"
  },
  "context": {
    "location_type": "fitting_room | bedroom | private_event | bathroom | walk_in_wardrobe | hotel_room | studio",
    "event_type": "trying_on | being_fitted | considering | post_choosing | arriving | leaving | private_fitting_event",
    "lighting_setup": {
      "key_light": "Rembrandt | butterfly | soft_box | window | fitting_room_lamp | chandelier",
      "raking_light": "low_angle_left | low_angle_right | low_angle_behind | both_sides",
      "fill": "soft | minimal | none"
    }
  },
  "state": {
    "garment_state": "being_worn | being_considered | being_tried_on | just_chosen | just_removed | just_purchased",
    "tag_state": "tag_on | tag_off | tag_being_examined | tag_removed",
    "body_state": "fully_dressed | half_dressed | mid_change | post_change | in_mirror | pre_mirror"
  },
  "subject_state": {
    "expression_intent": "considering | satisfied | surprised | delighted | amused | neutral | caught_you_looking | playful_embarrassment | decay_smile | suppressed_smile | neutral_plus",
    "posture": "standing | seated | leaning | mid_turn | looking_in_mirror | back_to_camera | side_view",
    "mirror_state": "in_mirror | mirror_reflecting | mirror_angled_away | no_mirror"
  },
  "desirability_score": {
    "brand_specificity": 0.0..1.0,
    "vocabulary_specificity": 0.0..1.0,
    "context_specificity": 0.0..1.0,
    "lighting_quality": 0.0..1.0,
    "primary_detail_presence": 0.0..1.0,
    "garment_beat_fit": 0.0..1.0,
    "any_FP_match": 0.0..1.0,
    "overall": 0.0..1.0
  }
}
```

The `desirability_score.overall` is the engine's own estimate. A score < 0.6 should not be passed to the generator without review.

---

## 4. State

The engine maintains a per-character, per-session state:

- `default_brand`: the character's preferred brand (e.g., Wacoal Salute for "classic luxury" characters, Ravijour for "fashion-forward" characters).
- `garment_history`: list of garments used in recent frames (to prevent repetition).
- `beat_to_brand_map`: per-character mapping of beats to brand defaults (e.g., this character uses Ravijour for `caught_you_looking` and Aubade for `shared_joke`).

The state persists across frames within a session.

---

## 5. Core rules (from research file §13)

The engine enforces the 15 R015 rules. Each rule is a *hard* constraint.

| Rule ID | Rule | Pass criteria |
|---|---|---|
| R015-01 | Brand vocabulary | Garment is a named brand, not "black bra" |
| R015-02 | Construction vocabulary | Cup type, construction, seam engineering specified |
| R015-03 | Material vocabulary | Fabric is named, light behaviour implied |
| R015-04 | Hardware vocabulary | At least one piece of hardware specified |
| R015-05 | Fitting-room frame realism | Location is fitting_room with "no" pile / tag / mid-decision |
| R015-06 | Designer preview / invitation-only | Location is private_event with named brand or designer |
| R015-07 | P033A template (fashion vocabulary, not swimwear) | Branded garment + private context + considered state |
| R015-08 | Premium fabrics through light | Raking light on the fabric, key + raking light setup |
| R015-09 | One luxury detail | Exactly one primary luxury detail, in a natural state |
| R015-10 | Cup construction vocabulary | Cup type is specified |
| R015-11 | Brand aesthetic is the engine | Brand's aesthetic matches the beat |
| R015-12 | French luxury signals Parisian taste | Brand is Chantelle / Aubade / Simone Pérèle for taste beats |
| R015-13 | Japanese fitting-room is the fashion reference | High subject-to-frame ratio, mitsumeru-me, designed garment |
| R015-14 | Mesh vocabulary adds depth | Mesh is specified by type, contributes to depth |
| R015-15 | Luxury packaging creates context | At least one packaging element (ribbon-wrapped box, etc.) |

---

## 6. Forbidden patterns (R015-specific, 10 patterns)

| FP ID | Pattern |
|---|---|
| FP-15-01 | Generic catalogue composition (no brand, no construction) |
| FP-15-02 | Multiple luxury details competing |
| FP-15-03 | Garment in feature position (centred, in focus) |
| FP-15-04 | No raking light on fabric |
| FP-15-05 | Brand-aesthetic mismatch (e.g., Wacoal Salute in a teasing beat) |
| FP-15-06 | Mass-market construction (no craftsmanship details) |
| FP-15-07 | Garment state doesn't match the beat |
| FP-15-08 | Subject fully dressed in a "considering" beat |
| FP-15-09 | "Black bra" or "white lingerie" with no specification |
| FP-15-10 | No hardware or branded detail |

---

## 7. Beat-to-garment mapping (default)

| Beat | Default brand | Default category | Default state | Default context |
|---|---|---|---|---|
| Caught-you-looking | Ravijour | bralette | being_worn | private_event |
| Shared joke | Peach John | bra | being_considered | fitting_room |
| Trying-not-to-laugh | Wacoal Salute | chemise | mid_change | bedroom |
| Playful embarrassment | Aubade | bra | being_tried_on | fitting_room |
| Teasing | Simone Pérèle modern | bodysuit | being_worn | walk_in_wardrobe |
| Resting with viewer | La Perla | slip | post_choosing | bedroom |
| Pre-speech | Chantelle | bra | considering | private_event |
| Post-speech | Triumph Premium | full_cup_bra | being_worn | bedroom |
| Mid-speech | Fleur of England | bralette | mid_change | walk_in_wardrobe |
| Post-laugh | Agent Provocateur | balconette_bra | being_worn | bedroom |
| Suppressed laugh | Ravijour | mesh_bodysuit | being_considered | private_event |
| Pre-laugh | Peach John | lace_chemise | mid_change | bedroom |
| Fake innocence | Wacoal Salute | silk_chemise | being_worn | walk_in_wardrobe |

The brand assignments are *defaults*. Production can override per-character or per-campaign.

---

## 8. Brand vocabulary (the canonical map)

The engine ships with the canonical brand vocabulary from research file §1:

| Brand | Aesthetic | Vocabulary |
|---|---|---|
| Wacoal Salute | Bridal, luxury, classic | Salute group, Salute silk, French Leavers lace, scalloped edges, hand-stitching, branded charm, gold-tone hardware |
| Ravijour | Fashion-forward, modern, slightly aggressive | Cutouts, mesh panels, branded hardware, geometric |
| Peach John | Playful, kawaii-influenced, girly | PJ lace, PJ bow, PJ ribbon, pastel palettes |
| Triumph Premium | European heritage, refined | Triumph premium, Triumph embroidery, body-shaping |
| Chantelle | Parisian, classic luxury | Chantelle lace, Chantelle embroidery |
| Aubade | Parisian, sensual luxury | Aubade lace, Aubade embroidery, French knicker |
| Simone Pérèle | Parisian, modern luxury | Simone cut, Simone contrast |
| La Perla | Italian, classic luxury | La Perla silk, La Perla lace, handcraft, heritage |
| Fleur of England | British, modern luxury | Fleur lace, hand-finishing, contemporary cuts |
| Agent Provocateur | British, provocative luxury | AP satin, AP lace, boudoir |
| Coco de Mer | British, ultra-luxury | CdM silk, handcraft, investment piece |

---

## 9. Construction vocabulary (the canonical map)

The engine ships with the canonical construction vocabulary from research file §2:

| Cup type | Visual signature | Brand reference |
|---|---|---|
| Moulded cup | Smooth, seamless | Triumph Premium, Chantelle basic |
| Soft-cup | Unstructured, follows body | Aubade, Simone Pérèle |
| Plunge | Deep V at centre gore | Wacoal Salute, La Perla |
| Balconette | Horizontal cut, lifts and separates | Agent Provocateur, Aubade |
| Full-cup | Maximum coverage, structured | Triumph Premium, Wacoal |
| Triangle / soft triangle | Minimal, unstructured | Fleur of England, Simone Pérèle modern |

---

## 10. Material vocabulary (the canonical map)

The engine ships with the canonical material vocabulary from research file §3:

| Fabric | Visual signature | Light behaviour |
|---|---|---|
| Silk (mulberry, charmeuse, habotai) | Liquid sheen, drapes heavily | High specular, sharp highlights |
| French Leavers lace | Intricate, scalloped edges | Lace shadows on skin |
| Raschel lace | Lighter, more open | Lighter shadows, more transparency |
| Chantilly lace | Fine, delicate | Soft shadows |
| Tulle | Fine netting, layered | Soft transparency |
| Powernet | Structured mesh | Geometric transparency |
| Stretch mesh | Soft, flexible | Soft transparency |
| Satin | Smooth, glossy | High specular, broad highlights |
| Velvet | Plush, light-absorbing | Low specular, deep shadows |

---

## 11. Hardware vocabulary (the canonical map)

The engine ships with the canonical hardware vocabulary from research file §4:

| Hardware | Brand reference | Taste signal |
|---|---|---|
| Branded charm | Wacoal Salute, La Perla, Ravijour | High |
| Gold-tone sliders | Most luxury brands | High |
| Silver-tone sliders | Most luxury brands | Medium |
| Rose gold hardware | Modern luxury | High |
| Custom bow | Peach John, Aubade | High |
| Ribbon tie | Aubade, La Perla | High |
| Embroidered logo | Triumph Premium, Wacoal | Medium |
| Branded elastic | Most luxury brands | Medium |
| Hook-and-eye closure | All brands | 2-hook basic, 4-hook luxury |
| Rhinestone detail | Agent Provocateur, La Perla seasonal | Medium |

---

## 12. Desirability scoring

```
overall = 0.20 * brand_specificity
        + 0.18 * vocabulary_specificity
        + 0.15 * context_specificity
        + 0.15 * lighting_quality
        + 0.10 * primary_detail_presence
        + 0.10 * garment_beat_fit
        + 0.12 * (1 - any_FP_match)
```

Each sub-score is 0–1:
- `brand_specificity`: 1.0 if a named brand is specified, 0.5 if `generic_luxury`, 0.0 if unbranded.
- `vocabulary_specificity`: 1.0 if all of fabric / cup_type / construction / hardware are specified, scaled by missing attributes.
- `context_specificity`: 1.0 if location and event_type are both specified, 0.5 if one, 0.0 if neither.
- `lighting_quality`: 1.0 if both key + raking are specified, 0.5 if only key, 0.0 if neither.
- `primary_detail_presence`: 1.0 if exactly one primary luxury detail is specified, 0.0 if multiple or none.
- `garment_beat_fit`: 1.0 if the brand-aesthetic matches the beat, 0.5 if neutral, 0.0 if mismatched.
- `any_FP_match`: 1.0 if no FP matches, 0.0 if any matches.

---

## 13. Interaction with sibling engines

### R015 ↔ R012 (Conversation Illusion)

R012 reads the garment's `state` and `garment_beat_fit`. For intimate frames, R012 ensures the expression matches the garment beat.

### R015 ↔ R014 (Viewer Gaze)

R014 reads the garment's `primary_luxury_detail` and treats it as the second anchor (after the face).

### R015 ↔ R016 (Swimwear Design Language)

R015 and R016 share the brand vocabulary for swimwear (R016 swim lines overlap with R015 intimate lines). For a "bikini" frame, R016's output is used as input to R015's vocabulary.

### R015 ↔ R017 (Female Teasing Behaviour)

R017 reads the garment's `state` to determine the appropriate teasing beat. For example, a "being_considered" garment state pairs with the `considering` or `shared_joke` beat.

### R015 ↔ R011 (Scene Composition)

R015 reads the scene's `conversation_beat` to drive the brand-aesthetic mapping.

### R015 ↔ Persona Visual Anchor

R015 reads the persona's `garment_signature` (preferred brands, beat fit, default state) to seed the output contract.

---

## 14. Version and changelog

**v0.1.0** (2026-06-05) — Initial engine module. Canon status: BLOCKED.

**Planned for v0.2.0 (post-production-test):**
- Per-character tuning of the `default_brand` and `beat_to_brand_map`.
- Per-campaign tuning of the brand palette.
- A learning loop that updates the `desirability_score` based on production A/B test data.

---

**End R015 engine spec.** Companion: `R015_LUXURY_INTIMATE_FASHION_ENGINE.md` (research), `VERIFICATION_R015_INTIMATE_FASHION.md` (verification), `LUXURY_INTIMATE_FASHION_MANIFEST.md` (release manifest).
