# V16 ANTI-FORMULA RESEARCH — VERIFICATION REPORT

**Date:** May 29, 2026  
**Engine:** lil.troublr V16  
**Status:** STEP 2 — VERIFY + EXTEND  
**Assessor:** Hermes Agent  

---

## EXECUTIVE SUMMARY

All 7 areas contain substantial research with good structure. **No area is a placeholder.** Each has:
- Token library with architectures
- Grammar/prompt format
- Anti-repetition rules
- HK-specific content

**Overall Verdict: 3 VERIFIED | 4 FLAGGED**

| Area | Verdict | Completeness | Critical Issue |
|------|---------|--------------|---------------|
| 01 Streetwear Diversity | FLAGGED | 8/10 | Missing mid-layer and CNY patterns |
| 02 Silhouette Variation | VERIFIED | 9/10 | — |
| 03 Camera Distance | FLAGGED | 8/10 | Group dynamics thin, prompt grammar ambiguous |
| 04 Emotional Rhythm | VERIFIED | 9/10 | — |
| 05 Accidental Sexiness | FLAGGED | 8/10 | Environmental causality incomplete |
| 06 AI Noise Reduction | VERIFIED | 9/10 | — |
| 07 Feed-Level Realism | FLAGGED | 8/10 | Photodump composition rules vague |

---

## Area 01: Streetwear Diversity

**Verdict: FLAGGED**

**Completeness:** 8/10  
**Consistency:** 9/10  
**Accuracy:** 7/10  
**Practicality:** 8/10  
**Novelty:** 8/10

### Issues

1. **Mid-layer concept missing**: Real HK girls wear 內層 (inner layer) as critical identity marker. Plain beige sleeveless top under oversized shirt = very common HK look. Not in architecture.

2. **CNY/X'mas dressing not addressed**: 年初一唔好笑住著新衣 (First day of CNY don't laugh at new clothes). Festive dressing patterns absent.

3. **Brand-as-identity token missing**: HK girls use brand tags as identity markers. izzone, A Pu,小眾品牌, Supreme copy, 淘寶 direct. Need [FAST_FASHION_BRAND] [LUXURY_REPLICATE] [VINTAGE_SHOP] tokens.

4. **運動服 (sportswear) category thin**: 運動套裝, 瑜伽服, 跑步背心. Real HK content大量運動風. Should be its own category.

5. **HK context gaps**: 
   - 凍奶茶後生女 (Milk tea girl) — oversized tee + track pants + sneakers
   - 宿生妹 (boarding school girl) — uniform variation, dorm life
   - 深圳shopping回来 (Shenzhen shopping hauls) — specific wardrobe from 淘寶

6. **Rhythm categories overlap with V15**: Some categories (GIRLY_CASUAL, PARTY_REFERENCE) feel like V15 concepts. Anti-formula should specifically call out what V15 did wrong here.

### Extensions Required

```markdown
### Category F: Inner Layer Systems (Critical Missing)

| Architecture | Description | Token |
|-------------|-------------|-------|
| F1: PLAIN_TANK_BLACK | Basic black tank, worn under sheer | [PLAIN_TANK_UNDER] |
| F2: SKIVVY_WHITE | White round-neck, visible collar | [VISIBLE_UNDERSHIRT] |
| F3: UNIQLO_HEATECH | Tech inner, thin functional | [FUNCTIONAL_INNER] |
| F4: STRAPLESS_CAMISOLE | Worn under low-back tops | [STRAPLESS_BASE] |

### Category G: Sports/Active Wear

| Architecture | Description | Token |
|-------------|-------------|-------|
| G1: SPORTS_SET_MATCH | Matching top + leggings | [MATCHING_SPORTS_SET] |
| G2: YOGA_PANTS_CROP | Cropped yoga pants + oversized tee | [YOGA_CROP_COMBO] |
| G3: RUNNING_VEST | Running vest + shorts + cap | [RUNNING_CASUAL] |
| G4: GYM_COMPLETE | Full gym outfit, post-workout | [GYM_COMPLETE] |

### HK Brand Identity Tokens

[FAST_FASHION_TAGGED] — brand tag visible (Uniqlo, ZARA)
[LUXURY_MINI_REPLICATE] — designer-inspired piece
[VINTAGE_MARKET_FIND] — 潮流廣場 or 女人街 purchase
[TAOBAO_DIRECT] — obvious Taobao item
[中古_VINTAGE] — second-hand store piece
```

