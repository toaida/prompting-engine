# LUXURY_INTIMATE_FASHION_MANIFEST

**Manifest ID:** MANIFEST-R015-V01
**Engine:** R015 Luxury Intimate Fashion Engine
**Project:** lil.troublr
**Canon status:** BLOCKED (engine itself) — manifest is the *release* document, not the engine canon
**Version:** 0.1.0
**Last updated:** 2026-06-05
**Owner:** V20 production track (lil.troublr)

---

## 1. Purpose

This manifest declares the public surface of the R015 Luxury Intimate Fashion Engine for downstream systems, partners, and production tooling. It specifies what the engine emits, what it consumes, and what the release criteria are.

The manifest is the *contract*; the engine is the *implementation*. Downstream systems (image generators, content pipelines, partner APIs) integrate against the manifest, not against the engine directly.

---

## 2. Public surface

### 2.1 Engine identifier

```
engine_id: V20-ENG-015
engine_name: "Luxury Intimate Fashion Engine"
project: "lil.troublr"
version: "0.1.0"
canon_status: "BLOCKED"
```

### 2.2 Engine purpose

```
purpose: |
  Give every generated intimate-garment frame a fashion-grade vocabulary of brand,
  cup, fabric, hardware, and design. Convert generic intimate frames ("black bra",
  "white lingerie") into designed intimate frames (Wacoal Salute noir silk plunge
  with French Leavers lace trim and branded charm).

objective: "premium texture, craftsmanship, luxury materials, fashion desirability,
            female taste signalling — NOT sexuality."
```

### 2.3 Engine inputs (public subset)

```yaml
inputs:
  required:
    - persona_id: string                    # from Persona Visual Anchor
    - persona_garment_signature: object     # from Persona Visual Anchor
    - scene_id: string                      # from R011
    - scene_conversation_beat: enum         # from R011 or R012
    - garment_category: enum                # from this engine
    - garment_state: enum                   # from this engine
    - location_type: enum                   # from Environment Engine
    - event_type: enum                      # from Environment Engine
    - lighting_setup: object                # from this engine
    - platform_target: enum                 # from R018
  optional:
    - cover_layer_ref: object               # from R016 if applicable
```

### 2.4 Engine output (public)

The engine emits a JSON object of the form:

```json
{
  "engine_id": "V20-ENG-015",
  "version": "0.1.0",
  "timestamp": "<ISO 8601>",
  "garment": {
    "brand": "...",
    "category": "...",
    "color": "...",
    "fabric": ["..."],
    "cup_type": "...",
    "construction": "...",
    "hardware": ["..."],
    "primary_luxury_detail": "..."
  },
  "context": {
    "location_type": "...",
    "event_type": "...",
    "lighting_setup": {...}
  },
  "state": {
    "garment_state": "...",
    "tag_state": "...",
    "body_state": "..."
  },
  "subject_state": {
    "expression_intent": "...",
    "posture": "...",
    "mirror_state": "..."
  },
  "desirability_score": {
    "brand_specificity": 0.0,
    "vocabulary_specificity": 0.0,
    "context_specificity": 0.0,
    "lighting_quality": 0.0,
    "primary_detail_presence": 0.0,
    "garment_beat_fit": 0.0,
    "any_FP_match": 0.0,
    "overall": 0.0
  }
}
```

### 2.5 Brand vocabulary (canonical)

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

### 2.6 Cup vocabulary (canonical)

Moulded, soft-cup, plunge, balconette, full-cup, triangle, demi-cup.

### 2.7 Fabric vocabulary (canonical)

Charmeuse silk, French Leavers lace, Raschel lace, Chantilly lace, eyelet lace, tulle, powernet, stretch mesh, satin, velvet, cashmere, cotton.

### 2.8 Hardware vocabulary (canonical)

