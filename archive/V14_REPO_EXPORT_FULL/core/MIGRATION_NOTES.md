# MIGRATION_NOTES.md
## V3 / V5 / V7 to V14 Repo Migration

Status: ACTIVE MIGRATION GUIDE  
Version: V14

---

# 1. Migration Goal

Transform the repo from:

advanced prompting project

into:

cinematic human realism generation architecture.

The new architecture must reduce retrieval contamination, consolidate duplicate systems, and replace obsolete prompt-first logic with V14 environmental-causality logic.

---

# 2. New File Tree

```text
/core
  ENGINE_V14_MASTER.md
  CURRENT_IMAGE_RULES.md
  MODERATION_INTELLIGENCE.md
  CHARACTER_LOCK.md
  VISUAL_INTELLIGENCE_SUMMARY.md
  MIGRATION_NOTES.md

/research
  V5_VISUAL_INTELLIGENCE_REPORT.md
  EXTERNAL_AESTHETIC_REPORTS.md
  HK_ENVIRONMENT_REFERENCE.md
  CAMERA_REALISM_STUDIES.md
  NANO_BANANA_REFERENCES.md

/reference-library
  JSON_PROMPT_EXAMPLES/
  GRAVURE_REFERENCE/
  CCD_REFERENCE/
  COSPLAY_REFERENCE/
  OLD_EXPERIMENTS/

/archive
  ENGINE_V3_MASTER.md
  ENGINE_V5_NOTES.md
  ENGINE_V7_REFERENCE_LOCK_NOTES.md
  OLD_PROMPT_SUMMARIES.md
  LEGACY_MODERATION_NOTES.md
  DEPRECATED_PROMPT_PACKS.md
```

---

# 3. Active Core Files

## ENGINE_V14_MASTER.md

Single source of truth.

Use for:

- Codex
- child agents
- retrieval
- onboarding
- future sessions
- architecture logic

## CURRENT_IMAGE_RULES.md

Short runtime execution layer.

Use before every generation round.

## MODERATION_INTELLIGENCE.md

Standalone safety and moderation-risk system.

Use for:

- swimwear
- nightlife
- home/bedroom
- close camera
- emotionally intimate scenes
- bold styling

## CHARACTER_LOCK.md

Identity-through-behavior system.

Use for:

- reference lock
- face retention
- expression consistency
- identity audits

## VISUAL_INTELLIGENCE_SUMMARY.md

Compressed retrieval summary.

Use to reduce token cost and recover active V14 vocabulary quickly.

---

# 4. Deprecated Files

Move to /archive:

- old ENGINE_V3_MASTER.md
- V5 wording-heavy summaries
- V7 angle-only reference-lock notes
- old prompt-reference summaries that emphasize wording over world simulation
- fragmented moderation notes
- seductive/glamour-first templates
- outdated identity -> outfit -> pose documents

Reason:

These files may contaminate retrieval with obsolete hierarchy.

---

# 5. Research Files

Move to /research:

- external visual intelligence reports
- Nano Banana / YouMind prompt studies
- camera taxonomy studies
- expression research notes
- Hong Kong environment research
- color grading studies
- FACS/FACE behavior research if not integrated into core

Research files are inspirational.

They should not override core execution rules.

---

# 6. Reference Library

Move examples to /reference-library:

- JSON prompt examples
- gravure templates
- cosplay templates
- lingerie ad templates
- Nano Banana examples
- old experiments

These files may contain useful structure but also unsafe or off-lane content.

Use only for:

- structure mining
- taxonomy extraction
- negative prompt examples
- formatting patterns

Not for direct style adoption.

---

# 7. Retrieval Risk Warnings

Biggest risks:

## Old Seductive Vocabulary

Terms like:

- sexy
- seductive
- viewer intimacy
- charged
- private encounter
- body emphasis

can shift generation into unsafe or off-brand territory.

## Old Hierarchy

identity -> outfit -> pose -> attractiveness -> scene

creates static beauty display.

## Prompt Library Noise

External prompt libraries may include:

- random girl identities
- youth-coded styling
- fetish-adjacent framing
- anime / cosplay logic
- cyber street fantasy
- body-first wording

Do not import them directly into active generation.

## V3/V5 Drift

Old files may over-prioritize:

- outfit diversity
- beauty wording
- sensual framing
- direct attraction

V14 prioritizes:

- world coherence
- camera psychology
- social plausibility
- environmental causality
- behavioral identity

---

# 8. Replacement Vocabulary

Replace:

- sexy
- seductive
- body emphasis
- viewer intimacy
- curve-focused
- glamour-first
- influencer look
- private encounter
- charged

With:

- environmental realism
- emotional accessibility
- observational attractiveness
- camera-observed femininity
- posture-generated silhouette
- fabric causality
- social plausibility
- behavioral identity
- world-coherent moment
- interrupted realism
- narrative residue

---

# 9. Migration Checklist

- [ ] Create /core directory
- [ ] Add ENGINE_V14_MASTER.md
- [ ] Add CURRENT_IMAGE_RULES.md
- [ ] Add MODERATION_INTELLIGENCE.md
- [ ] Add CHARACTER_LOCK.md
- [ ] Add VISUAL_INTELLIGENCE_SUMMARY.md
- [ ] Add MIGRATION_NOTES.md
- [ ] Move V3/V5/V7 files to /archive
- [ ] Move external research to /research
- [ ] Move JSON examples to /reference-library
- [ ] Update README.md to point to /core
- [ ] Update GPT-IMAGE-HANDOFF.md to reference V14
- [ ] Update any agent instructions to use V14 hierarchy
- [ ] Remove old glamour-first retrieval priority
- [ ] Flag risky old prompts as reference-only

---

# 10. Future Extension Recommendations

Recommended next modules:

- COLOR_TONE_RENDERING_SYSTEM.md
- HK_LOCAL_ENVIRONMENT_PACK.md
- CAMERA_LANGUAGE_TAXONOMY.md
- TEMPORAL_SEQUENCE_ENGINE.md
- FEED_RHYTHM_SYSTEM.md
- OBJECT_PERSISTENCE_SYSTEM.md
- REFERENCE_LOCK_AUDIT_SCORECARD.md
- BATCH_DIVERSITY_TRACKER.md
- MULTI_IMAGE_CAROUSEL_LOGIC.md

---

# 11. Final Migration Principle

Do not preserve old files because they are familiar.

Preserve only what supports:

World Rule
-> Environmental Physics
-> Camera Operator Logic
-> Social Justification
-> Emotional Situation
-> Activity
-> Posture Mechanics
-> Fabric Causality
-> Narrative Whitespace
-> Environmental Texture
-> Human Imperfection
-> Attraction as Emergent Result

Everything else becomes archive.