### Anti-Formula Clarification

Current grammar is good but needs explicit note:
- **V15 did:** Oversized knit + tight bottom + same silhouette
- **V16 must:** Same category (tee) but DIFFERENT silhouette (fitted tee vs oversized tee ≠ same outfit). Repeat category not repeat architecture.

---

## Area 02: Silhouette Variation

**Verdict: VERIFIED**

**Completeness:** 9/10  
**Consistency:** 8/10  
**Accuracy:** 8/10  
**Practicality:** 8/10  
**Novelty:** 7/10

### Issues

1. **HK-specific postures missing**: 
   - MTR扶手桿倚靠 (leaning on MTR handrail) — one hand holding rail, body angle
   - 排隊時重心转移 (queue weight shift) — waiting in long line, hip shift
   - 蹲低睇嘢 (squat to look at something) — very common HK地面活動

2. **Exhaustion categories could add**: 
   - 中伏 (after being let down) — specific disappointment posture
   - OT後 (post-overtime) — exhausted from work

3. **Compression point CP_07 ambiguous**: "Shoulder blade prominence" is more body-type dependent than other points. Need clarification: this works for lean/athletic bodies, not all body types.

### Minor Extensions

```markdown
### Category F: HK Context Postures (Add to existing)

F1: MTR_HANDRAIL_LEAN
- One hand on rail, body tilted, hip shift
- Token: [MTR_RAIL_LEAN]

F2: QUEUE_WEIGHT_CYCLE
- Standing in line, shifting weight leg to leg
- Token: [QUEUE_WEIGHT_SHIFT]

F3: SQUAT_GROUND_HK
- Squatting on ground, common in street markets
- Token: [STREET_SQUAT_HK]
```

### Good Practices Found

- Physical cause clearly linked to posture ✓
- Compression points well documented ✓
- Anti-repetition rules clear and enforceable ✓
- Grammar complete ✓

---

## Area 03: Camera Distance Diversity

**Verdict: FLAGGED**

**Completeness:** 8/10  
**Consistency:** 8/10  
**Accuracy:** 7/10  
**Practicality:** 7/10  
**Novelty:** 7/10

### Issues

1. **Group dynamics thin**: Only 5 group types. Real HK feeds often show:
   - 4-5人 group (common for dinners)
   - 大合照 (big group photo) with all faces visible
   - Someone taking photo of other person (not selfie)
   - Photo bomber in background
   - 背影為主 (back view as main subject)

2. **HK framing situations limited**: 6 situations but missing:
   - 屋邨樓梯 (estate stairwell) — specific HK architecture framing
   - 天橋欄杆 (footbridge rail) — common HK vantage
   - 便利店玻璃 (convenience store glass reflection) — different from 7-11 windows
   - 的士後座 (taxi backseat) — interior car framing
   - 大學聯誼活動 (university orientation) — group framing

3. **Intimacy-distance matrix vague**: "FRIEND_DISTANCE (0.5-1.5m)" — this overlaps Level 3 and Level 4 boundaries. Prompt generation could produce ambiguous results.

4. **Awareness level grammar ambiguous**: "unaware_forgotten_aware_cooperating_performing" — how does this interact with shot_type P1-P5? Need explicit mapping.

5. **Distance category naming conflicts**: "THREE_QUARTER" is typically a pose term, not a distance term. Could cause confusion with Area 02.

### Extensions

```markdown
### Group Dynamics Expansion

| Type | Description | Token |
|------|-------------|-------|
| GROUP_DYNAMIC_4P | Four people, casual dinner setup | [GROUP_DINNER_4] |
| GROUP_LARGE_CELEBRATION | 6+ people, event photo | [LARGE_GROUP_EVENT] |
| PHOTOGRAPHER_CAPTURE | Someone else photographing subject | [SOMEONE_ELSE_PHOTO] |
| PHOTO_BOMB_BACKGROUND | Accidental person in background | [PHOTO_BOMB_HK] |
| BACK_VIEW_MAIN | Subject's back as primary subject | [BACK_VIEW_PRIMARY] |
| OVERHEARD_STRANGER | Random person in frame, not posed | [RANDOM_IN_FRAME] |

### HK-Specific Framing (Add)

| Situation | Framing | Token |
|-----------|---------|-------|
| 屋苑平台花園 | Estate podium garden, natural light | [ESTATE_FRAMING] |
| 行人天橋 | Footbridge, elevated view | [FOOTBRIDGE_WIDE] |
| 的士後座 | Taxi interior, rear seat view | [TAXI_REAR_SEAT] |
| 大學校園樓梯 | University stairwell, layered | [UNI_STAIRS] |
```

