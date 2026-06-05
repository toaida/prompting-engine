# ENGINE_V20_SWIMWEAR_DESIGN_LANGUAGE

**Engine ID:** V20-ENG-016
**Engine name:** Swimwear Design Language Engine (R016)
**Canon status:** BLOCKED — awaiting production testing per VERIFICATION_R016
**Version:** 0.1.0
**Last updated:** 2026-06-05
**Owner:** V20 production track (lil.troublr)
**Research file:** `research/V20_RESEARCH/R016_SWIMWEAR_DESIGN_LANGUAGE_ENGINE.md`
**Verification file:** `verification/V20_RESEARCH/VERIFICATION_R016_SWIMWEAR.md`
**Release manifest:** `gpt-release/manifests/SWIMWEAR_DESIGN_LANGUAGE_MANIFEST.md`
**Companion engines:** R012 (Conversation Illusion), R014 (Viewer Gaze), R015 (Luxury Intimate Fashion), R017 (Female Teasing Behaviour)

---

## 1. Mission

Give every generated swimwear frame in the lil.troublr pipeline a **design-grade vocabulary** of silhouette, construction, fabric behaviour, and cover layer. The engine exists to convert *colour-only* swimwear prompts ("black bikini", "white bikini") into *designed* swimwear prompts (asymmetrical one-shoulder with ruched cups, tie-side high-waist in Eres noir).

The engine does NOT decide:
- Who the persona is (Persona Visual Anchor)
- Where she is (R017 / Environment Engine)
- What expression she has (R012 / Conversation Illusion)
- What her gaze anchors are (R014 / Viewer Gaze)
- What her teasing beat is (R017 / Female Teasing Behaviour)

The engine DOES decide, given the above inputs:
- The garment (silhouette, construction, fabric, hardware, coverage zones).
- The primary design signal (the one element that creates desire).
- The context (setting, lighting setup, cover layer, wet elements).
- The subject state (expression intent, posture, wet state).

---

## 2. Inputs

| Input | Type | Source | Required? |
|---|---|---|---|
| `persona_id` | string | Persona Visual Anchor | required |
| `persona_swimwear_signature` | object (preferred brands, design_signal preferences) | Persona Visual Anchor | required |
| `scene_id` | string | R011 | required |
| `scene_setting` | enum { hotel_pool, beach_club, poolside, villa, yacht, beach, private_resort } | R011 | required |
| `scene_conversation_beat` | enum { ... } | R011 or R012 | required |
| `garment_category` | enum { bikini_top, bikini_bottom, one_piece, monokini, tankini, swim_dress } | this engine | required |
| `garment_state` | enum { being_worn, being_considered, being_tried_on, mid_emerging, post_swim, pre_swim } | this engine | required |
| `lighting_setup` | object { key_light, raking_light, wet_elements } | this engine | required |
| `cover_layer` | object (type, state) | this engine | optional |
| `platform_target` | enum { instagram, xiaohongshu, twitter, douyin, generic } | R018 | required |

---

## 3. Output contract

