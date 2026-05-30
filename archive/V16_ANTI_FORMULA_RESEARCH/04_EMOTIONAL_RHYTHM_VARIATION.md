# AREA 04: EMOTIONAL RHYTHM VARIATION SYSTEM

## The Problem

Current engine emotional output: **overwhelmingly "cute + flirty + warm."**
- Most expressions: smile, laugh, coy glance
- Same emotional pacing: positive → positive → positive
- No emotional dips, no variety, no honesty

Real KOL feeds: **emotionally alive**. They show tired, distracted, bored, shy, awkward — because that's real life. A feed that's permanently happy is suspicious.

---

## EMOTIONAL_RHYTHM_LIBRARY

### Category A: Low Energy States (Honest Fatigue)

**Why important:** Exhausted = not performing. Realest state.

| Type | Description | Visual Markers | Token |
|------|-------------|----------------|-------|
| A1: POST_TIRED | Just-woke or late-night tired | Heavy lids, minimal expression, slack mouth | [POST_TIRED_EXPRESSION] |
| A2: MID_ACTIVITY_TIRED | Tired from doing something | Slight slouch, reduced posture | [MID_ACTIVITY_TIRED] |
| A3: EXHAUSTED_LAYERED | Multiple fatigue sources | Zoned out, distant gaze | [EXHAUSTED_LAYERED] |
| A4: SLEEPY_HEAD_NOD | Head dropping, fighting sleep | Micro-sleep fragments | [SLEEPY_NOD] |
| A5: ENERGY_CRASH | Was high-energy, now flat | Expression drop, slack posture | [ENERGY_CRASH] |

### Category B: Distracted/Absent States

**Why important:** Real people are often mentally elsewhere.

| Type | Description | Visual Markers | Token |
|------|-------------|----------------|-------|
| B1: PHONE_ABSORBED | Looking at phone, oblivious | Slight furrow, concentrated | [PHONE_ABSORBED] |
| B2: WINDOW_GAZING | Looking at nothing, mind wandering | Soft unfocused gaze | [WINDOW_GAZING] |
| B3: DEEP_THOUGHT | Thinking hard about something | Furrowed brow, distant | [DEEP_THOUGHT] |
| B4: OVERSTIMULATED | Too much input, shutting down | Slightly overwhelmed expression | [OVERSTIMULATED] |
| B5: MORNING_FOG | Not fully awake, processing | Blank, unfocused | [MORNING_FOG] |
| B6: THOUGHT_INTERRUPTED | Was thinking, got interrupted | Caught mid-process | [THOUGHT_INTERRUPTED] |

### Category C: Socially Uncomfortable States

**Why important:** Awkward = honest. Shows social reality.

| Type | Description | Visual Markers | Token |
|------|-------------|----------------|-------|
| C1: SHY_APPROACH | Not sure of camera/photographer | Averted gaze, slight smile | [SHY_APPROACH] |
| C2: AWKWARD_SMILE | Forced smile, uncomfortable | Too wide, eyes not engaged | [AWKWARD_SMILE] |
| C3: TOO_MANY_PEOPLE | Uncomfortable with group energy | Edge of frame, looking away | [CROWD_OVERWHELM] |
| C4: POSING_ANXIETY | Knows camera, unsure how to pose | Stiff posture, tentative expression | [POSING_ANXIETY] |
| C5: POST_ARGUMENT | Just finished disagreeing | Tense jaw, flat expression | [POST_ARGUMENT] |
| C6: FIRST_MEETING | New person, evaluating | Curious but guarded | [NEW_PERSON_CURIOSITY] |

### Category D: Negative-Adjacent Emotions

**Why important:** Perfect happiness is suspicious. Real includes irritation, boredom, frustration.

| Type | Description | Visual Markers | Token |
|------|-------------|----------------|-------|
| D1: BORED_STARE | Nothing interesting happening | Flat expression, slight frown | [BORED_STARE] |
| D2: SLIGHT_IRRITATION | Minor frustration | Furrowed brow, tight lips | [SLIGHT_IRRITATION] |
| D3: DISAPPOINTED | Expectation not met | Sighing posture, downturned | [DISAPPOINTED] |
| D4: MISSING_SOMEONE | Longing for absent person | Soft sad, distant | [MISSING_SOMEONE] |
| D5: REGRET_EXPRESSION | Something undone | Wincing, avoiding eye | [REGRET_EXPRESSION] |
| D6: FRUSTRATED_BITE_LIP | Biting lip in frustration | Tense, mouth involved | [FRUSTRATED_BITE_LIP] |

### Category E: Complex/Mixed Emotions

**Why important:** Real emotions are rarely pure. Mix = sophistication.

| Type | Description | Visual Markers | Token |
|------|-------------|----------------|-------|
| E1: HAPPY_BUT_TIRED | Positive but low energy | Soft smile, heavy eyes | [HAPPY_BUT_TIRED] |
| E2: EXCITED_BUT_SHY | Eager but nervous | Bright eyes, averting gaze | [EXCITED_BUT_SHY] |
| E3: SAD_BUT_OKAY | Sad but coping | Neutral-ish, eyes give it away | [SAD_BUT_OKAY] |
| E4: TEASING_PLAYFUL | Pushing boundaries playfully | Mischief in eyes, slight smirk | [TEASING_PLAYFUL] |
| E5: CONFIDENT_VULNERABLE | Strong but open | Direct gaze, soft mouth | [CONFIDENT_VULNERABLE] |
| E6: PROUD_BUT_HUMBLE | Accomplished but modest | Quiet satisfaction | [PROUD_BUT_HUMBLE] |
| E7: LYING_TO_SELF | Expression contradicts reality | Micro-tells, asymmetry | [DENIAL_EXPRESSION] |

