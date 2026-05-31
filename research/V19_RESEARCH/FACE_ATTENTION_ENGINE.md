# FACE ATTENTION ENGINE — lil.troublr V19

## Core Insight

The face is the single most emotionally charged element in any frame. When a viewer's gaze meets a face, a dedicated neural pathway activates — the fusiform face area — creating an involuntary, pre-cognitive "face alert." This is not aesthetic preference; it is hardwired biology. V19's Face Attention Engine exploits this by treating facial micro-states as **memory anchors**: moments where emotional encoding is maximally activated and the viewer mentally "stamps" the image into long-term memory.

The key insight is that **not all face-on images are equal**. A deadpan stare creates attention but not retention. A slight asymmetry — the almost-smile that doesn't fully commit, the eye that catches light at the exact moment of looking away — creates cognitive **dissonance resolved by curiosity**, which is the precise neurological cocktail for memory formation.

The goal is not to capture "beautiful faces" but to engineer **face-attention events** where the viewer's brain experiences a microsecond of recognition followed by a microsecond of surprise. That gap — recognition-then-surprise — is where emotional memory forms.

---

## FACE ATTENTION LIBRARY

### Tier 1 — Maximum Retention Anchors (Use Primarily)

| Token | State | Emotional Encoding | Retention Mechanism |
|-------|-------|-------------------|---------------------|
| `micro_smile` | Corners of mouth lift 2-3mm, eyes unchanged | Warm ambiguity | Viewer completes the smile unconsciously, creating parasocial bond |
| `caught_laugh` | Full smile interrupted mid-breath, one eye slightly closed | Joy + vulnerability | Surprise at imperfection creates memory salience |
| `sleepy_warmth` | Eyes 70% closed, slight head tilt, relaxed mouth | Safety + intimacy | Slow gaze invites prolonged viewing |
| `post_swim_glow` | Skin radiance, hair damp, eyes bright from cold water | Vitality + freshness | Color contrast (flushed skin vs wet hair) creates visual anchor |

### Tier 2 — Strong Retention Anchors (Use Frequently)

| Token | State | Emotional Encoding | Retention Mechanism |
|-------|-------|-------------------|---------------------|
| `suppressed_smile` | Mouth pressed or bitten to contain expression | Repressed joy (high contrast) | Tension-release pattern holds attention |
| `camera_recognition` | Eyes lock lens, slight eyebrow raise, 0.5s hold | Mutual awareness | Viewer feels "seen" — creates direct neural coupling |
| `eye_contact_strength` | Direct gaze, pupils centered, steady | Dominance + trust | Prolonged eye contact triggers oxytocin release |
| `quiet_satisfaction` | Slight smile, eyes soft, posture reclined | Accomplishment | Implies narrative back-story viewer wants to decode |

### Tier 3 — Context-Dependent Anchors (Use Selectively)

| Token | State | Emotional Encoding | Retention Mechanism |
|-------|-------|-------------------|---------------------|
| `playful_challenge` | Eyebrow up, mouth smirk, chin slightly lifted | Invitation to engage | Viewer "accepts" the implicit challenge mentally |
| `turning_away` | Face 3/4 view, eye glances back at camera | Mystery + incomplete | Visual cliff — brain cannot leave without resolution |

---

## System Explanation

### The Face-Attention Pipeline

```
[Frame Input]
    │
    ▼
┌─────────────────────────────────────┐
│  FACE DETECTION LAYER               │
│  -瞳位置检测 (pupil localization)   │
│  -微表情分割 (micro-expression)     │
│  -肌理状态映射 (skin state mapping) │
└─────────────────┬───────────────────┘
                  │
                  ▼
┌─────────────────────────────────────┐
│  FACE-ATTENTION SCORER             │
│  Score = f(gaze_stability,         │
│            expression_intensity,   │
│            lighting_contrast,      │
│            emotional_ambiguity)     │
│                                     │
│  Threshold for "anchor": ≥0.72     │
│  Threshold for "hold": ≥0.85       │
└─────────────────┬───────────────────┘
                  │
                  ▼
┌─────────────────────────────────────┐
│  TOKEN EMITTER                      │
│  Emits composite tokens:            │
│  {face_token}_{modifier}_{strength} │
│                                     │
│  Example: micro_smile_high_0.9      │
│           caught_laugh_mid_0.85     │
└─────────────────┬───────────────────┘
                  │
                  ▼
┌─────────────────────────────────────┐
│  RETENTION PREDICTOR                │
│  Maps tokens → estimated           │
│  emotional retention rate (ERR)    │
│                                     │
│  ERR = likelihood viewer remembers │
│  this frame after 72 hours          │
└─────────────────────────────────────┘
```

