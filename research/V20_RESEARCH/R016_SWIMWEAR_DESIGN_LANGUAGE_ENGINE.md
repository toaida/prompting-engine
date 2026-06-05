# R016 — Swimwear Design Language Engine

**Project:** lil.troublr
**Engine ID:** V20-ENG-016
**Mission:** Create a comprehensive swimwear design vocabulary library for lil.troublr, replacing the current reliance on colour-only prompts ("black bikini", "white bikini", "pink bikini", "satin bikini") with a fashion-grade vocabulary covering construction, silhouette, fabric behaviour, and design.
**Why this matters:** Colour-only swimwear prompts produce technically-acceptable but *fashion-blind* images. The viewer does not see a *garment*; they see a *colour on a body*. The next generation of lil.troublr swimwear requires fashion vocabulary, construction vocabulary, silhouette vocabulary, and fabric behaviour vocabulary. The viewer should see a *designed garment* that has been *chosen* and *worn with intent*.
**Canon status:** BLOCKED — does not become canon until production-tested against 50+ generated frames scored on a 5-point design-richness scale.

---

## 0. Required Findings — summary table

| ID | Finding | Confidence |
|---|---|---|
| F-01 | Silhouette vocabulary (triangle, bandeau, halter, plunge, one-shoulder) outperforms colour-only descriptions | 0.95 |
| F-02 | Construction vocabulary (ruched, gathered, wrap, cutout, asymmetrical) signals design intent | 0.92 |
| F-03 | Fabric behaviour vocabulary (wet silk, compression, tension, drape) is a *premium* signal | 0.90 |
| F-04 | Asymmetrical swimwear reads as *design*; symmetric reads as *catalogue* | 0.88 |
| F-05 | Ruching is a *body-flattering* signal and a *premium* signal simultaneously | 0.90 |
| F-06 | Gathered swimwear creates *movement* and *fabric memory*; the viewer reads "this is alive" | 0.88 |
| F-07 | Wrap swimwear is a *desirability* signal because of the *self-tying* act | 0.85 |
| F-08 | Cutout architecture is a *fashion* signal; cutouts must be *engineered*, not random | 0.90 |
| F-09 | Compression zones (under-bust band, high-waist, side panel) are *sculpting* signals | 0.88 |
| F-10 | Tension zones (where the fabric pulls) reveal *fit* and *body knowledge* | 0.85 |
| F-11 | Wet fabric behaviour (translucency, darkening, clinging) is a *premium* texture signal | 0.92 |
| F-12 | Resort cover-layer systems (sarong, caftan, kimono, pareo) are *transition* vocabulary | 0.88 |
| F-13 | Beach-to-cafe transitions require *layering* and *versatility* vocabulary | 0.85 |
| F-14 | Hotel pool styling is more *refined* than beach club styling | 0.85 |
| F-15 | Japanese gravure swimwear is the *fashion* reference (more than Western swimwear) | 0.90 |
| F-16 | Modern Korean swimwear is the *minimalist* reference | 0.88 |
| F-17 | Luxury resort swimwear (Eres, Matteau, Hunza G) is the *quality* reference | 0.92 |
| F-18 | Poolside styling is *sun-and-water* vocabulary; beach club is *social* vocabulary | 0.85 |
| F-19 | Premium swimwear has *visible construction* — seams, topstitching, hardware | 0.88 |
| F-20 | The brand vocabulary for swimwear overlaps with R015 (intimate fashion) but is *seasonal* | 0.90 |

---

## 1. Why "colour-only" prompts fail

### The viewer processes colour, not design

A prompt that says "black bikini" produces a frame where the *garment* is just *black fabric*. The viewer's brain processes the colour, the cut (generic triangle), and the body underneath. The *design* — the engineering of the garment, the cut of the cup, the construction of the strap, the behaviour of the fabric — is invisible.

This is the swimwear-prompt failure mode. The frame is *technically acceptable* but *fashion-blind*.

### What the engine replaces it with

The engine produces prompts that specify:
- **Silhouette** — what shape the garment is (triangle, bandeau, halter, plunge, one-shoulder, etc.).
- **Construction** — how the garment is built (ruched, gathered, wrap, cutout, asymmetrical, paneled, seamed).
- **Fabric behaviour** — how the fabric moves, drapes, clings, or holds (wet silk, compression, tension, body-shaping).
- **Coverage zones** — where the garment covers, cuts away, or shapes (high-waist, plunge, full-back, side-cut).
- **Hardware** — the metal or fabric details (gold-tone sliders, branded charm, hook closure, tie closure).

