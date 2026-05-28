# V15 RESEARCH: SOCIAL CAMERA + BAD PHOTO REALISM

**RESEARCH DATE:** May 28, 2026  
**ENGINE VERSION:** V15  
**STATUS:** COMPLETE — ALL DELIVERABLES IMPLEMENTED + HK EXTENSION

---

# AREA 01: SOCIAL CAMERA

## The Human Operator Problem

When a real person holds the camera instead of a tripod or remote trigger, the resulting photograph carries fingerprints of human consciousness, human error, and human relationship. The subject is not just "posing" — they are interacting with a photographer who has intentions, preferences, affection, awkwardness, or indifference. This relational dynamic creates image characteristics that no automated system currently replicates.

The social camera system models the photographer not as a neutral capture device but as an active agent whose behavior, relationship to subject, and technical skill level fundamentally alter the output.

---

## CAMERA_OPERATOR_LIBRARY_V2

### Operator Type Definitions

#### OP_01: THE INTIMATE PARTNER (Boyfriend / Girlfriend / Close Partner)

**Relationship Dynamic:** High emotional investment, physical comfort, often in private or semi-private settings. The photographer knows the subject's "good angles" from memory. They have likely taken hundreds of photos of this person over time. The subject trusts the photographer implicitly.

**Behavioral Signature:**
- Shoots from slightly below or at eye level — the classic "downward angle of affection" where the subject appears slightly elevated and adored
- Rapid fire bursts because they know the subject's expressions and can time the shot to a genuine moment
- Tends to let subject move freely rather than directing heavily — captures rather than constructs
- Often includes full body or environmental context because intimacy breeds comfort with space
- Subject frequently mid-laugh or genuine expression rather than posed smile
- Rarely asks subject to "smile" — the photographer waits for it naturally

**Technical Habits:**
- Uses portrait mode aggressively, sometimes incorrectly — blur bleeding onto a shoulder or ear
- Zooms to approx 1.5x-2x on smartphone (the "beauty zoom") — never full wide
- Front-facing camera common for "mirror selfies together" when both in frame
- Flash almost never used — relies on available light, accepts grain

**Image Failures Specific to This Operator:**
- Accidental partial face cut when subject moves unexpectedly
- Ghosting in low light from slow shutter
- Subject eye-blink caught mid-motion
- Phone handling shake in low light (often artistic)

**Example Prompt Grammar:**
> Shot by intimate partner using smartphone front camera at arm's length, boyfriend's perspective, subject mid-laugh with head tilted slightly back, warm afternoon window light on face, imperfect soft bokeh on shoulder, slight motion blur on hair from natural movement, unposed genuine moment not staged, social photography authenticity, analog-inspired warm tones, casual intimate document not professional

---

#### OP_02: THE GIRLFRIEND AMATEUR (Female Friend with Smartphone Experience)

**Relationship Dynamic:** The female friend who "takes good photos" — she has likely practiced on herself and others. She understands framing, lighting, and angle in a way that is more conscious than the average male photographer. She is comfortable directing the subject.

**Behavioral Signature:**
- Directs the subject actively: "turn a little," "chin down," "look at me"
- Has a mental library of "good poses" she has seen or used before
- Shoots from slightly above (high angle) more often than below — flattering downward geometry
- Uses the rear camera more than front, demonstrating comfort with the device
- Will reposition herself multiple times until she finds the right angle — patient
- Often includes environment intentionally as aesthetic backdrop

**Technical Habits:**
- Uses portrait mode correctly — clean edge detection on well-dressed subject
- More likely to use grid lines (rule of thirds) consciously
- May adjust exposure compensation manually
- Uses natural light more than artificial, often positions subject near windows
- Cleans the lens before shooting (wipes fingerprint grease — this matters)

**Image Failures Specific to This Operator:**
- Over-processing: too much brightness, oversaturated sky, skin smoothed beyond reality
- Over-cropped: face too large in frame, no breathing room
- Occasionally cuts off tops of heads or hair in pursuit of "face filling frame"
- Clean but sterile — technically correct yet emotionally empty

**Example Prompt Grammar:**
> Shot by female friend photographer with smartphone, above-angle slightly, subject directed to tilt chin, natural window light side-warm, portrait mode clean bokeh, rule-of-thirds composition with face at right intersection, slight smile not grin, intentional environmental background included, social photography framing, clean sharp capture with warm tone, Instagram-worthy composed shot not candid

---

#### OP_03: THE BOYFRIEND CLUELESS (Male Partner with Low Camera Skill)

**Relationship Dynamic:** Takes photos because asked, not because interested in photography. Views camera as a tool to complete a task. Minimal emotional investment in composition. May be distracted, tired, or rushing.

**Behavioral Signature:**
- Takes few shots — does not iterate, does not review
- Always shoots at full wide angle (no zoom) — "get everything in"
- Holds phone at face height regardless of subject height
- Does not communicate direction — subject is left to self-direct
- Shows subject the screen rarely
- Standoffish body language — snaps photo and walks away

**Technical Habits:**
- No portrait mode — wide open everything is in focus
- No flash consideration — auto mode only
- Vertical orientation default
- Possibly smudged lens from pocket carry
- Low light results in severe motion blur or underexposure

**Image Failures Specific to This Operator:**
- Subject appears tiny in vast empty space (full wide captures too much environment)
- Random person walking through background uncropped
- Severe motion blur — photographer moved before subject was ready
- Subject looks awkward because no direction was given — caught mid-blink or weird expression
- Horizontal horizon tilt — nothing aligned

**Example Prompt Grammar:**
> Shot by uninterested boyfriend using full wide smartphone lens, no zoom, camera held at face height parallel to subject, vertical format, no direction given to subject, auto exposure no flash, harsh overhead or backlit situation, messy uncropped background with unrelated elements, subject caught mid-unpose with awkward expression, unintentional motion blur from hasty capture, snapshot documentation not aesthetic creation, raw unpolished result

---

#### OP_04: THE TOURIST STRANGER (Bystander Asked to Photograph)

**Relationship Dynamic:** Complete stranger who has no relationship investment. They will take the photo as a transactional favor. They have no idea what the subject looks like "good." They will shoot quickly and hand back the phone. The subject is acutely aware of being photographed by a stranger — self-consciousness is at maximum.

**Behavioral Signature:**
- Subject is hyper-aware of being captured — stiffens, over-smiles, or goes blank
- Photographer does not know to wait for natural moment — may count down from three loudly
- Usually uses full wide and holds phone at face level
- May not understand portrait orientation vs landscape — randomness ensues
- Will take one photo, rarely offers to take more unless prompted

**Technical Habits:**
- Full wide lens, auto mode, no flash consideration
- Holds phone with both hands but not steadily — slight wobble
- May accidentally switch to front camera during the fumble
- Never uses portrait mode — doesn't know it exists or doesn't know how

**Image Failures Specific to This Operator:**
- Subject frozen in overposed stance — "say cheese" mentality
- Face completely frontal, arms at sides — most unnatural body arrangement
- Forehead chopped off or face cut in half by frame edge
- Background chaos — stranger had no compositional intent
- Extreme wide angle distortion — subject's face looks wrong due to proximity

**Example Prompt Grammar:**
> Shot by random stranger tourist asked to photograph, full wide smartphone lens held at face height parallel to subject, subject stiff overposed with arms at sides and forced smile, stranger counting down 1-2-3 before capture, no photographer-subject relationship, no direction or comfort, frontal face-on pose most unnatural, uncropped chaotic background, possible camera tilt horizon error, tourist snapshot aesthetic, subject self-conscious and unrelaxed, inauthentic staged moment appearance, disposable film camera approximation not professional portrait

---

#### OP_05: THE STREET DOCUMENTARY PHOTOGRAPHER (Stranger with Intentional Eye)

**Relationship Dynamic:** Someone with photographic awareness who is documenting a scene, not specifically directing a subject. The "subject" may be unaware they are being captured, or aware but not interacting with the photographer. This creates candor that staged photography cannot achieve.

**Behavioral Signature:**
- Photographer is separate from subject — observer, not participant
- Long lens or cropped framing — distance maintained
- Does not interact with subject — does not direct, does not engage
- Shooting quickly — may fire burst and leave
- Subject is in natural behavior — walking, laughing with others, looking away

**Technical Habits:**
- May use rear camera with significant zoom (2x-5x)
- Often shoots in burst — selects best frame later
- May use portrait mode on unaware subject (edge detection fails when no one is posing)
- Tends toward natural light, available ambient

**Image Failures Specific to This Operator:**
- Subject eye-line diverted — looking away or partially away
- Motion blur from long lens on moving subject
- Face partially turned — only one eye visible, cheek shadow on far side
- Strangers in background overlapping subject unintentionally
- Image cropped tight enough to feel intrusive

**Example Prompt Grammar:**
> Shot by documentary photographer maintaining distance, smartphone telephoto lens 2-3x zoom, subject unaware or partially aware of capture, candid natural behavior not directed, subject mid-stride or mid-conversation with others, single eye visible face angle, soft natural available light, environmental context included, unposed moment stolen not given, street photography aesthetic with authentic human activity, subject not performing for camera, 85mm equivalent compression and background separation, raw journalistic quality not composed portrait

---

#### OP_06: THE SELFIE SPECIALIST (Subject Holds Own Camera)

**Relationship Dynamic:** The subject operates the camera themselves. No photographer-subject relationship exists — the subject is simultaneously both. This creates self-awareness that produces specific image characteristics: the over-examined angle, the controlled expression, the calculated framing.

**Behavioral Signature:**
- Front camera default — subject sees themselves constantly
- Arm extended fully or held by selfie stick — creates specific distance geometry
- Subject's "good side" is maximally exploited — face always angled toward brighter side
- No third-party perspective — only the subject's chosen self-representation
- Often multiple attempts — subject reviews and deletes until satisfied

**Technical Habits:**
- Front camera with beauty mode potentially enabled
- Arms extended at fixed length — consistent distance relationship
- Selfie stick adds ~50cm effective reach — face is smaller in frame
- Timer mode used for group shots where subject joins
- Portrait mode on front camera sometimes fails — edge detection on self-facing is difficult

**Image Failures Specific to This Operator:**
- Beauty mode too aggressive — skin texture removed, features smoothed unreal
- Face fills frame completely — no context, no environmental presence
- Both arms visible holding phone — elbows flare wide — posture awkward
- Expression is examined and controlled — frozen smile, no micro-expression
- Eye contact directly with lens is uncanny — staring contest with viewer

**Example Prompt Grammar:**
> Front-facing smartphone selfie held at arm's length, subject controls camera themselves, beauty mode potentially active smoothing skin texture, both arms visible holding phone sides, eyes locked directly with front camera lens at close proximity, expression controlled examined not genuine, face dominant in frame no environmental context, arm extension geometry visible, subject's "good side" maximally exploited, overpolished digital perfection not authentic human moment, mirrored self-documentation aesthetic, sterile self-presentation not intimate document, sharp front camera capture with slight selfie distortion

---

#### OP_07: THE CREATIVE COLLABORATOR (Two Friends Co-Directing)

**Relationship Dynamic:** The photographer and subject are comfortable enough to co-create. The subject offers poses, the photographer suggests adjustments. There is a shared aesthetic vision. The photographer may be shooting film or using more deliberate equipment. This is an active collaboration, not a passive capture.

**Behavioral Signature:**
- Back and forth direction — "do that thing with your hands"
- Photographer shows subject the screen — subject reacts — photographer adjusts
- Subject may hold pose for multiple shots — iteration on same setup
- Environmental scouting — photographer and subject together find the light/location
- Mood is collaborative — laughter between shots, genuine warmth

**Technical Habits:**
- May use rear camera with portrait mode actively
- May use grid lines or level tool
- Deliberate about light — may turn subject or wait for cloud cover
- Will take multiple exposures — bracketing or burst — then choose
- Sometimes uses flash fill in harsh light

**Image Failures Specific to This Operator:**
- Too many options — subject has pose fatigue from too many iterations
- Overdirected — subject appears stiff from instruction overload
- Overcomposed — background is so carefully chosen it looks staged even if natural
- Film photography delays — subject blinks or moves during exposure
- Flash sync issues — fill flash creates double exposure ghosting in low light

**Example Prompt Grammar:**
> Shot by collaborative friend photographer with subject actively co-directing poses, mutual aesthetic direction shared between photographer and subject, multiple exposures taken of same setup, photographer showing screen and subject responding, natural light scouted and deliberate, portrait mode intentional bokeh, subject mid-collaboration warmth with pose fatigue, slightly overdirected but authentic creative process, environmental context composed but not sterile, body position intentional hand gesture, genuine laughter between shots not posed fake smile, analog-inspired warm grain, creative social photography collaboration not passive document

---

#### OP_08: THE UNDERCOVER SHOT (Photographer Hiding Camera)

**Relationship Dynamic:** The photographer is attempting to capture a subject who does not know they are being photographed. This may be for comedic effect, memory preservation, or documentary purpose. The subject's unawareness produces natural behavior unavailable in posed photography.

**Behavioral Signature:**
- Photographer suppresses all tells — no eye contact, no verbal announcement
- Phone held low — near hip or胸口, not at face
- Subject continues natural behavior unaware of capture
- Photographer may be part of a group that includes subject — the subject trusts the environment
- Quick trigger — capture and conceal

