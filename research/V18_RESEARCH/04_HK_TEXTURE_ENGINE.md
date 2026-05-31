# HK Texture Engine — V18

## Philosophy

Generic Hong Kong prompts produce generic results. AI models generate "Hong Kong" as a collision of neon and skyscrapers — a stereotype stripped of soul. The city that photographers like **Fan Ho**, **Brian Ching**, **Kelvin Lam**, and **Eric Leung** captured is a city of **compressed density**, **humid decay**, **contradictory signage**, and **hyper-specific locality**. Every district breathes differently. Sham Shui Po has a different texture than Mong Kok. A wet market smells different than a cha chaan teng. V17 could not distinguish these micro-layers. V18 must.

---

## Token 01 — MONG KOK SIGNAGE LAYER

**Problem Statement**
Generic HK images show "neon signs." This is false. Mong Kok's signage is a **vertical collision** of hand-painted shop signs, peeling vinyl stickers, religious notices, Cantonese characters in varying font weights, and government health warnings layered at 3–4 depths. No two signs share the same material condition. AI models flatten this into "colorful backgrounds."

**Why V17 Cannot Solve It**
V17 recognized "Hong Kong signage" as a single texture class. It could not distinguish between: a fading 家俬 storesign, a fresh bubble tea vinyl, a 燒味 restaurant hanging board, and a Trolleybuses route sticker. These exist in different material states, lighting angles, and decay gradients simultaneously.

**Real Photography References**
- Fan Ho's 1950s–70s Mong Kok work (sharp shadows, single-source tungsten, wet pavement reflection)
- Kelvin Lam's Mong Kok series (desaturated, high contrast, layered glass)
- Brian Ching's night market studies (overexposed neon bleeding into tungsten)

**Local Behavioral Logic**
Shop owners in Mong Kok add signs without removing old ones. Religious pamphlets from 天后廟 sit next to condom ads next to property flyers. The street-level visual is a palimpsest — new ink on old ink on older ink. Residents do not see clutter; they see accumulated proof of commerce survival.

**Visual Evidence**
- Staggered vertical sign placement (signs hung at varying heights, not aligned)
- Mixed media: painted metal, vinyl sticker, handwritten red运气纸, printed A4 laminated
- Color temperature collision: warm tungsten inside shops, blue LED outside, green health posters
- Humidity haze: slight bloom on distant signs during summer
- Density: 15–30 visible sign faces in a single 90° street view

**Prompt Vocabulary**
```
 Mong Kok signage palimpsest, layered 街招, peeling vinyl 膠牌, hand-painted 漆字,
 faded 家俬 shop sign, stacked religious pamphlet, health notice 告示, wet路面反光,
 tungsten shop-front glow, blue LED signage bleed, mixed Chinese typeface collision,
 vertically staggered shopfronts, Mong Kok 女人街 parallel signage wall
```

**Integration Rules**
- Use only with street-level Mong Kok prompts
- Pair with humidity/haze token for summer conditions
- Separate signage into 3 depth layers: foreground (peeling), mid-ground (shop-front), background (distant billboard)
- Do not align signs; force collision and stagger

**Anti-AI Benefits**
The organic decay patterns, sticker edge curling, and material weathering are statistically nearly impossible for AI to reproduce consistently. Generic "neon Hong Kong" is instantly identifiable. This token forces the chaotic material history that AI cannot hallucinate from memory.

**Example Prompt Fragments**
```
"wet Mong Kok night market, peeling 膠牌 signs at staggered heights, 
tungsten shop glow mixing with blue LED, handwritten 运气纸 under glass, 
humidity haze, 1980s 茶餐廳 facade, faded red gold characters over painted metal"
```

---

## Token 02 — SHAM SHUI PO TENEMENT LAYER

**Problem Statement**
AI models treat Sham Shui Po as "old HK" and produce brown/desaturated滤镜. Real Sham Shui Po tenement buildings are **structurally specific**: external metal staircases, window grilles (花碼),晾衫架 poles, subdivided units with mismatched window sizes, and a gray-green facade palette punctuated by neon shop signs. The district has a vertical logic AI ignores.

**Why V17 Cannot Solve It**
V17 had no concept of tenement architecture as a distinct visual system. It could not separate: external staircases (消防逃生梯) from window grilles from晾衫架 from subdivided unit windows. These elements exist in precise spatial relationships that define the district's character.

**Real Photography References**
- Fan Ho's Sham Shui Po street work (long shadows, laundry poles, children on tenement steps)
- Eric Leung's 公屋 studies (geometric window grille patterns,晾衫架 diagonals)
- Social documentary work by 大榮街拍

**Local Behavioral Logic**
Tenement residents use external space intensively. Clothes dry on window-facing poles. Air conditioners drip onto the street (造成水滴滴聲). Metal staircases are the primary vertical circulation, not internal hallways. The building facade is an active social surface.

**Visual Evidence**
- External metal staircase: open-riser, riveted, slightly rusting, attached to building face
- 花碼 window grilles: geometric metal patterns, unit-specific modifications
- 晾衫架: bamboo or plastic poles extended from windows at ~30° angle, clothes visible
- Window size variation: subdivided units have irregular window placement (not uniform grid)
- Ground floor: shop front with metal gate (鐵閘) rolled halfway open
- Facade color: 1960s–70s concrete with lime, gray-green, and faded orange paint

**Prompt Vocabulary**
```
 Sham Shui Po tenement, external metal 逃生梯, riveted open-riser staircase,
 花碼 window grille, subdivided unit irregular windows, bamboo 晾衫架 poles,
 air conditioner drip tray, 鐵閘 metal shop gate, lime-gray facade,
 1960s concrete texture, water stain streaks, Sham Shui Po 桂林街夜市,
 subdivided unit window collision, vertical laundry poles, building facade decay gradient
```

**Integration Rules**
- Pair with humidity token for authentic air conditioner drip effect
- Do not place windows in regular grid — force irregular subdivided layout
- External staircase must be attached to building face at slight angle, not centered
- Ground floor always: shop + half-open metal gate

**Anti-AI Benefits**
The irregular window placement from subdivision is statistically unique to Sham Shui Po and Sai Ying Pun. AI tends to generate regular grids. The specific riveted metal staircase construction is not in most training sets with this specificity.

**Example Prompt Fragments**
```
"Sham Shui Po tenement block, external 逃生梯 at building corner, irregular 花碼 grilles,
 bamboo poles extended at angles with clothes drying, water stains on gray-green facade,
 half-open 鐵閘 shop front, subdivided unit windows not aligned, humid afternoon haze"
```

---

## Token 03 — WET MARKET VISUAL SYSTEM

**Problem Statement**
Generic "Hong Kong market" produces a fish market with ice and blue tarps. Real wet markets have a **specific visual hierarchy**: hanging poultry (已劏), open drains, mosaic tile walls, scale weight stalls, plastic basin stacking, and a specific spectral quality from morning light hitting wet concrete and fish scales. The smell is visual.

**Why V17 Cannot Solve It**
V17 treated wet markets as "colorful local markets." It could not separate: butcher hanging meat from fish stall from vegetable stall from dried goods corner. These have completely different material cultures, lighting needs, and floor conditions. Wet market visual logic is a progression from wet (fish/poultry) to damp (vegetable) to dry (dried fish/ herbs).

**Real Photography References**
- Fan Ho's wet market work (shadow play between hanging meat and morning light)
- Local documentary photographer @wethehkers (G/F wet market realism)
- Kelvin Lam's market series (long exposure, empty market at dawn, mosaic tile reflections)

**Local Behavioral Logic**
Wet markets operate before 7am setup and after 12pm slowdown. The most visually dense period is 7–10am. Vendors display goods on tiered plastic basins, hang chickens by the feet, lay fish on ice over blue tarp. Customers bring their own plastic bags or baskets. Floor is constantly rinsed — wet concrete reflects ceiling-mounted fluorescent light differently than dry areas.

**Visual Evidence**
- Hanging poultry: white plastic string, hooks, feathers still visible, reddish skin tones
- Mosaic wall tiles: small white/green/blue squares, water-stained, at ~1.2m height
- Basin stacking: transparent plastic basins in 3-tier tiers, colored vegetables inside
- Open drains: metal grate covers, visible water flow toward drain
- Scale weights: brass analogue scale with metal pan, printed 價錢牌
- Ceiling: exposed pipes, fluorescent tubes (4000K, slightly flickering), cloth sun shades
- Floor: slightly sloped wet concrete, puddles reflecting fluorescent

