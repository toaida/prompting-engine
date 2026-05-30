# lil.troublr V6 — Visual Sociology & Photography Research Report

> Research Date: 2026-05-13
> Agent: lucy/hermes
> Focus: Smartphone realism · Motion · Temporal · Hand · Group social dynamics

---

## SECTION 1: SMARTPHONE CAMERA REALISM

### 1.1 iPhone HDR Artifacts

**Rendering Behavior:**
iPhone HDR works by capturing multiple exposures (3-7 frames) and blending them. In high-contrast scenes, this creates specific artifacts:

- **Highlight crush in bright areas:** Sky overexposed to white even in HDR photos. The phone's HDR isn't strong enough to recover blown highlights, especially in backlit situations.
- **Face luminosity jump:** When subject is in shade and background is bright sky, iPhone will sometimes over-brighten the face, making it look like a studio-lit portrait against a blown-out background. This is the "HDR face glow" artifact.
- **Chromatic aberration at high-contrast edges:** Purple fringing on backlit hair, especially at temple edges where light hits. This is a real iPhone artifact, not a lens flaw.
- **Ghost edge on moving subjects:** When the subject moves between HDR frames, there's a faint double-edge on the side of the body. This is "motion ghosting within a single frame" from the HDR stack.
- **Over-bright skin in backlit:** iPhone tends to lift shadow on skin too aggressively, making face look lighter/cleaner than real life.

**Artifact Vocabulary:**
- "iPhone HDR highlight crush"
- "ghost edge on subject periphery"
- "chromatic aberration at temple hair edge"
- "over-bright face in backlit HDR"
- "HDR stack misalignment on moving fabric"

**Realism Marker:** When an image looks "too well-lit for a backlit shot," it's an iPhone HDR over-correction. Natural backlit photos should have face 1-2 stops darker than iPhone produces.

---

### 1.2 Android Oversharpening

**Rendering Behavior:**
Most Android phones (Samsung, Xiaomi, OPPO) apply aggressive unsharp mask sharpening in their JPEG pipeline. The sharpening creates:

- **Halo edges:** White/dark line at the boundary of skin and background. More visible on neck/cheek edge against hair.
- **Skin texture over-emphasis:** Pores look like craters. Small imperfections become more prominent than in real life.
- **Hair strand definition:** Individual hairs become too visible, making hair look like a wig or rendered texture rather than organic.
- **Eye white sharpening:** The sclera of the eye becomes too crisp, looking unnatural in portrait mode.
- **"Texture painting" on smooth surfaces:** Flat surfaces like walls or fabric get artificial texture that wasn't in the scene.

**Realism Marker:** Android oversharpening is the OPPOSITE of AI smoothness. It adds texture. The key anti-AI move is to describe skin with LESS texture detail, not more.

---

### 1.3 Portrait Mode Depth Failures

**Rendering Behavior:**
Portrait mode uses dual-camera or ToF (time-of-flight) sensors to create depth maps for background blur. The failures:

- **Hair-depth confusion:** Wispy hair at temple or ear gets included in "background" and blurred. Stray strands disappear or become halos.
- **Collar-bust separation failure:** When subject's collar is near chest (bust area), depth map confuses fabric layers and blurs part of the chest area incorrectly.
- **Shoulder-edge halos:** Around the shoulder perimeter, there's a visible halo edge where subject meets blur. Subject edge is too crisp relative to the blur.
- **Glass/glass refraction:** Looking through glass in portrait mode causes complete depth map failure — glass is transparent but depth map treats it as a surface, blurring what's behind it.
- **Fence/mesh/barcode failures:** Any regular pattern behind subject causes depth map to confuse background elements with subject.
- **Depth jump at neck:** On neck/chin transition, the depth map has a visible seam. The face is sharp but the neck sometimes shows a "depth cliff."

**Artifact Vocabulary:**
- "portrait mode wispy hair dissolution"
- "collar-chest depth confusion"
- "halo edge at shoulder perimeter"
- "depth cliff at neck transition"
- "glass depth map failure"

**Realism Marker:** Portrait mode images are identified by the characteristic "sharp subject + wrong blur + halo edges." Real cameras with real shallow DOF have natural falloff, not algorithmic blur.

---

### 1.4 Night Mode Stacking Artifacts

**Rendering Behavior:**
Night mode captures 3-30 frames over 1-3 seconds and aligns/stacks them. Artifacts:

- **Ghost people:** If someone moves through the frame during capture, they appear as translucent ghost in the final image. This is a real accidental artifact.
- **Light trail fragmentation:** Car headlights or neon signs get broken into segments because frames don't align perfectly.
- **Flat lighting look:** Night mode brightens everything so much it loses the night atmosphere. Face looks like it was photographed at noon.
- **Color noise in midtones:** The stacking process introduces chroma noise (color speckling) in skin midtones — pink, green, and purple speckles in shadow areas.
- **Over-sharpened edges:** After alignment, edge enhancement is applied aggressively, creating the "AI-drawn" look on subject edges.

**Artifact Vocabulary:**
- "night mode ghost person"
- "fragmented light trail"
- "color speckling in shadow"
- "over-sharpened subject edges post-stack"
- "flattened night atmosphere"

---

### 1.5 Rolling Shutter

**Rendering Behavior:**
Most smartphone cameras use a rolling shutter (not global shutter). This means the sensor captures rows of pixels sequentially, not simultaneously. Effect:

- **Vertical subject tilt during fast pan:** If you pan quickly, a standing subject (like a person) appears tilted — top of head captured at a different time than feet, creating a "falling forward" look.
- **Propeller blade bend:** Circular shapes become curved arcs. Any radial element (spinning wheel, ceiling fan) bends.
- **LED screen flicker:** LED lights (which blink rapidly) appear as stripes of color variation across the frame.
- **Flash sync failure:** Under flash, the top and bottom of the frame are lit differently because flash fires while sensor is still reading.

**Realism Marker:** Rolling shutter artifacts are MOST visible in fast action. A candid walking photo with a slight rolling shutter tilt on the body = extremely realistic. The absence of rolling shutter in AI images is a tell.

---

### 1.6 Motion Ghosting

**Rendering Behavior:**
When subject moves during exposure (especially in low-light or with slow shutter), the image has:

- **Double-image at edges:** Moving limbs (arm, leg, hair) appear as double images with partial transparency between them.
- **Body blur trail:** Fast movement (dancing, running) creates a body trail — the body appears multiple times as a motion sequence.
- **Face stays sharp, body blurs:** In flash photography, face is frozen (flash is instantaneous) but body/limbs continue moving during the ambient exposure, creating a "frozen face + blurred body" image.

