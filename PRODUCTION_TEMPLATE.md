# Production Template for Densworld Field Sketches

**Ready-to-use prompt formula for Bible mnemonic images**

---

## Generator

**Use ChatGPT (DALL-E)** — produces the best balance of atmospheric murk and object clarity.

Gemini produces more crosshatching (good for texture, but can obscure loci).

---

## The Gold Standard

**The Scavenger's Tunnel** (Image 2 from testing) established these qualities:

- Blue-dark atmospheric dominance
- Lantern light that STOPS rather than illuminates
- Crosshatched void that breathes (the tunnel darkness has texture)
- Figure with presence (pale eyes, hunched, ancient)
- Objects scattered but FINDABLE (bone piles visible, countable)
- The watching element (the darkness behind her knows)

Every image should aim for this balance.

---

## Prompt Formula

```
Densworld field sketch: [LOCATION AND TIME]. [ATMOSPHERIC COLOR] watercolor
wash dominates the [sky/walls/space], with ink line work defining forms.

[SCENE DESCRIPTION — what is happening, who is present, what objects are visible.
Weave specific visual details INTO the scene description naturally. Do NOT
list objects separately or create a "zoomed details" section — this causes
the model to generate segmented images with inset panels.]

[BACKGROUND ELEMENTS — rendered softer, part of atmosphere]

No text, no caption, no border, no signature.
```

### Critical: No Zoom Sections

**DO NOT** include sections like:
- "Zoomed details:"
- "Close-up on:"
- "Detail shots:"

These cause the image model to create segmented compositions with circular inset panels instead of a single coherent scene. Weave all visual details directly into the scene description.

---

## Atmospheric Color by Region

| Region | Primary Atmosphere | Light Behavior |
|--------|-------------------|----------------|
| Yeller Quarry | Amber/rust wash | Amber glow that weighs, presses down |
| Eastern Tunnels | Blue-dark wash | Lantern light that stops at edges |
| The Dens | Gray-purple wash | Sourceless light, no shadows because everything is shadow |
| Denstone edge | Purple-gray bruise | Sick glow where dens meets sky |
| Capital Archive | Dust-yellow/blue-black | Candlelight confined, doesn't spread |
| Tower of Mirado | Steel gray/fountain blue | Light that rejects, anti-illumination |
| Dead River | Green-black | Bioluminescence, water that glows wrong |

---

## Color Variety: Accents and Highlights

While one atmospheric color dominates each image, **add variety through accents**:

### Red Accents
- Rust stains on metal equipment
- Dried blood on bone fragments
- Faded red cloth (tent patches, rope bindings)
- Ember glow from dying fires
- Ochre-red mineral deposits on cave walls

### Yellow Accents
- Lantern flames (small, intense)
- Brass fittings on equipment (spyglass, compass edge)
- Yeller mineral deposits
- Parchment/journal pages catching light
- Sick yellow where bioluminescence fails

### Blue Accents (in warm scenes)
- Steel of blades or tools
- Shadow edges that go cold
- Reflected sky in still water
- Ink on open pages

### Secondary Glow Technique
Add to prompt when appropriate:
```
A secondary [color] glow from [source] picks out [specific objects],
creating contrast against the dominant [atmospheric color].
```

**Example:** "A secondary red glow from dying embers picks out the brass compass and journal spine, creating contrast against the dominant blue-dark."

---

## Watching Elements by Scene Type

Every image needs something that watches or is aware:

| Scene Type | Watching Element |
|------------|------------------|
| Quarry exterior | Five figures on ridge (Yeller) |
| Tunnel interior | The darkness beyond lantern light |
| Dens boundary | The dens itself, through gap or on horizon |
| Denstone | Yeller's shack / five women walking away |
| Archive | The stacks thinking / darkness between shelves |
| Camp/tent | Figures visible through tent flap |

---

## Object Selection Rules

**Each image needs 6 findable objects as mnemonic loci.**

### Good Objects (Clear Silhouettes)
- Lantern (glass and metal frame)
- Boots (distinctive shape)
- Coiled rope
- Open journal/book
- Surveying equipment (tripod, spyglass)
- Compass (circular, readable)
- Canteen/water skin
- Bone piles (countable)
- Crate/box
- Chair/stool
- Mug/cup

### Avoid
- Objects that merge into background
- Too-similar objects (two lanterns, two books)
- Objects used in recent images (check registry)
- Abstract or unclear shapes

### Position Template
```
Foreground left:   [Object 1]
Foreground center: [Object 2]
Foreground right:  [Object 3]
Middle left:       [Object 4]
Middle center:     [Object 5]
Middle right/back: [Object 6]
```

Or for interior scenes:
```
Left side:    [Objects 1-2]
Center:       [Objects 3-4]
Right side:   [Objects 5-6]
```

---

## Example Prompts

### Interior/Cave (Blue-Dark)