---

## Area 04: Emotional Rhythm Variation

**Verdict: VERIFIED**

**Completeness:** 9/10  
**Consistency:** 8/10  
**Accuracy:** 8/10  
**Practicality:** 8/10  
**Novelty:** 8/10

### Issues

1. **HK-specific emotional contexts thin**: Only 6 HK situations. Missing:
   - 考試後 (post-exam) — relief + exhaustion
   - 工時長 (long work hours) — drained
   - 屋企人被催婚 (family pressure to marry) — tension
   - 深圳購物被呃 (Shenzhen shopping cheated) — frustration
   - 失恋 (broken relationship) — mood
   - 直播睇緊張 (watching livestream, nervous)

2. **Emotion density percentages might conflict**: Rule 1 (every 5 images must have low energy) + Rule 2 (positive emotions ≤60%) could conflict in small samples. Need clarification on precedence.

3. **Combination rules slightly vague**: "[EXHAUSTED_LAYERED] + [SLEEPY_NOD]" — these ARE too similar but rule says "CANNOT_COMBINE" for "too similar" but research doesn't explain WHY they're too similar to combine.

### Minor Extensions

```markdown
### HK Emotional Context Expansion

| Situation | Emotional State | Token |
|-----------|-----------------|-------|
| Post-DSE exam | [RELIEF_EXHAUST] + [FREEING] | [DSE_RELEASE] |
| Long overtime work | [MENTAL_DRAIN] + [TUNNEL_VISION] | [OT_HEAVY] |
| Family dinner tension | [SUPPRESSED_IRRITATION] + [PASSIVE_FACE] | [FAMILY_DINNER_TENSE] |
| Shenzhen haggle fail | [DISAPPOINTED] + [FRUSTRATED_BITE_LIP] | [SHENZHEN_HAGGLE] |
| Post-breakup | [SAD_BUT_OKAY] + [NIGHTLIFE_LONELY] | [POST_BREAKUP] |
| Livestream shopping | [EXCITED_BUT_SHY] + [OVERSTIMULATED] | [LIVE_SHOPPING_NERVOUS] |
| Waiting for bf (late) | [MISSING_SOMEONE] + [SLIGHT_IRRITATION] | [WAITING_BF_LATE] |
```

---

## Area 05: Accidental Sexiness

**Verdict: FLAGGED**

**Completeness:** 8/10  
**Consistency:** 8/10  
**Accuracy:** 8/10  
**Practicality:** 7/10  
**Novelty:** 8/10

### Issues

1. **Physical causality chain incomplete**: The grammar shows [physical_cause] → [clothing_response] → [resulting_exposure] but doesn't address intermediate steps. Example: reaching up (cause) → tee rises (response) → midriff exposed (exposure) — but what about the BREATH moment when chest compresses?

2. **Environmental causality HK-context weak**: Missing:
   - 冷氣機風 (AC unit direct blast) — fabric movement from wind
   - 暴曬後入商場 (hot to cold transition) — goosebumps, fabric shift
   - 濕笠笠夏天 (humid summer) — sweat + fabric cling combo
   - 暴雨後 (post-rain) — wet fabric + wind

3. **"Forbidden patterns" list incomplete**: Missing:
   - Subject holding exposure in place (hand on shirt to keep it up)
   - Subject actively creating the cause (leaning intentionally)
   - Subject's gaze returning to camera after exposure

4. **Category C (Fabric/Clothing) duplicates Area 02**: C4 "FABRIC_GAP_SKIN" overlaps with CP_05 "NECK_BASE_EXPOSED" and CP_04 "UNDERARM_EXPOSED". Need clearer boundary between accidental clothing behavior and structured compression points.

5. **Grammar has redundancy**: [accidental_level] has 3 levels but then "environmental_accident" is also used. Need consistent terminology.

### Extensions

```markdown
### HK Environmental Accidental (Add to E)

E7: AC_UNIT_DIRECT_BLOW
- Standing directly in AC wind
- Fabric moves, shifts position
- Token: [AC_WIND_SHIFT]

E8: HOT_COLD_TRANSITION
- Entering AC building from heat
- Goosebumps + fabric adjustment
- Token: [HEAT_COLD_TRANSITION]

E9: HUMID_SWEAT_CLING
- Humid day, light fabric
- Sweat + fabric = body visible
- Token: [HUMID_BODY_CLING]

E10: POST_RAIN_WET
- Rain on fabric
- Water tracks + transparency shift
- Token: [WET_FABRIC_HK]
```

