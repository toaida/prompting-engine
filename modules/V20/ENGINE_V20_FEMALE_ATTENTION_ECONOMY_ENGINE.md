# ENGINE V20 — Female Attention Economy Engine

**Engine ID:** V20-ENG-021
**Version:** 0.1.0
**Canon status:** BLOCKED until production testing
**Source research:** `research/V20_RESEARCH/R021_FEMALE_ATTENTION_ECONOMY_ENGINE.md`

---

## 1. Purpose

Convert R021 research into a runtime prompt contract. The engine does not promote itself to canon; it supplies testable production rules for the V20 pipeline.

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

- **R021-01: Attraction is the stop-scroll layer, not the full engine** — Prompt attraction as the opening layer: "face-first beauty, clean silhouette, flattering light" but do not stop there.
- **R021-02: Retention comes from a readable gaze path** — Prompt: "viewer path: eyes → suppressed smile → hand/object → small clue → return to eyes."
- **R021-03: Attachment comes from personality continuity** — Prompt: "show a familiar habit or preference that would still appear tomorrow."
- **R021-04: Curiosity comes from withheld context, not mystery aesthetics** — Prompt: "one specific unanswered question, visually present but not fully answered."
- **R021-05: Emotional attachment requires low-status vulnerability mixed with competence** — Prompt: "beautiful but caught in a human micro-vulnerability, not defeated, not messy for its own sake."

---

## 4. Output contract

```json
{
  "engine_id": "V20-ENG-021",
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
- Separate attraction, retention, curiosity, attachment, conversion behaviour.
- Routeable detail uses selective sharpness, never all-over sharpness.
- Temporal decay: attraction stops, retention holds, curiosity/attachment create save/repeat.
