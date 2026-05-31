# HK Texture Engine — V18
## Unified HK Texture Tokens for V18

---

## Philosophy

Generic Hong Kong prompts produce generic results. AI models generate "Hong Kong" as a collision of neon and skyscrapers — a stereotype stripped of soul. The city that photographers like **Fan Ho**, **Brian Ching**, **Kelvin Lam**, and **Eric Leung** captured is a city of **compressed density**, **humid decay**, **contradictory signage**, and **hyper-specific locality**. Every district breathes differently. Sham Shui Po has a different texture than Mong Kok. A wet market smells different than a cha chaan teng. V17 could not distinguish these micro-layers. V18 must.

This V18 document unifies two research streams: **15 specific location deep-dives** from the HK Texture Library with **20 behavioral/material tokens**. The result is a unified token system where architectural specificity (from the 15 locations) combines with behavioral realism (from the 20 tokens) to produce imagery that local HK people recognize instantly without captions.

---

## Unified Token Architecture

The V18 system is organized into three tiers:

| Tier | Type | Count | Function |
|------|------|-------|----------|
| **LOCATION TOKENS** | Architectural specificity | 15 | Ground prompts in real HK places — authentic geometry, materials, objects |
| **MATERIAL/BEHAVIORAL TOKENS** | Behavioral realism | 20 | Control material decay, light collision, typography, social density |
| **AMBIENT TOKENS** | Atmospheric conditions | 3 | Cross-cutting: humidity (06), lighting (14), weather (19) |

**Integration Rule**: Every authentic HK prompt requires minimum **1 Location Token + 1 Material/Behavioral Token + 1 Ambient Token** (when applicable).

---

## PART I: LOCATION TOKENS (15)

### Location Token 01 — PUBLIC HOUSING CORRIDORS (公共屋邨走廊)

**Research Source**: HK_TEXTURE_LIBRARY.md Location 01

**Visual Identity**
Endless linear corridors in HK-type public housing blocks (公屋). Cream/off-white painted concrete walls bearing decades of moisture stains, patches of mold near ceilings, faded painted numbers on doors. The走廊 feeling is uniquely HK — always slightly humid, slightly stuffy, with that particular smell of cooking oil and detergent mixing in the enclosed space. Corridors run the full length of each floor, exposed to elements via open windows on one side.

**Architectural Cues**
- Narrow corridor width (~1.5m), doors on both sides, slightly curved ceiling from water damage
- **Floor material**: Grey square floor tiles (600x600mm) with black rubber kickplates at door thresholds
- **Door types**: Metal unit doors (單位門) — hollow metal with small window, painted cream or faded pastel colors (mint green, powder blue, dusty pink)
- **Door numbers**: White painted metal plates, always offset to one side, with Chinese floor designation (e.g., 5/F, 11/F)
- **Windows**: Aluminum frame louvered windows (百葉窗) on outer wall, slightly crooked from building settling
- **Ceiling height**: ~2.7m, pipes running exposed along ceiling
- **Light switches**: Chunky white plastic, positioned low on walls near doors

**Object Library**
- Chopstick holders: Plastic or ceramic containers on door thresholds (門口位置)
- Plastic slippers: Flip-flops left outside doors, arranged neatly
- Door mats: Small rubber doormats (門墊), often with "出入平安" or similar blessing
- Brooms: Broom handles sticking out from behind doors, dustpan brushes leaning on walls
- Dried laundry: Hanging inside the corridor through interior doors (visible through gaps), primarily white or pastel vests, underwear on simple plastic hangers
- Moisture fans: Exhaust fans (浴室扇) on ceilings near toilets, dirty plastic grilles
- Water meters: Analog meters in metal boxes mounted on walls at corridor ends
- Warning signs: Fluorescent orange/yellow "請勿吸煙" (No Smoking) signs, slightly sun-rotted
- Fire extinguishers: Red extinguishers (滅火筒) at corridor ends behind glass boxes
- Sticker residue: Old election posters, tenancy renewal notices, damp-affected flyers layered on walls

**Lighting Behavior**
- **Fluorescent tube lights** (光管): 2-foot or 4-foot white fluorescent tubes in cheap plastic diffusers, slightly flickering, positioned at regular intervals
- Light casts **harsh shadows** on doors and walls — every imperfection amplified
- Slight **yellowing** of light from aged tubes
- No warm light sources — everything 4000K+ daylight/neutral white

**Social Density**
- Low-density in terms of people visible, but high-density in terms of accumulated life evidence
- Occasional elderly residents shuffling slowly, checking mailbox (郵箱) at corridor end
- Children running in bursts then disappearing into apartments
- Minimal eye contact between residents — privacy culture

**Camera Opportunities**
- **Long corridor perspective shots** with doors receding into distance, slightly crooked door frames
- **Close detail shots**: water stains, sticker layers, moisture damage, rust on door frames
- **Ambient shots**: flickering fluorescent, shadow patterns on floor tiles

**Proof-of-Life Objects**
- Plastic slippers arranged outside a door, clearly well-used
- Chopstick holder on a door threshold — actual chopsticks visible inside
- Television sound bleeding through door gaps — a muffled drama playing inside
- Water pipe drips in corner creating small puddle with foam

**Unified Token Integration**
- Pair with **Token 05** (Public Housing Block Geometry) for full building context
- Pair with **Token 10** (Public Housing Laundry System) for corridor context
- Pair with **Token 06** (Humidity) for authentic corridor atmosphere
- Use **Token 09** (Typography) for door number authenticity

---

### Location Token 02 — TAI KWUN (大館)

**Research Source**: HK_TEXTURE_LIBRARY.md Location 02

**Visual Identity**
Colonial-era police compound (now cultural heritage center) in Central. Limestone walls in warm honey tones, Victorian ironware (wrought iron), high ceilings, symmetrical courtyard geometry. The compound feels suspended in time — British colonial formality mixed with institutional decay now arrested as heritage. Red brickwork accents, wooden window shutters (百葉窗), stone archways. The contrast between old colony architecture and modern HK pace makes this distinctive.

**Architectural Cues**
- **Central Hall**: Double-height space with polished concrete floors, exposed brick walls, massive arched windows letting in directed light
- **Barrack building**: Two-story yellow brick with verandah (走廊), red tiled roof
- **Court building**: Victorian colonnade with cast-iron columns, checkerboard floor tiles (石屎地磚)
- **Gallery spaces**: Whitewashed walls, track lighting installed discretely in heritage context
- **Staircases**: Stone steps with iron handrails, slight wear on nosings from century of use
- **Archways**: Rounded arches in sandstone, shadows pooling underneath

**Object Library**
- **Wooden benches**: Colonial-style slatted wooden seating in courtyards
- **Cast-iron lanterns**: Heritage-style light fixtures, some with warm LED conversions
- **Guard boxes**: Small wooden sentry posts at building entrances, weathered paint
- **Information plaques**: Cream metal plates with Chinese and English text about heritage
- **Planters**: Simple stone or concrete planters with manicured greenery
- **Art installations**: Contemporary art pieces placed in courtyards — sharp contrast to heritage setting