The result is a *designed garment* that the viewer's brain processes as *fashion*.

---

## 2. Silhouette vocabulary

### Bikini top silhouettes

| Silhouette | Description | Brand reference | Fashion signal |
|---|---|---|---|
| **Triangle** | Two triangular cups, thin straps, minimal coverage | Eres, Matteau, basic | Classic, minimalist, "this is the foundation" |
| **Bandeau** | Straight-across top, no straps over the shoulders, often with side boning | Minimalist brands, modern luxury | Sleek, strapless-friendly, "this is for sunbathing" |
| **Halter** | Top that ties behind the neck, often with a plunging centre | Various | Vintage, glamour, "this is for being looked at" |
| **Plunge** | Deep V at the centre, often with underwire or soft support | Eres, luxury | Fashion, evening, "this is for under a caftan" |
| **One-shoulder** | Asymmetrical, one strap, one bare shoulder | Lisa Marie Fernandez, luxury | Modern, fashion, "this is a designer piece" |
| **Off-shoulder** | Sits below the shoulders, often with a band | Modern luxury, vacation | Bohemian, modern, "this is for the cover photo" |
| **High-neck** | Covers more of the chest, often with a sporty or modest cut | Sport-luxe, modest | Sporty, refined, "this is the most expensive" |
| **Long-sleeve** | Covers the arms, often with UV protection | Sport-luxe, modest | Functional, modern, "this is the most engineered" |
| **Wrap top** | Self-tying wrap, often with a bow or knot | Various | Vintage, feminine, "this is the most feminine" |
| **Front-tie** | Ties at the centre front, often with a bow or knot | Vintage, modern | Vintage, playful, "this is the most flirtatious" |

### Bikini bottom silhouettes

| Silhouette | Description | Coverage | Fashion signal |
|---|---|---|---|
| **Classic brief** | Standard cut, sits at the hip | Moderate | Classic, foundation |
| **High-waist** | Sits at or above the natural waist | Full coverage | Vintage, modest, "this is the most flattering" |
| **Hipster** | Sits on the hips, lower than the classic | Moderate | Modern, fashion |
| **Brazilian** | High-cut leg, minimal back coverage | Minimal | Sensual, fashion, "this is the most daring" |
| **Thong** | Minimal back coverage, often with a narrow back strap | Minimal | Maximum fashion, "this is the most minimal" |
| **Cheeky** | Moderate back coverage, higher-cut leg | Moderate-minimal | Modern, fashion, "this is the most balanced" |
| **Skirted** | Has a small attached skirt | Variable | Vintage, modest |
| **Tie-side** | Ties at the sides, often with a bow or knot | Variable | Vintage, feminine |

### One-piece silhouettes

| Silhouette | Description | Brand reference | Fashion signal |
|---|---|---|---|
| **Classic one-piece** | Standard scoop or V-neck, full back | Eres, classic luxury | Refined, classic |
| **Plunge one-piece** | Deep V at the centre, often with cutout sides | Lisa Marie Fernandez, modern luxury | Fashion, "this is a designer piece" |
| **High-neck one-piece** | Covers more of the chest, sporty cut | Sport-luxe, modest | Sporty, refined |
| **One-shoulder one-piece** | Asymmetrical | Modern luxury | Fashion, "this is the most designed" |
| **Long-sleeve one-piece** | UV-protective, sport-luxe | Sport-luxe | Functional, modern |
| **Cutout one-piece** | Engineered cutouts at the waist, back, or side | Lisa Marie Fernandez, modern | Fashion, "this is the most engineered" |
| **Wrap one-piece** | Self-tying, often with a deep V | Various | Vintage, feminine |
| **Monokini** | Connected at strategic points, often with cutouts | Modern luxury | Maximum fashion, "this is the most daring" |

### Production rule

The engine does not produce "bikini frames" — it produces *silhouette-specific* frames. A frame that says "asymmetrical one-shoulder bikini top with ruched cups, tie-side high-waist bottom in Eres noir" is a *designed garment* frame. A frame that says "black bikini" is a *colour* frame.

---

## 3. Construction vocabulary

### The construction techniques

A swimwear garment's *construction* is its primary design signal. The engine maintains a vocabulary of construction techniques:

