# Color Experiments for Densworld Visualization

**Expanding the palette through atmospheric primaries**

---

## The Problem

The existing `regional_color_palettes.csv` treats color as:
- **Material-derived** — pigments from creatures, minerals, inks
- **Functional** — primary, secondary, accent, background
- **Clean** — precise hex codes, spot application

This produces images where colors are *applied to objects* rather than *present in the world*.

---

## The New Approach: Atmospheric Primaries

Primary colors (red, blue, yellow) become the **color of light, air, and shadow** — not the color of things.

### Red Atmospheres

| Condition | Description | When to Use |
|-----------|-------------|-------------|
| Maw-light | Air tinged red near apex predators | Yeller Quarry danger zones |
| Fever-cast | Sickly red warmth of illness | Disease scenes, wrong warmth |
| Membrane-glow | Organic red like light through flesh | Creature interiors, the body |
| Blood-dusk | Sky the color of old wounds | End of things, finality |

**Prompt language:**
- "The air takes on a red tinge, as if something is bleeding into the light"
- "Red-dark shadows that pulse like something living"
- "The warmth is wrong — fever-colored, organic"

### Blue Atmospheres

| Condition | Description | When to Use |
|-----------|-------------|-------------|
| Watch-dark | The blue of being observed | The dens at night, awareness |
| Deep-water | Everything seen through ocean | Submerged feeling, pressure |
| Tower-glow | Luminescent blue from Mirado | Technology, rehabilitation |
| Cold-aware | Blue that knows you're there | Capital archives, institutions |

**Prompt language:**
- "Blue-dark, the color of being watched from the water"
- "The darkness is blue rather than black — aware, cold"
- "Light the color of the Tower's crown — luminescent, alien"

### Yellow Atmospheres

| Condition | Description | When to Use |
|-----------|-------------|-------------|
| Amber-weight | Heavy yellow pressing down | Yeller Quarry, thick air |
| Sickness-fog | Yellow haze of wrongness | Plague, miasma, corruption |
| Sulfur-cast | Mineral yellow, volcanic | Underworld, processing |
| Prime-light | The yellow of Yeller's attention | When she's watching |

**Prompt language:**
- "Amber light with mass, pressing down like something solid"
- "Yellow fog that isn't fog — too thick, too aware"
- "The light is sulfurous, mineral, coming from below"

---

## Combining Primaries

### Amber-Blue (Quarry at Dusk)
The dominant amber sky meeting blue-black tunnel mouths. Warmth above, cold awareness below. The creatures know both.

### Red-Blue (The Dens at Night)
Fever-warmth of the boundary meeting the watch-dark of the interior. Invitation in red, observation in blue.

### Yellow-Red (Maw Territory)
Sickness-yellow haze with Maw-light bleeding through. Everything is warning. Nothing is safe.

### All Three (Yeller's Presence)
When she appears, all primaries intensify. Amber weighs more. Blue watches harder. Red pulses at the edges. The world responds to her attention.

---

## The Darkness Spectrum

Black in Densworld is not uniform. Each darkness has character:

| Darkness | Hex | Character | Found |
|----------|-----|-----------|-------|
| Densmuck Black | #1A1A1A | Oily, pulling, wants you | The dens surface |
| Grimslew Scale | #030712 | Deepest, blue-hint, ancient | Grimslenken waters |
| Iron Gall | #1F2937 | Formal, institutional, remembers | Capital archives |
| Tunnel-mouth | #0F0F0F | Watching, might contain anything | Yeller Quarry |
| Wrong-shadow | varies | Doesn't belong to any object | Everywhere, unpredictably |

### Prompt Language for Darkness

- "The shadow doesn't attach to the rock — it exists independently"
- "Darkness that has weight, that might reach"
- "Black that is also blue, also watching, also patient"
- "The tunnel mouth is darker than physics allows"

---

## Experimental Palettes

### Palette 1: Quarry Amber
For Yeller Quarry scenes.

```
Atmosphere: Amber (#D97706) at 40% opacity over everything
Shadows: Warm black (#1C1917) with red undertone
Highlights: Sulfur yellow (#FDE047) in the particulate
Ground: Rust and ochre (#B45309, #78350F)
Sky: Amber pressing into gray (#92400E → #57534E)
Tunnel mouths: Pure watching black (#0A0A0A)
```

### Palette 2: Dens Gray-Alive
For dens boundary scenes.

```
Atmosphere: Gray that breathes — shifting between #6B7280 and #9CA3AF
Ground: Ash-skin texture (#D1D5DB with organic variation)
Boundary: Where gray meets gray (no clear line)
Sky: Sourceless — same gray as ground
Accent: Sickly yellow (#FEF08A) where light shouldn't be
Deep: Blue-black (#1E293B) at the center, pulling
```

### Palette 3: Capital Archive
For institutional scenes.

```
Atmosphere: Dust-yellow (#FEF3C7) at low opacity
Stone: Cold gray (#64748B) that absorbs light
Wood: Dark enough to hide things (#3F3F46)
Paper: Aged yellow (#FFFBEB) with foxing
Ink: Iron gall (#1F2937) that moves when you don't look
Shadows in stacks: Go too deep (#0F172A)
Candlelight: Doesn't help (#F59E0B confined, not spreading)
```

### Palette 4: Tower Uncanny
For Tower of Mirado scenes.

```
Tower: Steel that rejects light (#9CA3AF → #6B7280)
Crown: Fountain blue (#60A5FA) luminescent
Sky: Too dark for day (#1E3A8A)
Desert: Ochre beneath (#B45309) but cold
Shadow: The Tower casts wrong — shape doesn't match
Atmosphere: Blue-tint as if underwater
Horizon: Where sky meets desert is uncertain
```

---

## Color in Prompts: Examples

### Bad (Old Style)
```
Color palette: Quarry Ochre (#B45309), Iron Gall Black (#1F2937),
Knocker-bug Gold (#CA8A04) accents.
```

### Good (New Style)
```
The light itself is amber — not golden highlights on objects, but
amber as the medium through which everything is seen. Shadows run
toward rust-red rather than black. The darkness in the tunnel mouth
is the exception: pure watching black, no amber reaches there.
Where the amber light meets the tunnel darkness, the boundary
vibrates slightly. Something knows the light is trying to enter.
```

---

## Testing Color Choices

After generating an image, ask:

1. **Is the atmosphere colored?** (Not just objects)
2. **Do the primaries feel heavy/present?** (Not decorative)
3. **Does the darkness have character?** (Not just absence)
4. **Would this palette exist on Earth?** (It shouldn't quite)

---

## Notes for AI Generators

Different generators handle atmospheric color differently:

- **Midjourney:** Responds well to "tinted," "cast," "suffused with"
- **DALL-E:** Needs explicit "the light is [color]" statements
- **Stable Diffusion:** Responds to color temperature language
- **Nano Banana / Gemini:** Unknown — test with explicit atmosphere statements

When in doubt, be more explicit:
- "The air is amber-colored, thick with particulate"
- "Everything is seen through a blue-dark filter"
- "Red tinges the shadows, organic and warm"

---

## Revision Log

| Date | Change |
|------|--------|
| 2025-12-27 | Initial creation |

---

*Test these palettes. Document what works. This file will evolve.*
