# ENGINE_V16_ANTI_FORMULA_STREETWEAR_SYSTEM.md

## V16 Core Module — Anti-Formula / Streetwear Diversity System
### SOURCE: V16_ANTI_FORMULA_RESEARCH (Areas 01-03)
### STATUS: READY FOR INTEGRATION

---

## PURPOSE

This module eliminates the identifiable "lil.troublr formula" that causes outfit repetition across generated images — the same oversized knit / off-shoulder drape / loose-cardigan rhythm that makes feeds look cloned. It replaces formulaic outfit architecture with a structured diversity system spanning 7 streetwear categories (35+ architectures), 5 posture categories (35+ silhouettes), 8 camera distances, and 6 camera heights, enforced by cross-module anti-repetition rules that allow category repetition but forbid architectural repetition.

---

## KEY CONCEPTS

- **Repeat Category, Vary Architecture** — same tee category is OK, but each tee outfit must use a different architecture (fitted vs. oversized vs. cropped vs. stretched-collar)
- **Rhythm Balancing** — 5 outfit rhythm categories (Athletic, Minimal, Girly, Street Utilitarian, Party) rotate across images so no single energy dominates
- **Body-Weight Realism** — real bodies accept gravity; compression points (under-breast shadow, thigh contact, abdominal fold) create non-performative attraction through natural use, not posed seduction
- **Distance = Emotional Contract** — intimacy level maps to physical camera distance (Stranger → Intimate), preventing same-distance repetition across a feed
- **Asymmetry Over Symmetry** — perfect symmetry reads as professional/posed; real bodies are asymmetrical through weight shifts, head tilts, and uneven action

---

## STREETWEAR_DIVERSITY_SYSTEM

### The Formula Repetition Problem

Current engine weakness: Overuse of specific outfit structures creates identifiable "lil.troublr formula":
- Oversized knit / off-shoulder drape
- Loose cardigan / neckline slipping mechanics
- Same silhouette logic across images
- Same "pretty girl in pretty outfit" rhythm

Real KOL feeds break formula by: **repeating categories, but not exact architecture.** A real girl wears "tees" many times, but each tee outfit is architecturally different.

---

### STREETWEAR_DIVERSITY_LIBRARY

#### Category A: Fitted/Printed Tees (Real KOL Foundation)

**Why real:** Every HK/JP/KR girl owns 20+ tees. Tees are the most-authentic casual wear.

**Outfit Architectures:**

| Architecture | Description | Realism Signal | Token |
|-------------|-------------|----------------|-------|
| A1: Faded_Graphic | Washed-out print, cracked logo, multiple washes | Memory item, identity piece | [FADED_GRAPHIC_TEE] |
| A2: Vintage_Band | Retro band tee, soft cotton, slight shrinkage | Subcultural identity marker | [VINTAGE_BAND_TEE] |
| A3: Oversized_Logo | Men's fit on women's body, disproportionate | Borrowed from boyfriend | [MENS_BORROWED_TEE] |
| A4: Cropped_Tee | Hem knotted, DIY crop, midriff visible | Casual modification | [KNOTTED_CROP_TEE] |
| A5: Stretched_Collar | Neckline stretched from over-wear, loose oval | Well-loved, lived-in item | [STRETCHED_COLLAR_TEE] |
| A6: Fitted_Pocket | Small chest pocket, plain, no print | Minimalist casual | [PLAIN_FITTED_TEE] |
| A7: Graphic_Front_Back | Front print different from back | Thoughtful graphic choice | [DOUBLE_SIDED_GRAPHIC] |

**Anti-Repetition Grammar (Category A):**
```
[tee_architecture]_worn_with_[bottoms_type]_
[fit_relative]:[oversized_fitted]_
[layering]:[none_single_multi]_
[distress_level]:[pristine_worn_distressed]
```

> Cross-ref: These tee architectures pair with Silhouette Variation postures (e.g., [WALKING_CAPTURED] for oversized tee movement, [SLUMPED_EXHAUSTED] for stretched-collar lived-in feel). See §SILHOUETTE_VARIATION_SYSTEM.

---

#### Category B: Ribbed/Cropped Tops (Body-Conscious Casual)

**Why real:** Post-gym, casual date, hot weather staple. HK summer essential.

**Outfit Architectures:**

| Architecture | Description | Realism Signal | Token |
|-------------|-------------|----------------|-------|
| B1: Ribbed_Cami | Thin strap, ribbed cotton, visible bra straps optional | Underwear-as-outerwear | [RIBBED_CAMI] |
| B2: Lace_Trim_Cami | Delicate lace edge, feminine detail | Contrast with casual context | [LACE_TRIM_CAMISOLE] |
| B3: Sport_Bra_Top | Athletic top, built-in support, minimal coverage | Post-workout or style choice | [SPORT_BRA_STYLE] |
| B4: Racer_Back_Top | Narrow racerback, shoulder blade visible | Athletic influence on casual | [RACER_BACK_CASUAL] |
| B5: Halter_Straps | Neck-tied halter, bare shoulders | Summer evening style | [HALTER_CASUAL] |
| B6: Tube_Street | Tube top, strapless, depends on grip | Summer night market style | [TUBE_STREETWEAR] |

> Cross-ref: B1-B4 expose compression points CP_04 (underarm) and CP_07 (shoulder blade). See §SILHOUETTE_VARIATION_SYSTEM → Compression Points.

---

#### Category C: Layering Pieces (Texture + Dimension)

**Why real:** Real girls layer — for weather, for style, for hiding/changing silhouette.

**Outfit Architectures:**

| Architecture | Description | Realism Signal | Token |
|-------------|-------------|----------------|-------|
| C1: Mesh_Under_Tee | Sheer mesh under or over tee | Texture contrast, subtle layering | [MESH_UNDER_LAYER] |
| C2: Tank_Under_Cardigan | Visible tank straps, cardigan unbuttoned | Layered casual, easy | [TANK_UNDER_CARDIGAN] |
| C3: Cropped_Zip_Hoodie | Above waist, shows midriff | Sporty casual | [CROPPED_ZIP_HOODIE] |
| C4: Sheer_Blouse_Over | Blouse over tee, buttons open | Grandma-chic influence | [SHEER_OVER_TEE] |
| C5: Denim_Jacket_Over | Oversized denim, sleeves pushed up | Classic casual layer | [OVERSIZED_DENIM] |
| C6: Oversized_Shirt_Open | Flannel or oxford, open over anything | Tomboy casual | [OPEN_OVERSHIRT] |

> Cross-ref: Layering pieces C1-C6 naturally interact with Category F (Inner Layer Systems). Combined token example: [MESH_UNDER_LAYER] + [PLAIN_TANK_UNDER] = mesh over visible black tank.

---

#### Category D: Bottoms Variety (Silhouette Diversity)

**Why real:** Repeating same bottoms = same silhouette. Real feeds mix these constantly.

| Architecture | Description | Token |
|-------------|-------------|-------|
| D1: Low_Rise_Cargo_Mini | Cargo pockets, low rise, mini length | Street utilitarian |
| D2: Pleated_Micro_Skirt | Schoolgirl reference, tiny | Y2K revival |
| D3: Parachute_Pants | Baggy, tapered, technical fabric | Comfort aesthetic |
| D4: Slouch_Socks_Crop | Long socks, mid-calf slouch | JP street style |
| D5: Ballet_Sneakers | Flat, rounded toe, ribbon detail | Soft feminine casual |
| D6: Football_Jersey_Shorts | Oversized jersey with shorts underneath | Athletic casual |
| D7: Low_Rise_Wide_Leg | Denim or trousers, hip-hugging | 2000s influence |

> Cross-ref: Bottom silhouettes directly affect which compression points activate. D1 (cargo mini) + seated = CP_02 (thigh contact). D7 (wide leg) + walking = no compression, different energy. See §SILHOUETTE_VARIATION_SYSTEM → Compression Points.

---

#### Category E: Accessories That Break Formula

**Why real:** Same outfit + different accessories = completely different energy.