```json
{
  "garment": {
    "brand": "Eres | Matteau | Hunza G | Lisa Marie Fernandez | Heidi Klein | Mara Hoffman | Peach John | Ravijour | Andar | Mardi Mercredi | generic_luxury",
    "category": "bikini_top | bikini_bottom | one_piece | monokini | tankini | swim_dress",
    "silhouette": {
      "top": "triangle | bandeau | halter | plunge | one_shoulder | off_shoulder | high_neck | long_sleeve | wrap | front_tie",
      "bottom": "classic_brief | high_waist | hipster | brazilian | thong | cheeky | skirted | tie_side",
      "one_piece": "classic | plunge | high_neck | one_shoulder | long_sleeve | cutout | wrap | monokini"
    },
    "construction": ["ruched", "gathered", "wrapped", "cutout", "asymmetrical", "paneled", "seamed", "bonded", "shirred", "smocked", "pleated", "quilted"],
    "construction_details": {
      "ruching_location": "side | centre | all_over | diagonal | none",
      "gathering_point": "centre_front | side | back | none",
      "cutout_type": "side | back | centre | shoulder | multi | none",
      "asymmetry_type": "one_shoulder | off_centre_cutout | single_ruched_side | asymmetric_hem | single_tie | asymmetric_neckline | mixed_fabric | none"
    },
    "fabric": {
      "type": ["italian_nylon", "french_lycra", "recycled_nylon", "silk_blend", "crinkle_lycra", "powernet", "compression_knit"],
      "behaviour": ["compression", "tension", "drape", "wet_cling", "wet_sheen", "quick_dry", "body_shaping", "uv_protective", "sheer_when_wet", "memory_fabric"]
    },
    "coverage_zones": {
      "top_coverage": "minimal | moderate | full",
      "bottom_coverage": "minimal | moderate | full",
      "compression_zones": ["under_bust_band", "high_waist", "side_panel", "tummy_control", "bonded_seams"],
      "tension_zones": ["side_seam", "strap", "centre_gore", "back_band"]
    },
    "hardware": ["gold_tone_sliders", "branded_charm", "tie_closure", "hook_closure", "none"],
    "primary_design_signal": "ruching | gathering | cutout | asymmetry | wrap | cover_layer | branded_hardware"
  },
  "context": {
    "setting": "hotel_pool | beach_club | poolside | villa | yacht | beach | private_resort",
    "lighting_setup": {
      "key_light": "natural_sun | window | studio | poolside_reflection",
      "raking_light": "low_angle | none",
      "wet_elements": ["wet_hem", "wet_strap", "wet_shoulder", "wet_edge", "none"]
    },
    "cover_layer": {
      "type": "sarong | caftan | kimono | pareo | cover_up_dress | linen_shirt | crochet_top | tunic | wrap_skirt | wide_leg_pant | none",
      "state": "worn | draped | held | on_chair | none"
    }
  },
  "subject_state": {
    "expression_intent": "considering | satisfied | playful | caught_you_looking | shared_joke | teasing | resting | decay_smile | suppressed_smile | neutral_plus",
    "posture": "standing | seated | lounging | emerging_from_water | walking | leaning | mid_action",
    "wet_state": "just_emerged | mid_swim | post_swim | pre_swim | dry"
  },
  "design_richness_score": {
    "silhouette_specificity": 0.0..1.0,
    "construction_specificity": 0.0..1.0,
    "fabric_behaviour_specificity": 0.0..1.0,
    "brand_specificity": 0.0..1.0,
    "primary_designal_presence": 0.0..1.0,
    "garment_beat_fit": 0.0..1.0,
    "any_FP_match": 0.0..1.0,
    "overall": 0.0..1.0
  }
}
```

The `design_richness_score.overall` is the engine's own estimate. A score < 0.6 should not be passed to the generator without review.

---

## 4. State

The engine maintains a per-character, per-session state:

- `default_brand`: the character's preferred swim brand.
- `garment_history`: list of garments used in recent frames.
- `design_signal_preferences`: per-character design signal preferences (this character prefers ruching, this character prefers cutout).

The state persists across frames within a session.

---

## 5. Core rules (from research file §15)

The engine enforces the 20 R016 rules. Each rule is a *hard* constraint.

