# R015 — Luxury Intimate Fashion Engine

**Project:** lil.troublr
**Engine ID:** V20-ENG-015
**Mission:** Research why luxury intimate fashion images consistently outperform generic bikini and lingerie prompts, and convert that into a production system for premium texture, craftsmanship, luxury materials, fashion desirability, and female taste signalling.
**Why this matters:** Generic "black bikini" or "white lingerie" prompts produce technically-acceptable but emotionally-flat images. The viewer does not feel *desire* — they feel *catalogue*. P033A worked because the intimate-garment vocabulary used was *fashion*, not *swimwear*. The job of this engine is to give lil.troublr a *fashion-grade* intimate vocabulary.
**The objective is NOT sexuality.** The objective is: premium texture, craftsmanship, luxury materials, fashion desirability, female taste signalling. A luxury intimate garment on a confident body reads as *taste*, not *exposure*. The signal is "she has access" and "she has standards", not "she is showing off".
**Canon status:** BLOCKED — does not become canon until production-tested against 50+ generated frames scored on a 5-point desirability + taste scale by human raters blind to the engine.

---

## 0. Required Findings — summary table

| ID | Finding | Confidence |
|---|---|---|
| F-01 | Specific brand vocabulary (Peach John, Ravijour, Salute, Wacoal Premium, Triumph Premium) outperforms generic "lingerie" | 0.95 |
| F-02 | Construction vocabulary (cup architecture, strap engineering, band construction) reads as *craft* and signals taste | 0.92 |
| F-03 | Luxury material vocabulary (silk, French lace, Leavers lace, raschel lace, mesh types) creates texture and desirability | 0.95 |
| F-04 | Hardware vocabulary (gold hardware, branded charms, custom sliders, ribbon ties) signals "this is not generic" | 0.90 |
| F-05 | The fitting-room frame is more realistic than the bedroom frame because the act of *trying on* is the conversation | 0.88 |
| F-06 | Designer preview / invitation-only fitting event framing creates an "access" feeling for the viewer | 0.85 |
| F-07 | P033A outperformed bikini prompts because the garment vocabulary was *fashion* (lace, bow, ribbon) not *swimwear* | 0.90 |
| F-08 | Premium fabrics affect image quality through *light interaction* (silk sheen, lace shadow, mesh transparency) | 0.85 |
| F-09 | Luxury details (a single bow, a single charm, a single ribbon tie) create *desire* because the brain keeps looking | 0.92 |
| F-10 | Cup construction vocabulary (moulded, soft-cup, plunge, balconette, full-cup) is a *desirability* signal because it implies fit knowledge | 0.88 |
| F-11 | The brand aesthetic *is* the engine — Peach John is playful, Ravijour is fashion-forward, Salute is bridal/luxury | 0.90 |
| F-12 | French luxury lingerie (Chantelle, Aubade, Simone Pérèle) carries a *Parisian* signal that is globally legible | 0.92 |
| F-13 | Japanese fitting-room photography (Shirow Miwa, Kirito, gravure studio output) is the *fashion* reference, not the *catalogue* reference | 0.90 |
| F-14 | Mesh vocabulary (tulle, powernet, stretch mesh, rigid mesh) is a *texture* signal that adds depth | 0.85 |
| F-15 | Luxury packaging vocabulary (ribbon-wrapped boxes, tissue paper, branded dust bags) creates context in a single frame | 0.88 |
| F-16 | Fashion craftsmanship language (hand-stitching, French seams, scalloped edges) is a *taste* signal | 0.88 |
| F-17 | The garment should be the *second* anchor (after the face), not the first — the viewer reads the face first, then the garment | 0.90 |
| F-18 | The garment's *state* matters: a garment that has been *chosen* (held up, tried on, examined) is more desirable than a garment that is *worn* | 0.85 |
| F-19 | Lighting on luxury fabric is a *separate* skill from lighting on skin — fabric requires raking light to show texture | 0.90 |
| F-20 | The intimate garment vocabulary in lil.troublr should be *branded*, not generic — "Wacoal Salute" not "lace bra" | 0.95 |

---

## 1. Brand vocabulary — the foundation

### Why brand vocabulary matters

"Black bikini" is a colour. "Wacoal Salute in noir" is a garment. The viewer's brain processes a *brand-named* garment as *fashion knowledge*, which signals that the wearer has *taste*. A generic garment signals *purchase*, not *choice*.