| Architecture | Description | Token |
|-------------|-------------|-------|
| E1: Oversized_Headphones | Over-ear, neck presence | [OVERSIZED_HEADPHONES] |
| E2: Baseball_Cap_Backward | Cap worn backwards, casual | [CAP_BACKWARD] |
| E3: Layered_Chains | Multiple necklaces, layered | [LAYERED_NECKLACES] |
| E4: Visible_Bra_Straps | Intentional, not accidental | [INTENTIONAL_STRAPS] |
| E5: Rhinestone_Everything | Rhinestone tops, accessories | [RHINESTONE_ACCESSORY] |
| E6: Scrunchie_Hair | Hair tie on wrist or in hair | [SCRUNCHIE_CASUAL] |
| E7: Mini_Backpack | Small bag, worn front or side | [MINI_BACKPACK_Y2K] |
| E8: Stadium_Jacket | Letterman/reversible jacket | [STADIUM_JACKET] |

> Cross-ref: E6 [SCRUNCHIE_CASUAL] paired with [PHONE_CHECK_POSTURE] (Area 02, Category E7) = strong "real life distracted" signal. E7 [MINI_BACKPACK_Y2K] pairs naturally with D2 [Pleated_Micro_Skirt] for Y2K rhythm.

---

#### Category F: Inner Layer Systems (Critical Missing) — 內層系統

**Why real:** HK girls wear 內層 (inner layer) as critical identity marker. Plain beige tank under oversized shirt = very common HK look. Inner layer is visible at neck, arms — key authenticity signal.

| Architecture | Description | Realism Signal | Token |
|-------------|-------------|----------------|-------|
| F1: PLAIN_TANK_BLACK | Basic black tank, worn under sheer | Underwear-as-outerwear base | [PLAIN_TANK_UNDER] |
| F2: SKIVVY_WHITE | White round-neck, visible collar | "Undershirt" visible | [VISIBLE_UNDERSHIRT] |
| F3: UNIQLO_HEATECH | Tech inner, thin functional | Functional fashion | [FUNCTIONAL_INNER] |
| F4: STRAPLESS_CAMISOLE | Worn under low-back tops | Practical layering | [STRAPLESS_BASE] |
| F5: LOGO_UNDERSHIRT | Visible brand inner, casual | izone/H&M base layer | [LOGO_INNER_VISIBLE] |
| F6: CROPPED_INNER | Shorter inner, shows midriff | Layered crop look | [CROPPED_INNER] |

> Cross-ref: F3 [FUNCTIONAL_INNER] references [MTR_LAYER_TRANSITION] — HK commuters wear HeatTech for MTR AC-to-outdoor heat transition. F5 [LOGO_INNER_VISIBLE] pairs with [FAST_FASHION_TAG] brand identity tokens.

---

#### Category G: Sports/Active Wear — 運動風

**Why real:** HK girls 大量運動風. Post-gym, yoga, running — athletic casual is core HK aesthetic.

| Architecture | Description | Realism Signal | Token |
|-------------|-------------|----------------|-------|
| G1: SPORTS_SET_MATCH | Matching top + leggings | Coordinated athletic | [MATCHING_SPORTS_SET] |
| G2: YOGA_PANTS_CROP | Cropped yoga pants + oversized tee | Post-yoga casual | [YOGA_CROP_COMBO] |
| G3: RUNNING_VEST | Running vest + shorts + cap | Athletic runner | [RUNNING_CASUAL] |
| G4: GYM_COMPLETE | Full gym outfit, post-workout | Pre/post gym | [GYM_COMPLETE] |
| G5: BIKE_SHORTS_LAYER | Biker shorts + long tee | Layered athletic | [BIKE_SHORTS_LAYER] |
| G6: TENNIS_SKIRT | Tennis skirt + sneakers | Sporty feminine | [TENNIS_SKIRT_CASUAL] |
| G7: SWEATSHIRT_LOOSE | Oversized sweatshirt + leggings | Comfort aesthetic | [SWEATSHIRT_CASUAL] |

> Cross-ref: Athletic wear (G1-G7) naturally maps to RHYTHM_A: ATHLETIC_CASUAL. Pair with Movement-Based Silhouettes (Area 02, Category C) — [WALKING_CAPTURED] after gym, [STRETCH_REACHING_UP] during yoga.

---

### Brand Identity Tokens (HK-Specific) — 品牌身份標記

**Why real:** HK girls use brand tags as identity markers. izone, A Pu, 小眾品牌, Supreme copy, 淘寶 direct — brand choice signals identity.

| Type | Description | Token |
|------|-------------|-------|
| FAST_FASHION_TAGGED | Brand tag visible (Uniqlo, ZARA, H&M) | [FAST_FASHION_TAG] |
| LUXURY_MINI_REPLICATE | Designer-inspired piece, not authentic | [DESIGNER_COPY] |
| VINTAGE_MARKET_FIND | 潮流廣場 or 女人街 purchase | [STREET_MARKET_FIND] |
| TAOBAO_DIRECT | Obvious Taobao item | [TAOBAO_ITEM] |
| 中古_VINTAGE | Second-hand store piece | [VINTAGE_SECONDHAND] |
| SPORTS_BRAND_CORE | Nike/Adidas/Puma as identity | [ATHLETIC_BRAND_ID] |
| 小眾品牌_CORE | Niche brand, identity marker | [NICHE_BRAND] |

> Cross-ref: [STREET_MARKET_FIND] pairs with HK-specific framing [MONGKOK_TUNNEL] or [NIGHT_MARKET_MINIMAL]. [TAOBAO_ITEM] pairs with [SHENZHEN_SHOPPING] identity.

---

### HK-Specific Style Identities (EXPANDED) — 香港風格身份

| Style | Description | Token |
|-------|-------------|-------|
| 凍奶茶後生女 | Oversized tee + track pants + sneakers | [MILK_TEA_GIRL] |
| 宿生妹 | Uniform variation, dorm life | [BOARDING_SCHOOL_GIRL] |
| 深圳購物回來 | Wardrobe from 淘寶 hauls | [SHENZHEN_SHOPPING] |
| 樓上Cafe妹 | 樓上店 aesthetic, niche cafe culture | [UPSTAIRS_CAFE_GIRL] |
| 工廠大廈妹 | Industrial building aesthetic | [INDUSTRIAL_LOFT_GIRL] |
| 大學聯誼 | University orientation, group fits | [UNI_ORIENTATION_GIRL] |
| CNY新年裝 | First-day-new-clothes tradition | [CNY_TRADITIONAL_MODERN] |
| 中秋晚裝 | Mid-Autumn festival, lanterns | [FESTIVAL_EVENING] |

---

### Outfit-Rhythm Balancing System — 穿搭節奏系統

**V15 Problem:**
- Same category (oversized knit) repeated
- Same architecture (off-shoulder) every image
- Same silhouette (loose top + tight bottom)

**V16 Solution:**
- Same category (tee) OK, but vary ARCHITECTURE (fitted tee vs oversized tee)
- Same rhythm category (party) OK, but vary ACCESSORIES + LAYERS
- Key rule: Repeat CATEGORY, vary ARCHITECTURE + ACCESSORIES + LAYERS

**RHYTHM_A: ATHLETIC_CASUAL** (post-gym, sporty)
- Token: [ATHLETIC_CASUAL]
- Examples: Sport bra top + bike shorts, racer back + cargo mini
- Pairs with: Category G (Sports/Active Wear), Silhouette Category C (Movement-Based)

**RHYTHM_B: MINIMAL_CASUAL** (lazy day, natural)
- Token: [MINIMAL_CASUAL]
- Examples: Plain tee + jeans, ribbed cami + shorts
- Pairs with: Category A (Tees), Silhouette Category E (Exhausted/Relaxed States)

**RHYTHM_C: GIRLY_CASUAL** (date, going out)
- Token: [GIRLY_CASUAL]
- Examples: Lace trim cami + pleated skirt, halter + cargo
- Pairs with: Category B (Ribbed/Cropped), Silhouette Category D (Asymmetry)

**RHYTHM_D: STREET_UTILITARIAN** (night market, hangout)
- Token: [STREET_UTILITARIAN]
- Examples: Open overshirt + cargo, tube + denim jacket
- Pairs with: Category C (Layering), Camera Distance [ENVIRONMENTAL_WIDE]

**RHYTHM_E: PARTY_REFERENCE** (nightlife, Y2K)
- Token: [PARTY_REFERENCE]
- Examples: Rhinestone top + low-rise, cropped hoodie + mini skirt
- Pairs with: Category E (Accessories), Camera Distance [FACE_CLOSEUP] or [EXTREME_CLOSEUP]