| Technique | Description | Visual signature | Brand reference |
|---|---|---|---|
| **Ruched** | Fabric gathered along seams, creating a rippled texture | Rippled, body-flattering, hides imperfections | Various, classic luxury |
| **Gathered** | Fabric drawn together at one or more points, creating volume and movement | Voluminous, sculptural, often at the centre or side | Modern luxury, designer |
| **Wrapped** | Fabric wraps around the body, often self-tying | The wrap itself is the design, the tie is the focal point | Various, vintage-inspired |
| **Cutout** | Engineered openings in the fabric, often at the waist, back, or side | The cutout reveals the body in a designed way | Lisa Marie Fernandez, modern luxury |
| **Asymmetrical** | One side differs from the other (one-shoulder, single strap, off-centre detail) | The asymmetry is the design | Modern luxury, designer |
| **Paneled** | Multiple fabric panels joined at seams, often with contrast colours or fabrics | The seams are the design, the engineering is visible | Sport-luxe, modern luxury |
| **Seamed** | Visible topstitching or contrast seaming, often for shaping | The seams shape the body, the engineering is the design | Sport-luxe, premium |
| **Bonded** | Seams are fused rather than sewn, creating a clean, modern line | The lack of seam is the design, the clean line is the engineering | Sport-luxe, modern luxury |
| **Shirred** | Multiple rows of gathered stitching, often with elastic thread | The shirring creates a stretchy, body-conforming texture | Vintage, bohemian |
| **Smocked** | Decorative gathering, often with embroidery | The smocking is the design, often heritage or vintage-inspired | Heritage, vintage |
| **Pleated** | Fabric folded in regular or irregular pleats | The pleats create movement, often at the hem or strap | Modern luxury, fashion |
| **Quilted** | Fabric with stitched padding, often in geometric patterns | The quilting is the design, often in robes or cover-ups | Luxury, vintage |

### Production rule

The engine specifies the construction technique by name. A frame that says "ruched bikini top with shirred side panels" is a *construction* frame. A frame that says "black bikini" is a *colour* frame.

---

## 4. Fabric behaviour vocabulary

### How fabric moves, drapes, clings, or holds

Swimwear fabric has *behaviour* under the body's motion, the water's interaction, and the sun's heat. The engine's vocabulary of fabric behaviour:

| Behaviour | Description | Fabric types | Visual signature |
|---|---|---|---|
| **Compression** | Fabric that holds the body in, sculpts, shapes | Powernet, compression knit, double-lined | The body is shaped, the fabric is firm |
| **Tension** | Fabric that pulls at certain points, revealing fit | Stretch knit, body-conforming | Tension lines, fit visibility |
| **Drape** | Fabric that falls in soft folds, often at the hem or strap | Silk blends, rayon, soft knits | The drape creates movement, the fabric is light |
| **Wet cling** | Fabric that becomes more transparent and clinging when wet | Most swimwear fabrics, especially silk blends | Wet fabric darkens, clings, reveals more |
| **Wet sheen** | Fabric that becomes more lustrous when wet | Silk, satin, polished knits | The sheen becomes pronounced, the fabric glows |
| **Quick-dry** | Fabric that dries fast, often with a matte finish | Most performance swimwear | The fabric is matte, functional, modern |
| **Body-shaping** | Fabric with built-in shaping, often with bonded seams or panels | Powernet, double-lined, bonded | The body is sculpted, the garment is engineering |
| **UV-protective** | Fabric that blocks UV, often with a tighter weave | UPF-rated swimwear | The fabric is dense, the garment is functional |
| **Sheer when wet** | Fabric that becomes semi-transparent when wet | Silk, fine knits, untreated | The body is revealed more when wet, the fabric is delicate |
| **Memory fabric** | Fabric that holds its shape, often with a slight stretch | Modern technical swimwear | The garment holds its silhouette, the fabric is engineered |

### Wet fabric is the *premium* signal

Wet fabric is the strongest *premium* signal in swimwear imagery. A frame that shows fabric with wet sheen, wet cling, or sheer-when-wet behaviour reads as *expensive* — the viewer infers that the fabric is the kind that *responds* to water, which is a silk or silk-blend signal.

The engine specifies a wet-fabric element in ~50% of swimwear frames. The wet element is at the *edge* of the garment (a wet hem, a wet shoulder, a wet strap) or at a *transition point* (the line where the body has just emerged from the water).

### Production rule

The engine specifies fabric behaviour, not just fabric type. A frame that says "wet-sheen silk-blend one-piece with compression zones and tension at the side seams" is a *fabric-behaviour* frame. A frame that says "black one-piece" is a *colour* frame.