**Artifact Vocabulary:**
- "motion blur ghosting at arm"
- "body trail during dance"
- "frozen face + ambient body blur"
- "motion persistence at dress hem"

---

### 1.7 Mirror Selfie Lens Inconsistencies

**Rendering Behavior:**
Front cameras on smartphones have specific characteristics:

- **Focal length exaggeration:** The front camera is typically 20-24mm equivalent (wide-angle), making the face appear wider/closer than a mirror reflection. Nose looks bigger, face wider.
- **Face flip inconsistency:** Some phones flip the preview but not the final image, or vice versa. The subject often isn't sure which side "is their good side" and it shows in the asymmetry.
- **Selfie mirror correction:** In real mirrors, you see your reversed self. In photos, others see your non-reversed face. The discrepancy between mirror self-perception and photo reality causes subtle asymmetric poses — subject tilts to a "better side" that only exists in mirror.
- **Forehead magnification:** Wide front camera exaggerates forehead size. Subjects tilt chin down to compensate, creating a slightly upturned nose perspective.
- **Chin-up distortion:** To avoid forehead exaggeration, subjects tilt chin up, creating nostril-visible perspective.

**Realism Vocabulary:**
- "front camera wide-angle face distortion"
- "chin-up nostril perspective"
- "asymmetric mirror correction pose"
- "selfie angle compensation"

---

### 1.8 Digital Zoom Collapse

**Rendering Behavior:**
Digital zoom (as opposed to optical zoom) simply crops and upscales. At high zoom (5x, 10x digital):

- **Texture collapse:** Fine textures (skin pores, fabric weave) become smudged blocks.
- **Noise multiplication:** The upscaling algorithm amplifies noise from the original crop.
- **Edge aliasing:** Jagged edges on hair, eyebrows, clothing seams.
- **"Watercolor" areas:** Large flat areas (walls, sky, skin) develop a smudged, painted quality.

**Realism Marker:** AI images often look too sharp at zoom. Real digital zoom shows degradation. If an image claims to be "zoomed in," it should show the texture collapse.

---

### 1.9 TikTok / Xiaohongshu Compression Artifacts

**Rendering Behavior:**
Video/social platform compression (H.264/H.265) destroys image quality specifically in certain ways:

- **Block artifacts:** Large compression creates 8x8 pixel block boundaries visible in smooth gradient areas (sky, skin).
- **Color bleeding:** Sharp color transitions bleed into adjacent areas. Especially visible on: red lips against skin, dark hair against light background.
- **Stabilization wobble:** TikTok's in-app stabilization causes a slight "fish-eye breathing" effect — the image subtly zooms in and out rhythmically.
- **Frame interpolation:** To create smooth slow-mo, the app synthesizes intermediate frames, creating a "motion smear" in fast-moving areas.
- **Face beautification artifacts:** Beautify filter creates a characteristic "smooth but not detailed" skin look. It removes texture entirely, which is different from AI smoothness (AI adds texture).
- **Aspect ratio cropping:** Vertical 9:16 creates head-top and waist-cut framing that isn't seen in 4:3 or 1:1.
- **Screenshot vs. export quality:** A screenshot of a TikTok is lower quality than a video export. The artifact type differs.

**Artifact Vocabulary:**
- "H.264 block artifacts in sky/skin"
- "color bleeding at lip-skin boundary"
- "face beautification texture removal"
- "vertical 9:16 head-cut framing"
- "video stabilization breathing"

---

## SECTION 2: MOTION REALISM

### 2.1 Candid Walking Photography

**Weight-Transfer Vocabulary:**
Walking creates a predictable cycle of weight transfer:

1. **Heel strike:** Foot lands heel-first. Body weight shifts forward. Front foot is planted; back foot is pushing off.
2. **Mid-stance:** Weight over planted foot. Hip rises slightly as opposite leg swings forward.
3. **Toe-off:** Back foot pushes off. Body moves forward. Front hip is the high point of the stride.
4. **Flight phase:** Both feet briefly off ground (running only; walking has no flight phase at normal pace).
5. **Opposite heel strike:** Cycle repeats.

**Key Visual Moments:**
- The "mid-stride" moment: Both feet visible, one forward (toe down), one back (pushing off). This is the most dynamic walking pose.
- The "planted" moment: Weight fully on one foot, other foot swinging through. Creates a still, grounded moment.
- The "turn" moment: Walking and turning creates body rotation. Shoulders lead, hips follow.

**Asymmetry:**
- Walking pace varies: Fast walk = more forward lean, more arm swing. Slow walk = more upright, minimal arm movement.
- Bag-carrying side: If carrying a bag on one shoulder, that shoulder drops 1-2cm. The arm on bag side swings less. Hip on bag side tilts slightly down.
- Shoe type changes gait: Heels shorten stride and slow pace. Sneakers allow longer stride. Platform shoes add bounce.

**Movement Vocabulary for Prompt:**
- "weight transferring to front foot"
- "mid-stride — left leg planted, right foot pushing off"
- "bag-carrying hip tilt (right shoulder)"
- "slow casual pace — minimal arm swing"
- "fast walk — exaggerated arm counter-swing"

---

### 2.2 Commuter Movement

**Weight-Transfer on Public Transit:**

- **MTR/Subway standing:** Bracing against motion. Feet are shoulder-width. One hand on overhead rail or pole. Body leans slightly into motion direction. Free hand may hold phone or bag.
- **Bus standing:** More body sway than subway. Body adjusts constantly to bus motion. One foot slightly ahead of the other for stability.
- **Ferry standing:** Rocking motion. Body follows the wave rhythm. Slight knee bend to absorb motion.
- **Escalator:** Fixed position. Slight holding-on posture. One hand on railing or holding bag strap. Eyes may be on phone.

**Commuter Fatigue Markers:**
- Posture collapse: Shoulders roll forward, chin tilts forward. Body "shrinks" from fatigue.
- Weight shifts to one side more (asymmetric standing).
- Standing with eyes closed (commuting with eyes closed = public transport exhaustion).
- Bag sliding down shoulder (fatigue lowers muscle tone).

**Movement Vocabulary:**
- "standing balance sway on bus"
- "overhead rail grip — arm extended"
- "shoulder roll fatigue collapse"
- "eyes closed on MTR (exhausted)"

