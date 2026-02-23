# How to Modify Settings with Claude Code

You can ask Claude Code to modify any setting in this modpack. Here's how to request changes for each system.

---

## Modifying Crafting Recipes

**Recipe files location:** `minecraft/config/paxi/datapacks/Otherworld_Recipes/data/[mod]/recipes/[item].json`

**To change an existing recipe, ask:**

> "Change the Eye of Nothingness recipe to use diamonds instead of crying obsidian"

**To add a new recipe, ask:**

> "Add a new crafting recipe for [item] that uses [ingredients]"

### Shaped Recipe Format

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

### Shapeless Recipe Format

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

---

## Modifying Mob Levels (Autoleveling)

**Per-entity config:** `minecraft/config/paxi/datapacks/Otherworld_Autoleveling/data/[mod]/leveling_settings/entities/[mob].json`

**Example requests:**

> "Make zombies start at level 5 instead of level 1"
>
> "Reduce the Ender Dragon's level from 25 to 15"
>
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
>
> "Increase attack damage bonus per level from 0.2 to 0.5"

---

## Modifying Apotheosis Loot (Rarities, Affixes, Gems)

**Rarity weights:** `minecraft/config/paxi/datapacks/Otherworld_Apotheosis/data/apotheosis/rarities/`

> "Make Mythic items twice as common" → Double the weight value in mythic.json

**Affix values:** `minecraft/config/paxi/datapacks/Otherworld_Apotheosis/data/apotheosis/affixes/[type]/`

> "Increase the Piercing affix armor bypass from 2.0 to 3.0"

**Gem bonuses:** `minecraft/config/paxi/datapacks/Otherworld_Apotheosis/data/apotheosis/gems/`

> "Make the Inferno gem give more fire damage"

**Global adventure settings:** `minecraft/config/apotheosis/adventure.cfg`

> "Increase the chance of mobs spawning with magical gear from 7.5% to 15%"
>
> "Make bosses spawn more frequently"

---

## Modifying Temperature & Thirst

**Armor temperature:** `minecraft/config/paxi/datapacks/legendarysurvival_config/data/[mod]/legendarysurvivaloverhaul/temperature/items/[item].json`

> "Make diamond armor warmer instead of cooling"
>
> "Add temperature values for a new armor set"

**Thirst values:** `minecraft/config/paxi/datapacks/legendarysurvival_config/data/[mod]/legendarysurvivaloverhaul/thirst/consumables/[item].json`

> "Make whiskey not cause the thirst debuff"
>
> "Increase the hydration from golden apples"

**Global survival settings:** `minecraft/config/legendarysurvivaloverhaul/legendarysurvivaloverhaul-common.toml`

> "Disable the temperature system entirely"
>
> "Enable the body damage system"
>
> "Change difficulty from NORMAL to EASY"

---

## Modifying Combat Settings

**Weapon animations:** `minecraft/config/paxi/datapacks/Otherworld_Better_Combat/data/[mod]/weapon_attributes/[weapon].json`

> "Increase the attack range of the Valkyrie Lance from 6.5 to 8"
>
> "Change the Dragonsteel Sword to one-handed"

**Global combat settings:** `minecraft/config/bettercombat/server.json5`

> "Allow hitting more enemies with sweep attacks"
>
> "Remove the movement speed penalty while attacking"
>
> "Increase dual-wield attack speed bonus"

---

## Modifying Bounties & Gateways

**Bounty objectives/rewards:** `minecraft/config/paxi/datapacks/Otherworld_Loot_Tweaks/data/extrabounties/bounty_decrees/`

> "Add a new bounty for killing Ender Dragons"

**Gateway difficulty:** `minecraft/config/paxi/datapacks/Otherworld_Loot_Tweaks/data/extrabounties/gateways/`

> "Make the large gateways spawn fewer mobs per wave"
>
> "Increase gateway rewards"

---

## Modifying Tags

**Item/damage tags:** `minecraft/config/paxi/datapacks/Otherworld_Tags/data/[namespace]/tags/`

> "Add a new armor set to the boots tag"
>
> "Make a new spell type bypass armor"

---

## General Tips

1. **Be specific about the item/mob/setting** — Use the actual mod name and item name when possible
2. **Describe the desired outcome** — "I want zombies to be weaker" is clearer than "change zombie settings"
3. **Mention the mod** if you know it — "The Apotheosis gem drop rate" is easier to find than "gem drop rate"
4. **For new recipes** — Describe the grid layout, ingredients, and result
5. **After changes** — Restart Minecraft for config changes to take effect. Datapack changes may require `/reload` in-game

---

## Quick Reference: File Locations

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