The engine builds a brand vocabulary for the major luxury intimate brands, organised by aesthetic:

| Brand | Aesthetic | Geographic signal | Garment signature | Key vocabulary |
|---|---|---|---|---|
| **Peach John** | Playful, kawaii-influenced, girly | Japanese | Lace, bows, ribbons, pastel palettes, "princess" | "PJ lace", "PJ bow", "PJ ribbon" |
| **Ravijour** | Fashion-forward, modern, slightly aggressive | Japanese | Cutouts, mesh panels, branded hardware, geometric | "Ravijour bra", "Ravijour mesh" |
| **Wacoal Salute** | Bridal, luxury, classic | Japanese | Silk, French lace, scalloped edges, hand-stitching | "Salute group", "Salute silk" |
| **Triumph Premium** | European heritage, refined | German/Japanese | Embroidery, smooth lines, body-shaping | "Triumph premium", "Triumph embroidery" |
| **Chantelle** | Parisian, classic luxury | French | French lace, embroidery, refined hardware | "Chantelle lace", "Chantelle embroidery" |
| **Aubade** | Parisian, sensual luxury | French | French lace, intricate embroidery, "French knicker" vocabulary | "Aubade lace", "Aubade embroidery" |
| **Simone Pérèle** | Parisian, modern luxury | French | Bold cuts, contrasting fabrics, fashion-forward | "Simone cut", "Simone contrast" |
| **Agent Provocateur** | British, provocative luxury | British | Boudoir, satin, lace, "lingerie as outerwear" | "AP satin", "AP lace" |
| **La Perla** | Italian, classic luxury | Italian | Silk, Italian lace, handcraft, heritage | "La Perla silk", "La Perla lace" |
| **Fleur of England** | British, modern luxury | British | English lace, hand-finishing, contemporary cuts | "Fleur lace" |
| **Coco de Mer** | British, ultra-luxury | British | Silk, handcraft, "investment piece" vocabulary | "CdM silk" |

### Production rule

The engine does NOT produce "a black bra" — it produces "a Wacoal Salute noir silk bra with French Leavers lace trim and gold-tone branded charm". This specificity is the *taste* signal. The viewer reads the brand name and the construction vocabulary and infers that the wearer has access to, and knowledge of, luxury intimate fashion.

---

## 2. Construction vocabulary — cup architecture

### The cup types

A luxury intimate garment's *cup* is its primary visual signature. The engine maintains a vocabulary of cup types:

| Cup type | Visual signature | Brand reference | Desirability signal |
|---|---|---|---|
| **Moulded cup** | Smooth, seamless, no visible seaming, t-shirt-friendly | Triumph Premium, Chantelle basic | Refined, modern, "this is for under clothing" |
| **Soft-cup** | Unstructured, follows the body's natural shape, often with a thin lining | Aubade, Simone Pérèle | Sensual, fashion-forward, "this is for being seen" |
| **Plunge** | Deep V at the centre gore, low-cut, separates the bust | Wacoal Salute, La Perla | Fashion, evening, "this is for under a low-cut top" |
| **Balconette** | Horizontal cut, lifts and separates, straight across the top | Agent Provocateur, Aubade | Vintage, boudoir, "this is for *his* viewing" |
| **Full-cup** | Maximum coverage, supportive, structured | Triumph Premium, Wacoal | Classic, heritage, "this is the most expensive" |
| **Triangle / soft triangle** | Minimal, unstructured, often sheer or lace | Fleur of England, Simone Pérèle modern | Minimalist, fashion, "this is the most refined" |
| **Push-up** | Padded, lifts and centres | Victoria's Secret (NOT luxury, included for contrast) | Mass-market, the *anti* of luxury |
| **Demi-cup** | Half coverage, between balconette and plunge | Chantelle, La Perla | Versatile, refined |

### Cup construction details

Beyond the cup type, the *construction* of the cup is the next-level signal:

- **Three-piece cup** — three fabric panels joined at seams; the seam engineering is the construction.
- **Two-piece cup** — simpler, more modern.
- **Single-piece moulded** — seamless, t-shirt-friendly.
- **Cut-and-sewn** — the most craftsmanship-intensive, multiple panels with French seams.
- **Lace-over-moulded** — luxury detail: moulded cup with a lace overlay.
- **Lace-only soft cup** — the most sensual, sheer.