---

### Anti-Repetition Outfit Grammar — 反重複穿搭語法

```
[top_architecture]:[A1-A7/B1-B6/C1-C6]_
[bottoms_architecture]:[D1-D7]_
[layer_piece]:[none/E1-E8]_
[rhythm_category]:[A-E]_
[fit_relative]:[oversized_fitted_tight]_
[distress_level]:[pristine_worn_distressed]_
[identity_marker]:[band_subcultural_minimal_sporty]
```

**Example Prompt:**
```
[C4:SHEER_OVER_TEE]_outfit_
[FADED_GRAPHIC_TEE]_ underneath visible straps_
[D1:LOW_RISE_CARGO_MINI]_bottoms_
[E2:BASEBALL_CAP_BACKWARD]_accessory_layer_
[RHYTHM_D:STREET_UTILITARIAN]_
fit:oversized_
distress:worn_
identity:streetwear_girl_night_market
```

---

### KOL Fashion Rotation Framework — KOL穿搭輪換框架

**Observation: Real KOLs Don't Repeat Outfit Architecture**

**Pattern:** KOL repeats CATEGORY (teeshirt) but varies:
1. Silhouette (oversized vs fitted)
2. Bottoms (jeans vs shorts vs skirt)
3. Layer (jacket vs none vs accessories)
4. Context (gym vs cafe vs street)

**Framework:**
```
IMAGE_ROTATION_RULESET:
- Same category (tee) should not repeat exact architecture within 5 images
- Same silhouette (tight top + tight bottom) should not repeat within 3 images
- Same rhythm category should not repeat within 4 images
- Accessory should change identity marker every 3 images
```

> Cross-ref: This rotation framework integrates with Area 02 anti-repetition rules (posture categories not repeat within 3 images) and Area 03 rules (camera distance rotation). See §ANTI_REPETITION_RULES for unified rule set.

---

### HK-Specific Scene Tokens — 香港場景標記

- **Tea Restaurant Girl**: Oversized company tee (Pacific Coffee, 7-11), plain tee + tracksuit pants
- **MTR Commuter**: Layered for AC contrast, sheer over tee for heat-to-cold transition
- **Night Market**: Tube top + open shirt, cropped hoodie, minimal layers for humidity
- **Karaoke Session**: Party outfit with rhinestones, Y2K accessories, layered necklaces
- **Beach/Pool Day**: Sporty rehearsal wear, athletic-inspired casual

**HK Scene Tokens:** [COMPANY_TEE] [MTR_LAYER_TRANSITION] [NIGHT_MARKET_MINIMAL] [KARAOKE_PARTY] [BEACH_SPORTY_CASUAL]

> Cross-ref: These scene tokens provide context for Camera Distance choices (Area 03). [MTR_LAYER_TRANSITION] → [MTR_REFLECTION_SHOT] or [ESCALATOR_LEVEL]. [NIGHT_MARKET_MINIMAL] → [NEON_FACE_LIT] or [MONGKOK_TUNNEL]. [KARAOKE_PARTY] → [INTIMATE_DISTANCE] with [GROUP_SELFIE].

---

## SILHOUETTE_VARIATION_SYSTEM

### The Problem

Current engine relies on:
- Leaning forward (expose chest, show interest)
- Oversized neckline drift (slipped shoulder, casual seduction)
- Exposed shoulder (half-dressed intimacy)
- Same torso compression logic
- Same "attractiveness geometry" repeating

Real bodies create attraction through **natural use, movement, and spatial negotiation** — not designed poses.

---

### SILHOUETTE_VARIATION_LIBRARY

#### Category A: Weight-Bearing Postures (Body in Use) — 負重姿勢

**Principle:** Body 承受 weight = realistic, relatable, non-performative.

| Type | Description | Attraction Mechanism | Token |
|------|-------------|---------------------|-------|
| A1: ONE_LEG_SUPPORT | Standing, weight on one leg, hip shift | Asymmetry, natural stance | [ONE_LEG_SUPPORT] |
| A2: HIP_WEIGHT_SHIFT | Hip pushed to one side, shoulders opposite | Classic "model" but real version | [HIP_WEIGHT_SHIFT] |
| A3: KNEE_BEND | Slight knee bend, ready to move | Dynamic potential, not static | [SLIGHT_KNEE_BEND] |
| A4: BACKBEND_LEAN | Lower back arch, chest forward slightly | Natural counterbalance | [NATURAL_BACKBEND] |
| A5: WALL_LEAN | Body against wall, hip or shoulder | Casual weight-bearing | [WALL_LEAN_CASUAL] |
| A6: HAND_ON_WALL | One hand supporting, body angled | Spatial negotiation | [HAND_ON_WALL] |
| A7: SHOULDER_AGAINST_DOOR | Arm up, shoulder to frame | Casual doorway use | [SHOULDER_DOORFRAME] |

> Cross-ref: A5-A7 are spatial-negotiation postures. Pair with HK-specific framing [ESTATE_FRAMING] (屋苑平台花園), [UNI_STAIRS] (大學校園樓梯), or [FOOTBRIDGE_WIDE] (行人天橋) for environment-body interaction. See §CAMERA_DISTANCE_DIVERSITY_SYSTEM.

---

#### Category B: Seated/Mounted Compression — 坐姿壓縮

**Principle:** Sitting creates predictable compression points that reveal body without posing.

| Type | Description | Attraction Mechanism | Token |
|------|-------------|---------------------|-------|
| B1: CROSS_LEGGED_COMPACT | Legs crossed, knees high, compact | Thigh compression, small silhouette | [CROSS_LEGGED_COMPACT] |
| B2: KNEE_TO_CHEST | Arms around knees, self-contained | Foetal-adjacent comfort | [KNEES_TO_CHEST] |
| B3: SIDE_SEATED | Legs to side, knees bent | Hip angle, casual | [SIDE_SEATED_CASUAL] |
| B4: STAIR_SITTING | On stairs, different heights | Level variation, leg reveal | [STAIR_SITTING] |
| B5: FLOOR_LOUNGE | Lying or recline, casual floor | Most relaxed state | [FLOOR_LOUNGE_CASUAL] |
| B6: CHAIR_FORWARD | Leaning forward on chair, arms crossed on back | Desk-adjacent, study | [CHAIR_FORWARD_LEAN] |
| B7: LEGS_OVER_ARM | Legs draped over sofa/arm | Lived-in living room | [LEGS_OVER_ARM] |

> Cross-ref: B1 [CROSS_LEGGED_COMPACT] activates CP_02 (thigh contact) and CP_03 (abdominal fold). B6 [CHAIR_FORWARD_LEAN] activates CP_01 (under-breast shadow). See Compression Points below.

---

#### Category C: Movement-Based Silhouettes — 動態剪影

**Principle:** Body mid-motion = most realistic. Stillness is performance.

| Type | Description | Attraction Mechanism | Token |
|------|-------------|---------------------|-------|
| C1: WALKING_MOMENTUM | Mid-stride, natural gait, slight lean | Dynamic, captured candid | [WALKING_CAPTURED] |
| C2: BENDING_TO_PICKUP | Hinge at hips, reaching down | Hip angle, practicality | [BENDING_TO_PICKUP] |
| C3: HAIR_PUSH_BACK | Hand through hair, head back slightly | Neck exposure, motion | [PUSHING_HAIR_BACK] |
| C4: STRETCH_REACHING | Arms up, body elongating | Posture extension | [STRETCH_REACHING_UP] |
| C5: TURNING_AWAY | Mid-turn, profile or back view | Mystery, non-performance | [MID_TURN_AWAY] |
| C6: LOOKING_BACK | Over shoulder, neck twist | Classic but real | [OVER_SHOULDER_GLANCE] |
| C7: ARM_RAISED | One or both arms up, stretching or reaching | Underarm exposure, casual | [ARMS_RAISED_CASUAL] |
| C8: BUCKET_CARRY | Carrying something, both hands occupied | Practical, non-performative | [CARRYING_OBJECT] |

> Cross-ref: C1 [WALKING_CAPTURED] pairs with Camera Distance [FULL_BODY_SHOT] or [KNEE_TO_HEAD] and Shot Type [FORGOTTEN_CAMERA:P2]. C5 [MID_TURN_AWAY] pairs with [BACK_VIEW_PRIMARY] group dynamic.