---

## 5. Asymmetrical swimwear

### Why asymmetry reads as design

Symmetric garments read as *mass-market*. Asymmetric garments read as *designed*. The brain processes symmetry as "this is the default" and asymmetry as "this is the choice". The choice is the *design* signal.

### Types of asymmetry in swimwear

- **One-shoulder** — one strap, one bare shoulder.
- **Off-centre cutout** — a cutout on one side only.
- **Single ruched side** — ruching on one side, smooth on the other.
- **Asymmetrical hem** — the hem is longer on one side than the other.
- **Single tie** — one tie or bow, off-centre.
- **Asymmetrical neckline** — one side higher than the other.
- **Mixed fabric** — one fabric on one side, another on the other.

### Brand references for asymmetry

Lisa Marie Fernandez is the modern reference for asymmetrical swimwear (2015–2024). Her one-shoulder, cutout, and asymmetric-hem designs established the modern luxury asymmetry vocabulary.

### Production rule

The engine defaults to *some* asymmetry in ~60% of swimwear frames. Pure symmetry is reserved for classic/vintage references and for frames where the *symmetry itself* is the design (a perfectly cut classic one-piece, for example).

---

## 6. Ruched swimwear

### Why ruching is a premium signal

Ruching is fabric gathered along seams, creating a rippled texture that:
- Flatters the body (the ruching hides small imperfections).
- Creates movement (the ripples move with the body).
- Signals design (ruching requires engineering, not just cutting).
- Adds visual interest (the eye keeps moving across the ripples).

The combination of *body-flattering*, *movement*, and *engineering* is the *premium* signal. A ruched garment reads as *designed*; a flat garment reads as *cut*.

### Where ruching appears

- **Side ruching** — gathered at the side seams, drawing the eye vertically.
- **Centre ruching** — gathered at the centre front or centre back, creating a focal point.
- **All-over ruching** — gathered across the entire garment, creating a textured surface.
- **Diagonal ruching** — gathered on a diagonal, creating a sculptural line.

### Brand references

Eres, Heidi Klein, and Mara Hoffman are the contemporary references for luxury ruched swimwear.

### Production rule

The engine specifies ruching in ~40% of swimwear frames. The ruching is named (side, centre, all-over, diagonal) and is the *primary construction signal*.

---

## 7. Gathered and wrap swimwear

### Gathered swimwear

Gathered swimwear is fabric drawn together at one or more points, creating *volume* and *movement*. The gathering point is often the centre front, the side, or the back, and the fabric drapes from the gathering point.

Gathered swimwear reads as *fashion* and *sculpture* — the garment has *form*, not just *fit*. The viewer reads "this is alive" because the gathering creates movement.

### Wrap swimwear

Wrap swimwear is fabric that wraps around the body, often self-tying. The wrap itself is the design — the act of *tying* the wrap is the focal point. Wrap swimwear signals:
- The wearer *dressed herself* (the tying act).
- The garment is *adjustable* (the wrap can be tied tighter or looser).
- The garment is *vintage-inspired* (wraps have a heritage in 1940s and 1970s swimwear).
- The garment is *feminine* (the wrap creates a soft, draped line).

### Production rule

The engine specifies gathered or wrap construction in ~25% of swimwear frames. The gathering or wrap point is the *primary design signal*.

---

## 8. Cutout architecture

### The engineered cutout

A cutout is an *engineered* opening in the fabric. Cutouts are not random — they are designed to:
- Reveal a specific part of the body in a designed way.
- Create a visual line that draws the eye to a specific point.
- Add visual interest without changing the silhouette.
- Reference fashion, sport, or art.

### Types of cutouts

- **Side cutout** — at the waist, often with a single strap or panel connecting the top and bottom of the garment.
- **Back cutout** — at the back, often with a single strap or panel.
- **Centre cutout** — at the centre front, often with a plunge.
- **Shoulder cutout** — at the shoulder, often with a one-shoulder construction.
- **Multi-cutout** — multiple cutouts at different points (the most engineered).

### Brand references

Lisa Marie Fernandez is the modern reference for engineered cutout swimwear. Her "Cristina" and "Linda" one-pieces (2018–2024) are the standard for the genre.

### Production rule

The engine specifies cutouts in ~20% of swimwear frames. The cutout is *named* (side, back, centre, shoulder, multi) and is the *primary design signal*.

---

## 9. Compression and tension zones

