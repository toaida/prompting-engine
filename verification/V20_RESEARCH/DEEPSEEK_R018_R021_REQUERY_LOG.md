

# R018_ATTENTION_ANCHOR_ENGINE.md

## Verdict: **PARTIALLY ADDRESSED**

## Remaining Blockers

1. **Gaze direction rules** — Not added. Still missing: camera vs. object vs. off-frame logic, gaze-hand coordination, and off-frame gaze requiring visible reason.

2. **Face quality prerequisites** — Not added. No micro-expression, skin texture, or familiarity criteria specified.

3. **Production-specific constraints** — Not added. Missing: character prompt integration, style compatibility (anime/painterly/photo), resolution minimums, and generation failure modes.

4. **Lighting hierarchy** — Not added. No face luminance ratio (1.5–2x background) or curiosity anchor brightness limit.

5. **Frame composition** — Not added. No anchor placement rules (face upper-left, curiosity lower-right, etc.).

6. **Negative space requirement** — Not added. No 30% minimum rule.

7. **Behavioural consistency** — Not added. No hand-object physics or functional purpose rule.

## OK to production-test? **NO**

The temporal layer and contradiction definition are fixed, but 7 of 11 flagged issues remain unaddressed. The hierarchy revision and Finding 4 clarification are correct but insufficient alone.


# R019_CAMERA_AWARENESS_ENGINE.md

## Verdict

**PARTIALLY ADDRESSED — 3 of 7 issues resolved, 4 remain.**

## Remaining Blockers

1. **Finding 4 still lumped** — "Indirect awareness" still bundles photographer, mirror, and off-frame friend as one mode. These produce different visual outcomes and need sub-findings or distinct prompt translations.

2. **Production rules still vague** — "Plausible pause" and "genre contract" remain undefined. What counts as a plausible pause? What genre conventions override realism? Need concrete examples or thresholds.

3. **Attention routing & gaze arc missing** — The consolidation accepted the thesis ("attention routing, not subject description") but did not add the hierarchy or gaze arc as production tools. These are needed to operationalize the thesis.

4. **Cultural variation note missing** — Japanese gravure vs. Korean editorial vs. Western influencer norms are not reflected in the mode definitions. This will cause failures in market-specific prompts.

## OK to Production-Test?

**NO** — The 4 remaining blockers will cause measurable failures in indirect gaze scenes, action sequences, and cross-cultural prompts. Fix these first, then test.


# R020_CHARACTER_PRESERVATION_ENGINE.md

## Verdict: **ISSUES ADDRESSED — 2 remaining blockers**

### What was fixed
- **Role-risk classification** ✓ — clear distinction between high-risk role nouns and low-risk situational descriptors
- **Identity decay management** ✓ — layered decay model with priority ordering
- **Environment-to-character ratio** ✓ — specific visual weight percentages
- **Action-scene preservation** ✓ — pre/post recovery beats
- **Priority ordering** ✓ — tiered prompt budget

### Remaining blockers

1. **Attention phase model not adopted.** The three-phase model (first glance 0-500ms, second glance 500ms-2s, sustained 2s+) is absent. Your consolidation only addresses *what* to preserve, not *when* to target each attention phase. This is the core gap from the original Finding 1 (attention routing thesis).

2. **Testing methodology unchanged.** The consolidation doesn't specify sample size, blind rating protocol, or attention phase metrics. The original verification flagged 20-frame tests as insufficient; this remains unaddressed.

### OK to production-test?
**No** — Blocked by missing attention phase targeting. Without specifying which attention phase each scene targets, the engine collapses all visual processing into one rule set, which contradicts your own thesis that gaze is task-driven. Fix this first, then test with proper methodology.


# R021_FEMALE_ATTENTION_ECONOMY_ENGINE.md

## Verdict: **BLOCKERS RESOLVED — OK to production-test**

**Remaining blockers:** None. The consolidation directly addresses all six flagged issues:

1. **Attention capture hierarchy** — Now explicit with 5-layer stack (Attraction → Retention → Curiosity → Attachment → Conversion)
2. **Routeable detail vs. all-over sharpness** — Resolved with "selective sharpness" rule and clear forbidden case
3. **Gaze path failure modes** — Four specific failure types defined with behavioral consequences
4. **Temporal attention decay** — Three time windows mapped to specific engagement decisions
5. **Cultural variance** — Three distinct gaze norms documented with production examples
6. **Category boundary ambiguity** — Implicitly resolved by the 5-layer stack's clear separation of concerns

**OK to production-test?** Yes. The framework is now structurally complete with actionable guardrails. Begin with the salience audit and gaze path reward tests as specified.