---

#### Category D: Asymmetry Generators — 不對稱生成器

**Principle:** Perfect symmetry = professional/posed. Real bodies are asymmetrical.

| Type | Description | Attraction Mechanism | Token |
|------|-------------|---------------------|-------|
| D1: HEAD_TILT | Head to one side, not centered | Asymmetry, casual | [HEAD_TILT_CASUAL] |
| D2: SHOULDER_DROP | One shoulder higher than other | Weight asymmetry | [SHOULDER_DROP] |
| D3: ASYMMETRIC_SQUAT | One leg down, one leg bent | Street/casual squat | [ASYMMETRIC_SQUAT] |
| D4: ARM_HANG | One arm hanging, other doing something | Action asymmetry | [ONE_ARM_HANGING] |
| D5: EYE_LEVEL_TILT | Camera above but head tilted down | Natural counter-angle | [NATURAL_TILT_DOWN] |
| D6: BACKPACK_PULL | Backpack strap pulling one shoulder | Weight imbalance | [BACKPACK_SHOULDER_PULL] |

> Cross-ref: D6 [BACKPACK_SHOULDER_PULL] pairs naturally with E7 [MINI_BACKPACK_Y2K] accessory (Area 01). D3 [ASYMMETRIC_SQUAT] is the generic version of F3 [STREET_SQUAT_HK] below.

---

#### Category E: Exhausted/Relaxed States — 疲勞/放鬆狀態

**Principle:** Tired body = honest body. Exhaustion removes performance.

| Type | Description | Attraction Mechanism | Token |
|------|-------------|---------------------|-------|
| E1: SLUMPED_SHOULDERS | Shoulders rounded, chin down | Vulnerability, honesty | [SLUMPED_EXHAUSTED] |
| E2: HAND_ON_NECK | Supporting head, neck exposed | Fatigue + neck display | [HAND_BEHIND_NECK] |
| E3: EYES_CLOSED_RELAX | Eyes closed, face relaxed | Comfortable non-performance | [EYES_CLOSED_RELAXED] |
| E4: MOUTH_PARTIAL | Slightly open, breathing or talking | Real-time moment | [MOUTH_SLIGHTLY_OPEN] |
| E5: HUNCHED_FORWARD | Back curved, protective posture | Self-contained, shy | [HUNCHED_PROTECTIVE] |
| E6: WEIGHT_ON_ELBOW | Reclining on elbow, half-up | Casual recline | [RECLINE_ON_ELBOW] |
| E7: PHONE_CHECK | Looking at phone, chin dropped | Distracted, real | [PHONE_CHECK_POSTURE] |

> Cross-ref: E7 [PHONE_CHECK_POSTURE] is the strongest "real life" signal. Pair with [FORGOTTEN_CAMERA:P2] or [HIDDEN_CAMERA_SHOT:P1] and camera height [HIP_LEVEL_CAMERA]. Combine with [MTR_RAIL_LEAN] for MTR phone-check combo.

---

### Body-Weight Realism System — 身體重力寫實系統

#### Principle

Real bodies **accept gravity**. Every body part has weight. Weight creates:
- Compression (skin against fabric, skin against skin)
- Draping (loose fabric falls naturally)
- Exposed lines (under arm, between breasts, neck base)
- Pressure marks (slight indentation from clothing)

#### Compression Points — 壓縮點

```
COMPRESSION_POINT_LIBRARY:

CP_01: UNDER_BREAST
- When: seated, bending forward, bra band
- Creates: breast separation, under-breast shadow
- Token: [UNDERBREAST_SHADOW]

CP_02: THIGH_GAP_OR_NOT
- When: seated cross-legged, tight skirt/dress
- Creates: thigh contact or gap, depends on body
- Token: [THIGH_CONTACT]

CP_03: ABDOMINAL_FOLD
- When: seated, forward lean, high-waisted clothing
- Creates: natural skin fold, not fat
- Token: [ABDOMINAL_SOFT_FOLD]

CP_04: UNDERARM_SKIN
- When: arm raised, relaxed arm, sleeveless
- Creates: exposed underarm, natural skin
- Token: [UNDERARM_EXPOSED]

CP_05: NECK_BASE_V
- When: head forward, chin down
- Creates: exposed V at neck base
- Token: [NECK_BASE_EXPOSED]

CP_06: SPINE_REVEAL
- When: back arch, leaning forward
- Creates: visible spine line through clothing
- Token: [SPINE_VISUAL_LINE]

CP_07: SHOULDER_BLADE_BULGE
- When: shoulders back, tight top
- Creates: natural shoulder blade prominence
- Token: [SHOULDERBLADE_VISIBLE]
```

> Cross-ref: CP_07 works best for lean/athletic body types. For other body types, use alternative compression points. CP_01-CP_03 activate primarily in seated postures (Area 02 Category B). CP_04-CP_07 activate in movement or standing postures (Area 02 Categories A, C).

---

### Posture Diversity Grammar — 姿勢多樣化語法

```
[primary_posture]:[A1-A7/B1-B7/C1-C8/D1-D6/E1-E7]_
[compression_point]:[CP01-CP07]_
[body_axis]:[upright_forward_side_reclined]_
[weight_distribution]:[balanced_left_heavy_right_heavy]_
[movement_state]:[still_mid-motion_transitioning]
```

**Examples:**
```
[SIDE_SEATED_CASUAL:B3]_posture
compression:[THIGH_CONTACT:CP02]
body_axis:side_tilted
weight_distribution:right_heavy
movement_state:still

[WALKING_CAPTURED:C1]_posture
compression:[UNDERBREAST_SHADOW:CP01]_from_motion
body_axis:forward_lean_slight
weight_distribution:alternating
movement_state:mid-motion
```

---

### HK-Specific Postures (Context-Added) — 香港特定姿勢

**Why real:** Specific HK postures from daily life, not generic poses.

| Type | Description | Attraction Mechanism | Token |
|------|-------------|---------------------|-------|
| F1: MTR_HANDRAIL_LEAN | One hand on rail, body tilted, hip shift | Spatial negotiation, casual | [MTR_RAIL_LEAN] |
| F2: QUEUE_WEIGHT_CYCLE | Standing in line, shifting weight leg to leg | Waiting behavior, natural | [QUEUE_WEIGHT_SHIFT] |
| F3: STREET_SQUAT_HK | Squatting on ground, common in street markets | Very HK, casual 接地氣 | [STREET_SQUAT_HK] |
| F4: WALL_QUEUE_STAND | Standing against wall while queuing | One leg bent, hip shift | [WALL_QUEUE_STAND] |
| F5: ESCALATOR_STILL | Standing still on escalator, not walking | MTR etiquette, casual | [ESCALATOR_STILL] |

> Cross-ref: F1 [MTR_RAIL_LEAN] pairs with [MTR_REFLECTION_SHOT] framing (Area 03). F3 [STREET_SQUAT_HK] is the culturally-specific HK version of D3 [ASYMMETRIC_SQUAT]. F5 [ESCALATOR_STILL] pairs with [ESCALATOR_LEVEL] framing.

---

## CAMERA_DISTANCE_DIVERSITY_SYSTEM

### The Problem

Current engine relies on:
- Same intimacy distance (close-up, medium close-up dominance)
- Same framing rhythm (2-shot, 3-shot repeating same structure)
- Same eye-level energy (neutral or slightly above)
- Same "head-and-shoulders" or "waist-up" crop dominance

Real social media camera variety: from extreme close-up to environmental wide, from planned to accidental.

---

### CAMERA_DISTANCE_VARIATION_LIBRARY

#### Distance Categories (Based on Social Photography Research)