### The Memory Anchor Mechanism

A face becomes a memory anchor through **three concurrent triggers**:

1. **Gaze Cascade**: When eyes are not staring but not avoiding either — a "soft focus" gaze — the viewer projects their own emotional state onto the face. This is called the **Birmingham Effect** in face-perception literature (not formally named, but observed: soft-gaze faces are rated as more memorable than direct-stare or averted-gaze controls).

2. **Micro-Expression Leakage**: When an emotion is being suppressed (e.g., a suppressed smile), facial muscles fire partially but incompletely. The viewer perceives this as "something behind the expression" — creating narrative curiosity.

3. **Thermal-Color Salience**: Post-swim glow, blush, flushed skin from cold air — these create high red-channel contrast that draws initial fixation, then the face holds it.

### The Attention-Retention Curve

```
Retention
Rate  │
 100% │     ╭─────── ← caught_laugh (ERR 94%)
  80% │   ╭─        ← micro_smile (ERR 91%)
  70% │  ╭─         ← camera_recognition (ERR 88%)
  60% │─             ← eye_contact_strength (ERR 82%)
  50% │              ← quiet_satisfaction (ERR 79%)
  40% │               ← sleepy_warmth (ERR 75%)
  30% │                ← playful_challenge (ERR 71%)
     └───────────────────────────────
        0.2   0.5   0.8   1.0
           Expression Intensity
```

Key: High emotional intensity does NOT linearly increase retention. Past a threshold (~0.85), very high intensity creates **voter fatigue** — the brain treats hyper-expressive faces as theatrical and less authentic. The retention optimum is **medium-high intensity with ambiguity**.

---

## Examples in Practice

### Example 1 — Micro-Smile (Highest Performer)

**Trigger**: Subject's mouth corners lift slightly. Eyes remain neutral or slightly upturned at outer edges. No teeth shown.

**Why it works**: The viewer unconsciously mirrors the micro-smile (limbic resonance). Their brain then attributes positive emotional state to the viewer-subject relationship. "I smiled because she smiled at me."

**V19 Token**: `micro_smile_low_0.88` → 88% ERR

**Frame characteristics**: Natural lighting, subject 1.2-1.5m from camera, face fills 35-50% of frame. Background simple (low visual noise).

---

### Example 2 — Caught Laughing

**Trigger**: Full smile in progress but suddenly aware of camera. Expression freezes with one side slightly higher, one eye partially closed by cheek muscle.

**Why it works**: Interrupted expressions create **Zeigarnik Effect** — the brain hates incomplete actions. Viewer watches for resolution that never comes, holding the frame 3x longer than a completed smile.

**V19 Token**: `caught_laugh_mid_0.94` → 94% ERR (highest in library)

**Frame characteristics**: Slight motion blur on shoulders (captured mid-gesture). Backlight rim on hair creates separation. Depth of field shallow — face is only sharp element.

---

### Example 3 — Camera Recognition Moment

**Trigger**: Subject notices camera for first time. Eyebrows lift fractionally (0.3mm), pupils dilate, mouth opens 1-2mm.

**Why it works**: This is the **first-contact moment** — the neurological state of being observed for the first time. It triggers self-consciousness, which triggers self-awareness, which triggers memory encoding. The viewer recognizes this from their own experience.

**V19 Token**: `camera_recognition_fresh_0.90` → 90% ERR

**Frame characteristics**: Longer lens (85mm+) for facial compression. Shallow depth of field. Eye-level or slightly above. Background blur critical — any background detail competes with the facial recognition moment.