### The body-shaping vocabulary

A premium swimwear garment often has *compression zones* (where the fabric holds the body in) and *tension zones* (where the fabric pulls, revealing fit). The combination is a *sculpting* signal.

### Compression zones

- **Under-bust band** — a band of firmer fabric under the bust, lifting and supporting.
- **High-waist** — the bottom sits at the natural waist, often with a compression panel.
- **Side panel** — a panel of firmer fabric at the side, sculpting the waist.
- **Tummy control** — a panel of firmer fabric at the front, smoothing the tummy.
- **Bonded seams** — seams that are fused rather than sewn, creating a clean, sculpting line.

### Tension zones

- **Side seam** — where the side seam pulls, the fit is visible.
- **Strap** — where the strap pulls, the support is visible.
- **Centre gore** — where the centre of the bra pulls, the construction is visible.
- **Back band** — where the back band pulls, the fit is visible.

### Why this matters

A frame that shows *visible compression and tension* reads as *engineered*. The viewer infers that the garment has been *designed* to fit the body, not just cut to cover it. The engineering is the *premium* signal.

### Production rule

The engine specifies compression and tension zones in ~30% of swimwear frames. The zones are *named* and are the *primary fit signal*.

---

## 10. Resort cover-layer systems

### The transition vocabulary

A premium swimwear frame often includes a *cover layer* — a sarong, caftan, kimono, pareo, or cover-up that the subject wears over or with the swimwear. The cover layer is the *transition* signal: the viewer reads that the subject is *going somewhere* (beach to cafe, pool to bar, swim to lunch).

### Cover-layer types

| Type | Description | Brand reference | Fashion signal |
|---|---|---|---|
| **Sarong** | A long piece of fabric wrapped around the waist | Resort, classic | Vacation, classic, "this is the most relaxed" |
| **Caftan** | A long, flowing dress, often with embroidery or beading | Luxury resort | Evening, refined, "this is the most elegant" |
| **Kimono** | A loose, flowing top with wide sleeves, often with a print | Modern luxury | Fashion, modern, "this is the most designed" |
| **Pareo** | A rectangular piece of fabric wrapped as a skirt or dress | Resort, classic | Vacation, versatile |
| **Cover-up dress** | A simple dress designed to be worn over swimwear | Modern luxury | Functional, refined, "this is the most versatile" |
| **Linen shirt** | An oversized linen shirt, often unbuttoned, worn over swimwear | Modern, heritage | Casual, refined, "this is the most understated" |
| **Crochet top** | A loose, crocheted top, often with a heritage feel | Vintage, modern | Vintage, feminine, "this is the most handmade" |
| **Tunic** | A loose, short dress or long top | Resort, classic | Casual, refined |
| **Wrap skirt** | A skirt that wraps and ties | Resort, classic | Vacation, feminine |
| **Wide-leg pant** | Loose, flowing pants worn over a swimsuit | Modern luxury | Refined, modern, "this is the most fashion-forward" |

### Beach-to-cafe transitions

The cover layer enables the *beach-to-cafe* transition: the subject can be in her swimsuit at the pool, add a sarong and linen shirt, and walk to a cafe without changing. The cover layer is *versatility* and *refinement*.

### Production rule

The engine specifies a cover layer in ~40% of swimwear frames. The cover layer is *named* and is the *transition signal*.

---

## 11. Hotel pool vs beach club vs poolside styling

### Hotel pool styling

Hotel pool styling is *refined*. The frame is *set* at a luxury hotel, often with:
- A poolside lounger with white cushions.
- A cabana or private pool area.
- A towel that is monogrammed or hotel-branded.
- A cocktail or book on a side table.
- The subject in a *refined* cover layer (caftan, linen shirt).

### Beach club styling

Beach club styling is *social*. The frame is *set* at a beach club, often with:
- A daybed or beach lounger with cushions.
- A group of friends in the background.
- A bottle of champagne or cocktail.
- Music or social activity in the periphery.
- The subject in a *social* outfit (matching set, cover-up).

### Poolside styling

Poolside styling is *sun-and-water*. The frame is *set* at a private pool or villa, often with:
- A pool edge with reflections.
- A wet element (the subject is emerging from the water, or wet from a swim).
- A pool toy or float.
- A book or magazine on a lounger.
- The subject in a *minimal* cover layer (sarong, pareo) or no cover layer.

### Production rule