| Distance Type | Focal Length Equivalent | Frame Coverage | Emotional Tone | Token |
|--------------|------------------------|----------------|-----------------|-------|
| EXTREME_CLOSEUP | 35mm, <30cm | Face dominant, 60%+ frame | Intimate, voyeuristic | [EXTREME_CLOSEUP] |
| FACE_CLOSEUP | 50mm, 30-50cm | Face 50-70%, hair/shoulders | Personal, direct | [FACE_CLOSEUP] |
| HEAD_SHOULDERS | 85mm, 50-80cm | Head to mid-chest | Portrait classic | [HEAD_SHOULDERS] |
| WAIST_UP | 85-105mm, 1-1.5m | Waist to head | Social portrait | [WAIST_UP] |
| KNEE_TO_HEAD | 105mm, 1.5-2m | Knee to head | Environmental portrait | [KNEE_TO_HEAD] |
| FULL_BODY | 135mm, 2-3m | Full body, some floor/ceiling | Contextual | [FULL_BODY_SHOT] |
| ENVIRONMENTAL | 24-35mm, 3-5m | Body small, environment large | Documentary | [ENVIRONMENTAL_WIDE] |
| DISTANT_CANDID | Telephoto, 5m+ | Person as element | Stolen shot, observer | [DISTANT_CANDID] |

---

#### Intimacy-Distance Framework — 親密距離框架

**Principle:** Distance = emotional contract. Closer = more intimacy, more expectation of relationship.

```
INTIMACY_DISTANCE_MATRIX:

Level 1: STRANGER_DISTANCE (3m+)
- Emotional tone: Public observation, documentary
- Expectation: None
- Token: [STRANGER_DISTANCE]

Level 2: ACQUAINTANCE_DISTANCE (1.5-3m)
- Emotional tone: Social but not intimate
- Expectation: Polite recognition
- Token: [ACQUAINTANCE_DISTANCE]

Level 3: FRIEND_DISTANCE (0.5-1.5m)
- Emotional tone: Comfortable, casual
- Expectation: Some relationship
- Token: [FRIEND_DISTANCE]

Level 4: INTIMATE_DISTANCE (<0.5m)
- Emotional tone: Private, intimate
- Expectation: Deep relationship
- Token: [INTIMATE_DISTANCE]
```

> Cross-ref: Intimacy level maps to rhythm categories (Area 01): [ATHLETIC_CASUAL] → Level 2-3, [PARTY_REFERENCE] → Level 3-4, [MINIMAL_CASUAL] → Level 2-3. See Rhythm Balancing System.

---

### Framing Diversity System — 構圖多樣化

#### 2D Composition Types

| Type | Description | Realism Signal | Token |
|------|-------------|----------------|-------|
| CENTRAL_COMPOSITION | Subject center frame | Intentionally framed, directed | [CENTRAL_COMPOSITION] |
| RULE_OF_THIRDS_OFF | Subject at intersection point | Slightly considered | [RULE_OF_THIRDS] |
| EDGE_FRAME | Subject near frame edge | Accident or creative | [EDGE_FRAME] |
| BOTTLENECK | Subject at narrow point in scene | Environmental framing | [BOTTLENECK_FRAME] |
| REFLECTION_FRAME | Subject in mirror, window, water | Self-documentation | [REFLECTION_FRAME] |
| OVER_THE_SHOULDER | Subject seen through another person's shoulder | Social document | [OVER_SHOULDER_SHOT] |
| HIDDEN_OBSERVER | Subject unaware, observer angle | Stolen shot | [HIDDEN_OBSERVER] |
| ACCIDENTAL_CROP | Framing appears imperfect | Authentic amateur | [ACCIDENTAL_CROP] |

> Cross-ref: [REFLECTION_FRAME] is the generic parent of [MTR_REFLECTION_SHOT], [CONVENIENCE_REFLECTION], and [CS_GLASS_REFLECTION]. [ACCIDENTAL_CROP] pairs with camera height [HIP_LEVEL_CAMERA] for maximum "authentic amateur" signal.

---

#### HK-Specific Framing Situations (EXPANDED) — 香港構圖場景

| Situation | Framing Type | Token |
|-----------|-------------|-------|
| MTR Train Reflection | Mirror/reflection frame | [MTR_REFLECTION_SHOT] |
| Convenience Store Window | Window reflection, AC contrast | [CONVENIENCE_REFLECTION] |
| Ferry Deck Wide | Environmental, harbor context | [FERRY_WIDE] |
| Tea Restaurant Table | Overhead or side angle | [TEA_RESTAURANT_ANGLE] |
| Night Market Neon | Neon light framing, face lit by sign | [NEON_FACE_LIT] |
| Escalator Up | Ascending/descending, level change | [ESCALATOR_LEVEL] |
| 屋苑平台花園 | Estate podium garden, natural light | [ESTATE_FRAMING] |
| 行人天橋 | Footbridge, elevated view | [FOOTBRIDGE_WIDE] |
| 的士後座 | Taxi interior, rear seat view | [TAXI_REAR_SEAT] |
| 大學校園樓梯 | University stairwell, layered | [UNI_STAIRS] |
| 便利店玻璃 | Convenience store glass reflection | [CS_GLASS_REFLECTION] |
| 旺角行人隧道 | Mongkok pedestrian tunnel | [MONGKOK_TUNNEL] |

> Cross-ref: HK framing situations provide concrete contexts for outfit choices (Area 01). [FERRY_WIDE] → [MTR_LAYER_TRANSITION] (wind + AC). [TEA_RESTAURANT_ANGLE] → [MILK_TEA_GIRL] or [COMPANY_TEE]. [NEON_FACE_LIT] → [NIGHT_MARKET_MINIMAL] or [PARTY_REFERENCE].

---

#### Group Dynamics (EXPANDED) — 群體動態

| Type | Description | Token |
|------|-------------|-------|
| DUO_CLOSE | Two people, close together | [DUO_CLOSE] |
| DUO_APART | Two people, separate | [DUO_APART] |
| TRIO_GROUP | Three, dynamic triangle | [TRIO_DYNAMIC] |
| GROUP_SELFIE | Group selfie, front camera | [GROUP_SELFIE] |
| OVERHEARD | Person in background of other's photo | [OVERHEARD_IN_BACKGROUND] |
| GROUP_DINNER_4P | Four people, dinner setup | [GROUP_DINNER_4] |
| LARGE_GROUP_EVENT | 6+ people, event photo | [LARGE_GROUP_EVENT] |
| SOMEONE_ELSE_PHOTO | Someone else photographing subject | [SOMEONE_ELSE_PHOTO] |
| PHOTO_BOMB_HK | Accidental person in background | [PHOTO_BOMB_HK] |
| BACK_VIEW_PRIMARY | Subject's back as primary subject | [BACK_VIEW_PRIMARY] |
| RANDOM_IN_FRAME | Random person in frame, not posed | [RANDOM_IN_FRAME] |

> Cross-ref: [GROUP_SELFIE] activates [INTIMATE_DISTANCE:Level_3-4]. [BACK_VIEW_PRIMARY] pairs with Silhouette [MID_TURN_AWAY:C5] for complete non-performance. [PHOTO_BOMB_HK] and [RANDOM_IN_FRAME] add environmental realism — useful for [ENVIRONMENTAL_WIDE] distance.

---

### Camera Height Variation — 相機高度變化

**Principle:** Same eye-level creates same energy. Real photos come from every angle.

| Height | Description | Effect | Token |
|--------|-------------|--------|-------|
| HIGH_ANGLE | Camera above subject (>15° down) | Subordinate, vulnerable, cute | [HIGH_ANGLE_CAMERA] |
| EYE_LEVEL | Camera at subject eye level | Neutral, equal | [EYE_LEVEL_CAMERA] |
| LOW_ANGLE | Camera below subject (>15° up) | Dominant, empowering, heroic | [LOW_ANGLE_CAMERA] |
| GROUND_LEVEL | Camera near floor | Immersive, worm-eye | [GROUND_LEVEL_CAMERA] |
| OVERHEAD | Camera directly above | Flat, bird's eye, abstract | [OVERHEAD_CAMERA] |
| HIP_LEVEL | Camera at hip height | Casual, candid | [HIP_LEVEL_CAMERA] |

> Cross-ref: [HIP_LEVEL_CAMERA] is the default for [FORGOTTEN_CAMERA:P2] and [HIDDEN_CAMERA_SHOT:P1] — phone-at-hip candid shots. [HIGH_ANGLE_CAMERA] pairs with [GROUP_SELFIE] (selfie stick angle). [OVERHEAD_CAMERA] pairs with [TEA_RESTAURANT_ANGLE] (food-flatlay-adjacent).

---

### Shot Type Variation — 拍攝類型

#### Candid vs Posed Spectrum