**Lighting Behavior**
- **Natural light dominance**: Light enters through tall arched windows creating strong volumetric beams
- **Stone reflectivity**: Limestone walls reflect warm golden light back into spaces
- **Shadow depth**: Deep shadows under archways and colonnades
- **Artificial light**: Warm Edison bulb style (2700K) in heritage-style fixtures, used sparingly for evening events

**Social Density**
- Weekday afternoons: sparse visitors, professionals eating lunch on benches
- Weekends: families, tourists, young couples doing engagement photos
- Events: art openings, corporate functions, film screenings
- No residents — pure public/administrative space

**Proof-of-Life Objects**
- Coffee cups from on-site café on benches
- Security guard uniforms — distinctive dark blue
- Event programs left on seats after screenings
- Exhibition postcards in the gift shop

**Unified Token Integration**
- Pair with **Token 08** (Night Light Collision) for evening heritage lighting
- Pair with **Token 09** (Typography) for bilingual signage authenticity
- Ambient: 2700K warm light for evening events

---

### Location Token 03 — PMQ (元創方)

**Research Source**: HK_TEXTURE_LIBRARY.md Location 03

**Visual Identity**
Former Police Married Quarters (已婚警察宿舍) converted to creative hub in Mid-Levels. Institutional architecture repurposed as design entrepreneurship space. Creamy yellow/cream building, simple geometric windows (方正窗), large communal terraces. The vibe is "local creative meets colonial heritage" — local designers selling locally-made products, not tourist tat. Chinos and sneakers rather than mainland tour groups.

**Architectural Cues**
- **Building massing**: Two L-shaped blocks surrounding central courtyard (open to sky)
- **Windows**: Simple rectangular openings with dark frames, no ornamentation
- **Corridors**: Open-sided covered walkways (騎樓式走廊) on each floor facing courtyard
- **Stairwells**: Exposed concrete, emergency lighting strips
- **Rooftop terrace**: Open-air space with concrete pavers, remnant of police residence times
- **Floor material**: Polished concrete in common areas, original mosaic tiles in some units

**Object Library**
- **Designer studios**: Individual boutique shops with custom display fixtures
- **Fabric samples**: Textile rolls visible through shop windows, color-coded
- **Design tools**: Sketchbooks, drafting equipment, laptop stands visible in open studios
- **Seating areas**: Minimalist metal chairs on terraces, scattered
- **Art installations**: Rotating sculpture pieces in stairwells
- **Signage**: Handwritten chalk boards, minimalist acrylic店名 plates

**Lighting Behavior**
- **Daylight through windows**: Even illumination from courtyard-facing windows, no harsh direct sun
- **Track lighting**: Gallery-style adjustable spotlights in corridors
- **Shop lighting**: Individual warmth from each tenant — some warm (2700K), some neutral daylight

**Social Density**
- Local design community (设计师) during work hours
- Weekend visitors (本地人) browsing, not mass tourism
- Low decibel — conversations happen in undertones
- Instagram-bait spots but managed crowd flow

**Proof-of-Life Objects**
- Coffee cups from adjacent café scattered on terrace tables
- Sewing pattern papers pinned to design studio windows
- Design sketches taped to studio glass doors

**Unified Token Integration**
- Pair with **Token 09** (Typography) for designer shop signage
- Ambient: mixed 2700K-4000K for gallery warmth

---

### Location Token 04 — CENTRAL MARKET (中環街市)

**Research Source**: HK_TEXTURE_LIBRARY.md Location 04

**Visual Identity**
Wet market building (街市) in Central core, brutalist concrete structure from 1930s. Simple rectangular footprint, internal void with staircases and shops arranged around central well. Characterized by market decay, fish stall water runoff, institutional paint colors (sage green, dirty cream), and the organized chaos of local wet market trading. The building sits between fancy landmarks — Crown Heights and PMQ nearby — and acts as a bridge between colonial heritage and current local market use.

**Architectural Cues**
- **External facade**: Art Deco influence — simple geometric patterns, horizontal banding
- **Internal void**: Open-sided market stalls surrounding central atrium, goods displayed on concrete platforms
- **Staircases**: Wide concrete stairs with metal handrails, connecting each floor
- **Shop fronts**: Simple metal shutters (鐵閘) rolled up in morning, closed by afternoon
- **Floor drainage**: Central floor channel (排水渠) running through building, slight smell
- **Windows**: Large openings for ventilation, no air conditioning

**Object Library**
- **Wet market stalls**: Steel tables (冰台) with plastic sheets, hanging scale (磅), plastic buckets
- **Umbrellas**: Folded umbrellas in stalls — rain gear vendors mixed with vegetables
- **Cool boxes**: Styrofoam coolers (冰箱) with ice blocks keeping fish fresh
- **Trolleys**: Market trolleys (購物車) — collapsible metal with plastic wheels
- **Price boards**: Handwritten cardboard price signs held by bulldog clips on stall frames
- **Plastic tarps**: Colorful tarps covering goods outside when needed

**Lighting Behavior**
- **Fluorescent tubes**: Harsh white light above each stall, creating pool-of-light effect
- **No warmth**: Pure functional lighting, 5000K+ daylight tubes
- **Shadow contrast**: Dark ceiling areas above lights, creating vertical striation

**Social Density**
- Morning (6-10am): Very dense, vendors and regular market-goers
- Afternoon: Sparse, many stalls closed, elderly resting on benches
- Weekends: Mixed local residents, some tourists discovering on walking tours

**Proof-of-Life Objects**
- Wet fish on ice, scales visible
- Plastic shopping bags with market vendor stamps
- Elderly vendor sorting vegetables slowly
- Water puddles on floor near fish stalls

**Unified Token Integration**
- Integrates with **Token 03** (Wet Market Visual System) for material specificity
- Pair with **Token 06** (Humidity) for morning market condensation
- Ambient: 5000K+ harsh fluorescent

---

### Location Token 05 — GOLD FISH STREET (金魚街)

**Research Source**: HK_TEXTURE_LIBRARY.md Location 05

**Visual Identity**
Pak Hoi Ting Street (白鶴堤街) in Mong Kok — actually specializing in aquarium shops and goldfish vendors. The street is narrow, covered by简易棚架 (simple awning), tanks stacked on both sides creating blue-green color gradient. The distinctive feature is the clear plastic bags of water hanging from shop fronts — each bag containing a single goldfish floating in its own portable universe. Hundreds of these bags create a curtain of living color against the street.

**Architectural Cues**
- **Shops**: Ground floor metal shutters rolled up, tanks visible inside
- **Awning**: Blue or green PVC sheeting creating tunnel effect, reducing daylight
- **Street width**: Very narrow, barely fits two people walking
- **Ground**: Concrete with water runoff, drains visible

**Object Library**
- **Fish bags**: Clear plastic bags filled with water, tied at top with rubber band, one goldfish each
- **Aquarium tanks**: Stacked glass tanks inside shops, air pumps visible, colorful gravel
- **Oranda goldfish**: The iconic oversized-head ranchu style — most recognizable HK goldfish
- **Betta fish**: Siamese fighting fish in small cups, iridescent blues and reds
- **Plastic bags of worms**: Red earthworms in bags for fishing
- **Water plants**: Java moss, water hyacinth in bags for aquarium plants
- **Tank decorations**: Ceramic mushrooms, plastic plants, small treasure chests