| Rule ID | Rule | Pass criteria |
|---|---|---|
| R016-01 | Silhouette vocabulary | Silhouette (top/bottom/one-piece) specified with type names |
| R016-02 | Construction vocabulary | At least one construction technique specified |
| R016-03 | Fabric behaviour vocabulary | Fabric behaviour specified (wet_cling, wet_sheen, etc.) |
| R016-04 | Asymmetry reads as design | Some asymmetry present (one-shoulder, cutout, single ruched side, etc.) |
| R016-05 | Ruching is body-flattering + premium | Ruching specified with location |
| R016-06 | Gathered creates movement | Gathering specified with point |
| R016-07 | Wrap is a desirability signal | Wrap construction specified |
| R016-08 | Cutout architecture is a fashion signal | Cutout specified with type |
| R016-09 | Compression zones are sculpting signals | Compression zones specified |
| R016-10 | Tension zones reveal fit | Tension zones specified |
| R016-11 | Wet fabric is a premium signal | Wet elements present |
| R016-12 | Cover layers are transition vocabulary | Cover layer specified with state |
| R016-13 | Beach-to-cafe transitions require layering | Cover layer is worn or draped, not on a chair |
| R016-14 | Hotel pool is more refined than beach club | Setting is hotel_pool with refined props |
| R016-15 | Japanese gravure is the fashion reference | Frame follows gravure visual standards |
| R016-16 | Modern Korean swimwear is the minimalist reference | Frame follows Korean minimalist standards |
| R016-17 | Luxury resort swimwear is the quality reference | Brand is named, construction is premium |
| R016-18 | Poolside styling is sun-and-water vocabulary | Setting is poolside with wet elements |
| R016-19 | Visible construction is a premium signal | Seams, topstitching, or hardware visible |
| R016-20 | Brand vocabulary for swimwear overlaps with R015 but is seasonal | Brand's swim line is specified |

---

## 6. Forbidden patterns (R016-specific, 14 patterns)

| FP ID | Pattern |
|---|---|
| FP-16-01 | Colour-only prompt ("black bikini") |
| FP-16-02 | No silhouette specified |
| FP-16-03 | No construction specified |
| FP-16-04 | No fabric behaviour specified |
| FP-16-05 | Pure symmetry in a "design" beat |
| FP-16-06 | No asymmetry in a "design" beat |
| FP-16-07 | No ruching in a "ruching" beat |
| FP-16-08 | No cutout in a "cutout" beat |
| FP-16-09 | Cover layer on a chair (not worn) in a "transition" beat |
| FP-16-10 | Beach club setting in a "hotel pool" beat |
| FP-16-11 | No wet elements in a "pool" beat |
| FP-16-12 | No brand specified in a "luxury" beat |
| FP-16-13 | Mass-market construction in a "premium" beat |
| FP-16-14 | Heavily embellished garment in a "minimalist" beat |

---

## 7. Silhouette vocabulary (the canonical map)

The engine ships with the canonical silhouette vocabulary from research file §2:

**Bikini top silhouettes:** triangle, bandeau, halter, plunge, one-shoulder, off-shoulder, high-neck, long-sleeve, wrap, front-tie.

**Bikini bottom silhouettes:** classic brief, high-waist, hipster, brazilian, thong, cheeky, skirted, tie-side.

**One-piece silhouettes:** classic, plunge, high-neck, one-shoulder, long-sleeve, cutout, wrap, monokini.

### Brand references

- **Eres** — French luxury, classic and refined.
- **Matteau** — Australian luxury, minimalist.
- **Hunza G** — British luxury, crinkle-texture signature.
- **Lisa Marie Fernandez** — American luxury, designer (cutouts, one-shoulder).
- **Heidi Klein** — British luxury, classic.
- **Mara Hoffman** — American luxury, fashion-forward (ruching, gathering).
- **Peach John (swim line)** — Japanese playful.
- **Ravijour (swim line)** — Japanese fashion-forward.
- **Andar / Mardi Mercredi / Lost in General / HAEKIM** — modern Korean minimalist.

---

## 8. Construction vocabulary (the canonical map)

The engine ships with the canonical construction vocabulary from research file §3:

| Technique | Visual signature | Brand reference |
|---|---|---|
| Ruched | Rippled, body-flattering | Various, classic luxury |
| Gathered | Voluminous, sculptural | Modern luxury, designer |
| Wrapped | The wrap is the design | Various, vintage-inspired |
| Cutout | Engineered openings | Lisa Marie Fernandez, modern luxury |
| Asymmetrical | One side differs | Modern luxury, designer |
| Paneled | Visible seams | Sport-luxe, modern luxury |
| Seamed | Visible topstitching | Sport-luxe, premium |
| Bonded | Fused seams, clean line | Sport-luxe, modern luxury |
| Shirred | Multiple rows of gathered stitching | Vintage, bohemian |
| Smocked | Decorative gathering | Heritage, vintage |
| Pleated | Folded in regular/irregular pleats | Modern luxury, fashion |
| Quilted | Stitched padding | Luxury, vintage |

