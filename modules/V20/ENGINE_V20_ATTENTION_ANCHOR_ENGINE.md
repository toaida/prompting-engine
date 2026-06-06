# ENGINE V20 — Attention Anchor Engine

**Engine ID:** V20-ENG-018
**Version:** 0.1.0
**Canon status:** BLOCKED until production testing
**Source research:** `research/V20_RESEARCH/R018_ATTENTION_ANCHOR_ENGINE.md`

---

## 1. Purpose

Convert R018 research into a runtime prompt contract. The engine does not promote itself to canon; it supplies testable production rules for the V20 pipeline.

---

## 2. Runtime inputs

```yaml
scene_type: string
subject_identity_scope: generic | lil_troublr_specific
activity_intensity: low | medium | high
camera_awareness_mode: direct | indirect | accidental | none
primary_attention_goal: attraction | retention | attachment | curiosity | identity_preservation
environment_role: support | narrative | product | action
canon_status: blocked_until_production_testing
```

---

## 3. Runtime rules

- **R018-01: Face + contradiction beats pure beauty** — Start prompt with one dominant human anchor, then add one unresolved clue: "her face is the sharpest and brightest anchor; one hand half-hides a small gift envelope; her eyes know the camera noticed before the scene explains why."
- **R018-02: Anchor hierarchy beats environment storytelling** — Use hierarchy language: "primary anchor: eyes; secondary anchor: mouth in suppressed smile; tertiary anchor: hand holding object; background only supports context."
- **R018-03: Curiosity requires one incomplete pattern, not many** — Add: "one incomplete pattern only: the card is visible but not readable; everything else is coherent."
- **R018-04: Zoom-in behaviour is created by legible micro-information** — Prompt micro-details as "legible at close inspection, secondary to face, not centered, not brighter than eyes."
- **R018-05: Anchor conflict kills retention** — Add negative contract: "no all-over sharpness, no background brighter than face, no competing large text, no second face as bright as subject."

---

## 4. Output contract

```json
{
  "engine_id": "V20-ENG-018",
  "canon_status": "blocked_until_production_testing",
  "primary_anchor": "face/eyes unless explicitly overridden",
  "secondary_anchor": "behaviour/object/expression",
  "curiosity_anchor_count": 1,
  "environment_priority": "support_subject_not_compete",
  "identity_scope": "follow prompt scope",
  "production_test_required": true
}
```

---

## 5. Negative prompt / guardrails

- no all-over HDR sharpness
- no background brighter than face
- no role stereotype replacing identity
- no unjustified direct gaze during high-effort action
- no catalogue object display without behaviour
- no mystery with no concrete visual question
- no more than one primary unresolved clue

---

## 6. Promotion criteria

Promote into V20 runtime only after production testing shows measurable improvement and GPT review does not flag conflict with Character Bible, runtime usability, prompt bloat, or duplicated rules.


## 7. Consolidated DeepSeek Fixes
- Use temporal attention layer: 0–200ms stop, 200ms–1s social resolution, 1–3s second-glance route, 3s+ zoom/re-look.
- Valid curiosity anchor = one resolvable social contradiction.
- R018 hierarchy excludes identity as core; identity cross-references R020.


## 8. Operational Prompt Template
```text
Attention anchor object: [object]. Owner: [owner]. Purpose: [purpose]. Last interaction: [event]. Current state: [physical state]. Visibility reason: [why visible]. Anchor priority: secondary to face, not centered, not brightest.
```
Post-check: face brightest/sharpest; one curiosity clue only; object has contact shadow/support; micro-detail secondary.


## 9. Concrete Micro-Detail Library
- gift_tag_for_later: cream tag, fragment "for later", partly hidden under thumb
- phone_preview_3_words: lock-screen notification with 3–5 visible words
- creased_receipt_time: café receipt with circled item/time under cup
- tiny_initial_charm: bracelet charm visible only in wrist catchlight
- compact_mirror_trace: blurred second cup/hand reflected in compact mirror
- strap_stitching_detail: tag/embroidered initial/stitching near strap edge