**Technical Habits:**
- Phone upside down or screen-off held in palm
- Front camera sometimes used for concealment (screen faces palm, subject in view)
- Silent shutter mode enabled
- No flash ever
- Burst mode — fire multiple shots without sound

**Image Failures Specific to This Operator:**
- Extreme down angle or up angle — unusual non-standard framing
- Subject partially cropped — photographer concealing position limits aiming precision
- Motion blur from low light and unsteady grip
- Blurry from missed focus — camera didn't know where to autofocus
- Audio recording artifact — physical press of button creates device movement

**Example Prompt Grammar:**
> Shot by concealing photographer hiding camera device, phone held low at hip or chest height with screen dark, subject completely unaware of capture, front camera used upside down concealment method, extreme unusual angle not standard portrait framing, subject mid-natural-behavior with genuine expression, no photographer-subject relationship active, subject isolated from environment without compositional awareness, possible severe motion blur from device movement during capture, extreme low light possible with no flash, accidental art documentary aesthetic, voyeuristic genuine moment not performed, analog-style grain and imperfect framing, covert capture film photography approximation not posed portrait

---

#### OP_09: THE DISTANT RELATIVE (Grandparent / Elder with Basic Phone)

**Relationship Dynamic:** Someone with minimal smartphone photography skill but maximum emotional investment. They take photos out of love and are proud to have "learned" to use the phone camera. They may have difficulty with timing, focus, or framing but the love is palpable. These images often have charming errors born from enthusiasm over skill.

**Behavioral Signature:**
- Holds phone at full arm's length for "safety" — far from subject
- Says "say cheese" or "smile" — old photography conditioning
- Takes many photos because they aren't sure they got it
- May have dirty or cracked camera lens — doesn't affect their joy
- Not sure how to review — may not know photos saved correctly

**Technical Habits:**
- Full wide angle always — no zoom concept
- Flash on auto if room darkens
- Vertical orientation almost always
- May hold phone horizontally for landscape — gets confused
- Uses camera button (physical or on-screen) — no gesture control

**Image Failures Specific to This Operator:**
- Subject extremely small in frame — massive distance creates tiny figure
- Subject blinking — elder delays shutter press after subject prepared
- Extreme horizon tilt — elder doesn't understand phone orientation
- Flash washout — subject face completely white from flash in low interior
- Subject not centered — elder frames based on old point-and-shoot muscle memory
- Cracked lens artifact — light flares in one direction on every photo

**Example Prompt Grammar:**
> Shot by elderly relative with basic smartphone at full arm extension, photographer calling out "say cheese" before capture, extreme distance between camera and subject creating small figure in vast empty frame, vertical format default, possible flash washout interior with subject face blown white, horizon tilt present severe, subject blinking caught from delayed shutter response, no zoom used full wide, dirty or cracked lens light flare artifact, warmth and love in imperfect capture despite technical failures, nostalgic family document, genuine elder photography behavior with charming errors, film photography grain approximation, unconditional love documented not aesthetic success

---

#### OP_10: THE PROFESSIONAL HIRE (Event Photographer or Paid Shoot)

**Relationship Dynamic:** A skilled photographer is being paid or asked to produce specific results. This creates performance pressure on the photographer and staged energy from the subject. The photographer has technical skill but lacks the intimate relationship knowledge that creates authentic captures. The subject may feel awkward being professionally photographed.

**Behavioral Signature:**
- Photographer directs everything — lighting, pose, expression, background
- Subject waits for instruction — passive recipient of direction
- Technical perfection is the goal — no expense for iteration
- Fast shooting pace — time is money
- Photographer may use DSLR or mirrorless rather than smartphone

**Technical Habits:**
- Uses professional lighting equipment — soft boxes, reflectors, gels
- Shoots in RAW format for post-processing flexibility
- Has backup equipment — multiple cameras, multiple lenses
- Uses burst to select from multiple expressions
- Poses subject fully before each shot

**Image Failures Specific to This Operator:**
- Perfect technical quality but emotionally dead — no authenticity
- Subject appears stiff from excessive direction — no natural moment
- Overretouched skin — professional post-production removes all texture
- Corporate or wedding aesthetic — overcomposed and overposed
- Background too clean — fake bokeh or heavy post-processing visible
- No relationship captured — just expensive equipment documenting strangers

**Example Prompt Grammar:**
> Shot by professional photographer hired for event, heavy direction given to subject pose and expression, subject waiting passively for instruction, professional lighting setup with softboxes and reflectors, RAW capture with professional post-processing, perfect technical quality with overretouched skin removing natural texture, clean sterile background with heavy artificial bokeh, no authentic moment captured, overposed subject with no photographer-subject relationship, expensive equipment used without emotional investment, wedding corporate photography aesthetic, technically proficient but emotionally void, overly polished digital perfection not genuine memory, sharp professional sensor quality with no soul

---

#### OP_11: THE DRUNK NIGHT PHOTOGRAPHER (Impaired Memory Capture)

**Relationship Dynamic:** Someone photographing in a state of impaired judgment — alcohol, celebration, exhaustion. The photographer's motor control is compromised. The subject may also be impaired. Flash photography in dark bars is common. The resulting images are chaotic, blurry, and often treasured as authentic memories of specific moments.

**Behavioral Signature:**
- Holds phone at unpredictable angles — sometimes vertical, sometimes horizontal
- Shouts instructions that don't make sense — "everybody smile — wait not yet — okay NOW"
- May take 50 photos in succession trying to "get one"
- Flash fires in dark environment — washed out subjects
- Background is dark bar with colored lights

**Technical Habits:**
- Flash on compulsively — auto or forced
- High ISO — phone compensates with grain
- Shutter speed too slow for unsteady hands
- Front camera used in dark interior (screen as light source)
- No review — photographer can't tell what they got

**Image Failures Specific to This Operator:**
- Severe motion blur from alcoholic hand shake
- Flash washout with red-eye from dark environment
- Subject squinting against flash — eyes barely visible
- Camera shake rotation — phone rotating during exposure
- Complete blur — out of focus from unsteady targeting
- Frame includes random bar patrons not meant to be in shot
- Multiple people in frame partially cropped — everyone grabbed in chaos

**Example Prompt Grammar:**
> Shot by drunk photographer at bar or party with severe motor impairment, phone held at unpredictable angle both vertical and horizontal mixed in sequence, forced flash firing in dark interior causing subject face washout and red-eye, shutter speed too slow for unsteady shaking hand creating motion blur rotation, high ISO grain throughout, subject squinting against flash with eyes barely visible, random bar patrons in background uncropped, chaotic shouting of "smile" before uneven delayed capture, 50 exposures taken in succession with no review, warm bar ambient light mixed with harsh flash creating color contamination, authentic chaotic celebration memory not aesthetic success, heavy grain and motion artifacts, treasured genuine impaired moment documented not composed, analog film grain simulation with severe technical failure

---

#### OP_12: THE LONG DISTANCE RELATIONSHIP PHOTOGRAPHER (Remote Partner)

**Relationship Dynamic:** The photographer captures images specifically to send to a partner they cannot see in person. The photography is an act of love and connection. The subject may dress up or do their hair for these photos. The camera becomes a proxy for physical presence. There is longing embedded in the composition.

**Behavioral Signature:**
- Subject may be dressed up intentionally — this is an "occasion" photograph
- More considered composition — the subject knows this will be scrutinized closely
- May use front camera in bedroom or mirror — intimate private setting
- Photographer (remote partner) has requested specific types of shots
- Double exposure or mirror photos common — "look I'm with you"

**Technical Habits:**
- Front camera in private space — bedroom, bathroom, mirror
- Self-timer used for full body shots
- May photograph outfit before going out — cataloging for partner
- Soft bedroom lighting — lamp or window, intimate warmth
- Smartphone held by hand or propped on books

**Image Failures Specific to This Operator:**
- Intimate setting creates specific awkward angles — bathroom mirror reflections
- Front camera held high creating chin-up perspective
- Bedroom context — unmade bed, personal items in frame
- Outfit photo feeling — subject modeling rather than being
- Mirror reflection captures phone in frame — breaks immersion
- Dual perspective — half face phone shadow visible in mirror shot

**Example Prompt Grammar:**
> Shot by remote partner using front camera in intimate private space bedroom or bathroom, subject dressed intentionally for partner viewing, mirror reflection used creating phone visible in frame, self-timer full body shot in intimate setting with bedroom context visible, soft warm lamp lighting creating cozy atmosphere, long-distance longing aesthetic embedded in composition, chin-up hold angle, subject modeling outfit for partner cataloging, phone shadow partially covering face in mirror capture, unpracticed bed visible in background, authentic longing document not composed aesthetic, imperfect intimate transfer moment, warm color temperature with soft focus, genuine relationship presence through technological proxy, unpolished private documentation not professional

---

#### OP_13: THE MTR PLATFORM COMMUTER (Hong Kong Transit Photographer)

**Relationship Dynamic:** Someone photographing on the MTR during commute — bored, passing time, or capturing the transit experience itself. The MTR is a liminal space where people are transitioning, waiting, or zoning out. Photography here captures human existence in transit.

**Behavioral Signature:**
- Waits for train arrival — captures motion blur of train entering station
- Photographs strangers sleeping or looking at phones
- Captures platform texture — tiles, signage, crowds
- Selfie with train as background common
- Long exposure of moving platform crowds
- Vertical format dominant — matching phone orientation

**Technical Habits:**
- Uses available platform light — fluorescent harsh
- Often shoots through glass partition reflections
- May use portrait mode on moving stranger (fails frequently)
- Zoom to 2x-3x to avoid being too close to subjects
- Night mode in stations produces surreal color

**Image Failures Specific to This Operator:**
- Platform fluorescent green-yellow color cast dominant
- Train motion blur — subject sharp but environment smeared
- Reflection of self or others in platform glass overlaying shot
- Stranger's face sharp when they turned suddenly — caught unaware
- Overhead MTR signage branding visible in frame — corporate intrusion
- Handrail or pole bisecting frame diagonally
- Crowd blur creating abstract people shapes
- Extreme contrast between bright platform and dark tunnel

**Example Prompt Grammar:**
> Shot by MTR platform commuter during transit, fluorescent platform lighting with harsh green-yellow color cast, motion blur of train entering or leaving station, reflection of photographer or others in platform glass partition overlaying frame, vertical format dominant, subjects mid-commute — sleeping, looking at phones, waiting with thousand-yard stare, signage and corporate branding visible in frame, handrails bisecting diagonal composition, strangers unaware of capture in public transit space, night mode surreal color processing, available fluorescent light with shadow, candid transit documentation not staged portrait, urban mobility aesthetic, Hong Kong MTR specific environment, authentic commute moment not composed

---

#### OP_14: THE LATE-NIGHT TAXI INTERIOR (Hong Kong Night-Time In-Car Photographer)

**Relationship Dynamic:** Someone in the backseat of a taxi documenting the night city passing by, or friends in a taxi capturing the moment of going somewhere together. The taxi is intimate space shared with strangers (the driver). The city's neon reflects through windows.

**Behavioral Signature:**
- Backseat selfie with friends — cramped three people in back
- Window shots of neon-lit streets passing — light streaks
- Driver's head and shoulders in peripheral frame
- Selfie stick used in confined space — hits ceiling
- Video documentation common — city lights streaming past
- Group in backseat excited going to or from venue

**Technical Habits:**
- Uses rear camera with flash blocked by own hand
- High ISO from dark interior
- Window glass adds reflection of interior over exterior
- May use burst to capture moment between neon pulses
- Front camera used for group backseat selfie
- Phone nearly touches window to avoid reflection

**Image Failures Specific to This Operator:**
- Interior visible over exterior — dashboard reflection with driver silhouette
- Neon color contamination — pink, blue, green reflecting on faces
- Extreme contrast — face in shadow against bright street lights
- Hand or arm of friend in front seated person visible
- Driver's eyes in rearview mirror catching light
- Rain on window if wet night — streaks and blur
- Extreme motion blur from vehicle movement while trying to shoot
- Taxi receipt or phone mount visible in frame corner
- Seatbelt cutting across chest of subject

**Example Prompt Grammar:**
> Shot by backseat taxi passenger in Hong Kong late night, neon-lit streets reflecting through window with pink blue green color contamination on faces, interior dashboard and driver silhouette visible over exterior city view, dark taxi interior with high ISO grain, rain on window possibly creating streaks, three friends cramped in backseat for group selfie, phone nearly touching window to minimize reflection, motion blur from vehicle speed while capturing, driver eyes catching light in rearview mirror, taxi receipt or phone mount visible at frame edge, red seatbelt strap crossing chest, extreme contrast between lit face and dark interior, authentic late-night taxi moment not composed, cramped intimate space with city passing, Hong Kong night neon aesthetic, genuine transit memory between venues

---

#### OP_15: THE ROOFTOP FRIEND PHOTOGRAPHER (Hong Kong High-Altitude Shot)

**Relationship Dynamic:** Friends climbing to a rooftop to capture the view or each other against the Hong Kong skyline. This is deliberate — they made an effort to get here. The photographer may be braver than the subject about edge safety. The skyline behind is the real subject.

**Behavioral Signature:**
- Subject at edge with skyline behind — dangerous composition
- Photographer shoots from further back, holding subject safe
- Sunset or night city light timing — golden hour chase
- Subject poses with arms spread or on railing
- Group shots with skyline — everyone cramped at edge
- Phone held high overhead for skyline above subject's head

