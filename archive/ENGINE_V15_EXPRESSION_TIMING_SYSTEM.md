# ENGINE_V15_EXPRESSION_TIMING_SYSTEM.md

## V15 Core Module — Expression Timing Library V2
### AREA: 04 (Emotional Instability) | Status: READY FOR INTEGRATION

---

## PURPOSE

Human emotional expression is never perfectly timed. The smile isn't finished before the camera catches it. The laugh catches mid-breath. The expression lags, anticipates, interrupts, and trails off. Emotional Instability is the temporal imperfection of internal state expression — the opposite of "ready for camera" performance.

---

## KEY CONCEPTS

**Timing Spectrum**: Every expression exists on anticipation → activation → peak → dissolution → residual

**Completeness Scale**: LEVEL 0-6 from neutral to peak to returning

**Unfinished Types**: Cut-off, held, fading, misaligned, stated-then-interrupted

**Distinction from Camera Awareness**: AREA 01 = whether subject knows they're photographed. AREA 04 = whether expression is fully formed.

---

## EXPRESSION_TIMING_LIBRARY_V2

### Category A: Joy-Laughter Spectrum

**A1: LAUGH ONSET (Pre-Sound)**
```
Description: Moment before laughter becomes audible — face changes before sound
Visual: Eye contraction FIRST (Orbicularis oculi), nasolabial furrows deepen
        Shoulders begin upward 100-200ms before vocalization
Duration: 150-400ms from first eye contraction to full mouth open
Realism: Photographing just before audible laugh = face already laughing
Prompt: "laugh onset with eye contraction before mouth opens,
        shoulder anticipation upward, pre-sound facial engagement,
        150-400ms before vocalization"
Token: [EXPR_LAUGH_ONSET]
```

**A2: LAUGH PEAK HOLD (Overextended)**
```
Description: Laughter continues past moment joke ended — overshot natural endpoint
Visual: Laughter 500-1000ms longer than script, head tilt back maintained
        Breath intake visible mid-resolution
Duration: 400-1200ms beyond expected endpoint
Realism: Captured at natural comedown = caught in actual joy
Prompt: "laugh overextended holding peak past joke ending,
        head tilted back, breath intake visible at end,
        500-1000ms longer than expected"
Token: [EXPR_LAUGH_PEAK_HOLD]
```

**A3: LAUGH DISSOLUTION (Trail-Off)**
```
Description: Laugh ends incompletely — mini-burst reformations after apparent end
Visual: Mouth open → teeth show → tongue visible → [moment] → slight reopening
        Residual eye crinkling 500ms+ after mouth closes
Duration: 800-2000ms total dissolution
Realism: Reformation signals genuine emotional overflow
Prompt: "laugh dissolution with mouth returning toward neutral then mini-reopening,
        eye crinkling residual 500ms+ after mouth closes,
        800-2000ms total"
Token: [EXPR_LAUGH_DISSOLUTION]
```

