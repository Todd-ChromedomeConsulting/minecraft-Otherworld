# Temperature & Thirst

**Datapack:** `legendarysurvival_config`

Configures the Legendary Survival Overhaul mod which adds temperature management and thirst/hydration mechanics. You need to stay warm/cool and drink water to survive.

---

## Temperature System

Every piece of armor has a temperature value. Positive = warming, negative = cooling.

### Armor Temperature Values

| Armor Type | Temperature | Best For |
|------------|-------------|----------|
| Leather | +1.0 (warm) | Cold biomes |
| Gold | +1.0 (warm) | Cold biomes |
| Iron | -0.5 (cool) | Hot biomes |
| Diamond | -1.0 (cold) | Hot biomes/Nether |
| Netherite | +1.5 (very warm) | Cold biomes |
| Ice Dragonsteel | -2.5 (very cold) | Nether/deserts |
| Fire Dragonsteel | +2.5 (very hot) | Cold biomes/mountains |

### Temporary Heating/Cooling Items

| Item | Effect | Duration |
|------|--------|----------|
| Charcoal Block | Heating | 4.5 minutes |
| Ice Block | Cooling | 30 seconds |
| Blue Ice | Cooling | 30 seconds |
| Packed Ice | Cooling | 30 seconds |
| Snowball | Cooling | 30 seconds |

---

## Thirst System

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

---

## Key Config Settings

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

---

## Config Files

| Config | Location |
|--------|----------|
| Per-item temperature/thirst | `legendarysurvival_config/data/[mod]/legendarysurvivaloverhaul/` |
| Global survival settings | `minecraft/config/legendarysurvivaloverhaul/legendarysurvivaloverhaul-common.toml` |