**Technical Habits:**
- Uses rear camera with HDR for sky-city contrast
- May hold phone in one hand while leaning back for safety
- Vertical panorama mode for full skyline
- Portrait mode struggles with edge railing and city behind
- Night mode essential for dark skyline with lit subject
- Self-timer used if photographer wants to be in shot

**Image Failures Specific to This Operator:**
- Skyline over-exposed against dark subject silhouette
- Railing or safety fence obliterating bottom of frame — metal bars over legs
- Subject tiny against massive skyline — perspective confusion
- Distant buildings too small to register — meaningless background
- Wind-blown hair creating motion blur at crucial moment
- Camera tilt anxiety — photographer leaning back capturing while scared
- Safety-first composition where skyline can't be captured fully
- Other rooftop people photobombing distant background
- Glare from direct building light — tower beam in lens

**Example Prompt Grammar:**
> Shot by friend on Hong Kong rooftop with city skyline behind, subject at edge posing dangerously with railing or safety fence cutting through frame, skyline either over-exposed bright or under-exposed dark from extreme contrast, massive buildings behind subject appearing tiny and meaningless, wind-blown hair motion blur, phone held high overhead angled down creating unnatural perspective, portrait mode failing on metal railing edge detection, other rooftop people visible in distant background, tower light beam glare entering lens, golden hour or night city lights creating warm atmospheric haze, genuine high-altitude moment with safety concern, Hong Kong rooftop specific context, authentic urban adventuring not posed studio shot, sky dominance over subject

---

#### OP_16: THE CONVENIENCE STORE WALK-BACK (Hong Kong 7-Eleven/gsr Ritual Shot)

**Relationship Dynamic:** The 7-Eleven or gsr便利店 is a Hong Kong social hub. Friends meet here, fuel up before going out, and photograph the ritual of the stop. The fluorescent interior and processed snacks are the aesthetic. This is pre-night-out documentation.

**Behavioral Signature:**
- Subject holding snack or drink — Maxim's, ready-to-drink bubble tea
- Standing in front of refrigerator case — bright backlight
- GSR uniform or convenience store employee friend
- Group of three crammed into narrow aisle
- Selfie with friends in front of the extensive alcohol display
- Slurpee or hot dog held up as prop

**Technical Habits:**
- Uses fluorescent convenience store lighting — very cool blue-white
- Front camera dominant — subject wants to see themselves
- Beauty mode enabled — subject wants to look good for pre-drinking
- Flash fired in low light — washes out everything
- Shot taken quickly — staff may ask them to move

**Image Failures Specific to This Operator:**
- Harsh fluorescent green-white color cast dominant
- Refrigerator case light turning subject blue
- Subject holding bright processed snack creating color conflict
- Background refrigerator shelves visible creating visual noise
- Reflection of store interior and photographer in refrigerator glass
- Red price tags and promotion signs visible creating visual clutter
- Flash washout from store's bright overhead fluorescent
- Subject squeezed between shelves with no compositional space
- Store employee or customer walking past in background uncropped
- GSR logo visible in frame — specific Hong Kong convenience store marker

**Example Prompt Grammar:**
> Shot by convenience store visitor in Hong Kong 7-Eleven or gsr, fluorescent overhead lighting with harsh green-white color cast washing out skin tones, subject holding bubble tea or snack as prop in front of refrigerator case, refrigerator light backlighting creating silhouette against bright shelves, reflection of store interior and photographer in glass door behind subject, price tags and red promotion signs cluttering background, flash fired washing out entire scene, cramped aisle with no compositional space, other customers or employees visible uncropped, GSR logo or 7-Eleven branding visible in frame corner, beauty mode active smoothing skin beyond reality, authentic pre-night-out fuel stop documentation, Hong Kong convenience store ritual not aesthetic portrait, blue-white fluorescent atmosphere dominant, genuine gsr便利店 moment with processed snack aesthetic

---

#### OP_17: THE FERRY DECK FRIEND-ANGLE (Hong Kong Harbour Crossing Shot)

**Relationship Dynamic:** Someone on the Star Ferry or other harbour crossing capturing the view or friends on deck. The harbour is iconic — this is about place documentation as much as people. The photographer is part of tourist documentation even if they're local.

**Behavioral Signature:**
- Subject against Victoria Harbour background — Kowloon or Hong Kong Island
- Sunset timing — chasing golden hour on the water
- Group on deck with harbour behind — crowded ferry rail
- Video of passing Central waterfront
- Selfie stick extended over water — dangerous for phone
- Waves and salt air affecting equipment

**Technical Habits:**
- Uses rear camera with harbour in frame
- May use panorama for full waterfront
- Portrait mode on moving boat — depth map fails constantly
- HDR for bright sky and darker water contrast
- Self-timer if photographer wants to join group
- High shutter speed to freeze boat motion

**Image Failures Specific to This Operator:**
- Boat motion creating constant micro-movement blur
- Water spray or salt haze reducing clarity
- Subject sharp but harbour too bright or too dark from contrast
- Other passengers' heads visible above shoulder of subject
- Sunglasses creating black reflections in eyes
- Wind-blown hair with harbour smell
- Handrail cutting through composition
- Subject tiny against massive harbour — Kowloon W hotels too small
- Ferry announcement or ferry name visible in frame
- Moving boat causing slight rotation blur in background

**Example Prompt Grammar:**
> Shot by friend on Star Ferry or harbour crossing deck with Victoria Harbour background, Kowloon or Central waterfront visible behind subject, sunset golden hour timing with warm light on water, other ferry passengers visible above subject's shoulder, boat motion micro-movement creating slight blur, water spray or salt air haze reducing clarity, portrait mode failing from constant boat movement, subject tiny against massive harbour backdrop with iconic buildings too small, handrail cutting diagonal across frame, wind-blown hair from sea breeze, sunglasses reflecting black in eyes, ferry name or announcement visible in frame, authentic harbour crossing moment not composed, Hong Kong iconic transit experience, genuine maritime document with tourist documentation energy, warm golden hour light on moving boat deck

---

#### OP_18: THE INDOOR PLAYGROUND CROUCH (Hong Kong Kids' Birthday Photographer)

**Relationship Dynamic:** A parent or relative crouching down to capture children at play in indoor play centres (McDonald's ball pit, Fisherman's Market, theme park play areas). The photographer is low to the ground, struggling with angles, capturing kids mid-chaos.

**Behavioral Signature:**
- Extreme low angle — photographer crouching or kneeling
- Shooting upward at child's face against ceiling
- Burst mode — children don't hold still
- No flash — want to capture natural play
- Waiting for moment — child to notice camera
- Parent calling child's name to get attention

**Technical Habits:**
- Uses rear camera with portrait mode attempted
- Low angle catches ceiling lights creating flare
- High ISO from indoor play centre darkness
- Zoom to 1.5x-2x to avoid being too close to kids
- Burst to capture motion — 10-20 frames
- Cleans lens after from being low to ground

**Image Failures Specific to This Operator:**
- Ceiling lights creating lens flare above child's head — halo effect
- Face up-shot perspective distortion — chin too wide, forehead too big
- Other children running through background uncropped
- Ball pit balls or toys cluttering foreground
- Motion blur from active child
- Autofocus missing fast-moving child — locked on background
- Parent's shadow falling across child from low angle
- Hand or arm of other child in frame corner
- Overhead signage visible — McDonald's or play centre branding
- Grain from high ISO dark interior

**Example Prompt Grammar:**
> Shot by parent crouching extremely low in indoor playground or play centre, upward angle at child's face against ceiling with ceiling lights creating lens flare halo, perspective distortion making chin too wide and forehead extended, other children running through background uncropped, ball pit balls or toys cluttering foreground frame, burst mode active with child in constant motion creating motion blur, autofocus locked on background not moving child, high ISO grain from dark interior, McDonald's play place or Fisherman's Market signage visible above, parent's shadow falling across child from low angle, another child's hand or arm entering frame corner, authentic parental documentation of chaotic active play, genuine birthday party or play centre moment not composed, warm indoor lighting mixed with ceiling flare, Hong Kong indoor playground specific context

---

#### OP_19: THE WEDDING GUEST PHONE SHOOTER (Hong Kong Banquet Photographer)

**Relationship Dynamic:** A guest at a Chinese wedding banquet (筵席) using their phone to capture moments. They are not the professional photographer — they are capturing personal memories at a social event with cultural significance. They are standing during toasts, photographing the couple.

**Behavioral Signature:**
- Shooting over heads of other guests
- Capturing couple during cake cutting or toast
- Phone held high to see over table
- Group guest photos — other guests in frame
- Video of couple's first dance or door ceremony
- Photographing food — the banquet dishes are part of the documentation

**Technical Habits:**
- Uses rear camera with flash disabled — respects event
- High angle shooting over banquet tables
- Portrait mode on couple — attempts to isolate
- May use zoom to frame out other tables
- Burst for toast moment
- Auto white balance confused by mixed banquet lighting — spotlights and fluorescents

**Image Failures Specific to This Operator:**
- Other guests' heads cropping into frame from low angle
- Overhead spotlight creating hot spot on couple
- Flash not used but low light causes blur
- Other banquet tables visible in background — visual chaos
- Guest phone screen glow visible if they reviewed photo
- Long table distance making couple tiny
- Green-white fluorescent wash from ceiling
- Bride's dress overexposed from spotlight
- Red and gold decoration cluttering frame — Chinese wedding aesthetic overload
- Other guests' wine glasses or chopsticks visible
- Aunties and uncles dancing in background at later hour

**Example Prompt Grammar:**
> Shot by wedding guest using smartphone at Chinese banquet or 筵席, phone held high over other guests' heads to capture couple, overhead spotlight creating hot spot on bride's dress with rest dark, other banquet tables and guests visible in background creating visual chaos, red and gold Chinese wedding decoration cluttering frame, green-white fluorescent ceiling light mixing with warm spotlight, couple tiny in frame from long table distance, guests' wine glasses and chopsticks visible at edges, aunties and uncles visible dancing in background during later portion of event, flash disabled with low light causing motion blur, portrait mode failing from complex wedding lighting, authentic guest documentation not professional capture, genuine celebration of Chinese wedding with cultural specificity, social photography from limited guest position, warm chaotic authentic moment not composed

---

#### OP_20: THE AIRPORT DEPARTURE GATE (Hong Kong Travel Photographer)

**Relationship Dynamic:** Someone at Hong Kong International Airport (HKG) documenting the departure moment — alone or with friends about to travel. The airport is liminal space, the goodbye happens here. The photographer documents leaving.

**Behavioral Signature:**
- Subject with boarding gate visible in frame — departure hall context
- Selfie with luggage, passport, boarding pass as props
- Group shot with departing friends
- Capturing someone at security or immigration line
- Window shot of airplane or tarmac
- Exhausted traveler waiting for early morning flight

**Technical Habits:**
- Uses rear camera with departure hall signage in frame
- Portrait mode on lone traveler
- May use flash in dark departure lounge
- Zoom to exclude other passengers
- Early morning or late night timing common
- Timer mode for group at gate

**Image Failures Specific to This Operator:**
- Departure hall fluorescent lighting creating green color cast
- Other passengers' heads and luggage handles in frame
- Departure board or flight information visible — date and flight number
- Airline branding prominent — Cathay Pacific specific markers
- Reflection of traveler in departure hall glass partition
- Extreme tiredness visible on face — pre-dawn flight exhaustion
- Security or immigration queue visible behind subject
- Suitcase handle or wheel visible at bottom of frame
- Passport face visible creating privacy concern
- Boarding pass with personal information visible

**Example Prompt Grammar:**
> Shot by traveler or friend at Hong Kong International Airport HKG departure gate, fluorescent departure hall lighting with green color cast, other passengers and luggage handles visible in frame, departure board or flight information visible with date and flight number, Cathay Pacific or airline branding prominent, security or immigration queue visible behind subject, reflection of traveler in glass partition, suitcase handle or wheel entering frame bottom, passport or boarding pass with personal information partially visible, early morning or late night timing with pre-flight exhaustion visible on face, portrait mode isolating lone traveler against chaotic departure environment, authentic travel documentation not composed, Hong Kong international airport specific context, genuine farewell moment or travel excitement, liminal space photography with departure hall aesthetic

---

#### OP_21: THE BEACH FRIEND-BEHIND-WALKING (Hong Kong Beach Photographer)

**Relationship Dynamic:** Friends at a Hong Kong beach (Repulse Bay, Stanley, Cheung Sha) walking along the shore while one photographs from behind. The photographer captures the walking figure against sea and sky. This is casual beach documentation.

**Behavioral Signature:**
- Photographer behind subject — walking alongside or behind
- Subject walking away or three-quarter view
- Beach, sea, sky framing the walking figure
- Wet sand creating reflections
- Mid-day sun creating harsh shadows
- Friends calling subject to turn around

**Technical Habits:**
- Uses rear camera with sky as background
- May underexpose to keep sky blue
- Zoom to 2x-3x to frame subject at distance
- Portrait mode on walking figure
- Hates the direct sun — seeks shade or golden hour
- Silhouette or backlit shot common

**Image Failures Specific to This Operator:**
- Sky overexposed while subject is silhouette or vice versa
- Harsh mid-day sun creating deep shadows under subject's chin
- Subject's shadow leading toward camera creating odd geometry
- Beach umbrella or beach chair photobombing background
- Other beach-goers visible in distance
- Sand blowing onto lens from beach walk
- Water-wet sand reflecting sun blinding the camera
- Subject walking into bright sky with face in shadow
- Distant high-rise buildings behind beach — Hong Kong density visible
- Droplets of sea water on lens creating blur spots