```
Densworld field sketch: Deep tunnel in eastern Yeller Quarry. Blue-dark
watercolor wash dominates the cave walls, with ink line work defining
the rock faces. Crosshatching in the deep tunnel mouth suggests a void
that breathes.

The darkness beyond the lantern light is watching. It has texture.

Six objects rendered with clear ink lines, findable within the atmospheric murk:

1. Bone pile — left foreground, yellowed femurs and skull fragments stacked
2. Oil lantern — center, on wooden crate, flame small, light stopping at edges
3. Seated figure — right of center, old woman with pale eyes, hunched
4. Second bone pile — right foreground, smaller, carefully sorted
5. Clay water bowl — near the figure's feet, surface still
6. Tunnel mouth — background center, deeper black than the walls

The cave walls rendered with crosshatch texture. The floor scattered with
smaller bone fragments.

Light source: Single lantern that illuminates only a small circle — beyond
that edge, light simply stops.

No text, no caption, no border, no signature.
```

### Exterior/Ridge (Amber)

```
Densworld field sketch: Ridge at Yeller Quarry at dusk. Amber and rust
watercolor wash dominates the sky, bleeding into gray-purple clouds.
Ink line work defines the rock formations and equipment.

On the far ridge, five women stand in perfect alignment. They are watching.

Six objects rendered with clear ink lines, findable within the atmospheric murk:

1. Surveying tripod — left foreground, brass and wood, sharp silhouette
2. Second tripod with instrument — left of center, slightly behind first
3. Canvas tent — right side, partially visible, darker interior
4. Camp supplies — center ground, crates and folded equipment
5. Coiled rope — foreground right, distinct spiral shape
6. The five figures — far ridge, backlit by amber, silhouettes only

The quarry walls and distant terrain rendered softer, part of the
atmospheric wash. Tents in middle distance merge with the murk.

Light source: Dying amber sun behind the ridge, creating silhouettes.
The figures glow at edges but have no features.

No text, no caption, no border, no signature.
```

### Interior/Tent (Gray-Purple)

```
Densworld field sketch: Interior of expedition tent at dens edge, gray dawn.
Gray-purple watercolor wash dominates the canvas walls, sourceless light
filtering through fabric. Ink lines define the objects within.

Through the tent flap, figures are visible on the dens. The dens are watching.

Six objects rendered with clear ink lines, findable within the atmospheric murk:

1. Wet boots — foreground center, standing upright, BLACK POOL beneath them
2. Camp cot — left side, blankets thrown back, rumpled
3. Wooden crate — beside cot, with tin mug on top
4. Tent pole — center, vertical line anchoring the composition
5. Tent flap opening — right side, showing gray exterior and distant figures
6. Pillow/bedding — on cot, indent where sleeper was

The canvas walls rendered with wash texture, draping folds suggested by
lighter and darker areas.

Light source: Sourceless gray dawn — no sun visible, light simply exists
without origin. The figures outside are darker than the gray should allow.

No text, no caption, no border, no signature.
```

---

## Workflow

1. **Select ore source** from ORE_SOURCES.json
2. **Identify the key moment** with visual potential
3. **Determine region** → atmospheric color
4. **Identify watching element** for this scene
5. **Select 6 objects** appropriate to location (check registry for repeats)
6. **Write prompt** using formula above
7. **Generate in ChatGPT**
8. **Evaluate:** Can you find all 6 loci? Does darkness have texture? Is something watching?
9. **Save image** to appropriate folder
10. **Map loci to verse phrases** — **CRITICAL: Follow LOCUS_PLACEMENT_GUIDE.md exactly**
11. **Update registries** (object registry, region usage)

---

## Locus Assignment (MUST FOLLOW)

**⚠️ ALWAYS consult `LOCUS_PLACEMENT_GUIDE.md` before assigning verse phrases to objects.**

The path schema is a zigzag:

```
┌─────────────────────────────────────────┐
│   (6)            (5)            (4)     │  ← TOP HALF
│  left third    middle third   right third
├─────────────────────────────────────────┤
│   (1)            (2)            (3)     │  ← BOTTOM HALF
│  left third    middle third   right third
└─────────────────────────────────────────┘
```

**Order:** Bottom L→M→R, then Top R→M→L

1. Phrase 1 → Bottom left
2. Phrase 2 → Bottom center
3. Phrase 3 → Bottom right
4. Phrase 4 → Top right
5. Phrase 5 → Top center
6. Phrase 6 → Top left

**Common mistakes to avoid:**
- Confusing "left" and "right" in the top half (the path reverses direction)
- Using vague placement terms like "middle left" — use "bottom left" or "top left"
- Assigning loci before carefully examining where objects actually appear in the generated image

---

## Quality Checklist

Before using an image for mnemonic work:

- [ ] All 6 objects findable within 5 seconds
- [ ] Atmospheric color dominates (not just accents)
- [ ] Something is watching (figures, darkness, the dens)
- [ ] Light behaves wrongly (stops, fails, doesn't illuminate)
- [ ] Crosshatching adds texture without obscuring
- [ ] No text, caption, border, or signature in image
- [ ] No Earth-specific architecture or cultural markers
- [ ] Mood is heavy, murky, aware — not flat or cheerful
- [ ] Loci assigned following LOCUS_PLACEMENT_GUIDE.md zigzag path

---

## Revision Log

| Date | Change |
|------|--------|
| 2025-12-27 | Initial production template based on successful tests |

---

*This template produces Densworld. Use it.*