**Prompt Vocabulary**
```
 Hong Kong 街市 wet market, hanging 已劏 poultry, white plastic string, hook,
 mosaic wall tile (白綠藍方磚), wet concrete floor, open metal drain grate,
 tiered 膠盆 vegetable display, brass analogue scale, fluorescent tube lighting,
 fish on blue tarp over ice, water reflection, humid morning market atmosphere,
 chicken feet dangling, fish scale glint, 7am setup hour, 魚檔 fish stall
```

**Integration Rules**
- Use dawn/early morning time token for authentic lighting (natural + fluorescent mix)
- Wet floor reflection is mandatory — always pair floor element with light source
- Separate market into wet zone (fish/poultry) and semi-dry zone (vegetable/dried)
- Mosaic tile always at waist height on walls

**Anti-AI Benefits**
The specific combination of mosaic tiles + fluorescent reflection + hanging meat + wet concrete is a highly specific visual system. AI separates these elements incorrectly or flattens them. The spectral quality of wet market lighting (yellow fluorescent + white morning light through tarp) is not commonly captured in training data.

**Example Prompt Fragments**
```
"early morning 街市, hanging chickens on white string, mosaic wall tiles at waist height,
 wet concrete reflecting fluorescent tubes, tiered 膠盆 vegetables, open drain,
 brass scale, fish on blue tarp, humid air, morning light through canvas shade,
 smell of sea and wet stone implied through visual texture"
```

---

## Token 04 — CHA CHAAN TENG INTERIOR LAYER

**Problem Statement**
AI generates "Hong Kong cafe" as: red leather booth, checkered floor, neon sign outside. This is cha chaan teng as caricature. Real cha chaan teng interiors are: plastic laminate tables (often floral pattern), metal folding chairs, ceiling fans on low speed, wall-mounted menus with tape repairs, fluorescent tubes behind plastic dividers, and a specific color temperature from mixing tungsten (food warmers) with fluorescent (general lighting).

**Why V17 Cannot Solve It**
V17 had no interior material system for cha chaan teng. It could not distinguish: the specific floral plastic laminate from the red leather of a Western diner, the metal folding chair from a normal chair, or the wall-mounted laminated menu (covered in tape marks) from a clean printed menu. These material specifics are the district's DNA.

**Real Photography References**
- Fan Ho's cha chaan teng photography (warm interior, patron anonymity, social document)
- Local food photographer @foodonherback (cha chaan teng interior studies)
- Instagram @cchc_chachaan (documentary interior series)

**Local Behavioral Logic**
Cha chaan teng is a speed-space. Customers read 3-minute menus, food arrives in 90 seconds. Interiors are designed for turnover: no cushions, hard surfaces, plastic laminate for wipe-clean. The visual clutter — menu tape, calendar, wall clock, condiment bottles — is functional, not decorative. Every item has a reason.

**Visual Evidence**
- Tables: rectangular plastic laminate, usually floral or marble pattern, slight wear at corners
- Chairs: metal folding chair, red rubber seat pad, sometimes plastic webbing
- Ceiling: dual-speed metal fan (轉速低), slightly tilted, fluorescent tube behind plastic cover
- Wall menu: laminated paper under glass, tape patches at corners, handwritten 追加 items
- Counter: stainless steel, visible steam marks, stacked bowls
- Condiment tray: dried chili in oil (指天椒), 胡椒瓶, 茄汁膠袋, soy sauce 膠袋
- Floor: small ceramic tile (馬賽克磚), usually green or brown, slightly cracked

**Prompt Vocabulary**
```
 cha chaan teng interior, floral plastic laminate table, metal folding chair,
 ceiling fan low speed, fluorescent tube plastic cover, laminated wall menu,
 tape patches on menu, stainless steel counter, steam marks, condiment tray,
 指天椒 dried chili oil, 胡椒瓶, 茄汁膠袋, ceramic tile floor, warm humid interior,
 morning light through window, 茶餐廳 speed-space, plastic chair
```

**Integration Rules**
- Interior temperature: always mix tungsten (counter/warmer) with fluorescent (general) — never single light source
- Condiment tray is mandatory: always includes 指天椒 and 茄汁膠袋
- Menu has tape marks — this is not damage, this is authenticity
- Floor tile is small format (50mm or smaller), cracked at entry points

**Anti-AI Benefits**
The specific floral plastic laminate pattern is extremely difficult for AI to reproduce accurately. The combination of object types (folding metal chair + ceiling fan + laminate table + laminated menu) at cha chaan teng scale is not well-represented in training data. AI tends toward Western diner or generic "Asian cafe" visual language.

**Example Prompt Fragments**
```
"Sham Shui Po cha chaan teng, floral plastic laminate table, metal folding chair,
 ceiling fan at low, laminated wall menu with tape patches, stainless counter,
 condiment tray with 指天椒 and 茄汁膠袋, green ceramic tile floor cracked at entrance,
 warm fluorescent-tungsten mix, humid breakfast hour, 7:30am customer rush"
```

---

## Token 05 — PUBLIC HOUSING BLOCK GEOMETRY

**Problem Statement**
AI produces "Hong Kong public housing" as: repetitive windows in a block, possibly a podium. Real HK public housing has specific typologies: Harmony 1/2/3 block configurations, single-tier vs double-tier/corridor access, specific window-to-wall ratios, laundry pole configuration rules, and color-coding by estate (MTR 太子, 旺角, etc. have estate-specific palettes). The geometry is systematic but not uniform.

**Why V17 Cannot Solve It**
V17 could not distinguish between Harmony 1 and Harmony 2 block types, could not identify single-loaded vs double-loaded corridor systems, and had no concept of estate-specific color coding. It generated generic concrete towers with window grids.

**Real Photography References**
- Eric Leung's public housing documentary series (geometry, laundry, window patterns)
- Instagram @hk.ura (Urban Renewal Authority housing studies)
- Kelso's public housing photography (interior corridor studies)

**Local Behavioral Logic**
Public housing residents use window space for laundry (晾曬), plant cultivation (陽台種植), and air conditioner installation (窗口機). The window grille (窗花) is always installed, often with varying patterns per unit. Laundry poles extend to specific angles — not random. The building base (platform/podium) has specific commercial uses (商場, 街市).

**Visual Evidence**
- Harmony 1: single corridor, windows on one side only, narrow profile
- Harmony 2: double corridor, windows both sides, wider block
- New Harmony: larger windows, rounded balcony edges, contemporary
- Window grille: 花碼 pattern, unit-specific modifications, often white or gray metal
- Laundry poles: bamboo or metal, extended at ~45°, clothes visible
- Air conditioners: stacked window units, drip trays, visible condensate pipe
- Building base: podium with commercial units, metal roller shutters
- Color coding: estate-specific (e.g., Lei Cheng Uk = blue/white, Lower Wong Tai Sin = orange/cream)

**Prompt Vocabulary**
```
 Hong Kong public housing Harmony block, single-loaded corridor, 花碼 window grille,
 bamboo laundry pole 45° extension, stacked window air conditioner, drip tray,
 podium commercial unit, metal roller shutter, estate-specific color coding,
 concrete texture with water stain, residential tower geometry, Harmony 1 type,
 Lower Wong Tai Sin estate orange facade, public housing typology
```

**Integration Rules**
- Specify Harmony type (1, 2, or new) — each has distinct geometry
- Estate color coding must be consistent with the estate type
- Laundry poles always at angle, never vertical
- Podium/base commercial use always visible at ground level
- Water stains run vertically on concrete (not random)

**Anti-AI Benefits**
The specific Harmony block typologies have precise geometric ratios that AI does not consistently reproduce. The combination of window grille patterns + laundry poles + stacked AC units is statistically unique to HK public housing. Estate color coding is a hyper-local detail AI conflates with "colorful buildings."

**Example Prompt Fragments**
```
"Harmony 1 public housing block, single-loaded corridor facade, 花碼 grilles on windows,
 bamboo laundry poles at 45°, stacked window AC units with drip trays,
 orange-cream Lei Cheng Uk estate palette, concrete with vertical water stains,
 podium commercial units with metal shutters, Lei Cheng Uk Estate, Kwun Tong,
 late afternoon shadow on concrete, humid summer"
```

---

## Token 06 — HONG KONG HUMIDITY ATMOSPHERE

**Problem Statement**
AI produces "humid" as: slight blur, desaturated colors, maybe some haze. Real Hong Kong humidity (avg 78–95% in summer) has specific visual markers: heat shimmer near ground, condensation on cold surfaces, haze gradient (not uniform), visible moisture on metal, specific color shift toward green-blue in distant views, and a particular quality of shadow that is never fully black.