**Lighting Behavior**
- **Filtered light through awning**: Green-blue tinted ambient light
- **Shop lighting**: Strong aquarium lights inside tanks creating glow effect
- **No warmth**: Everything lit by daylight tubes and tank lights, very cool palette

**Social Density**
- Weekends: Dense foot traffic, families with children pressing faces to tanks
- Weekdays: Shop owners sitting outside on plastic stools, maintenance routines

**Proof-of-Life Objects**
- Fish bags with visible movement inside
- Air pump bubbles audible
- Water splashing on ground from tank maintenance

**Unified Token Integration**
- Pair with **Token 01** (Mong Kok Signage Layer) for street context
- Ambient: Green-blue 5000K+ cool palette

---

### Location Token 06 — FLOWER MARKET (花墟)

**Research Source**: HK_TEXTURE_LIBRARY.md Location 06

**Visual Identity**
Yuen Po Street (園圃街) in Mong Kok — tree-lined with iron archways and corrugated metal roofing. Flower shops display merchandise outside under covered walkway. The dominant colors are green (plants, leaves), bright floral accents (roses, chrysanthemums, orchids), and brown (wooden crates, bamboo stakes). The air is humid and fragrant — jasmine, chrysanthemum, rose. Morning is the peak activity time.

**Architectural Cues**
- **Street structure**: Two rows of shops with covered walkway in middle (有蓋街道)
- **Roofing**: Corrugated galvanized steel (鍍鋅鐵皮) with occasional clear panels for daylight
- **Shop fronts**: Open to street, plants displayed on ground level, hanging plants above
- **Arches**: Green painted metal archways spanning street at intervals

**Object Library**
- **Plant display racks**: Metal or wooden tiered racks, plants arranged by type
- **Orchid pots**: Clear plastic pots with Phalaenopsis orchids, white roots visible through pot
- **Bamboo stakes**: Various heights for supporting plants
- **Watering cans**: Large galvanized metal cans (灑水壺)
- **Plastic pots**: Black plastic nursery pots stacked
- **Clay pots**: Traditional unglazed clay pots (瓦盆) for bonsai
- **Soil bags**: Nylon sacks of potting soil (培養土) leaning against shops
- **Chrysanthemum**: Yellow and white mums in plastic pots — funeral/worship offerings

**Lighting Behavior**
- **Diffused daylight**: Covered walkway reduces harsh sun
- **Green cast**: Heavy plant material absorbs warm light, reflecting green wavelengths
- **Water spray**: Fine mist from watering creates temporary light diffusion

**Social Density**
- Early morning (5-8am): Dense with shop owners preparing, some wholesalers
- Midday: Sparse, shoppers browsing slowly
- Chinese New Year: Extremely dense, people buying盆橘 (potted mandarin trees)

**Proof-of-Life Objects**
- Fresh flowers with water droplets on petals
- Bees or butterflies among flowers
- Shop owner pruning plants with scissors

**Unified Token Integration**
- Pair with **Token 06** (Humidity) for morning mist effect
- Ambient: Green-tinted diffused light

---

### Location Token 07 — MONG KOK PEDESTRIAN AREAS (旺角行人專區)

**Research Source**: HK_TEXTURE_LIBRARY.md Location 07

**Visual Identity**
Argyle Street (亞皆老街) and surrounding area — dense pedestrian flow, LED shop signs in Cantonese script, red/yellow/green neon (霓虹光管), air conditioning units (窗口機) stacked on building facades, street-level retail with metal shutters. The vertical density is HK's signature — every building face occupied by signs, AC units, pipes, windows. At street level: market stalls, phone accessory vendors, goldsmiths, mixed with international brands.

**Architectural Cues**
- **Shop signs**: Multi-layered signs, Chinese characters stacked vertically (直式招牌), some LED, some painted
- **AC units**: Window-type air conditioners (窗口式冷氣) densely packed, dripping condensate onto pavement
- **Metal shutters**: Corrugated steel (捲閘) half-open revealing shop interior
- **Street level**: Slightly raised footpaths (行人路) with uneven surfaces, street furniture
- **Sign clutter**: Minimal visual order, maximum information density

**Object Library**
- **Phone accessory stalls**: Phone cases, screen protectors, cables displayed on folding tables
- **Gold shops**: Gold jewelry displayed in bright-lit cases, ornate Chinese patterns on橱窗
- **Pharmacy**: Red cross (紅十字) signs, health products window display
- **Footpath obstacles**: Folding barriers, signage poles, pavement cracks
- **Vending carts**: Street food carts (車仔檔) — fish balls, stinky tofu, egg tarts
- **Umbrella stands**: Dense umbrella storage outside shops during rain

**Lighting Behavior**
- **Neon signs**: Bright red, orange, green, blue — actively glowing at all hours
- **LED shop lighting**: White bright shop lights, high color temperature (6000K+)
- **Mixed color temperature**: Warm tungsten from dai pai dongs mixed with cool LED from tech shops
- **Night dominance**: After dark, neon glow dominates — reflections on wet pavement

**Social Density**
- Extremely dense at all times — one of the world's highest pedestrian densities
- Slow movement required during weekends
- Constant sensory overload — visual, auditory, olfactory

**Proof-of-Life Objects**
- People checking phones while walking
- Shopping bags from multiple stores
- Street food in hands — curry fish balls on bamboo skewers

**Unified Token Integration**
- Core location for **Token 01** (Mong Kok Signage Layer)
- Core location for **Token 08** (Night Light Collision)
- Core location for **Token 09** (Typography)
- Pair with **Token 19** (Monsoon Rain) for umbrella sea phenomenon
- Ambient: Mixed neon + LED + tungsten

---

### Location Token 08 — HONG KONG DAI PAI DONG (大牌檔)

**Research Source**: HK_TEXTURE_LIBRARY.md Location 08

**Visual Identity**
Open-air food stalls (檔口) permitted by government license — characterized by gas burners (煤氣爐) in metal cabinets, menu boards in plastic laminate, plastic stools (膠凳) and foldable tables (摺枱) set up on pavement. The smell of frying oil, soy sauce, and charcoal fire. The identity is ephemeral — stalls set up for lunch service then packed away.

**Architectural Cues**
- **Stall cabinets**: Metal boxes with gas burners, open counter for serving
- **Signage**: Handwritten menus in marker on laminated cards, prices visible
- **Equipment**: Large rice cookers (電飯煲), steamers (蒸籠), wok burners (炒鑊)
- **Drainage**: Pavement drains visible, slight water accumulation
- **Canopy**: Simple tarp or umbrella for rain protection

**Object Library**
- **Plastic stools**: Low stools (膠凳) — typically red or blue, stackable, slightly dirty
- **Foldable tables**: Small aluminum tables with plastic tops, slightly wobbly
- **Bamboo chopsticks**: Paper-wrapped bundles of chopsticks (竹筷)
- **Thermos**: Large thermoses of Chinese tea (茶) in plastic covers
- **Serving dishes**: White or dark blue ceramic plates (碟)
- **Soy sauce dispensers**: Small ceramic or plastic containers for soy sauce (生抽老抽)
- **Menu items visible**: Curry鱼蛋 (fish balls), 雲吞麵 (wonton noodles), 叉燒飯 (char siu rice)