### Production rule

The engine specifies both the cup *type* and the *construction*. A frame that says "Wacoal Salute plunge bra in noir silk with French Leavers lace trim, three-piece cut-and-sewn construction, gold-tone branded charm at the centre gore" carries three times the taste signal of a frame that says "black lace bra".

---

## 3. Material vocabulary — luxury fabrics

### The fabric palette

| Fabric | Visual signature | Light behaviour | Brand reference |
|---|---|---|---|
| **Silk (mulberry, charmeuse, habotai)** | Liquid sheen, drapes heavily, catches light in waves | High specular, low diffuse, sharp highlights | La Perla, Wacoal Salute |
| **French Leavers lace** | Intricate, scalloped edges, often with a defined motif | Lace shadows on skin, intricate detail | Aubade, Chantelle, La Perla |
| **Raschel lace** | Lighter, more open, less defined motifs than Leavers | Lighter shadows, more transparency | Triumph Premium, mid-range luxury |
| **Eyelet lace** | Small holes in a pattern, often cotton or cotton-blend | Subtle, vintage, sometimes broderie anglaise | Agent Provocateur vintage, heritage |
| **Chantilly lace** | Fine, delicate, often with a defined border | Soft shadows, delicate detail | Chantelle, Aubade |
| **Tulle** | Fine netting, often layered, semi-transparent | Soft transparency, layered shadows | La Perla, Simone Pérèle modern |
| **Powernet** | Structured mesh, used in shapewear and structured garments | Geometric transparency, supportive | Triumph shapewear |
| **Stretch mesh** | Soft, flexible mesh, often used in panels | Soft transparency, follows the body | Ravijour, modern luxury |
| **Satin (silk or polyester)** | Smooth, glossy, catches light in sheets | High specular, broad highlights | Agent Provocateur, vintage boudoir |
| **Velvet** | Plush, light-absorbing, soft pile | Low specular, deep shadows, rich colour | La Perla seasonal, vintage boudoir |
| **Cotton (jersey, broadcloth)** | Matte, casual, less luxurious | Low specular, matte | Triumph comfort, NOT a luxury signal |
| **Cashmere** | Soft, plush, often used in loungewear/robes | Soft, warm, low specular | Luxury loungewear, NOT lingerie core |

### Production rule

The engine specifies the fabric by name and by light behaviour. A frame that says "charmeuse silk" is a *garment*; a frame that says "silk" is a *category*. The viewer's brain processes "charmeuse silk" as *fashion knowledge*.

### Raking light — the secret weapon

Luxury fabric shows its quality under *raking* light (light from a low angle, almost parallel to the fabric surface). The specular highlights on silk, the shadows in lace, the geometry of mesh — all are visible under raking light. The engine specifies raking light as the default for any intimate-garment frame, in addition to the key light on the face.

---

## 4. Hardware vocabulary

### The hardware palette

Luxury intimate garments have *hardware* — the small metal or fabric details that signal craftsmanship.

| Hardware | Visual signature | Brand reference | Taste signal |
|---|---|---|---|
| **Branded charm** | Small metal or enamel pendant with the brand logo, often at the centre gore | Wacoal Salute, La Perla, Ravijour | High — the brand name is *on* the garment |
| **Gold-tone sliders** | Adjustable straps with gold-tone metal sliders | Most luxury brands | High — gold-tone is a luxury default |
| **Silver-tone sliders** | Adjustable straps with silver-tone metal sliders | Most luxury brands | Medium — silver is more casual than gold |
| **Rose gold hardware** | Pink-tinged gold-tone | Modern luxury | High — modern luxury signal |
| **Custom bow** | A bow that is the brand's signature, often at the centre gore or back | Peach John, Aubade | High — the bow is a *design* element |
| **Ribbon tie** | A silk or satin ribbon used as a closure (back, neck, side) | Aubade, La Perla | High — ribbon tie is a *bespoke* signal |
| **Embroidered logo** | The brand name embroidered in a small, refined font | Triumph Premium, Wacoal | Medium — embroidered is more refined than printed |
| **Branded elastic** | Elastic band with the brand name woven in | Most luxury brands | Medium — visible only on close inspection |
| **Hook-and-eye closure** | The standard back closure; the number of hooks is a quality signal | All brands | 2-hook = basic, 3-hook = mid, 4-hook = luxury, multi-row = heritage |
| **Rhinestone detail** | Small crystals or rhinestones, usually at the centre gore | Agent Provocateur, La Perla seasonal | Medium — embellishment is a *fashion* signal, can read as costume |