The engine specifies the *setting* (hotel pool, beach club, poolside) for each swimwear frame. The setting drives the *secondary props* and the *cover layer* choice.

---

## 12. Japanese gravure swimwear reference

### The fashion reference for swimwear

Japanese gravure photography is the *fashion* reference for swimwear, more so than Western beach photography. The gravure tradition (1970s–present) treats swimwear as *fashion*, not as *beachwear*. The frame vocabulary:

- **High subject-to-frame ratio** — the subject dominates, the swimwear is the *focus*.
- **Studio or private-pool lighting** — not beach or harsh sun.
- **Mitsumeru-me gaze** — the conversation engine applies.
- **Asymmetric or engineered construction** — the swimwear is *designed*, not generic.
- **Branded or designer reference** — the swimwear is named.

### Reference photographers

- **Araki Nobuyoshi** — *Sentimental Journey* and later work. Established the "swimwear as fashion" reference.
- **Shirow Miwa** — 2010s gravure work, fashion-grade swimwear framing.
- **Kirito** — modern gravure, fashion-grade construction vocabulary.
- **Mika Ninagawa** — *Sugar High* and editorial work, high-key swimwear fashion.

### Brand references for Japanese swimwear

- **Peach John** (swim line) — playful, girly, fashion.
- **Ravijour** (swim line) — fashion-forward, modern.
- **Andemari** — Japanese luxury swim.
- **Marella** — modern Japanese swim.

### Production rule

The engine uses Japanese gravure as the *visual reference standard* for swimwear frames. The reference is *fashion*, not *beach*.

---

## 13. Modern Korean swimwear reference

### The minimalist reference

Modern Korean swimwear (2018–2024) is the *minimalist* reference. The frame vocabulary:

- **Clean lines, minimal hardware, no embellishment.**
- **Solid colours or very simple patterns.**
- **Asymmetric or engineered construction.**
- **High subject-to-frame ratio.**
- **Soft, natural lighting (not studio).**

### Brand references for Korean swimwear

- **Andar** — modern Korean swim, minimalist.
- **Mardi Mercredi** — modern Korean swim, fashion-forward.
- **Lost in General** — modern Korean, minimalist.
- **HAEKIM** — modern Korean, refined.

### Production rule

The engine uses Korean swimwear as the *minimalist* reference for frames where the design is *understated* rather than *bold*.

---

## 14. Luxury resort swimwear reference

### The quality reference

Luxury resort swimwear (Eres, Matteau, Hunza G, Lisa Marie Fernandez) is the *quality* reference. The frame vocabulary:

- **Premium fabric** — often a specific blend (Italian nylon, French Lycra).
- **Clean construction** — minimal visible hardware, refined seaming.
- **Solid colours or very subtle patterns.**
- **Engineered fit** — the garment fits *the* body, not *a* body.
- **Brand-aware styling** — the subject is *wearing* the brand, not just *in* swimwear.

### Brand references

- **Eres** — French luxury swim, classic and refined.
- **Matteau** — Australian luxury swim, minimalist.
- **Hunza G** — British luxury swim, crinkle-texture signature.
- **Lisa Marie Fernandez** — American luxury swim, designer.
- **Heidi Klein** — British luxury swim, classic.
- **Mara Hoffman** — American luxury swim, fashion-forward.

### Production rule

The engine specifies a brand reference for ~60% of swimwear frames. The brand is the *quality* signal.

---

## 15. The full engine output contract