**Lighting Behavior**
- **Daylight**: Bright, flat, overhead sun — harsh shadows under canopies
- **Warm cooking light**: Orange glow from wok fire, steam rising
- **No artificial ambient**: Only functional lights for cooking, no aesthetic lighting

**Social Density**
- Lunch peak: Dense with workers, queuing, standing while eating
- Limited seating: People often eat standing or perched on stools
- Fast turnover: Tables clear quickly, constant motion

**Proof-of-Life Objects**
- Food being actively cooked on wok — visible steam and oil splatter
- Condiment bottles in use — soy sauce bottle with oil residue on neck
- Stool occupied — worn plastic surface showing use pattern

**Unified Token Integration**
- Core location for **Token 04** (Cha Chaan Teng Interior) — related food establishment system
- Core location for **Token 15** (Dim Sum Brewery Fog) for steam behavior
- Ambient: Wok fire ~2000K warm orange

---

### Location Token 09 — HONG KONG IZAKAYA (居酒屋)

**Research Source**: HK_TEXTURE_LIBRARY.md Location 09

**Visual Identity**
Japanese-style pub-restaurants (居酒屋) found in Kwun Tong, Quarry Bay, and areas with Japanese expat populations. Characterized by wooden interiors (木質裝修), paper lanterns (紙燈籠), izakaya-style seating (counter seating with high tables), and shared small plates (sharing culture). The vibe is casual Japanese meets HK industrial space — basement or Factory building locations common.

**Architectural Cues**
- **Interior**: Dark wood paneling (深木色), warm lighting
- **Seating**: High wooden tables, wooden stools or standing tables
- **Counter**: Open kitchen behind counter, chef preparing sashimi and yakitori
- **Decorative elements**: Paper lanterns (paper lantern) with Japanese characters, bonsai in corner, Japanese sake bottles display
- **Space**: Often below street level — basement or factory building floors

**Object Library**
- **Sake bottles**: Large takasake bottles (大吟醸) on shelves behind counter
- **Yakitori skewers**: Chicken meat on bamboo skewers, grilled visible
- **Beer taps**: Draft beer (Draft Beer) systems, Sapporo or Asahi brand
- **Small plates**: Various dishes — edamame, karaage (炸雞), takoyaki (章魚燒)
- **Lanterns**: Paper lanterns with warm bulb inside, slightly smoky appearance near tops

**Lighting Behavior**
- **Warm ambient**: 2700K-3000K warm white, intentionally dim
- **Paper lantern glow**: Each lantern creates pool of warm light
- **Counter lighting**: Stronger light on food prep area for kitchen visibility
- **Candle**: Small candles on tables for intimate atmosphere

**Social Density**
- After-work crowds (6-9pm): Dense with salarymen (打工仔) drinking
- Late night (10pm+): Quieter, more intimate groups
- Japanese expat community visible — Japanese language heard

**Proof-of-Life Objects**
- Beer glasses with lipstick marks
- Sake cup with remaining sake
- Yakitori bones on plate — partially eaten
- Someone taking photo of food for social media

**Unified Token Integration**
- Pair with **Token 08** (Night Light Collision) for warm interior night atmosphere
- Ambient: 2700K-3000K warm

---

### Location Token 10 — HONG KONG LAUNDROMAT (洗衣店)

**Research Source**: HK_TEXTURE_LIBRARY.md Location 10

**Visual Identity**
Self-service laundromats (自助洗衣店) found in old districts (深水埗, 旺角, 北角). Characterized by industrial washing machines (工業洗衣機) lined up, dryers (乾衣機) humming, plastic chairs for waiting, detergent vending machines (洗衣液售賣機), and the pervasive smell of fabric softener (柔順劑). Often run 24/7, fluorescent lighting, tiled floors.

**Architectural Cues**
- **Machines**: Front-loading washing machines (滾筒洗衣機) in rows, stainless steel or white plastic fronts
- **Floor**: White or light grey ceramic tiles (紙皮石), slightly cracked
- **Ceiling**: Low, fluorescent tube lights in plastic diffusers
- **No windows**: Interior spaces, climate controlled

**Object Library**
- **Washing machines**: Industrial-sized, coin-operated or stored-value card
- **Dryers**: Large tumbling dryers, heat emitting from tops
- **Plastic chairs**: Stackable chairs for waiting, faded colors
- **Laundry baskets**: Collapsible fabric laundry baskets (洗衣籃)
- **Detergent dispensers**: Wall-mounted units selling laundry detergent (洗衣液)
- **Fold tables**: Long folding tables (摺疊枱) for folding clothes
- **Fabric softener bottles**: Large bottles of fabric softener (柔順劑) behind machines

**Lighting Behavior**
- **Fluorescent dominant**: Harsh white 4000K+ fluorescent lighting
- **No warmth**: No tungsten or warm lighting, pure functional
- **Heat from dryers**: Slight haze visible near tops of dryers
- **Humid ambient**: Moisture from machines, slight fog near floor

**Social Density**
- Low density — people typically alone or with one other person
- Evening and late night (10pm-1am) busy — night owl activity
- Elderly frequently present — washing routine for those without home machines

**Proof-of-Life Objects**
- Clothes inside machine, visible through porthole, in motion
- Water on floor from machine door seals
- Detergent residue on machine fronts
- Someone folding clothes slowly, paying attention

**Unified Token Integration**
- Pair with **Token 06** (Humidity) for interior moisture effect
- Ambient: 4000K+ harsh fluorescent

---

### Location Token 11 — MTR PLATFORM (港鐵月台)

**Research Source**: HK_TEXTURE_LIBRARY.md Location 11

**Visual Identity**
Mass Transit Railway (港鐵) platform — distinctive by the route color-coding (藍色, 紅色, 綠色 etc. based on line), vinyl tile floors (甲級石屎地磚), escalators connecting levels, platform screen doors (月台幕門) installed in newer stations, route maps (路線圖) in yellow frames. The identity is institutional — safe, clean, climate controlled, slightly antiseptic.

**Architectural Cues**
- **Platform floor**: Dark grey vinyl tiles, slightly reflective, showing wear patterns
- **Platform width**: Standard ~6m width for most lines, some older narrower
- **Columns**: Concrete columns at regular intervals, route color bands
- **Ceiling**: Rectangular acoustic panels, exposed services (pipes, cables)
- **Platform screen doors**: Full-height glass doors (月台幕門) at stations post-2000
- **Old doors**: Metal sliding doors (氣動屏蔽門) at older stations without screen doors

**Object Library**
- **Route maps**: Yellow-framed LCD displays showing route, next train arrival
- **Warning tiles**: Yellow tactile tiles (盲人指引) at platform edges
- **Help points**: Emergency intercom (緊急求助電話) in yellow boxes
- **Seating**: Metal benches (金屬座椅) bolted to floor, no backrests
- **Advertising frames**: Backlit poster frames (廣告牌) between columns
- **Pillars**: Concrete pillars wrapped with route color band at ~1m height

**Lighting Behavior**
- **Fluorescent strips**: Continuous fluorescent tube runs, no shadows
- **No contrast**: Flat, shadowless lighting designed for safety
- **Slightly warm**: Newer stations use 4000K, older stations 5600K-6500K
- **Train lighting**: Train interior visible through windows, warm interior light