---

### 2.3 Nightlife Movement

**Dancing:**
- **Casual club dancing:** Minimal foot movement. Body sways from hips. Arms may be up or loose. Movement is primarily torso, not legs.
- **Individual groove:** Head moves independently from body. One hand may touch hair, neck, or face. Hip rotation is the primary movement.
- **Partner dancing:** Body distance changes. One person leads (usually the man — hand on lower back). The woman turns under arm. Eye contact maintained or broken.
- **Drunk dancing:** Larger, less controlled movements. Balance shifts are exaggerated. Laughter is visible (head back). Arms wave more.

**Fabric Lag Systems:**
- **Hair:** Hair lags behind head movement by 2-5 frames. When head snaps left, hair continues right, then whips back. The lag increases with: hair length, product absence, humidity.
- **Dress hem:** Mini dress hem moves with hip rotation. Maximum swing occurs 2-3 frames AFTER the hip has already reversed direction. Hem continues rotating when body has stopped.
- **Long earrings:** Swing with momentum. When head turns, earrings swing in opposite arc. Heavy earrings (hoops, drops) swing more than studs.
- **Bag (crossbody):** Crossbody bag swings at a different frequency from body movement. When stopping suddenly, bag continues swinging forward.
- **Sleeve:** Long sleeves (especially loose) trail behind arm movement by 1-2 frames.

**Motion Vocabulary:**
- "hip rotation sway — arms loose"
- "head hair lag during snap turn"
- "dress hem continued rotation after hip stopped"
- "crossbody bag pendulum swing"
- "earring counter-swing to head turn"

---

### 2.4 Turning-Body Motion

**Full-Body Turn:**
A natural turn involves the kinetic chain: eyes lead → shoulders rotate → hips follow → feet adjust.

- **Recognition turn:** She sees something, turns toward it. Sequence: eyes, head, shoulders, torso, hips, feet. Takes 0.3-0.5 seconds.
- **Casual look-back:** Head and shoulders turn without moving feet. Upper body rotation only.
- **Pivot turn (walking direction change):** Front foot plants, back foot pushes off, body rotates on planted foot.
- **Stop-and-turn:** Full stop, then turn. More controlled. Used when something is interesting enough to stop for.

**Fabric Behavior During Turn:**
- **Hair:** Maximum hair lag during turn. Head is rotating but hair is still moving in original direction. Creates "hair waterfall" effect at turn apex.
- **Tight dress:** Rotates with body. Follows closely.
- **Loose dress:** Rotates with delay. Body has turned, dress is still rotating to catch up.
- **Coat/jacket (open):** Back of coat swings outward during turn (centrifugal force), then settles.

**Balance Shift Vocabulary:**
- "planted foot pivot — body rotating on heel"
- "recognition turn — eyes lead, shoulders follow"
- "loose coat back swing during turn"

---

### 2.5 Hair Lag Physics

**The Physics:**
Hair is subject to inertia. When the head moves, hair continues in its original direction and velocity. The lag depends on:

- **Length:** Longer hair = more mass = more lag
- **Texture:** Straight hair lags less (aerodynamic). Curly/wavy hair lags more (more mass per unit length)
- **Weight/product:** Heavy products (oils, serums) increase lag. Dry shampoo = less lag (lighter)
- **Humidity:** Humidity makes hair heavier and less aerodynamic = more lag
- **Braids/ponytail:** Hair in a style becomes a single mass. The point of attachment (ponytail elastic) is where rotation originates. The longer the ponytail, the more delay.

**Hair Lag Moments:**
1. **Snap turn:** Hair continues forward while head turns. Maximum visual drama.
2. **Stop:** Head stops, hair continues forward (slightly), then springs back.
3. **Wind entry:** Head enters wind zone. Hair is suddenly pushed backward while head is stationary = "frozen in moving wind" moment.
4. **Sit down:** Head moves toward pillow/lap. Hair falls/drapes over shoulder with gravity, not head movement.

**Vocabulary:**
- "hair inertia lag after snap turn"
- "ponytail swing delay during stop"
- "humid air heavy hair lag"
- "hair draping over shoulder on sit"

---

### 2.6 Bag Swing Mechanics

**Crossbody Bag:**
- At rest: bag hangs at hip, strap at 45-degree angle across torso.
- Walking: bag swings forward as body moves forward. Bag reaches maximum forward swing at mid-stride. At toe-off, bag swings back.
- Speed of swing: Slower than body movement. Bag oscillates 2-3 times slower.
- Stopping: Bag continues forward after body stops. Will swing past body and crash into hip (bag bump).

**Shoulder Bag:**
- On the shoulder: bag slides and bounces with each step.
- Shoulder drop: Without holding the bag strap, gravity pulls bag down with each step. Bag may slip down arm.
- Arm adjustment: Subject raises shoulder to compensate for bag sliding. This shoulder hiking is a fatigue marker.

**Handbag Clutch:**
- No swing. Position controlled entirely by hand.
- Hand grip changes: Tight at rest, looser when hands-free.

**Vocabulary:**
- "crossbody bag forward oscillation mid-stride"
- "bag crash into hip after stop"
- "shoulder hiking to prevent bag slide"
- "bag bounce on each step"

---

### 2.7 Imperfect Balance Shifts

**Natural Balance Behavior:**
Humans are never perfectly balanced. We constantly make micro-corrections.

- **Standing still:** Feet are shoulder-width apart. Body makes constant tiny sway adjustments. Sway frequency: 0.1-0.3 Hz (10-30 seconds per cycle). These are invisible in photos unless at slow shutter.
- **One-leg standing:** When standing on one leg (putting on shoe, getting off bus), the other hip drops (contralateral tilt). Body leans toward standing leg.
- **Leaning to see:** When trying to see past someone in front, body leans forward and to one side. Head tilts.
- **Intoxication balance:** Wide stance, larger sway, slower corrections, hands used for balance (holding wall, person, or bag).

**V6 Application:**
For any shot where she's standing still, there should be subtle asymmetry:
- Weight on one leg more than the other
- Slight shoulder drop on bag-carrying side
- One hip higher than other

---

## SECTION 3: TEMPORAL REALISM

### 3.1 Before vs. After Going Out

**The "Before" State (pre-event preparation):**
- Makeup: freshly applied, precise lines, perfect coverage, product still on surface of skin
- Hair: freshly styled, no frizz, product holding shape, as left by iron/brush
- Outfit: unwrinkled, pristine, no deodorant marks, no under-arm fabric stress
- Expression: energized, excited, adrenaline-affected, eyes bright
- Skin: moisturized, slight shine from primer, no oil breakthrough yet