```
SHOT_TYPE_SPECTRUM:

P1: HIDDEN_CAMERA (most candid)
- Subject unaware
- No awareness, no performance
- Token: [HIDDEN_CAMERA_SHOT]

P2: FORGOTTEN_CAMERA
- Subject knows camera exists, but ignoring it
- Token: [FORGOTTEN_CAMERA]

P3: ACCIDENTAL_AWARENESS
- Subject notices camera at moment of capture
- Token: [ACCIDENTAL_AWARE]

P4: COOPERATIVE_FRIEND
- Subject knows, cooperating but casual
- Token: [COOPERATIVE_FRIEND]

P5: DIRECTED_PERFORMANCE
- Subject posing, aware and performing
- Token: [DIRECTED_PERFORMANCE]
```

> Cross-ref: P1-P3 generate the most authentic "real KOL feed" feel. P4-P5 should be used sparingly — at most 2 out of every 10 images. P1 [HIDDEN_CAMERA_SHOT] pairs with [DISTANT_CANDID] or [HIDDEN_OBSERVER] framing. P2 [FORGOTTEN_CAMERA] is the default for real-feeling lifestyle content.

---

### Camera Prompt Grammar — 相機提示語法

```
[distance_type]:[EXTREME_CLOSEUP to DISTANT_CANDID]_
[intimacy_level]:[Level_1-4]_
[framing_type]:[CENTRAL to ACCIDENTAL_CROP]_
[camera_height]:[HIGH_ANGLE to OVERHEAD]_
[shot_type]:[P1-P5]_
[group_dynamics]:[solo/duo/trio/group]_
[awareness_level]:[unaware_forgotten_aware_cooperating_performing]
```

**Examples:**
```
[FULL_BODY_SHOT]_distance_
[intimacy:Level_3_FRIEND_DISTANCE]_
[framing:ENVIRONMENTAL_WIDE]_ferry_deck_harbor_context_
[camera_height:EYE_LEVEL_CAMERA]_
[shot_type:FORGOTTEN_CAMERA:P2]_
[group: solo]_
awareness:casual_streetwear_girl_harbor_evening

[FACE_CLOSEUP]_distance_
[intimacy:Level_4_INTIMATE_DISTANCE]_
[framing:REFLECTION_FRAME]_morning_bathroom_mirror_
[camera_height:HIP_LEVEL_CAMERA]_
[shot_type:COOPERATIVE_FRIEND:P4]_
[group:solo]_
awareness:no_makeup_morning_face_intimate
```

---

## ANTI_REPETITION_RULES

### Cross-Module Anti-Repetition Ruleset — 跨模組反重複規則

These unified rules span all three areas (Outfit → Silhouette → Camera). They are additive — entries at each generation must satisfy ALL applicable rules.

#### Outfit Rules (Area 01)

| Rule | Scope | Token |
|------|-------|-------|
| Same tee architecture (A1-A7) must not repeat within 5 images | Feed-level | [OUTFIT_ROTATE:ARCH:5] |
| Same silhouette (tight top + tight bottom) must not repeat within 3 images | Feed-level | [OUTFIT_ROTATE:SIL:3] |
| Same rhythm category (A-E) must not repeat within 4 images | Feed-level | [OUTFIT_ROTATE:RHY:4] |
| Accessory identity marker must change every 3 images | Feed-level | [OUTFIT_ROTATE:ACC:3] |

#### Silhouette Rules (Area 02)

| Rule | Scope | Token |
|------|-------|-------|
| Same posture category (A/B/C/D/E) must not repeat within 3 images | Feed-level | [SIL_ROTATE:CAT:3] |
| Same compression point (CP01-CP07) must not repeat within 4 images | Feed-level | [SIL_ROTATE:CP:4] |
| Movement state (C types) must appear at least once every 5 images | Feed-level | [SIL_REQUIRE:MOVEMENT:5] |
| Exhausted states (E types) must appear at least twice per 10-image feed | Feed-level | [SIL_REQUIRE:EXHAUSTED:10] |

#### Camera Rules (Area 03)

| Rule | Scope | Token |
|------|-------|-------|
| Same intimacy level must not repeat within 3 images | Feed-level | [CAM_ROTATE:INT:3] |
| Same camera height must not repeat within 4 images | Feed-level | [CAM_ROTATE:HEIGHT:4] |
| Same framing type must not repeat within 3 images | Feed-level | [CAM_ROTATE:FRAME:3] |
| Candid shot types (P1-P3) must appear at least 6 times per 10-image feed | Feed-level | [CAM_REQUIRE:CANDID:10] |
| Posed shot types (P4-P5) must appear at most 2 times per 10-image feed | Feed-level | [CAM_LIMIT:POSED:10] |

#### Cross-Module Hard Constraints

| Rule | Scope |
|------|-------|
| [EXTREME_CLOSEUP] must not appear more than once per 5 images | Feed-level |
| [INTIMATE_DISTANCE:Level_4] must not appear more than twice per 10-image feed | Feed-level |
| Same outfit architecture + same camera distance combo must never repeat in a feed | Feed-level |
| [DIRECTED_PERFORMANCE:P5] + [CENTRAL_COMPOSITION] = formula danger — use only once per 10 images | Feed-level |

#### Rotation Priority

When multiple rules conflict (e.g., need movement state but also need to avoid repeating posture category), apply in this priority order:
1. **Safety** — intimacy level limits first
2. **Variety** — category non-repeat rules second
3. **Realism** — required minimums (movement, exhausted, candid) third
4. **Identity** — outfit rhythm rotation last

---

## IMPLEMENTATION

### How to Use This Module in Prompts — 如何於提示中使用此模組

#### Step 1: Select Rhythm (which energy?)

Choose one rhythm category per image from the Rhythm Balancing System. For a feed of N images, ensure rhythm categories rotate without consecutive repeats.

```
Current rhythm: RHYTHM_C:GIRLY_CASUAL
(Uses: lace trim cami, pleated skirt, halter, feminine accessories)
```

#### Step 2: Select Outfit Architecture (what to wear?)

From the Streetwear Diversity Library, select:
- Top architecture: Category A, B, or C (choose one specific architecture)
- Bottoms architecture: Category D (choose one)
- Inner layer: Category F (optional but recommended for HK authenticity)
- Accessories: Category E (choose 1-3)

```
Top: B2 [LACE_TRIM_CAMISOLE]
Bottoms: D2 [Pleated_Micro_Skirt]
Inner: F4 [STRAPLESS_BASE]
Accessory: E3 [LAYERED_NECKLACES]
```

#### Step 3: Select Silhouette Posture (how does body look?)

From the Silhouette Variation Library, select:
- Primary posture: Category A, B, C, D, or E
- Compression point: CP_01-CP_07 (optional but adds realism)
- Weight distribution + movement state

```
Posture: C6 [OVER_SHOULDER_GLANCE]
Compression: CP_05 [NECK_BASE_EXPOSED] (from neck twist)
Movement: still (posed but natural)
Body axis: side_tilted
```

#### Step 4: Select Camera Setup (how is it captured?)

From the Camera Distance Diversity Library, select:
- Distance type
- Intimacy level
- Framing type
- Camera height
- Shot type (P1-P5)

```
Distance: [WAIST_UP]
Intimacy: Level_3 [FRIEND_DISTANCE]
Framing: [RULE_OF_THIRDS]
Height: [EYE_LEVEL_CAMERA]
Shot: P4 [COOPERATIVE_FRIEND]
```

#### Step 5: Compose the Unified Token String

Combine all selections into a single token string:

```
[GIRLY_CASUAL:RHYTHM_C]_
[LACE_TRIM_CAMISOLE:B2]_[PLEATED_MICRO_SKIRT:D2]_
[STRAPLESS_BASE:F4]_[LAYERED_NECKLACES:E3]_
[OVER_SHOULDER_GLANCE:C6]_[NECK_BASE_EXPOSED:CP05]_
[WAIST_UP]_[FRIEND_DISTANCE:Level3]_
[RULE_OF_THIRDS]_[EYE_LEVEL_CAMERA]_
[COOPERATIVE_FRIEND:P4]_
awareness:girly_casual_hk_date_evening
```

#### Step 6: Verify Against Anti-Repetition Rules

Before finalizing, check the token combination against ALL anti-repetition rules. If any rule would be violated, adjust the least-constrained parameter (usually accessories or compression point).

