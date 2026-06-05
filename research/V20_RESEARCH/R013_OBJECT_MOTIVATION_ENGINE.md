# R013 — Object Motivation Engine

**Mission:** Investigate why AI-generated environments feel staged and prop-arranged-for-viewer rather than naturally existing, then convert that into a production rule system that every visible object in a V20 frame must satisfy.

**Why this matters:** Viewers can't articulate why an image feels "AI" but a major component is the staging of objects. Birthday cards face the camera. Shopping bags are centred and the contents are perfectly visible. Invitation cards on a table are angled to the lens. This engine forbids the staging grammar and replaces it with a residue grammar — objects that look like they got there through use, not through arrangement.

**Canon status:** BLOCKED — does not become canon until production-tested against 50+ generated frames scored on a 5-point realism scale by human raters blind to the engine.

---

## 1. Why humans place objects

### Psychological principle

People do not place objects for viewers. They place objects for *themselves*, for *the next person who will use them*, or for *no one at all*. This is the foundational premise of the engine. Once accepted, the design of object placement becomes a study of *use*, not *display*.

The relevant theory is Gibson's *ecological approach to visual perception* (1979) — affordances. A coffee mug is placed *where the hand expects it* on a wake-up morning, not where a camera would frame it. A shopping bag is dropped *where the foot landed first*, not where the photographer would centre it. An open book lies *where the elbow rested* on the page.

Real-object placement is functional residue of the last interaction. Staged-object placement is compositional residue of the next viewer.

### Visual signature in real placement