**Example Prompt Grammar:**
> Shot by friend walking behind subject on Hong Kong beach at Repulse Bay or Stanley, subject three-quarter view walking with sea and sky as background, sky overexposed while subject is dark silhouette or face in shadow from harsh mid-day sun, beach umbrella or other beach-goers visible in distance, wet sand reflecting sun creating bright patches, water droplets on lens from sea spray, distant high-rise buildings visible behind beach indicating Hong Kong density, friend's shadow leading into frame, sea water droplets or sand on lens creating blur spots, portrait mode isolating walking figure against beach backdrop, authentic casual beach documentation not composed, Hong Kong beach specific context, genuine beach walk moment with sand and sea aesthetic, warm golden or harsh white beach lighting

---

#### OP_22: THE ESCALATOR FRIEND-ABOVE (Hong Kong Mid-Levels Escalator Photographer)

**Relationship Dynamic:** Someone standing above their friend on the moving escalator (Mid-Levels Escalator, SOGO escalators, or mall escalators) capturing them ascending or descending. The escalator is iconic Hong Kong — this is place documentation as much as people photography.

**Behavioral Signature:**
- Photographer on upper escalator shooting down at friend on lower escalator
- Or photographer on lower landing shooting up at friend ascending toward them
- Friend may not be looking at camera — watching the street
- Captures escalator movement — steps and structure
- Mid-levels SOHO street scene behind subject
- Rain cover or umbrella if wet day
- Tourist snapshot with escalator as destination

**Technical Habits:**
- Uses rear camera with zoom to 2x-3x
- Portrait mode on subject
- May have to wait for escalator to bring friend into frame
- Vertical format to capture full escalator span
- Backlight from street if shooting against sun

**Image Failures Specific to This Operator:**
- Escalator steps creating diagonal motion lines through frame
- Other escalator riders' heads visible above subject's shoulder
- Subject sharp but escalator structure too busy behind
- Backlit subject with bright sky or street behind — face dark
- Rain umbrella creating pattern over subject's head
- SOGO or mall signage visible in background — commercial clutter
- Escalator handrail bisecting frame diagonally
- Motion blur on escalator steps from movement
- Subject's expression caught mid-interaction with street view
- Hong Kong hillside or street scene visible behind escalator

**Example Prompt Grammar:**
> Shot by friend standing above on Hong Kong escalator (Mid-Levels, SOGO, or mall) photographing friend on lower escalator section, escalator steps and structure creating diagonal motion lines through frame, other escalator riders' heads visible above subject's shoulder, subject sharp but busy escalator structure behind, backlit with bright street or sky behind making face dark, rain umbrella or rain cover visible over subject, mall or SOHO signage cluttering background, escalator handrail bisecting diagonal, motion blur on escalator steps from continuous movement, subject's expression caught mid-observation of street scene below, Hong Kong hillside or urban street visible behind escalator, authentic escalator documentation not composed portrait, mid-levels SOHO specific context, genuine Hong Kong transit moment with escalator as social space, urban vertical mobility aesthetic

---

### Operator Priority Matrix

**Operational Definitions:**
- **Authenticity** = Degree of unposed/genuine capture vs. directed/posed (HIGHEST = fully candid, LOW = fully directed)
- **Technical Quality** = Camera skill level: focus accuracy, exposure control, composition intentionality (HIGHEST = professional, LOWEST = random/failed)
- **Relationship Warmth** = Emotional intimacy between photographer and subject (HIGHEST = decades-long bond, NONE = complete stranger, LOW = casual acquaintance)
- **Failures Frequency** = Likelihood of interesting "bad photo" artifacts (HIGHEST = almost guaranteed chaotic failures, LOW = clean and predictable)

|| Operator Type | Authenticity | Technical Quality | Relationship Warmth | Failures Frequency |
||--------------|--------------|-------------------|---------------------|--------------------|
|| OP_01 (Intimate Partner) | HIGH | MEDIUM | HIGH | MEDIUM |
|| OP_02 (Female Friend Amateur) | MEDIUM | HIGH | MEDIUM | LOW |
|| OP_03 (Boyfriend Clueless) | MEDIUM | LOW | LOW | HIGH |
|| OP_04 (Tourist Stranger) | LOW | LOW | LOW | HIGH |
|| OP_05 (Street Documentary) | HIGH | MEDIUM | NONE | MEDIUM |
|| OP_06 (Selfie Specialist) | LOW | MEDIUM | NONE | HIGH |
|| OP_07 (Creative Collaborator) | HIGH | HIGH | HIGH | LOW |
|| OP_08 (Undercover Shot) | HIGHEST | LOW | NONE | HIGH |
|| OP_09 (Elder Relative) | MEDIUM | LOW | HIGHEST | HIGH |
|| OP_10 (Professional) | LOW | HIGHEST | LOW | LOW |
|| OP_11 (Drunk Night) | HIGHEST | LOWEST | HIGH | HIGHEST |
|| OP_12 (Long Distance) | HIGH | MEDIUM | HIGHEST | MEDIUM |
|| OP_13 (MTR Platform Commuter) | HIGH | LOW | NONE | HIGH |
|| OP_14 (Late-Night Taxi) | HIGH | LOW | MEDIUM | HIGH |
|| OP_15 (Rooftop Friend) | HIGH | MEDIUM | HIGH | MEDIUM |
|| OP_16 (Convenience Store Walk-Back) | HIGH | LOW | HIGH | HIGH |
|| OP_17 (Ferry Deck Friend-Angle) | HIGH | MEDIUM | HIGH | MEDIUM |
|| OP_18 (Indoor Playground Crouch) | MEDIUM | LOW | HIGHEST | HIGH |
|| OP_19 (Wedding Guest Phone) | MEDIUM | LOW | MEDIUM | HIGH |
|| OP_20 (Airport Departure Gate) | MEDIUM | LOW | HIGH | MEDIUM |
|| OP_21 (Beach Friend-Behind-Walking) | HIGH | MEDIUM | HIGH | LOW |
|| OP_22 (Escalator Friend-Above) | HIGH | MEDIUM | MEDIUM | MEDIUM |

**Usage:** Use this matrix to select operators based on desired output profile. For maximum authenticity + interesting failures, choose OP_08 or OP_11. For clean, directed imagery, choose OP_07 or OP_10.

---

## SOCIAL DISTANCE TAXONOMY

Social distance determines how subjects orient themselves toward the camera and each other, producing specific photographic geometries that carry relationship information.

### SD_01: Intimate Distance (< 45cm / 18 inches)

**Physical Description:** The camera is within arm's reach of the subject. The subject can touch the lens or blow on it. This distance is reserved for lovers, children, and occasionally close family. The subject's face fills the frame completely.

**Behavioral Characteristic:** Subject does not "perform" for the camera — the camera is an extension of their space. They may look at the lens and talk to the person holding it simultaneously. Eye contact with camera is comfortable and routine. Subjects may touch the lens or hold the phone. Breathing is audible in video. The intimacy is physical, not performed.

**Image Characteristics:**
- Face dominates frame — no context
- Skin texture visible — pore detail
- Eyes large and direct — no averted gaze
- Slight wide-angle distortion at close range (nose appears larger than real)
- Possible lens contamination from subject breath or touch
- Depth of field extremely shallow at this distance even on full-frame cameras

**Example Prompt Grammar:**
> Intimate distance captured at less than 45cm from subject, face fills frame completely with no environmental context, subject breathing close enough to fog lens, eyes direct and comfortable with camera presence, skin texture visible with pore detail, slight wide-angle facial distortion from proximity, nose proportion slightly enlarged, subject not performing but existing naturally in camera space, physical intimacy documented not aesthetic framing, ultra-close smartphone lens with portrait mode struggling at close range, warm available light from adjacent proximity, authentic physical closeness not composed shot

---

### SD_02: Personal Distance (45cm - 120cm / 18-48 inches)

**Physical Description:** The camera is held at arm's length or slightly beyond. One person fits in frame from waist up. The subject can be touched but requires reach. This is the distance of friends, colleagues, and acquaintances.

**Behavioral Characteristic:** Subject acknowledges the camera's presence — they know they are being photographed. They may smile or pose, but the pose is "for" a specific person they trust. The subject and photographer have an established relationship. Eye contact with lens is deliberate but not uncomfortable. Body language is open and relaxed — not staged but not fully candid.

**Image Characteristics:**
- Waist to head framing typical
- Face is primary focus but shoulders and some torso visible
- Background context appears — environment signals relationship
- Eye contact with camera is direct but less intense than intimate distance
- Natural smile rather than forced "say cheese"
- Hair and clothing visible with full detail
- Bokeh appears on background — partial separation from context

**Example Prompt Grammar:**
> Personal distance captured at arm's length approximately 60-90cm from subject, waist-up framing with face primary, subject aware of camera but comfortable within established relationship, direct eye contact with lens deliberate but not forced, natural smile arising from photographer relationship not mechanical response, environmental context visible indicating setting and mood, shoulders and upper torso in frame with slight bokeh on background, available natural light slightly warm, skin texture partially softened by portrait mode, authentic friendship or familiarity dynamic captured not stranger awkwardness, social photography documentation of comfortable relationship, warm tones slightly desaturated

---

### SD_03: Social Distance (120cm - 360cm / 48 inches - 12 feet)

**Physical Description:** The camera is several feet from the subject. One or two full figures fit in frame. This is the distance of group photos, party documentation, and public interaction. The subject cannot be touched from this distance.

**Behavioral Characteristic:** The subject is aware of being photographed but less focused on it — the camera is a background condition rather than a direct invitation. They interact with people around them rather than with the camera. The photographer is part of a social event, not directing it. Subjects often cluster — the photograph captures social geometry.

**Image Characteristics:**
- Full figure(s) in frame with substantial environmental context
- Multiple people may be present — relationship between subjects visible
- Subject orientation is not centered on camera — attention directed elsewhere
- Environmental context occupies 40-60% of frame
- Social interaction visible — subjects talking, laughing together
- Background contributes to story — venue, decoration, weather
- Wider lens creates natural compression if using smartphone 1x

**Example Prompt Grammar:**
> Social distance captured at 120-360cm from subject group, full figures with substantial environmental context occupying 40-60% of frame, subjects oriented toward each other not toward camera, attention directed to social interaction among group members, multiple people clustered in natural arrangement, environmental context contributes narrative information about setting mood occasion, subjects mid-conversation mid-laugh with faces partially away from camera, photographer part of event not directing it, candid group photography within social context, smartphone wide lens natural compression, available warm interior light, authentic social moment not posed portrait, bokeh minimal environmental details sharp, casual documentation of friendship or gathering, natural interpersonal geometry captured not composed group shot

---

### SD_04: Public Distance (360cm+ / 12 feet+)

**Physical Description:** The subject is far from the camera — a small figure in a vast environment. Street photography, architecture, and landscape include humans as scale elements. The photographer is a stranger to the subject. No relationship exists.

**Behavioral Characteristic:** The subject is unaware of the camera or aware but indifferent. They behave naturally — walking, waiting, talking — without performance for the lens. The photograph captures human activity as it occurs rather than as directed. The photographer has no social relationship with any subject.

**Image Characteristics:**
- Subject is small — environmental context dominates
- Subject may be in motion — blur from movement
- Face detail limited or absent — too far for feature recognition
- Environmental narrative primary — what the place feels like
- No eye contact with camera — subject looking away or down
- Light source is ambient environmental — sun, street lamp, sky
- No portrait mode advantage — subject too small for bokeh

**Example Prompt Grammar:**
> Public distance captured at 360cm or greater from subject figure, human small scale element in vast environmental context, subject moving walking or standing unaware of camera presence, face detail limited to generalized shape not specific features, environmental narrative dominant over subject documentation, street photography urban landscape context with subject providing human scale reference, no eye contact or performance for camera, ambient environmental light source sun or artificial street illumination, smartphone wide lens maximum environmental capture, subject caught in natural activity without awareness or consent, documentary photography aesthetic, human activity as ambient element not focal point, candid moment from public distance, authentic scene documentation not staged portrait

---

### SD_05: Technical Distance (Inverted Social Distance)

**Physical Description:** The subject operates the camera themselves — selfie distance. This creates an inversion where the photographer and subject are the same person. The spatial relationship is fixed: arm's length + phone width + face distance.

**Behavioral Characteristic:** Maximum self-awareness. The subject controls exactly what they look like, exactly what expression they make, exactly how they angle their face. They see themselves in the preview. There is no "other person" to interact with — the subject performs for themselves. Micro-expressions are rehearsed and examined. The "good side" is maximally exploited.

**Image Characteristics:**
- Face fills frame or extends to edges with arm visible
- Eyes locked directly with lens — staring
- Expression controlled and examined — frozen smile or studied neutrality
- "Good side" angle fixed — no accidental bad angles
- Arm extension geometry visible — elbows at 90 degrees
- Background is chosen for aesthetic not documentary value
- Skin may be smoothed by beauty mode

