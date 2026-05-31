# ENGINE_V15_POST_SWIM_SYSTEM.md

## V15 Core Module — Wet Hair Mechanics + Post-Swim Behavioral
### AREA: 06 (Wet Hair Post-Swim) | Status: READY FOR INTEGRATION

---

## PURPOSE

Post-swim appearance carries distinctive realism markers: wet tangled strands, chlorine-affected dryness, reduced alertness, relaxed musculature, and genuine tiredness. This "just-swam" state combines authenticity and desirability through physics-first wet hair behavior, fatigue sexiness, and post-swim behavioral mechanics.

---

## KEY CONCEPTS

**Wet Hair Physics**: Hydration weight, tangle topology, chlorine/salt interaction

**Fatigue Sexiness**: Sleepy eyes, tired smile, exhausted posture, relaxed gait

**Post-Swim Behavioral**: Uncoordinated grace, water toss, cold shiver, towel handling

---

## WET_HAIR_MECHANICS

**HYDRATION_WEIGHT**
```
Wet hair weighs 20-40% more than dry
Strand diameter increases 15-25%
Gravity creates lengthward elongation
Visual: Longer appearance, reduced volume at crown
Token: [WET_HEAVY] [STRAND_EXPANDED] [GRAVITY_PULL]
```

**TANGLE_TOPOLOGY**
```
Post-swim tangles: irregular, clumped sections
Less "styled" than deliberate teased wet-look
Random knot formations at nape, behind ears
Token: [UNTANGLED_CLUMP] [IRREGULAR_KNOT] [POST_SWIM_TANGLE]
```

**CHLORINE_INTERACTION**
```
Chlorine binds to hair cuticle, removes natural oils
Creates: dullness, slight greenish tint (blondes), rough texture
Hair becomes: porous, absorbent, matte finish
Token: [CHLORINE_MATTE] [POROUS_TEXTURE] [CUTICLE_STRIPPED]
```

**SEA_SALT_INTERACTION** (alternative)
```
Salt crystallizes on strand surface
Creates: crunchy texture, enhanced wave definition
Slightly lighter color (bleaching effect)
Token: [SALT_CRYSTAL] [CRUNCHY_TEXTURE] [WAVE_ENHANCED]
```

**WATER_DRIP_SIGNATURE**
```
Isolated droplets on nape, shoulders, collarbone
Beading pattern: irregular, gravity-determined
Drip rate: immediate post-swim (heavy to light over 5-15 min)
Token: [WATER_DRIP] [DRIP_TRICKLE] [COLLARBONE_DROPS]
```

---

## FATIGUE_SEXINESS_MODULE

**SLEEPY_EYES**
```
Pupils slightly dilated (post-exertion relaxation)
Eyelids heavy, 5-15% more closed than alert state
Sclera shows slight redness (capillary flush)
Token: [SLEEPY_HEAVY_LID] [DILATED_PUPIL] [CAPILLARY_FLUSH]
```

**TIRED_SMILE**
```
Genuine smile with reduced muscle tension
Slightly asymmetric (natural fatigue asymmetry)
Corners of mouth 2-5° lower than full-energy smile
Accompanied by cheek rise, softened eye crinkle
Token: [RELAXED_SMILE] [ASYMMETRIC_LOWER] [SOFT_CHEEK]
```

**EXHAUSTED_POSTURE**
```
Shoulder elevation reduced (dropped shoulders)
Upper spine posterior curve (slight slouch)
Neck tilt: chin slightly elevated, throat exposed
Hip shift: weight distribution more relaxed, uneven
Token: [DROPPED_SHOULDERS] [SLIGHT_SLOUCH] [NAPE_EXPOSED]
```

**RELAXED_GAIT_AND_MOVEMENT**
```
Arms slightly abducted from body
Steps slower, less bouncy
Movement efficiency over style
Token: [RELAXED_GAIT] [SLOW_STEPS] [ARM_ABDUCTED]
```

**FLUSHED_SKIN**
```
Capillary dilation from exertion + cool-down
Cheeks: warmer tone (0.5-2 skin tone shades rosy)
Neck/chest: visible flush gradient
Skin texture: slightly dewy (residual moisture)
Token: [CAPILLARY_FLUSH] [WARM_CHEEKS] [DEWY_TEXTURE]
```

---

## FATIGUE_SEXINESS_BEHAVIORAL_MECHANICS (EXTENDED)

**HEAVY_LID_DROOP**
```
Direct fixation requires more effort post-swim
Gaze becomes slightly unfocused / distant
Eye contact breaks more frequently (natural, not shy)
Blink rate increases 10-20% (fatigue marker)
Token: [UNFOCUSED_GAZE] [BLINK_RATE_UP] [CONTACT_BREAK]
```