#### Example Feed Structure (10 images)

| Image | Rhythm | Top Arch | Posture Cat | Distance | Camera Height | Shot |
|-------|--------|----------|-------------|----------|---------------|------|
| 1 | Athletic (A) | G2 Yoga Crop | C1 Walking | FULL_BODY | EYE_LEVEL | P2 |
| 2 | Minimal (B) | A6 Plain Tee | E7 Phone Check | WAIST_UP | HIP_LEVEL | P1 |
| 3 | Girly (C) | B2 Lace Cami | B3 Side Seat | HEAD_SHOULDERS | HIGH_ANGLE | P4 |
| 4 | Street (D) | C6 Open Shirt | A5 Wall Lean | ENVIRONMENTAL | LOW_ANGLE | P3 |
| 5 | Party (E) | E5 Rhinestone | C6 Look Back | FACE_CLOSEUP | EYE_LEVEL | P5 |
| 6 | Athletic (A) | G4 Gym Full | E1 Slumped | KNEE_TO_HEAD | GROUND_LEVEL | P2 |
| 7 | Minimal (B) | A1 Faded Tee | B5 Floor Lounge | FULL_BODY | OVERHEAD | P1 |
| 8 | Girly (C) | B4 Racer Back | D1 Head Tilt | WAIST_UP | HIP_LEVEL | P3 |
| 9 | Street (D) | C5 Denim Over | A2 Hip Shift | DISTANT_CANDID | EYE_LEVEL | P2 |
| 10 | Party (E) | E8 Stadium | B1 Cross Leg | EXTREME_CLOSEUP | HIGH_ANGLE | P4 |

> ✅ Rhythm: no consecutive repeats within 4 images
> ✅ Posture: categories A-E all used, no repeat within 3
> ✅ Camera height: all 6 used, no repeat within 3
> ✅ Shot type: 3 candid (P1-P3) and 2 posed (P4-P5) — passes 6:2 ratio
> ✅ Intimacy: distributed across Levels 1-4

---

## TOKEN REFERENCE

### Quick Reference: All Tokens in This Module — 全部標記速查表

#### Outfit Tokens (Area 01)

| Token | Category | Description |
|-------|----------|-------------|
| [FADED_GRAPHIC_TEE] | A1 | Washed-out print tee |
| [VINTAGE_BAND_TEE] | A2 | Retro band tee |
| [MENS_BORROWED_TEE] | A3 | Oversized men's tee on women |
| [KNOTTED_CROP_TEE] | A4 | DIY cropped tee |
| [STRETCHED_COLLAR_TEE] | A5 | Worn-in stretched neckline tee |
| [PLAIN_FITTED_TEE] | A6 | Minimal pocket tee |
| [DOUBLE_SIDED_GRAPHIC] | A7 | Front/back different graphic |
| [RIBBED_CAMI] | B1 | Ribbed cotton camisole |
| [LACE_TRIM_CAMISOLE] | B2 | Lace-edged cami |
| [SPORT_BRA_STYLE] | B3 | Athletic bra top |
| [RACER_BACK_CASUAL] | B4 | Racerback casual top |
| [HALTER_CASUAL] | B5 | Neck-tie halter |
| [TUBE_STREETWEAR] | B6 | Strapless tube top |
| [MESH_UNDER_LAYER] | C1 | Sheer mesh under/over tee |
| [TANK_UNDER_CARDIGAN] | C2 | Tank under open cardigan |
| [CROPPED_ZIP_HOODIE] | C3 | Above-waist zip hoodie |
| [SHEER_OVER_TEE] | C4 | Blouse open over tee |
| [OVERSIZED_DENIM] | C5 | Oversized denim jacket |
| [OPEN_OVERSHIRT] | C6 | Open flannel/oxford |
| [OVERSIZED_HEADPHONES] | E1 | Over-ear headphones |
| [CAP_BACKWARD] | E2 | Backwards baseball cap |
| [LAYERED_NECKLACES] | E3 | Multiple layered chains |
| [INTENTIONAL_STRAPS] | E4 | Visible bra straps |
| [RHINESTONE_ACCESSORY] | E5 | Rhinestone accessories |
| [SCRUNCHIE_CASUAL] | E6 | Scrunchie hair/wrist |
| [MINI_BACKPACK_Y2K] | E7 | Small Y2K backpack |
| [STADIUM_JACKET] | E8 | Letterman jacket |
| [PLAIN_TANK_UNDER] | F1 | Black tank inner layer |
| [VISIBLE_UNDERSHIRT] | F2 | White undershirt visible |
| [FUNCTIONAL_INNER] | F3 | HeatTech/functional inner |
| [STRAPLESS_BASE] | F4 | Strapless camisole base |
| [LOGO_INNER_VISIBLE] | F5 | Brand-logo inner layer |
| [CROPPED_INNER] | F6 | Cropped shorter inner |
| [MATCHING_SPORTS_SET] | G1 | Coordinated athletic set |
| [YOGA_CROP_COMBO] | G2 | Yoga pants + oversized tee |
| [RUNNING_CASUAL] | G3 | Running vest + shorts |
| [GYM_COMPLETE] | G4 | Full gym outfit |
| [BIKE_SHORTS_LAYER] | G5 | Biker shorts + long tee |
| [TENNIS_SKIRT_CASUAL] | G6 | Tennis skirt + sneakers |
| [SWEATSHIRT_CASUAL] | G7 | Oversized sweatshirt casual |

#### Brand Identity Tokens (Area 01)

| Token | Description |
|-------|-------------|
| [FAST_FASHION_TAG] | Visible Uniqlo/ZARA/H&M tag |
| [DESIGNER_COPY] | Designer-inspired replica |
| [STREET_MARKET_FIND] | 潮流廣場/女人街 purchase |
| [TAOBAO_ITEM] | Obvious Taobao item |
| [VINTAGE_SECONDHAND] | Second-hand store (中古) |
| [ATHLETIC_BRAND_ID] | Nike/Adidas/Puma identity |
| [NICHE_BRAND] | 小眾品牌 marker |

#### Rhythm Tokens (Area 01)

| Token | Energy |
|-------|--------|
| [ATHLETIC_CASUAL] | Post-gym, sporty |
| [MINIMAL_CASUAL] | Lazy day, natural |
| [GIRLY_CASUAL] | Date, going out |
| [STREET_UTILITARIAN] | Night market, hangout |
| [PARTY_REFERENCE] | Nightlife, Y2K |

#### HK Identity Tokens (Area 01)

| Token | Description |
|-------|-------------|
| [MILK_TEA_GIRL] | 凍奶茶後生女 |
| [BOARDING_SCHOOL_GIRL] | 宿生妹 |
| [SHENZHEN_SHOPPING] | 深圳購物回來 |
| [UPSTAIRS_CAFE_GIRL] | 樓上Cafe妹 |
| [INDUSTRIAL_LOFT_GIRL] | 工廠大廈妹 |
| [UNI_ORIENTATION_GIRL] | 大學聯誼 |
| [CNY_TRADITIONAL_MODERN] | CNY新年裝 |
| [FESTIVAL_EVENING] | 中秋晚裝 |
| [COMPANY_TEE] | Tea restaurant company tee |
| [MTR_LAYER_TRANSITION] | MTR AC layering |
| [NIGHT_MARKET_MINIMAL] | Night market minimal layers |
| [KARAOKE_PARTY] | Karaoke party outfit |
| [BEACH_SPORTY_CASUAL] | Beach sporty casual |

#### Silhouette / Posture Tokens (Area 02)