Branded charm, gold-tone sliders, silver-tone sliders, rose gold hardware, custom bow, ribbon tie, embroidered logo, branded elastic, hook-and-eye closure (2/3/4-hook), rhinestone detail.

---

## 3. Public rules

The engine enforces 15 R015 rules. Downstream systems can validate outputs against these rules:

| Rule ID | Rule | Pass criteria |
|---|---|---|
| R015-01 | Brand vocabulary | Garment is a named brand |
| R015-02 | Construction vocabulary | Cup type, construction, seam engineering specified |
| R015-03 | Material vocabulary | Fabric is named, light behaviour implied |
| R015-04 | Hardware vocabulary | At least one piece of hardware specified |
| R015-05 | Fitting-room frame realism | Fitting room with "no" pile / tag / mid-decision |
| R015-06 | Designer preview / invitation-only | Private event with named brand |
| R015-07 | P033A template | Branded garment + private context + considered state |
| R015-08 | Premium fabrics through light | Raking light on the fabric |
| R015-09 | One luxury detail | Exactly one primary luxury detail |
| R015-10 | Cup construction vocabulary | Cup type is specified |
| R015-11 | Brand aesthetic is the engine | Brand's aesthetic matches the beat |
| R015-12 | French luxury signals Parisian taste | Brand is French luxury for taste beats |
| R015-13 | Japanese fitting-room is the fashion reference | High subject-to-frame ratio, mitsumeru-me |
| R015-14 | Mesh vocabulary adds depth | Mesh is specified by type |
| R015-15 | Luxury packaging creates context | At least one packaging element |

### Forbidden patterns (R015-specific)

| FP ID | Pattern |
|---|---|
| FP-15-01 | Generic catalogue composition |
| FP-15-02 | Multiple luxury details competing |
| FP-15-03 | Garment in feature position |
| FP-15-04 | No raking light on fabric |
| FP-15-05 | Brand-aesthetic mismatch |
| FP-15-06 | Mass-market construction |
| FP-15-07 | Garment state doesn't match the beat |
| FP-15-08 | Subject fully dressed in a "considering" beat |
| FP-15-09 | "Black bra" or "white lingerie" with no specification |
| FP-15-10 | No hardware or branded detail |

---

## 4. Release criteria

The engine can be released (canon status updated from BLOCKED to UNBLOCKED) when:

- [ ] All 30 verification test prompts pass at ≥ 80%.
- [ ] 30-day production run completed.
- [ ] 3-rater blind panel scoring ≥ 4.0 average on desirability, taste, realism.
- [ ] Brand-specific signatures verified for at least 3 brands.
- [ ] Documentation complete: research, verification, engine, manifest all present.
- [ ] All public surface (this manifest) is consistent with the engine implementation.

---

## 5. Compatibility

### Compatible with

- R012 (Conversation Illusion Engine) — reads `garment_state` and `garment_beat_fit`.
- R014 (Viewer Gaze Engine) — reads `primary_luxury_detail` for second-anchor.
- R016 (Swimwear Design Language Engine) — shares brand vocabulary for swimwear.
- R017 (Female Teasing Behaviour Engine) — reads `garment_state` for beat selection.
- Persona Visual Anchor — reads `persona_garment_signature`.
- Environment Engine — reads `location_type` and `event_type`.
- R011 (Scene Composition) — reads `scene_conversation_beat`.
- R018 (Platform Targeting) — reads `platform_target`.

### Incompatible with

- Engines not in the lil.troublr V20 stack.
- Production runs without the verification protocol.
- Outputs with `desirability_score.overall < 0.6`.

---

## 6. Versioning

| Version | Date | Changes | Canon status |
|---|---|---|---|
| 0.1.0 | 2026-06-05 | Initial manifest. 11 brands, 7 cup types, 12 fabrics, 10 hardware types. | BLOCKED |

Future versions will add brands, expand vocabulary, and tune per-character defaults.

---

**End LUXURY_INTIMATE_FASHION_MANIFEST.**