**THROAT_EXPOSURE_TILT**
```
Chin lifts slightly to compensate for heavy eyelids
Exposes submental area and throat
Creates vulnerability signal (relaxation + fatigue)
Token: [CHIN_LIFT] [THROAT_OPEN] [VULNERABILITY_SIGNAL]
```

**WEIGHT_SHIFT_RELAXATION**
```
Standing: hip sways, one leg relaxed, slight lean
Sitting: spine curves, head tilts back against support
Creates S-curve silhouette vs alert straight line
Token: [HIP_SWAY] [SPINE_CURVE] [DELIBERATE_MOVEMENT]
```

**ARM_HEAVINESS**
```
Arms hang with reduced muscle tone
Hands rest on surfaces (not actively posed)
Fingers slightly curled (relaxed flexion)
Elbows rest on tables, knees, or own shoulders
Token: [ARM_HEAVY] [HAND_REST] [RELAXED_FLEXION] [ELBOW_REST]
```

**SHOULDER_RELEASE**
```
Trapezius muscles visibly released
Shoulders drop 1-3cm from alert position
Creates elongated neck appearance
Shoulder line slopes toward viewer
Token: [SHOULDER_RELEASE] [TRAPEZIUS_DOWN] [NECK_LENGTHEN]
```

**BREATH_RHYTHM_VISUAL**
```
Post-swim breath rate still elevated
Chest rises/falls more visible than resting
Creates subtle movement even in static poses
Accompanied by slightly parted lips
Token: [BREATH_VISIBLE] [CHEST_RISE] [SLIGHTLY_PARTED]
```

**LAZY_EYE_RUB**
```
Back of hand rubs eye area (not dainty, functional)
Rub is slow, eyes close during rub
Accompanied by slight squint release
Token: [EYE_RUB] [SLOW_RUB] [SQUINT_RELEASE]
```

**MOUTH_GAPE**
```
Jaw relaxes, mouth slightly open
Not dramatic, just slack
Tongue may press against teeth
Creates vacant, unfocused, "just swam" expression
Token: [JAW_SLACK] [MOUTH_GAPE] [VACANT_EXPRESSION]
```

**PROVOCATIVE_LAZINESS**
```
Post-swim fatigue removes performance anxiety
Actions become less coordinated, more honest
Sexual availability signals increase (unconscious)
Eye contact is slower, more deliberate when it occurs
Token: [NO_PERFORMANCE] [HONEST_SIGNAL] [LAZY_SEXUAL]
```

---

## POST_SWIM_BEHAVIORAL_MECHANICS (EXTENDED)

**UNCOORDINATED_GRACE**
```
Post-swim movement is genuine-fresh (not staged)
Hair adjustment attempts: multiple small touches
Expression: neutral with micro-flinch at cold air
Token: [FRESH_WET] [MULTI_TOUCH_HAIR] [COLD_FLICH]
```

**WATER_TOSS_MECHANICS**
```
Head toss to clear eyes: incomplete, water still in hair
Animation: slower than dry hair flip, follows gravity briefly
Ends with slight head shake, residual drips
Token: [INCOMPLETE_TOSS] [GRAVITY_FOLLOW] [RESIDUAL_DRIP]
```

**CHLORINE_SNIFF_RESPONSE**
```
Slight nose wrinkling at chlorine smell
Occurs naturally, not performed
Small nose scrunch, quick release
Token: [CHLORINE_WRINKLE] [NATURAL_NOSE_SCRUNCH]
```

**SKIN_PRESS_RESPONSE**
```
Residual wetness on skin invites immediate wipe
Hand goes to cheek, temple, or neck
Quick, efficient, not pose-like
Token: [WET_WIPE_REFLEX] [EFFICIENT_HAND] [CHEEK_WIPE]
```

**TOWEL_HANDLING**
```
Pat-dry motion (not rub) for hair
Towel turban attempt: often loose, slides
Hand holds towel in place (no clip/bands)
Token: [PAT_DRY] [SLIDING_TURBAN] [HAND_HOLD]
```

**CHLORINE_SUNSCREEN_STICKY_RESIDUE**
```
Combination creates tacky texture
Skin feels "gummy" when dry
Especially visible on shoulders, upper arms, back of neck
Touch response: fingers stick briefly when pressing
Token: [STICKY_RESIDUE] [CHLORINE_SPF] [TACKY_TEXTURE]
Note: Texture audible when fabric slides against skin
```

**POST_SWIM_GOOSEBUMPS**
```
Cool water triggers piloerection response
Visible on shoulders, upper arms, sides of torso
Accompanies slight shivering (not always visible)
Creates skin texture detail (pores + goosebumps together)
Timing: immediate post-swim, reduces after 5-10 min
Token: [GOOSEBUMPS] [PILOERECTION] [COOL_RESPONSE]
```

