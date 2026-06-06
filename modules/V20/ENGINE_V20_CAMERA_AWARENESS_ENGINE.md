# ENGINE V20 — Camera Awareness Engine

**Engine ID:** V20-ENG-019
**Version:** 0.1.0
**Canon status:** BLOCKED until production testing
**Source research:** `research/V20_RESEARCH/R019_CAMERA_AWARENESS_ENGINE.md`

---

## 1. Purpose

Convert R019 research into a runtime prompt contract. The engine does not promote itself to canon; it supplies testable production rules for the V20 pipeline.

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

- **R019-01: Direct eye contact improves retention when the scene can plausibly pause** — Use: "she has paused for half a second and noticed the camera; eyes meet the lens while the body remains in the previous action."
- **R019-02: No eye contact is required during high-effort action** — Use: "no camera awareness; gaze locked on the ball/path; camera is observing, not being acknowledged."
- **R019-03: Accidental awareness is the bridge between realism and retention** — Use: "accidental camera awareness: eyes just flick back to the lens while her hands continue the action."
- **R019-04: Indirect eye contact works when intimacy would be too strong** — Use: "gaze to the person just beside the camera, not the lens; viewer feels included but not directly addressed."
- **R019-05: Intentional camera awareness needs a reason** — Use: "intentional camera awareness justified by her friend taking the photo / mirror selfie / fitting-room check."

---

## 4. Output contract

```json
{
  "engine_id": "V20-ENG-019",
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
- Five modes: direct, indirect, accidental, no-awareness, broken-fourth-wall campaign.
- Direct gaze requires scene physics or genre contract.
- Multi-frame transitions require narrative bridge.