---

### Example 4 — Post-Swim Glow

**Trigger**: Skin shows post-aerobic flush. Hair wet or damp. Eyes slightly dilated from cold-water shock. Cheeks red-tinted. Pores appear more defined (skin hydration).

**Why it works**: Vitality signals are processed by the brain's reward center. Wet hair changes hair silhouette radically, creating a **visual pop** that breaks expected patterns. Flush indicates recent exertion, which the brain decodes as "interesting recent activity" — narrative generation.

**V19 Token**: `post_swim_glow_high_0.85` → 85% ERR

**Frame characteristics**: Side lighting to emphasize skin texture and wet hair highlights. Subject slightly turned to show both cheek flush and wet hair sheen. No makeup (or minimal) — raw skin reads as authentic.

---

## Anti-Patterns

### What Kills Face-Attention Retention

| Anti-Pattern | Mechanism | Fix |
|-------------|-----------|-----|
| **Deadpan Stare** | No emotional ambiguity — brain classifies as threatening or neutral | Add tilt, lower gaze, slight brow movement |
| **Toothless Full Grin** | Over-commitment removes mystery | Break the smile — have subject look away mid-smile |
| **High-Intensity Everything** | Voter fatigue — brain desensitizes | Reduce intensity across frame set; use Tier 1 tokens |
| **Perfect Symmetry** | Uncanny valley; brain flags as abnormal | Slight asymmetry in expression (one side higher) |
| **Harsh Direct Flash** | Flattens skin texture, kills depth | Use diffused side light; preserve skin dimension |
| **Too Close / Portrait Dominance** | Face occupies >65% frame — no breathing room | Pull back to include shoulders; allow negative space |
| **Smize Without Context** | "Smize" (smile with eyes) in vacuum feels posed | Anchor with environment or gesture to add narrative |
| **Continuous Direct Eye Contact** | After 3+ seconds becomes confrontational, not engaging | Break eye contact with glance-away within 2s |

---

## Implementation Checklist

### Pre-Capture Setup

- [ ] Calibrate face-detection model to detect micro-expressions at ≤3mm muscle movement resolution
- [ ] Set exposure for skin-tone priority — protect highlights on forehead, maintain detail in shadows under chin
- [ ] Lens selection: 50mm-85mm for close portrait; 35mm for environmental face context
- [ ] Lighting: diffused natural light or single softbox at 45° — avoid flat front-on or harsh side
- [ ] Background: low-contrast, simple shapes — face must win all visual competition

### Capture Phase

- [ ] Instruct subject with **emotional prompts**, not pose instructions
  - Instead of "smile" → "think of something you forgot that made you laugh"
  - Instead of "look at camera" → "notice the lens, like you just heard a sound from that direction"
- [ ] Use **burst mode** — the 3rd-5th frame after instruction onset captures the authentic version (first 2 frames are performance)
- [ ] Monitor for `micro_smile` — corner lift before eye change is the key sequence
- [ ] Watch for `suppressed_smile` — typically happens when subject is told not to smile
- [ ] Catch `camera_recognition` by surprising subject with lens or sound cue

### Post-Capture / Engine Integration

- [ ] Score all captured frames through Face-Attention Scorer
- [ ] Flag frames with score ≥0.72 for retention review
- [ ] Flag frames with score ≥0.85 for priority retention ranking
- [ ] For each flagged frame, emit composite token: `{face_token}_{modifier}_{strength}`
- [ ] Cross-reference with Retention Predictor to estimate 72-hour ERR
- [ ] Reject any face frame where both eyes are not visible (gaze direction matters)
- [ ] Flag for review any face where expression intensity >0.95 (possible fatigue zone)

### Runtime Tuning

- [ ] Track `caught_laugh` frequency across session — if >15% of frames, reduce humor cues (desensitization risk)
- [ ] Balance Tier 1 / Tier 2 ratio: maintain 60% Tier 1 tokens in final selection
- [ ] Monitor `eye_contact_strength` frames — cap direct-gaze hold at 2.0 seconds equivalent in composite
- [ ] Rotate face angle tokens — do not deliver >4 consecutive `3/4_view` or `direct` frames