**The "After" State (3-4 hours in):**
- Makeup: beginning to settle into fine lines, especially around eyes and mouth; slight creasing in smile lines; lip color slightly faded at inner lip
- Hair: beginning to lose style, slight expansion from heat/dancing, humidity effect; roots starting to show (if colored); any styled volume collapsing
- Outfit: deodorant marks under arms (white/dark marks from fabric stress); slight wrinkles from sitting; hem may have shifted; one heel scuffed
- Expression: slightly tired, smile slightly less controlled, eyes slightly less bright (not dead, just less peak)
- Skin: oil breakthrough in T-zone; makeup settling; slight shine in nose/forehead area; any dress/blouse has shifted slightly

**Key Temporal Markers:**
- "3-hour makeup creasing at smile line"
- "t-zone oil breakthrough"
- "root growth visible at crown"
- "deodorant friction marks under arm"
- "hem shifted from seated"

---

### 3.2 Commuter Fatigue

**Morning Commute (7-9am):**
- Skin: Puffiness from sleep (especially under eyes). Post-shower glow still visible (if showered before). Minimal makeup at this point (or none).
- Hair: Post-sleep style may still be present (flat on one side if slept on it). Post-shower hair still damp at roots.
- Expression: Neutral to slightly tired. Coffee in hand. Eyes slightly dull. Phone in other hand.
- Outfit: Clean, unwrinkled, at peak condition. Morning outfit hasn't had time to degrade.
- Posture: Upright at start of commute. Gradually collapses over 30-60 min on transit.

**Evening Commute (6-9pm):**
- Skin: Day-old makeup (if worn). Oil and environmental pollution buildup. Slight dullness.
- Hair: Humidity/rain/AC has affected it. May be frizzier than morning. Flat at crown from transit headwear.
- Expression: More tired than morning. Social battery lower. Less smile energy.
- Outfit: Has been worn all day. Wrinkles from sitting. Possible food stains (lunch). Under-arm marks from heat.
- Posture: More collapsed. Shoulders more forward.

**Vocabulary:**
- "morning eye puffiness"
- "evening T-zone oil accumulation"
- "transit hour posture collapse"
- "evening shoulder roll"

---

### 3.3 Nightlife Temporal Progression

**Arrival (9-11pm):**
- Peak of pre-event preparation. Outfit pristine. Makeup fresh. Hair perfect. Energy high. Expression excited.

**Peak (12-2am):**
- First alcohol/social glow. Skin flushed from warmth/dancing. Eyes brighter. Expression more open. Confidence elevated.
- Hair: Beginning to be affected by heat (dance floor) or humidity (outdoor smoking area). Slight frizz at temples. Volume may have collapsed.
- Makeup: Flash photography has affected color (see CCD section). Lip color may have transferred to glass.

**Late Night (2-4am):**
- Energetic crash beginning. Eyes slightly droopy. Expression more relaxed/controlled. Laughter more genuine but less frequent.
- Makeup: Significantly worn. Eyeliner may have smudged. Foundation may have settled into lines. Highlighter still visible (oils make it glow more, not less).
- Hair: Heat/damage fully visible. Frizz not just at temples now. Some style may be completely lost.
- Outfit: Has been danced in. Wrinkled from leaning. Possible drink spill. Heels may have been removed.

**Dawn (4-7am):**
- The "morning after" preparation. Minimal energy. Eyes at their most tired. Expression is most genuine — no social performance left.
- Makeup: Mostly gone or significantly degraded. What remains is the "survivor" makeup — the products that lasted.
- Hair: Whatever style was there is largely gone. Natural texture is showing through.

**Vocabulary:**
- "arrival peak makeup precision"
- "1am flash photography color bloom"
- "3am eye droop + genuine smile"
- "4am survivor makeup"
- "post-dance frizz expansion"

---

### 3.4 Post-Gym Appearance

**Immediately Post-Workout:**
- Skin: Flushed, red, particularly on cheeks, neck, and upper chest. Sweat is visible on forehead, hairline, neck, and collarbone area. Skin has "post-exercise glow" — not the dewy glow of skincare, but the vascular flush of exertion.
- Hair: Sweat at hairline. Ponytail may have slipped. Roots are wet. Any styled hair is now flat at forehead.
- Face: Slightly swollen from exertion (not puffiness — actual inflammation from muscle use). Eyes slightly bloodshot. Makeup is gone (if worn).
- Expression: Relaxed, satisfied. A natural high from endorphins. Less self-conscious.

**30-60 Minutes Post-Workout:**
- Skin: Flush fades. Oil begins to appear as sweat dries. The "sweat-to-oil" transition.
- Hair: Hair begins to dry in the shape of the movement. Flyaways at forehead from sweat drying.
- Face: Swelling reduces. Glow becomes less vascular, more sebum-based.
- Posture: Shoulders roll back more (post-workout confidence). Muscle fatigue sets in (affects how she sits, stands).

**Vocabulary:**
- "post-exercise vascular flush"
- "sweat at hairline + forehead"
- "sweat-to-oil transition"
- "post-workout relaxed shoulders"

---

### 3.5 Makeup Wear Over Time

**First Hour:**
- Foundation: Still on surface. Seamless. Pores visible through makeup (product sitting in pores).
- Eye makeup: Cream products (cream blush, cream shadow) may have migrated slightly — creased into smile lines.

**3-4 Hours:**
- Oil breakthrough: T-zone becomes visible. Nose oil makes foundation look "melted" (darker shade showing through). Nose shine is most visible.
- Lip color: Outer edge fades first. Inner lip (wet area) loses color fastest.
- Eye makeup: Inner corner may have creased. Mascara may have transferred to under-eye (light smudge).
- Blush: Cream blush becomes less visible. Powder blush may look cakey where oil has accumulated.

**6+ Hours:**
- Foundation: Settled into fine lines. Pore filling effect has reversed — pores look more visible through makeup.
- Concealer: Creased under eyes. May have "caked" in fine lines.
- Setting spray (if used): May have worn off in T-zone. Oil zone is uncontrolled.
- Overall: Makeup has a "lived in" look. Not ruined, not fresh. The subject still looks good but it's clearly later in the day.

