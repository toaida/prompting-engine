# SWIMWEAR_DESIGN_LANGUAGE_MANIFEST

**Manifest ID:** MANIFEST-R016-V01
**Engine:** R016 Swimwear Design Language Engine
**Project:** lil.troublr
**Canon status:** BLOCKED (engine itself) — manifest is the *release* document, not the engine canon
**Version:** 0.1.0
**Last updated:** 2026-06-05
**Owner:** V20 production track (lil.troublr)

---

## 1. Purpose

This manifest declares the public surface of the R016 Swimwear Design Language Engine for downstream systems, partners, and production tooling. It specifies what the engine emits, what it consumes, and what the release criteria are.

The manifest is the *contract*; the engine is the *implementation*. Downstream systems (image generators, content pipelines, partner APIs) integrate against the manifest, not against the engine directly.

---

## 2. Public surface

### 2.1 Engine identifier

```
engine_id: V20-ENG-016
engine_name: "Swimwear Design Language Engine"
project: "lil.troublr"
version: "0.1.0"
canon_status: "BLOCKED"
```

### 2.2 Engine purpose

```
purpose: |
  Give every generated swimwear frame a design-grade vocabulary of silhouette,
  construction, fabric behaviour, and cover layer. Convert colour-only swimwear
  prompts ("black bikini", "white bikini") into designed swimwear prompts
  (asymmetrical one-shoulder with ruched cups, tie-side high-waist in Eres noir).

objective: "fashion vocabulary, construction vocabulary, silhouette vocabulary,
            fabric behaviour vocabulary — replacing the current reliance on
            colour-only descriptions."
```

### 2.3 Engine inputs (public subset)

```yaml
inputs:
  required:
    - persona_id: string
    - persona_swimwear_signature: object
    - scene_id: string
    - scene_setting: enum [hotel_pool, beach_club, poolside, villa, yacht, beach, private_resort]
    - scene_conversation_beat: enum
    - garment_category: enum [bikini_top, bikini_bottom, one_piece, monokini, tankini, swim_dress]
    - garment_state: enum
    - lighting_setup: object
    - platform_target: enum
  optional:
    - cover_layer: object [type, state]
```

### 2.4 Engine output (public)

The engine emits a JSON object of the form:

```json
{
  "engine_id": "V20-ENG-016",
  "version": "0.1.0",
  "timestamp": "<ISO 8601>",
  "garment": {
    "brand": "...",
    "category": "...",
    "silhouette": {
      "top": "...",
      "bottom": "...",
      "one_piece": "..."
    },
    "construction": ["..."],
    "construction_details": {...},
    "fabric": {
      "type": ["..."],
      "behaviour": ["..."]
    },
    "coverage_zones": {...},
    "hardware": ["..."],
    "primary_design_signal": "..."
  },
  "context": {
    "setting": "...",
    "lighting_setup": {...},
    "cover_layer": {...}
  },
  "subject_state": {
    "expression_intent": "...",
    "posture": "...",
    "wet_state": "..."
  },
  "design_richness_score": {
    "silhouette_specificity": 0.0,
    "construction_specificity": 0.0,
    "fabric_behaviour_specificity": 0.0,
    "brand_specificity": 0.0,
    "primary_designal_presence": 0.0,
    "garment_beat_fit": 0.0,
    "any_FP_match": 0.0,
    "overall": 0.0
  }
}
```

### 2.5 Silhouette vocabulary (canonical)

**Bikini top:** triangle, bandeau, halter, plunge, one-shoulder, off-shoulder, high-neck, long-sleeve, wrap, front-tie.
**Bikini bottom:** classic brief, high-waist, hipster, brazilian, thong, cheeky, skirted, tie-side.
**One-piece:** classic, plunge, high-neck, one-shoulder, long-sleeve, cutout, wrap, monokini.

### 2.6 Construction vocabulary (canonical)

Ruched, gathered, wrapped, cutout, asymmetrical, paneled, seamed, bonded, shirred, smocked, pleated, quilted.

### 2.7 Fabric behaviour vocabulary (canonical)

Compression, tension, drape, wet_cling, wet_sheen, quick_dry, body_shaping, uv_protective, sheer_when_wet, memory_fabric.

### 2.8 Cover-layer vocabulary (canonical)

Sarong, caftan, kimono, pareo, cover_up_dress, linen_shirt, crochet_top, tunic, wrap_skirt, wide_leg_pant.

---

## 3. Public rules

The engine enforces 20 R016 rules. Downstream systems can validate outputs against these rules:

| Rule ID | Rule |
|---|---|
| R016-01 | Silhouette vocabulary |
| R016-02 | Construction vocabulary |
| R016-03 | Fabric behaviour vocabulary |
| R016-04 | Asymmetry reads as design |
| R016-05 | Ruching is body-flattering + premium |
| R016-06 | Gathered creates movement |
| R016-07 | Wrap is a desirability signal |
| R016-08 | Cutout architecture is a fashion signal |
| R016-09 | Compression zones are sculpting signals |
| R016-10 | Tension zones reveal fit |
| R016-11 | Wet fabric is a premium signal |
| R016-12 | Cover layers are transition vocabulary |
| R016-13 | Beach-to-cafe transitions require layering |
| R016-14 | Hotel pool is more refined than beach club |
| R016-15 | Japanese gravure is the fashion reference |
| R016-16 | Modern Korean swimwear is the minimalist reference |
| R016-17 | Luxury resort swimwear is the quality reference |
| R016-18 | Poolside styling is sun-and-water vocabulary |
| R016-19 | Visible construction is a premium signal |
| R016-20 | Brand vocabulary for swimwear overlaps with R015 but is seasonal |

### Forbidden patterns (R016-specific, 14 patterns)

| FP ID | Pattern |
|---|---|
| FP-16-01 | Colour-only prompt |
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

## 4. Release criteria

The engine can be released (canon status updated from BLOCKED to UNBLOCKED) when:

- [ ] All 30 verification test prompts pass at ≥ 80%.
- [ ] 30-day production run completed.
- [ ] 3-rater blind panel scoring ≥ 4.0 average on design richness, premium, fashion.
- [ ] Brand-specific signatures verified for at least 3 brands.
- [ ] Documentation complete: research, verification, engine, manifest all present.
- [ ] All public surface (this manifest) is consistent with the engine implementation.

---

## 5. Compatibility

### Compatible with

- R012 (Conversation Illusion Engine) — reads `primary_design_signal` for expression match.
- R014 (Viewer Gaze Engine) — reads `primary_design_signal` for second-anchor.
- R015 (Luxury Intimate Fashion Engine) — shares brand vocabulary for swimwear.
- R017 (Female Teasing Behaviour Engine) — reads `garment_state` and `cover_layer.state` for beat selection.
- Persona Visual Anchor — reads `persona_swimwear_signature`.
- Environment Engine — reads `setting`.
- R011 (Scene Composition) — reads `scene_conversation_beat`.
- R018 (Platform Targeting) — reads `platform_target`.

### Incompatible with

- Engines not in the lil.troublr V20 stack.
- Production runs without the verification protocol.
- Outputs with `design_richness_score.overall < 0.6`.

---

## 6. Versioning

| Version | Date | Changes | Canon status |
|---|---|---|---|
| 0.1.0 | 2026-06-05 | Initial manifest. 10 top silhouettes, 8 bottom silhouettes, 8 one-piece silhouettes, 12 construction techniques, 10 fabric behaviours, 10 cover layers. | BLOCKED |

Future versions will add silhouettes, expand construction vocabulary, and tune per-character defaults.

---

**End SWIMWEAR_DESIGN_LANGUAGE_MANIFEST.**