**Social Density**
- Extremely dense during rush hour (7-9am, 6-8pm) — body-to-body density
- Off-peak: Comfortable density
- Quietest: Late night after 11pm — very sparse, echo effect
- Eye contact avoidance: Cultural norm, everyone on phone

**Proof-of-Life Objects**
- Someone holding MTR ticket (車票) or Octopus card (八達通) near reader
- Bodies swaying with train motion through doors
- Phones with screen showing MTR app with arrival times

**Unified Token Integration**
- Pair with **Location Token 12** (MTR Interior) for complete transit system
- Ambient: 4000K-6500K flat fluorescent

---

### Location Token 12 — MTR INTERIOR (港鐵車廂)

**Research Source**: HK_TEXTURE_LIBRARY.md Location 12

**Visual Identity**
Inside MTR trains — recirculating air with slight warmth, vinyl seats (膠座椅) in route colors, pole handles (扶手柱), interior gangway connections (車卡貫通道). The confined space creates intimacy among strangers. Announcements in Cantonese, Mandarin, English. Scrolling LED route displays (路線顯示板).

**Architectural Cues**
- **Seat arrangement**: Longitudinal seats (縱向座位) along sides, some cross-seat sections
- **Poles**: Stainless steel vertical and horizontal handrails (扶手桿) at regular intervals
- **Doors**: Double doors (車門) at each end of car, with rubber seals
- **Windows**: Large windows at door positions, some tinted
- **Gangway**: Flexible accordion connection between cars (貫通道)

**Object Library**
- **Seats**: Cushioned vinyl, route color, slightly worn at edges
- **Handrails**: Brushed stainless steel, finger-grip texture, condensation visible
- **Route displays**: LED dot-matrix display showing station names in Chinese and English
- **Priority seats**: Orange color seats (關愛座) near doors
- **Next stop announcements**: LCD screens above doors showing route map
- **Emergency equipment**: Yellow emergency handle (緊急拉手) at each door

**Lighting Behavior**
- **Even fluorescent**: Interior lit by continuous fluorescent strips in ceiling
- **No shadows**: Even illumination from all sides, no depth
- **Train movement**: Light flicker when moving through tunnels
- **Window light**: Natural light entering through tunnel sections

**Social Density**
- Rush hour: Standing room only, bodies pressed, minimal personal space
- Off-peak: Seats available, people reading or on phones
- Eye contact: None during rush hour — everyone looking at phones or ceiling

**Proof-of-Life Objects**
- Phones showing MTR app or social media
- Hands gripping poles, condensation lines showing grip positions
- Earbuds (耳機) with wires trailing
- Standing passengers swaying with train motion

**Unified Token Integration**
- Complete transit system with **Location Token 11** (MTR Platform)
- Ambient: 4000K flat fluorescent

---

### Location Token 13 — KENNEDY TOWN WATERFRONT (堅尼地城海旁)

**Research Source**: HK_TEXTURE_LIBRARY.md Location 13

**Visual Identity**
Western District waterfront (西環海旁) — former container port area (葵涌貨櫃碼頭) now being revitalized. Characterized by concrete pier (混凝土平台), industrial harbor elements (起重機, 貨櫃), wide open horizon overwater, and HK Island skyline backdrop. The vibe is industrial meets recreation — people jogging, dog walking, fishing off the pier edge.

**Architectural Cues**
- **Pier surface**: Concrete with expansion joint lines (防滑紋), wide and flat
- **Railings**: Painted metal railings (鐵欄杆) in grey/white, slightly rust-stained
- **Harbor structures**: Container cranes (橋式起重機) visible in middle harbor, container stacks
- **Water edge**: Concrete edge with mooring rings (繫船柱), tidal marks visible
- **Lighting poles**: Simple metal poles with sodium vapor lights (鈉燈), orange-yellow

**Object Library**
- **Fishing rods**: People fishing from pier edge, telescopic rods, tackle boxes (魚具箱)
- **Jogger equipment**: Reflective vests, running shoes, water bottles
- **Dog walkers**: Small dogs on extendable leads, waste bag dispensers
- **Crane silhouettes**: Ship-to-shore cranes in background, iconic harbor shape
- **Container stacks**: Colored containers (blue, green, red) in background

**Lighting Behavior**
- **Warm sodium light**: Orange-yellow from street lamps, creates warm atmosphere at dusk
- **Water reflections**: Bright specular reflections on water surface
- **Sky gradient**: Orange to purple at sunset, reflected on water
- **Night**: Crane lights visible, ship navigation lights, city lights on horizon

**Social Density**
- Evening: Moderate density — joggers, dog walkers, families
- Weekends: More visitors, photography enthusiasts
- Early morning: Fishermen in small numbers, solitary activity

**Proof-of-Life Objects**
- Fishing line visible in water
- Jogger condensation visible in cool air
- Dog leash under tension
- Someone taking selfie with cranes behind

**Unified Token Integration**
- Pair with **Token 14** (Public Lighting Specificity) for sodium vapor lighting
- Pair with **Token 08** (Night Light Collision) for evening reflection system
- Ambient: 2000K-2200K sodium orange

---

### Location Token 14 — SAI YING PUN STAIR STREETS (西營盤樓梯街)

**Research Source**: HK_TEXTURE_LIBRARY.md Location 14

**Visual Identity**
Western District hill streets (西環) — stone steps (石級) descending hill, street-level shops on slope, buildings leaning over steps, drainage channels (雨水渠) running down center or side of steps. The vertical navigation creates exercise routine for residents. Visual identity: old Hong Kong scale, narrow streets (橫街窄巷), morning goods delivery by hand trolley (手推車).

**Architectural Cues**
- **Steps**: Stone or concrete steps, irregular height due to settling, metal handrails
- **Street sections**: Flat sections between step runs, shop frontages
- **Building separation**: Thin building widths (5-8m frontage), mid-building heights (5-10 floors)
- **Drainage**: Open concrete channel (明渠) sometimes running alongside steps
- **Light wells**: Small gaps between buildings creating vertical light shafts

**Object Library**
- **Hand trolleys**: Folding hand trucks (手推車) used by shop deliveries, parked on steps
- **Delivery goods**: Boxes of vegetables, boxes of meat from wholesale market
- **Trays**: Stacked plastic crates (膠箱) on sidewalks
- **Drying racks**: Bamboo clothing racks (竹衣架) on sidewalks, shirts and pants airing
- **Awnings**: Cloth awnings over shops, faded stripes
- **Door god**: Paper door god (門神) stickers on shop doors, slightly sun-rotted

**Lighting Behavior**
- **Directional light**: Steps face specific direction, creating directional shadow patterns
- **Building shade**: Tall buildings create shade on lower steps
- **Morning light**: East-facing steps get morning light, creating dramatic shadow angles
- **Street level**: Warm shop light spilling onto steps from open shop doors

**Social Density**
- Morning: Delivery workers, shop owners setting up
- Midday: Elderly residents descending/ascending, occasional visitor
- Evening: Quieter, residents returning home
- Dense but not crowded — small scale

**Proof-of-Life Objects**
- Hand trolley with delivery boxes, driver resting
- Plastic crates stacked at shop entrance
- Clothing on racks moving slightly in breeze

**Unified Token Integration**
- Core location for **Token 17** (Sai Ying Pun / Sheung Wan Verticality)
- Pair with **Token 02** (Sham Shui Po Tenement) for building context
- Ambient: Directional morning shadows