**Example Prompt Grammar:**
> Technical selfie distance with front camera held at fixed arm's length, subject operating camera themselves with maximum self-awareness and control, eyes locked directly with lens at close range creating intense direct stare, expression controlled examined frozen not genuine, face at fixed angle exploiting "good side" consistently, both arms visible holding phone with elbows flared wide, background selected for aesthetic value not documentary context, beauty mode potentially active smoothing skin texture, arm extension geometry fixed and visible in frame, subject performing for self not interacting with another person, selfie aesthetic with no photographer-subject relationship, mirror or preview screen influence visible in composition, sharp front camera capture with slight wide-angle distortion near edges, neutral or slightly warm color temperature, optimal technical quality with zero authentic moment capture, mirrored self-documentation

---

## PHOTOGRAPHER PRESENCE SYSTEM

Photographer presence is a spectrum from maximum invisibility (candid) to maximum visibility (posed). The position on this spectrum fundamentally alters the subject's behavior and the resulting image authenticity.

### PP_LEVEL_01: Completely Invisible (Subject Unaware)

The photographer exists as an observer without social presence. The subject does not know they are being documented. This is the purest form of candid photography.

**Subject Behavior:** Completely natural — no performance, no awareness, no adjustment. The subject behaves as if alone. Facial expressions arise from genuine emotion. Body language is unconscious. No one is watching.

**Technical Marks:**
- Extreme or unusual angles — photographer didn't need to be in front of subject
- No eye contact with camera ever
- Subject may be partially turned away — the camera caught a moment
- Background overlaps or crowds — no compositional isolation of subject
- Timing is random — subject mid-motion or mid-expression

**Example Prompt Grammar:**
> Photographer completely invisible with subject unaware of camera presence, subject mid-natural behavior without performance or awareness, face partially turned away from lens, extreme non-standard angle unusual for normal photography, timing random catching subject mid-motion or mid-expression, environmental context dominant, no compositional isolation, subject photographed as ambient element in scene, no photographer-subject relationship exists, documentary observation without social presence, voyeuristic authenticity, analog-inspired grain, imperfect framing from concealed position

---

### PP_LEVEL_02: Minimally Visible (Subject Aware But Not Interacting)

The subject knows they are being photographed but does not interact with the photographer. The photographer observes; the subject is aware of being observed but continues their activity.

**Subject Behavior:** Aware but not performing. The subject knows the camera exists and may feel its presence but does not change behavior significantly. They may be too busy (walking, working, talking) to adjust. Occasionally they look at the camera and then return to their activity. The awareness creates slight tension — they are "on record" — but the behavior is still mostly natural.

**Technical Marks:**
- Occasional direct eye contact with camera
- Slightly more composed body positioning than fully unaware
- Awareness visible in expression — a certain "being documented" quality
- Still includes action or activity — subject not frozen
- Some compositional awareness — photographer might have moved to position

**Example Prompt Grammar:**
> Subject minimally aware of photographer presence with camera present but no direct interaction occurring, subject acknowledging camera with occasional glance but continuing activity, slightly composed body orientation not fully natural but not posed, expression includes subtle awareness of being documented, some environmental compositional awareness by photographer, action and activity still present in frame, subject not frozen but slightly self-conscious, warm candid photography with partial awareness, photographer observing not directing, natural behavior still predominant with slight performance edge

---

### PP_LEVEL_03: Active Social Presence (Photographer Participates)

The photographer is part of the social situation. They interact with the subject before, during, or after the shot. The photographer is a friend, partner, or companion who happens to be holding a camera. The social relationship creates comfort and authenticity.

**Subject Behavior:** Comfortable and warm. The subject trusts the photographer. They laugh together. The photographer may call out "hey look at this" or "do that thing." The subject responds with genuine affection or amusement. The relationship produces authentic emotional content.

**Technical Marks:**
- Subject laughing or smiling at photographer — direct eye contact with lens in response to photographer
- Warm body language toward camera
- Photographer vocal in capture — audible sounds of getting attention
- Subject not performing for camera but for the person holding it
- Authenticity arises from relationship not from direction

**Example Prompt Grammar:**
> Photographer actively participating in social situation with subject, photographer calling attention and subject responding with genuine laughter or affection, direct eye contact with camera as response to photographer personality, warm body language oriented toward camera position, audible sounds of photographer engaging subject before or during capture, subject performing for person holding camera not for device, authentic emotion arising from relationship not instruction, comfort and trust visible in body orientation, social photography with active participation, genuine moment between people not between camera and subject, warmth captured through interaction not direction

---

### PP_LEVEL_04: Directorial Presence (Photographer Commands)

The photographer is actively directing the subject. This is a performance relationship: the photographer tells, the subject obeys. Posing, composition, expression — all are directed. The subject may feel self-conscious under direction but the photographer has full control.

**Subject Behavior:** Following instructions. The subject moves as told. They adjust their face as instructed. They say "cheese" or smile on command. The relationship is instructional, not emotional. The subject may feel awkward under direct observation and direction. Some subjects freeze; others over-perform.

**Technical Marks:**
- Subject positioned in specific pose — hands placed, chin tilted, shoulders angled
- Expression on command — smile may appear forced or mechanical
- No interaction with photographer — direction is verbal not relational
- Background adjusted or selected to frame subject
- Camera angle chosen for flattering not for relationship
- Multiple shots with adjustments between each

**Example Prompt Grammar:**
> Photographer directly commanding subject position pose expression through verbal instruction, subject following direction adjusting chin tilt and hand placement as told, expression given on command like "smile" not arising naturally from interaction, no photographer-subject relationship in shot — direction is instructional not relational, background selected or adjusted to frame subject, camera angle chosen for technical flattering not organic, mechanical or forced smile in response to command, multiple exposures with adjustment between each, overposed and overdirected, professional portrait aesthetic with technical quality but emotional void, composed and controlled not authentic

---

### PP_LEVEL_05: Complete Performance (Subject Fully Aware of Final Use)

The subject knows the image will be used for a specific purpose — profile photo, dating app, advertisement, ID card. The subject is performing a representation of themselves for an audience they cannot see. This creates a strange self-consciousness: the subject is both the performer and the imagined audience.

**Subject Behavior:** Representing. The subject is not being themselves — they are being the version of themselves they want to present. This may be aspirational (better-looking version), professional (appropriate-for-context version), or strategic (what will get the most engagement). The performance is toward an invisible future audience.

**Technical Marks:**
- Specific pose associated with "good photo" — same angles repeated across subjects
- Expression is "the smile" — practiced, consistent, branded
- Clothing and grooming are intentional and considered
- Background selected for context signaling — not random
- Camera quality maximal — this photo matters
- Possible heavy post-processing or filter application

**Example Prompt Grammar:**
> Subject fully aware of image's future audience and purpose, performing representation of self for unseen viewers, specific pose associated with good photo practiced over time and repeated, expression "the smile" consistent across multiple shots, clothing and grooming intentional and considered, background selected for context signaling not random organic, camera quality maximal — this image matters, heavy post-processing potential, dating profile or social media aesthetic, representation not documentation, subject projecting idealized self toward imagined audience, branded consistent appearance across shots, aspirational self-presentation, clean sharp technical quality with controlled expression, no authentic moment — deliberate construction for external evaluation

---

## CAMERA-SUBJECT INTERACTION MATRIX

The relationship between camera position, subject position, and social context creates a matrix of possible interactions. Each cell produces distinct image characteristics.

| Camera Position | Subject Position | Social Context | Result |
|----------------|------------------|----------------|--------|
| Eye level | Standing | Alone | Standard portrait |
| Above | Standing | Alone | Flattering, empowering subject |
| Below | Standing | Alone | Diminishing, subordinate subject |
| Eye level | Seated | Alone | Relaxed, intimate |
| Eye level | Lying | Alone | Intimate, private, vulnerable |
| Eye level | Standing | Group | Social geometry, relationship visible |
| Above | Group | Group | Equality through perspective |
| Various | Various | Moving | Captured motion, behavioral document |

---

# AREA 02: BAD PHOTO REALISM

## Why Imperfect Photos Feel More Real

The human visual system is trained on billions of imperfect photographs taken by amateurs. We have learned to read blur as motion, tilt as urgency, grain as darkness, cropped faces as accidental framing. When an image is technically perfect — sharp in all planes, perfectly lit, perfectly composed — the visual system reads it as constructed, artificial, and "photoshopped." Imperfection is the signature of the real.

The bad photo realism system identifies the specific failure modes that signal authentic human capture rather than professional construction. Each failure type has a mechanical cause, a visual signature, and an authenticity signal.

---

## IMPERFECT_PHOTO_SYSTEM

### FAILURE TYPE 01: The Accidental Crop

**Mechanical Cause:** The photographer failed to frame the subject correctly. The subject's face, body, or relevant element is partially cut off by the frame edge. This is never intentional in amateur photography — it is always a failure of attention or skill.

**Visual Signature:**
- Face cut off at edge — forehead, ear, chin, or jawline at frame boundary
- Body truncated at waist, hip, or knee — missing lower half
- Hand or arm severed at wrist or elbow — the arm simply ends
- Architectural element bisected — column through head, horizon through face
- Crop is asymmetric — off-center in a way that suggests inattention

**Authenticity Signal:** The accidental crop tells the viewer that no professional spent time composing this image. Professionals check their framing. Amateurs miss. The miss is evidence of authenticity.

**Example Prompt Grammar:**
> Accidental face crop with forehead and top of head cut off by frame edge, ear partially visible at left border, asymmetric framing suggesting inattention, amateur photographer missed framing and cut into subject's face, no professional composition awareness — subject's head bisected by top of frame, jawline cut by right edge, handheld smartphone framing with no awareness of edges, authentic accidental crop not intentional composition, real human moment not carefully staged, bad but genuine photography error

---

### FAILURE TYPE 02: Motion Blur From Subject Movement

**Mechanical Cause:** The shutter speed was too slow to freeze the subject's motion. This happens in low light (indoor, night) or when the subject is moving. The photographer did not have flash or did not want to use it. The motion blur tells the story of what was happening in that moment.

**Visual Signature:**
- Subject's body or face is smeared — edges trail behind movement direction
- Sharp to blurred gradient across the frame — frozen background, moving subject
- In severe cases, subject becomes an abstract shape — identity obscured
- Hair blurs most dramatically — fine strands create motion trails
- Double-image ghosting in mild blur — subject appears in two positions

**Authenticity Signal:** Motion blur is impossible to fake convincingly without expensive software. It requires the actual physics of light and time. The blur is proof that the moment happened in real time. You cannot pose motion blur.

**Example Prompt Grammar:**
> Severe motion blur from subject movement during exposure, body and face smeared with edges trailing behind motion direction, hair creating motion trails with fine strand blur, background sharp while subject is abstract shape identity partially obscured, low light interior with shutter speed too slow for movement, no flash used or flash unavailable, genuine human motion captured not staged, impossible to fake convincingly — real-time physics of light and time, blur as proof of authentic moment, movement happened in real life, slight double-image ghosting in mild blur areas, warm interior available light with grain

---

### FAILURE TYPE 03: Motion Blur From Camera Shake

**Mechanical Cause:** The photographer's hand moved during the exposure. This happens in low light when the photographer holds the camera steadily enough for autofocus but not steadily enough for sharp capture. The blur direction reveals the camera's movement vector.

**Visual Signature:**
- Entire frame blurs uniformly — background and subject share blur
- Blur direction is diagonal or rotational — the camera twisted or shifted
- Straight lines in environment become slanted or wavy
- Subject face is recognizable but soft — edges undefined
- Blur is consistent across frame — not subject-specific like motion blur

**Authenticity Signal:** Camera shake is an intimate signature of the specific person holding the phone. The angle and direction of shake is unique to that person's tremor patterns, grip, and breathing. Camera shake is the fingerprint of handheld amateur capture.

**Example Prompt Grammar:**
> Uniform camera shake blur affecting entire frame including background, diagonal rotational blur direction revealing photographer's hand movement, entire image soft with edges undefined and straight lines slanted, subject face recognizable but unsharp, photographer's individual tremor pattern and grip visible in blur direction, handheld smartphone in low light without stabilization, authentic amateur camera shake fingerprint not tripod setup, impossible to replicate artificially, personal physical signature of specific human holding device, breathing and hand pressure visible in blur angle, warm interior low light with grain, genuine handheld capture evidence

---

### FAILURE TYPE 04: Severe Underexposure (Image Too Dark)

**Mechanical Cause:** The camera exposed for the background or for highlights, leaving the subject dark. This happens in backlit situations — subject in front of window, subject in front of sun — when the camera's meter gets confused.

**Visual Signature:**
- Subject is silhouette — features unreadable, shape only
- Subject face is near-black with minimal detail — eyes not visible
- Background is correctly exposed — bright and detailed
- Strong rim light may separate subject from background
- Shadow fills most of frame — only highlights survive

**Authenticity Signal:** Underexposure is a failure of technical skill, which is precisely why it reads as authentic. Professionals use fill flash or exposure compensation. Amateurs let the camera decide and lose the subject. The darkness is evidence of no professional intervention.

**Example Prompt Grammar:**
> Severe underexposure with subject in silhouette shape only features unreadable, background correctly exposed and bright while subject is near-black with minimal detail, strong backlight creating rim light separation from environment, camera metered for background not subject, no fill flash used or exposure compensation adjusted, professional would have used flash or exposure lock — this failure is amateur evidence, darkness is authentic no-intervention signature, intentional or not this image looks unprocessed and real, subject shape readable but face detail lost in shadow, dramatic natural light with extreme contrast, authentic technical failure not aesthetic choice

---

### FAILURE TYPE 05: Severe Overexposure (Image Too Bright)

