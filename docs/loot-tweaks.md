# Bounties, Gateways & Loot

**Datapack:** `Otherworld_Loot_Tweaks`

This is the largest datapack. It sets up the bounty/quest system (Extra Bounties mod), wave-based mob arenas (Gateways), and modifies loot tables across multiple mods.

---

## Bounty System (58 mod integrations)

The bounty system gives players quests to complete for rewards. Bounty decrees are found in villages and define what quests are available.

### How Bounties Work

1. Find a Bounty Board in a village
2. Pick up a Bounty Decree (quest contract)
3. Complete objectives (kill mobs, gather items, etc.)
4. Return for rewards (coins, rare items, etc.)

### Currency

Uses Numismatic Overhaul coins:

- **Bronze coins** (1-99, common reward)
- **Silver coins** (1-48, worth 100 bronze each)
- **Gold coins** (1-8, worth 5000 bronze each, rare)

### Supported Mods

Create (6 different categories), Iron's Spellbooks, Ice and Fire, Alex's Mobs, Mowzie's Mobs, Farmer's Delight, Sophisticated Storage/Backpacks, Powah, and 45+ more.

---

## Gateway Arenas (225 configurations)

Gateways are wave-based mob arenas in 3 sizes:

| Size | Mobs per Wave | Loot Rolls | Waves |
|------|--------------|------------|-------|
| **Small** | 3-7 | 10 | 5 |
| **Medium** | 6-14 | 20 | 5 |
| **Large** | 9-21 | 30 | 5 |

### Wave Difficulty Scaling

Each wave gets progressively harder:

| Wave | Armor Bonus | Health/Damage Bonus | Notes |
|------|-------------|---------------------|-------|
| 1 | — | — | Normal stats |
| 2 | +6 | +45% | — |
| 3 | +9 | +60% | Faster |
| 4 | +15 | +75-90% | — |
| 5 | +15 | +105% health, +150% damage | Final wave |

Covers all standard Minecraft mobs (cow, pig, sheep, creeper, skeleton, zombie, etc.)

---

## Level-Scaled Healing Drops

Leveled mobs drop healing items based on their level (2% base chance):

| Mob Level | Drop |
|-----------|------|
| 1-7 | Healing Vial (Valoria) |
| 8-14 | Healing Flask (Valoria) |
| 15+ | Healing Elixir (Valoria) |

---

## Void Cathedral Loot

The Traveloptics Void Cathedral has a custom high-tier loot table including:

- Arcane Essence (8-16)
- Enchanted netherite swords (level 20-39 enchantments)
- Enchanted diamond/iron armor
- Ender school spell scrolls
- Various building materials and rare items

---

## Config Files

| Config | Location |
|--------|----------|
| Bounty decrees | `Otherworld_Loot_Tweaks/data/extrabounties/bounty_decrees/` |
| Bounty pools | `Otherworld_Loot_Tweaks/data/extrabounties/bounty_pools/` |
| Gateways | `Otherworld_Loot_Tweaks/data/extrabounties/gateways/` |
| Loot tables | `Otherworld_Loot_Tweaks/data/[mod]/loot_tables/` |