---

## Area 06: AI Noise Reduction

**Verdict: VERIFIED**

**Completeness:** 9/10  
**Consistency:** 9/10  
**Accuracy:** 9/10  
**Practicality:** 8/10  
**Novelty:** 7/10

### Issues

1. **HK-specific optical situations thin**: 5 scenarios but missing:
   - 西多士光 (fluorescent + steam from food) — tea restaurant special
   - 迪迪尼尼 (theme park night) — flash + darkness
   - 天台夜景 (rooftop night view) — city lights + soft
   - 巴士上層 (bus upper deck) — motion blur + window

2. **Token naming inconsistency**: Some use SENSOR_SMOOTH_SKIN (sensor characteristic) but WIDE_APERTURE_SOFT (optical softness). Doesn't follow consistent naming convention.

3. **Detail hierarchy rule "ANTI-AI RULE: If background is as sharp as face = AI" is slightly wrong**: Modern smartphone cameras can achieve very sharp backgrounds in Portrait mode. This rule should be "If background has AI-like uniform sharpness (no lens falloff) = AI."

### Minor Extensions

```markdown
### HK Optical Situations Expansion

| Situation | Optical Combo | Token |
|-----------|--------------|-------|
| 茶餐廳油煙 | [LOW_LIGHT_SOFT] + greasy steam | [TEA_REST_STEAM] |
| 主題公園煙火 | [FLASH_SMOOTH] + dark + sparkles | [FIREWORKS_OPTICAL] |
| 天台夜景 | [TELEPHOTO_SOFT] + city lights | [ROOFTOP_NIGHT_OPTICAL] |
| 巴士上層 | [MOTION_BLUR_SOFT] + window frame | [BUS_INTERIOR_OPTICAL] |
| 旺角行人隧道 | [FLUORESCENT_POLLUTION] + footsteps | [MONGKOK_TUNNEL_OPTICAL] |
```

---

## Area 07: Feed-Level Realism

**Verdict: FLAGGED**

**Completeness:** 9/10  
**Consistency:** 8/10  
**Accuracy:** 8/10  
**Practicality:** 8/10  
**Novelty:** 8/10

### Issues

1. **Photodump composition rules vague**: "2-3 good + 1-2 filler" is subjective. What defines "good"? How do you enforce "mix quality" in generation? Need clearer metrics.

2. **PHOTODUMP_TOKEN lacks structure**: Should have sub-tokens for:
   - [PHOTODUMP_CLOSE_MEDIUM_WIDE] — distance variation within session
   - [PHOTODUMP_SAME_OUTFIT] — same clothes different angles
   - [PHOTODUMP_MIXED_QUALITY] — quality variation

3. **Filler types incomplete**: Missing HK-specific fillers:
   - 垃圾徵費膠袋 (garbage bag with charges visible) — very HK daily
   - 排隊 receipt (queue ticket) — MTR/minivan
   - 八達通升值 (Octopus reload receipt) — daily life
   - 外賣包裝 (takeaway packaging) — food delivery culture

4. **Anti-repetition rule "No bad photos = AI signal" needs nuance**: V16 should distinguish between "accidental bad" (good — realism) and "consistently low quality" (bad — looks like low-skill generation). Rule should be: variation in quality, not just presence of bad photos.

5. **HK Feed Patterns section thin**: Only 6 patterns. Missing:
   - 樓上cafe系列 (upstairs cafe series) — HK's 樓上店 culture
   - 深圳地鐵系列 (Shenzhen metro) — cross-border content
   - 工作日常vlog型 (work day vlog style) — office content
   - 同一人唔同日子 (same person different days) — lifecycle content

6. **WEEK_ARCHITECTURE may be too prescriptive**: Real feeds don't follow "1 hero post" pattern consistently. Some KOLs do 3-4 hero posts in a week, then nothing for days. Flexibility needed.

### Extensions

```markdown
### Photodump Session Structure (Clarify)

PHOTODUMP_SESSION now has sub-types:

[PHOTODUMP_SAME_OUTFIT] — 3-4 shots, same clothes, different activities
[PHOTODUMP_LOCATION] — 3-4 shots, same location, different angles
[PHOTODUMP_MOMENT] — sequential moments, like mini-story
[PHOTODUMP_MIXED] — random selection, like phone dump

Rules:
- Within session: at least 1 distance change
- Within session: at least 1 "lower quality" shot
- Within session: max 1 "hero" quality shot
```