**Mechanical Cause:** The camera exposed for the subject, leaving the background blown to white. Or the flash fired in a dark room and washed out the entire scene. Or the subject is in front of a bright light source and the camera overcompensated.

**Visual Signature:**
- Subject face is white — skin tones gone, features merged
- Background is white wall — no detail, no texture, no context
- Highlights are clipped — no information in the brightest areas
- Eyes appear as dark holes in white face — pupils invisible
- Flash washout creates flat white fog throughout frame

**Authenticity Signal:** Overexposure destroys information. Once the sensor saturates, no software can recover the detail. This is a one-way failure — you cannot fix it in post without looking fake. The blown highlights are proof that no skilled photographer controlled this capture.

**Example Prompt Grammar:**
> Severe overexposure with subject face completely white and skin tones absent, highlights clipped with no recoverable detail in brightest areas, background blown to white wall with no texture or information, eyes appear as dark holes in white face with pupils invisible, flash washout creating flat white fog throughout frame, camera metered for face not environment, no exposure compensation or flash diffusion used, amateur evidence of no professional control, one-way failure — clipped highlights unrecoverable, authentic technical failure visible, white space replacing real information, harsh flash in dark interior, genuine bad capture not aesthetic choice

---

### FAILURE TYPE 06: Incorrect White Balance (Wrong Color Temperature)

**Mechanical Cause:** The camera's white balance algorithm chose incorrectly for the lighting situation. Mixed indoor lighting (tungsten and fluorescent together) confuses auto white balance. The resulting image has wrong colors — orange skin, green walls, blue shadows.

**Visual Signature:**
- Skin tones shift to orange or blue — not natural flesh color
- White objects have strong color cast — white shirt is actually blue or yellow
- Background walls or furniture have incorrect colors
- Mixed lighting creates conflicting zones of color temperature
- Fluorescent flicker may create banding or inconsistent color across frame

**Authenticity Signal:** Incorrect white balance is a consumer camera artifact. Professionals set white balance manually or shoot RAW and correct in post. Auto white balance errors are endemic to smartphone photography in mixed lighting. The wrong colors are a signature of the device's limited processing.

**Example Prompt Grammar:**
> Incorrect white balance with skin tones shifted to orange or blue not natural flesh color, white objects carrying strong color cast — white shirt actually blue or yellow, mixed interior lighting tungsten and fluorescent creating conflicting color temperature zones, fluorescent flicker possibly creating banding or inconsistent color across frame, auto white balance confused by complex lighting situation, smartphone processing limited in mixed light, authentic consumer camera artifact not professional color correction, wrong colors as signature of limited device processing, amateur evidence visible in color failure, warm orange skin or cool blue shadows, natural but incorrect, unedited bad capture aesthetic

---

### FAILURE TYPE 07: Extreme Lens Distortion (Wide Angle Failure)

**Mechanical Cause:** The subject is too close to the wide-angle lens and the perspective is warped. Facial features near the edges of the frame are stretched. The nose appears larger than reality. The face looks "funny" in a specific way that smartphone cameras produce.

**Visual Signature:**
- Nose appears significantly larger than real — enlarged at close range
- Face edges stretched — eyes wider apart than real, forehead extended
- Subject near edge of frame has severe distortion
- Background may be artificially expanded — rooms look larger than real
- Straight lines near edges bow inward or outward

**Authenticity Signal:** Extreme wide angle distortion is specific to smartphone cameras used incorrectly. Professionals use longer lenses or step back. Amateurs get close and create cartoonish faces. The distortion is an anti-professional signature.

**Example Prompt Grammar:**
> Extreme wide angle lens distortion from subject too close to smartphone wide lens, nose significantly larger than real with facial features stretched near frame edges, eyes appearing wider apart than actual proportion, forehead extended and chin compressed, subject positioned near edge with severe perspective warp, background artificially expanded with rooms larger than real, straight lines bowing inward or outward near edges, amateur failure — professional would use portrait lens or step back, smartphone wide used at intimate distance creating cartoonish face, authentic device limitation not aesthetic choice, distortion signature of consumer camera used without skill, funny not flattering appearance, real person looks like phone camera made them look

---

### FAILURE TYPE 08: Finger or Hand Blocking Lens

**Mechanical Cause:** The photographer's finger or thumb accidentally covered part of the lens. This creates a dark shape — usually a curved finger pad — partially over the image. The blocking object is in focus because it's close to the lens.

**Visual Signature:**
- Finger pad or thumb visible in corner or edge of frame — curved shape
- Dark vignette from finger covering part of lens opening
- Finger in focus because it's at lens distance — not part of the scene
- May show skin detail — fingerprint texture visible
- No explanation within the scene — the finger doesn't belong to any subject

**Authenticity Signal:** Finger blocking is a purely amateur artifact. It requires the photographer to be holding the camera incorrectly. It cannot happen with a tripod or remote trigger. The finger in frame is proof that a human was holding the camera at the moment of capture.

**Example Prompt Grammar:**
> Finger accidentally blocking portion of lens creating dark curved shape at frame edge, thumb pad or finger covering corner with skin detail visible and in focus, dark vignette from finger blocking lens opening, finger at lens distance not part of scene — doesn't belong to any subject in frame, purely amateur artifact requiring photographer to hold camera incorrectly, impossible with tripod or remote trigger, human holding device evidence, finger in focus close to lens, accidental not intentional, authentic bad smartphone hold, skin texture visible on blocking finger, real human error captured in frame

---

### FAILURE TYPE 09: Autofocus Miss (Wrong Area Sharp)

**Mechanical Cause:** The camera autofocus locked onto the wrong part of the scene — the background, a foreground object, the floor — while the subject remains soft and out of focus. The subject may be sharp at a different distance.

**Visual Signature:**
- Subject face is soft — out of focus while background is sharp
- Camera focused on background object instead — plant, wall, chair
- Foreground element is sharp — something closer than subject
- Hair and facial features lack edge definition — creamy blur
- Eyes are particularly soft — the area of intended focus missed them

**Authenticity Signal:** Autofocus misses are specific to single-af systems in smartphone cameras. Professionals use single-point autofocus or manual focus and verify. Amateurs trust the camera completely and miss. The soft subject is evidence that no one checked the focus before shooting.

**Example Prompt Grammar:**
> Autofocus missed subject with camera locking onto background instead, subject face soft and out of focus while background environment is sharp and detailed, camera focused on wall or plant behind subject, eyes particularly soft without edge definition, hair lacking sharpness and detail, creamy bokeh on intended subject with sharp unintended elements, smartphone single-af system confused by scene complexity, amateur trust of auto focus without verification, no professional checking focus point before capture, soft subject evidence of no manual intervention, authentic camera failure not aesthetic choice, wrong part of scene sharp

---

### FAILURE TYPE 10: ISO Noise and Grain in Low Light

**Mechanical Cause:** The camera used a high ISO setting to compensate for low light, introducing visible noise and grain throughout the image. This is endemic to smartphone cameras in interior and night situations.

**Visual Signature:**
- Visible grain across entire frame — not just in shadows
- Color noise — red and blue specks in areas of solid color
- Luminance noise — brightness variation creating texture
- Detail loss — fine textures eaten by noise
- Grain pattern is non-uniform — stronger in darker areas

**Authenticity Signal:** ISO grain is physics — it's the random variation of photons hitting the sensor. You can reduce it with better hardware, but the presence of significant grain tells you the light was low and the camera was working hard. Grain is evidence of real low-light capture.

**Example Prompt Grammar:**
> High ISO grain throughout entire frame with visible noise and luminance variation, color noise with red and blue specks in solid color areas, fine textures lost to noise, grain stronger in darker areas with non-uniform pattern, low light interior or night exterior with camera working at high ISO, smartphone sensor struggling in insufficient light, authentic low-light capture evidence — grain is physics cannot be faked, real light situation not constructed, natural grain pattern not heavy post-processing, warmth from high ISO, genuine low-light moment with visible noise, imperfect but authentic

---

### FAILURE TYPE 11: Flash Sync Failure (Dark Image With Flash-lit Strip)

**Mechanical Cause:** The flash fired but the shutter was too slow to capture the lit moment across the entire frame. This creates a dark image with a bright strip where the flash illuminated, and the rest of the frame remains dark.

**Visual Signature:**
- Horizontal or vertical bright strip from flash — subject or environment lit
- Rest of frame dark — far below flash range
- Harsh shadow transitions at strip edges
- Motion frozen in lit strip, motion blur in dark areas
- Very limited lit area — only what flash reached before shutter closed

**Authenticity Signal:** Flash sync failure requires using flash in a dark environment with a slow shutter. Professionals avoid this with proper flash setup or by using bounce flash. Amateurs trigger flash in auto mode and get this strange artifact. The partial illumination is proof of amateur flash use.

**Example Prompt Grammar:**
> Flash sync failure with bright strip of flash illumination across frame while rest remains dark, harsh shadow transitions at strip edges, subject only lit in narrow horizontal band, rest of frame dark below flash range, shutter speed too slow for full frame flash sync, amateur flash use in dark environment without proper setup, motion frozen in lit strip with blur in dark areas, harsh partial illumination not balanced or diffused, real flash artifact not aesthetic choice, limited lit area evidence of cheap or misused flash, dark bar or interior with direct on-camera flash, authentic technical failure visible

---

### FAILURE TYPE 12: Lens Flare and Ghost Images

**Mechanical Cause:** Light entered the lens at an angle and created internal reflections. This produces bright artifacts, hazy light streaks, or ghost images of bright sources in the frame.

**Visual Signature:**
- Bright light streak across frame — lens flare in diagonal direction
- Ghost image of sun or bright light source — duplicate shape offset in frame
- Haze reducing contrast — flare reducing image quality
- Colored artifacts — green or purple tint from lens coating reflections
- Flare position relates to light source location in frame

**Authenticity Signal:** Lens flare happens when you point a camera toward a bright light and don't shield the lens with your hand. Professionals shade the lens or compose to avoid flare. Amateurs shoot directly into lights and get artifacts. The flare is evidence of shooting toward bright light without technique.

**Example Prompt Grammar:**
> Lens flare artifact with bright streak across diagonal of frame, ghost image of sun or bright light source appearing offset in composition, haze reducing contrast and image quality, colored artifacts green or purple from lens coating internal reflections, photographer shooting toward bright light without shielding lens with hand, amateur technique without professional shading or compositional awareness, authentic lens artifact not aesthetic choice, flare evidence of shooting toward light source, natural but unwanted, real camera behavior not constructed

---

### FAILURE TYPE 13: Double Exposure (Ghost Overlap)

**Mechanical Cause:** The camera captured two images in one frame — either from slow shutter combined with flash, or from a malfunction, or from very rapid shooting in low light. The subject appears twice at different positions.

**Visual Signature:**
- Subject appears twice — ghost image offset from primary
- Ghost is semi-transparent — overlay of two captures
- Position shift matches time between exposures
- Environment may also be doubled — architectural features overlapping
- Blur follows both subjects — motion blur consistent

**Authenticity Signal:** Double exposure is a film photography artifact that occasionally appears in digital when things go wrong. It requires two moments to be captured in one frame. The overlay is evidence that the camera malfunctioned or the timing was unfortunate. It cannot be staged without intention.

**Example Prompt Grammar:**
> Double exposure ghost overlap with subject appearing twice in frame at different positions, semi-transparent overlay of two captures with position shift matching time between exposures, environment also doubled with architectural features overlapping, motion blur consistent across both subject instances, slow shutter combined with flash creating ghosting or camera malfunction in low light, authentic technical failure requiring two moments captured in one frame, film photography artifact appearing in digital, evidence of malfunction or unfortunate timing, not staged without specific intent, real camera error, imperfect but genuine

---

### FAILURE TYPE 14: Tilted Horizon (Unintentional Angle)

**Mechanical Cause:** The camera was held at an angle and the horizon in the frame is not level. This creates diagonal horizon lines, making the image feel unstable and urgent.

**Visual Signature:**
- Horizon line tilts — not level with frame edges
- Architectural features angle upward or downward
- Subject may appear off-balance — leaning or falling
- Trees and buildings lean in ways that look wrong
- Diagonal tension throughout — nothing is level

**Authenticity Signal:** Tilted horizons are amateur mistakes. Professionals use level indicators or calibrate their tripod. Amateurs hold the camera however and the horizon tilts. The instability is evidence of no professional control.

**Example Prompt Grammar:**
> Tilted horizon with camera held at angle making horizon line not level with frame edges, architectural features angles upward or downward creating instability, subject appears off-balance with body leaning or falling sensation, trees and buildings leaning in wrong directions, diagonal tension throughout image — nothing is level, amateur hold with no level indicator or professional calibration used, authentic unintentional tilt not artistic choice, instability as evidence of no professional control, natural urgency from angle not composed stability, real human hold error

---

### FAILURE TYPE 15: Flash Red-Eye

**Mechanical Cause:** The flash reflects off the subject's retina and bounces back to the lens, creating red pupils. This happens in low light when the pupils are dilated.

**Visual Signature:**
- Eyes have red pupils — bright red rather than natural eye color
- Subject appears demonic or inhuman in severe cases
- Both eyes usually affected symmetrically
- Red reflection visible in iris and pupil area
- Face otherwise normally lit — only eyes show color error

**Authenticity Signal:** Red-eye is endemic to built-in camera flashes in dark environments. It requires a flash in low light. Professionals use bounce flash, off-camera flash, or red-eye reduction mode. Amateurs fire direct flash and get demon eyes. The red eyes are signature evidence of amateur flash use.