**Why V17 Cannot Solve It**
V17 treated humidity as a single value (0–100% "humidity" prompt). It could not distinguish: morning humidity (95%, condensation-heavy, green cast) from afternoon humidity (78%, heat shimmer, blue cast) from post-rain humidity (100%, reflective everything, saturated colors). These are completely different visual systems.

**Real Photography References**
- Fan Ho's summer Hong Kong work (heat shimmer, shadow softness, haze quality)
- Kelvin Lam's summer series (blue-green distant haze, condensation details)
- Brian Ching's pre-rain humidity studies

**Local Behavioral Logic**
HK humidity follows a daily cycle. Morning (6–9am): condensation on every cold surface, visibility reduced, green-gray palette. Midday: heat shimmer begins at street level, haze rises. Afternoon: blue-white haze, heat distortion visible. Evening: humidity rises again, condensation returns. Post-rain: 100% humidity, every surface wet, maximum saturation.

**Visual Evidence**
- Condensation: water droplets on metal surfaces, plastic, glass (not uniform film)
- Heat shimmer: distortion near ground level, strongest 2–4pm
- Haze gradient: thicker at eye level, clearer above rooftop line, blue-white shift
- Shadow quality: never pure black, always warm-tinted from scattered light
- Color shift: greens push toward blue-green, reds push toward orange, whites become cream
- Visibility: street-level visibility ~60–70% at high humidity, not fog density

**Prompt Vocabulary**
```
 Hong Kong summer humidity, 95% condensation, water droplet on metal surface,
 heat shimmer street level, blue-white haze gradient, green cast morning humidity,
 shadow not pure black, warm scattered light, humid air density, visibility 60%,
 post-rain humidity 100%, wet surface reflection, cream white balance,
 afternoon heat distortion, humid evening condensation, MTR station condensation
```

**Integration Rules**
- Time of day is mandatory with humidity token — morning/afternoon/post-rain produce different results
- Humidity must be expressed as condensation OR heat shimmer, not both (they occur at different times)
- Color temperature shift: morning = green-gray, afternoon = blue-white, post-rain = saturated
- Shadow warmth: always tint shadows warm (slightly orange), never cool or black

**Anti-AI Benefits**
Heat shimmer and condensation physics are difficult for AI to simulate. The specific HK humidity color shift (green-gray morning, blue afternoon) is based on real atmospheric data. Generic "humid" from AI does not differentiate by time of day or produce the specific color temperature shifts.

**Example Prompt Fragments**
```
"9am Mong Kok, 95% humidity, condensation droplets on metal signage,
 green-gray morning palette, shadow warmth not black, street-level visibility 60%,
 slight haze at eye level, cream white balance, wet market floor reflection,
 warm scattered light in alley, humid morning air density"
```

---

## Token 07 — OLD MALL DECAY SYSTEM

**Problem Statement**
AI produces "Hong Kong old mall" as: 1990s mall with generic Asian decor. Real old HK malls (the 1980s–90s era: 美好年代) have specific decay markers: cracked mosaic floors, faded gold accent paint, water-stained gyptile ceilings, roller-shutter closed shops, specific fluorescent tube arrangements, and a specific population demographic (elderly residents, small-batch traders, not tourists).

**Why V17 Cannot Solve It**
V17 could not distinguish between a functioning mall and a dying mall. It had no concept of: roller-shutter percentage (how many shops are closed vs open), specific decay material system (gyptile + mosaic + faded gold), or the specific social use (elderly sitting area, chess players, not foot traffic).

**Real Photography References**
- Local photographer @oldhkstyle (1980s–90s mall documentation)
- Instagram @wan_chai_rate (Wan Chai old mall studies)
- Photographer David shares: 舊商場 series

**Local Behavioral Logic**
Old malls serve the elderly and working-class residents who cannot afford newer spaces. They become informal social spaces: elderly chess games at center court, domestic workers on days off, small traders (衣服改褲, 鎖匙配) using mall as front. Shops that close leave roller shutters permanently down. The mall slowly transitions from commercial to community social space.

**Visual Evidence**
- Floor: small ceramic mosaic tile (30–50mm), cracked, faded, not reflective
- Ceiling: gyptile (石膏板) with water stains, fluorescent tube in metal housing
- Gold accents: 1980s gold paint on trim, now oxidized/tarnished to bronze-green
- Roller shutters: 70–80% of shops closed, metal shutters with rust patches
- Open shops: small trader (改衣, 鎖匙, 手機貼膜), very specific
- Seating area: plastic chairs, elderly residents, chess table
- Population: elderly, domestic workers, not young/tourist demographic
- Signage: faded 出租 unit signs, old POS terminal visible through glass

**Prompt Vocabulary**
```
 1980s Hong Kong old mall, cracked mosaic tile floor, water-stained gyptile ceiling,
 oxidized gold trim, 70% roller shutter closed, small trader open shop,
 elderly residents chess table, domestic workers on plastic chairs,
 fluorescent tube metal housing, faded gold accent, dying mall atmosphere,
 美好年代 mall, Wan Chai old mall interior, small-format tile floor,
 mall center void, informal social space, non-tourist demographic
```

**Integration Rules**
- Specify roller-shutter percentage — empty mall without this reads as "nighttime" not "decaying"
- Elderly/social use must be present — empty mall without people reads as "abandoned" not "transitioning"
- Gold accent must be oxidized (not bright gold) — bright gold = new construction, not old mall
- Small-format mosaic tile (not large format) is critical for authenticity

**Anti-AI Benefits**
The specific decay material system (gyptile + oxidized gold + cracked mosaic) and social use pattern (elderly chess, small traders) is statistically unique to HK's 1980s–90s malls. AI cannot consistently produce the roller-shutter density + social demographic combination.

**Example Prompt Fragments**
```
"1980s Sham Shui Po mall, 70% roller shutters down, mosaic tile floor cracked,
 gyptile ceiling water stains, oxidized bronze-gold trim, elderly chess players,
 domestic worker on plastic chair, fluorescent tubes in metal housing,
 small 改衣 trader open shop, faded 出租 signs, humid stale air, no foot traffic"
```

---

## Token 08 — HONG KONG NIGHT LIGHT COLLISION

**Problem Statement**
AI produces "Hong Kong night" as: neon pink-blue dominant palette, sharp contrast. Real HK night has a specific light collision system: tungsten (warm, 2700K), fluorescent (cool, 4000K), neon (red/green/yellow, specific to shop type), LED (white/blue), and natural sky (deep blue, 6800K). These exist simultaneously and create specific color bleeding at boundaries.

**Why V17 Cannot Solve It**
V17 could not manage multi-source light collision. It defaulted to dominant single-source (usually neon) or failed to show how different color temperatures interact at object surfaces. It could not show: red neon reflecting on wet pavement, blue LED mixing with yellow tungsten at a shop front, or deep blue sky conflicting with warm street-level light.

**Real Photography References**
- Fan Ho's night work (single-source tungsten with shadow, no mixed light — but the absence is informative)
- Brian Ching's mixed-source night photography (actual collision of sources)
- Instagram @hklightstudy (light source studies)

**Local Behavioral Logic**
HK night has no single dominant light source. Each shop maintains its own lighting regardless of neighbors. A 燒味 shop runs warm tungsten. Next door a phone shop runs blue-white LED. Across the street a 藥房 runs green neon. Wet pavement acts as a horizontal reflector that mixes all sources into a single warm-tinted surface.

**Visual Evidence**
- Tungsten: 2700K, warm yellow, from food establishments and residential windows
- Fluorescent: 4000K, cool white, from wet markets, offices, under canopy lighting
- Neon: red (food), green (pharmacy), yellow (jewelry/money changer), specific to shop type
- LED: white/blue, from electronics shops, modern retail
- Sky: deep blue-black, 6800K, visible between buildings
- Reflection: wet pavement mixes all sources into warm-tinted horizontal plane
- Color bleeding: red neon bleeds into adjacent surfaces, green pharmacy neon reflects on glass
- Shadow: from tungsten only (dominant at street level), other sources too diffuse for hard shadow

**Prompt Vocabulary**
```
 Hong Kong night light collision, mixed 2700K tungsten, 4000K fluorescent,
 red 燒味 neon, green 藥房 neon, blue-white LED phone shop, deep blue sky 6800K,
 wet pavement multi-source reflection, color temperature bleeding, red neon on wet surface,
 green pharmacy glow on glass, yellow jewelry neon, shadow from tungsten only,
 Mong Kok night market light mix, multi-source night photography
```

**Integration Rules**
- Minimum 3 light sources required in any HK night scene (tungsten + fluorescent + one neon color)
- Wet pavement is the color-mixing surface — always include wet floor with night lights
- Sky must be deep blue-black, not black — HK night sky has light pollution but retains blue
- Color bleeding at object edges is mandatory — light sources do not stay in their lanes
- Shadow only from tungsten — other sources too diffuse

