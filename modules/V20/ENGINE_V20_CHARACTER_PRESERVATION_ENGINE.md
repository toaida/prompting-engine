# ENGINE V20 — Character Preservation Engine

**Engine ID:** V20-ENG-020
**Version:** 0.1.0
**Canon status:** BLOCKED until production testing
**Source research:** `research/V20_RESEARCH/R020_CHARACTER_PRESERVATION_ENGINE.md`

---

## 1. Purpose

Convert R020 research into a runtime prompt contract. The engine does not promote itself to canon; it supplies testable production rules for the V20 pipeline.

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

- **R020-01: Activities overpower identity when role nouns replace character nouns** — Write character first, role second: "lil.troublr remains herself first; the sport is something she is doing today, not a new identity."
- **R020-02: Identity lock needs face, body, and behaviour simultaneously** — Use a four-part lock: "face identity preserved; body proportions preserved; expression signature preserved; behavioural signature preserved."
- **R020-03: Environment should frame her habits, not overwrite them** — Prompt: "environment supports her existing personality: she uses the gym/market/beach in her own slightly teasing, lived-in way."
- **R020-04: Wardrobe and styling must contain a signature carry-over** — Add: "one signature carry-over remains visible even in the new environment."
- **R020-05: Action scenes need personality residue after the action** — Use: "capture the recovery beat after the action; her personality returns through the reaction, not through posing during the action."

---

## 4. Output contract

```json
{
  "engine_id": "V20-ENG-020",
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
- Classify role nouns by drift risk.
- Preserve face/body/expression before styling/environment.
- Use environment-to-character ratio: subject 55–70%, object 15–25%, support environment 10–20%.


## 8. Operational Identity Lock
```text
[character] remains the same person: same face geometry, eye shape, nose-mouth relation, body proportions, expression grammar. Scene role is temporary: doing [activity], not becoming [role stereotype]. Preserve signature carry-over: [detail].
```
Pass scale 1–5; production pass = avg identity >=4.0, personality >=3.8, <=20% frames scored 1–2. Rollback after two consecutive role-drift frames.