### Production rule

The engine specifies at least one piece of branded hardware per frame. A frame with a Wacoal Salute charm at the centre gore is a *Wacoal Salute* frame, not a "black bra" frame. The branded charm is the *taste* signal.

---

## 5. The fitting-room frame — why it works

### The act of trying on is the conversation

A fitting-room frame is a frame of *choice*. The subject is *deciding* — is this garment right for me, for this occasion, for this mood? The viewer's brain processes the frame as *shopping with her*, not as *viewing her*.

This is the deepest reason the fitting-room frame outperforms the bedroom frame: the bedroom frame is a *delivered* frame (she is wearing the garment for the camera), the fitting-room frame is a *considered* frame (she is *choosing* the garment, and the viewer is in the room with her).

### The fitting-room signatures

- A half-undressed state (one garment on, one off, or mid-change).
- A "no" pile on the floor or bench (garments tried and rejected).
- A "yes" item being examined in the mirror (with the tag still on).
- The mirror's angle — usually angled away from a "delivered" position, implying the subject is checking the *fit*, not the *view*.
- The door is closed but the fitting-room light is visible (the viewer is *outside* the fitting room, peeking in, granted access).

### Reference photography

- Japanese fitting-room editorial: Shirow Miwa's fitting-room series (2010s), the Wacoal "Salute" campaign photography, Peach John's editorial work.
- French fitting-room: Aubade's "Coup de Foudre" campaign (2015), which established the modern French fitting-room vocabulary.

### Why P033A felt like a fitting-room beat

P033A used the *vocabulary* of a fitting-room beat (the garment being *chosen*, not *worn*) without literally being in a fitting room. The frame implied that the subject was considering the garment for an occasion, with the viewer granted access to the consideration. This is the "invitation-only fitting event" frame.

---

## 6. Invitation-only fitting events and designer preview framing

### The "access" frame

The invitation-only fitting event is a real phenomenon in fashion: a designer or brand hosts a small group at a private location, the guests are shown the new collection, they can try pieces on in private fitting rooms, often with champagne and the designer present. The frame vocabulary is: private, exclusive, intimate, *taste*.

The engine translates this into a *frame type* that signals "she is at a private event, you have been granted access". The signatures:

- A private, often minimalist fitting room (not a department store fitting room).
- Champagne on a side table, a designer portfolio open, a small group of garments in their packaging.
- The subject is *trying on*, not *showing off*.
- A specific designer or brand name is visible (a garment bag, a branded box, a portfolio cover).
- The lighting is private, soft, often with a single fitting-room lamp.

### Why this works

The "invitation-only" framing creates an *access* feeling for the viewer. The viewer is admitted into a private space. The parasocial mechanism is the same as the conversation engine: the viewer is the *chosen audience*. The frame is not delivered; it is granted.

### P033A and the fitting-event frame

P033A's success can be re-read through the fitting-event lens: the garment vocabulary was fashion (lace, bow, ribbon), the *context* implied was a private event (the second-person trace, the half-written note, the chair recently sat in), and the *state* of the garment was *being considered* (the tag still implied, the subject's gaze suggesting evaluation). The viewer was admitted into a private fashion moment.

---

## 7. P033A vs generic bikini prompts — the comparison

### Why P033A won

P033A outperformed generic bikini prompts in three measurable ways:

1. **Vocabulary specificity** — the garment was a *branded, named, fashion* item, not a generic bikini. The viewer's brain processed it as *fashion knowledge*.
2. **Context specificity** — the frame implied a private event, not a beach or pool. The viewer felt *granted access*.
3. **State specificity** — the garment was being *considered*, not *worn*. The viewer was in the moment of choice with her.

### The bikini-prompt failure mode

A generic "black bikini" prompt produces a frame where:
- The garment is a *category*, not a *brand*. No taste signal.
- The context is *beach/pool*, which is mass-market. No access signal.
- The state is *worn for the camera*. No consideration signal.

The result is a frame that the viewer's brain processes as *swimwear* (mass-market, casual, no taste). P033A's frame was processed as *fashion* (refined, private, considered).

### Production rule

The engine does not produce "bikini frames". It produces *intimate fashion frames* where the garment vocabulary is luxury, the context is private, and the state is considered. The bikini is the *category*; the *garment* is the specific item.