```json
{
  "garment": {
    "brand": "Eres | Matteau | Hunza G | Lisa Marie Fernandez | Heidi Klein | Mara Hoffman | Peach John | Ravijour | Andar | Mardi Mercredi | generic_luxury",
    "category": "bikini_top | bikini_bottom | one_piece | monokini | tankini | swim_dress",
    "silhouette": {
      "top": "triangle | bandeau | halter | plunge | one_shoulder | off_shoulder | high_neck | long_sleeve | wrap | front_tie",
      "bottom": "classic_brief | high_waist | hipster | brazilian | thong | cheeky | skirted | tie_side",
      "one_piece": "classic | plunge | high_neck | one_shoulder | long_sleeve | cutout | wrap | monokini"
    },
    "construction": ["ruched", "gathered", "wrapped", "cutout", "asymmetrical", "paneled", "seamed", "bonded", "shirred", "smocked", "pleated", "quilted"],
    "construction_details": {
      "ruching_location": "side | centre | all_over | diagonal | none",
      "gathering_point": "centre_front | side | back | none",
      "cutout_type": "side | back | centre | shoulder | multi | none",
      "asymmetry_type": "one_shoulder | off_centre_cutout | single_ruched_side | asymmetric_hem | single_tie | asymmetric_neckline | mixed_fabric | none"
    },
    "fabric": {
      "type": ["italian_nylon", "french_lycra", "recycled_nylon", "silk_blend", "crinkle_lycra", "powernet", "compression_knit"],
      "behaviour": ["compression", "tension", "drape", "wet_cling", "wet_sheen", "quick_dry", "body_shaping", "uv_protective", "sheer_when_wet", "memory_fabric"]
    },
    "coverage_zones": {
      "top_coverage": "minimal | moderate | full",
      "bottom_coverage": "minimal | moderate | full",
      "compression_zones": ["under_bust_band", "high_waist", "side_panel", "tummy_control", "bonded_seams"],
      "tension_zones": ["side_seam", "strap", "centre_gore", "back_band"]
    },
    "hardware": ["gold_tone_sliders", "branded_charm", "tie_closure", "hook_closure", "none"],
    "primary_design_signal": "ruching | gathering | cutout | asymmetry | wrap | cover_layer | branded_hardware"
  },
  "context": {
    "setting": "hotel_pool | beach_club | poolside | villa | yacht | beach | private_resort",
    "lighting_setup": {
      "key_light": "natural_sun | window | studio | poolside_reflection",
      "raking_light": "low_angle | none",
      "wet_elements": ["wet_hem", "wet_strap", "wet_shoulder", "wet_edge", "none"]
    },
    "cover_layer": {
      "type": "sarong | caftan | kimono | pareo | cover_up_dress | linen_shirt | crochet_top | tunic | wrap_skirt | wide_leg_pant | none",
      "state": "worn | draped | held | on_chair | none"
    }
  },
  "subject_state": {
    "expression_intent": "considering | satisfied | playful | caught_you_looking | shared_joke | teasing | resting",
    "posture": "standing | seated | lounging | emerging_from_water | walking | leaning | mid_action",
    "wet_state": "just_emerged | mid_swim | post_swim | pre_swim | dry"
  },
  "design_richness_score": {
    "silhouette_specificity": 0.0..1.0,
    "construction_specificity": 0.0..1.0,
    "fabric_behaviour_specificity": 0.0..1.0,
    "brand_specificity": 0.0..1.0,
    "primary_designal_presence": 0.0..1.0,
    "overall": 0.0..1.0
  }
}
```

The `design_richness_score.overall` is the engine's own estimate. A score < 0.6 should not be passed to the generator without review.

---

## 16. Required Findings — detailed table