**Vocabulary:**
- "3-hour T-zone oil breakthrough"
- "inner lip color fade"
- "under-eye concealer creasing"
- "nose foundation melt"

---

### 3.6 Humidity Damage Over Time

**First 30 Minutes Outside (HK Summer):**
- Hair: Slight frizz at temples. Flyaways beginning. Volume at crown slightly reduced.
- Makeup: Dew point reached. Skin appears dewy (but it's sweat, not glow). Blotting paper may be needed.
- Outfit: Light fabrics are absorbing humidity. Slightly heavier drape than air-conditioned space.

**1-2 Hours:**
- Hair: Pronounced frizz. Loss of style. Flyaways at temples + crown. Sleek styles (straight, pulled back) most affected.
- Makeup: T-zone oil + humidity sweat = makeup slide. Makeup may be transferring to hands when touching face.
- Skin: Combination of sweat and oil. Pore appearance more pronounced.

**3+ Hours:**
- Hair: Maximum damage. Some styles completely collapsed. Natural texture fully visible. May look significantly different from morning.
- Makeup: Slide is obvious. Makeup may look patchy — some areas gone, some still present.
- Outfit: Absorbed humidity. May feel heavy on body. Natural fabrics (cotton, linen) may show sweat marks.

**Vocabulary:**
- "30-minute temple frizz onset"
- "2-hour hair volume collapse"
- "humidity sweat + oil combination"
- "sweat mark at collar"

---

### 3.7 Late-Night Exhaustion

**Expression Markers:**
- Eyes: Heavy eyelids (not closed — just not fully open). Eyes appear smaller. The muscle that holds eyes open is fatigued.
- Mouth: Lips slightly parted. Less controlled smile (asymmetric or wobbly smile line).
- Eyebrows: Lower position than alert state. At rest, eyebrows sit 2-3mm lower when tired.
- Posture: Head tilts forward (chin toward chest). Shoulders roll. Spine curves.
- Hands: May prop up head. Hand near face (supporting chin) is a tiredness signal.

**Skin Markers:**
- Under-eye: Darker. Due to pooling blood from fatigue + thinner skin in that area.
- Color: Duller. Less blood flow to surface = paler, less vibrant skin tone.
- Texture: Skin may look slightly "thinner" — more translucent at nose/under-eye.

**Vocabulary:**
- "heavy eyelid fatigue"
- "forward head tilt with chin drop"
- "tired mouth — lips slightly parted"
- "under-eye shadow pooling"

---

### 3.8 Travel Fatigue

**Long-Haul Flight Effects:**
- Skin: Extremely dry (airplane recycled air = 10-15% humidity). Foundation may flake. Lips are cracked. Eyes are puffy.
- Hair: Static electricity from recycled air = hair stands away from head. "Frizzy halo" effect. No humidity outside at altitude (relative humidity is low but absolute humidity at altitude is very low).
- Face: Puffiness from altitude + sitting + fluid retention. "Flight face" = puffy + pale + dry.
- Outfit: Wrinkled from sitting. Wrinkles are most severe at seatbelt area (waist), upper thigh (edge of seat), and back of legs.
- Posture: Slumped from discomfort. May have sat in awkward positions to sleep.

**Arrival (First Hours):**
- Eyes: Bloodshot from recycled air and alcohol (if consumed). Still puffy.
- Hair: Static has resolved (indoor humidity helps). Still limp.
- Expression: Disoriented. Slightly confused. "Where am I?" expression.
- Outfit: Still wrinkled. She may have changed clothes but wrinkles persist.

**Vocabulary:**
- "airplane recycled air dry skin"
- "static electricity hair frizz"
- "flight face puffiness + pallor"
- "seatbelt wrinkle at waist"

---

## SECTION 4: HAND & FINGER REALISM

### 4.1 Realistic Phone Holding

**Grip Types:**

**Type 1: Two-Hand Bracket (Selfie/camera)**
- Both hands hold phone from sides or bottom
- Thumbs on screen (may be covering part of screen)
- Phone tilted slightly toward face
- Elbows not tucked (tucked elbows = selfie arm extension)
- Slight phone rotation (not perfectly level)

**Type 2: One-Hand Grip (Bottom)**
- Phone held in palm, fingers wrapped around side/back
- Thumb on screen for scrolling
- Wrist bent to angle phone toward face
- This is the most common "reading" or "texting" grip

**Type 3: One-Hand Grip (Pinch)**
- Phone held between thumb and index finger (tablet style)
- Less stable — phone may be resting on fingers
- Used for taking photos or quick checks

**Finger Behavior on Phone:**
- Thumb doesn't move smoothly when scrolling — it taps in segments
- Index finger may be hovering (not touching) near screen for stability
- Other fingers spread to stabilize phone in palm
- When typing: fingers move rapidly in small segments, not flowing
- Pinky finger often extended to support bottom of phone (iPhone size)
- "Phone thumb" — thumb joint has a slightly different bend angle than index finger

**Vocabulary:**
- "one-hand grip — fingers spread for stability"
- "pinky extended as phone base"
- "thumb hovering near screen while holding"
- "wrist bent to angle phone toward face"

---

### 4.2 Drink Holding

**Cup/Glass Grip:**

**Wine Glass (bowl):**
- Stem held between thumb and index finger (the "correct" way) OR
- Bowl held in palm (casual — glass is between thumb and fingers, palm facing inward)
- When holding bowl, fingers curve around the bowl shape
- Finger position reveals intoxication level: correct grip = more sober, palm grip = relaxed/drunk

**Beer Bottle/Can:**
- Four fingers wrapped around body
- Thumb along side
- Index finger may extend to touch label (reading alcohol content/brand)
- Condensation on bottle makes grip tighter (fingers wrapped hard)
- Can: fingers may leave condensation dents in the aluminum

**Bubble Tea / Cup:**
- Both hands: one supporting bottom, one wrapping around body
- One hand: fingers wrapped through the handle (if present)
- Straw in position: index finger + middle finger pinch straw; thumb on cup
- No straw: direct cup drinking position — cup lifted to mouth, fingers spread on body

**Vocabulary:**
- "palm-grip wine glass — relaxed"
- "condensation dent in beer can"
- "straw pinch between index + middle finger"
- "both hands supporting bubble tea cup base"

---

### 4.3 Sleeve Interaction

**Sleeve Pull:**
- Pulling sleeve over hands (cold weather, shyness, covering)
- Sleeve pulled past wrist to knuckles — hands are inside sleeves
- Thumb emerges from sleeve hole while rest of hand is covered
- This is the "I want to disappear" / cozy / shy hand behavior

**Sleeve Cuff:**
- Cuffing sleeves — rolling sleeves up
- One cuff higher than the other (asymmetric — she started one side, forgot the other)
- Cuff falling down — it was rolled but has unrolled during activity
- Fingerless gloves effect: when sleeve is long enough to cover hand but she needs fingers free

**Sleeve Stretch:**
- Sleeve being pulled taut by other hand (checking time, fidgeting)
- Stretch lines visible at wrist where fabric is tensioned
- When released, sleeve returns to normal (but repeated stretch creates permanent wrinkle line)

**Sleeve Fabric Wear:**
- Inner wrist area: Most common deodorant mark location
- Outside of wrist: Watch/band tan line visible
- Cuff area: Lip balm or product transfer (shiny mark from applying balm, then touching cuff)

**Vocabulary:**
- "sleeve pulled over knuckles — hands inside"
- "asymmetric sleeve cuff — one side higher"
- "cuff fabric stretched taut by other hand"
- "deodorant mark at inner wrist"

---

### 4.4 Fidgeting Behavior

**Common Fidget Patterns:**

**Hair Fidget:**
- Twirling a strand of hair (usually left side of face — right-handed people use left hand on left side)
- Playing with ponytail elastic
- Adjusting hair behind ear
- Pushing hair behind ear
- The fidget often accompanies thinking or boredom

**Clothing Fidget:**
- Pulling at shirt hem (straightening)
- Adjusting collar
- Playing with jewelry (ring spin, bracelet fidget)
- Lint picking (imaginary or real)

**Object Fidget:**
- Tapping fingers on surface (table, phone, glass)
- Pen clicking
- Straw bending (paper straw)
- Wrapping/unwrap phone charging cable

**Hand Fidget (when idle):**
- Crossed fingers (casual)
- Hands clasped (nervous or cold)
- One hand holding the other (protective, tired)
- Pointing at nothing (thinking)
- Chin prop (tired or bored)

**Vocabulary:**
- "twirling left temple strand — right-handed fidget"
- "shirt hem straightening pull"
- "ring spin — index finger rotation"
- "hands clasped — protective posture"

---

### 4.5 Hair Touching

**Hair Touching Moments:**

**Hair Push (casual):**
- Palm flat on forehead, pushing hair back
- Or fingers combing from forehead to crown
- Results in: hair displaced at forehead, flyaways created
- After touch: hand leaves, hair stays pushed back for 10-30 seconds

**Hair Tuck (multiple types):**
- Tuck behind ear (index finger pushes hair, ear stops it)
- Tuck into collar (hand pushes hair under collar at neck)
- Tuck into shirt (hand pushes hair down shirt neckline — intentional intimate or nervous gesture)
- The "failed" tuck: hair falls back out immediately

**Hair Hold:**
- Holding hair away from neck (hot weather)
- Holding hair up while putting on necklace
- Lifting hair off neck to cool down

**Hair Play:**
- Split-end examination (picking at ends)
- Hair tangling/twisting between fingers
- This happens when bored or anxious

**Aftermath of Hair Touch:**
- Finger prints in hair (hair displaced in the shape of the finger)
- Slight oily sheen where fingers touched (natural hair oil transfer)
- Displaced flyaways remain after hand leaves

**Vocabulary:**
- "hair push — palm flat on forehead"
- "failed ear tuck — hair falling back out"
- "neck cool — hair lifted away"
- "finger print displacement in hair"

---

### 4.6 Bag Strap Gripping

**Shoulder Bag Strap:**
- Hand gripping strap while carrying
- Grip may slide up and down strap as weight shifts
- Finger impressions visible in leather strap after holding
- Thumb rubbing along strap edge (fidget behavior)

**Crossbody Strap:**
- Hand holds strap at hip level (to control swing, to shorten effective length)
- Fingers wrap around strap
- Strap may be twisted between fingers (fidget)

**Handbag Handle:**
- Hands alternate gripping each handle
- Arms may cross (hugging bag) when standing in crowd
- Fingers may wrap around handle (single grip) or hands may go through handle (double grip)
- "Bag on forearm" — handle at elbow, bag on forearm (hands free)

**Strap Position Shift:**
- When tired: strap slides off shoulder (gravity + muscle fatigue)
- When in crowd: pulls bag closer to body (protective)
- When hot: bag held away from body (avoid sweat)

**Vocabulary:**
- "hand gripping crossbody strap at hip"
- "strap slide off shoulder — fatigue"
- "bag hugged close in crowd"
- "twisted strap between fingers — fidget"

---

### 4.7 Seated Hand Behavior

**Table Seated:**
- Both hands flat on table (relaxed, open)
- One hand propping chin (tired)
- Hands wrapped around cup/glass
- Arms crossed on table (leaning forward)
- Arms off table (leaning back)

**Chair Seated (no table):**
- Hands on knees (relaxed)
- Hands clasped between knees
- One hand on armrest
- Both arms on armrests
- Hand holding phone on lap
- Arm draped over chair back

**Floor/Casual Seated:**
- Hands flat on floor (supporting weight)
- Hands on ankles
- Arms hugging knees
- One arm draped over eyes (lying down)

**Hand Position Patterns by Mood:**
- Hands visible and open = relaxed/social
- Hands hidden (in lap, crossed) = reserved/nervous
- Hands touching face = thinking/tired
- Hands gesturing = engaged/excited

**Vocabulary:**
- "hands flat on table — relaxed open"
- "one hand propping chin — tired lean"
- "hands clasped between knees — reserved"
- "arms draped over chair back — casual power"

---

## SECTION 5: GROUP SOCIAL DYNAMICS

### 5.1 Female Friend Group Photos

**Photo Hierarchy in Groups:**
- Central position = highest status (consciously or unconsciously assigned)
- Front row (closer to camera) = attention focus
- Back row = peripheral but included
- Edge = lower status OR new member

**Group Camera Dynamics:**
- Who takes photo: Usually one person steps out, gives phone to a designated photographer or uses timer.
- The "stepping out" moment: Subject steps back to join group, adjusting position.
- Timer group: Everyone scrambles into position, last 3 seconds are chaotic, final 1 second everyone freezes with forced smiles.

**Body Language in Groups:**
- Arm around shoulder (same height = comfort)
- Arm around waist (intimacy — closer than shoulder)
- Hand on back (guiding/supporting)
- Touching hair of friend (casual affection)
- Brace lean (leaning against friend for support or to look casual)

**Overlapping Body Language:**
- When close, bodies overlap in frame
- Forearms cross (one person's arm over another's shoulder)
- Hair overlaps into adjacent frame space
- Shopping bags overlap at feet

**The "Decoy" Photo:**
- One person is clearly the intended subject, others are incidental
- The incidental people are blurry or partially cropped
- The intended subject is sharp and centered

**Vocabulary:**
- "group central position — status"
- "arm around waist — intimate friendship"
- "forearm overlap on shoulder"
- "decoy background friends"

---

### 5.2 Nightlife Snapshots

**Group Nightlife Photography:**
- Flash burst: Most impactful nightlife photos use on-camera or held flash. Creates flat, bright subject against dark background.
- Arms holding phone high: The "arm extended high" shot — common in clubs where crowd blocks direct shot.
- "Find the light" behavior: Moving toward light source (DJ booth, bar glow) to be visible.
- Group squeeze: More people = more body contact. Strangers pressed together. Shoulders at different heights.

**Photo Content Distribution:**
- Group selfie: Everyone wants face visibility. Smaller people move to front. Tall people spread out or bend.
- The "one person checking photo" moment: After photo, one person grabs phone to check it. Other people reach over/around to see.
- "Delete and retake" reaction: Visible disappointment or excitement.

**Nightlife Group Behavior:**
- Cheers gesture: Glasses raised together. One person's glass slightly higher than others.
- Hugs: In crowded club, hugs are abbreviated (arms over shoulder, not full embrace).
- Dancing: Groups form circles, each person takes turn in center.

**Vocabulary:**
- "flash burst against dark background"
- "phone held high above crowd"
- "arm raised for visibility in club"
- "cheers glass height hierarchy"

---

### 5.3 Photobooth Behavior

**Photobooth Types:**

**Street Photobooth (JP/KR/HK):**
- 4 frames, strips printed
- 10-30 second intervals between frames
- Some booths have props (JP style: glasses, signs)
- Limited space forces subjects close

**Photobooth Behavior:**
- Frame 1: Group settles in, awkward, smile is forced
- Frame 2: Relaxed, real smile emerging
- Frame 3: Peak expression — most natural OR most exaggerated
- Frame 4: Wind-down OR most natural

**Body Packing:**
- In 4-person booth, bodies overlap
- Knees against seat edge
- Arms in laps or on shoulders
- Small space = forced physical contact

**Expression Timing:**
- You see the countdown (LED numbers)
- Must hold expression through flash (1-2 second flash)
- "Mouth slightly open" during flash = caught mid-word

**Physical Pressure:**
- Shoulders pressed by each other
- Head overlaps (one head in front of another)
- Feet visible at bottom of frame
- Hands may be out of frame

**Vocabulary:**
- "photobooth forced smile — Frame 1"
- "head overlap in small booth space"
- "flash catch mid-word — mouth open"
- "props held too close — face partially blocked"

---

### 5.4 Overlapping Body Language

**The "Overlap" in Group Shots:**
- When subjects are close, body parts cross in front of each other
- Forearm crossing torso (adjacent subject)
- Hair overlapping face (friend behind)
- Hand on hip of adjacent person
- Shopping bags overlapping legs

**The "Blur Hierarchy":**
- Subjects in front = sharpest
- Subjects behind = progressively blurrier
- The "blur" indicates who is primary vs secondary in the frame

**Layered Depth in Groups:**
- Back row heads visible above front row shoulders
- Arm at shoulder height appears to float above head behind
- Legs of standing people visible through gaps in seated row

**Proxemics in Groups:**
- Intimate distance (0-45cm): Close friends, couples
- Personal distance (45-120cm): Friends, acquaintances
- Social distance (120-360cm): Formal groups, strangers
- Most HK/JP/KR female friend groups photograph at intimate to personal distance

**Vocabulary:**
- "forearm crossing torso overlap"
- "back row heads above front row shoulders"
- "intimate distance shoulder press"
- "layered depth blur hierarchy"

---

### 5.5 Interrupted Attention

**The "Caught Looking" Moment:**
- Subject is looking at something off-camera (a person, a menu, a scene)
- Camera catches her looking AWAY from camera at the decisive moment
- This creates: "She didn't know I was taking this" = authentic

**The "Interrupted Conversation":**
- She was talking to someone off-camera
- Camera catches her mid-sentence — mouth open, eyebrows raised, hands gesturing
- Expression is engaged but not performing for camera

**The "Phone Notification" Moment:**
- She was looking at phone
- Something (notification, vibration) catches her attention
- Head lifts, eyes look up from phone
- The moment of lifting gaze is the photo moment

**The "Someone Called Her Name" Moment:**
- She turns toward the voice (blurry off-frame person calling)
- Head + torso + gaze all rotate toward voice
- Camera catches the moment of turning — not settled

**The "Distraction to Focus" Shift:**
- She was distracted (looking away, on phone, talking)
- She notices camera
- Her expression shifts from distant to present
- The transition expression is the most authentic

**Vocabulary:**
- "caught looking — gaze fixed off-camera"
- "mid-conversation — open mouth gesture"
- "phone notification lift — gaze rising"
- "someone called her name — turn toward voice"

---

### 5.6 Accidental Background Interactions

**The "Background Character" Effect:**
- Subject is in background of someone else's photo
- She doesn't know she's being photographed
- Most authentic expressions (genuine curiosity, boredom, distraction)
- She's not in focus (depth blur separates her)
- Slightly off-center composition (she's incidental)

**The "Walking Through Someone's Shot" Moment:**
- She walks through the frame of someone taking a photo
- Her expression: mild surprise, "sorry," or amused
- She continues walking — the photo captures the transit moment

**The "Witnessing Something Funny" Background:**
- She sees something off-camera that she finds funny
- She laughs but is unaware she's visible to camera
- This is the most prized candid moment

**The "Noticing the Camera After" Moment:**
- She realizes someone's photographing the scene
- Her expression changes — from unaware to slightly aware
- The half-aware expression is the sweet spot

**Environmental Overlap:**
- Her body partially overlaps with a street sign, poster, or object behind her
- Creates intentional framing (she's in focus, object is slightly blurred in front)
- Or she overlaps with object that's part of the scene

**Vocabulary:**
- "background blur — unaware subject"
- "walking through frame — transit moment"
- "witnessing something funny — real laugh"
- "environmental body overlap — depth composition"

---

## SECTION 6: V6 UPGRADE MODULES & ANTI-AI MOVEMENT MARKERS

### 6.1 Recommended V6 Engine Modules

**MODULE-13: SMARTPHONE_ARTIFACT_INJECTION_SYSTEM**
What: Injects specific smartphone camera artifacts (HDR failures, portrait mode halos, rolling shutter tilt, night mode ghosting, compression blocks) into images to break AI-polish.
Trigger: All shots, minimum 1 artifact per 3-shot sequence.
Implementation: ARTIFACT_TYPE + LOCATION + MAGNITUDE. e.g., PORTRAIT_MODE_HALO + shoulder_perimeter + subtle_2px.

**MODULE-14: MOTION_LAG_SEQUENCE_SYSTEM**
What: Specifies fabric inertia and hair lag physics for movement shots. Creates before/after relationship between body position and fabric/hair position.
Trigger: All movement shots (dancing, walking, turning).
Implementation: BODY_MOVEMENT + FABRIC_TYPE + LAG_FRAMES + DIRECTION. e.g., SNAP_TURN_RIGHT + LOOSE_DRESS + 3_frames + DRESS_ROTATES_LEFT.

**MODULE-15: TEMPORAL_DEGRADATION_SYSTEM**
What: Applies time-based appearance changes: makeup wear, humidity damage, fatigue progression, nightlife sequence.
Trigger: Any multi-shot sequence that implies time passing (pre/post event, commute, night out).
Implementation: TIME_POINT + DEGRADATION_TYPE + VISIBLE_EFFECTS. e.g., 3_HOURS_IN + MAKEUP_SETTLED + T_ZONE_OIL + LIP_COLOR_FADED.

**MODULE-16: HAND_OBJECT_INTERACTION_SYSTEM**
What: Specifies realistic hand grip mechanics and fidget behaviors for all held objects (phone, cup, bag, sleeve, hair).
Trigger: All shots where subject holds something or hands are visible.
Implementation: HAND_TYPE + OBJECT + GRIP_STYLE + FIDGET_PATTERN. e.g., RIGHT_HAND + WINE_GLASS + PALM_BOWL + FIDGET_TWIRL.

**MODULE-17: GROUP_SOCIAL_LAYER_SYSTEM**
What: Adds second-person and third-person social context to group shots: overlapping bodies, attention hierarchy, decoy subjects.
Trigger: All shots with implied social group.
Implementation: GROUP_SIZE + BODY_OVERLAP + ATTENTION_TARGET + STATUS_HIERARCHY. e.g., 3_PERSON + FOREARMS_CROSSED + CAMERA + CENTER_IS_PRIMARY.

**MODULE-18: INTERRUPTED_ATTENTION_CAPTURE_SYSTEM**
What: Specifies the moment of interrupted attention for candids: caught-looking, phone-lift, name-called, distraction-to-focus.
Trigger: All candid shots.
Implementation: INTERRUPTION_TYPE + EXPRESSION_PHASE + TIME_POSITION. e.g., PHONE_NOTIFICATION + LIFTING_GAZE + EARLY_TRANSITION.

**MODULE-19: DIGITAL_ZOOM_DEGRADATION_SYSTEM**
What: Applies digital zoom quality collapse (texture smear, aliasing, watercolor effect) when zoom level exceeds optical limit.
Trigger: Any shot claiming >3x zoom on smartphone.
Implementation: ZOOM_LEVEL + DEGRADATION_TYPE + SUBJECT_IMPACT. e.g., 8X_DIGITAL + SKIN_TEXTURE_COLLAPSE + PORES_SMEARED.

**MODULE-20: TACTILE_DEGRADATION_SYSTEM**
What: Applies physical wear to objects over time: shoe scuffs, glass lip prints, phone screen fingerprints, bag strap marks, deodorant friction marks.
Trigger: Any shot where subject has been wearing/using item for 2+ hours.
Implementation: ITEM + WEAR_TYPE + LOCATION + SEVERITY. e.g., STILETTO + SOLE_SCRUFF + HEEL_TIP + LIGHT.

---

### 6.2 Anti-AI Movement Markers (Quick Reference)

**Movement + AI Detection:**

| Human Behavior | AI Tendency | Anti-AI Marker |
|---|---|---|
| Hair lags body | Hair = body (no inertia) | Hair position ≠ head position |
| Fabric follows with delay | Fabric = body (no physics) | Hem rotation after hip stopped |
| Weight on one leg | Perfect bilateral balance | Hip tilt, shoulder drop |
| Slight rolling shutter tilt | Sharp everywhere | 1-3 degree body tilt |
| Fingerprints on glass | Pristine glass | Smudge at grip point |
| Bag swing after stop | Bag stops with body | Bag pendulum at hip |
| Motion blur on limbs | Everything sharp | Limb ghosting |
| Uneven blink timing | Perfect bilateral symmetry | One eye slightly more closed |
| Asymmetric grip | Bilateral symmetry | Thumb position ≠ index finger |
| Seatbelt wrinkle | No wrinkle | Wrinkle at waistband |
| Shoe scuff | Pristine shoe | Dark mark at toe box |

---

### 6.3 Top 5 Highest-Value V6 Upgrades

1. **SMARTPHONE_ARTIFACT_INJECTION** — injects iPhone HDR halos, portrait mode depth failures, rolling shutter tilt. The single fastest way to make images feel like real smartphone photos. 1 artifact per 3 shots.

2. **HAND_OBJECT_INTERACTION** — realistic phone/cup/bag grip mechanics. Hands are the hardest thing to render and most AI images get hand-object interaction wrong. Specifying grip creates immediate realism.

3. **TEMPORAL_DEGRADATION** — time-based makeup/oil/humidity/fatigue changes. Makes sequences feel like real time passing, not staged same-moment shots. Essential for multi-shot storylines.

4. **MOTION_LAG_SEQUENCE** — fabric inertia and hair lag physics. AI renders hair and fabric as attached to body with no inertia. Any movement shot needs 1-3 frame lag on hair/fabric.

5. **INTERRUPTED_ATTENTION_CAPTURE** — the "caught looking" / "phone-lift gaze" moment. The single most believable candid expression mechanism. Every candid should have an interruption type specified.

---

*V6 Research Report Complete*
*Research Agent: lucy/hermes | Date: 2026-05-13*
*Total sections: 6 | Modules recommended: 8 | Movement markers catalogued: 10+*