**HAIR_STUCK_TO_POSTERIOR_CERVICAL**
```
Wet hair adheres to back of neck completely
No air gap between hair and skin
Creates visible hair strand patterns pressed into skin
Water transfer visible: skin appears darker where wet
Token: [HAIR_STUCK_BACK] [CERVICAL_WET] [STRAND_PRESS]
```

**TOWEL_MARK_ON_SHOULDER**
```
Sitting on damp towel creates impressions
Visible rectangular pattern lines on shoulder blade
Pattern: woven towel texture transfer
Fades as skin dries or towel moved
Token: [TOWEL_IMPRINT] [SHOULDER_MARK] [DAMP_SITTING]
```

**EXHAUSTED_BEACH_CHAIR_SITTING**
```
Body weight fully deposited in plastic chair
Arms hang off sides, head tilts back
Legs spread wider than alert sitting
Chair creaks with each micro-movement
Token: [DEPOSITED_SITTING] [CHAIR_CREEK] [ARM_HANG] [HEAD_BACK]
```

**POST_SWIM_MIRROR_SELFIE_ENERGY**
```
Standing at mirror, slight lean toward reflection
Hand holds towel at chest (not dropped)
Eyes checking hair status, not performing
Slight exhale-fog on mirror surface
Token: [MIRROR_ASSESS] [LEAN_REFLECT] [TOWEL_HOLD] [FOG_BREATH]
```

**MELTED_SUNSCREEN_RESIDUE**
```
SPF melts from body heat + sun exposure
Creates white cast streaks on shoulders, collarbone
Texture slightly chalky when touched
Combined with sweat creates milky drips
Token: [SPF_MELT] [WHITE_CAST] [CHALKY_RESIDUE] [MILKY_DRIP]
```

**WATER_DRIPPING_FROM_HAIR_ENDS**
```
Gravity pulls remaining water to lowest points
Drip rate intermittent, 1 drop per 3-10 seconds
Location hair tips especially at back and sides
Creates dark wet spots on towel or floor beneath
Token: [DRIP_FALL] [HAIR_TIP_DROP] [INTERMITTENT_DRIP]
```

**POST_SWIM_COLD_SHIVER**
```
Body temperature regulation response
Visible small tremor in shoulders, arms
Occurs immediately post-swim after leaving water
Duration 30-60 seconds of visible shivering
May be suppressed by sunlight exposure
Token: [COLD_SHIVER] [BODY_TREMOR] [THERMAL_REGULATE]
```

**CHLORINE_HAND_SMELL**
```
Distinctive chemical odor on hands
Triggers smell-specific micro-expression
Nose scrunch + slight upper lip lift
Token: [CHLORINE_ODOR] [HAND_SMELL] [CHEMICAL_SCRUNCH]
```

**BEACH_SAND_IN_BIKINI_LINE**
```
Sand adheres to wet skin in intimate areas
Creates gritty texture in bikini edges
Especially bikini bottom lines, underband
Token: [SAND_STICK] [WET_GRIT] [BIKINI_ADHERE]
```

**POST_SWIM_LIPS_CHEKS_SALT**
```
Salt water residue creates taste response
Tongue licks lips, slight lip smack
Creates glistening momentary
Token: [SALT_LICK] [LIP_SMACK] [TASTE_RESPONSE]
```

**INCOMPLETE_TOWEL_WRAP**
```
Towel gap reveals midriff or hip
Wrapping is rushed, not adjusted
One side higher than other
Token: [TOWEL_GAP] [RUSHED_WRAP] [ASYMMETRIC_TOWEL]
```

---

## WET_HAIR_FRAMING_SYSTEM

**NAPE_MOISTURE_DETAIL**
```
Water pools in hairline at nape
Drip pattern: single channel down center OR spray pattern scattered
Token: [NAPE_DRIP] [CERVICAL_POOL] [WATER_COLLECT]
```

**SHOULDER_WATER_PATTERN**
```
Shoulder plane retains pooled water
Gravity creates trailing droplets toward deltoid
Shirt neckline shows wet front border
Token: [SHOULDER_POOL] [DELTOID_DRIP] [WET_NECKLINE]
```

**POSTERIOR_CERVICAL_HAIR_ADHESION**
```
Wet hair sticks to back of neck
Creates direct view of nape, hairline, cervical vertebrae bumps
Hair separates in strands not uniform coverage
Small water beads visible between hair strands on skin
Token: [CERVICAL_ADHERE] [NAPE_BARE] [STRAND_SEPARATION]
Note: Highly intimate — reveals true hairline and neck
```

