# Cross-Mod Compatibility Tags

**Datapack:** `Otherworld_Tags`

Ensures modded items work correctly across different systems by tagging them properly. Without these, mods wouldn't recognize each other's items.

---

## Magic Damage Types

All Iron's Spellbooks magic schools (eldritch, blood, ender, evocation, fire, holy, ice, lightning, nature) plus Traveloptics aqua magic, Cataclysm abyssal magic, and Alshanex sound magic are registered as:

- **Magic damage** — for resistance calculations
- **Armor-bypassing damage** — spells ignore physical armor
- **Witch resistance** — witches resist all magic

---

## Elemental Damage Types

- Fire spells count as **fire damage**
- Ice spells count as **freezing damage**
- Lightning spells count as **lightning damage**

---

## Armor Registration

35+ modded armor sets are tagged as proper boots/chestplates/helmets/leggings for cross-mod recognition. Mods covered:

- Ancient Aether
- Aquamirae
- Blood Magic
- Eidolon
- Epic Empires
- Forbidden Arcanus
- Immersive Armors
- Knights & Mages
- Endless Biomes
- Eldritch End
- BetterEnd

---

## Other Tags

| Tag | What It Does |
|-----|-------------|
| Supplementaries quiver → Curios quiver slot | Makes the quiver equippable in the Curios slot |
| Quark Ancient Tome → `otherworld:tomes` | Used as ingredient in the [Eye of Nothingness recipe](recipes.md) |
| Biomes O' Plenty biomes → forest biomes | Ensures BOP forests are recognized as forests by other mods |

---

## Config Files

**Location:** `Otherworld_Tags/data/[namespace]/tags/`