**A4: SMILE INCOMPLETE (Doesn't Finish)**
```
Description: Smile begins but doesn't complete — attention redirects before peak
Visual: Mouth opens briefly → returns halfway, asymmetric onset (one side first)
        Orbicularis oculi: NO eye engagement = social smile not genuine
Prompt: "smile onset mouth slightly open then freezes before full engagement,
        asymmetric onset left/right first, eye contraction absent,
        expression incomplete disrupted mid-state"
Token: [EXPR_SMILE_INCOMPLETE]
```

**A5: SLEEPY JOY (Low-Arousal Positive)**
```
Description: Tired/sleepy person finds something genuinely funny
Visual: Eyelids 40-60% closed during laugh, delayed response 500-800ms
        Facial flush from effort, head nod forward from tiredness
Realism: Contrast between humor strength and physical limitation = complexity
Prompt: "sleepy joy with eyes half-open 40-60% closure attempting full engagement,
        laugh delayed 500-800ms from stimulus, head nodding forward from fatigue,
        slight facial flush from staying present"
Token: [EXPR_SLEEPY_JOY]
```

### Category B: Startle-Surprise States

**B1: PRE-PEAK ANTICIPATORY TENSION**
```
Description: Registering surprise but not yet at peak expression
Visual: Eyebrows rising but not fully, eyes still engaged not widened
        Hands possibly in motion toward face, body leaning toward
Timing: 50-150ms after surprising stimulus
Prompt: "pre-peak anticipation with eyebrows rising not yet fully elevated,
        eyes still engaged not widened, body leaning toward,
        50-150ms after stimulus before peak"
Token: [EXPR_SURPRISE_PRE_PEAK]
```

**B2: PEAK REACTION OVERHOLD**
```
Description: Full surprise held slightly beyond natural duration
Visual: Full eyebrow elevation sustained, hand(s) to face
        Slight backward lean, mouth "O" fully open
Timing: 300-600ms past natural de-escalation point
Prompt: "surprise overexaggeration with full eyebrow elevation sustained,
        hands to face, mouth O fully open, held 300-600ms past peak natural duration"
Token: [EXPR_SURPRISE_OVERHOLD]
```

### Category C: Fatigue-Sleep States

**C1: SLEEPY DROWSINESS (Not Yet Asleep)**
```
Description: Approaching sleep but not there — awareness fluctuating
Visual: Eyelids 30-50% closure, blinks lasting 400-700ms (normal 100-200ms)
        Head forward droop developing, body sinking into support
Prompt: "sleepy drowsiness with eyelids drooping 30-50% closed,
        single blinks lasting 400-700ms, head forward drooping,
        body sinking into support"
Token: [EXPR_DROWSINESS]
```

**C2: MICRO-SLEEP FRAGMENT (Involuntary)**
```
Description: Brief loss of awareness 2-10 seconds
Visual: Sudden head drop to chest, eyelid flutter, body jerk
        Recovery: startled reawakening 2-5 seconds later
Prompt: "micro-sleep fragment with sudden head drop chin to chest,
        eyelid flutter, body jerk, 2-10 seconds duration"
Token: [EXPR_MICRO_SLEEP]
```

**C3: FATIGUE PAIN (Accumulated)**
```
Description: Accumulated fatigue showing on face
Visual: Malar flush on cheekbones, under-eye puffiness/dark circles
        Shoulders elevated forward, mouth slightly open for breathing
Prompt: "fatigue face with malar flush concentrated on cheekbones,
        under-eye puffiness and darkened circles, shoulders elevated forward,
        mouth slightly open facilitating breathing"
Token: [EXPR_FATIGUE_FACE]
```

### Category D: Distraction-Interruption States

**D1: MID-SENTENCE INTERRUPTION**
```
Description: Person talking, photographed while mid-thought
Visual: Mouth still in position for recently finished word
        Eyes looking at something else mouth wasn't addressed to
        Eyebrows in position appropriate to thought being held
Prompt: "mid-sentence interruption with mouth still forming finished word,
        eyes not synchronized with mouth, looking elsewhere,
        eyebrows still in expression position from prior thought"
Token: [EXPR_MID_SENTENCE]
```

**D2: ATTENTION MIGRATION (Partially There)**
```
Description: Attention divided — part engaged with camera, part with something else
Visual: Eyes looking at camera but focus "through" it at something else
        Mouth slight smile but eyes not reciprocating
        One eyebrow raised one neutral (divided attention)
Prompt: "attention divided with eyes looking at camera but focused through,
        mouth smile not supported by eyes, one eyebrow raised one neutral,
        body shoulders angled back toward distraction source"
Token: [EXPR_ATTENTION_DIVIDED]
```

### Category E: Cognitive Load Expressions

**E1: THINKING FACE (Mid-Process)**
```
Description: Working through thought — not yet reached conclusion
Visual: Gaze upward and lateral (searching for words/memory)
        Eyebrows slightly inward contracted (Corrugator)
        Lips pressed or slight protrusion, head slight lateral tilt
Duration: 2-30 seconds depending on complexity
Prompt: "thinking face with gaze upward and lateral searching,
        eyebrows contracted inward, lips pressed or protruding,
        head tilted laterally, 2-30 seconds duration"
Token: [EXPR_THINKING]
```

**E2: THOUGHT INTERRUPTION (Just Got Idea)**
```
Description: Mid-thought, idea strikes suddenly
Visual: Sudden eyebrow raise (frontalis), eye roll-up straight not lateral
        Mouth small "o" or lips parted "oh", gesture frozen mid-air
Prompt: "thought interruption with sudden eyebrow raise and eye roll-up,
        mouth forming small o, hands frozen mid-gesture,
        brief recognition flash before full engagement"
Token: [EXPR_THOUGHT_IDEA]
```

### Category F: Social Inhibition Expressions

**F1: SUPPRESSED LAUGHTER**
```
Description: Something funny but social context requires suppression
Visual: Orbicularis oculi WITHOUT full mouth engagement (crow's feet, slight upturn)
        Head turn/duck away, hand to mouth covering, shoulder elevation
Prompt: "suppressed laughter with eye engagement present crow's feet visible,
        mouth just slightly upturned, hand to mouth covering,
        head turning away, shoulder elevated"
Token: [EXPR_LAUGH_SUPPRESSED]
```

**F2: EXPRESSION ASYMMETRY (Controlled/Uncontrolled)**
```
Description: One side expressing state while other maintains control
Visual: One corner more elevated than other, one eyebrow raised other neutral
        One eye engaged while other neutral
Prompt: "expression asymmetry with one corner mouth elevated asymmetric,
        one eyebrow raised one neutral, one eye engaged one neutral,
        controlled versus genuine self visible"
Token: [EXPR_ASYMMETRIC]
```

### Category G: Residual Expression States

**G1: POST-EMOTION RESIDUAL**
```
Description: Expression complete but muscles not fully returned to neutral
Visual: Nasolabial folds still slightly deepened, residual crow's feet
        Mouth corner slight upward turn, eyebrows not fully returned
Duration: 1-3 seconds after expression resolves
Prompt: "post-emotion residual with nasolabial folds still deepened,
        residual crow's feet visible, mouth corner still slightly upturned,
        1-3 seconds post-expression"
Token: [EXPR_RESIDUAL]
```

**G2: EMOTION-CONTAMINATED NEUTRAL**
```
Description: Face trying to return to neutral but emotion bleeds through
Visual: Slight mouth corner elevation, brow almost neutral but slight inner raise
        Eye brightness remaining from recent positive emotion
Prompt: "emotion-contaminated neutral with slight mouth corner elevation,
        brow almost neutral with subtle inner raise suggesting recent humor,
        residual eye brightness from positive emotion"
Token: [EXPR_CONTAMINATED_NEUTRAL]
```

---

## COMPLETENESS SPECTRUM

```
LEVEL 0: NO EXPRESSION (neutral baseline)
LEVEL 1: ANTICIPATORY (beginning but not externally visible)
LEVEL 2: ONSET (micro-expression under 200ms)
LEVEL 3: EMERGING (expression beginning to claim face)
LEVEL 4: PEAK (fully formed expression)
LEVEL 5: POST-PEAK (dissolving, residual activation)
LEVEL 6: RETURNING (almost neutral but contamination visible)

Distribution Target:
- 50% non-peak (LEVEL 1-2, LEVEL 5-6)
- 30% peak expressions (natural timing)
- 15% interrupted or incomplete
- 5% overexaggerated (specific character types)
```

---

## UNFINISHED_EXPRESSION_SYSTEM

**TYPE_1: CUT-OFF SMILE**
```
What Missing: Onset present but mouth doesn't fully engage
Visual: Mouth opens slightly then freezes rather than drawing back
Reader: "Something interrupted before smile could complete"
Prompt: "smile_onset_mouth_slightly_open_before_full_engagement
        orbicularis_incomplete_activation expression_cut"
Token: [UNFINISHED_CUTOFF_SMILE]
```

**TYPE_2: HELD LAUGH**
```
What Missing: Laugh begins but held back internally
Visual: Eye engagement present, mouth just slightly upturned, breath held
Reader: "Something very funny but subject chose not to fully laugh"
Prompt: "genuine_laugh_suppressed_hand_to_mouth_breath_held
        orbicularis_fully_active_mouth_slight_smile"
Token: [UNFINISHED_HELD_LAUGH]
```

**TYPE_3: FADING EXPRESSION**
```
What Missing: Already dissolving when captured (peak missed)
Visual: Nasolabial partially deepened, residual eye crinkling, mouth returning
Reader: "This expression was real and already passing"
Prompt: "expression_fading_smile_residual_nasolabial_crowfeet
        activation_300ms_post_peak_level_moderate"
Token: [UNFINISHED_FADING]
```

**TYPE_4: MISALIGNED EXPRESSION**
```
What Missing: Simultaneous contradictory emotional positions
Visual: Eyes showing attention to environment, mouth showing engagement with camera/person
Reader: "Attention and expression divided — caught between two states"
Prompt: "divided_attention_face_eye_looking_at_mouth_smile_asymmetric
        left_eye_right_mouth_mismatch simultaneous_contradiction"
Token: [UNFINISHED_MISALIGNED]
```

**TYPE_5: STATED-THEN-INTERRUPTED**
```
What Missing: Residual markers from earlier event + current different state
Visual: Residual Duchenne markers (eye crinkling) + current neutral/negative
Reader: "This face was just laughing — caught in transition back"
Prompt: "post_expression_residual_smile_current_state_neutral
        transition_ongoing muscle_return_rate_slow"
Token: [UNFINISHED_STATED_INTERRUPTED]
```

---

## INSTABILITY TYPE DISTRIBUTION

```
Sleepy-joy combos: 15-20%
Laugh interruption: 20-25%
Distracted mid-expression: 20-25%
Cognitive interruption: 10-15%
Residual expression: 15-20%
```

---

## TOKEN LIBRARY

```
JOY-LAUGH:
[EXPR_LAUGH_ONSET] [EXPR_LAUGH_PEAK_HOLD] [EXPR_LAUGH_DISSOLUTION]
[EXPR_SMILE_INCOMPLETE] [EXPR_SLEEPY_JOY]

SURPRISE:
[EXPR_SURPRISE_PRE_PEAK] [EXPR_SURPRISE_OVERHOLD]

FATIGUE-SLEEP:
[EXPR_DROWSINESS] [EXPR_MICRO_SLEEP] [EXPR_FATIGUE_FACE]

DISTRACTION:
[EXPR_MID_SENTENCE] [EXPR_ATTENTION_DIVIDED]

COGNITIVE:
[EXPR_THINKING] [EXPR_THOUGHT_IDEA]

SOCIAL INHIBITION:
[EXPR_LAUGH_SUPPRESSED] [EXPR_ASYMMETRIC]

RESIDUAL:
[EXPR_RESIDUAL] [EXPR_CONTAMINATED_NEUTRAL]

UNFINISHED TYPES:
[UNFINISHED_CUTOFF_SMILE] [UNFINISHED_HELD_LAUGH] [UNFINISHED_FADING]
[UNFINISHED_MISALIGNED] [UNFINISHED_STATED_INTERRUPTED]

COMPLETENESS:
[LEVEL_0_NEUTRAL] [LEVEL_1_ANTICIPATORY] [LEVEL_2_ONSET]
[LEVEL_3_EMERGING] [LEVEL_4_PEAK] [LEVEL_5_POST_PEAK] [LEVEL_6_RETURNING]
```

---

*V15 Module: ENGINE_V15_EXPRESSION_TIMING_SYSTEM.md*
*Status: READY FOR INTEGRATION*
*Cross-ref: ENGINE_V15_CONTINUITY_PERSISTENCE_SYSTEM (residual markers combine with continuity objects)*
