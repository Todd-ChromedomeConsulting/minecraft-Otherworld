# Otherworld [Dungeons & Dragons] — Complete Modpack Guide

> **Minecraft 1.20.1 | Forge 47.4.13 | ~392 Mods | CurseForge Pack ID: 1418133 (v5)**

This guide explains every custom datapack in the Otherworld modpack, what each one does, all crafting recipes, configurable options, how to change settings, and progression gating.

---

## Table of Contents

1. [How the Pack is Organized](#1-how-the-pack-is-organized)
2. [Otherworld_Recipes — Custom Crafting Recipes](#2-otherworld_recipes--custom-crafting-recipes)
3. [Otherworld_Apotheosis — Loot Rarity & Gem System](#3-otherworld_apotheosis--loot-rarity--gem-system)
4. [Otherworld_Autoleveling — Mob Scaling System](#4-otherworld_autoleveling--mob-scaling-system)
5. [Otherworld_Better_Combat — Weapon Animation Overhaul](#5-otherworld_better_combat--weapon-animation-overhaul)
6. [Otherworld_Loot_Tweaks — Bounties, Gateways & Loot](#6-otherworld_loot_tweaks--bounties-gateways--loot)
7. [Otherworld_Tags — Cross-Mod Compatibility Tags](#7-otherworld_tags--cross-mod-compatibility-tags)
8. [Legendary Survival Config — Temperature & Thirst](#8-legendary-survival-config--temperature--thirst)
9. [Otherworld_Fixes — Balance Patches](#9-otherworld_fixes--balance-patches)
10. [Smaller Datapacks (Zipped)](#10-smaller-datapacks-zipped)
11. [All Crafting Recipes Reference](#11-all-crafting-recipes-reference)
12. [Progression & Resource Gating](#12-progression--resource-gating)
13. [How to Modify Settings with Claude Code](#13-how-to-modify-settings-with-claude-code)

---

## 1. How the Pack is Organized

All custom datapacks live in:
```
minecraft/config/paxi/datapacks/
```

**Paxi** is a mod that automatically loads datapacks from this folder — no need to manually install them into each world save. Any changes you make here apply to all worlds.

There are **7 custom Otherworld datapacks** (folders) and **14 additional datapacks** (zip files).

### Key Config Locations

| What | Where |
|------|-------|
| Datapack files | `minecraft/config/paxi/datapacks/` |
| Mod configs (.toml, .cfg) | `minecraft/config/` |
| Resource packs | `minecraft/resourcepacks/` |
| Mod JARs | `minecraft/mods/` |

---

## 2. Otherworld_Recipes — Custom Crafting Recipes

**What it does:** Adds 2 custom shaped crafting recipes for items that either didn't have recipes or had recipes the pack author wanted to change.

### Recipe 1: Eye of Nothingness (Traveloptics)

A powerful teleportation/dimension item.

```
  B F B        B = Crying Obsidian
  V G V        F = Ancient Knowledge Fragment (Iron's Spellbooks)
  B Q B        V = Void Spellweave Ingot (Traveloptics)
               G = Eye of Ender
               Q = Any item tagged "otherworld:tomes" (= Quark Ancient Tome)
```

**Result:** 1x Eye of Nothingness

**File:** `Otherworld_Recipes/data/traveloptics/recipes/eye_of_nothingness.json`

### Recipe 2: Blackstone Pedestal (Soulslike Weaponry)

A crafting station used for boss weapon creation.

```
  I L I        I = Moonstone (Soulslike Weaponry)
  X Y X        L = Lord Soul Purple (Soulslike Weaponry boss drop)
  O O O        X = Ender Pearl
               Y = Obsidian
               O = Polished Blackstone Bricks
```

**Result:** 1x Blackstone Pedestal

**File:** `Otherworld_Recipes/data/soulsweapons/recipes/blackstone_pedestal.json`

---

## 3. Otherworld_Apotheosis — Loot Rarity & Gem System

**What it does:** Completely configures the Apotheosis mod's adventure module — the system that makes enemies drop weapons and armor with random magical properties (affixes), gems you can socket into gear, and a full rarity tier system. Think Diablo-style loot.

### Rarity Tiers (6 levels)

| Tier | Color | Drop Weight | What You Get |
|------|-------|-------------|--------------|
| **Common** | Gray | 400 (very common) | 2 stat bonuses |
| **Uncommon** | Green | 320 | 2 stats + 50% chance for a gem socket |
| **Rare** | Blue | 150 | 2 stats + 2 potion effects + 1 ability + sockets |
| **Epic** | Purple | 90 | 3 stats + 2 potions + 1 ability + more sockets |
| **Mythic** | Orange | 40 | 4 stats + everything + lots of sockets |
| **Ancient** | Rainbow | 1 (extremely rare) | 4 stats + everything + possible extra ability |

**Config files:** `Otherworld_Apotheosis/data/apotheosis/rarities/`

### Affix Types (80+ affixes across all gear types)

Affixes are random bonuses that appear on dropped gear. They're organized by equipment slot:

**Swords (13 affixes):** Piercing (armor bypass), Violent (extra damage), Graceful (attack speed), Infernal (fire damage), Thunderstruck (lightning), and more.

**Armor (16 affixes):** Blast Forged (explosion resist), Dwarven (fire resist), Blessed (extra health), Windswept (speed), Winged (reduced gravity), and more.

**Shields (9 affixes):** Psychic (reflects 5-15% damage back), Catalyzing (spell boost), Devilish/Venomous/Withering (applies debuffs to attackers).

**Ranged Weapons (12 affixes):** Agile (faster draw), Streamlined (arrow velocity), Acidic/Grievous/Satanic (debuff arrows).

**Heavy Weapons/Axes (13 affixes):** Cleaving (7.5-12.5% chance for AOE hit), Giant Slaying (bonus vs large enemies), Executing (bonus vs low-health enemies).

**Pickaxes/Shovels (7 affixes):** Enlightened (auto-places torches), Radial (mines in a radius), Lucky (fortune boost).

**Config files:** `Otherworld_Apotheosis/data/apotheosis/affixes/`

### Gems (20+ types)

Gems are socketable items that add bonuses depending on what gear slot they go in. They come in two categories:

**Overworld Gems (always available):** Solar, Lightning, Combatant, Warlord, Samurai, Slipstream, Breach, Guardian, Brawlers, Lunar, Splendor, Tyrannical, Earth, Royalty

**Dimension-Locked Gems (found only in specific dimensions):**

| Gem | Dimension | Min Rarity | Key Bonus |
|-----|-----------|------------|-----------|
| **Inferno** | Nether | Rare | 3-6 fire damage on heavy weapons, detonation effect |
| **Blood Lord** | Nether | Rare | 2.5-12% life steal, damage boost with health penalty |
| **Endersurge** | The End | Epic | Global sharpness enchantment boost |
| **Queen** | Twilight Forest | Rare | Cold damage, 5-15% Twilight Fortification trigger |

**Config files:** `Otherworld_Apotheosis/data/apotheosis/gems/` and `data/irons_spellbooks/gems/`

### Iron's Spellbooks Integration

The Apotheosis system also has custom affixes and gems for spellcasting gear:
- **Armor affixes:** Cooldown reduction, Mana boost, Spell Power, Spell Resist
- **Weapon affixes:** Mana Regen
- **Spell gems:** Fire/Ice/Lightning/Holy/Nature/Blood/Ender/Evocation spell power gems

### Spawner Modification Recipes (24 recipes)

You can modify mob spawners by right-clicking them with specific items:

| Item | Effect |
|------|--------|
| Dragon Egg | Spawner ignores all conditions |
| Soul Lantern | Spawner ignores light level |
| Clock | Reduces spawn delay by 10 (min 100, max -1) |
| Fermented Spider Eye | Adds 1 to spawn count (max 8) |

**Config files:** `Otherworld_Apotheosis/data/apotheosis/recipes/spawner/`

### Key Apotheosis Config Settings

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

---

## 4. Otherworld_Autoleveling — Mob Scaling System

**What it does:** Makes mobs get stronger the further you travel from spawn and the deeper you go underground. Also scales mobs differently per dimension. This is the core difficulty scaling system.

### How Leveling Works

Every mob gets a level when it spawns based on:
1. **Distance from world spawn** — further away = higher level
2. **Depth below sea level** — deeper underground = higher level
3. **Dimension** — different dimensions have different base levels
4. **Random bonus** — some mobs get extra random levels

Each level gives the mob bonus stats:
- **+0.2 attack damage** per level
- **+0.2 armor** per level
- **+0.2 max health** per level
- **+0.2 spell resist** per level
- **+0.2 projectile damage** per level
- **+0.1 explosion damage** per level

**Max level cap: 20**

### Dimension Scaling

| Dimension | Starting Level | Max Level | Scaling |
|-----------|---------------|-----------|---------|
| **Overworld** | 1 | 12 | Slow (0.0001/block distance, 0.02/block depth) |
| **The Nether** | 8 | 12 | Fast (0.01/block distance & depth) |
| **The End** | 20 | 20 | Fixed (no scaling, everything is max) |
| **The Aether** | 6 | 6 | Minimal (0.001/block) |
| **Minecells Ramparts** | 10 | 10 | Fixed |
| **Minecells Crypt** | 12 | 12 | Fixed |

### Boss Entity Levels

| Boss | Starting Level | Max Level | Notes |
|------|---------------|-----------|-------|
| Ender Dragon | 25 | 25 | Fixed, +9.7% per level to all stats |
| Ice/Fire/Lightning Dragon | 15 | 20 | Scales with distance, +10% damage, +2.5% health per level |
| Lich (Soulslike Weaponry) | 20 | 20 | Fixed |
| Leviathan (Cataclysm) | 15 | 20 | Scales with depth |
| Champion Goblin | 10 | 12 | +0-1 random bonus levels |
| Orc Boss | 4 | 12 | +0-3 random bonus levels |

### Mods with Autoleveling Support (28 namespaces)

Minecraft (vanilla), Aether, Alex's Caves, Alex's Mobs, Ancient Aether, Animated Mobs, Aquamirae, Born in Chaos, Bosses of Mass Destruction, Cataclysm, Dark Doppelganger, EEEAB's Mobs, Eidolon, Goblins Tyranny, Ice and Fire, Iron's Spellbooks, Legendary Monsters, Lost Aether Content, Minecells, Mobs of Mythology, Mowzie's Mobs, Realm RPG Demons, Realm RPG Quests, Rotten Creatures, Soulslike Weaponry, The Orcs, Traveloptics, Valoria

**Config file (global settings):** `minecraft/config/autoleveling-common.toml`
**Per-entity configs:** `Otherworld_Autoleveling/data/[mod]/leveling_settings/entities/[mob].json`
**Per-dimension configs:** `Otherworld_Autoleveling/data/[mod]/leveling_settings/dimensions/[dimension].json`

---

## 5. Otherworld_Better_Combat — Weapon Animation Overhaul

**What it does:** Defines custom attack animations, combo chains, attack ranges, and hitbox shapes for modded weapons. This makes combat feel like an action RPG instead of vanilla Minecraft clicking.

### Weapon Categories Configured

| Category | Range | Handed | Example Weapons |
|----------|-------|--------|-----------------|
| **Lance** | 6.5 blocks | One-hand | Valkyrie Lance (Aether) |
| **Claymore** | 3.0 blocks | Two-hand | Dragonsteel Swords (Ice and Fire) |
| **Double Axe** | 3.25 blocks | Two-hand | Dragonsteel Axes (Ice and Fire) |
| **Hammer** | 3.5 blocks | Two-hand | Troll Weapons (Ice and Fire) |
| **Trident** | 3.2 blocks | Inherited | Coral Lance, Sweet Lance (Aquamirae) |
| **Cutlass** | Inherited | Inherited | Remnants Saber (Aquamirae) |
| **Dagger** | 2.5 blocks | Inherited | Amphithere Macuahuitl, Divider, Dagger of Greed |
| **Sword** | Inherited | Inherited | Poisoned Blade, Terrible Sword (Aquamirae) |
| **Soul Knife** | Inherited | Inherited | Fin Cutter (Aquamirae) |
| **Battlestaff** | Inherited | Inherited | Whisper of the Abyss (Aquamirae) |

### Combo Chains

**Claymore combo (3 hits):** Horizontal Slash → Stab → Overhead Slam (0.75x → 1.0x → 1.25x damage)

**Double Axe combo (4 hits):** Right Slash → Left Slash → Right Slash → 360° Spin (all 1.0x damage)

**Hammer combo (3 hits):** Light Slam → Medium Slam → Heavy Slam (0.8x → 0.9x → 1.2x damage)

**Lance:** Changes animation based on mounted vs. on foot.

### Key Better Combat Config Settings

**File:** `minecraft/config/bettercombat/server.json5`

| Setting | Value | What It Means |
|---------|-------|---------------|
| Upswing multiplier | 0.5 | Attacks start fast (50% wind-up) |
| Max sweep targets | 4 | Hit up to 4 enemies before damage penalty |
| Sweep damage penalty | 50% max | Extra targets take up to 50% less damage |
| Movement while attacking | 50% speed | You slow down while swinging |
| Dual wield attack speed bonus | +20% | Dual wielding is faster |
| Combo reset | 3x weapon cooldown | Stop attacking to reset combo |

**Mods covered:** Aether, Ice and Fire (all dragonsteel + troll weapons), Aquamirae (all weapons), plus the massive MalfuCombatDatapack (covers Cataclysm, Simply Swords, and more).

---

## 6. Otherworld_Loot_Tweaks — Bounties, Gateways & Loot

**What it does:** This is the largest datapack. It sets up the bounty/quest system (Extra Bounties mod), wave-based mob arenas (Gateways), and modifies loot tables across multiple mods.

### Bounty System (58 mod integrations)

The bounty system gives players quests to complete for rewards. Bounty decrees are found in villages and define what quests are available.

**How bounties work:**
1. Find a Bounty Board in a village
2. Pick up a Bounty Decree (quest contract)
3. Complete objectives (kill mobs, gather items, etc.)
4. Return for rewards (coins, rare items, etc.)

**Currency:** Uses Numismatic Overhaul coins:
- **Bronze coins** (1-99, common reward)
- **Silver coins** (1-48, worth 100 bronze each)
- **Gold coins** (1-8, worth 5000 bronze each, rare)

**Mods with bounties:** Create (6 different categories), Iron's Spellbooks, Ice and Fire, Alex's Mobs, Mowzie's Mobs, Farmer's Delight, Sophisticated Storage/Backpacks, Powah, and 45+ more.

### Gateway Arenas (225 configurations)

Gateways are wave-based mob arenas in 3 sizes:

| Size | Mobs per Wave | Loot Rolls | Waves |
|------|--------------|------------|-------|
| **Small** | 3-7 | 10 | 5 |
| **Medium** | 6-14 | 20 | 5 |
| **Large** | 9-21 | 30 | 5 |

Each wave gets progressively harder:
- Wave 1: Normal stats
- Wave 2: +6 armor, 45% bonus health/damage
- Wave 3: +9 armor, 60% bonus health/damage, faster
- Wave 4: +15 armor, 75-90% bonus health/damage
- Wave 5: +15 armor, 105% bonus health, 150% bonus damage

Covers all standard Minecraft mobs (cow, pig, sheep, creeper, skeleton, zombie, etc.)

### Level-Scaled Healing Drops

Leveled mobs drop healing items based on their level (2% base chance):

| Mob Level | Drop |
|-----------|------|
| 1-7 | Healing Vial (Valoria) |
| 8-14 | Healing Flask (Valoria) |
| 15+ | Healing Elixir (Valoria) |

### Void Cathedral Loot

The Traveloptics Void Cathedral has a custom high-tier loot table including:
- Arcane Essence (8-16)
- Enchanted netherite swords (level 20-39 enchantments)
- Enchanted diamond/iron armor
- Ender school spell scrolls
- Various building materials and rare items

### Config Files

**Bounty decrees:** `Otherworld_Loot_Tweaks/data/extrabounties/bounty_decrees/`
**Bounty pools:** `Otherworld_Loot_Tweaks/data/extrabounties/bounty_pools/`
**Gateways:** `Otherworld_Loot_Tweaks/data/extrabounties/gateways/`
**Loot tables:** `Otherworld_Loot_Tweaks/data/[mod]/loot_tables/`

---

## 7. Otherworld_Tags — Cross-Mod Compatibility Tags

**What it does:** Ensures modded items work correctly across different systems by tagging them properly. Without these, mods wouldn't recognize each other's items.

### What Gets Tagged

**Magic Damage Types:** All Iron's Spellbooks magic schools (eldritch, blood, ender, evocation, fire, holy, ice, lightning, nature) plus Traveloptics aqua magic, Cataclysm abyssal magic, and Alshanex sound magic are registered as:
- Magic damage (for resistance calculations)
- Armor-bypassing damage (spells ignore physical armor)
- Witch resistance (witches resist all magic)

**Elemental Damage Types:**
- Fire spells count as fire damage
- Ice spells count as freezing damage
- Lightning spells count as lightning damage

**Armor Registration:** 35+ modded armor sets from Ancient Aether, Aquamirae, Blood Magic, Eidolon, Epic Empires, Forbidden Arcanus, Immersive Armors, Knights & Mages, Endless Biomes, Eldritch End, and BetterEnd are tagged as proper boots/chestplates/helmets/leggings for cross-mod recognition.

**Other Tags:**
- Supplementaries quiver → tagged as Curios quiver slot
- Quark Ancient Tome → tagged as `otherworld:tomes` (used in Eye of Nothingness recipe)
- Biomes O' Plenty biomes → tagged as forest biomes

**Config files:** `Otherworld_Tags/data/[namespace]/tags/`

---

## 8. Legendary Survival Config — Temperature & Thirst

**What it does:** Configures the Legendary Survival Overhaul mod which adds temperature management and thirst/hydration mechanics. You need to stay warm/cool and drink water to survive.

### Temperature System

Every piece of armor has a temperature value. Positive = warming, negative = cooling.

| Armor Type | Temperature | Best For |
|------------|-------------|----------|
| Leather | +1.0 (warm) | Cold biomes |
| Gold | +1.0 (warm) | Cold biomes |
| Iron | -0.5 (cool) | Hot biomes |
| Diamond | -1.0 (cold) | Hot biomes/Nether |
| Netherite | +1.5 (very warm) | Cold biomes |
| Ice Dragonsteel | -2.5 (very cold) | Nether/deserts |
| Fire Dragonsteel | +2.5 (very hot) | Cold biomes/mountains |

**Temporary heating/cooling items:**

| Item | Effect | Duration |
|------|--------|----------|
| Charcoal Block | Heating | 4.5 minutes |
| Ice Block | Cooling | 30 seconds |
| Blue Ice | Cooling | 30 seconds |
| Packed Ice | Cooling | 30 seconds |
| Snowball | Cooling | 30 seconds |

### Thirst System

Different drinks/foods restore different amounts of hydration:

| Item | Hydration | Saturation | Side Effects |
|------|-----------|------------|--------------|
| Enchanted Golden Apple | 16 | 16 | None |
| Healing Elixir | 8 | 6 | None |
| Golden Apple | 4 | 2 | None |
| Healing Potion | 4 | 2 | None |
| Tea Cups | 4 | 2 | None |
| Whiskey/Rum/Liquor | 4 | 0 | 20% chance of Thirst debuff |
| Berries/Raw Fruit | 1-2 | 1 | None |

**Key config settings:**

**File:** `minecraft/config/legendarysurvivaloverhaul/legendarysurvivaloverhaul-common.toml`

| Setting | Value | What It Means |
|---------|-------|---------------|
| Temperature system | Enabled | Must manage body temperature |
| Thirst system | Enabled | Must drink fluids |
| Body damage system | Disabled | No localized damage (headshots, etc.) |
| Health overhaul | Enabled | Modified health mechanics |
| Difficulty mode | NORMAL | Temperature can reduce you to 1 heart |
| Biome temp multiplier | 2.0x | Biomes strongly affect temperature |
| Max bonus health | 20 (10 hearts) | Can gain up to 10 extra hearts |
| Natural health regen | Disabled | Must use healing items/food |

**Per-item configs:** `legendarysurvival_config/data/[mod]/legendarysurvivaloverhaul/`

---

## 9. Otherworld_Fixes — Balance Patches

**What it does:** Disables or rebalances specific items/features that were too powerful or caused issues.

### Changes Made

- **BetterNether Flaming Ruby gear:** Most recipes disabled (too easy to get powerful Nether gear)
- **BetterNether Ruby ore worldgen:** Modified (likely reduced spawn rate)
- **Backpack recipe:** Overridden (rebalanced)
- **EEEAB's Mobs Bloody Altar:** Biome restriction changed (controls where the structure spawns)
- **Valoria decorative pots:** Worldgen adjusted

**File:** `Otherworld_Fixes.zip` (zipped datapack)

---

## 10. Smaller Datapacks (Zipped)

### MalfuCombatDatapack V3.1
**What it does:** Massive combat animation pack (647 files) that defines Better Combat weapon animations for Cataclysm, Simply Swords, Simply More, and Mythic Metals weapons. Adds combo chains, swing sounds, and hitbox definitions.

### create_chipped_cutting
**What it does:** Adds 3,878 Create mechanical saw recipes for cutting between Chipped block texture variants. Instead of using the Chipped workbench, you can use Create's mechanical saw.

### mmc_disable_onjoin_books
**What it does:** Prevents Iron's Spellbooks from giving you a guide book every time you join a server.

### Incendium
**What it does:** Overrides 8 Incendium Nether biome definitions to adjust mob spawns and features for the pack's balance.

### FarmersDelight_ToolFix
**What it does:** Makes modded axes, pickaxes, and shovels work properly with Farmer's Delight cutting board recipes.

### apexcore-no-visualizer
**What it does:** Disables ApexCore's block visualizer overlay.

### formationsoverworldconfig
**What it does:** Adjusts how frequently "rare" Formations Overworld structures generate.

### intstrong_alexsmobs
**What it does:** Adds Alex's Mobs creatures to Integrated Stronghold's stronghold generation as spawners.

### Quark x FD Bark Cutting Compat
**What it does:** Adds Farmer's Delight cutting board recipes for Quark's extra wood types (azalea, blossom, ancient).

### Other Zipped Packs
- **BE_default_endgen_fix** — Fixes BetterEnd end generation for 1.20.x
- **ichphilipp-s-endcity-better-end** — Integrates End Cities with BetterEnd
- **idasalexsmobs** — Integrates Alex's Mobs with Integrated Dungeons and Structures
- **trueending** — True Ending mod compatibility fix

---

## 11. All Crafting Recipes Reference

### Custom Otherworld Recipes

#### Eye of Nothingness
```
┌───┬───┬───┐
│ B │ F │ B │  B = Crying Obsidian
├───┼───┼───┤  F = Ancient Knowledge Fragment (Iron's Spellbooks)
│ V │ G │ V │  V = Void Spellweave Ingot (Traveloptics)
├───┼───┼───┤  G = Eye of Ender
│ B │ Q │ B │  Q = Quark Ancient Tome
└───┴───┴───┘
→ 1x Eye of Nothingness
```

#### Blackstone Pedestal
```
┌───┬───┬───┐
│ I │ L │ I │  I = Moonstone (Soulslike Weaponry)
├───┼───┼───┤  L = Lord Soul Purple (boss drop)
│ X │ Y │ X │  X = Ender Pearl
├───┼───┼───┤  Y = Obsidian
│ O │ O │ O │  O = Polished Blackstone Bricks
└───┴───┴───┘
→ 1x Blackstone Pedestal
```

### Spawner Modification Recipes (Apotheosis)

These are "use item on spawner" recipes, not crafting table recipes:

| Action | Item Used | Effect |
|--------|-----------|--------|
| Right-click spawner | Dragon Egg | Spawner ignores all spawn conditions |
| Right-click spawner | Soul Lantern | Spawner ignores light level |
| Right-click spawner | Clock | Reduces max spawn delay by 10 |
| Right-click spawner | Fermented Spider Eye | Increases spawn count by 1 |

### Disabled Recipes

The following recipes are intentionally disabled in this pack:
- **Iron's Spellbooks ward rings** (Fireward, Frostward, Poisonward) — disabled in Loot Tweaks
- **BetterNether Flaming Ruby equipment** — disabled in Otherworld_Fixes
- **Apotheosis elongated sword affix** — disabled in Better Combat pack

---

## 12. Progression & Resource Gating

This section maps out which crafting ingredients are hard to get and what progression gates they represent.

### Progression Tiers

#### Tier 1: Early Game (Overworld Surface)
- **Polished Blackstone Bricks** — Mine blackstone in the overworld or find in structures
- **Obsidian** — Requires diamond pickaxe + water/lava interaction
- **Crying Obsidian** — Found in ruined portals, Piglin bartering

#### Tier 2: Nether Access Required
- **Ender Pearls** — Kill Endermen (available in Overworld but much more common in Nether/Warped Forest)
- **Soul Lantern** — Crafted with soul torch + iron nuggets (soul sand from Nether)
- **Fermented Spider Eye** — Spider eye + brown mushroom + sugar (mushrooms easier in Nether)
- **Clock** — Gold + redstone (gold abundant in Nether)
- **Inferno Gem** (Apotheosis) — Only drops from Nether enemies, Rare+ rarity
- **Blood Lord Gem** (Apotheosis) — Only drops from Nether enemies, Rare+ rarity

#### Tier 3: Boss Kills Required
- **Lord Soul Purple** (Blackstone Pedestal recipe) — **Dropped by a Soulslike Weaponry boss.** This is one of the hardest ingredients to obtain. You must defeat a major boss enemy from the Marium's Soulslike Weaponry mod.
- **Dragon Egg** (spawner recipe) — Kill the Ender Dragon in The End
- **Moonstone** (Blackstone Pedestal recipe) — Soulslike Weaponry material, obtained through the mod's progression

#### Tier 4: Advanced Magic / Late Game
- **Ancient Knowledge Fragment** (Eye of Nothingness recipe) — Found in Iron's Spellbooks dungeon loot. Requires exploring magic-themed structures.
- **Void Spellweave Ingot** (Eye of Nothingness recipe) — Traveloptics endgame material. Requires significant Traveloptics mod progression.
- **Quark Ancient Tome** (Eye of Nothingness recipe) — Rare dungeon loot from Quark. Found in stronghold libraries and other structures.
- **Eye of Ender** (Eye of Nothingness recipe) — Blaze powder (Nether fortress blazes) + Ender Pearl

#### Tier 5: Dimension-Locked Content
- **Endersurge Gem** — Only found in The End, minimum Epic rarity
- **Queen Gem** — Only found in Twilight Forest dimension, requires Rare+ rarity
- **Ice/Fire/Lightning Dragonsteel** — Requires killing Ice and Fire dragons and processing their materials
- **Void Cathedral loot** — Requires accessing Traveloptics dimension

### Resource Gating Summary

```
Overworld Start
  │
  ├─→ Diamond Pickaxe → Obsidian → Nether Portal
  │                                    │
  │                    ┌───────────────┤
  │                    │               │
  │              Blaze Rods      Soul Sand
  │              (Fortress)     (Soul Valley)
  │                    │               │
  │              Blaze Powder    Soul Lantern
  │                    │         (spawner mod)
  │                    │
  │              Eye of Ender ─────────────┐
  │                                        │
  │                                   Stronghold
  │                                   (End Portal)
  │                                        │
  │                                    The End
  │                                        │
  │                            ┌───────────┤
  │                            │           │
  │                      Dragon Egg   Endersurge
  │                      (spawner)      Gem
  │
  ├─→ Soulslike Weaponry Bosses
  │         │
  │    Lord Soul Purple + Moonstone
  │         │
  │    Blackstone Pedestal
  │
  ├─→ Iron's Spellbooks Dungeons
  │         │
  │    Ancient Knowledge Fragment
  │         │
  │    Eye of Nothingness (+ Void Spellweave Ingot + Ancient Tome)
  │
  └─→ Ice and Fire Dragons → Dragonsteel Gear
```

### Difficulty Progression by Dimension

| Dimension | Mob Levels | Apotheosis Loot | Notes |
|-----------|-----------|-----------------|-------|
| Overworld (near spawn) | 1-3 | Common-Uncommon | Safe starting area |
| Overworld (far from spawn) | 5-12 | Common-Uncommon | Gets challenging |
| The Aether | 6 (fixed) | — | Moderate, consistent |
| The Nether | 8-12 | Common-Epic | Dangerous, good loot |
| Minecells Ramparts | 10 (fixed) | — | Challenging dungeon |
| Minecells Crypt | 12 (fixed) | — | Harder dungeon |
| The End | 20 (fixed) | Rare-Legendary | Endgame, best loot |

---

## 13. How to Modify Settings with Claude Code

You can ask Claude Code to modify any setting in this modpack. Here's how to request changes for each system:

### Modifying Crafting Recipes

**Recipe files location:** `minecraft/config/paxi/datapacks/Otherworld_Recipes/data/[mod]/recipes/[item].json`

**To change an existing recipe, ask:**
> "Change the Eye of Nothingness recipe to use diamonds instead of crying obsidian"

**To add a new recipe, ask:**
> "Add a new crafting recipe for [item] that uses [ingredients]"

**Recipe format reference (shaped crafting):**
```json
{
  "type": "minecraft:crafting_shaped",
  "category": "misc",
  "pattern": ["ABC", "DEF", "GHI"],
  "key": {
    "A": {"item": "minecraft:diamond"},
    "B": {"tag": "forge:ingots/iron"}
  },
  "result": {"item": "mod:item_name", "count": 1}
}
```

- `"item"` = a specific item (e.g., `"minecraft:diamond"`)
- `"tag"` = any item in a tag group (e.g., `"forge:ingots/iron"` matches any iron ingot)
- Spaces in the pattern mean empty slots
- The pattern can be 1x1 up to 3x3

**Shapeless recipe format:**
```json
{
  "type": "minecraft:crafting_shapeless",
  "ingredients": [
    {"item": "minecraft:diamond"},
    {"item": "minecraft:gold_ingot"}
  ],
  "result": {"item": "mod:item_name", "count": 1}
}
```

### Modifying Mob Levels (Autoleveling)

**Per-entity config:** `minecraft/config/paxi/datapacks/Otherworld_Autoleveling/data/[mod]/leveling_settings/entities/[mob].json`

**Example requests:**
> "Make zombies start at level 5 instead of level 1"
> "Reduce the Ender Dragon's level from 25 to 15"
> "Disable level scaling for creepers"

**To disable scaling for a mob, set:**
```json
{
  "starting_level": 1,
  "max_level": 1,
  "levels_per_distance": 0,
  "levels_per_deepness": 0
}
```

**Global config:** `minecraft/config/autoleveling-common.toml`
> "Change the max level cap from 20 to 30"
> "Increase attack damage bonus per level from 0.2 to 0.5"

### Modifying Apotheosis Loot (Rarities, Affixes, Gems)

**Rarity weights:** `minecraft/config/paxi/datapacks/Otherworld_Apotheosis/data/apotheosis/rarities/`
> "Make Mythic items twice as common" → Double the weight value in mythic.json

**Affix values:** `minecraft/config/paxi/datapacks/Otherworld_Apotheosis/data/apotheosis/affixes/[type]/`
> "Increase the Piercing affix armor bypass from 2.0 to 3.0"

**Gem bonuses:** `minecraft/config/paxi/datapacks/Otherworld_Apotheosis/data/apotheosis/gems/`
> "Make the Inferno gem give more fire damage"

**Global adventure settings:** `minecraft/config/apotheosis/adventure.cfg`
> "Increase the chance of mobs spawning with magical gear from 7.5% to 15%"
> "Make bosses spawn more frequently"

### Modifying Temperature & Thirst

**Armor temperature:** `minecraft/config/paxi/datapacks/legendarysurvival_config/data/[mod]/legendarysurvivaloverhaul/temperature/items/[item].json`
> "Make diamond armor warmer instead of cooling"
> "Add temperature values for a new armor set"

**Thirst values:** `minecraft/config/paxi/datapacks/legendarysurvival_config/data/[mod]/legendarysurvivaloverhaul/thirst/consumables/[item].json`
> "Make whiskey not cause the thirst debuff"
> "Increase the hydration from golden apples"

**Global survival settings:** `minecraft/config/legendarysurvivaloverhaul/legendarysurvivaloverhaul-common.toml`
> "Disable the temperature system entirely"
> "Enable the body damage system"
> "Change difficulty from NORMAL to EASY"

### Modifying Combat Settings

**Weapon animations:** `minecraft/config/paxi/datapacks/Otherworld_Better_Combat/data/[mod]/weapon_attributes/[weapon].json`
> "Increase the attack range of the Valkyrie Lance from 6.5 to 8"
> "Change the Dragonsteel Sword to one-handed"

**Global combat settings:** `minecraft/config/bettercombat/server.json5`
> "Allow hitting more enemies with sweep attacks"
> "Remove the movement speed penalty while attacking"
> "Increase dual-wield attack speed bonus"

### Modifying Bounties & Gateways

**Bounty objectives/rewards:** `minecraft/config/paxi/datapacks/Otherworld_Loot_Tweaks/data/extrabounties/bounty_decrees/`
> "Add a new bounty for killing Ender Dragons"

**Gateway difficulty:** `minecraft/config/paxi/datapacks/Otherworld_Loot_Tweaks/data/extrabounties/gateways/`
> "Make the large gateways spawn fewer mobs per wave"
> "Increase gateway rewards"

### Modifying Tags

**Item/damage tags:** `minecraft/config/paxi/datapacks/Otherworld_Tags/data/[namespace]/tags/`
> "Add a new armor set to the boots tag"
> "Make a new spell type bypass armor"

### General Tips for Asking Claude Code

1. **Be specific about the item/mob/setting** — Use the actual mod name and item name when possible
2. **Describe the desired outcome** — "I want zombies to be weaker" is clearer than "change zombie settings"
3. **Mention the mod** if you know it — "The Apotheosis gem drop rate" is easier to find than "gem drop rate"
4. **For new recipes** — Describe the grid layout, ingredients, and result
5. **After changes** — Restart Minecraft for config changes to take effect. Datapack changes may require `/reload` in-game

### Quick Reference: File Locations

| System | Config Location |
|--------|----------------|
| Custom recipes | `config/paxi/datapacks/Otherworld_Recipes/data/` |
| Apotheosis affixes | `config/paxi/datapacks/Otherworld_Apotheosis/data/apotheosis/affixes/` |
| Apotheosis gems | `config/paxi/datapacks/Otherworld_Apotheosis/data/apotheosis/gems/` |
| Apotheosis rarities | `config/paxi/datapacks/Otherworld_Apotheosis/data/apotheosis/rarities/` |
| Apotheosis global | `config/apotheosis/adventure.cfg` |
| Mob leveling (per-mob) | `config/paxi/datapacks/Otherworld_Autoleveling/data/[mod]/leveling_settings/` |
| Mob leveling (global) | `config/autoleveling-common.toml` |
| Combat animations | `config/paxi/datapacks/Otherworld_Better_Combat/data/[mod]/weapon_attributes/` |
| Combat settings | `config/bettercombat/server.json5` |
| Bounties | `config/paxi/datapacks/Otherworld_Loot_Tweaks/data/extrabounties/` |
| Gateways | `config/paxi/datapacks/Otherworld_Loot_Tweaks/data/extrabounties/gateways/` |
| Loot tables | `config/paxi/datapacks/Otherworld_Loot_Tweaks/data/[mod]/loot_tables/` |
| Tags | `config/paxi/datapacks/Otherworld_Tags/data/[namespace]/tags/` |
| Temperature items | `config/paxi/datapacks/legendarysurvival_config/data/[mod]/legendarysurvivaloverhaul/temperature/` |
| Thirst items | `config/paxi/datapacks/legendarysurvival_config/data/[mod]/legendarysurvivaloverhaul/thirst/` |
| Survival global | `config/legendarysurvivaloverhaul/legendarysurvivaloverhaul-common.toml` |
| Balance fixes | `config/paxi/datapacks/Otherworld_Fixes.zip` |

> All paths are relative to the `minecraft/` directory in the pack root.