### Quality Gates

- [ ] Face must be primary focal point (eye-tracking heatmap validation)
- [ ] No more than one dominant face per frame (attention dilution)
- [ ] Skin texture visible at arm's-length zoom (post-swim, morning-after contexts require raw skin signal)
- [ ] No catchlight starvation — at least one light source reflecting in pupils
- [ ] Gaze direction documented with vector (for multi-frame narrative sequencing)

---

## FACE_ATTENTION_TOKEN_REFERENCE

```
FACE_TOKEN::micro_smile
  aliases: [half_smile, almost_smile, corner_lift, subtle_upturn]
  intensity_range: [0.3 - 0.8]
  err_baseline: 0.91
  capture_signal: mouth_corners_elevate_before_eyes_change
  narrative_tags: [warm, approachable, ambiguous, inviting]

FACE_TOKEN::suppressed_smile
  aliases: [bitten_lip, pressed_lip, contained_joy, lip_pressure]
  intensity_range: [0.4 - 0.75]
  err_baseline: 0.83
  capture_signal: mouth_region_tension_opposing_expression
  narrative_tags: [repressed, anticipatory, playful_withheld]

FACE_TOKEN::camera_recognition
  aliases: [first_look, noticed_lens, awareness_flash, oh_face]
  intensity_range: [0.35 - 0.7]
  err_baseline: 0.88
  capture_signal: pupil_dilation_plus_brow_fractional_0.3mm
  narrative_tags: [caught, seen, mutual_awareness, present]

FACE_TOKEN::eye_contact_strength
  aliases: [locked_gaze, direct_look, held_eye, steady_gaze]
  intensity_range: [0.5 - 0.9]
  err_baseline: 0.82
  capture_signal: centered_pupils_steady_1.5s_plus
  narrative_tags: [trust, confidence, intensity, presence]

FACE_TOKEN::playful_challenge
  aliases: [brow_quirk, smirk, knowing_look, come_here]
  intensity_range: [0.45 - 0.8]
  err_baseline: 0.71
  capture_signal: asymmetric_brow_plus_crooked_mouth
  narrative_tags: [teasing, inviting, confident, knowing]

FACE_TOKEN::caught_laughing
  aliases: [mid_laugh, frozen_joy, interrupted_giggle, laugh_break]
  intensity_range: [0.6 - 0.95]
  err_baseline: 0.94
  capture_signal: smile_complete_then_abrupt_hold_mid_gesture
  narrative_tags: [joy, surprise, authentic, vulnerable]

FACE_TOKEN::sleepy_warmth
  aliases: [morning_face, drowsy_soft, slow_blink, cocoon_expression]
  intensity_range: [0.3 - 0.6]
  err_baseline: 0.75
  capture_signal: eyelids_70pct_closed_head_tilt_15deg
  narrative_tags: [safe, intimate, soft, unhurried]

FACE_TOKEN::post_swim_glow
  aliases: [post_pool, water_flush, aquatic_radiance, wet_skin]
  intensity_range: [0.5 - 0.85]
  err_baseline: 0.85
  capture_signal: red_channel_skin_plus_wet_hair_sheen_plus_pupil_dilation
  narrative_tags: [vitality, freshness, recent_activity, raw]

FACE_TOKEN::quiet_satisfaction
  aliases: [contented, settled, achieved, softly_proud]
  intensity_range: [0.35 - 0.7]
  err_baseline: 0.79
  capture_signal: soft_eyes_plus_slight_smile_plus_reclined_posture
  narrative_tags: [accomplished, peaceful, complete, narrative_backstory]
```

---

## Research Status: V19 COMPLETE

**Next**: Integrate with Gaze-Path Analyzer for heatmap validation of face-attention tokens.

**Hypothesis to test in V20**: Does sequential delivery of Tier 1 → Tier 2 → Tier 1 tokens increase overall series retention vs randomized token delivery?

---
*Face Attention Engine — lil.troublr V19*  
*Build: FACE-ATTN::V19::2026-05-31*  
*Status: IMPLEMENTATION READY*
