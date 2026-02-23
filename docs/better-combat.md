# Combat System — Weapon Animation Overhaul

**Datapack:** `Otherworld_Better_Combat`

Defines custom attack animations, combo chains, attack ranges, and hitbox shapes for modded weapons. This makes combat feel like an action RPG instead of vanilla Minecraft clicking.

---

## Weapon Categories

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

---

## Combo Chains

### Claymore (3 hits)

Horizontal Slash → Stab → Overhead Slam (0.75x → 1.0x → 1.25x damage)

### Double Axe (4 hits)

Right Slash → Left Slash → Right Slash → 360° Spin (all 1.0x damage)

### Hammer (3 hits)

Light Slam → Medium Slam → Heavy Slam (0.8x → 0.9x → 1.2x damage)

### Lance

Changes animation based on mounted vs. on foot.

---

## Key Config Settings

**File:** `minecraft/config/bettercombat/server.json5`

| Setting | Value | What It Means |
|---------|-------|---------------|
| Upswing multiplier | 0.5 | Attacks start fast (50% wind-up) |
| Max sweep targets | 4 | Hit up to 4 enemies before damage penalty |
| Sweep damage penalty | 50% max | Extra targets take up to 50% less damage |
| Movement while attacking | 50% speed | You slow down while swinging |
| Dual wield attack speed bonus | +20% | Dual wielding is faster |
| Combo reset | 3x weapon cooldown | Stop attacking to reset combo |

---

## Mods Covered

- **Aether** — Valkyrie Lance
- **Ice and Fire** — All dragonsteel + troll weapons
- **Aquamirae** — All weapons
- **MalfuCombatDatapack** — Cataclysm, Simply Swords, and more (647 files)