**Anti-AI Benefits**
Real multi-source light collision is one of the most difficult lighting systems to reproduce. AI tends to either dominant single-source (all neon or all tungsten) or fails at color bleeding. The specific HK shop-type-to-neon-color correlation (pharmacy = green, food = red) is hyper-local knowledge AI lacks.

**Example Prompt Fragments**
```
"Mong Kok night, red neon 燒味 sign, green 藥房 neon, blue LED phone shop,
 warm tungsten window light, wet pavement reflecting all sources,
 color bleeding at shop edge, deep blue-black sky between buildings,
 2700K warm shadow, fluorescent under canopy, mixed night light collision,
 street-level reflection"
```

---

## Token 09 — HONG KONG SIGNBOARD LANGUAGE

**Problem Statement**
AI produces Chinese characters but gets context wrong. Real HK signboards have a specific typographic system: traditional characters (not simplified), specific font choices (魏碑, 隸書, 超明體 for traditional; rarely used), mixed Chinese-English (茶餐厅 menu system), and most critically: the way characters are spatially arranged for phonetic reading (Cantonese reading order differs from Mandarin).

**Why V17 Cannot Solve It**
V17 had no Cantonese-specific typographic system. It could not distinguish: when a sign uses 靑 (traditional) vs 青 (simplified), when font choice signals shop type (冰室 font vs 酒樓 font vs 藥房 font), or how Cantonese reading order (left-to-right or vertical-top-to-bottom) differs from Mandarin conventions.

**Real Photography References**
- Fan Ho's sign studies (typography as social document)
- Local typography archive @hongkongtype
- Design studio @publicrecordhk (signage typography research)

**Local Behavioral Logic**
HK sign typography is read as sound first, meaning second. Cantonese has 9 tones and many homophones. Signs use typography to maximize phonetic distinctiveness. Font choice signals shop era: 超明體 (1950s–60s), 勘亭流 (1970s–80s food), 隸書 (1980s–90s), modern sans-serif (post-2000). A shop's font is its birth certificate.