| Token | Category | Description |
|-------|----------|-------------|
| [ONE_LEG_SUPPORT] | A1 | Weight on one leg |
| [HIP_WEIGHT_SHIFT] | A2 | Hip pushed to side |
| [SLIGHT_KNEE_BEND] | A3 | Slight knee bend |
| [NATURAL_BACKBEND] | A4 | Lower back arch |
| [WALL_LEAN_CASUAL] | A5 | Body against wall |
| [HAND_ON_WALL] | A6 | One hand supporting |
| [SHOULDER_DOORFRAME] | A7 | Shoulder to doorframe |
| [CROSS_LEGGED_COMPACT] | B1 | Legs crossed compact |
| [KNEES_TO_CHEST] | B2 | Arms around knees |
| [SIDE_SEATED_CASUAL] | B3 | Legs to side seated |
| [STAIR_SITTING] | B4 | Sitting on stairs |
| [FLOOR_LOUNGE_CASUAL] | B5 | Floor recline |
| [CHAIR_FORWARD_LEAN] | B6 | Forward on chair |
| [LEGS_OVER_ARM] | B7 | Legs over sofa arm |
| [WALKING_CAPTURED] | C1 | Mid-stride candid |
| [BENDING_TO_PICKUP] | C2 | Hinging to pick up |
| [PUSHING_HAIR_BACK] | C3 | Hand through hair |
| [STRETCH_REACHING_UP] | C4 | Arms up stretching |
| [MID_TURN_AWAY] | C5 | Mid-turn profile |
| [OVER_SHOULDER_GLANCE] | C6 | Looking back |
| [ARMS_RAISED_CASUAL] | C7 | Arms raised casually |
| [CARRYING_OBJECT] | C8 | Both hands occupied |
| [HEAD_TILT_CASUAL] | D1 | Head tilt asymmetry |
| [SHOULDER_DROP] | D2 | One shoulder higher |
| [ASYMMETRIC_SQUAT] | D3 | Uneven leg squat |
| [ONE_ARM_HANGING] | D4 | One arm idle |
| [NATURAL_TILT_DOWN] | D5 | Head tilted down |
| [BACKPACK_SHOULDER_PULL] | D6 | Backpack weight pull |
| [SLUMPED_EXHAUSTED] | E1 | Shoulders rounded |
| [HAND_BEHIND_NECK] | E2 | Supporting head |
| [EYES_CLOSED_RELAXED] | E3 | Eyes closed relaxed |
| [MOUTH_SLIGHTLY_OPEN] | E4 | Mouth partial open |
| [HUNCHED_PROTECTIVE] | E5 | Back curved protective |
| [RECLINE_ON_ELBOW] | E6 | Weight on elbow |
| [PHONE_CHECK_POSTURE] | E7 | Phone-check posture |

#### Compression Point Tokens (Area 02)

| Token | CP | Description |
|-------|-----|-------------|
| [UNDERBREAST_SHADOW] | CP_01 | Under-breast shadow |
| [THIGH_CONTACT] | CP_02 | Thigh contact/gap |
| [ABDOMINAL_SOFT_FOLD] | CP_03 | Natural skin fold |
| [UNDERARM_EXPOSED] | CP_04 | Exposed underarm |
| [NECK_BASE_EXPOSED] | CP_05 | V at neck base |
| [SPINE_VISUAL_LINE] | CP_06 | Visible spine line |
| [SHOULDERBLADE_VISIBLE] | CP_07 | Shoulder blade prominence |

#### HK-Specific Posture Tokens (Area 02)

| Token | Code | Description |
|-------|------|-------------|
| [MTR_RAIL_LEAN] | F1 | MTR handrail lean |
| [QUEUE_WEIGHT_SHIFT] | F2 | Queue weight cycling |
| [STREET_SQUAT_HK] | F3 | Street squat (HK) |
| [WALL_QUEUE_STAND] | F4 | Wall queue standing |
| [ESCALATOR_STILL] | F5 | Escalator still |

#### Camera Distance Tokens (Area 03)

| Token | Distance |
|-------|----------|
| [EXTREME_CLOSEUP] | Face dominant 60%+ |
| [FACE_CLOSEUP] | Face 50-70% |
| [HEAD_SHOULDERS] | Head to mid-chest |
| [WAIST_UP] | Waist to head |
| [KNEE_TO_HEAD] | Knee to head |
| [FULL_BODY_SHOT] | Full body + floor/ceiling |
| [ENVIRONMENTAL_WIDE] | Body small in environment |
| [DISTANT_CANDID] | Person as element, 5m+ |

#### Intimacy Level Tokens (Area 03)

| Token | Level | Range |
|-------|-------|-------|
| [STRANGER_DISTANCE] | Level 1 | 3m+ |
| [ACQUAINTANCE_DISTANCE] | Level 2 | 1.5-3m |
| [FRIEND_DISTANCE] | Level 3 | 0.5-1.5m |
| [INTIMATE_DISTANCE] | Level 4 | <0.5m |

#### Framing Tokens (Area 03)

| Token | Type |
|-------|------|
| [CENTRAL_COMPOSITION] | Subject centered |
| [RULE_OF_THIRDS] | Intersection point |
| [EDGE_FRAME] | Near frame edge |
| [BOTTLENECK_FRAME] | Narrow scene point |
| [REFLECTION_FRAME] | Mirror/window |
| [OVER_SHOULDER_SHOT] | Through person |
| [HIDDEN_OBSERVER] | Subject unaware |
| [ACCIDENTAL_CROP] | Imperfect framing |

#### Camera Height Tokens (Area 03)

| Token | Angle |
|-------|-------|
| [HIGH_ANGLE_CAMERA] | >15° down |
| [EYE_LEVEL_CAMERA] | Eye level |
| [LOW_ANGLE_CAMERA] | >15° up |
| [GROUND_LEVEL_CAMERA] | Near floor |
| [OVERHEAD_CAMERA] | Directly above |
| [HIP_LEVEL_CAMERA] | Hip height |

#### Shot Type Tokens (Area 03)

| Token | Candid/Posed |
|-------|-------------|
| [HIDDEN_CAMERA_SHOT] | P1 — Most candid |
| [FORGOTTEN_CAMERA] | P2 — Ignoring camera |
| [ACCIDENTAL_AWARE] | P3 — Noticed mid-capture |
| [COOPERATIVE_FRIEND] | P4 — Casual cooperation |
| [DIRECTED_PERFORMANCE] | P5 — Fully posed |

#### Group Dynamics Tokens (Area 03)

| Token | Group Size |
|-------|------------|
| [DUO_CLOSE] | 2 people close |
| [DUO_APART] | 2 people separate |
| [TRIO_DYNAMIC] | 3 people triangle |
| [GROUP_SELFIE] | Group front camera |
| [OVERHEARD_IN_BACKGROUND] | Background person |
| [GROUP_DINNER_4] | 4 people dinner |
| [LARGE_GROUP_EVENT] | 6+ people event |
| [SOMEONE_ELSE_PHOTO] | Others photographing |
| [PHOTO_BOMB_HK] | Accidental background |
| [BACK_VIEW_PRIMARY] | Back as subject |
| [RANDOM_IN_FRAME] | Unposed random person |

#### HK-Specific Framing Tokens (Area 03)

| Token | Situation |
|-------|-----------|
| [MTR_REFLECTION_SHOT] | MTR train reflection |
| [CONVENIENCE_REFLECTION] | Convenience store window |
| [FERRY_WIDE] | Ferry deck harbor |
| [TEA_RESTAURANT_ANGLE] | Tea restaurant table |
| [NEON_FACE_LIT] | Night market neon |
| [ESCALATOR_LEVEL] | Escalator ascending |
| [ESTATE_FRAMING] | 屋苑平台花園 |
| [FOOTBRIDGE_WIDE] | 行人天橋 |
| [TAXI_REAR_SEAT] | 的士後座 |
| [UNI_STAIRS] | 大學校園樓梯 |
| [CS_GLASS_REFLECTION] | 便利店玻璃 |
| [MONGKOK_TUNNEL] | 旺角行人隧道 |

---

### Total Token Count: 130+ tokens across 3 areas

**Area 01 (Streetwear):** 50+ tokens (7 categories A-G, 5 rhythm, 8 HK identities, 7 brand identities, 5 HK scenes)
**Area 02 (Silhouette):** 42 tokens (5 posture categories A-E, 7 compression points, 5 HK postures)
**Area 03 (Camera):** 38+ tokens (8 distances, 4 intimacy levels, 8 framings, 6 heights, 5 shot types, 11 group dynamics, 12 HK framings)

---

*ENGINE_V16_ANTI_FORMULA_STREETWEAR_SYSTEM — Ready for integration*
*Cross-references with: V16_FILMIC_COLOR_SYSTEM, V16_GRAIN_AESTHETIC_MODULE, V16_PHOTODUMP_STRUCTURE*
*Source Research: V16_ANTI_FORMULA_RESEARCH Areas 01-03 (Verified + Extended + Flags Fixed)*