---

### Location Token 15 — QUARRY BAY HOUSING BLOCKS (鰂魚涌屋苑)

**Research Source**: HK_TEXTURE_LIBRARY.md Location 15

**Visual Identity**
Large-scale public and private housing complexes (屋苑) in Quarry Bay/Healthy Street (健康村). Characterized by high-rise slab blocks (高層大廈), landscaped podiums (平台花園), multi-level carparking basements, connecting footbridges (行人天橋). The scale is large — blocks 30-40 floors, arranged in parallel or pinwheel formations.

**Architectural Cues**
- **Block form**: Rectangular slab blocks (長方形大廈), concrete facade (混凝土外牆)
- **Window pattern**: Grid of window openings, some with aluminum shutters (鋁窗), some with晾衣桿 (clothes-drying poles)
- **Podium**: Open podium level (平台) with landscape, seating, children play equipment
- **Footbridge**: Covered walkway connecting blocks, elevated above podium (行人天橋)
- **Carpark**: Multi-level basement carparks, ramp entries visible at grade

**Object Library**
- **Clothes poles**: Metal or bamboo poles extended from windows (晾衫竹), with clothing
- **Air conditioning units**: Window units (窗口機) creating rhythm on facades, drip trays
- **Community facilities**: Elderly fitness equipment (長者健身區), children's slides
- **Planters**: Concrete planters with low maintenance shrubs
- **Bicycle parking**: Bike racks (單車泊位) on podium, colorful bikes
- **Signs**: Estate management signs (屋苑管理), flat numbers in metal plates

**Lighting Behavior**
- **Podium daylight**: Even daylight on podium, building shadows creating patterns
- **Facade reflection**: Window reflections showing sky, building faces reflecting each other
- **Night lighting**: Estate lighting (路燈) creating pools on podium, warm sodium
- **Interior light**: Warm yellow from residential windows at night, visible as points

**Social Density**
- High density: Thousands of residents in complex
- Podium activity: Families in evening, elderly in morning
- Children's areas: Dense with kids after school
- Quiet except at activity nodes

**Proof-of-Life Objects**
- Children's toys left on podium — ball, skipping rope
- Elderly person doing tai chi (太極) on podium in morning
- Clothes on poles with breeze movement
- Light on in apartment, someone visible moving inside

**Unified Token Integration**
- Pair with **Token 05** (Public Housing Block Geometry) for Harmony typology
- Pair with **Token 10** (Public Housing Laundry System) for window context
- Pair with **Token 16** (Wong Tai Sin Tenant Signage) for podium commercial context
- Ambient: Podium daylight / sodium night

---

## PART II: MATERIAL / BEHAVIORAL TOKENS (20)

### Token 01 — MONG KOK SIGNAGE LAYER

**Problem Statement**
Generic HK images show "neon signs." This is false. Mong Kok's signage is a **vertical collision** of hand-painted shop signs, peeling vinyl stickers, religious notices, Cantonese characters in varying font weights, and government health warnings layered at 3–4 depths. No two signs share the same material condition. AI models flatten this into "colorful backgrounds."

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
- Use only with street-level Mong Kong prompts
- Pair with humidity/haze token for summer conditions
- Separate signage into 3 depth layers: foreground (peeling), mid-ground (shop-front), background (distant billboard)
- Do not align signs; force collision and stagger

---

### Token 02 — SHAM SHUI PO TENEMENT LAYER

**Problem Statement**
AI models treat Sham Shui Po as "old HK" and produce brown/desaturated滤镜. Real Sham Shui Po tenement buildings are **structurally specific**: external metal staircases, window grilles (花碼),晾衫架 poles, subdivided units with mismatched window sizes, and a gray-green facade palette punctuated by neon shop signs. The district has a vertical logic AI ignores.

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

---

### Token 03 — WET MARKET VISUAL SYSTEM

**Problem Statement**
Generic "Hong Kong market" produces a fish market with ice and blue tarps. Real wet markets have a **specific visual hierarchy**: hanging poultry (已劏), open drains, mosaic tile walls, scale weight stalls, plastic basin stacking, and a specific spectral quality from morning light hitting wet concrete and fish scales. The smell is visual.

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

---

### Token 04 — CHA CHAAN TENG INTERIOR LAYER

**Problem Statement**
AI generates "Hong Kong cafe" as: red leather booth, checkered floor, neon sign outside. This is cha chaan teng as caricature. Real cha chaan teng interiors are: plastic laminate tables (often floral pattern), metal folding chairs, ceiling fans on low speed, wall-mounted menus with tape repairs, fluorescent tubes behind plastic dividers, and a specific color temperature from mixing tungsten (food warmers) with fluorescent (general lighting).

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

---

### Token 05 — PUBLIC HOUSING BLOCK GEOMETRY

**Problem Statement**
AI produces "Hong Kong public housing" as: repetitive windows in a block, possibly a podium. Real HK public housing has specific typologies: Harmony 1/2/3 block configurations, single-tier vs double-tier/corridor access, specific window-to-wall ratios, laundry pole configuration rules, and color-coding by estate (MTR 太子, 旺角, etc. have estate-specific palettes). The geometry is systematic but not uniform.

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

**Integration Rules**
- Specify Harmony type (1, 2, or new) — each has distinct geometry
- Estate color coding must be consistent with the estate type
- Laundry poles always at angle, never vertical
- Podium/base commercial use always visible at ground level
- Water stains run vertically on concrete (not random)

---

### Token 06 — HONG KONG HUMIDITY ATMOSPHERE

**Problem Statement**
AI produces "humid" as: slight blur, desaturated colors, maybe some haze. Real Hong Kong humidity (avg 78–95% in summer) has specific visual markers: heat shimmer near ground, condensation on cold surfaces, haze gradient (not uniform), visible moisture on metal, specific color shift toward green-blue in distant views, and a particular quality of shadow that is never fully black.

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

---

### Token 07 — OLD MALL DECAY SYSTEM

**Problem Statement**
AI produces "Hong Kong old mall" as: 1990s mall with generic Asian decor. Real old HK malls (the 1980s–90s era: 美好年代) have specific decay markers: cracked mosaic floors, faded gold accent paint, water-stained gyptile ceilings, roller-shutter closed shops, specific fluorescent tube arrangements, and a specific population demographic (elderly residents, small-batch traders, not tourists).

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

**Integration Rules**
- Specify roller-shutter percentage — empty mall without this reads as "nighttime" not "decaying"
- Elderly/social use must be present — empty mall without people reads as "abandoned" not "transitioning"
- Gold accent must be oxidized (not bright gold) — bright gold = new construction, not old mall
- Small-format mosaic tile (not large format) is critical for authenticity

---

### Token 08 — HONG KONG NIGHT LIGHT COLLISION

**Problem Statement**
AI produces "Hong Kong night" as: neon pink-blue dominant palette, sharp contrast. Real HK night has a specific light collision system: tungsten (warm, 2700K), fluorescent (cool, 4000K), neon (red/green/yellow, specific to shop type), LED (white/blue), and natural sky (deep blue, 6800K). These exist simultaneously and create specific color bleeding at boundaries.

**Real Photography References**
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