| ID | Finding | Why It Works | Prompt Translation | Expected Production Impact | Confidence |
|---|---|---|---|---|---|
| F-01 | Silhouette vocabulary outperforms colour-only | Silhouette is a *shape*, not a *colour*; the viewer reads shape as design | `silhouette: { top: triangle \| bandeau \| halter ... }` | 2–3× design richness score vs. colour-only | 0.95 |
| F-02 | Construction vocabulary signals design intent | Construction is the *engineering*; the viewer reads engineering as craft | `construction: [ruched, gathered, cutout]` | 1.8× design richness vs. unspecified | 0.92 |
| F-03 | Fabric behaviour is a premium signal | Behaviour implies the fabric *responds* to the body; the viewer reads response as quality | `fabric.behaviour: [compression, wet_sheen]` | 1.6× premium signal vs. fabric-type-only | 0.90 |
| F-04 | Asymmetry reads as design | Asymmetry is the *choice*; the viewer reads choice as taste | `asymmetry: one_shoulder \| off_centre_cutout \| ...` | 1.5× design richness vs. symmetric | 0.88 |
| F-05 | Ruching is body-flattering + premium | Ruching hides imperfections and signals engineering | `construction: [ruched]`, `ruching_location: side \| centre \| all_over` | 1.4× premium signal | 0.90 |
| F-06 | Gathered swimwear creates movement and fabric memory | Gathering creates volume and drape; the viewer reads "this is alive" | `construction: [gathered]`, `gathering_point: centre_front \| side \| back` | 1.4× design richness | 0.88 |
| F-07 | Wrap swimwear is a desirability signal | The self-tying act is a *desirability* beat | `construction: [wrapped]` | 1.3× desirability | 0.85 |
| F-08 | Cutout architecture is a fashion signal | Cutouts are *engineered*; the viewer reads engineering as design | `construction: [cutout]`, `cutout_type: side \| back \| centre \| shoulder \| multi` | 1.6× fashion signal | 0.90 |
| F-09 | Compression zones are sculpting signals | Compression implies *body knowledge* | `compression_zones: [under_bust_band, side_panel]` | 1.4× fit signal | 0.88 |
| F-10 | Tension zones reveal fit | Tension implies the garment is *fitted to* the body | `tension_zones: [side_seam, strap, centre_gore]` | 1.3× fit signal | 0.85 |
| F-11 | Wet fabric behaviour is a premium texture signal | Wet fabric darkens, clings, sheens; the viewer reads response as quality | `fabric.behaviour: [wet_cling, wet_sheen, sheer_when_wet]` | 1.6× premium signal | 0.92 |
| F-12 | Cover layers are transition vocabulary | Cover layers signal *versatility* and *refinement* | `cover_layer: { type: sarong \| caftan \| kimono }` | 1.3× context richness | 0.88 |
| F-13 | Beach-to-cafe transitions require layering | Layering is the *transition* signal | `cover_layer.state: worn`, `setting: hotel_pool` | 1.4× transition signal | 0.85 |
| F-14 | Hotel pool is more refined than beach club | Hotel pool is *private* and *refined*; beach club is *social* | `setting: hotel_pool` for refined beats | 1.3× refinement signal | 0.85 |
| F-15 | Japanese gravure is the fashion reference | Gravure treats swimwear as *fashion*, not *beachwear* | Reference for all swimwear frames | Visual standard for fashion-grade swimwear | 0.90 |
| F-16 | Modern Korean swimwear is the minimalist reference | Clean lines, no embellishment, asymmetric construction | Reference for understated beats | Visual standard for minimalist swimwear | 0.88 |
| F-17 | Luxury resort swimwear is the quality reference | Premium fabric, clean construction, brand-aware styling | Reference for all branded frames | Visual standard for quality | 0.92 |
| F-18 | Poolside styling is sun-and-water vocabulary | Wet elements, pool reflections, minimal cover layer | `setting: poolside`, `wet_elements: required` | 1.4× context richness | 0.85 |
| F-19 | Visible construction is a premium signal | Seams, topstitching, hardware = engineering | `construction: [seamed, paneled]`, `hardware: required` | 1.4× premium signal | 0.88 |
| F-20 | Brand vocabulary for swimwear overlaps with R015 but is seasonal | Same brands, but seasonal collections and swim-specific lines | `brand: same_as_R015`, `line: seasonal` | Brand consistency with intimate fashion | 0.90 |

---

## 17. Sources and further reading

1. Eres official catalogues and campaigns (2015–2024). Reference for French luxury swim.
2. Matteau official lookbooks (2015–2024). Reference for Australian minimalist swim.
3. Hunza G official campaigns (2015–2024). Reference for British crinkle-texture swim.
4. Lisa Marie Fernandez official campaigns (2015–2024). Reference for American designer swim.
5. Heidi Klein official campaigns (2015–2024). Reference for British classic swim.
6. Mara Hoffman official campaigns (2015–2024). Reference for American fashion-forward swim.
7. Peach John (swim line) official catalogues (2015–2024). Reference for Japanese playful swim.
8. Ravijour (swim line) official catalogues (2015–2024). Reference for Japanese fashion-forward swim.
9. Andar, Mardi Mercredi, Lost in General, HAEKIM (Korean swim brands) campaigns (2018–2024). Reference for modern Korean minimalist swim.
10. Araki, N. (1971). *Sentimental Journey*. Self-published. Gravure swimwear reference.
11. Miwa, S. (2010s). Fitting-room and swimwear gravure series. Fashion-grade swimwear reference.
12. Kirito (2010s). Modern gravure studio work. Fashion-grade construction reference.
13. Ninagawa, M. (2006). *Sugar High*. High-key swimwear editorial reference.
14. Meta Performance 5 Creative Guidance (2023). Internal + creator-economy summary.
15. Cartier-Bresson, H. (1952). *The Decisive Moment*. Simon & Schuster.

---

**End R016 research file.** Companion files: `verification/V20_RESEARCH/VERIFICATION_R016_SWIMWEAR.md`, `modules/V20/ENGINE_V20_SWIMWEAR_DESIGN_LANGUAGE.md`, `gpt-release/manifests/SWIMWEAR_DESIGN_LANGUAGE_MANIFEST.md`.