### HK Filler Expansion

| Type | Description | Token |
|------|-------------|-------|
| OCTOPUS_RECEIPT | Octopus reload receipt | [OCTOPUS_RECEIPT] |
| GARBAGE_BAG_TAG | Trash bag charge receipt | [GARBAGE_TAG] |
| TAKEAWAY_BOX | Delivery packaging, open | [TAKEAWAY_LUNCH] |
| QUEUE_TICKET | Number ticket from queue | [QUEUE_TICKET] |
| PARKING_TICKET | Parking receipt on dashboard | [PARKING_RECEIPT] |
```

---

## Cross-Area Issues

### 1. Token Naming Convention Inconsistent

Across 7 files, tokens use different naming patterns:
- Area 01: UPPERCASE_WITH_UNDERSCORE (FADED_GRAPHIC_TEE)
- Area 02: UPPERCASE_WITH_UNDERSCORE (ONE_LEG_SUPPORT)
- Area 05: UPPERCASE_WITH_UNDERSCORE (SHIRT_RISE_MOVEMENT)
- Area 06: MIXED (WIDE_APERTURE_SOFT vs SENSOR_SMOOTH_SKIN)

**Recommendation:** Standardize all tokens as [CATEGORY_SUBTYPE_DETAIL]. Every token should be parseable by machine.

### 2. Grammar Syntax Conflicts

Area 01 grammar: `[tee_architecture]_worn_with_[bottoms_type]`  
Area 02 grammar: `[primary_posture]:[A1-A7/B1-B7/C1-C8/D1-D6/E1-E7]_`  
Area 05 grammar: `[physical_cause]:[movement_posture_environment]_`

These use different delimiters (_ vs : vs -). Should standardize on one syntax.

### 3. Anti-Repetition Rules Don't Communicate

Each area has its own anti-rep rules, but there's no cross-area awareness. If Area 01 uses tee architecture A3 and Area 02 uses posture C5 in the same image, is there a conflict?

**Recommendation:** Add cross-area compatibility matrix showing which tokens from different areas can coexist in same image without creating formula.

### 4. HK Context Depth Varies

Area 04 has 6 HK contexts, Area 07 has 6, Area 06 has 5, but Area 03 has only 6 (and they're thin), Area 05 has none in main body (only in extension).

**Recommendation:** Every area should have minimum 8 HK-specific tokens/contexts.

---

## Recommendations

### Priority 1: Fix FLAGGED Areas

1. **Area 01**: Add mid-layer category, sportswear category, HK brand identity tokens
2. **Area 03**: Expand group dynamics, clarify intimacy-distance boundaries, fix naming conflict (THREE_QUARTER)
3. **Area 05**: Complete environmental causality, add HK-specific environmental causes, fix grammar redundancy
4. **Area 07**: Clarify photodump rules, expand HK fillers, add photodump sub-types

### Priority 2: Cross-Area Standardization

1. Standardize token naming convention
2. Standardize grammar syntax
3. Add cross-area compatibility matrix
4. Create unified anti-formula enforcement layer

### Priority 3: Novelty Enhancement

Areas need to explicitly call out what V15 did wrong and how V16 fixes it. Without this, anti-formula research risks being "more of the same with extra tokens."

---

## Final Verdict by Area

| Area | Verdict | Must-Fix |
|------|---------|----------|
| 01 Streetwear Diversity | FLAGGED | Add mid-layer + sportswear + brand identity |
| 02 Silhouette Variation | VERIFIED | Minor HK posture additions only |
| 03 Camera Distance | FLAGGED | Expand group dynamics + fix naming |
| 04 Emotional Rhythm | VERIFIED | Minor HK emotional context additions |
| 05 Accidental Sexiness | FLAGGED | Complete environmental causality |
| 06 AI Noise Reduction | VERIFIED | Minor HK optical situation additions |
| 07 Feed-Level Realism | FLAGGED | Clarify photodump + expand HK fillers |

**Overall Assessment:** Research foundation is strong. No placeholders. Structure is solid. Execution needs tightening in 4 flagged areas before implementation.

---

*Report generated: May 29, 2026*  
*Next step: Apply fixes to FLAGGED areas, then move to implementation phase.*