**Integration Rules**
- Minimum 3 light sources required in any HK night scene (tungsten + fluorescent + one neon color)
- Wet pavement is the color-mixing surface — always include wet floor with night lights
- Sky must be deep blue-black, not black — HK night sky has light pollution but retains blue
- Color bleeding at object edges is mandatory — light sources do not stay in their lanes
- Shadow only from tungsten — other sources too diffuse

---

### Token 09 — HONG KONG SIGNBOARD LANGUAGE

**Problem Statement**
AI produces Chinese characters but gets context wrong. Real HK signboards have a specific typographic system: traditional characters (not simplified), specific font choices (魏碑, 隸書, 超明體 for traditional; rarely used), mixed Chinese-English (茶餐厅 menu system), and most critically: the way characters are spatially arranged for phonetic reading (Cantonese reading order differs from Mandarin).

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

**Integration Rules**
- Match font era to shop type and approximate year of establishment
- Traditional characters only — simplified is an immediate authenticity breaker
- Vertical AND horizontal reading orders both acceptable — right-to-left only for specific retro Japanese-influenced contexts
- Decay on sign must be material-appropriate: rust on metal, peeling on vinyl, chalking on paint
- Font correlation (冰室=超明體) is hyper-specific and increases authenticity significantly

---

### Token 10 — PUBLIC HOUSING LAUNDRY SYSTEM

**Problem Statement**
AI produces "laundry" as: white sheets on clothesline, generic. Real HK public housing laundry is a specific visual system: bamboo poles at precise angles, specific fabric colors (white vests, colored睡衣, school uniforms), the 竹竿 (bamboo) vs 鐵竿 (metal pole) distinction, and the way laundry interacts with window grille (花碼) geometry.

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

**Integration Rules**
- Bamboo pole angle ~45° is mandatory — vertical or horizontal reads as wrong
- Fabric colors: white + navy + pastel only — no bright synthetic colors (unrealistic for public housing)
- Multiple floors visible — single-floor laundry is not authentic
- 花碼 interaction: fabric against window grille creates pattern that must be implied in lighting

---

### Token 11 — KOWLOON WALLS TYPOLOGY

**Problem Statement**
AI produces "Hong Kong wall" as: graffiti, concrete. Real HK walls have specific typologies: Tong Lau (唐樓) external walls with tile patterns, government wall murals (Bidet 1990s style), construction site walls (金屬圍板) with specific typography, and the specific patina of 50-year-old masonry in Mong Kok/Yau Ma Tei.

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

**Integration Rules**
- Specify wall type: Tong Lau (tile), government (mural), construction (圍板), or residential (concrete/masonry)
- Moisture gradient on masonry: always darker at base, lighter at top
- 1990s government mural has specific graphic style: bold outline, simplified figure, red-white-blue palette
- 金屬圍板 always has developer branding — no blank construction fence

---

### Token 12 — HONG KONG FERRY LIGHT SYSTEM

**Problem Statement**
AI produces "Hong Kong ferry" as: generic boat, maybe Victoria Harbour backdrop. Real Hong Kong ferry light has specific characteristics: the yellow-orange of the 燃燒器 (burner) in the engine room visible through hull gaps, the blue-white of navigation lights, the way ferry decks reflect in water at night, and the specific wind environment on the lower deck.

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

**Integration Rules**
- Specify Star Ferry vs other ferry — color livery differs
- Lower deck vs upper deck produces completely different light/social environment
- Harbor water is dark (not blue), reflections are orange-white (not blue reflection)
- Engine room amber glow is visible through gaps — this is a key authenticity marker

---

### Token 13 — YA U MA TEI GHOST SIGN LAYER

**Problem Statement**
AI produces no ghost signs or incorrect ghost signs. Real Yau Ma Tei has ghost sign layers: old painted signs from the 1950s–70s visible under current signage, fading on building facades, and a specific palette (chrome, red, white, black) from that era. Ghost signs in HK are being demolished — they have ~10 years of documented life left.

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

**Integration Rules**
- Ghost sign requires old building facade — new construction cannot have ghost signs
- Chrome ghost sign palette: red + chrome + white + black only (not multicolor)
- Ghost sign appears as "better preserved area" where current sign partially covers
- Fading must follow stroke pattern, not random blotches

---

### Token 14 — HONG KONG PUBLIC LIGHTING SPECIFICITY

**Problem Statement**
AI produces generic street lighting. Real HK street lighting has specific characteristics: the orange of HK street lamps (sodium vapor, 2000K), the way they create halos in humid air, the specific 路灯 (street lamp) post design (concrete or metal, specific arm configuration), and the way street light interacts with wet pavement.

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

**Integration Rules**
- Specify district age — old district (Yau Ma Tei) = sodium vapor only, new district = LED only
- Halo effect only with sodium vapor in humid conditions
- Wet pavement reflection is elongated (not circular point source)
- Alley single bulb is always slightly swaying (visual marker of authenticity)

---

### Token 15 — DIM SUM BREWERY FOG SYSTEM

**Problem Statement**
AI produces generic steam. Real dim sum/Douhua/豆品店 steam has specific visual characteristics: the way it rises in cold air-conditioned interior (visible steam vs invisible), the specific bamboo basket stack, the way steam interacts with overhead fluorescent lighting, and the humid-heat boundary at the kitchen entrance.

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

**Integration Rules**
- Air conditioning must be present — visible steam only occurs in cold interior
- Bamboo basket stack is 3-tier minimum — single basket is not authentic
- Fluorescent light above creates steam diffusion effect — this is mandatory for authentic dim sum interior
- Kitchen boundary visible steam wall is a key authenticity marker

---

### Token 16 — KOWLOON WONG TAI SIN TENANT SIGNAGE

**Problem Statement**
AI produces generic Chinese signs. Real Wong Tai Sin Estate (and similar 1980s-era public housing) has specific commercial signage on the podium level: the way 茶餐廳, 藥房, 髮型屋 signs relate to the podium geometry, the specific signage material (backlit acrylic, box sign), and the way signs collide vertically on podium face.

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

**Integration Rules**
- Podium must be 4–6 floors — lower podium is different estate type
- Shop types are standard for daily needs: at least 茶餐廳 + 藥房 + 髮型屋
- Vertical stacking: signs at different heights, not horizontal alignment
- Material aging: newer shops = acrylic (yellowing), older shops = painted metal (rusting)
- Estate name visible above commercial podium

---

### Token 17 — SAI YING PUN / SHEUNG WAN VERTICALITY

**Problem Statement**
AI produces "Hong Kong hillside" as: generic slope with buildings. Real Sai Ying Pun and Sheung Wan have specific vertical systems: the way streets incline at ~15–30°, the staircase streets (石板街), the mid-level walkway system, and how buildings stack vertically to accommodate slope. This creates visual perspectives AI cannot manage.

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

**Integration Rules**
- Staircase street must have iron railing — this is the authenticity marker
- Building stacking illusion: upper building base visible above lower building roof
- Perspective distortion: must force either looking-up OR looking-down vanishing point
- Dried seafood shop (海味) is specific to Sheung Wan ground floor — include when authenticating location
- Mid-levels Escalator visible when using Sheung Wan/Sai Ying Pun

---

### Token 18 — HONG KONG TROLLEYBUS / TRAM SYSTEM