### Category F: Post-Activity Emotional States

**Why important:** After something, during something = honest context.

| Type | Description | Context | Token |
|------|-------------|---------|-------|
| F1: POST_LAUGH_RESIDUE | Just finished laughing | Residual smile, tear | [POST_LAUGH_RESIDUE] |
| F2: POST_CRY_RED | Cried recently | Red eyes, puffy | [POST_CRY_REDNESS] |
| F3: POST_ARGUMENT_TENSION | Tension remains | Avoidance, stiffness | [POST_ARGUMENT_TENSION] |
| F4: POST_WORKOUT | Post-exercise glow | Flushed, energised | [POST_WORKOUT] |
| F5: POST_SWIM_MOOD | Post-pool ambience | Chlorine, relaxed | [POST_SWIM_MOOD] |
| F6: POST_PARTY | Post-event comedown | Tired but wired | [POST_PARTY] |
| F7: TRAIN_RIDE_REFLECTION | Late night transport mood | Contemplative, alone | [TRAIN_RIDE_REFLECTION] |
| F8: NIGHTLIFE_LONELY | In party setting but alone | Contrast, disconnect | [NIGHTLIFE_LONELY] |

---

## Mood-Rotation System

### Feed-Level Rhythm Rules

```
EMOTIONAL_ROTATION_RULESET:

Rule 1: Every 5 images must have at least one "low energy" (A types) emotion
Rule 2: Positive emotions (happy, flirty, warm) should not exceed 60% of feed
Rule 3: Every 10 images should have at least one "negative-adjacent" (D types) emotion
Rule 4: "Cute + flirty" should not appear in consecutive images
Rule 5: Post-activity states (F types) should appear every 3-4 images
```

### Emotion Density Guidelines

| Emotion Type | Percentage of Feed | Purpose |
|-------------|-------------------|---------|
| Warm/Positive (classic) | 40-50% | Core lil.troublr identity |
| Low Energy (honest) | 15-20% | Realism anchor |
| Distracted/Absent | 10-15% | Life-continuity |
| Uncomfortable (social) | 5-10% | Social reality |
| Negative-adjacent | 5-10% | Honesty variety |
| Complex/Mixed | 5-10% | Sophistication |

---

## Anti-Emotional-Loop Grammar

### Combination Rules

```
CAN_COMBINE:
- [POST_TIRED_EXPRESSION] + [SAD_BUT_OKAY]
- [BORED_STARE] + [WINDOW_GAZING]
- [EXCITED_BUT_SHY] + [TEASING_PLAYFUL]
- [PHONE_ABSORBED] + [MORNING_FOG]

CANNOT_COMBINE (too similar):
- [EXHAUSTED_LAYERED] + [SLEEPY_NOD]
- [AWKWARD_SMILE] + [POSING_ANXIETY]
- [SLIGHT_IRRITATION] + [FRUSTRATED_BITE_LIP]

CONTEXT_REQUIRED:
- [POST_ARGUMENT] → requires social context
- [POST_CRY_REDNESS] → requires story context
- [NIGHTLIFE_LONELY] → requires nightlife context
```

### Prompt Grammar

```
[primary_emotion]:[A1-F8]_
[secondary_emotion]:[if_applicable]_
[intensity]:[mild_moderate_strong]_
[expression_completeness]:[full_partial_residual]_
[context_marker]:[location_or_activity]
```

**Examples:**
```
[POST_TIRED_EXPRESSION:A1]_emotion
intensity:moderate
expression_completeness:partial
context:late_morning_home

[EXCITED_BUT_SHY:E2]_emotion
intensity:mild
expression_completeness:full_with_micro_tells
context:first_time_trying_something

[BORED_STARE:D1]_emotion
intensity:mild
expression_completeness:full
context:waiting_for_friend_at_cafe
```

---

## HK-Specific Emotional Contexts (EXPANDED)

| Situation | Emotional State | Token |
|-----------|----------------|-------|
| MTR Rush Hour | [CROWD_OVERWHELM] + [OVERSTIMULATED] | [MTR_RUSH_EXHAUSTED] |
| Late Night Delivery | [TRAIN_RIDE_REFLECTION] + tired | [LATE_NIGHT_ALONE] |
| Post-Exam | [ENERGY_CRASH] + relieved | [POST_EXAM] |
| First Day at New Job | [NEW_PERSON_CURIOSITY] + nervous | [NEW_JOB_NERVOUS] |
| After Gym | [POST_WORKOUT] + tired | [POST_GYM] |
| Waiting for Boyfriend | [MISSING_SOMEONE] + anticipatory | [WAITING_BOYFRIEND] |
| Post-DSE exam | Relief + exhaustion | [DSE_RELEASE] |
| Long overtime work | Mental drain + tunnel vision | [OT_HEAVY] |
| Family dinner tension | Suppressed irritation + passive face | [FAMILY_DINNER_TENSE] |
| Shenzhen haggle fail | Disappointed + frustrated | [SHENZHEN_HAGGLE] |
| Post-breakup | Sad but okay + nightlife lonely | [POST_BREAKUP] |
| Live shopping nervous | Excited but shy + overstimulated | [LIVE_SHOPPING_NERVOUS] |
| Waiting BF late | Missing + slight irritation | [WAITING_BF_LATE] |

---

*Research: AREA 04 — Emotional Rhythm Variation System*
*Status: IN PROGRESS — Ready for DeepSeek verification + extension*