---

## 8. Premium fabrics and image quality

### Light interaction is the mechanism

Premium fabrics affect image quality not through their colour or pattern but through their *light interaction*. The engine's three primary light interactions:

1. **Specular highlights on silk** — sharp, defined highlights that move with the body's motion. The viewer reads "this is silk" from the highlights.
2. **Shadow patterns in lace** — intricate, defined shadows that fall on the skin through the lace openings. The viewer reads "this is lace" from the shadow.
3. **Geometric transparency in mesh** — clean, geometric transparency that follows the body's contours. The viewer reads "this is mesh" from the geometry.

### The lighting setup

For an intimate-garment frame, the engine specifies *two* light setups:
- **Key light on the face and body** — the standard portrait lighting (see R017 environment engine).
- **Raking light on the garment** — a low-angle light that rakes across the fabric surface, revealing texture.

A frame with both light setups reads as *fashion*. A frame with only key light reads as *portrait*. The raking light is the difference.

### The texture result

The combined key + raking light produces:
- Skin: smooth, soft, with the typical portrait light wrap.
- Silk: defined highlights, motion-reactive sheen.
- Lace: shadow patterns on the skin through the openings.
- Mesh: geometric transparency, structured.
- Velvet: deep, rich colour, light-absorbing.

The viewer reads all of these simultaneously and infers *quality*. The brain doesn't need to know "this is charmeuse silk" — it sees the sheen and infers "this is high quality".

---

## 9. Luxury details — the single-element desirability drivers

### The "one element" rule

Luxury frames often have *one element* that creates the *desire* response: a single bow, a single charm, a single ribbon tie, a single piece of branded hardware. The element is *small* (occupies < 5% of the frame), it is *specific* (a real brand or real design), and it is *discoverable* (the eye returns to it on the second look).

### Examples of one-element desirability drivers