**UPPER_BACK_HAIR_DRAPE**
```
Wet hair falls across upper back
Strand groups cling to trapezius muscles
Water drips along spine path
Creates cool sensation visible in goosebump response
Token: [BACK_DRAPE] [TRAPEZIUS_CLING] [SPINE_DRIP]
```

---

## TOKEN LIBRARY

```
WET HAIR:
[WET_HEAVY] [STRAND_EXPANDED] [GRAVITY_PULL]
[UNTANGLED_CLUMP] [IRREGULAR_KNOT] [POST_SWIM_TANGLE]
[CHLORINE_MATTE] [POROUS_TEXTURE] [CUTICLE_STRIPPED]
[SALT_CRYSTAL] [CRUNCHY_TEXTURE] [WAVE_ENHANCED]
[WATER_DRIP] [DRIP_TRICKLE] [COLLARBONE_DROPS]

FATIGUE SEXINESS:
[SLEEPY_HEAVY_LID] [DILATED_PUPIL] [CAPILLARY_FLUSH]
[RELAXED_SMILE] [ASYMMETRIC_LOWER] [SOFT_CHEEK]
[DROPPED_SHOULDERS] [SLIGHT_SLOUCH] [NAPE_EXPOSED]
[RELAXED_GAIT] [SLOW_STEPS] [ARM_ABDUCTED]
[CAPILLARY_FLUSH] [WARM_CHEEKS] [DEWY_TEXTURE]

EXTENDED FATIGUE:
[UNFOCUSED_GAZE] [BLINK_RATE_UP] [CONTACT_BREAK]
[CHIN_LIFT] [THROAT_OPEN] [VULNERABILITY_SIGNAL]
[HIP_SWAY] [SPINE_CURVE] [DELIBERATE_MOVEMENT]
[ARM_HEAVY] [HAND_REST] [RELAXED_FLEXION] [ELBOW_REST]
[SHOULDER_RELEASE] [TRAPEZIUS_DOWN] [NECK_LENGTHEN]
[BREATH_VISIBLE] [CHEST_RISE] [SLIGHTLY_PARTED]
[EYE_RUB] [SLOW_RUB] [SQUINT_RELEASE]
[JAW_SLACK] [MOUTH_GAPE] [VACANT_EXPRESSION]
[NO_PERFORMANCE] [HONEST_SIGNAL] [LAZY_SEXUAL]

POST-SWIM BEHAVIOR:
[FRESH_WET] [MULTI_TOUCH_HAIR] [COLD_FLICH]
[INCOMPLETE_TOSS] [GRAVITY_FOLLOW] [RESIDUAL_DRIP]
[CHLORINE_WRINKLE] [NATURAL_NOSE_SCRUNCH]
[WET_WIPE_REFLEX] [EFFICIENT_HAND] [CHEEK_WIPE]
[PAT_DRY] [SLIDING_TURBAN] [HAND_HOLD]
[STICKY_RESIDUE] [CHLORINE_SPF] [TACKY_TEXTURE]
[GOOSEBUMPS] [PILOERECTION] [COOL_RESPONSE]
[HAIR_STUCK_BACK] [CERVICAL_WET] [STRAND_PRESS]
[TOWEL_IMPRINT] [SHOULDER_MARK] [DAMP_SITTING]
[DEPOSITED_SITTING] [CHAIR_CREEK] [ARM_HANG] [HEAD_BACK]
[MIRROR_ASSESS] [LEAN_REFLECT] [TOWEL_HOLD] [FOG_BREATH]
[SPF_MELT] [WHITE_CAST] [CHALKY_RESIDUE] [MILKY_DRIP]
[DRIP_FALL] [HAIR_TIP_DROP] [INTERMITTENT_DRIP]
[COLD_SHIVER] [BODY_TREMOR] [THERMAL_REGULATE]
[CHLORINE_ODOR] [HAND_SMELL] [CHEMICAL_SCRUNCH]
[SAND_STICK] [WET_GRIT] [BIKINI_ADHERE]
[SALT_LICK] [LIP_SMACK] [TASTE_RESPONSE]
[TOWEL_GAP] [RUSHED_WRAP] [ASYMMETRIC_TOWEL]

WET HAIR FRAMING:
[NAPE_DRIP] [CERVICAL_POOL] [WATER_COLLECT]
[SHOULDER_POOL] [DELTOID_DRIP] [WET_NECKLINE]
[CERVICAL_ADHERE] [NAPE_BARE] [STRAND_SEPARATION]
[BACK_DRAPE] [TRAPEZIUS_CLING] [SPINE_DRIP]
```

---

*V15 Module: ENGINE_V15_POST_SWIM_SYSTEM.md*
*Status: READY FOR INTEGRATION*
*Cross-ref: ENGINE_V15_SMARTPHONE_GEOMETRY_SYSTEM (humidity affects distortion)*
