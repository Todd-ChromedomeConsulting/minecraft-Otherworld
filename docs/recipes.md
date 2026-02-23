# Custom Crafting Recipes

**Datapack:** `Otherworld_Recipes`

This datapack adds 2 custom shaped crafting recipes for items that either didn't have recipes or had recipes the pack author wanted to change.

---

## Recipe 1: Eye of Nothingness (Traveloptics)

A powerful teleportation/dimension item.

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

**File:** `Otherworld_Recipes/data/traveloptics/recipes/eye_of_nothingness.json`

---

## Recipe 2: Blackstone Pedestal (Soulslike Weaponry)

A crafting station used for boss weapon creation.

```
┌───┬───┬───┐
│ I │ L │ I │  I = Moonstone (Soulslike Weaponry)
├───┼───┼───┤  L = Lord Soul Purple (Soulslike Weaponry boss drop)
│ X │ Y │ X │  X = Ender Pearl
├───┼───┼───┤  Y = Obsidian
│ O │ O │ O │  O = Polished Blackstone Bricks
└───┴───┴───┘
→ 1x Blackstone Pedestal
```

**File:** `Otherworld_Recipes/data/soulsweapons/recipes/blackstone_pedestal.json`

---

## Spawner Modification Recipes (Apotheosis)

These are "use item on spawner" recipes, not crafting table recipes:

| Action | Item Used | Effect |
|--------|-----------|--------|
| Right-click spawner | Dragon Egg | Spawner ignores all spawn conditions |
| Right-click spawner | Soul Lantern | Spawner ignores light level |
| Right-click spawner | Clock | Reduces max spawn delay by 10 |
| Right-click spawner | Fermented Spider Eye | Increases spawn count by 1 |

See [Apotheosis](apotheosis.md#spawner-modification-recipes) for full details on the 24 spawner recipes.

---

## Disabled Recipes

The following recipes are intentionally disabled in this pack:

- **Iron's Spellbooks ward rings** (Fireward, Frostward, Poisonward) — disabled in Loot Tweaks
- **BetterNether Flaming Ruby equipment** — disabled in [Balance Patches](fixes.md)
- **Apotheosis elongated sword affix** — disabled in Better Combat pack