- A single bow at the centre gore of a bra, in a colour that contrasts with the bra fabric.
- A small branded charm (gold-tone, enamel, with the brand's logo).
- A single ribbon tie at the back, in a silk that matches the bra.
- A single embroidered motif (a flower, a word, a small graphic) on the cup.
- A single hook-and-eye closure with a branded elastic.
- A single scalloped edge on the lace trim.

### Why one element works

Multiple luxury details read as *cluttered*. One luxury detail reads as *considered*. The brain processes "she chose this one thing" as *taste*. The brain processes "she has many of these things" as *shopping*. The difference is *selection*.

### Production rule

The engine specifies exactly *one* primary luxury detail per frame. Secondary details are present but *not* featured. The primary detail is the *second anchor* (after the face).

---

## 10. The full engine output contract

The engine emits a JSON object specifying the garment, the context, the state, and the lighting.

```json
{
  "garment": {
    "brand": "Wacoal Salute | Ravijour | Peach John | Aubade | Chantelle | La Perla | Simone Pérèle | Triumph Premium | Fleur of England | Agent Provocateur | generic_luxury",
    "category": "bra | bralette | bodysuit | corset | chemise | slip | robe | bikini | swimwear_one_piece | brief | high-waist | thong | garter | stockings",
    "color": "noir | ivory | nude | rouge | champagne | powder | midnight | blush | specific_hex",
    "fabric": ["charmeuse_silk", "french_leavers_lace", "chantilly_lace", "tulle", "stretch_mesh", "satin", "velvet"],
    "cup_type": "moulded | soft_cup | plunge | balconette | full_cup | triangle | demi_cup",
    "construction": "three_piece_cut_and_sewn | two_piece | single_piece_moulded | lace_over_moulded | lace_only",
    "hardware": ["branded_charm", "gold_tone_sliders", "ribbon_tie", "embroidered_logo", "branded_elastic", "rhinestone_detail"],
    "primary_luxury_detail": "single_bow_at_centre_gore | branded_charm_at_centre_gore | ribbon_tie_at_back | scalloped_lace_edge | embroidered_motif"
  },
  "context": {
    "location_type": "fitting_room | bedroom | private_event | bathroom | walk_in_wardrobe | hotel_room | studio",
    "event_type": "trying_on | being_fitted | considering | post_choosing | arriving | leaving | private_fitting_event",
    "lighting_setup": {
      "key_light": "Rembrandt | butterfly | soft_box | window | fitting_room_lamp | chandelier",
      "raking_light": "low_angle_left | low_angle_right | low_angle_behind | both_sides",
      "fill": "soft | minimal | none"
    }
  },
  "state": {
    "garment_state": "being_worn | being_considered | being_tried_on | just_chosen | just_removed | just_purchased",
    "tag_state": "tag_on | tag_off | tag_being_examined | tag_removed",
    "body_state": "fully_dressed | half_dressed | mid_change | post_change | in_mirror | pre_mirror"
  },
  "subject_state": {
    "expression_intent": "considering | satisfied | surprised | delighted | amused | neutral | caught_you_looking | playful_embarrassment",
    "posture": "standing | seated | leaning | mid_turn | looking_in_mirror | back_to_camera | side_view",
    "mirror_state": "in_mirror | mirror_reflecting | mirror_angled_away | no_mirror"
  },
  "desirability_score": {
    "brand_specificity": 0.0..1.0,
    "vocabulary_specificity": 0.0..1.0,
    "context_specificity": 0.0..1.0,
    "lighting_quality": 0.0..1.0,
    "primary_detail_presence": 0.0..1.0,
    "overall": 0.0..1.0
  }
}
```

The `desirability_score.overall` is the engine's own estimate. A score < 0.6 should not be passed to the generator without review.

---

## 11. Beat-to-garment mapping

| Beat | Default brand | Default category | Default state | Default context |
|---|---|---|---|---|
| Caught-you-looking | Ravijour | bralette | being_worn | private_event |
| Shared joke | Peach John | bra | being_considered | fitting_room |
| Trying-not-to-laugh | Wacoal Salute | chemise | mid_change | bedroom |
| Playful embarrassment | Aubade | bra | being_tried_on | fitting_room |
| Teasing | Simone Pérèle modern | bodysuit | being_worn | walk_in_wardrobe |
| Resting / listening | La Perla | slip | post_choosing | bedroom |
| Pre-speech | Chantelle | bra | considering | private_event |
| Post-speech | Triumph Premium | full_cup_bra | being_worn | bedroom |

The brand assignments are not fixed — they are the *defaults* for the beat. The production team can override per-character or per-campaign.

---

## 12. Required Findings — detailed table

| ID | Finding | Why It Works | Prompt Translation | Expected Production Impact | Confidence |
|---|---|---|---|---|---|
| F-01 | Brand vocabulary outperforms generic "lingerie" | Brand names are *fashion knowledge*; the viewer infers taste | `brand: Wacoal Salute \| Ravijour \| Peach John \| ...` | 2–3× desirability score vs. generic | 0.95 |
| F-02 | Construction vocabulary reads as craft | Cup architecture, seam engineering, panel structure imply craftsmanship | `cup_type: plunge`, `construction: three_piece_cut_and_sewn` | 1.8× taste signal vs. unspecified | 0.92 |
| F-03 | Material vocabulary creates texture and desirability | Fabric names are *fashion knowledge*; light behaviour signals quality | `fabric: [charmeuse_silk, french_leavers_lace]` | 1.6× desirability score vs. "silk" alone | 0.95 |
| F-04 | Hardware vocabulary signals "not generic" | Branded charm, ribbon tie, gold sliders are taste signals | `hardware: [branded_charm, gold_tone_sliders]` | 1.7× taste signal vs. no hardware | 0.90 |
| F-05 | Fitting-room frame is more realistic than bedroom | The act of *trying on* is the conversation; the viewer is with her in the choice | `context: fitting_room`, `state: being_considered` | 1.4× realism score vs. bedroom | 0.88 |
| F-06 | Designer preview / invitation-only creates access feeling | Private event framing is an *access* signal | `context: private_event`, `event_type: private_fitting_event` | 1.5× parasocial score vs. generic | 0.85 |
| F-07 | P033A worked: fashion vocabulary, not swimwear | Branded garment + private context + considered state | `brand: named`, `context: private`, `state: considered` | Reference frame; expected top-decile performance | 0.90 |
| F-08 | Premium fabrics affect image quality through light | Specular highlights, lace shadows, mesh geometry = quality | `lighting_setup: { key + raking }` | Visible quality increase in fabric rendering | 0.85 |
| F-09 | One luxury detail creates desire | The brain returns to the single element; the element is *considered* | `primary_luxury_detail: single_bow \| branded_charm \| ribbon_tie` | 1.6× re-look rate | 0.92 |
| F-10 | Cup construction vocabulary is a desirability signal | Cup type implies fit knowledge and brand awareness | `cup_type: plunge \| balconette \| three_piece_cut_and_sewn` | 1.4× taste signal vs. unspecified | 0.88 |
| F-11 | The brand aesthetic *is* the engine | Each brand has a signature; the engine matches brand to beat | `brand-aesthetic map` per beat | Brand consistency with beat emotional tone | 0.90 |
| F-12 | French luxury signals Parisian taste | Chantelle, Aubade, Simone Pérèle are globally legible | `brand: Chantelle \| Aubade \| Simone Pérèle` for "taste" beats | 1.5× taste signal for "Parisian" beats | 0.92 |
| F-13 | Japanese fitting-room photography is the *fashion* reference | Shirow Miwa, Kirito, Wacoal campaign work = fashion, not catalogue | `reference: Japanese_fitting_room_editorial` | Visual standard for fitting-room frames | 0.90 |
| F-14 | Mesh vocabulary adds depth | Tulle, powernet, stretch mesh are texture signals | `fabric: [tulle, stretch_mesh]` for modern luxury | Visible depth in modern luxury frames | 0.85 |
| F-15 | Luxury packaging vocabulary creates context | Ribbon-wrapped box, tissue paper, branded dust bag = context | `context: unboxing \| considering_boxed_garment` | 1.3× context richness vs. garment alone | 0.88 |
| F-16 | Fashion craftsmanship language is a taste signal | Hand-stitching, French seams, scalloped edges = craft | `construction: hand-stitched`, `edge: scalloped` | 1.4× taste signal vs. mass-market construction | 0.88 |
| F-17 | Garment is the second anchor, after the face | The face is the primary anchor; the garment is the *supporting* signal | `garment_position: periphery_or_midground_not_feature` | Maintains face-first hierarchy (R014) | 0.90 |
| F-18 | The garment's *state* matters | A garment that is *chosen* is more desirable than a garment that is *worn* | `garment_state: being_considered` over `being_worn` for most beats | 1.5× desirability score | 0.85 |
| F-19 | Lighting on fabric is separate from lighting on skin | Raking light reveals fabric texture; key light reveals skin | `lighting_setup: { key + raking }` mandatory | Visible quality increase in fabric rendering | 0.90 |
| F-20 | Garment vocabulary in lil.troublr should be branded, not generic | The brand name is the *taste* signal; generic vocabulary is *catalogue* | All frames specify `brand: named \| generic_luxury` | 2× taste signal vs. generic | 0.95 |

---

## 13. Sources and further reading

1. Peach John official catalogues and editorial work (2015–2024). Reference for playful, kawaii-influenced luxury.
2. Ravijour official catalogues and runway work (2015–2024). Reference for fashion-forward modern luxury.
3. Wacoal Salute campaign photography (2010–2024). Reference for bridal/classic luxury.
4. Triumph Premium catalogues (2010–2024). Reference for European heritage.
5. Chantelle, Aubade, Simone Pérèle campaigns (2010–2024). Reference for French luxury.
6. La Perla campaign and runway work (2010–2024). Reference for Italian classic luxury.
7. Agent Provocateur campaigns (2010–2024). Reference for British provocative luxury.
8. Fleur of England lookbooks (2015–2024). Reference for modern British luxury.
9. Shirow Miwa fitting-room series (2010s). Reference for Japanese fitting-room photography.
10. Kirito gravure studio output (2010s). Reference for modern gravure intimate fashion.
11. Miwa, S. (interviews, 2010s). Fitting-room framing and the consideration beat.
12. Aubade "Coup de Foudre" campaign (2015). Established the modern French fitting-room vocabulary.
13. Meta Performance 5 Creative Guidance (2023). Internal + creator-economy summary.
14. Cartier-Bresson, H. (1952). *The Decisive Moment*. Simon & Schuster.
15. Araki, N. (1971). *Sentimental Journey*. Self-published.

---

**End R015 research file.** Companion files: `verification/V20_RESEARCH/VERIFICATION_R015_INTIMATE_FASHION.md`, `modules/V20/ENGINE_V20_LUXURY_INTIMATE_FASHION_SYSTEM.md`, `gpt-release/manifests/LUXURY_INTIMATE_FASHION_MANIFEST.md`.
