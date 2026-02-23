# Mob Scaling System

**Datapack:** `Otherworld_Autoleveling`

Makes mobs get stronger the further you travel from spawn and the deeper you go underground. Also scales mobs differently per dimension. This is the core difficulty scaling system.

---

## How Leveling Works

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

---

## Dimension Scaling

| Dimension | Starting Level | Max Level | Scaling |
|-----------|---------------|-----------|---------|
| **Overworld** | 1 | 12 | Slow (0.0001/block distance, 0.02/block depth) |
| **The Nether** | 8 | 12 | Fast (0.01/block distance & depth) |
| **The End** | 20 | 20 | Fixed (no scaling, everything is max) |
| **The Aether** | 6 | 6 | Minimal (0.001/block) |
| **Minecells Ramparts** | 10 | 10 | Fixed |
| **Minecells Crypt** | 12 | 12 | Fixed |

---

## Boss Entity Levels

| Boss | Starting Level | Max Level | Notes |
|------|---------------|-----------|-------|
| Ender Dragon | 25 | 25 | Fixed, +9.7% per level to all stats |
| Ice/Fire/Lightning Dragon | 15 | 20 | Scales with distance, +10% damage, +2.5% health per level |
| Lich (Soulslike Weaponry) | 20 | 20 | Fixed |
| Leviathan (Cataclysm) | 15 | 20 | Scales with depth |
| Champion Goblin | 10 | 12 | +0-1 random bonus levels |
| Orc Boss | 4 | 12 | +0-3 random bonus levels |

---

## Supported Mods (28 namespaces)

Minecraft (vanilla), Aether, Alex's Caves, Alex's Mobs, Ancient Aether, Animated Mobs, Aquamirae, Born in Chaos, Bosses of Mass Destruction, Cataclysm, Dark Doppelganger, EEEAB's Mobs, Eidolon, Goblins Tyranny, Ice and Fire, Iron's Spellbooks, Legendary Monsters, Lost Aether Content, Minecells, Mobs of Mythology, Mowzie's Mobs, Realm RPG Demons, Realm RPG Quests, Rotten Creatures, Soulslike Weaponry, The Orcs, Traveloptics, Valoria

---

## Config Files

| Config | Location |
|--------|----------|
| Global settings | `minecraft/config/autoleveling-common.toml` |
| Per-entity configs | `Otherworld_Autoleveling/data/[mod]/leveling_settings/entities/[mob].json` |
| Per-dimension configs | `Otherworld_Autoleveling/data/[mod]/leveling_settings/dimensions/[dimension].json` |