**Example Prompt Grammar:**
> Flash red-eye with eyes showing bright red pupils not natural eye color, severe case making subject appear demonic or inhuman, both eyes affected symmetrically, red reflection visible in iris and pupil area, face otherwise normally lit with only eyes showing color error, built-in camera flash used in low light interior with subject pupils dilated, amateur direct flash fire without bounce or diffusion, red-eye reduction mode not engaged, professional would use bounce flash off-camera setup or red-eye pre-flash — this is amateur evidence, authentic technical failure, real flash artifact

---

### FAILURE TYPE 16: JPEG Compression Artifacts

**Mechanical Cause:** The image was saved in aggressive JPEG compression and block artifacts are visible. This happens with heavy social media compression or cameras set to low-quality JPEG.

**Visual Signature:**
- Blocky artifacts in areas of uniform color — sky, walls
- Mosquito noise near edges — spurious pixels near high-contrast boundaries
- Color banding — gradients stair-step instead of smooth
- Detail loss in fine patterns — grass becomes blocky smear
- Overall softness from information loss

**Authenticity Signal:** JPEG artifacts are the signature of heavily compressed images — the kind that get uploaded, downloaded, re-uploaded, and re-downloaded through social media pipelines. Each generation loses quality. The artifacts are evidence of image age and social media transit.

**Example Prompt Grammar:**
> JPEG compression artifacts with blocky artifacts in uniform color areas like sky or walls, mosquito noise near edges with spurious pixels at high-contrast boundaries, color banding with gradients stair-stepping instead of smooth, detail loss in fine patterns like grass becoming blocky smear, overall softness from information loss, heavy social media compression pipeline — image uploaded downloaded re-uploaded multiple times, evidence of image age and social media transit, authentic compression artifacts not original capture quality, imperfect digital history visible in image degradation, real social media document not pristine original

---

### FAILURE TYPE 17: Depth Map Failure (Portrait Mode Edge Errors)

**Mechanical Cause:** The camera's portrait mode depth mapping failed to correctly identify the subject's edges. Background bleeds into hair, shoulders blend into background, or random background patches appear sharp when they should be blurred.

**Visual Signature:**
- Hair merges with background — no clean edge
- Shoulder blends into background — silhouette broken
- Random background patches sharp while intended bokeh areas are blurred
- Subject edges have halos — bright outline where blur meets sharp
- Complex edges — ears, glasses, wispy hair — fail completely

**Authenticity Signal:** Portrait mode failures are specific to smartphone computational photography. They cannot happen in optical capture — only computational cameras produce these errors. The artificial bokeh gone wrong is a signature of fake background blur.

**Example Prompt Grammar:**
> Portrait mode depth map failure with hair merging into background with no clean edge, shoulder blending into background breaking silhouette, random background patches sharp while intended bokeh areas blurred, halos at subject edges with bright outline where blur meets sharp, complex edges like ears glasses wispy hair failing completely, smartphone computational photography only error — cannot happen in optical capture, fake bokeh gone wrong is signature of computational camera, authentic portrait mode failure not professional lens, artificial blur incorrectly applied, real smartphone limitation, imperfect but authentic digital process failure

---

### FAILURE TYPE 18: Focus Hunt (Camera Searching for Focus)

**Mechanical Cause:** The camera autofocus was searching and did not settle before the photo was taken. The image is sharp in some areas and blurry in others, with the sharp area in the wrong place.

**Visual Signature:**
- Multiple focal planes visible — different distances sharp
- Subject sharp but background also sharp — no depth separation
- Or subject blurry and background sharp — focus on wrong distance
- Slight motion in image — camera was moving while hunting
- Inconsistent sharpness across frame

**Authenticity Signal:** Focus hunting happens when the photographer half-pressed the shutter too early and the camera was still adjusting when the full press happened. Professionals wait for lock. Amateurs press too early and get uncertain results. The inconsistent focus is evidence of no patient professional technique.

**Example Prompt Grammar:**
> Focus hunt with camera searching and not settling before photo captured, multiple focal planes visible with different distances sharp simultaneously, subject sharp with background also sharp no depth separation, or subject blurry while background sharp with focus on wrong distance, slight camera motion during hunt, inconsistent sharpness across frame, photographer half-pressed shutter too early with camera still adjusting, professional would wait for focus lock before full press — amateur impatience, authentic uncertain technique, no professional patience or confirmation, real technical behavior visible

---

### FAILURE TYPE 19: Color Fringing (Chromatic Aberration)

**Mechanical Cause:** The lens created color separation at high-contrast edges — typically purple or green halos along object edges. This is a lens optical error that cheap smartphone lenses produce in bright situations.

**Visual Signature:**
- Purple or green halos along edges of high-contrast boundaries
- Tree branches against sky — color fringing visible
- Subject edges show color split — red and cyan separation
- Strong in corners and edges of frame — less in center
- Lens optics failing at edges and high-contrast situations

**Authenticity Signal:** Chromatic aberration is a lens optical error — it comes from the glass. Cheap lenses produce it more. Professional photographers avoid it with better glass or stop down the aperture. The color split at edges is a lens quality signature.

**Example Prompt Grammar:**
> Chromatic aberration with purple or green halos along high-contrast edges, tree branches against sky with visible color fringing, subject edges showing red and cyan color split, stronger in frame corners and edges less in center, cheap smartphone lens optics failing at extreme edges and bright situations, professional would use better lens or stop down aperture to reduce, authentic lens quality signature not professional glass, real optical error from glass properties, imperfect but genuine smartphone camera lens behavior

---

### FAILURE TYPE 20: Dust or Sensor Spot (Dark Circle in Frame)

**Mechanical Cause:** Dust landed on the sensor or lens and created a dark spot in the image. The spot appears in the same position in all photos taken with that device until the dust is cleaned.

**Visual Signature:**
- Dark circular spot in frame — same position every image
- Slightly soft edges — dust on sensor creates shadow
- Always same location — consistent across all photos from device
- Background darkens at that point — not removable in post easily
- May be multiple spots — dust cluster

**Authenticity Signal:** Dust on sensor is a camera maintenance failure. The photographer either doesn't know to clean their lens/sensor or has given up on cleaning it. The spot is consistent evidence of a specific device's condition. It's amateur evidence of no camera maintenance.

**Example Prompt Grammar:**
> Dust or sensor spot creating dark circular blemish in frame at consistent position, soft-edged shadow from dust on sensor, same position in every image from this device until cleaned, not removable in post without cloned removal, multiple spots possible cluster of dust, camera maintenance failure — photographer doesn't know to clean or has given up, consistent device condition evidence, amateur lack of camera care, authentic device imperfection not cleaned or maintained, real camera hygiene failure, imperfect but genuine

---

### FAILURE TYPE 21: Out of Frame (Subject Not In Image)

**Mechanical Cause:** The photographer pressed the shutter but the subject moved before or during the exposure, or the photographer misframed and captured only background.

**Visual Signature:**
- Subject missing from frame — only environment captured
- Subject may be partially visible at edge — caught moving through
- Photographer misframed — no human in image at all
- Evidence of timing error — subject was there but not captured

**Example Prompt Grammar:**
> Out of frame with subject completely missing — only environment captured, photographer pressed shutter but subject moved through or was never in frame, severe framing error with no human present, evidence of timing failure — subject was there but not captured, amateur misframe or subject movement between autofocus and capture, authentic failure, no subject in image, real moment missed

---

### FAILURE TYPE 22: Camera Drop or Shake During Capture

**Mechanical Cause:** The camera was jostled during the exposure — dropped, hit, or shaken — creating a specific chaotic blur pattern that doesn't match normal camera shake or subject motion.

**Visual Signature:**
- Chaotic blur not in consistent direction
- Parts of frame displaced — jagged motion
- Entire frame affected — no single plane sharp
- Impact or drop moment captured — physical camera trauma
- Rotation and translation both present

**Example Prompt Grammar:**
> Camera dropped or shaken during exposure creating chaotic blur not in consistent direction, parts of frame displaced with jagged motion, entire frame affected with no single plane sharp, physical camera trauma during capture, rotation and translation both present, impact moment captured, amateur physical failure not technical error, authentic camera being dropped or hit, real physical event during photography, imperfect chaotic result, genuine camera accident

---

### FAILURE TYPE 23: Neon Sign Reflection Contamination (HK-Specific)

**Mechanical Cause:** Hong Kong's dense neon signage at night creates intense colored reflections on wet streets, glass surfaces, and subjects. The camera's dynamic range cannot handle both the neon and the ambient, causing color contamination.

**Visual Signature:**
- Pink, blue, green neon reflections on wet pavement bleeding onto subjects
- Face or clothing tinted by nearby neon sign color
- Multiple neon sources creating conflicting color zones on single surface
- Reflections more prominent than the actual sign
- Water puddle reflections doubling or tripling neon contamination

**Authenticity Signal:** This is specifically a Hong Kong dense-urban-night environment artifact. The concentration of neon signs in areas like Mong Kok, Central, and Wan Chai creates lighting conditions found nowhere else. The contamination is proof of authentic Hong Kong night environment.

**Example Prompt Grammar:**
> Hong Kong neon sign reflection contamination with pink blue green neon from dense signage reflecting on wet street surface and bleeding onto subjects, face or clothing tinted by nearby neon source, multiple neon sources creating conflicting color zones, reflections more prominent than actual signs, water puddle reflections doubling neon contamination, Kowloon or Mong Kok night environment dominant, authentic Hong Kong dense-urban-night specific artifact, city neon characteristic only possible in specific Hong Kong locations, genuine night market atmosphere, real neon-dominant lighting impossible to construct artificially

---

### FAILURE TYPE 24: Humidity Haze and Heat Distortion (HK-Specific)

**Mechanical Cause:** Hong Kong's high humidity and temperature differential between air-conditioned interiors and hot exterior creates atmospheric haze. Long distance shots through humidity lose contrast and sharpness. The heat from street level creates shimmer distortion.

**Visual Signature:**
- Distant buildings or mountains have washed-out low-contrast appearance
- Heat shimmer visible in vertical direction — wavy distortion
- Loss of detail in far backgrounds — features obscured by atmospheric haze
- Green tinge from vegetation humidity interaction
- White sky merges with white building tops — no separation

**Authenticity Signal:** Hong Kong's specific climate and urban heat island creates atmospheric conditions that cannot be easily replicated. The haze is evidence of real Hong Kong humidity and temperature. The heat shimmer proves the image was captured at street level in summer conditions.

**Example Prompt Grammar:**
> Humidity haze and heat distortion specific to Hong Kong summer conditions, distant buildings or mountains washed out with low contrast, heat shimmer visible in vertical direction with wavy distortion, loss of detail in far backgrounds from atmospheric moisture, green tinge from vegetation humidity interaction, white sky merging with building tops without separation, authentic Hong Kong climate artifact, street-level summer heat captured, genuine urban heat island effect, real humidity conditions only found in Hong Kong sub-tropical environment, atmospheric perspective with reduced contrast from moisture, imperfect but location-specific authentic

---

### FAILURE TYPE 25: Wet Market Fluorescent Contamination (HK-Specific)

**Mechanical Cause:** Hong Kong wet markets (街市) use mixed fluorescent and sodium vapor lighting that creates extreme green-yellow color casts. The combination of fresh fish water, wet floors, and these lights produces unique color signature impossible to replicate.

**Visual Signature:**
- Extreme green-yellow color cast dominant — not natural daylight
- Fish or meat display cases creating bright white spots surrounded by green
- Wet floor reflecting fluorescent tubes creating stripe pattern
- Skin tones completely shifted — not recognizable as natural
- White shirts appearing green or yellow
- Blue sky through market roof appearing gray-green

**Authenticity Signal:** Wet market lighting is specific to Hong Kong's open-air and semi-covered market spaces. The combination of fluorescent tubes, sodium lights, and water reflection creates a color signature found only in these specific locations. The contamination proves authentic wet market environment.

**Example Prompt Grammar:**
> Wet market fluorescent contamination specific to Hong Kong 街市 environment, extreme green-yellow color cast from mixed fluorescent and sodium vapor lighting, fish or meat display cases creating bright white spots surrounded by green, wet floor reflecting fluorescent tubes creating stripe pattern across frame, skin tones completely shifted and unrecognizable as natural, white shirts appearing green or yellow, blue sky through market roof appearing gray-green, authentic wet market artifact, Hong Kong open-air market specific lighting, genuine 街市 atmosphere with fish water and wet concrete, real market environment impossible to fake

---

### FAILURE TYPE 26: Dense Building Background Clash (HK-Specific)

**Mechanical Cause:** Hong Kong's extreme building density means subjects are often photographed against multiple building layers at different distances. Portrait mode depth mapping cannot handle the visual complexity, creating bokeh that looks wrong in multiple directions simultaneously.

**Visual Signature:**
- Bokeh circles appear at multiple sizes indicating multiple distance layers
- Buildings at 10m, 50m, and 200m all visible behind subject simultaneously
- Depth confusion — no clear foreground-background relationship
- City texture overwhelms subject — building windows competing with face
- Background busy with no coherent plane to blur toward

**Authenticity Signal:** The extreme density of Hong Kong's urban environment creates depth complexity that no other city produces. Portrait mode failures here are proof of authentic Hong Kong location — the background complexity is specifically Hong Kong's building density signature.

