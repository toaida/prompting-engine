---
name: ENGINE_V15_FACE_FIRST_COMPOSITION_SYSTEM
description: Face-First Composition System — face as primary visual payload
areas: AREA 10
version: V15
status: READY FOR INTEGRATION
---

# ENGINE_V15_FACE_FIRST_COMPOSITION_SYSTEM

## Core Philosophy

**Face-First**: The face is the gravitational center. Viewers look at the face first — every time, without exception. The body provides context; the face provides meaning. In V15, the face is not just a feature — it's the structural anchor around which everything else organizes.

This is why face-first outperforms body-first: the body communicates action, the face communicates *reason* for action.

---

## FACE_PRIORITY_COMPOSITION_LIBRARY

### System A: Facial Primacy Architecture (5 Rules)

| Rule | Principle | Application |
|------|-----------|-------------|
| FP_01 | Face brightness > body brightness | Face is lit, body accepts shade |
| FP_02 | Face focus > body focus | Sharpest point = face, not background |
| FP_03 | Face orientation leads body | Face direction determines crop |
| FP_04 | Face expression justifies body | Body position matches facial emotion |
| FP_05 | Face coverage > body coverage | More frame to face, less to environment |

### Upper-Body Dominance Matrix

| Type | Face % | Body % | Use Case | Token |
|------|--------|--------|----------|-------|
| TIGHT_FACE | 70%+ | 5% | Emotion-focused, minimal context | [TIGHT_FACE] |
| FACE_PRIMARY | 50-70% | 15-25% | Standard face-first | [FACE_PRIMARY] |
| FACE_BALANCED | 35-50% | 30-40% | Environment-aware | [FACE_BALANCED] |
| UPPER_BODY | 20-35% | 40-60% | Action with face legibility | [UPPER_BODY] |
| CONTEXTUAL | 10-20% | 50-70% | Scene with face anchor | [CONTEXTUAL_FACE] |

### Eye-Contact System (3 Components)

| Component | Duration | Effect | Token |
|-----------|----------|--------|-------|
| GLANCE | < 500ms | Brief acknowledgment | [EYE_GLANCE] |
| SUSTAINED | 500-1500ms | Engagement, connection | [EYE_SUSTAINED] |
| AVERTED | Subject looks away | Discomfort, distraction | [EYE_AVERTED] |

**Eye-Contact Probability Matrix:**

| Operator (from AREA 01) | Eye Contact Likelihood |
|------------------------|----------------------|
| OP_01 Intimate Partner | 40% direct, 40% glance, 20% averted |
| OP_05 Street Documentary | 10% direct, 30% glance, 60% averted |
| OP_09 Elder Relative | 70% direct, 20% glance, 10% averted |
| OP_11 Drunk Night | 50% direct, 20% glance, 30% averted |

### Face Retention Architecture (5 Rules)

1. **Minimum 30% of frame** — Face should occupy at least 30% of image area
2. **Center or near-center** — Face should be in center third horizontally
3. **Upper third priority** — Face should be in upper half of frame
4. **No competing brightness** — Nothing in frame should be brighter than face
5. **No competing focus** — Nothing should be sharper than face

---

## UPPER_BODY_FRAMING_GRAMMAR

### Framing Types

```
STANDARD: [subject]_upper_body_face_primary
- Face 50-70%, body 15-25%, environment 10-30%
- Balanced composition

TIGHT: [subject]_tight_face_emotional_focus
- Face 70%+, body <5%
- Intimate, expression-focused

ENVIRONMENTAL: [subject]_face_anchor_scene_context
- Face 20-35%, body 40-60%, environment 20-40%
- Activity with face legibility

PROFILE: [subject]_face_side_profile_contour
- Face at 90° turn
- Dramatic, contemplative

THREE_QUARTER: [subject]_face_three_quarter_angle
- Face at 45° turn
- Classic flattering, legible expression
```

---

## 64 Core Tokens

**Face Priority:** [FACE_BRIGHTEST] [FACE_SHARPEST] [FACE_CENTER_LEAD] [FACE_EXPRESSION_JUSTIFY] [FACE_COVERAGE_MAX]
**Crop Types:** [TIGHT_FACE] [FACE_PRIMARY] [FACE_BALANCED] [UPPER_BODY] [CONTEXTUAL_FACE]
**Eye Contact:** [EYE_GLANCE] [EYE_SUSTAINED] [EYE_AVERTED] [EYE_DOWNCAST] [EYE_LAUGHING]
**Lighting:** [FACE_LIT_BODY_SHADE] [FACE_CATCH_LIGHT] [FACE_RIM_LIGHT] [FACE_NATURAL_Window] [FACE_AMBIENT_FILLED]
**Focus:** [FACE_SHARP_BODY_SOFT] [FACE_SHARP_ALL_SHARP] [FACE_BOKEH_BACKGROUND] [FACE_ENVIRON_CLEAR]

---

## Prompt Grammar

```
[composition_type]:[face_priority_architecture]_
[face_percentage]:_[body_percentage]_
[eye_contact]:_[duration_type]_
[lighting_priority]:_[face_lighting]_
[focus_distribution]:_[face_focus_body_focus]
```

**Examples:**
```
[TIGHT_FACE]_composition_face_priority
face_percentage:75_body_percentage:5
eye_contact:[EYE_SUSTAINED]_moment_of_connection
lighting_priority:[FACE_CATCH_LIGHT]_warm_window_right
focus_distribution:[FACE_SHARP_BODY_SOFT]

[FACE_BALANCED]_composition_environmental_awareness
face_percentage:45_body_percentage:35
eye_contact:[EYE_GLANCE]_brief_acknowledgment
lighting_priority:[FACE_NATURAL_WINDOW]_ diffused_soft
focus_distribution:[FACE_ENVIRON_CLEAR]
```

---

## HK-Specific Content

- **MTR Reflection**: Face visible in window/train metal, double exposure effect
- **Night Market Neon**: Face lit by colorful signage, moody face-first
- **Tea Restaurant Table**: Upper body over dim sum, intimate sharing moment
- **Ferry Deck**: Face against harbour backdrop, wind in hair

**HK Tokens:** [MTR_REFLECTION_FACE] [NEON_FACE_LIT] [DIM_SUM_UPPER_BODY] [FERRY_WIND_FACE]

---

## Moderation Profile

**PRESERVES:**
- Natural face expressions (all 7 categories)
- Authentic eye contact patterns
- Environmental lighting that illuminates face

**REMOVES:**
- Overly studio-lit face-first (unrealistic)
- Extreme face crops that distort anatomy
- Forced eye contact for performance

**CONTENT BOUNDARIES:**
→ Do not use face-framing on subjects in distress
→ TIGHT_FACE should preserve anatomy integrity
→ Face retention rules should not override subject comfort signals

---

## Cross-References

- Complements MICRO_SOCIAL (micro social interactions trigger face expressions)
- Complements EXPRESSION_TIMING (face-first amplifies expression timing effects)
- Complements BAD_PHOTO (face preserved, body accepts technical failures)

---

*Module: ENGINE_V15_FACE_FIRST_COMPOSITION_SYSTEM.md*
*Source: AREA 10 — V15 Research*
*Status: READY FOR INTEGRATION*