- **Objects cluster near the body that just used them** (in the chair, on the side table nearest the bed).
- **Objects rest in the orientation they were placed, not in their most photogenic orientation** (a book lies spine-up, a cup sits with the handle turned to the user's dominant hand).
- **Objects that have been left alone are not straightened** (a coat thrown over a chair stays thrown; a magazine stays where it was dropped).
- **Path of motion is visible**: a wet towel is on the floor, not in a basket, because the basket was too far. The residue reveals a specific body's habits.

### Visual signature in staged placement

- All objects face the same direction.
- All objects are at the same "depth" of focus priority.
- No object is in a state that would be the result of having been used.
- No object is closer to the user than the camera would suggest is reasonable.
- No object is partially occluded in a way that doesn't make sense for the user's POV.

### Failure modes

- **Boutique display logic in a private space**: every item is presented as if in a shop window. Bedrooms, bathrooms, kitchens should not look like retail.
- **Symmetric arrangement**: a table with two candles, a flower, a tray, all centred and equally weighted. This is a "tablescape" — a real genre with its own rules, but it is not a "room someone lives in" genre.
- **Stacking with no functional reason**: books stacked to a height that wouldn't fit a normal shelf; towels folded into thirds like a hotel; cups nested.

### Prompt-construction implications

The engine must mandate a *last user* for every visible object. The user has a body size, a dominant hand, a morning routine, an evening routine, and a sleep position. Every object falls out of these.

---

## 2. Last-interaction state

### Psychological principle

Every object in a real room is in the state of its last interaction. The phone screen still shows the last app because the user was just looking at it. The cup has a waterline because the user took a sip and put it down. The pen is uncapped because the user was just writing.

This is the same principle behind the "props in a crime scene tell you the story" logic that forensic TV has trained viewers to read. The brain parses object states and reconstructs the most recent action.

### Visual signature

- **Wetness, warmth, or stickiness residue**: a glass with condensation, a fork with sauce on it, a pen with a still-wet cap.
- **Position implies a hand just left it**: a handle is still warm, a chair is still slightly pulled out, a book is still in the orientation the hand let go of.
- **Asymmetry of "in progress" objects**: a hand is in the frame still mid-gesture; a sleeve is on the floor because the person is mid-undress.
- **Time-of-day markers**: morning room has bright window light, unmade bed, half-drunk coffee, unopened mail. Evening room has warm lamp light, partial undress, full ashtray or open wine.

### Failure modes

- **Static objects in a "live" environment**: nothing is in the state of having been just used.
- **Over-residue**: every object is wet, warm, full, half-eaten. The brain reads this as over-acting. Residue is a *sparse* signal.
- **Time-of-day incoherence**: morning light with a full ashtray and a half-undone dress.

### Prompt-construction implications

The engine must specify the last interaction for every object: who used it, when, and how it was set down. The prompt can then specify the resulting state.

---

## 3. Visibility justification

### Psychological principle

In a real environment, the *visible* objects are a tiny fraction of the *existing* objects. A room has 200 objects; a frame shows 8–15. The question is: why is *this* object visible from *this* angle?

Possible answers: the object is on the table, the object is the largest, the object is at eye level, the object is in the path of motion, the object was just placed there and not yet put away.

The engine's rule is that every visible object must have at least one of these justifications. A visible object with no justification reads as a prop.

### Visual signature of justified visibility

- An object is on a surface that the camera is looking at.
- An object is large enough to be a focal element.
- An object is at the depth of field that explains why the lens picked it up.
- An object is in motion, being placed, being held.
- An object is part of a larger functional cluster (laptop + mouse + notebook + coffee cup on a desk).

### Visual signature of unjustified visibility

- A single object on a large empty surface (a lone candle, a single shopping bag on a clean floor).
- A perfectly composed "feature object" (a gift box on a pedestal) with no context.
- A surface with one of each "expected" type (one towel, one toothbrush, one cup) with no functional cluster around it.

### Failure modes

- **Feature-object syndrome**: the AI places one of each category, well-composed, to fill the frame. This is the most common AI failure mode for environment generation.
- **Catalogue composition**: every object is the best version of its category (the best pen, the most beautiful book, the photogenic coffee cup). Real rooms have a mix of best, OK, and slightly-broken.

### Prompt-construction implications

Engine must include a *visibility-audit* step: for each visible object, the generator must be able to answer "why is this in the frame from this angle?" If the answer is "because it looks nice", the object should be cut.

---

## 4. Object ownership logic

### Psychological principle

Every object has an owner. Some objects have an obvious owner (a toothbrush in a one-person bathroom). Some have an implied owner (a child's drawing on the fridge has a child as owner). Some have a shared owner (a remote control on a shared couch).

The ownership logic determines *why this object is here*. A shared-object is more central, more accessible, more often used. A personal object is more peripheral, more curated, more often hidden.

### Visual signature

- **Personal items in personal spaces**: her laptop, her book, her skincare on her side of the bathroom counter. Each object has a "her" attached.
- **Sentimental objects with no functional use**: a dried flower, a polaroid stuck to the mirror, a child's drawing. These are owner-anchored.
- **Impersonal shared items at neutral positions**: the salt shaker in the middle of the table, the tissue box in the shared living room.

### Failure modes

- **Generic catalogue objects** with no owner signature: a coffee cup with no fingerprint, no lipstick mark, no wear. Whose cup is this?
- **Multiple owners implied by multiple signatures** on one object: a coffee cup with both a lipstick mark (her) and a bite mark (him) reads as staged because real cups tend to be single-owner.
- **No personal items in a personal space**: a kitchen with no photos, no magnets, no specific-user items = a model home, not a lived-in home.

### Prompt-construction implications

Engine must generate an *occupant list* for every space and assign every visible object to an owner. Objects that cannot be assigned are cut.

---

## 5. Hidden vs visible objects

### Psychological principle

In real spaces, far more is hidden than visible. Drawers are closed, cabinets are shut, wardrobes are closed, bags are zipped, phones are face-down. Visibility requires a *reason*. The default state of storage is closed.

The AI tendency is to *show* things. Open drawers showing neatly arranged contents. Open bags showing the contents arranged for visibility. Open wardrobes showing the clothes arranged by colour. This is staging.

### Visual signature of real hiding

- Most storage is closed by default.
- What's visible is the *in-use* or *just-used* object.
- Open storage implies a specific moment (cleaning, packing, unpacking, looking for something specific).
- The inside of a closed drawer, when glimpsed, is messy. The inside of a closed cabinet is messier than the outside would suggest.

### Visual signature of staged hiding

- The "open the cabinet to reveal a perfectly arranged interior" beat. This is real estate photography, not lived-in photography.
- Objects placed *outside* their normal storage for no reason (a laptop on the floor, a book on the kitchen counter, a coat on the bed).
- The "peek into the bag" beat where the contents are perfectly arranged for visibility.

### Failure modes

- **Real-estate open cabinet reveal**.
- **Open wardrobe showing full wardrobe perfectly organised**.
- **Open drawer showing the inside of a junk drawer as if curated**.

### Prompt-construction implications

Engine must default to closed storage and *justify* every open storage. Openness implies a specific in-progress activity. If the activity isn't specified, the storage is closed.

---

## 6. Life-in-progress clutter

### Psychological principle

A room someone lives in has a baseline level of clutter that is *not* the result of untidiness — it's the result of *life-in-progress*. The bed is unmade because the person is still using the bedroom, not because they are slovenly. The table has crumbs because the person was eating. The desk has stacks because the person is mid-project.

This clutter is *informative* — it tells the viewer about the person's life, habits, and current state. It is also *sparse* — there is usually one cluster of clutter (the active area) and the rest of the space is at baseline. Total chaos is its own kind of staging.

### Visual signature

- One *active* cluster of clutter (desk, kitchen counter, bedside table) where the current activity is happening.
- The rest of the space is at "rest state" — the bed is made elsewhere, the closet is closed elsewhere.
- A "next action" is implied by the clutter: half-paid bills, a half-packed suitcase, a half-read book with the bookmark still in.
- The clutter is in *logical* positions: the desk has the desk clutter, the bedside has the bedside clutter, the kitchen counter has the kitchen clutter. No cross-contamination.

### Failure modes

- **Uniform clutter**: every surface equally messy. This is a "messy room" cliché, not a lived-in room.
- **Clutter with no narrative**: a pile of stuff on the floor that doesn't tell a story.
- **Clutter with no active cluster**: nothing is in the state of being worked on; the whole space is in the same level of disarray.

### Prompt-construction implications

Engine must identify the *one active cluster* and the *baseline* of the rest. The active cluster is in-progress. The baseline is at rest.

---

## 7. Hotel room realism

### Psychological principle

Hotel rooms are a unique case: they are *almost* real and *almost* staged. The bed is made, the towels are folded, the amenities are arranged. But the guest leaves traces — the bed is unmade, a single towel is on the floor, the TV remote is on the bed, a shopping bag is by the door. The contrast between hotel-arranged and guest-trace is what makes a hotel-room frame feel real.

References: Saul Leiter's hotel-room photographs (*In My Room*, 2012, posthumous), which capture the lived-in quality of transient spaces; Todd Hido's *Hotel/Motel* series (2007), which uses the wet-window motif to imply the guest's POV.

### Visual signature

- Hotel-room furniture that has not been re-arranged by the guest (most things in place).
- Guest traces: a single item of clothing, an open suitcase, a half-drunk bottle, the TV on.
- Privacy-residue details: the "Do Not Disturb" sign still on the door, the curtains half-drawn, the safe still open.
- The bed is the central feature: either made-up-hotel-style (just arrived) or guest-unmade (mid-stay).

### Failure modes

- **The "stock hotel" frame**: symmetrical bed, symmetric lamps, no guest traces. This is a real-estate listing, not a stay.
- **The "trashed hotel" frame**: every surface covered, nothing arranged. This is a post-party scene, not a mid-stay scene.

### Prompt-construction implications

Engine must specify the *night number* (1st, 2nd, 3rd) of the stay. The traces differ: night 1 has a fresh unpack, night 3 has a lived-in unmake. The specific night tells the engine what to show.

---

## 8. Bathroom realism

### Psychological principle

Bathrooms are the most-staged, least-real space in most AI generation. The default is the "all products visible" look, which is a beauty-advertising frame, not a bathroom.

Real bathrooms have a small number of *current-use* products and a much larger number of stored products. The visible ones are the ones she used today: the open toothpaste, the wet toothbrush, the towel that was just used. The closed cabinets hide the rest.

References: Roni Horn's *Weather* series (water surfaces) and her bathroom photographs; Peter Hujar's bathroom portraits (*Portraits in Life and Death*, 1976) for the candour.

### Visual signature

- The visible products are the *active* products: open, wet, recently placed.
- The toothbrush is at a specific angle (the user's brushing angle, not a display angle).
- The mirror has *real* smudges and watermarks.
- The towel is in a *used* state: damp, slightly crumpled, on the counter or the floor, not on the rack.
- A single personal item: a hair tie, a razor with a used blade, a contact lens case, a half-finished cup of water.

### Failure modes

- **Beauty counter display**: every product visible, perfectly arranged, mirror clean, towel neatly folded. This is a stock photo.
- **Empty bathroom**: a clean, white, productless bathroom reads as a model home.
- **Product overload**: twenty products visible. This is overcorrection, and reads as a YouTube "what's in my bathroom" video.

### Prompt-construction implications

Engine must specify the *post-shower state* or *pre-shower state* and generate the products implied by that state. Two states: in-use (mid-shower, mid-skincare) and post-use (just finished, drying off).

---

## 9. Shopping bag realism

### Psychological principle

Shopping bags have one of the most distinctive staging signatures: they are *almost always* shown as featured props, perfectly upright, in the centre of the frame. In real life, shopping bags are dropped, kicked, sat on, leaned against things, and partially emptied.

References: André Kertész's *The Day of Paris* (1945) and his later distortion series; Helen Levitt's street photography of New York shopping and errand-running. The bag is incidental in both, not the subject.

### Visual signature

- A shopping bag is *leaning against* something, not standing free.
- The bag is partially open if the user is mid-unpack, closed if the user just got home.
- The contents are not arranged for visibility — they are arranged for *use*.
- The bag is the size and brand that the character would actually carry. A Chanel shopper carried by a 20-something is a different signal than a Muji tote.
- Receipts are sometimes visible, sometimes spilling out, sometimes tucked back in. The bag is rarely pristine.

### Failure modes

- **The "featured bag" frame**: the bag is the subject, perfectly upright, in focus, against a clean background. This is fashion advertising.
- **The "haul video" frame**: multiple bags, all visible, all accessible. This is YouTube content.
- **The "just-bought, just-placed" frame**: the bag is on a clean surface, the contents visible through the opening, the receipt on top. This is product placement.

### Prompt-construction implications

Engine must specify: where the bag is *between* the user's home and the user's most recent destination, what step of unpacking (or non-unpacking) she is in, and what other objects are *not* the bag.

---

## 10. Fitting-room realism

### Psychological principle

Fitting rooms are private spaces that AI tends to render as either fully-staged (clothes arranged on hangers, mirror angled for "outfit of the day" content) or fully-clinical (empty room, single hook). The real fitting room has *try-on residue*: a half-taken-off shirt draped on the bench, a pile of "no" items on the floor, a tag still attached to the "maybe" item, a phone in the user's hand.

### Visual signature

- The "no" pile on the floor or bench: clothes she tried and rejected.
- The "yes" item is being worn, with the tag possibly still on (she hasn't decided yet).
- The mirror shows the current state: an outfit half-on, a back-view being checked, a side-view being assessed.
- Her bag is on the bench or floor, not on a hook.
- The door is closed (this is a fitting room) but the light from outside is visible underneath.

### Failure modes

- **The "OOTD" fitting-room shot**: full outfit, mirror angled for camera, lighting perfect. This is influencer content, not a real fitting room.
- **The empty fitting room**: stock photography of a fitting room with nothing in it.
- **The tag-still-on fashion shot**: the tag is featured as an "unfiltered" detail. Real fitting rooms have tags, but they're not featured.

### Prompt-construction implications

Engine must specify the *try-on decision state*: she is in the middle of deciding on a specific item. The frame captures the indecision, not the decision.

---

## 11. Prop placement psychology

### Psychological principle

"Prop" in photography usually means a small object placed in a frame to imply context — a notebook, a flower, a cup of coffee, a magazine. These are the most heavily-staged objects in any image because they are the ones the photographer or stylist placed deliberately. The engine's hardest job is to make props feel like they were placed by the *character*, not by the photographer.

The trick is to place props in a *use-signature*: the notebook is open to a specific page, with a specific pen on it, in a specific orientation. The flower is in a specific vase, in a specific state (blooming, wilting, fresh-cut). The cup is at a specific angle, in a specific spot on the table, with a specific liquid level.

References: Irving Penn's *Still Life* (1998) and his food photography; Wolfgang Tillmans' "Lutz & Alex" series (1992) for the casual-precise prop placement; Saul Leiter's colour photography for the "found prop" approach.

### Visual signature

- The prop is *used* or *just used*: the book is open, the notebook has writing in it, the magazine has a folded page.
- The prop is in a *non-photogenic* orientation but a *use-significant* orientation: the coffee cup handle is to the user's hand, not to the camera.
- The prop has *siblings* — the coffee cup has a saucer, the book has a bookmark, the pen has a cap.
- The prop is *not* centred or featured. It is on the periphery of the frame, in the depth of field that explains the lens's attention.

### Failure modes

- **The "feature prop" frame**: a single object in the centre, in focus, against a clean background. The most common AI failure mode for prop generation.
- **The "mood prop" frame**: a candle, a flower, a journal — all placed in soft light, all suggesting "wellness". This is a marketing aesthetic, not a real space.
- **The "aspirational prop" frame**: the most expensive, most beautiful, most desirable version of each object.

### Prompt-construction implications

Engine must specify the *use-signature* for every prop. The use-signature is the state the object is in *because of the last person who used it*. If no use-signature is specified, the object is cut.

---

## 12. Casual object entropy

### Psychological principle

Entropy in a real space is *casual* — it is the result of routine, not of any event. The chair is at the angle the person usually leaves it. The pillow is on the side of the couch the person usually sits. The book is at the page the person stopped on. None of this is dramatic; it is just the residue of habit.

Casual entropy is *opposite* to event-driven entropy (the post-party mess, the post-argument mess, the post-move mess). Casual entropy is the *default* state.

References: William Eggleston's *The Democratic Forest* (1989) for the entropy of the American living room; Nan Goldin's *The Ballad of Sexual Dependency* (1986) for the entropy of intimate spaces; Stephen Shore's *Uncommon Places* (1982) for the entropy of the American road.

### Visual signature

- The "default" state of every object: where it usually lives, how it usually sits, what state it is usually in.
- Small drifts from the default (a slightly-pulled-out chair, a half-open drawer) imply recent use.
- No *event* has happened recently. The space is at baseline, with small personal drifts.
- The objects are not in their *best* state. They are in their *most-used* state.

### Failure modes

- **Event entropy**: the room looks like a party happened, an argument happened, a move happened. This is a different genre.
- **Catalog entropy**: every object is in its best, freshest, most-photogenic state. This is a product catalogue.
- **Stage entropy**: the "deliberately messy" look — objects placed at angles for the camera.

### Prompt-construction implications

Engine must specify the *time since last event*. The default is "no event in 24+ hours". The space is at baseline. The small drifts are from normal use, not from any specific incident.

---

## 13. The Object Motivation Engine — production rule set

### Required attributes for every visible object

Every object in the final frame must be assigned the following five attributes. An object missing any attribute is cut.

| Attribute | Definition | Example (coffee cup) |
|---|---|---|
| **Owner** | Whose object is this? | Her (main character) |
| **Purpose** | What is this object for? | Drinking morning coffee |
| **Last Interaction** | When was it last used and by whom? | Used 8 minutes ago by her, mid-sip |
| **Current Resting State** | What state is it in right now? | Half-full, warm, on the nightstand at her-dominant-hand angle, handle facing her |
| **Visibility Reason** | Why is it visible from this camera angle? | It's on the nightstand which is in the foreground depth of the frame |

### Core rules

**R013-01 — Object list audit.** Before rendering, every visible object must have all five attributes assigned. The list is auditable.

**R013-02 — Last-interaction timestamp.** Every object has a "last used" timestamp. The timestamp is plausible for the time of day and the object type. No object is in a state that contradicts its last-use time (no cold coffee in a "5 minutes ago" frame, no warm coffee in a "3 hours ago" frame).

**R013-03 — Default closed.** Storage is closed by default. Open storage requires an in-progress activity to be specified.

**R013-04 — Active cluster mandate.** Exactly one cluster of objects in the frame is in the "active" state (mid-use, mid-action). The rest of the space is at baseline. No uniform clutter.

**R013-05 — Use-signature props.** Every visible prop has a use-signature. No "feature prop" placement. No "mood prop" placement.

**R013-06 — Owner signature.** Every object has an owner. The owner's habits (dominant hand, sleep side, morning routine) are consistent across all objects the owner owns.

**R013-07 — Path of motion.** Objects in motion are mid-motion. Objects at rest are at rest. No object is in a state that contradicts its motion path.

**R013-08 — Visibility justification.** Every visible object can answer "why is this in the frame from this angle". If the answer is "because it looks nice", the object is cut.

**R013-09 — Time-of-day coherence.** All objects in the frame are consistent with the time of day implied by the lighting. No morning light with evening objects, no evening lamp with morning clutter.

**R013-10 — Casual entropy default.** The default state is "no event in 24+ hours". Event-driven entropy requires explicit specification of the event.

**R013-11 — No real-estate angles.** No open-cabinet reveals, no open-wardrobe reveals, no "peek into the bag" beats.

**R013-12 — No catalogue composition.** No "best of" objects only. Real rooms have a mix of best, OK, and slightly-broken. Include at least one *slightly worn* object per active cluster.

**R013-13 — No bilaterally symmetric arrangement.** No two candles flanking a centred object. No matching pairs at equal distances. Object arrangement reflects use, not composition.

**R013-14 — Hotel-room guest traces.** In hotel-room frames, include at least one guest trace per room. In bathroom frames, include at least one post-shower state marker.

**R013-15 — Shopping bag lean rule.** Shopping bags lean against objects, sit on floors, or are held. They do not stand free in the centre of the frame.

---

## 14. Failure-mode checklist (for the verification file)

| # | Failure mode | Detection signal |
|---|---|---|
| F1 | Feature-object syndrome | One of each category, well-composed, filling the frame |
| F2 | Real-estate open storage | Open cabinet showing curated interior |
| F3 | Catalogue composition | All "best of" objects, no wear, no personal items |
| F4 | Bilateral symmetry | Two-of-each, equally weighted, centred |
| F5 | Mood-prop pile-up | Candle + flower + journal, soft light, "wellness" aesthetic |
| F6 | Time-of-day incoherence | Morning light with evening items or vice versa |
| F7 | Uniform clutter | Every surface equally messy |
| F8 | Empty personal space | No photos, no magnets, no personal items in a private space |
| F9 | Upright shopping bag | Bag standing free in centre, fully visible |
| F10 | Hanger-ready clothes | Wardrobe or fitting-room with clothes on hangers, perfectly arranged |
| F11 | Stock fitting room | Empty fitting room, single hook, no try-on residue |
| F12 | OOTD fitting room | Full outfit, mirror angled, no "no" pile on the floor |
| F13 | Hotel-room stock | Made bed, symmetric lamps, no guest traces |
| F14 | Beauty counter bathroom | All products visible, mirror clean, towel folded |
| F15 | Event entropy without event | Room looks post-party, post-argument, post-move with no event specified |

---

## 15. Sources and further reading

1. Gibson, J.J. (1979). *The Ecological Approach to Visual Perception*. Houghton Mifflin.
2. Goffman, E. (1959). *The Presentation of Self in Everyday Life*. Anchor Books.
3. Leiter, S. (2012). *In My Room*. Steidl. (Posthumous.)
4. Hido, T. (2007). *Hotel/Motel*. Nazraeli Press.
5. Penn, I. (1998). *Still Life*. Pace/MacGill Gallery.
6. Tillmans, W. (1992). *Lutz & Alex*. Exhibition catalogue.
7. Eggleston, W. (1989). *The Democratic Forest*. Doubleday.
8. Goldin, N. (1986). *The Ballad of Sexual Dependency*. Aperture.
9. Shore, S. (1982). *Uncommon Places*. Aperture.
10. Hujar, P. (1976). *Portraits in Life and Death*. Da Capo Press.
11. Deakins, R. (interviews, 2010s–2020s). Practical object lighting in cinematography.
12. Haynes, T. (multiple films, 1995–2020s). Period-accurate prop placement.
13. Kertész, A. (1945). *The Day of Paris*.
14. Levitt, H. (1965). *A Way of Seeing*. Viking Press.
15. Mann, S. (1992). *Immediate Family*. Aperture.

---

**End R013 research file.** Companion files: VERIFICATION_R013_OBJECT_MOTIVATION.md, ENGINE_V20_OBJECT_MOTIVATION_SYSTEM.md.
