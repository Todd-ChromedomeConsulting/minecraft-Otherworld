# Apotheosis — Loot Rarity & Gem System

**Datapack:** `Otherworld_Apotheosis`

This datapack completely configures the Apotheosis mod's adventure module — the system that makes enemies drop weapons and armor with random magical properties (affixes), gems you can socket into gear, and a full rarity tier system. Think Diablo-style loot.

---

## Rarity Tiers (6 levels)

| Tier | Color | Drop Weight | What You Get |
|------|-------|-------------|--------------|
| **Common** | Gray | 400 (very common) | 2 stat bonuses |
| **Uncommon** | Green | 320 | 2 stats + 50% chance for a gem socket |
| **Rare** | Blue | 150 | 2 stats + 2 potion effects + 1 ability + sockets |
| **Epic** | Purple | 90 | 3 stats + 2 potions + 1 ability + more sockets |
| **Mythic** | Orange | 40 | 4 stats + everything + lots of sockets |
| **Ancient** | Rainbow | 1 (extremely rare) | 4 stats + everything + possible extra ability |

**Config files:** `Otherworld_Apotheosis/data/apotheosis/rarities/`

---

## Affix Types (80+ affixes across all gear types)

Affixes are random bonuses that appear on dropped gear. They're organized by equipment slot:

### Swords (13 affixes)

Piercing (armor bypass), Violent (extra damage), Graceful (attack speed), Infernal (fire damage), Thunderstruck (lightning), and more.

### Armor (16 affixes)

Blast Forged (explosion resist), Dwarven (fire resist), Blessed (extra health), Windswept (speed), Winged (reduced gravity), and more.

### Shields (9 affixes)

Psychic (reflects 5-15% damage back), Catalyzing (spell boost), Devilish/Venomous/Withering (applies debuffs to attackers).

### Ranged Weapons (12 affixes)

Agile (faster draw), Streamlined (arrow velocity), Acidic/Grievous/Satanic (debuff arrows).

### Heavy Weapons/Axes (13 affixes)

Cleaving (7.5-12.5% chance for AOE hit), Giant Slaying (bonus vs large enemies), Executing (bonus vs low-health enemies).

### Pickaxes/Shovels (7 affixes)

Enlightened (auto-places torches), Radial (mines in a radius), Lucky (fortune boost).

**Config files:** `Otherworld_Apotheosis/data/apotheosis/affixes/`

---

## Gems (20+ types)

Gems are socketable items that add bonuses depending on what gear slot they go in. They come in two categories:

### Overworld Gems (always available)

Solar, Lightning, Combatant, Warlord, Samurai, Slipstream, Breach, Guardian, Brawlers, Lunar, Splendor, Tyrannical, Earth, Royalty

### Dimension-Locked Gems

Found only in specific dimensions:

| Gem | Dimension | Min Rarity | Key Bonus |
|-----|-----------|------------|-----------|
| **Inferno** | Nether | Rare | 3-6 fire damage on heavy weapons, detonation effect |
| **Blood Lord** | Nether | Rare | 2.5-12% life steal, damage boost with health penalty |
| **Endersurge** | The End | Epic | Global sharpness enchantment boost |
| **Queen** | Twilight Forest | Rare | Cold damage, 5-15% Twilight Fortification trigger |

**Config files:** `Otherworld_Apotheosis/data/apotheosis/gems/` and `data/irons_spellbooks/gems/`

---

## Iron's Spellbooks Integration

The Apotheosis system also has custom affixes and gems for spellcasting gear:

- **Armor affixes:** Cooldown reduction, Mana boost, Spell Power, Spell Resist
- **Weapon affixes:** Mana Regen
- **Spell gems:** Fire/Ice/Lightning/Holy/Nature/Blood/Ender/Evocation spell power gems

---

## Spawner Modification Recipes

24 recipes for modifying mob spawners by right-clicking them with specific items:

| Item | Effect |
|------|--------|
| Dragon Egg | Spawner ignores all conditions |
| Soul Lantern | Spawner ignores light level |
| Clock | Reduces spawn delay by 10 (min 100, max -1) |
| Fermented Spider Eye | Adds 1 to spawn count (max 8) |

**Config files:** `Otherworld_Apotheosis/data/apotheosis/recipes/spawner/`

---

## Key Config Settings

**File:** `minecraft/config/apotheosis/adventure.cfg`

| Setting | Value | What It Means |
|---------|-------|---------------|
| Random affix chance on mobs | 7.5% | 1 in ~13 mobs spawns with magical gear |
| Gem drop chance | 3.5% | Chance an affix mob drops a gem |
| Boss spawn rate | 0.005-0.012/tick | Very rare boss mob spawns |
| Boss cooldown | 72,000 ticks (1 hour) | Time between boss spawns |
| Overworld loot rarity | Common-Uncommon | Chests contain lower-tier items |
| Nether loot rarity | Common-Epic | Better loot in Nether chests |
| End loot rarity | Rare-Legendary | Best chest loot in the End |
