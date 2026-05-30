# CHARACTER_LOCK.md
## lil.troublr Identity-Through-Behavior System

Status: ACTIVE CORE FILE  
Version: V14

---

# 1. Public / Internal Naming

Public account identity:

- lil.troublr

Internal legacy repo label:

- Celine

Rule:

If older files mention Celine, treat that as the same core character anchor unless explicitly replaced.

For new outward-facing prompts, use lil.troublr.

---

# 2. Fixed Character Identity

lil.troublr is:

- adult Hong Kong woman
- age 24+
- around 170cm tall
- long slim legs
- dramatic 36E-24-36 hourglass body structure
- 丰腴身材，S曲线，轮廓饱满
- 成熟美女模特
- naturally full bust
- narrow waist
- firmed and rounded hips
- realistic softness and weight distribution
- middle-class / local Hong Kong realism
- cute but mature
- playful, warm, socially believable
- confident but approachable
- flirty
- natural KOL daily-life presence

Important:

The body identity anchor is used for continuity.  
In final prompts, translate it into posture, fabric, gravity, and silhouette logic rather than repeating explicit body wording.

---

# 3. Fixed Face Anchors

Preserve:

- soft oval face
- slight apple-cheek fullness
- expressive almond-shaped eyes
- chestnut-dark layered hair
- softly full lips
- realistic warm East Asian skin texture
- tiny faint beauty mark beside the left eye near the outer corner
- visible cheek movement during smiles
- natural facial asymmetry
- realistic pores and color transitions

Avoid drift into:

- generic influencer face
- Korean-idol face unless requested as influence only
- anime face
- doll symmetry
- porcelain skin
- teen-coded face
- overly sharp jawline
- luxury-rich-girl overcoding

---

# 4. Identity Through Behavior

Identity is not only face geometry.

Identity includes:

- how her smile starts
- cheek movement
- gaze timing
- eye responsiveness
- posture habits
- social warmth
- shy/playful rhythm
- how her hair reacts to humidity
- how her body weight settles
- how she notices the camera
- how she carries casual confidence

The goal:

same woman across emotional situations

not only:

same face across angles.

---

# 5. Behavioral Anchors

lil.troublr should often feel:

- socially warm
- cute but mature
- expressive
- slightly playful
- occasionally shy
- naturally confident
- emotionally reachable
- flirty
- camera-aware but not over-posed
- local Hong Kong, not luxury fantasy

Expression tendencies:

- asymmetric smile
- cheek-lift warmth
- relaxed half-lowered eyelids when tired
- gaze reconnecting half a beat late
- very slight head tilt
- small 瞇眼 smile when appropriate
- laughter recovery rather than perfect laugh
- gentle embarrassment rather than seductive performance

---

# 6. Reference Lock Requirements

Reference lock should preserve:

- face geometry
- eye spacing
- cheek softness
- mouth shape
- beauty mark placement
- hair density and silhouette
- skin tone and pore realism
- body proportion family
- emotional warmth
- expression timing
- posture logic
- gaze behavior
- same local-girl realism

Reference lock should not only test:

- front face
- 3/4 angle
- side profile

It should also test:

- same smile behavior
- same cheek response
- same gaze rhythm
- same hair behavior under different air
- same posture habits
- same social energy

---

# 7. Recommended Reference-Lock Set

Generate one image per prompt only.

Do not create:

- collage
- grid
- contact sheet
- thumbnail set
- magazine layout
- multi-panel image

Recommended set:

## 1. Front Face Anchor

- indoor natural window light
- chest-up or upper-waist portrait
- full front face
- soft shy smile
- hair down, chestnut-dark waves
- simple fitted cream / sage knit top
- neutral Hong Kong apartment background

## 2. Left 3/4 Soft Smile

- same room / same wardrobe family
- left 3/4 angle
- looking slightly into camera
- smile beginning on one side
- window side light

## 3. Right 3/4 Shy Phone Moment

- right 3/4 angle
- slight chin-down
- eyes softly lifted
- gentle 瞇眼 smile
- phone or mug as small prop
- warm indoor realism

## 4. Mirror Selfie Identity Test

- bright window beside mirror
- side-profile mirror selfie
- head turned back toward phone camera
- phone partly covers one side of face
- natural room clutter
- upper-thigh crop
- realistic phone compression

## 5. Expression Timing Test

- same identity
- caught before smile fully forms
- gaze reconnecting late
- soft cheek movement
- slight head tilt
- no face drift

## 6. Environment Reaction Test

- humid HK doorway or old mall
- hair slightly affected by humidity / AC
- same identity under environmental stress
- natural posture and fabric reaction

---

# 8. Reference Lock Avoids

Reject if:

- younger-looking face
- school-coded or teen-coded styling
- fetish framing
- overbuilt body distortion
- AI-beauty-filter face
- generic glamour model
- face drift
- altered eye spacing
- lost beauty mark
- pale porcelain skin
- anime/doll face
- body proportions become fantasy rather than realistic continuity
- expression feels like a different personality

---

# 9. Reference Prompt Reminder

Use this in generation sessions:

```text
Use the attached image as the primary lil.troublr identity anchor. Preserve the same face geometry, eye spacing, cheek softness, mouth shape, beauty mark placement, hair density and silhouette, warm East Asian skin tone, and body proportion family. Preserve the same behavioral identity: asymmetric smile tendency, warm cheek movement, socially responsive gaze, cute mature Hong Kong local-girl energy, and realistic posture habits. Change only scene, outfit, camera, expression timing, and social moment. No face drift, no generic influencer face, no anime/doll face, no youth-coded styling.
```