---

## 9. Fabric behaviour vocabulary (the canonical map)

The engine ships with the canonical fabric behaviour vocabulary from research file §4:

| Behaviour | Description | Visual signature |
|---|---|---|
| Compression | Holds the body in, sculpts | Body is shaped, fabric is firm |
| Tension | Pulls at certain points | Tension lines, fit visibility |
| Drape | Falls in soft folds | Drape creates movement |
| Wet cling | Becomes more transparent and clinging | Wet fabric darkens, clings |
| Wet sheen | Becomes more lustrous | Sheen becomes pronounced |
| Quick-dry | Dries fast, matte finish | Matte, functional |
| Body-shaping | Built-in shaping | Body is sculpted |
| UV-protective | Blocks UV | Dense, functional |
| Sheer when wet | Becomes semi-transparent | Body is revealed more |
| Memory fabric | Holds its shape | Garment holds silhouette |

---

## 10. Cover-layer vocabulary (the canonical map)

The engine ships with the canonical cover-layer vocabulary from research file §10:

| Type | Description | Fashion signal |
|---|---|---|
| Sarong | Long fabric wrapped around waist | Vacation, classic |
| Caftan | Long, flowing dress | Evening, refined |
| Kimono | Loose, flowing top with wide sleeves | Fashion, modern |
| Pareo | Rectangular fabric wrapped | Vacation, versatile |
| Cover-up dress | Simple dress over swimwear | Functional, refined |
| Linen shirt | Oversized, often unbuttoned | Casual, refined |
| Crochet top | Loose, crocheted | Vintage, feminine |
| Tunic | Loose, short dress or long top | Casual, refined |
| Wrap skirt | Wraps and ties | Vacation, feminine |
| Wide-leg pant | Loose, flowing pants | Refined, modern |

---

## 11. Design-richness scoring

```
overall = 0.18 * silhouette_specificity
        + 0.16 * construction_specificity
        + 0.14 * fabric_behaviour_specificity
        + 0.12 * brand_specificity
        + 0.12 * primary_designal_presence
        + 0.10 * garment_beat_fit
        + 0.18 * (1 - any_FP_match)
```

Each sub-score is 0–1, computed from the rule-check outputs.

---

## 12. Interaction with sibling engines

### R016 ↔ R012 (Conversation Illusion)

R012 reads R016's `primary_design_signal` and matches the expression to the design. For example, a "cutout" design signal pairs with a `playful_embarrassment` or `teasing` beat.

### R016 ↔ R014 (Viewer Gaze)

R014 reads the garment's `primary_design_signal` and treats it as a possible second anchor.

### R016 ↔ R015 (Luxury Intimate Fashion)

R015 and R016 share the brand vocabulary for swimwear. R015's `garment_state` and R016's `garment_state` are kept consistent (e.g., "being_considered" in R015 → "being_considered" in R016).

### R016 ↔ R017 (Female Teasing Behaviour)

R017 reads R016's `garment_state` and `cover_layer.state` to determine the appropriate teasing beat.

---

## 13. Version and changelog

**v0.1.0** (2026-06-05) — Initial engine module. Canon status: BLOCKED.

**Planned for v0.2.0 (post-production-test):**
- Per-character tuning of the `default_brand` and `design_signal_preferences`.
- Per-campaign tuning of the silhouette palette.
- A learning loop that updates the `design_richness_score` based on production A/B test data.

---

**End R016 engine spec.** Companion: `R016_SWIMWEAR_DESIGN_LANGUAGE_ENGINE.md` (research), `VERIFICATION_R016_SWIMWEAR.md` (verification), `SWIMWEAR_DESIGN_LANGUAGE_MANIFEST.md` (release manifest).