**Visual Evidence**
- Traditional characters only: 靑/銀/雲/書 (not simplified equivalents)
- Font era markers: 超明體 (1950s–60s, food), 勘亭流 (1970s–80s, cha chaan teng), 隸書 (1980s–90s), 魏碑 (institutional)
- Mixed Chinese-English: 茶餐廳 menu format (中文 + English item names, not translated)
- Reading order: vertical top-to-bottom OR left-to-right, never right-to-left (that's Mandarin/Japanese)
- Shop-type font correlation: 冰室 = 超明體/勘亭流, 酒樓 = 隸書, 藥房 = modern sans, 髮型屋 = 超明體
- Material: painted metal, vinyl sticker, hand-painted, backlit acrylic
- Decay: rust on metal, sticker edge curl, paint chalking, crack along stroke

**Prompt Vocabulary**
```
 Hong Kong traditional characters, 靑銀雲書, 超明體typography, 勘亭流 food shop,
 隸書 traditional, 魏碑 institutional, Cantonese reading order, mixed Chinese-English menu,
冰室字體, 酒樓字體, 藥房字體, hand-painted sign, painted metal sign decay,
 rust chalking, sticker curl, traditional character set, HK typography era system,
 shop-type font correlation, phonetic readability, backlit acrylic sign
```

**Integration Rules**
- Match font era to shop type and approximate year of establishment
- Traditional characters only — simplified is an immediate authenticity breaker
- Vertical AND horizontal reading orders both acceptable — right-to-left only for specific retro Japanese-influenced contexts
- Decay on sign must be material-appropriate: rust on metal, peeling on vinyl, chalking on paint
- Font correlation (冰室=超明體) is hyper-specific and increases authenticity significantly

**Anti-AI Benefits**
The specific HK typography era system + traditional character set + shop-type correlation is extremely difficult for AI. AI frequently uses simplified characters (by mistake), uses wrong font era, or uses Mandarin reading order. This token forces traditional + era-correct + shop-appropriate typography.

**Example Prompt Fragments**
```
"1960s-style 冰室 sign, 超明體 hand-painted characters, traditional 靑銀雲書,
 painted metal sign with rust chalking, vertical reading order, warm tungsten backlight,
 faded paint at stroke edges, Hong Kong typography era marker, Cantonese phonetic arrangement,
 超明體 food shop era, shop-type font correlation correct, aged metal substrate"
```

---

## Token 10 — PUBLIC HOUSING LAUNDRY SYSTEM

**Problem Statement**
AI produces "laundry" as: white sheets on clothesline, generic. Real HK public housing laundry is a specific visual system: bamboo poles at precise angles, specific fabric colors (white vests, colored睡衣, school uniforms), the 竹竿 (bamboo) vs 鐵竿 (metal pole) distinction, and the way laundry interacts with window grille (花碼) geometry.

**Why V17 Cannot Solve It**
V17 could not distinguish between public housing laundry (bamboo pole, specific colors) and village house laundry (different pole system) or private residence laundry (balcony system). It had no concept of: the specific 45° angle rule, the 花碼 window grille interaction, or the specific fabric color palette of HK public housing residents.

**Real Photography References**
- Eric Leung's public housing laundry studies (geometry, fabric, color)
- Fan Ho's tenement laundry work (bamboo pole diagonals, shadow)
- Instagram @laundryhk (dedicated HK laundry photography)

**Local Behavioral Logic**
Public housing residents hang laundry outside windows because indoor drying space is insufficient (units are 26–40 sq meters). Bamboo poles are inserted through window grille gaps and extended to ~45°. School uniforms (white shirt, navy pants/skirt) are laundered and hung prominently.睡衣 (sleepwear) in pastel colors is common. Nothing is synthetic-looking — these are cotton blends dried in humid air.

**Visual Evidence**
- Bamboo poles: 竹竿, natural light brown, diameter ~25mm, extended through 花碼 gap at ~45°
- Metal poles: 鐵竿, gray metal, newer installations, less character
- Fabric: white cotton school uniforms, pastel睡衣, colored 內衣, no synthetic bright colors
- Pattern interaction: laundry fabric against 花碼 window grille creates half-transparent pattern
- Shadow: fabric shadow on building facade, soft-edged, warm (from sunlight)
- Position: always external to window, visible from street level, at multiple floors
- Time: most visible mid-morning (10am–12pm) when residents flip/collect laundry

**Prompt Vocabulary**
```
 public housing bamboo 竹竿 laundry, 45° pole angle, 晾衫架 system,
 white cotton school uniform, navy校服, pastel睡衣, 花碼 window grille interaction,
 fabric half-transparent pattern, public housing laundry geometry, natural bamboo pole,
 mid-morning Hong Kong public housing, fabric shadow on facade, cotton blend laundry,
 Sham Shui Po public housing laundry, laundry visible from street level
```

**Integration Rules**
- Bamboo pole angle ~45° is mandatory — vertical or horizontal reads as wrong
- Fabric colors: white + navy + pastel only — no bright synthetic colors (unrealistic for public housing)
- Multiple floors visible — single-floor laundry is not authentic
- 花碼 interaction: fabric against window grille creates pattern that must be implied in lighting

**Anti-AI Benefits**
The specific bamboo pole geometry + 花碼 interaction + public housing fabric palette is statistically unique to HK public housing. AI generates generic "laundry on line" without these micro-details. The 45° bamboo pole angle is a specific material behavior AI does not consistently reproduce.

**Example Prompt Fragments**
```
"Sham Shui Po public housing, bamboo 竹竿 extended at 45° through 花碼 grilles,
 white校服 and navy校服 hanging, pastel睡衣, cotton fabric in humid morning air,
 fabric pattern against window grille, multiple floors visible, soft shadow on facade,
 natural bamboo texture, 10am laundry hour, laundry swaying slightly"
```

---

## Token 11 — KOWLOON WALLS TYPOLOGY

**Problem Statement**
AI produces "Hong Kong wall" as: graffiti, concrete. Real HK walls have specific typologies: Tong Lau (唐樓) external walls with tile patterns, government wall murals (Bidet 1990s style), construction site walls (金屬圍板) with specific typography, and the specific patina of 50-year-old masonry in Mong Kok/Yau Ma Tei.

**Why V17 Cannot Solve It**
V17 could not distinguish between: Tong Lau tile wall vs public housing concrete vs construction 金屬圍板. It had no concept of the specific HK government mural style (1990s health campaign aesthetic), the 金屬圍板 typography system, or the way moisture creates specific patina patterns on old masonry.

**Real Photography References**
- Instagram @kowloonwalls (documentary wall series)
- Local photographer @tonglaudistrict (唐樓 tile wall studies)
- 大榮街拍 wall studies

**Local Behavioral Logic**
HK walls are social surfaces. Government uses them for health campaigns (控煙, 愛滋病). Property developers use 金屬圍板 for branding. Residents of 唐樓 have tile facades maintained (or not) by owners. The wall tells you who controls that vertical surface and when.

**Visual Evidence**
- Tong Lau tile wall: small-format ceramic tile (75mm), two-tone or three-tone, moisture-stained
- Government mural: 1990s health campaign aesthetic, bold graphic style, specific color palette (red/white/blue)
- 金屬圍板: corrugated metal construction fence, developer branding, 2010s+ style
- Masonry patina: lime deposit streaks, black mold at base, cracking pattern specific to HK humidity
- Graffiti: tag-style, Cantonese characters, not mural-style
- Utility surface: electrical box, junction box, transformer, painted but peeling

**Prompt Vocabulary**
```
 Tong Lau tile wall facade, two-tone ceramic tile, moisture stain streaks,
 1990s government health mural, bold graphic style, 金屬圍板 corrugated metal fence,
 developer branding, masonry patina, lime deposit, black mold base,
 Cantonese tag graffiti, utility box, electrical junction, Yau Ma Tei wall typology,
 50-year-old masonry texture, vertical moisture gradient
```

**Integration Rules**
- Specify wall type: Tong Lau (tile), government (mural), construction (圍板), or residential (concrete/masonry)
- Moisture gradient on masonry: always darker at base, lighter at top
- 1990s government mural has specific graphic style: bold outline, simplified figure, red-white-blue palette
- 金屬圍板 always has developer branding — no blank construction fence

**Anti-AI Benefits**
The specific HK wall typology (Tong Lau tiles + 1990s mural + 金屬圍板 + masonry patina) is extremely location-specific. The moisture patina on old masonry has specific chemical composition from HK humidity (lime + mold + pollution). AI cannot consistently produce these material systems with location accuracy.

**Example Prompt Fragments**
```
"Yau Ma Tei Tong Lau, two-tone ceramic tile wall, moisture streak vertical gradient,
 black mold at base, 1990s health campaign mural, bold simplified figure,
 faded red-white-blue palette, masonry patina, Cantonese tag at lower wall,
 humid afternoon, aged tile surface, building facade wall typology"
```

---

## Token 12 — HONG KONG FERRYLIGHT SYSTEM

**Problem Statement**
AI produces "Hong Kong ferry" as: generic boat, maybe Victoria Harbour backdrop. Real Hong Kong ferry light has specific characteristics: the yellow-orange of the 燃燒器 (burner) in the engine room visible through hull gaps, the blue-white of navigation lights, the way ferry decks reflect in water at night, and the specific wind environment on the lower deck.

**Why V17 Cannot Solve It**
V17 could not distinguish between: Star Ferry (green and white livery, amber interior light), Ferry pier navigation lights (green/red), and the water reflection system specific to Victoria Harbour (tidal current + ferry wake + street light reflection). It had no concept of the specific ferry deck material or the wind-rain interaction on lower deck.

**Real Photography References**
- Fan Ho's ferry photography (the lower deck social space, people between light and shadow)
- Kelvin Lam's Victoria Harbour night series (ferry light reflection system)
- Instagram @starferry (documentary ferry studies)

**Local Behavioral Logic**
The Star Ferry crossing is a liminal space. Lower deck passengers (mostly working-class, elderly) sit in a specific light environment: amber engine room glow from below, blue-green harbor light from porthole, wind and spray. The upper deck is tourist space, different light, different posture, different social texture.

**Visual Evidence**
- Star Ferry hull: green and white livery, riveted steel, salt corrosion pattern
- Lower deck: wooden bench seating (green painted), amber light from engine room below
- Porthole: small round window, slightly fogged, blue-green harbor light
- Deck material: painted steel, slightly uneven, grip pattern
- Water: dark harbor water (not blue), ferry wake white, street light reflection (orange dots)
- Wind environment: hair/clothes movement, spray on lower deck in rain
- Navigation lights: green (port), red (starboard), white (masthead)

**Prompt Vocabulary**
```
 Star Ferry lower deck, wooden bench green paint, amber engine room glow below,
 small porthole blue-green harbor light, riveted steel hull, salt corrosion,
 painted steel deck, dark harbor water, orange street light reflection dots,
 ferry wake white, lower deck wind environment, Hong Kong ferry light system,
 working-class passenger, social document, spray on deck in rain
```

**Integration Rules**
- Specify Star Ferry vs other ferry — color livery differs
- Lower deck vs upper deck produces completely different light/social environment
- Harbor water is dark (not blue), reflections are orange-white (not blue reflection)
- Engine room amber glow is visible through gaps — this is a key authenticity marker

**Anti-AI Benefits**
The specific amber engine room light + blue porthole light + dark harbor water reflection system is a unique visual environment. AI conflates ferry photography with generic boat photography. The social document aspect (lower deck as working-class liminal space) is not captured in generic "Hong Kong ferry" prompts.

**Example Prompt Fragments**
```
"Star Ferry lower deck at night, green painted wooden bench, amber light from engine room below,
 porthole casting blue-green harbor light on deck, riveted steel hull with salt corrosion,
 dark harbor water, orange street light reflection, spray on deck in rain,
 wind in passenger hair, working-class passenger, liminal ferry space,
 humid night crossing, Victoria Harbour"
```

---

## Token 13 — YA U MA TEI GHOST SIGN LAYER

**Problem Statement**
AI produces no ghost signs or incorrect ghost signs. Real Yau Ma Tei has ghost sign layers: old painted signs from the 1950s–70s visible under current signage, fading on building facades, and a specific palette (chrome, red, white, black) from that era. Ghost signs in HK are being demolished — they have ~10 years of documented life left.

**Why V17 Cannot Solve It**
V17 could not distinguish between: old painted ghost sign (1950s–70s chrome + red palette) vs faded vinyl sign (1990s) vs chalked concrete (very old). It had no concept of the specific ghost sign palette, the way ghost signs appear as shadow-faded areas when current sign is removed, or the building facade condition that preserves ghost signs.

**Real Photography References**
- Instagram @ghostsignshk (HK ghost sign documentation)
- Local preservation group documentation
- Fan Ho's signage studies (some ghost signs visible in his work from the 1960s)

**Local Behavioral Logic**
Ghost signs survive in Yau Ma Tei because buildings are old and owners defer maintenance. The ghost sign is visible when: current signage partially脱落 (falls off), or building repaints over partial area leaving some coverage. Chrome ghost signs were painted with LEAD-BASED paint (now illegal), giving them a specific reflectivity that fading cannot fully erase.

**Visual Evidence**
- Ghost sign type: 1950s–70s painted metal sign, chrome and red palette, white outline
- Chrome paint: lead-based, retains slight reflectivity even when faded
- Fading pattern: character stroke edges remain sharp while field color fades
- Building facade: lime-wash or paint, moisture-stained, ghost sign area better preserved
- Current sign: partially covering ghost sign, creating layered collision
- Common ghost sign content: tobacco, medicine, soda (1950s consumer culture)
- Location: Yau Ma Tei, Mong Kok, Sham Shui Po — old commercial districts

**Prompt Vocabulary**
```
 ghost sign, old painted sign, chrome red palette, lead-based chrome paint,
 fading character strokes, building facade moisture-stained, ghost sign shadow area,
 partially covered by current sign, 1950s consumer culture, tobacco medicine,
 Yau Ma Tei ghost sign, layered signage collision, chrome reflectivity,
 lime-wash facade, building facade preservation, ghost sign documentation
```

**Integration Rules**
- Ghost sign requires old building facade — new construction cannot have ghost signs
- Chrome ghost sign palette: red + chrome + white + black only (not multicolor)
- Ghost sign appears as "better preserved area" where current sign partially covers
- Fading must follow stroke pattern, not random blotches

**Anti-AI Benefits**
Ghost signs in HK are a dying document of pre-1970s commercial culture. The specific chrome + red palette from that era and the lead-based paint reflectivity are extremely specific. AI cannot consistently produce ghost sign fading patterns or the specific HK ghost sign palette.

**Example Prompt Fragments**
```
"Yau Ma Tei old building, ghost sign chrome red paint, partially visible under current signage,
 lead-based chrome reflectivity still visible, fading at field not stroke,
 moisture-stained facade, 1950s tobacco ghost sign, layered signage collision,
 building facade preservation, faded character strokes, aged building"
```

---

## Token 14 — HONG KONG PUBLIC LIGHTING SPECIFICITY

**Problem Statement**
AI produces generic street lighting. Real HK street lighting has specific characteristics: the orange of HK street lamps (sodium vapor, 2000K), the way they create halos in humid air, the specific 路灯 (street lamp) post design (concrete or metal, specific arm configuration), and the way street light interacts with wet pavement.

**Why V17 Cannot Solve It**
V17 had no concept of HK-specific street light color temperature, no concept of the specific post types (concrete vs metal arm), and could not simulate the sodium vapor halo effect in humid air. It treated street lighting as generic orange light, not as a specific atmospheric system.

**Real Photography References**
- Brian Ching's street light studies (sodium vapor halo, humidity interaction)
- Kelvin Lam's night street series (road light on wet surface)
- Fan Ho's night street work (single source tungsten street light era — pre-LED)

**Local Behavioral Logic**
HK street lighting follows district age. Old districts (Yau Ma Tei, Sham Shui Po) still have sodium vapor orange lights (2000K). Newer districts have LED (4000K+). Some transitional streets have both simultaneously. The orange sodium vapor light creates distinctive halos in humid air — a blue-white fog ring around each lamp visible at night.

**Visual Evidence**
- Sodium vapor lamp: 2000K, deep orange, concrete post or curved metal arm
- LED lamp: 4000K+, white, modern cobra head or shoebox fixture
- Halo effect: blue-white fog ring around lamp visible in humid air, 2–3x lamp diameter
- Wet pavement: orange light reflected as elongated pool, not point source
- Transition street: both lamp types visible simultaneously (old + new districts)
- Alley lighting: single bulb, no fixture, exposed wire, directly visible
- MTR exit lighting: fluorescent strip, bright white, under canopy

**Prompt Vocabulary**
```
 Hong Kong street light, sodium vapor 2000K orange, concrete lamp post,
 metal curved arm, blue-white humidity halo, halo ring 2x lamp diameter,
 wet pavement orange reflection, elongated light pool, alley single bulb,
 exposed wire, MTR exit fluorescent strip, orange sodium vapor,
 mixed old-new street light, humid night air, street lamp post concrete
```

**Integration Rules**
- Specify district age — old district (Yau Ma Tei) = sodium vapor only, new district = LED only
- Halo effect only with sodium vapor in humid conditions
- Wet pavement reflection is elongated (not circular point source)
- Alley single bulb is always slightly swaying (visual marker of authenticity)

**Anti-AI Benefits**
The specific Hong Kong sodium vapor halo effect in humid air is a physically distinctive phenomenon. The concrete post design and curved metal arm configurations are district-specific. AI produces generic "orange street light" without the halo physics or post-specific geometry.

**Example Prompt Fragments**
```
"Sham Shui Po night, sodium vapor street lamp 2000K orange, concrete post,
 blue-white humidity halo ring, wet pavement elongated orange reflection,
 humid night air, slight haze, alley single bulb exposed wire,
 old district street light, orange sodium vapor, atmospheric halo"
```

---

## Token 15 — DIM SUM BREWERY FOG SYSTEM

**Problem Statement**
AI produces generic steam. Real dim sum/Douhua/豆品店 steam has specific visual characteristics: the way it rises in cold air-conditioned interior (visible steam vs invisible), the specific bamboo basket stack, the way steam interacts with overhead fluorescent lighting, and the humid-heat boundary at the kitchen entrance.

**Why V17 Cannot Solve It**
V17 could not simulate visible steam physics in air-conditioned space vs non-air-conditioned space. It had no concept of: the bamboo basket stack system (different tiers), the way steam shows in cold interior (visible, dissipates slowly) vs hot interior (invisible), or the specific humidity boundary at the kitchen threshold.

**Real Photography References**
- Local food photographer @dimsumdocumentary
- Instagram @hkfoodculture (steam studies)
- Fan Ho's food establishment work (steam visible in cold interior)

**Local Behavioral Logic**
Dim sum establishments are cold inside (air conditioning = customer comfort, food preservation). The temperature difference between kitchen (hot + humid) and dining area (cold + air-conditioned) creates a visible steam boundary at the kitchen entrance. Inside, steam from bamboo baskets rises but is visible because the surrounding air is colder than the steam.

**Visual Evidence**
- Bamboo basket: woven bamboo, slight brown-yellow color, stacked in tiers
- Steam: white-gray, visible in cold interior, rises then dissipates, affected by ceiling fan
- Kitchen boundary: visible humidity/steam wall at entrance, warm side vs cold side
- Lighting: fluorescent tubes above bamboo baskets, steam creates diffusion/masking effect
- Food items: 蝦餃 visible through bamboo weave, skin texture visible
- Interior: plastic laminate tables, usually blue or green, ceiling fan (sometimes)
- Temperature contrast: condensation on cold surfaces near steam source

**Prompt Vocabulary**
```
 dim sum bamboo basket stack, visible steam cold interior, white-gray steam,
 fluorescent light diffusion, steam masking light, kitchen humidity boundary,
 warm-cold air threshold, condensation on cold surface, ceiling fan affecting steam,
 蝦餃 visible through bamboo weave, plastic laminate table, air conditioned dim sum,
 steam rising from bamboo basket, humid kitchen air vs cold dining area
```

**Integration Rules**
- Air conditioning must be present — visible steam only occurs in cold interior
- Bamboo basket stack is 3-tier minimum — single basket is not authentic
- Fluorescent light above creates steam diffusion effect — this is mandatory for authentic dim sum interior
- Kitchen boundary visible steam wall is a key authenticity marker

**Anti-AI Benefits**
The visible steam in air-conditioned interior physics is a specific phenomenon not commonly documented in AI training data. The bamboo basket stack system + fluorescent light diffusion + steam masking effect is a unique visual system. AI produces generic "food steam" without the air conditioning context or bamboo basket stacking.

**Example Prompt Fragments**
```
"air conditioned dim sum, bamboo basket stack 3-tier, visible white steam,
 fluorescent light diffusion through steam, steam masking light on baskets,
 kitchen humidity boundary visible, warm steam air meeting cold dining area,
 condensation near steam source, blue plastic laminate table,
 蝦餃 visible through bamboo weave, humid kitchen air, ceiling fan slow"
```

---

## Token 16 — KOWLOON WONG TAI SIN TENANT SIGNAGE

**Problem Statement**
AI produces generic Chinese signs. Real Wong Tai Sin Estate (and similar 1980s-era public housing) has specific commercial signage on the podium level: the way 茶餐廳, 藥房, 髮型屋 signs relate to the podium geometry, the specific signage material (backlit acrylic, box sign), and the way signs collide vertically on podium face.

**Why V17 Cannot Solve It**
V17 had no concept of podium-level commercial signage collision, could not distinguish between podium signage (for estate residents) vs street-level signage (for general public), and could not manage the vertical stacking logic of estate commercial units.

**Real Photography References**
- Eric Leung's Wong Tai Sin series (podium geometry, signage stacking)
- Instagram @estatesignage (HK estate commercial signage documentation)
- 大榮街拍: public housing commercial podium

**Local Behavioral Logic**
Wong Tai Sin Estate podium commercial units are designed for daily-needs retail: 茶餐廳 (breakfast/lunch), 藥房 (pharmacy/daily goods), 髮型屋 (hairdresser), 超市 (supermarket). Each shop type has standard signage conventions. The podium face becomes a vertical commercial collage as each shop competes for attention from estate residents entering/exiting.

**Visual Evidence**
- Podium: concrete, 4–6 floors, rectangular footprint, single commercial face per street
- Signage types: backlit acrylic box sign (modern), painted metal sign (older), vinyl sticker (cheapest)
- Stacking: vertical collision, shop signs at varying heights, not aligned
- Color coding by shop type: 藥房 = green/red (health), 茶餐廳 = warm tones, 髮型屋 = pink/purple
- Material aging: acrylic yellows with UV, paint fades, sticker curls
- Entrance: pedestrian bridge or ground-level entrance, estate name visible above

**Prompt Vocabulary**
```
 Wong Tai Sin Estate podium, commercial signage collision, vertical stacking,
 backlit acrylic box sign, painted metal sign, vinyl sticker curl,
 茶餐廳 warm tone sign, 藥房 green red, 髮型屋 pink purple,
 acrylic yellowing, podium concrete, estate entrance, pedestrian bridge,
 1980s estate commercial unit, daily needs retail, estate resident service,
 podium geometry, commercial face collage, vertical sign stacking
```

**Integration Rules**
- Podium must be 4–6 floors — lower podium is different estate type
- Shop types are standard for daily needs: at least 茶餐廳 + 藥房 + 髮型屋
- Vertical stacking: signs at different heights, not horizontal alignment
- Material aging: newer shops = acrylic (yellowing), older shops = painted metal (rusting)
- Estate name visible above commercial podium

**Anti-AI Benefits**
The specific Wong Tai Sin podium geometry + commercial signage collision + shop-type color coding is a hyper-local system. AI does not consistently produce the vertical stacking collision or the specific shop-type color conventions. Estate name visibility is a location-specific marker.

**Example Prompt Fragments**
```
"Wong Tai Sin Estate podium, 4-floor commercial face, vertical sign stacking collision,
 green red 藥房 acrylic box sign, warm-toned 茶餐廳 sign, yellowing acrylic,
 pink 髮型屋 sign, podium concrete with water stains, pedestrian bridge entrance,
 estate name visible, 1980s public housing commercial system,
 daily needs retail podium, signage at varying heights"
```

---

## Token 17 — SAI YING PUN / SHEUNG WAN VERTICALITY

**Problem Statement**
AI produces "Hong Kong hillside" as: generic slope with buildings. Real Sai Ying Pun and Sheung Wan have specific vertical systems: the way streets incline at ~15–30°, the staircase streets (石板街), the mid-level walkway system, and how buildings stack vertically to accommodate slope. This creates visual perspectives AI cannot manage.

**Why V17 Cannot Solve It**
V17 had no concept of HK hillside geometry. It could not simulate: the staircase street perspective, the way buildings appear to stack vertically due to slope, the specific perspective distortion from looking up a hill street, or the mid-level walkway that cuts across building faces.

**Real Photography References**
- Fan Ho's Sheung Wan work (hillside perspective, staircase street)
- Instagram @sheungwanlife (verticality studies)
- Local photographer @hillonhongkong

**Local Behavioral Logic**
Sai Ying Pun and Sheung Wan are built on hillside. Buildings step down the slope, creating the illusion that buildings above are stacked on those below. Streets become staircases where pedestrian-level is not flat. The Mid-levels Escalator (半山扶手電梯) bisects the vertical system. Looking up or down any street creates a specific vanishing point distortion.

**Visual Evidence**
- Staircase street (石板街): stone steps, iron railing, buildings on both sides at different heights
- Inclined street: asphalt + step combination, ~15–30° incline, buildings at different foundation heights
- Building stacking: upper building appears to sit on lower building roof, not beside it
- Mid-levels Escalator: covered walkway, metal and glass, cuts across building faces
- Perspective distortion: looking up creates tall narrow corridor of buildings, looking down creates receding jutting building edges
- Sheung Wan character: dried seafood shop on ground floor, traditional wooden screen (木趟櫳) on old buildings

**Prompt Vocabulary**
```
 Sai Ying Pun hillside, staircase street 石板街, stone step street,
 iron railing, building stacking on slope, upper building on lower roof,
 Mid-levels Escalator 半山扶手電梯, inclined street 15-30 degrees,
 vertical perspective distortion, looking up hill street, receding building edge,
 dried seafood shop ground floor, traditional 木趟櫳, Sheung Wan slope geometry,
 hillside building stack illusion, mid-levels walkway system
```

**Integration Rules**
- Staircase street must have iron railing — this is the authenticity marker
- Building stacking illusion: upper building base visible above lower building roof
- Perspective distortion: must force either looking-up OR looking-down vanishing point
- Dried seafood shop (海味) is specific to Sheung Wan ground floor — include when authenticating location
- Mid-levels Escalator visible when using Sheung Wan/Sai Ying Pun

**Anti-AI Benefits**
The specific HK hillside staircase geometry + building stack illusion + slope perspective is one of the most physically distinctive environments in HK. AI consistently fails at the vertical perspective distortion. The Mid-levels Escalator bisecting the hillside is a unique infrastructure element.

**Example Prompt Fragments**
```
"Sheung Wan staircase street 石板街, iron railing, looking up incline,
 building stacking on slope, upper building base visible above lower roof,
 Mid-levels Escalator in background, dried seafood shop ground floor,
 traditional 木趟櫳, steep perspective distortion, hillside geometry,
 humid afternoon, stone step street, vertical Sheung Wan"
```

---

## Token 18 — HONG KONG TROLLEYBUS / TRAM SYSTEM

**Problem Statement**
AI produces "Hong Kong tram" as: generic streetcar. Real HK trams and trolleybuses have specific visual characteristics: the Rv (revenue) numbering system, the way the pole collector interacts with overhead wire, the specific livery (green and cream for Kowloon trolleybus, double-decker red for tram), and the way they interact with traffic flow.

**Why V17 Cannot Solve It**
V17 could not distinguish between: tram (港島) and trolleybus (九龍), could not simulate the overhead wire/collector pole system, could not produce the specific livery variations, and could not model the way these vehicles interact with HK traffic density.

**Real Photography References**
- Fan Ho's tram photography (1950s–60s era, different livery, street interaction)
- Instagram @hktrams (contemporary tram documentation)
- Local transit photographer @trolleymethk

**Local Behavioral Logic**
HK trams run only on Hong Kong Island (港島). Kowloon has trolleybuses (operated by KMB). The overhead wire system is visually distinctive: the collector pole (pantograph) maintains contact with the wire, creating a constantly flexing angle. Trams are double-decker (except new low-floor units). Traffic density means trams share lanes with other vehicles.

**Visual Evidence**
- HK Tram: double-decker, red livery with body advertising (full wrap), steel chassis, flat-front design
- Kowloon Trolleybus: single-decker, green and cream original livery, now various advertising liveries
- Overhead wire: single wire, visible tension, collector pole maintains contact angle
- Pole flex: collector pole angle changes as tram/bus moves, ~15–30° from vertical
- Tram route number: displayed on rollsign (not LED), white on green or red
- Traffic interaction: tram shares lane with taxi, bus, private car, pedestrian
- Tram bell: visible at roof line, rung at stops

**Prompt Vocabulary**
```
 Hong Kong tram double-decker, red livery, full body advertising wrap,
 overhead wire, collector pole pantograph, pole angle flex 15-30 degrees,
 tram route rollsign, white on green, tram shares lane with traffic,
 Kowloon trolleybus green cream, single-decker, overhead wire tension,
 trolleybus collector pole, traffic density, tram bell visible,
 港島電車, 九龍trolleybus, transit system specific
```

**Integration Rules**
- HK Island = tram (double-decker, overhead wire)
- Kowloon = trolleybus (single-decker, green-cream or advertising livery)
- Overhead wire must be visible — this is the defining visual element
- Collector pole angle must be shown (not vertical, not broken)
- Traffic density is mandatory — trams do not run in empty streets

**Anti-AI Benefits**
The specific HK tram + trolleybus overhead wire/collector system is not well-documented in AI training data outside HK. The livery variations (full body advertising vs original colors) and the pole flex physics are specific to this system. Traffic density context is essential — empty tram is not authentic.

**Example Prompt Fragments**
```
" Causeway Bay tram, double-decker red with full body advertising, overhead wire visible,
 collector pole 20° from vertical, rollsign showing route number,
 tram shares lane with taxi and pedestrian, traffic density, tram bell at roof,
 afternoon rush, steel rail, overhead wire tension, 港島電車"
```

---

## Token 19 — HONG KONG RAIN / MONSOON ATMOSPHERE

**Problem Statement**
AI produces "rain" as: blue-gray filter, wet surface. Real HK monsoon (四月, 六月–九月) has specific visual systems: the way rain appears in diagonal sheets (not vertical), the specific post-rain smell-implied visuals (steam from pavement), the way umbrellas create a sea of color at street level, and the specific amber-grey sky palette.

**Why V17 Cannot Solve It**
V17 could not simulate: diagonal monsoon rain sheets, the specific HK umbrella-sea phenomenon, the post-rain pavement steam, or the amber-grey sky palette specific to HK monsoon season. It treated rain as a uniform blue-gray condition.

**Real Photography References**
- Brian Ching's monsoon photography (diagonal rain sheets, umbrella sea)
- Kelvin Lam's post-rain studies (pavement steam, amber sky)
- Fan Ho's rain work (street level, umbrellas, wet surface reflection)

**Local Behavioral Logic**
HK monsoon rain is diagonal — driven by southwest monsoon winds from the South China Sea. Rain sheets move across the city in bands. People open umbrellas instantly, creating a street-level color phenomenon (black, navy, transparent). Post-rain, warm pavement heats trapped water, creating steam that rises into humid air. The sky becomes amber-grey (not blue-gray) — a specific monsoon sky palette.

**Visual Evidence**
- Rain: diagonal sheets, not vertical drops, driven by wind direction
- Umbrella sea: street level filled with umbrellas, colors: black, navy, transparent plastic
- Sky: amber-grey, not blue-gray, saturation reduced, no contrast
- Pavement post-rain: steam rising from warm asphalt, white wisps
- Wet surface: mirror reflection, slightly distorted, pooling in low points
- Building: water streams down facade, window reflections intensify
- Light: diffused, no hard shadow, overcast but warm-tinted
- Season marker: August/September rain, most intense

**Prompt Vocabulary**
```
 Hong Kong monsoon rain, diagonal rain sheet, southwest wind driven,
 umbrella sea, black navy transparent, street level color phenomenon,
 amber-grey monsoon sky, post-rain steam, pavement steam rising,
 warm asphalt, humid air, wet mirror surface, pooling water,
 water streams on building facade, diffused light no shadow,
 August monsoon, 六月 monsoon, overcast warm sky
```

**Integration Rules**
- Rain is always diagonal (wind direction from South China Sea) — never vertical
- Sky is amber-grey, not blue-gray — specific monsoon palette
- Post-rain steam (pavement) is separate from rain — specify post-rain or during-rain
- Umbrella colors: black + navy + transparent only (bright colors rare in monsoon)
- No hard shadow when raining or immediately post-rain

**Anti-AI Benefits**
The specific diagonal monsoon rain direction (driven by SW wind) + amber-grey sky palette + umbrella sea phenomenon is physically specific to the South China Sea monsoon system affecting Hong Kong. AI cannot consistently produce the diagonal rain direction or the amber-grey monsoon sky palette.

**Example Prompt Fragments**
```
"Mong Kok in monsoon rain, diagonal rain sheets driven by wind,
 umbrella sea street level, black navy transparent, amber-grey sky,
 wet pavement mirror surface, slightly diffused light,
 slight steam rising from warm pavement post-rain, humid air,
 August monsoon, building facade water streams, no hard shadow,
 overcast warm sky"
```

---

## Token 20 — HONG KONG ELECTRICAL CHAOS / OVERHEAD LINE SYSTEM

**Problem Statement**
AI produces "Hong Kong电线" as: clean overhead lines. Real HK has an electrical chaos system: overhead power lines at multiple voltages (33kV, 11kV, 400V), telephone cables, fibre cables, and signage support wires all sharing the same pole corridor. This creates a specific visual spaghetti that is being slowly buried underground but remains visible in old districts.

**Why V17 Cannot Solve It**
V17 could not manage the specific HK overhead line system: multiple wire types, multiple voltages, the specific pole structures, the way signs hang from these wires, or how the collision of utility types creates a specific visual density.

**Real Photography References**
- Instagram @hk_electricCHAOS (documentary overhead line series)
- Local photographer @wiresinhk (overhead wire studies)
- Brian Ching's alley studies (electrical wire density)

**Local Behavioral Logic**
HK's dense urban environment pushed utilities overhead when underground burial was impossible. Overhead poles carry everything: power (black cables, thick), telephone (gray bundles), fibre (thin, new), signage support wires (from shop signs to building), and sometimes tram/pole bus wires. In old districts, poles are crowded with 15–30 years of accumulated infrastructure.

**Visual Evidence**
- Power pole: concrete or steel, slightly tilted, carrying multiple wire types
- Power cables: black, 3-phase, various diameters (thick = high voltage)
- Telephone bundle: gray, multiple twisted pairs, drooping
- Fibre cable: thin, white or orange, newer addition
- Signage support wire: thin steel wire from shop sign to building or pole
- Wire density: multiple wire crossings creating spaghetti visual
- Collision with signage: wires pass behind, through, and around shop signs
- Street level: pole at sidewalk edge, sometimes blocking pedestrian path
- District: Yau Ma Tei, Sham Shui Po, Mong Kok = highest density

**Prompt Vocabulary**
```
 Hong Kong overhead wire, electrical spaghetti, multiple voltage overhead,
 33kV 11kV power cable, telephone bundle gray, fibre orange thin,
 power pole concrete, signage support wire, shop sign hanging from wire,
 wire density collision, multiple wire crossing, overhead utility spaghetti,
 Yau Ma Tei overhead system, electrical chaos, pole at sidewalk edge,
 undergrounding transition, old district overhead density
```

**Integration Rules**
- Multiple wire types required: power (black) + telephone (gray bundle) + at least one signage support wire
- Wire drooping (catenary) must be visible — straight lines are not authentic
- Pole slightly tilted (not vertical) is common in old districts
- Wires pass behind signage — they do not avoid it, they collide with it
- Old districts (Yau Ma Tei, Sham Shui Po) have highest wire density — new districts less so

**Anti-AI Benefits**
The specific HK overhead wire system with multiple voltage types + signage support wire + spaghetti crossing density is one of the most visually complex urban systems in HK. AI consistently produces clean overhead lines (power only) or fails at the multiple wire type + droop physics. This is one of the most anti-AI visual systems in Hong Kong.

**Example Prompt Fragments**
```
"Yau Ma Tei alley, overhead electrical spaghetti, black 11kV power cable,
 gray telephone bundle drooping, thin fibre orange, steel signage support wire,
 concrete pole slightly tilted, shop sign hanging from wire intersection,
 multiple wire crossing, wire catenary droop, pedestrian path blocked at edge,
 electrical chaos, overhead utility collision, humid air, 30 years accumulated infrastructure"
```

---

## Integration Framework

### Token Priority Matrix

| District/Context | Primary Tokens | Secondary Tokens | Ambient Tokens |
|---|---|---|---|
| Mong Kok Day | Token 01, Token 06 | Token 11, Token 14 | Token 03 |
| Sham Shui Po Night | Token 02, Token 08 | Token 07, Token 14 | Token 06 |
| Wet Market Morning | Token 03, Token 06 | Token 04 | Token 16 |
| Public Housing | Token 05, Token 10 | Token 06 | Token 16 |
| Cha Chaan Teng | Token 04 | Token 06, Token 15 | Token 09 |
| Sheung Wan | Token 17 | Token 19 | Token 09, Token 20 |
| Yau Ma Tei | Token 11, Token 13 | Token 01, Token 14 | Token 06 |
| Victoria Harbour | Token 08, Token 12 | Token 06, Token 14 | — |
| Monsoon Season | Token 19 | Token 06, Token 20 | Token 03 |
| Old Mall | Token 07 | Token 04, Token 09 | Token 06 |

### Token Combination Rules

1. **Minimum 3 tokens** per HK scene: 1 primary district/location token + 1 atmosphere token + 1 material/light token
2. **Never combine Token 06 (humidity)** with Token 19 (monsoon rain)** without specifying time sequence — they are different humidity conditions
3. **Token 09 (typography)** must be used when any signage is prominent — it is a forcing function for traditional characters
4. **Token 06 (humidity)** is ambient — use with any outdoor scene, adjust temperature by time of day
5. **Token 20 (electrical)** only in old districts — new districts have underground wiring

### Anti-AI Validation Checklist

For any output claiming HK authenticity, verify:
- [ ] Traditional characters (not simplified) if Chinese text is present
- [ ] Humidity expressed as specific time-of-day phenomena (morning condensation vs afternoon shimmer)
- [ ] Signage collision and stagger (not aligned)
- [ ] Multiple light sources in night scenes (not single neon)
- [ ] Material decay appropriate to building age
- [ ] District-specific population/social use (not generic crowd)
- [ ] Geometric specificity (Harmony block type, hillside geometry, pole system)
- [ ] Weather/season specificity (monsoon direction, humidity cycle)
- [ ] Overhead wire multiple types and droop
- [ ] Food establishment material system (dim sum bamboo basket, cha chaan teng plastic laminate)

### Version Notes

**V17 → V18 Changes:**
- V17 treated HK as single visual class; V18 separates into 20 distinct material/behavioral systems
- V17 had no Cantonese typography token; V18 Token 09 introduces era-specific font system
- V17 had no humidity time-of-day specificity; V18 Token 06 introduces morning/afternoon/post-rain differentiation
- V17 had no overhead wire system; V18 Token 20 introduces electrical chaos as distinct anti-AI system
- V17 had no ghost sign layer; V18 Token 13 introduces disappearing 1950s–70s ghost sign documentation
- V17 had no public housing laundry geometry; V18 Token 10 introduces bamboo pole + 花碼 interaction system
- V18 adds integration priority matrix for token combination
- V18 adds anti-AI validation checklist

---

*HK Texture Engine V18 — Authenticity through material specificity*
*Document the real. Resist the generic.*