**Example Prompt Grammar:**
> Dense building background clash specific to Hong Kong urban environment, multiple building layers at 10m 50m and 200m all visible behind subject simultaneously, bokeh circles at multiple sizes indicating depth confusion, portrait mode depth mapping failing from extreme urban density, city texture overwhelming subject with building windows competing with face detail, background busy with no coherent focal plane, authentic Hong Kong specific artifact, genuine Kowloon or Central density impossible to replicate, real extreme urban compression, imperfect but location-specific proof of Hong Kong

---

## SMARTPHONE_ERROR_LIBRARY

### Sensor Limitations

**Rolling Shutter:** CMOS sensors read rows sequentially, creating skew in fast motion or when flash fires. Vertical lines become slanted. This cannot be avoided in smartphone sensors without global shutter.

**Heat Buildup:** Extended video capture or burst photography heats the sensor, increasing noise and reducing dynamic range. The camera "gives up" in the final seconds of a long clip.

**Fixed Aperture:** No mechanical aperture control — exposure managed electronically. Low light performance is fixed — you cannot open up to gather more light.

**No Optical Zoom:** Digital zoom is interpolation — not real magnification. Zoomed images are soft and lack detail. The "2x" button is not equivalent to a 2x lens.

### Processing Failures

**Multi-Frame Synthesis Errors:** HDR and Night Mode combine multiple exposures, creating ghosting when something moves between frames. Faces double. Cars become transparent ghosts.

**Semantic Segmentation Failures:** Portrait mode AI misidentifies background elements as subject — a fence post becomes part of the person, a cloud becomes part of the hair.

**Over-Smoothing:** Aggressive noise reduction removes skin texture along with noise, creating plastic-looking skin in portrait mode. Pores disappear; fine lines vanish; faces become mannequin-like.

**Color Boosting:** The camera processing oversaturates blues (sky) and greens (grass), creating cartoonish colors that don't match real visual memory.

### Physical Failures

**Cracked Lens:** Light scatters through cracks, creating haze, flare, and color shifts that cannot be corrected. The crack is visible as a bright artifact in backlit shots.

**Fingerprint Grease on Lens:** Skin oils create soft-focus blobs that reduce sharpness and add warm color cast. The affected area is soft and has reduced contrast.

**Water Damage:** Moisture inside the camera creates internal fogging — not visible on outside but creates overall haze and reduced contrast in all images.

**Dirty Sensor Corners:** Dust accumulates in sensor corners and creates consistent dark spots. These are only visible at small apertures and bright scenes.

### Capture Timing Errors

**Shutter Lag:** The time between pressing the shutter and the image being captured is long enough that the subject moves or expression changes. The captured moment is not the intended moment.

**Pre-Capture Buffer:** Some phones capture frames before you press the shutter. If the subject blinks or moves, you may get a frame from 0.5 seconds earlier — before the intended moment.

**Post-Capture Processing:** The image you see in the gallery is not the captured image — it's been processed for 2-3 seconds. The "real" image is different from what you reviewed immediately after capture.

---

## COMBINED FAILURE PATTERNS

### The Night Out Sequence

A sequence of photos taken in low light with multiple failure types combined:
- High ISO grain throughout
- Flash red-eye from dark bar
- Motion blur from unsteady hands
- Camera shake from alcohol impairment
- Accidental face crops from difficult framing
- Color fringing from cheap lens in bright bar lights
- JPEG artifacts from heavy social media upload

This sequence carries maximum authenticity — the failures cluster is evidence of genuine human experience documented in real time.

### The Bathroom Mirror Selfie

A sequence from front camera with specific failures:
- Beauty mode over-smoothing creating plastic skin
- Extreme chin-up angle creating distorted proportions
- Lens distortion enlarging nose
- Finger blocking if held incorrectly
- Mirror reflection capturing phone in frame
- Harsh overhead lighting creating unflattering shadows
- Warm color cast from yellow bathroom bulb

The failures are specific to this genre — each signature identifies the selfie context.

### The Tourist Group Shot

A sequence from stranger with camera:
- Face crops — stranger doesn't know who to include
- Extreme wide angle from close proximity
- Someone blinking — timing error from count-down
- Horizon tilt from unfamiliar camera hold
- Background chaos from no compositional intent
- Flash washout in low interior
- Subject too small in frame from extreme distance

This cluster identifies the tourist capture context specifically.

### The Hong Kong Night Market Sequence

A sequence specific to Hong Kong night market environments:
- Neon sign reflections on wet pavement contaminating subject colors
- Extreme humidity haze reducing distant building contrast
- Mixed fluorescent and sodium vapor lighting creating green-yellow skin cast
- High ISO from market canopy darkness
- Motion blur from slow shutter speed
- Dense crowd creating accidental crops
- Other market shoppers uncropped in background

This cluster identifies authentic Hong Kong 夜市 night market capture context specifically.

### The Hong Kong Escalator/MTR Transit Sequence

A sequence specific to Hong Kong vertical transit:
- Escalator motion blur on steps
- Other passenger heads visible above subject's shoulder
- Fluorescent MTR station lighting with green cast
- Train motion blur through window
- Reflection of self in MTR door glass
- Dense passenger crowd creating accidental crops
- Platform fluorescent creating color contamination

This cluster identifies authentic Hong Kong transit documentation specifically.

---

## MODERATION PROFILE

### Authenticity Indicators

Images with multiple amateur failure signatures are scored as more authentic. The failure cluster is a stronger signal than any single failure. An image with motion blur AND finger blocking AND tilt is more likely to be real than an image with only motion blur.

### Quality Thresholds

- Perfect images (no failures) are scored as suspicious — high-end smartphones produce perfect images routinely, but authentic human capture rarely produces perfect images
- Single failures may be staged — a photographer could intentionally underexpose or tilt for artistic effect
- Multiple failures (3+) in different categories indicate genuine amateur capture
- Specific failure clusters (like the night out sequence or Hong Kong night market sequence) are strong authenticity signals

### Social Context Verification

Photographer-presence level should match image characteristics:
- PP_LEVEL_01 (invisible) should have no direct eye contact with camera
- PP_LEVEL_04 (directed) should have awkward posed quality
- SD_01 (intimate distance) should show relationship context in background

Mismatches indicate manipulation: a perfectly composed image with no failures claimed to be taken by a "drunk friend at a bar" is suspicious.

### Hong Kong Environment Verification

Images claiming Hong Kong location should show environment-specific characteristics:
- Dense building background complexity in urban shots
- Neon color contamination in night shots
- Fluorescent green-yellow cast in market or transit shots
- Humidity haze in distant backgrounds
- Specific signage or branding (GSR, 7-Eleven, MTR, etc.)

Absence of these markers in claimed Hong Kong images is suspicious. Presence of them in non-Hong Kong claims is equally problematic.

### Imperfect Authenticity Weighting

| Failure Type | Authenticity Weight | Notes |
|--------------|-------------------|-------|
| Finger Blocking | VERY HIGH | Requires human hold |
| Camera Shake | HIGH | Unique to handheld |
| Motion Blur (subject) | HIGH | Cannot be posed |
| Autofocus Miss | MEDIUM-HIGH | Auto system failure |
| ISO Grain | MEDIUM-HIGH | Real low light |
| Tilted Horizon | MEDIUM | Could be intentional |
| Portrait Mode Failure | MEDIUM | Computational only |
| Over/Underexposure | MEDIUM | Could be intentional |
| Accidental Crop | MEDIUM | Non-professional |
| Red-Eye | LOW-MEDIUM | Could be fixed |
| Color Cast | LOW | Could be intentional |
| Lens Flare | LOW | Could be intentional |
| Neon Contamination (HK) | HIGH | Location-specific |
| Humidity Haze (HK) | HIGH | Environment-specific |

---

## V15 PROMPT GRAMMAR: IMPERFECT PHOTO SYSTEM INTEGRATION

### Base Authenticity Phrase

> authentic bad smartphone photo not professional, imperfect amateur capture with errors, real human photography not constructed, genuine moment documented with technical failures

### Failure Type Phrases

#### Accidental Crop
> face partially cut off by frame edge, forehead or ear at border, asymmetric framing missed by amateur, no professional awareness of edges

#### Motion Blur
> motion blur from real movement not staged, subject blurred with trails, camera couldn't freeze action — real moment not posed

#### Camera Shake
> camera shake from handheld not tripod, entire frame soft from photographer tremor, real handheld fingerprint not stabilized shot

#### Underexposure
> too dark subject silhouette with background correctly lit, camera failed to meter for human not environment, no fill flash used, authentic technical failure

#### Overexposure
> blown highlights white sky behind subject, face washed out from flash, no exposure compensation used, authentic clip artifact

#### ISO Grain
> high ISO grain throughout image, sensor struggling in low light real physics, genuine low-light capture not constructed

#### Autofocus Miss
> soft subject with background sharp, camera locked onto wrong distance, no professional verification of focus point, authentic miss

#### Portrait Mode Failure
> fake bokeh with errors at hair edges, depth map failed on complex outline, smartphone computational failure only, authentic phone processing artifact

#### Neon Contamination (HK-Specific)
> Hong Kong neon sign color reflection contaminating subject, pink blue green neon on wet street bleeding onto face, authentic night market or Mong Kok environment artifact, genuine Hong Kong dense-urban lighting

#### Humidity Haze (HK-Specific)
> humidity haze reducing contrast on distant buildings, heat shimmer visible in vertical, authentic Hong Kong summer sub-tropical conditions, atmospheric moisture artifact

#### Wet Market Fluorescent (HK-Specific)
> green-yellow fluorescent cast from wet market lighting, fish water and wet floor reflecting tubes, authentic Hong Kong 街市 environment artifact, market-specific color contamination

### Operator Phrases

#### Intimate Partner
> boyfriend or girlfriend shot, intimate partner perspective, no professional direction, unposed genuine moment from relationship

#### Clueless Photographer
> taken by someone who doesn't know cameras, full wide lens no zoom, no direction given to subject, snapshot not composed

#### Tourist Stranger
> random person asked to photograph, tourist snapshot energy, stranger with no relationship to subject, awkward and unposed

#### MTR Platform Commuter (HK-Specific)
> MTR platform fluorescent lighting, transit commuter context, Hong Kong Mass Transit Railway specific environment, passengers mid-commute with thousand-yard stare

#### Late-Night Taxi (HK-Specific)
> Hong Kong taxi interior late night, neon city lights reflecting through window, cramped backseat with friends, wet weather street reflections

#### Convenience Store Walk-Back (HK-Specific)
> Hong Kong 7-Eleven or gsr便利店 context, fluorescent convenience store lighting, bubble tea or snack prop, pre-night-out fuel stop documentation

#### Ferry Deck Friend (HK-Specific)
> Star Ferry or harbour crossing deck, Victoria Harbour background, sunset golden hour, sea breeze hair blur, moving boat motion

#### Wedding Guest Phone (HK-Specific)
> Chinese wedding banquet 筵席 context, guest phone capture, overhead spotlight washout, red and gold decoration clutter, other banquet guests in frame

### Distance and Presence Phrases

#### Intimate Distance
> close up face filling frame with breath visible, skin texture with no environmental context, physical proximity documentation

#### Personal Distance
> arm's length waist up framing, natural smile for person not camera, comfortable relationship between photographer and subject

#### Social Distance
> multiple people in frame with environment, subjects oriented to each other not camera, candid group moment not composed

#### Public Distance
> subject small in vast environment, human as scale element not focal point, street photography documentary distance

#### Invisible Photographer
> subject completely unaware of camera, genuine natural behavior with no performance, candid from concealed or distant position

#### Active Direction
> photographer giving instructions to subject, subject following direction not making genuine expression, posed not captured

### Hong Kong Location Phrases

#### Urban Night (HK)
> Hong Kong night neon environment, Kowloon Mong Kok dense signage, wet street reflections, pink blue green neon contamination

#### Transit (HK)
> MTR station or bus terminus fluorescent, Mass Transit Railway specific context, commuter transit documentation

#### Market (HK)
> Hong Kong wet market 街市, open-air fresh food market, fish water wet floor, fluorescent sodium lighting

#### Residential (HK)
> Hong Kong tower residential background, high-density housing estate visible, urban living context

#### Tourist Landmark (HK)
> Victoria Harbour or Peak background, iconic Hong Kong landmark visible, tourist documentation context

---

## FILE VERIFICATION

**Output File:** ~/Documents/lil.troublr/Engine/V15_RESEARCH/01_SOCIAL_CAMERA_BAD_PHOTO.md  
**Status:** ENHANCED — HK EXTENSION COMPLETE  
**Content Areas:** AREA 01 (Social Camera) + AREA 02 (Bad Photo Realism)  
**Deliverables Completed:**
- CAMERA_OPERATOR_LIBRARY_V2 (22 operator types — 12 original + 10 HK-specific)
- Social-Distance Taxonomy (5 distance levels with behavioral characteristics)
- Photographer-Presence System (5 presence levels)
- IMPERFECT_PHOTO_SYSTEM (26 failure types — 22 original + 4 HK-specific)
- Smartphone-Error Library (sensor limitations, processing failures, physical failures, capture timing errors)
- Combined Failure Patterns (night out, bathroom selfie, tourist group, HK night market, HK transit)
- Moderation Profile (authenticity indicators, quality thresholds, social context verification, HK environment verification)
- V15 Prompt Grammar (base phrases, failure type phrases, operator phrases, distance/presence phrases, HK location phrases)
