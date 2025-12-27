# Visual Style Guide for Bible Mnemonic Images

A working guide for generating Densworld images as memory palaces.

---

## Core Principle

The better Densworld comes to life visually on its own terms, the better the images function as mnemonic devices. We are not illustrating Bible verses — we are depicting Densworld scenes that happen to hold Bible text.

---

## Image Types

### 1. Landscape View
Wide exterior scene with objects distributed across terrain.

**When to use:** Default choice. Good for establishing a region's character.

**Structure:**
- Viewer stands at a vantage point looking across the scene
- Three foreground objects (bottom third, left to right)
- Three background objects (top third, right to left)
- Clear spatial separation between all six

**Example regions:** Focal Meadow, Yeller Quarry rim, Dead River banks, Dens moors

---

### 2. Narrative Scene
A moment from an ore fragment with characters and action.

**When to use:** When the ore source has a vivid interpersonal moment.

**Structure:**
- Viewer observes the scene from a specific position
- Objects include character details (a hand, braided hair, a distinctive garment)
- Objects also include environmental elements
- Action is frozen mid-moment

**Example:** The girl-snatcher watching the child in Miasto (bible-001)

---

### 3. Object Interior
Close view of a single large object, with its parts as loci.

**When to use:** When a distinctive Densworld object (vehicle, furniture, device) can carry six distinct parts.

**Structure:**
- Viewer crouches beside or looks into the object
- Parts of the object become the six loci
- Background visible through/around the object anchors the region

**Example:** Interior of an abandoned Oneride flying craft (bible-002)

---

### 4. Architectural Interior
Inside a building or structure, with furnishings and features as loci.

**When to use:** When the ore source describes a specific interior space.

**Structure:**
- Viewer stands in doorway or corner looking across the room
- Furniture, fixtures, and objects distributed across the space
- Windows or openings show exterior context

**Example regions:** Capital Archive reading room, Tower of Mirado chamber, Densmok basement

---

## Prompt Template

```
A unified [interior/exterior] illustration of [location], viewed as if
[vantage point] looking [direction]. [One sentence of atmospheric context.]

In the foreground on the left, [object 1 with specific detail]. Beside it
in the center foreground, [object 2 with specific detail]. To the right
foreground, [object 3 with specific detail].

In the background on the right, [object 4 with specific detail]. At center
back, [object 5 with specific detail]. On the left in the background,
[object 6 with specific detail].

The color palette draws from Densworld materials: [2-4 materials with hex codes].

Cartographic illustration style with clean lines, unified lighting from
top-left, deep focus keeping all elements sharp. One continuous scene,
not separate panels. Six distinct objects clearly separated by negative space.
```

---

## Densworld Color Palette

### Primary Materials
| Material | Hex | Use |
|----------|-----|-----|
| Quarry Ochre | #B45309 | Warm earth, leather, brass |
| Iron Gall Black | #1F2937 | Shadows, ink, deep darks |
| Tower Steel Gray | #9CA3AF | Metal surfaces, overcast sky |
| Dead River Silt Gray | #78716C | Weathered stone, exhausted ground |
| Knocker-bug Gold | #CA8A04 | Accents, gilding, warm highlights |
| Meadow Oxidized Copper | #78350F | Evening light, aged metal |
| Fountain Blue | #60A5FA | Water, Tower crown, light effects |

### Elevation Gradient (for terrain)
Blue (#2C5282) → Teal (#319795) → Yellow (#ECC94B) → Orange (#DD6B20) → Red (#C53030)

---

## Object Selection Rules

### Avoid
- Open books, ledgers, journals, notebooks (overused)
- Generic "scholarly" props unless truly specific to the scene
- Objects that appeared in the last 10 images (check object_registry)

### Prefer
- Objects specific to the ore fragment's narrative
- Parts of larger objects (a hand, a wheel, a latch)
- Densworld-specific items (three-direction compass, regional tools)
- Objects with texture and material interest

### When stuck, ask:
1. What objects does the ore fragment explicitly mention?
2. What objects would this character carry or use?
3. What would be lying around in this specific location?
4. Can I zoom in on something and use its parts?

---

## Regional Visual Identity

*(To be developed as images accumulate)*

### Dead River
- Palette: Silt Gray, Iron Gall Black, muted ochre
- Atmosphere: Exhausted, silty, slow-moving water
- Common objects: Ferry equipment, fishing gear, stilted structures

### Capital
- Palette: Archive blues, Knocker-bug Gold accents, formal whites
- Atmosphere: Bureaucratic, preserved, dusty grandeur
- Common objects: Seals, filing systems, formal furniture

### Yeller Quarry
- Palette: Quarry Ochre, Knocker-bug Gold veins, earth tones
- Atmosphere: Industrial extraction, layered terrain, dust
- Common objects: Mining tools, ore carts, measuring equipment

### Tower of Mirado
- Palette: Tower Steel Gray, Fountain Blue, stark contrast
- Atmosphere: Hovering, impossible, luminous crown
- Common objects: Rehabilitation equipment, observation instruments

### Focal Meadow
- Palette: Oxidized copper, ochre grass, bare stone
- Atmosphere: Strange botany, crater mystery, terminal observation
- Common objects: Field equipment, translucent flora, bare rock

### Dens
- Palette: Muted greens, sludge browns, organic darks
- Atmosphere: Shifting, unstable, creature-haunted
- Common objects: Trapping gear, expedition supplies, creature traces

*(Add more regions as they appear in images)*

---

## What Not to Do

1. **Don't reference real-world art movements** — No "Renaissance style," "Baroque lighting," etc. Let Densworld's own visual vocabulary emerge.

2. **Don't match themes** — The Bible text and Densworld scene are arbitrarily paired. Don't try to make the image "fit" the verse's meaning.

3. **Don't repeat object types** — If the last image had a lantern, this one shouldn't. Check the registry.

4. **Don't use generic fantasy tropes** — No elves, dragons, medieval castles unless they're specifically Densworld.

5. **Don't forget the loci** — Every image needs six spatially separated, visually distinct objects. The scene serves the mnemonic function.

---

## Revision Log

| Date | Change |
|------|--------|
| 2025-12-27 | Initial guide created |

---

*This guide will evolve as we generate more images and learn what works.*