**Problem Statement**
AI produces "Hong Kong tram" as: generic streetcar. Real HK trams and trolleybuses have specific visual characteristics: the Rv (revenue) numbering system, the way the pole collector interacts with overhead wire, the specific livery (green and cream for Kowloon trolleybus, double-decker red for tram), and the way they interact with traffic flow.

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

**Integration Rules**
- HK Island = tram (double-decker, overhead wire)
- Kowloon = trolleybus (single-decker, green-cream or advertising livery)
- Overhead wire must be visible — this is the defining visual element
- Collector pole angle must be shown (not vertical, not broken)
- Traffic density is mandatory — trams do not run in empty streets

---

### Token 19 — HONG KONG RAIN / MONSOON ATMOSPHERE

**Problem Statement**
AI produces "rain" as: blue-gray filter, wet surface. Real HK monsoon (四月, 六月–九月) has specific visual systems: the way rain appears in diagonal sheets (not vertical), the specific post-rain smell-implied visuals (steam from pavement), the way umbrellas create a sea of color at street level, and the specific amber-grey sky palette.

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

**Integration Rules**
- Rain is always diagonal (wind direction from South China Sea) — never vertical
- Sky is amber-grey, not blue-gray — specific monsoon palette
- Post-rain steam (pavement) is separate from rain — specify post-rain or during-rain
- Umbrella colors: black + navy + transparent only (bright colors rare in monsoon)
- No hard shadow when raining or immediately post-rain

---

### Token 20 — HONG KONG ELECTRICAL CHAOS / OVERHEAD LINE SYSTEM

**Problem Statement**
AI produces "Hong Kong电线" as: clean overhead lines. Real HK has an electrical chaos system: overhead power lines at multiple voltages (33kV, 11kV, 400V), telephone cables, fibre cables, and signage support wires all sharing the same pole corridor. This creates a specific visual spaghetti that is being slowly buried underground but remains visible in old districts.

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

**Integration Rules**
- Multiple wire types required: power (black) + telephone (gray bundle) + at least one signage support wire
- Wire drooping (catenary) must be visible — straight lines are not authentic
- Pole slightly tilted (not vertical) is common in old districts
- Wires pass behind signage — they do not avoid it, they collide with it
- Old districts (Yau Ma Tei, Sham Shui Po) have highest wire density — new districts less so

---

## PART III: INTEGRATION FRAMEWORK

### Token Priority Matrix

| District/Context | Location Token | Primary Material Token | Secondary Tokens | Ambient Token |
|-----------------|----------------|------------------------|------------------|---------------|
| Mong Kok Day | Location 07 | Token 01, Token 09 | Token 11 | Token 06 |
| Mong Kok Night | Location 07 | Token 01, Token 08 | Token 09 | Token 14 |
| Sham Shui Po Day | Location 14 (vertical) | Token 02 | Token 11, Token 20 | Token 06 |
| Sham Shui Po Night | Location 14 | Token 02, Token 08 | Token 07, Token 20 | Token 14 |
| Wet Market Morning | Location 04 | Token 03 | Token 06 | Token 06 |
| Public Housing | Location 15 | Token 05, Token 10 | Token 16 | Token 06 |
| Cha Chaan Teng | Location 08 | Token 04 | Token 15 | Token 06 |
| Sheung Wan | Location 14 | Token 17 | Token 09, Token 20 | Token 06 |
| Yau Ma Tei | Location 07 + 14 | Token 11, Token 13 | Token 01, Token 14 | Token 06 |
| Victoria Harbour | Location 13 | Token 12 | Token 08 | Token 14 |
| MTR Station | Location 11 | Token 11 | — | Token 06 |
| MTR Train | Location 12 | Token 12 | — | — |
| Monsoon Season | Any outdoor | Token 19 | Token 06, Token 20 | Token 06 |
| Old Mall | — | Token 07 | Token 04, Token 09 | Token 06 |
| Tai Kwun Evening | Location 02 | Token 09 | Token 08 | Token 14 |
| Izakaya Night | Location 09 | Token 08 | Token 15 | Token 14 |
| Kennedy Town | Location 13 | Token 14 | Token 08 | — |
| Quarry Bay Housing | Location 15 | Token 05, Token 10 | Token 16 | Token 06 |

### Token Combination Rules

1. **Minimum 3 tokens** per HK scene: 1 Location Token + 1 Material/Behavioral Token + 1 Ambient Token (when applicable)
2. **Never combine Token 06 (humidity)** with Token 19 (monsoon rain)** without specifying time sequence — they are different humidity conditions
3. **Token 09 (typography)** must be used when any signage is prominent — it is a forcing function for traditional characters
4. **Token 06 (humidity)** is ambient — use with any outdoor scene, adjust temperature by time of day
5. **Token 20 (electrical)** only in old districts — new districts have underground wiring
6. **Location Tokens** ground the scene geographically — always start with a location token for authentic geometry

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
- [ ] Location-specific architectural cues present (e.g., 花碼 window grille in public housing, staircase street iron railing in Sheung Wan)
- [ ] Proof-of-life objects appropriate to location (e.g., fish bags in Goldfish Street, hand trolleys on stair streets)

### Color Temperature Reference

| Source | Temperature | Context |
|--------|-------------|---------|
| Harsh fluorescent | 5600K-6500K | Old markets, laundromats |
| Standard fluorescent | 4000K-5000K | MTR, modern interiors |
| Warm LED/CFL | 2700K-3000K | Izakaya, residential, heritage |
| Tungsten | 2700K | Food establishments, shops |
| Sodium vapor | 2000K-2200K | Old district street lights |
| Wok fire | ~2000K | Dai pai dong cooking |
| Daylight indirect | 4500K-5500K | Overcast |
| Daylight direct | 5500K-6500K | Clear sky |
| Deep blue sky | 6800K | Night sky |
| Amber-grey monsoon | 6000K-7000K | monsoon sky |

---

## Version Notes

**V17 → V18 Changes:**
- Unified 15 specific location deep-dives with 20 material/behavioral tokens into single system
- Location Tokens provide architectural specificity: authentic geometry, materials, objects for real HK places
- Material/Behavioral Tokens provide behavioral realism: typography, decay, light collision, social density
- Ambient Tokens (06, 14, 19) cross-cut all locations for atmospheric consistency
- V17 treated HK as single visual class; V18 separates into location-specific + behavior-specific components
- V17 had no Cantonese typography token; V18 Token 09 introduces era-specific font system
- V17 had no humidity time-of-day specificity; V18 Token 06 introduces morning/afternoon/post-rain differentiation
- V17 had no overhead wire system; V18 Token 20 introduces electrical chaos as distinct anti-AI system
- V17 had no ghost sign layer; V18 Token 13 introduces disappearing 1950s–70s ghost sign documentation
- V17 had no public housing laundry geometry; V18 Token 10 introduces bamboo pole + 花碼 interaction system
- V18 adds integration priority matrix for token combination
- V18 adds anti-AI validation checklist with location-specific verification
- V18 adds proof-of-life object requirements per location

---

*HK Texture Engine V18 — Unified HK Texture Tokens*
*Version 1.0 — Architectural Specificity + Behavioral Realism*
*Document the real. Resist the generic.*
*Local HK people must recognize without captions.*