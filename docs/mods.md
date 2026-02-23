# Mod List

Otherworld [Dungeons & Dragons] includes **~392 mods** on Minecraft 1.20.1 (Forge 47.4.13). This page lists every mod in the pack alphabetically, with detailed configuration notes for mods that have been customized.

---

## Mods with Custom Configuration

These mods have pack-specific settings that differ from their defaults. Click through for detailed breakdowns.

| Mod | What's Customized | Details |
|-----|-------------------|---------|
| [Apotheosis](apotheosis.md) | Loot rarities, 80+ affixes, 20+ gems, spawner recipes | Full wiki page |
| [Auto Leveling](autoleveling.md) | Per-mob/dimension scaling, stat bonuses per level | Full wiki page |
| [Better Combat](better-combat.md) | Weapon animations, combo chains, hitboxes | Full wiki page |
| [Bountiful / Extra Bounties](loot-tweaks.md) | 58 mod integrations, bounty rewards | Full wiki page |
| [ItemPhysic Full](#itemphysic-full) | Item rendering, pickup, floating, burning, throwing | Detailed below |
| [Legendary Survival Overhaul](survival.md) | Temperature and thirst values | Full wiki page |

---

## ItemPhysic Full

**Author:** CreativeMD | [CurseForge](https://www.curseforge.com/minecraft/mc-mods/itemphysic)

ItemPhysic overhauls how dropped items behave in the world. Instead of floating and spinning in the air (vanilla), items lay flat on the ground with realistic physics. It also adds systems for item buoyancy, combustion, indestructibility, pickup behavior, and throwing.

### Config Files

| File | Controls |
|------|----------|
| `minecraft/config/itemphysic.json` | Server-side behavior (physics, pickup, throw, item lists) |
| `minecraft/config/itemphysic-client.json` | Client-side rendering (visuals, tooltips, HUD) |

### General Settings (`itemphysic.json` > `general`)

| Setting | Value | What It Does |
|---------|-------|-------------|
| `fallSounds` | `true` | Dropped items make a sound when they hit the ground |
| `disableCactusDamage` | `true` | Dropped items won't be destroyed by cacti |

### Swimming Items (floating on water)

Items on the `swimmingItems` whitelist **float on water** instead of sinking. In this pack, the following item types float:

- Wood-related: logs, planks, doors, boats, fences (anything in `mineable/axe`)
- Nature: leaves, flowers, crops, seeds, snow, cactus, cobweb
- Light items: bows, arrows, feathers, paintings, saddles, bones, eggs
- Food: apples, bread, wheat, mutton, rabbit, beetroot, cake, melon, potatoes
- Equipment: shields, elytra, fishing rods, shears, bowls
- Misc: snowballs, sponges, ice

### Burning Items (destroyed by fire/lava)

Items on the `burningItems` whitelist **burn up when thrown into fire or lava**. This list is similar to swimming items but also includes:

- Leather and leather armor
- Paper, books, written books, maps, enchanted books
- Leads, name tags
- All fuel items (anything tagged as fuel)
- Spider eyes, rotten flesh
- Wool and wool carpets

### Indestructible Items

These items **cannot be destroyed by any means** (fire, lava, explosions, void, etc.):

- Nether Star
- Bedrock
- Obsidian
- Barrier

### Pickup Settings (`itemphysic.json` > `pickup`)

!!! note "Modified in this pack"
    Custom pickup has been **disabled** — items use default Minecraft walk-over auto-pickup.

| Setting | Value | What It Does |
|---------|-------|-------------|
| `customPickup` | `false` | Right-click pickup system (disabled) |
| `pickupWhenSneaking` | `true` | Can pick up items by sneaking near them |
| `pickupNormally` | `true` | Default walk-over auto-pickup (enabled) |
| `maximumPickupRange` | `5` | Maximum distance (blocks) to pick up items |
| `hitboxIncrease` | `0.2` | Extra hitbox size for pickup detection |

The `alwaysPickup` whitelist (coins, healing items, gems, tools, blocks) was used when custom pickup was active to auto-collect important drops. With normal pickup restored, this list has no effect.

### Throw Settings (`itemphysic.json` > `throw`)

| Setting | Value | What It Does |
|---------|-------|-------------|
| `enabled` | `true` | Hold the drop key to charge and throw items like projectiles |
| `maxStages` | `6` | Maximum charge levels (longer hold = further throw) |
| `multiplierPerStage` | `1` | Force multiplier per charge stage |
| `stageChargeTime` | `10` | Ticks (0.5 sec) per charge stage |

### Client Rendering Settings (`itemphysic-client.json`)

| Setting | Value | What It Does |
|---------|-------|-------------|
| `oldRotation` | `false` | Use new-style item rotation when falling |
| `vanillaRendering` | `false` | Items **lay flat on the ground** instead of vanilla spinning/hovering |
| `rotateSpeed` | `1.0` | How fast items spin while falling |
| `showPickupTooltip` | `false` | Show item name when looking at dropped items |
| `showPickupTooltipOnlyOnGround` | `false` | Only show tooltip for grounded items |
| `showPickupTooltipExtended` | `false` | Show extended info in tooltip |
| `showPickupTooltipKeybind` | `false` | Show keybind hint in tooltip |
| `disableThrowHUD` | `true` | Hide the throw charge meter HUD |
| `tooltipOffsetX` | `0` | Tooltip horizontal offset |
| `tooltipOffsetY` | `0` | Tooltip vertical offset |
| `blockRequireOffset` | snow, soul sand | Blocks needing special render offset for items resting on them |

---

## Complete Mod List

| Mod | Author(s) |
|-----|-----------|
| [Abridged](https://www.curseforge.com/minecraft/mc-mods/abridged) | Apollo |
| [Additional Attributes](https://www.curseforge.com/minecraft/mc-mods/additional-attributes) | Cadentem |
| [Advanced Loot Info](https://www.curseforge.com/minecraft/mc-mods/advanced-loot-info) | yanny7777 |
| [AeroBlender](https://www.curseforge.com/minecraft/mc-mods/aeroblender) | TeamRazor, 345boneshoss, dark_sonic_300, TunefulTurnip |
| [Aether Villages](https://www.curseforge.com/minecraft/mc-mods/aether-villages) | Aureljz, diamondtown_ |
| [Aether: Lost Content Addon](https://www.curseforge.com/minecraft/mc-mods/aether-lost-content) | ModdingLegacy, Lachney, Jorge_Sunspirit, KingPhygieBoo |
| [Alex's Caves](https://www.curseforge.com/minecraft/mc-mods/alexs-caves) | sbom_xela |
| [Alex's Delight](https://www.curseforge.com/minecraft/mc-mods/alexs-delight) | Baisylia, NCP_Bails |
| [Alex's Mobs](https://www.curseforge.com/minecraft/mc-mods/alexs-mobs) | sbom_xela |
| [AllTheLeaks (Memory Leak Fix)](https://www.curseforge.com/minecraft/mc-mods/alltheleaks) | Uncandango |
| [Alshanex's Familiars](https://www.curseforge.com/minecraft/mc-mods/alshanexs-familiars) | alshanex |
| [Alternate Current](https://www.curseforge.com/minecraft/mc-mods/alternate-current) | SpaceWalkerRS |
| [Alternate Origin GUI](https://www.curseforge.com/minecraft/mc-mods/altorigingui) | UltrusBot |
| [Ancient Aether](https://www.curseforge.com/minecraft/mc-mods/ancient-aether) | Builderdog841 |
| [Ancient Reforging](https://www.curseforge.com/minecraft/mc-mods/ancient-reforging) | ianm1647 |
| [Apotheosis](https://www.curseforge.com/minecraft/mc-mods/apotheosis) | Shadows_of_Fire |
| [Apothic Attributes](https://www.curseforge.com/minecraft/mc-mods/apothic-attributes) | Shadows_of_Fire |
| [AppleSkin](https://www.curseforge.com/minecraft/mc-mods/appleskin) | squeek502 |
| [Aquamirae (Forge)](https://www.curseforge.com/minecraft/mc-mods/aquamirae) | Obscuria |
| [Architectury API](https://www.curseforge.com/minecraft/mc-mods/architectury-api) | shedaniel, MaxNeedsSnacks, Juicebus |
| [(ARCHIVE) Faster Random](https://www.curseforge.com/minecraft/mc-mods/faster-random) | AnOpenSauceDev |
| [Ash API](https://www.curseforge.com/minecraft/mc-mods/ash-api) | Trikzon |
| [Athena](https://www.curseforge.com/minecraft/mc-mods/athena) | terrariumearth, ThatGravyBoat, CodexAdrian |
| [AttributeFix](https://www.curseforge.com/minecraft/mc-mods/attributefix) | DarkhaxDev |
| [Auto Leveling](https://www.curseforge.com/minecraft/mc-mods/auto-leveling) | Daripher |
| [AzureLib](https://www.curseforge.com/minecraft/mc-mods/azurelib) | AzureDoomC |
| [BadOptimizations](https://www.curseforge.com/minecraft/mc-mods/badoptimizations) | thosea |
| [BaguetteLib](https://www.curseforge.com/minecraft/mc-mods/baguettelib) | Project8gbDeRam |
| [Balm](https://www.curseforge.com/minecraft/mc-mods/balm) | BlayTheNinth |
| [BCLib](https://www.curseforge.com/minecraft/mc-mods/bclib) | Quiqueck |
| [Beautiful Enchanted Books](https://www.curseforge.com/minecraft/mc-mods/beautiful-enchanted-books) | Lupin, Cerbon |
| [Bee Fix](https://www.curseforge.com/minecraft/mc-mods/bee-fix) | MacTso, lupicus |
| [Better Advancements](https://www.curseforge.com/minecraft/mc-mods/better-advancements) | way2muchnoise |
| [Better Clouds](https://www.curseforge.com/minecraft/mc-mods/better-clouds) | Qendolin |
| [Better Combat](https://www.curseforge.com/minecraft/mc-mods/better-combat-by-daedelus) | daedelus_dev |
| [Better Combat Particle](https://www.curseforge.com/minecraft/mc-mods/better-combat-particle) | Malfu |
| [Better Combat x Apotheosis Compat](https://www.curseforge.com/minecraft/mc-mods/apothic-combat) | MuonR |
| [Better Compatibility Checker](https://www.curseforge.com/minecraft/mc-mods/better-compatibility-checker) | Gaz_ |
| [Better Mods Button](https://www.curseforge.com/minecraft/mc-mods/better-mods-button) | Fuzs, SHXRKIE |
| [Better World Loading](https://www.curseforge.com/minecraft/mc-mods/better-world-loading-forge) | h1ggsk |
| [BetterEnd](https://www.curseforge.com/minecraft/mc-mods/betterend) | Quiqueck |
| [Biome Music](https://www.curseforge.com/minecraft/mc-mods/biome-music) | someaddon |
| [BiomeSpy](https://www.curseforge.com/minecraft/mc-mods/biomespy) | moepus |
| [BisectHosting Server Integration Menu](https://www.curseforge.com/minecraft/mc-mods/bisecthosting-server-integration-menu-forge) | BisectHosting |
| [BlockUI](https://www.curseforge.com/minecraft/mc-mods/blockui) | Raycoms, OrionOnline, someaddon, Nightenom |
| [Bookshelf](https://www.curseforge.com/minecraft/mc-mods/bookshelf) | DarkhaxDev |
| [Born in Chaos](https://www.curseforge.com/minecraft/mc-mods/born-in-chaos) | mongoose_artist |
| [Born In Configuration](https://www.curseforge.com/minecraft/mc-mods/born-in-configuration) | CrimsonCrips |
| [Boss Ultimatum](https://www.curseforge.com/minecraft/mc-mods/boss-ultimatum) | ElocinDev |
| [Bosses of Mass Destruction](https://www.curseforge.com/minecraft/mc-mods/bosses-of-mass-destruction-forge) | Cerbon |
| [Bountiful](https://www.curseforge.com/minecraft/mc-mods/bountiful) | Ejektaflex |
| [Bountiful Villager](https://www.curseforge.com/minecraft/mc-mods/bountiful-villager) | P1nero |
| [Brewin' And Chewin'](https://www.curseforge.com/minecraft/mc-mods/brewin-and-chewin) | lumpazl, Probleyes, Farcr, RaymondBlaze, ChrysanthCow |
| [Butchery](https://www.curseforge.com/minecraft/mc-mods/butchery) | jmods |
| [Byzantine Styles Pack for Minecolonies](https://www.curseforge.com/minecraft/mc-mods/byzantine-styles-pack-for-minecolonies) | spumantii |
| [Caelus API](https://www.curseforge.com/minecraft/mc-mods/caelus) | TheIllusiveC4 |
| [Carry On](https://www.curseforge.com/minecraft/mc-mods/carry-on) | Tschipp, Purplicious_Cow_ |
| [CERBON's API](https://www.curseforge.com/minecraft/mc-mods/cerbons-api) | Cerbon |
| [Cerulean](https://www.curseforge.com/minecraft/mc-mods/cerulean) | Txni |
| [Certain Questing Additions](https://www.curseforge.com/minecraft/mc-mods/certain-questing-additions) | HollowHorizon |
| [Champions Unofficial](https://www.curseforge.com/minecraft/mc-mods/champions-unofficial) | kyogi, PickAID |
| [Charm of Undying](https://www.curseforge.com/minecraft/mc-mods/charm-of-undying) | TheIllusiveC4 |
| [Chipped](https://www.curseforge.com/minecraft/mc-mods/chipped) | terrariumearth, AlexNijjar |
| [Chunk Sending](https://www.curseforge.com/minecraft/mc-mods/chunk-sending-forge-fabric) | someaddon |
| [Citadel](https://www.curseforge.com/minecraft/mc-mods/citadel) | sbom_xela |
| [Client Crafting](https://www.curseforge.com/minecraft/mc-mods/client-crafting) | someaddon |
| [Climate Rivers](https://www.curseforge.com/minecraft/mc-mods/climate-rivers) | Fuzs |
| [Cloth Config API](https://www.curseforge.com/minecraft/mc-mods/cloth-config) | shedaniel, LinkieIsBetterThanK9 |
| [Collective](https://www.curseforge.com/minecraft/mc-mods/collective) | Serilum |
| [Colorwheel](https://www.curseforge.com/minecraft/mc-mods/colorwheel) | djefrey |
| [Colorwheel Patcher](https://www.curseforge.com/minecraft/mc-mods/colorwheel-patcher) | djefrey |
| [Comforts](https://www.curseforge.com/minecraft/mc-mods/comforts) | TheIllusiveC4 |
| [Compatibility addon for MineColonies](https://www.curseforge.com/minecraft/mc-mods/minecolonies-compatibility) | gisellevonbingen |
| [Configured Defaults](https://www.curseforge.com/minecraft/mc-mods/configured-defaults) | Fuzs, SHXRKIE |
| [Connectivity](https://www.curseforge.com/minecraft/mc-mods/connectivity) | someaddon |
| [Connector Extras](https://www.curseforge.com/minecraft/mc-mods/connector-extras) | Su5eD |
| [Continuity](https://www.curseforge.com/minecraft/mc-mods/continuity) | Pepper_Bell |
| [Controlling](https://www.curseforge.com/minecraft/mc-mods/controlling) | Jaredlll08 |
| [CorgiLib](https://www.curseforge.com/minecraft/mc-mods/corgilib) | Corgi_Taco, JT122406 |
| [Corpse](https://www.curseforge.com/minecraft/mc-mods/corpse) | henkelmax |
| [Corpse x Curios API Compat](https://www.curseforge.com/minecraft/mc-mods/corpse-x-curios-api-compat) | Project8gbDeRam |
| [CoroUtil](https://www.curseforge.com/minecraft/mc-mods/coroutil) | Corosus |
| [Crash Assistant](https://www.curseforge.com/minecraft/mc-mods/crash-assistant) | KostromDan |
| [CrashExploitFixer](https://www.curseforge.com/minecraft/mc-mods/crashexploitfixer) | drexhd |
| [CraterLib](https://www.curseforge.com/minecraft/mc-mods/craterlib) | HypherionSA |
| [Create](https://www.curseforge.com/minecraft/mc-mods/create) | simibubi |
| [Create Better FPS](https://www.curseforge.com/minecraft/mc-mods/create-better-fps) | moepus |
| [Create Contraption Terminals](https://www.curseforge.com/minecraft/mc-mods/create-contraption-terminals) | tom54541 |
| [Create Slice & Dice](https://www.curseforge.com/minecraft/mc-mods/slice-and-dice) | possible_triangle |
| [Create: Alex's Caves Compat](https://www.curseforge.com/minecraft/mc-mods/create-alexs-caves-compat) | SkellaTex |
| [Create: Central Kitchen](https://www.curseforge.com/minecraft/mc-mods/create-central-kitchen) | DragonsPlus, RaymondBlaze, MarbleGate |
| [Create: Dynamic Village](https://www.curseforge.com/minecraft/mc-mods/dynamic-village) | a0a7, Fatasiangamer, rdh |
| [Create: Enchantment Industry](https://www.curseforge.com/minecraft/mc-mods/create-enchantment-industry) | DragonsPlus, MarbleGate, RaymondBlaze |
| [Create: Wizardry](https://www.curseforge.com/minecraft/mc-mods/create-wizardry) | thetruezeraora |
| [CreativeCore](https://www.curseforge.com/minecraft/mc-mods/creativecore) | CreativeMD |
| [Cupboard](https://www.curseforge.com/minecraft/mc-mods/cupboard) | someaddon |
| [Curios API](https://www.curseforge.com/minecraft/mc-mods/curios) | TheIllusiveC4 |
| [Cursors Extended](https://www.curseforge.com/minecraft/mc-mods/minecraft-cursor) | fishstiz |
| [Dark Doppelganger](https://www.curseforge.com/minecraft/mc-mods/dark-doppelganger) | Bandit_Bytes |
| [Dark Window Bar](https://www.curseforge.com/minecraft/mc-mods/dark-window-bar) | Txni |
| [Despawn Tweaks](https://www.curseforge.com/minecraft/mc-mods/despawn-tweaks) | Txni |
| [Difficult Spawners](https://www.curseforge.com/minecraft/mc-mods/difficult-spawners) | InfernalEclipse |
| [Dimensional Sync Fixes](https://www.curseforge.com/minecraft/mc-mods/dimensional-sync-fixes) | _nArUTo_, 332iBnaiJ |
| [Distraction Free Recipes](https://www.curseforge.com/minecraft/mc-mods/distraction-free-recipes) | Txni |
| [Domum Ornamentum](https://www.curseforge.com/minecraft/mc-mods/domum-ornamentum) | OrionOnline, Raycoms |
| [Draconic Codex](https://www.curseforge.com/minecraft/mc-mods/draconic-codex-expansion-of-the-ancient-tome-from-quark) | Yoda_Legion |
| [Drippy Loading Screen](https://www.curseforge.com/minecraft/mc-mods/drippy-loading-screen) | Keksuccino |
| [Dungeons Delight](https://www.curseforge.com/minecraft/mc-mods/dungeons-delight) | Yirmiri |
| [Dungeons Enhanced](https://www.curseforge.com/minecraft/mc-mods/dungeonsenhanced) | Valarauko9 |
| [Easy Anvils](https://www.curseforge.com/minecraft/mc-mods/easy-anvils) | Fuzs |
| [EEEAB's Mobs](https://www.curseforge.com/minecraft/mc-mods/eeeabs-mobs) | EEEAB |
| [Elytra Slot](https://www.curseforge.com/minecraft/mc-mods/elytra-slot) | TheIllusiveC4 |
| [Embeddium (Rubidium) Extra](https://www.curseforge.com/minecraft/mc-mods/rubidium-extra) | dima_dencep |
| [Ember's Underground Rooms](https://www.curseforge.com/minecraft/mc-mods/embers-underground-rooms) | ember_slvtr |
| [EMF Entity Model Features](https://www.curseforge.com/minecraft/mc-mods/entity-model-features) | Traben |
| [Enchantment Descriptions](https://www.curseforge.com/minecraft/mc-mods/enchantment-descriptions) | DarkhaxDev |
| [Ender's Delight](https://www.curseforge.com/minecraft/mc-mods/enders-delight) | Furti_Two, Ax3dGaming_ |
| [Entity Culling](https://www.curseforge.com/minecraft/mc-mods/entityculling) | tr7zw |
| [EpheroLib](https://www.curseforge.com/minecraft/mc-mods/epherolib) | thethonk |
| [Equipment Compare](https://www.curseforge.com/minecraft/mc-mods/equipment-compare) | Grend_G |
| [ETF Entity Texture Features](https://www.curseforge.com/minecraft/mc-mods/entity-texture-features-fabric) | Traben |
| [Euphoria Patches](https://www.curseforge.com/minecraft/mc-mods/euphoria-patches) | SpacEagle17 |
| [Extra Bounties](https://www.curseforge.com/minecraft/mc-mods/extra-bounties) | DevDyna |
| [Falling Leaves](https://www.curseforge.com/minecraft/mc-mods/falling-leaves-forge) | Cheaterpaul |
| [FamiliarsLib](https://www.curseforge.com/minecraft/mc-mods/familiarslib) | alshanex |
| [FancyMenu](https://www.curseforge.com/minecraft/mc-mods/fancymenu) | Keksuccino |
| [Fancy Hotbar](https://www.curseforge.com/minecraft/mc-mods/fancy-hotbar) | ElocinDev |
| [Fancy Toasts](https://www.curseforge.com/minecraft/mc-mods/fancy-toasts) | Bivrik |
| [Fantasy Armor](https://www.curseforge.com/minecraft/mc-mods/fantasy-armor) | Kenddie |
| [Fantasy Weapons](https://www.curseforge.com/minecraft/mc-mods/fantasy-weapons-medieval-series) | Kenddie |
| [Fantasy's Dice](https://www.curseforge.com/minecraft/mc-mods/fantasys-dice) | ApexModder |
| [Fantasy's Furniture](https://www.curseforge.com/minecraft/mc-mods/fantasys-furniture) | ApexModder |
| [Farmer's Delight](https://www.curseforge.com/minecraft/mc-mods/farmers-delight) | vectorwing |
| [Farmers Structures](https://www.curseforge.com/minecraft/mc-mods/farmers-structures) | BlackAuresArt |
| [Fast Async World Save](https://www.curseforge.com/minecraft/mc-mods/fast-async-world-save-forge-fabric) | someaddon |
| [Fast IP Ping](https://www.curseforge.com/minecraft/mc-mods/fast-ip-ping) | Fallen_Breath |
| [Fast Item Frames](https://www.curseforge.com/minecraft/mc-mods/fast-item-frames) | Fuzs |
| [Fast Paintings](https://www.curseforge.com/minecraft/mc-mods/fast-paintings) | MehVahdJukaar |
| [Feature Recycler](https://www.curseforge.com/minecraft/mc-mods/feature-recycler) | Corgi_Taco |
| [FerriteCore](https://www.curseforge.com/minecraft/mc-mods/ferritecore) | malte0811 |
| [Feur - Dungeon Spawner](https://www.curseforge.com/minecraft/mc-mods/feur-dungeon-spawner) | Vayns |
| [Feur - Extension Desert](https://www.curseforge.com/minecraft/mc-mods/feur-extension-desert) | Vayns |
| [Feur - Extension Fossil](https://www.curseforge.com/minecraft/mc-mods/feur-extension-fossil) | Vayns |
| [Feur - Extension Jungle](https://www.curseforge.com/minecraft/mc-mods/feur-extension-jungle) | Vayns |
| [fix GPU memory leak](https://www.curseforge.com/minecraft/mc-mods/fix-gpu-memory-leak) | someaddon |
| [Flerovium](https://www.curseforge.com/minecraft/mc-mods/flerovium) | moepus |
| [Foolproof](https://www.curseforge.com/minecraft/mc-mods/foolproof) | Txni |
| [Forge Config Screens](https://www.curseforge.com/minecraft/mc-mods/config-menus-forge) | Fuzs, SHXRKIE |
| [Forgified Fabric API](https://www.curseforge.com/minecraft/mc-mods/forgified-fabric-api) | Su5eD |
| [Formations (Structure Library)](https://www.curseforge.com/minecraft/mc-mods/formations) | SuperMartijn642 |
| [Formations Nether](https://www.curseforge.com/minecraft/mc-mods/formations-nether) | SuperMartijn642 |
| [Formations Overworld](https://www.curseforge.com/minecraft/mc-mods/formations-overworld) | SuperMartijn642 |
| [Fragmentum](https://www.curseforge.com/minecraft/mc-mods/fragmentum) | Obscuria |
| [FTB Chunks](https://www.curseforge.com/minecraft/mc-mods/ftb-chunks-forge) | FTB, FTBTeam |
| [FTB Library](https://www.curseforge.com/minecraft/mc-mods/ftb-library-forge) | FTB, FTBTeam |
| [FTB Quests](https://www.curseforge.com/minecraft/mc-mods/ftb-quests-forge) | FTB, FTBTeam |
| [FTB Teams](https://www.curseforge.com/minecraft/mc-mods/ftb-teams-forge) | FTB, FTBTeam |
| [FTB XMod Compat](https://www.curseforge.com/minecraft/mc-mods/ftb-xmod-compat) | FTB, FTBTeam |
| [FullStack Watchdog](https://www.curseforge.com/minecraft/mc-mods/fullstack-watchdog) | telepathicgrunt |
| [Fzzy Config](https://www.curseforge.com/minecraft/mc-mods/fzzy-config) | fzzyhmstrs |
| [Gallant Gauntlets](https://www.curseforge.com/minecraft/mc-mods/gauntlets) | joshieman |
| [Game Stages](https://www.curseforge.com/minecraft/mc-mods/game-stages) | DarkhaxDev |
| [GeckoLib](https://www.curseforge.com/minecraft/mc-mods/geckolib) | Gecko, EliotL |
| [GlitchCore](https://www.curseforge.com/minecraft/mc-mods/glitchcore) | TheAdubbz |
| [Gnetum](https://www.curseforge.com/minecraft/mc-mods/gnetum) | decce |
| [Goblin's Tyranny](https://www.curseforge.com/minecraft/mc-mods/goblins-tyranny) | Paraste |
| [Golem Overhaul](https://www.curseforge.com/minecraft/mc-mods/golem-overhaul) | joosh_7889, AlexNijjar |
| [GTBC's Geomancy Plus](https://www.curseforge.com/minecraft/mc-mods/gtbcs-geomancy-plus) | GameTechBC |
| [GTBC's SpellLib/API](https://www.curseforge.com/minecraft/mc-mods/gtbcs-spelllib) | GameTechBC |
| [Handcrafted](https://www.curseforge.com/minecraft/mc-mods/handcrafted) | terrariumearth, AlexNijjar, kekie6 |
| [Hardcore Revival](https://www.curseforge.com/minecraft/mc-mods/hardcore-revival) | BlayTheNinth |
| [Horseman](https://www.curseforge.com/minecraft/mc-mods/horseman) | mortuusars |
| [HT's TreeChop](https://www.curseforge.com/minecraft/mc-mods/treechop) | hammertater |
| [Ice and Fire: Dragons](https://www.curseforge.com/minecraft/mc-mods/ice-and-fire-dragons) | sbom_xela, javaraptor |
| [Ice and Fire: Dragonseeker](https://www.curseforge.com/minecraft/mc-mods/ice-and-fire-dragonseeker) | syrikalis |
| [Ice and Fire: Spellbooks](https://www.curseforge.com/minecraft/mc-mods/ice-and-fire-spellbooks) | Ace_The_Eldritch_King |
| [Ice And Fire Patcher](https://www.curseforge.com/minecraft/mc-mods/ice-and-fire-patcher) | IAFEnvoy |
| [Iceberg](https://www.curseforge.com/minecraft/mc-mods/iceberg) | Grend_G |
| [ImmediatelyFast](https://www.curseforge.com/minecraft/mc-mods/immediatelyfast) | RaphiMC |
| [Immersive Armor HUD](https://www.curseforge.com/minecraft/mc-mods/immersive-armor-hud) | Txni |
| [Immersive Damage Indicators](https://www.curseforge.com/minecraft/mc-mods/immersive-damage-indicators) | Txni |
| [Immersive Lanterns](https://www.curseforge.com/minecraft/mc-mods/immersive-lanterns) | Txni |
| [Immersive Melodies](https://www.curseforge.com/minecraft/mc-mods/immersive-melodies) | Conczin |
| [Immersive Messages API](https://www.curseforge.com/minecraft/mc-mods/immersive-messages-api) | Txni |
| [In Control!](https://www.curseforge.com/minecraft/mc-mods/in-control) | McJty |
| [Integrated API](https://www.curseforge.com/minecraft/mc-mods/integrated-api) | CraisinLord |
| [Integrated Cataclysm](https://www.curseforge.com/minecraft/mc-mods/integrated-cataclysm) | CraisinLord |
| [Integrated Dungeons and Structures](https://www.curseforge.com/minecraft/mc-mods/idas) | CraisinLord |
| [Integrated Dungeons Arise](https://www.curseforge.com/minecraft/mc-mods/integrated-dungeons-arise) | Aarods |
| [Integrated Stronghold](https://www.curseforge.com/minecraft/mc-mods/integrated-stronghold) | CraisinLord |
| [Integrated Villages](https://www.curseforge.com/minecraft/mc-mods/integrated-villages) | CraisinLord |
| [Iris/Oculus Shader Folder](https://www.curseforge.com/minecraft/mc-mods/iris-shader-folder) | SpacEagle17 |
| [Iron's Spells 'n Spellbooks](https://www.curseforge.com/minecraft/mc-mods/irons-spells-n-spellbooks) | Iron431, Sma11s |
| [Item Filters](https://www.curseforge.com/minecraft/mc-mods/item-filters) | LatvianModder |
| [Item Highlighter](https://www.curseforge.com/minecraft/mc-mods/item-highlighter) | Grend_G |
| [Item Obliterator](https://www.curseforge.com/minecraft/mc-mods/item-obliterator) | ElocinDev |
| [ItemPhysic Full](https://www.curseforge.com/minecraft/mc-mods/itemphysic) | CreativeMD |
| [Jade](https://www.curseforge.com/minecraft/mc-mods/jade) | Snownee |
| [Jade Addons](https://www.curseforge.com/minecraft/mc-mods/jade-addons) | Snownee |
| [JadeColonies](https://www.curseforge.com/minecraft/mc-mods/jadecolonies) | uecasm |
| [Jaden's Nether Expansion](https://www.curseforge.com/minecraft/mc-mods/jadens-nether-expansion) | ThatJadenXgamer |
| [JeremySeq's Damage Indicators](https://www.curseforge.com/minecraft/mc-mods/jeremyseq-damage-indicator) | JeremySeq |
| [JourneyMap](https://www.curseforge.com/minecraft/mc-mods/journeymap) | techbrew, Mysticdrew, meme_sapiens |
| [JourneyMap Integration](https://www.curseforge.com/minecraft/mc-mods/journeymap-integration) | frankV |
| [JourneyMap Teams](https://www.curseforge.com/minecraft/mc-mods/journeymap-teams) | Mysticdrew |
| [Just Enough Breeding (JEBr)](https://www.curseforge.com/minecraft/mc-mods/justenoughbreeding) | Christofmeg |
| [Just Enough Items (JEI)](https://www.curseforge.com/minecraft/mc-mods/jei) | mezz |
| [Just Enough Professions (JEP)](https://www.curseforge.com/minecraft/mc-mods/just-enough-professions-jep) | Mrbysco, ShyNieke |
| [JustLeveling [Fork]](https://www.curseforge.com/minecraft/mc-mods/justleveling-fork) | SeniorS |
| [Kambrik](https://www.curseforge.com/minecraft/mc-mods/kambrik) | Ejektaflex |
| [Kiwi](https://www.curseforge.com/minecraft/mc-mods/kiwi) | Snownee |
| [KleeSlabs](https://www.curseforge.com/minecraft/mc-mods/kleeslabs) | BlayTheNinth |
| [Konkrete](https://www.curseforge.com/minecraft/mc-mods/konkrete) | Keksuccino |
| [Kotlin for Forge](https://www.curseforge.com/minecraft/mc-mods/kotlin-for-forge) | thedarkcolour |
| [L_Ender's Cataclysm](https://www.curseforge.com/minecraft/mc-mods/lendercataclysm) | mcl_ender |
| [Leaves Be Gone](https://www.curseforge.com/minecraft/mc-mods/leaves-be-gone) | Fuzs, SHXRKIE |
| [Legendary Monsters](https://www.curseforge.com/minecraft/mc-mods/legendary-monsters) | miauczel |
| [Legendary Survival Overhaul](https://www.curseforge.com/minecraft/mc-mods/legendary-survival-overhaul) | legendary_workshop, Alex_Hashtag, armkath, krampus_there |
| [Lionfish API](https://www.curseforge.com/minecraft/mc-mods/lionfish-api) | mcl_ender |
| [Lithostitched](https://www.curseforge.com/minecraft/mc-mods/lithostitched) | Apollo, SmellyModder |
| [Load My F***ing Tags](https://www.curseforge.com/minecraft/mc-mods/lmft) | Blodhgarm |
| [Lodestone](https://www.curseforge.com/minecraft/mc-mods/lodestone) | sammysemicolon |
| [Log Begone](https://www.curseforge.com/minecraft/mc-mods/log-begone) | AzureDoomC |
| [Long NBT Killer](https://www.curseforge.com/minecraft/mc-mods/long-nbt-killer) | Dovecot_Official, TachibanaSherry |
| [Loot Beams: Relooted!](https://www.curseforge.com/minecraft/mc-mods/loot-beams) | shiroroku, AmoAsterVT |
| [Loot Integrations](https://www.curseforge.com/minecraft/mc-mods/loot-integrations) | someaddon |
| [Loot Journal](https://www.curseforge.com/minecraft/mc-mods/loot-journal) | Obscuria |
| [Luki's Grand Capitals](https://www.curseforge.com/minecraft/mc-mods/lukis-grand-capitals) | lukidon |
| [Luna](https://www.curseforge.com/minecraft/mc-mods/luna) | LunaPixelStudios, SHXRKIE |
| [MapFrontiers](https://www.curseforge.com/minecraft/mc-mods/mapfrontiers) | meme_sapiens |
| [Marium's Soulslike Weaponry](https://www.curseforge.com/minecraft/mc-mods/mariums-soulslike-weaponry) | mariumbacchus |
| [Max Health Fix](https://www.curseforge.com/minecraft/mc-mods/max-health-fix) | DarkhaxDev |
| [Medieval Buildings](https://www.curseforge.com/minecraft/mc-mods/medieval-buildings) | Lupin |
| [Medieval Buildings [End Edition]](https://www.curseforge.com/minecraft/mc-mods/medieval-buildings-end-edition) | Lupin |
| [Medieval Buildings [Nether Edition]](https://www.curseforge.com/minecraft/mc-mods/medieval-buildings-nether-edition) | Lupin |
| [Melody](https://www.curseforge.com/minecraft/mc-mods/melody) | Keksuccino |
| [MES - Moog's End Structures](https://www.curseforge.com/minecraft/mc-mods/moogs-end-structures) | finndog_123 |
| [MidnightLib](https://www.curseforge.com/minecraft/mc-mods/midnightlib) | Motschen |
| [Mine Cells - Dead Cells Mod](https://www.curseforge.com/minecraft/mc-mods/minecells) | mim1q |
| [MineColonies](https://www.curseforge.com/minecraft/mc-mods/minecolonies) | Raycoms, someaddon, LDTTeam |
| [Miner's Delight +](https://www.curseforge.com/minecraft/mc-mods/miners-delight-plus) | soytutta |
| [Mining Speed Tooltips](https://www.curseforge.com/minecraft/mc-mods/mining-speed-tooltips) | Txni |
| [MixinTrace Resmithed](https://www.curseforge.com/minecraft/mc-mods/mixintrace-resmithed) | Txni |
| [MmmMmmMmmMmm (Target Dummy)](https://www.curseforge.com/minecraft/mc-mods/mmmmmmmmmmmm) | MehVahdJukaar |
| [MNS - Moog's Nether Structures](https://www.curseforge.com/minecraft/mc-mods/mns-moogs-nether-structures) | finndog_123 |
| [ModernFix](https://www.curseforge.com/minecraft/mc-mods/modernfix) | embeddedt |
| [Modpack Update Checker](https://www.curseforge.com/minecraft/mc-mods/modpack-update-checker) | Jab125 |
| [Monobank](https://www.curseforge.com/minecraft/mc-mods/monobank) | mortuusars |
| [Moog's Structure Lib](https://www.curseforge.com/minecraft/mc-mods/moogs-structure-lib) | finndog_123 |
| [Moonlight Lib](https://www.curseforge.com/minecraft/mc-mods/selene) | MehVahdJukaar |
| [More Villagers](https://www.curseforge.com/minecraft/mc-mods/more-villagers) | SameDifferent, Zero_DSRS_VX |
| [Mouse Tweaks](https://www.curseforge.com/minecraft/mc-mods/mouse-tweaks) | YaLTeR |
| [Mowzie's Cataclysm](https://www.curseforge.com/minecraft/mc-mods/mowzies-cataclysm) | Cyber_Rat |
| [Mowzie's Mobs](https://www.curseforge.com/minecraft/mc-mods/mowzies-mobs) | bobmowzie, vakypanda1, noonyeyzz, wadoo154, pau101 |
| [Multi-Piston](https://www.curseforge.com/minecraft/mc-mods/multi-piston) | Raycoms, OrionOnline, someaddon |
| [MVS - Moog's Voyager Structures](https://www.curseforge.com/minecraft/mc-mods/moogs-voyager-structures) | finndog_123, olver____, TFA120, havococcultist |
| [My Nether's Delight](https://www.curseforge.com/minecraft/mc-mods/my-nethers-delight) | soytutta |
| [NaNny Reforked](https://www.curseforge.com/minecraft/mc-mods/nanny-reforked) | adam98991, qther |
| [Nature's Compass](https://www.curseforge.com/minecraft/mc-mods/natures-compass) | Chaosyr |
| [Necronomicon API](https://www.curseforge.com/minecraft/mc-mods/necronomicon) | ElocinDev |
| [Neruina - Ticking Entity Fixer](https://www.curseforge.com/minecraft/mc-mods/neruina) | bawnorton |
| [No Report Button](https://www.curseforge.com/minecraft/mc-mods/no-report-button) | pices1237532 |
| [Nordic Adventure](https://www.curseforge.com/minecraft/mc-mods/nordic-adventure) | _NO_CHEESE_ |
| [Numismatic Bounties](https://www.curseforge.com/minecraft/mc-mods/numismatic-bounties) | DevDyna |
| [Numismatic Overhaul](https://www.curseforge.com/minecraft/mc-mods/numismatic-overhaul) | gliscowo, Noaaan |
| [Obscure API](https://www.curseforge.com/minecraft/mc-mods/obscure-api) | Obscuria |
| [OctoLib](https://www.curseforge.com/minecraft/mc-mods/octo-lib) | SSKirillSS |
| [Oculus](https://www.curseforge.com/minecraft/mc-mods/oculus) | Asek3 |
| [Oh The Biomes We've Gone](https://www.curseforge.com/minecraft/mc-mods/oh-the-biomes-weve-gone) | AOCAWOL, JT122406, YaBoiChips, Corgi_Taco |
| [Oh The Trees You'll Grow](https://www.curseforge.com/minecraft/mc-mods/oh-the-trees-youll-grow) | Corgi_Taco, JT122406 |
| [Origins (Forge)](https://www.curseforge.com/minecraft/mc-mods/origins-forge) | EdwinMindcraft |
| [Otherworld - Apotheosis](https://www.curseforge.com/minecraft/mc-mods/otherworld-apotheosis) | MuonR, SHXRKIE |
| [Otherworld - Origins](https://www.curseforge.com/minecraft/mc-mods/otherworld-origins) | MuonR, SHXRKIE |
| [Otherworld Core](https://www.curseforge.com/minecraft/mc-mods/otherworld-core) | MuonR |
| [Overflowing Bars](https://www.curseforge.com/minecraft/mc-mods/overflowing-bars) | Fuzs |
| [owo (owo-lib)](https://www.curseforge.com/minecraft/mc-mods/owo-lib) | gliscowo |
| [P1nero's Dialogue Lib](https://www.curseforge.com/minecraft/mc-mods/p1neros-dialogue-lib) | P1nero |
| [Pack Analytics](https://www.curseforge.com/minecraft/mc-mods/pack-analytics) | Txni |
| [Packet Fixer](https://www.curseforge.com/minecraft/mc-mods/packet-fixer) | TonimatasDEV |
| [Paintings ++](https://www.curseforge.com/minecraft/mc-mods/paintings) | AbsolemJackdaw |
| [Particle Core](https://www.curseforge.com/minecraft/mc-mods/particle-core) | fzzyhmstrs |
| [Particle Effects Reforged](https://www.curseforge.com/minecraft/mc-mods/particle-effects-reforged) | Project8gbDeRam, LopyTwich |
| [Patchouli](https://www.curseforge.com/minecraft/mc-mods/patchouli) | Vazkii |
| [Paxi (Forge)](https://www.curseforge.com/minecraft/mc-mods/paxi) | YUNGNICKYOUNG |
| [Pehkui](https://www.curseforge.com/minecraft/mc-mods/pehkui) | Virtuoel |
| [Perception](https://www.curseforge.com/minecraft/mc-mods/perception) | SSKirillSS |
| [Pillager Caravans](https://www.curseforge.com/minecraft/mc-mods/pillager-caravans) | Obscuria |
| [Placebo](https://www.curseforge.com/minecraft/mc-mods/placebo) | Shadows_of_Fire |
| [playerAnimator](https://www.curseforge.com/minecraft/mc-mods/playeranimator) | KosmX |
| [Polymorph](https://www.curseforge.com/minecraft/mc-mods/polymorph) | TheIllusiveC4 |
| [Prism](https://www.curseforge.com/minecraft/mc-mods/prism-lib) | Grend_G |
| [Projectile Damage Attribute](https://www.curseforge.com/minecraft/mc-mods/projectile-damage-attribute) | daedelus_dev |
| [Puzzles Lib](https://www.curseforge.com/minecraft/mc-mods/puzzles-lib) | Fuzs |
| [Quark](https://www.curseforge.com/minecraft/mc-mods/quark) | Vazkii, wiresegal |
| [Quests Kill Task Tweaks](https://www.curseforge.com/minecraft/mc-mods/quests-kill-task-tweaks) | MuonR |
| [Radium Reforged](https://www.curseforge.com/minecraft/mc-mods/radium-reforged) | Asek3 |
| [Realm RPG: Fallen Adventurers](https://www.curseforge.com/minecraft/mc-mods/realm-rpg-fallen-adventurers) | NoCube |
| [Realm RPG: Imps & Demons](https://www.curseforge.com/minecraft/mc-mods/realm-rpg-imps-demons) | NoCube |
| [Realm RPG: Quests & Rewards](https://www.curseforge.com/minecraft/mc-mods/realm-rpg-quests-rewards) | NoCube |
| [Recipe Essentials](https://www.curseforge.com/minecraft/mc-mods/recipe-essentials-forge-fabric) | someaddon |
| [Redirected](https://www.curseforge.com/minecraft/mc-mods/redirected) | Txni |
| [Regions Unexplored](https://www.curseforge.com/minecraft/mc-mods/regions-unexplored) | Apollo, UHQ_GAMES |
| [Reintegrated: Chipped](https://www.curseforge.com/minecraft/mc-mods/reintegrated-chipped) | Apollo |
| [Resource Pack Overrides](https://www.curseforge.com/minecraft/mc-mods/resource-pack-overrides) | Fuzs |
| [Resourceful Config](https://www.curseforge.com/minecraft/mc-mods/resourceful-config) | ThatGravyBoat, epic_oreo |
| [Resourceful Lib](https://www.curseforge.com/minecraft/mc-mods/resourceful-lib) | ThatGravyBoat, epic_oreo |
| [Rhino](https://www.curseforge.com/minecraft/mc-mods/rhino) | LatvianModder |
| [RunicLib](https://www.curseforge.com/minecraft/mc-mods/runiclib) | Yirmiri |
| [Sawmill](https://www.curseforge.com/minecraft/mc-mods/sawmill) | MehVahdJukaar, plantspookable |
| [Scholar](https://www.curseforge.com/minecraft/mc-mods/scholar) | mortuusars |
| [Searchables](https://www.curseforge.com/minecraft/mc-mods/searchables) | Jaredlll08 |
| [Serene Seasons](https://www.curseforge.com/minecraft/mc-mods/serene-seasons) | TheAdubbz, Forstride |
| [Server Browser](https://www.curseforge.com/minecraft/mc-mods/server-browser) | thethonk |
| [Smooth Chunk Save](https://www.curseforge.com/minecraft/mc-mods/smooth-chunk-save) | someaddon |
| [ServerCore](https://www.curseforge.com/minecraft/mc-mods/servercore) | Wesley8081 |
| [Shield Expansion](https://www.curseforge.com/minecraft/mc-mods/shield-expansion) | Nekomaster1000, tinytransfem |
| [Shoulder Surfing Reloaded](https://www.curseforge.com/minecraft/mc-mods/shoulder-surfing-reloaded) | _ForgeUser21552638, Exopandora |
| [Shoulder Surfing: Iron's Spells Integration](https://www.curseforge.com/minecraft/mc-mods/shoulder-surfing-irons-spells-integration) | Ellet |
| [Simple Discord RPC](https://www.curseforge.com/minecraft/mc-mods/simple-discord-rpc) | HypherionSA |
| [Simple Snowy Fix](https://www.curseforge.com/minecraft/mc-mods/simple-snowy-fix-forge-fabric) | KostromDan |
| [Sinytra Connector](https://www.curseforge.com/minecraft/mc-mods/sinytra-connector) | Su5eD |
| [Skeleton AI Fix](https://www.curseforge.com/minecraft/mc-mods/skeleton-ai-fix) | Fuzs |
| [Skin Layers 3D](https://www.curseforge.com/minecraft/mc-mods/skin-layers-3d) | tr7zw |
| [Smarter Farmers](https://www.curseforge.com/minecraft/mc-mods/smarter-farmers-farmers-replant) | MehVahdJukaar |
| [Snow! Real Magic!](https://www.curseforge.com/minecraft/mc-mods/snow-real-magic) | Snownee |
| [Sodium/Embeddium Dynamic Lights](https://www.curseforge.com/minecraft/mc-mods/dynamiclights-reforged) | Txni |
| [Sodium/Embeddium Options API](https://www.curseforge.com/minecraft/mc-mods/sodium-options-api) | Txni |
| [Sodium/Embeddium Options Mod Compat](https://www.curseforge.com/minecraft/mc-mods/sodium-embeddium-options-mod-compat) | Txni |
| [Sophisticated Backpacks](https://www.curseforge.com/minecraft/mc-mods/sophisticated-backpacks) | P3pp3rF1y |
| [Sophisticated Backpacks Create Integration](https://www.curseforge.com/minecraft/mc-mods/sophisticated-backpacks-create-integration) | P3pp3rF1y |
| [Sophisticated Core](https://www.curseforge.com/minecraft/mc-mods/sophisticated-core) | P3pp3rF1y |
| [Sophisticated Storage](https://www.curseforge.com/minecraft/mc-mods/sophisticated-storage) | P3pp3rF1y |
| [Sophisticated Storage Create Integration](https://www.curseforge.com/minecraft/mc-mods/sophisticated-storage-create-integration) | P3pp3rF1y |
| [Sound Physics Remastered](https://www.curseforge.com/minecraft/mc-mods/sound-physics-remastered) | henkelmax |
| [Sparse Structures](https://www.curseforge.com/minecraft/mc-mods/sparse-structures) | Maxence |
| [spark](https://www.curseforge.com/minecraft/mc-mods/spark) | Iucko |
| [Spyglass Improvements](https://www.curseforge.com/minecraft/mc-mods/spyglass-improvements) | Im_JC52 |
| [Structure Essentials](https://www.curseforge.com/minecraft/mc-mods/structure-essentials-forge-fabric) | someaddon |
| [Structure Gel API](https://www.curseforge.com/minecraft/mc-mods/structure-gel-api) | ModdingLegacy, silver_david |
| [Structure Layout Optimizer](https://www.curseforge.com/minecraft/mc-mods/structure-layout-optimizer) | telepathicgrunt |
| [Structurize](https://www.curseforge.com/minecraft/mc-mods/structurize) | Raycoms, someaddon, OrionOnline, Asherslab, Nightenom |
| [Stylecolonies](https://www.curseforge.com/minecraft/mc-mods/stylecolonies) | Raycoms, LDTTeam |
| [Subtle Effects](https://www.curseforge.com/minecraft/mc-mods/subtle-effects) | MincraftEinstein |
| [Supplementaries](https://www.curseforge.com/minecraft/mc-mods/supplementaries) | MehVahdJukaar |
| [T.O Magic 'n Extras](https://www.curseforge.com/minecraft/mc-mods/to-tweaks-irons-spells) | GameTechBC |
| [TACT - Tiny Alex's Caves Tweaks](https://www.curseforge.com/minecraft/mc-mods/tact) | telepathicgrunt |
| [Tectonic](https://www.curseforge.com/minecraft/mc-mods/tectonic) | Apollo |
| [TerraBlender](https://www.curseforge.com/minecraft/mc-mods/terrablender) | TheAdubbz |
| [The Aether](https://www.curseforge.com/minecraft/mc-mods/aether) | TheAetherTeam, KatiePayn |
| [The Guild](https://www.curseforge.com/minecraft/mc-mods/guild) | fulmineo64 |
| [The Orcs!](https://www.curseforge.com/minecraft/mc-mods/the-orcs) | TheUnknownDad |
| [Thief](https://www.curseforge.com/minecraft/mc-mods/thief) | mortuusars |
| [Tom's Simple Storage Mod](https://www.curseforge.com/minecraft/mc-mods/toms-storage) | tom54541 |
| [Toni's Immersive Lanterns](https://www.curseforge.com/minecraft/mc-mods/immersive-lanterns) | Txni |
| [Too Fast](https://www.curseforge.com/minecraft/mc-mods/too-fast) | Noobanidus, ZestyBlaze |
| [TownTalk](https://www.curseforge.com/minecraft/mc-mods/towntalk) | Raycoms |
| [Transparent](https://www.curseforge.com/minecraft/mc-mods/transparent) | Trikzon |
| [Traveler's Titles](https://www.curseforge.com/minecraft/mc-mods/travelers-titles) | YUNGNICKYOUNG |
| [Tridot](https://www.curseforge.com/minecraft/mc-mods/tridot) | IriDark, skoow_, auriny |
| [Tweaks addon for MineColonies](https://www.curseforge.com/minecraft/mc-mods/minecolonies-tweaks) | supernover0102, gisellevonbingen |
| [TxniLib](https://www.curseforge.com/minecraft/mc-mods/txnilib) | Txni |
| [ucrashedlol](https://www.curseforge.com/minecraft/mc-mods/ucrashedlol) | skycatminepokie |
| [Valoria](https://www.curseforge.com/minecraft/mc-mods/valoria) | IriDark |
| [Vanillin](https://www.curseforge.com/minecraft/mc-mods/vanillin) | jozufozu, Pepper_Bell |
| [Villager Comfort Updated](https://www.curseforge.com/minecraft/mc-mods/villager-comfort-updated) | leahx_y2k |
| [Villager Names](https://www.curseforge.com/minecraft/mc-mods/villager-names) | Serilum |
| [Vintage Animations](https://www.curseforge.com/minecraft/mc-mods/vintage-animations) | Thrasos |
| [Visual Workbench](https://www.curseforge.com/minecraft/mc-mods/visual-workbench) | Fuzs |
| [Wares](https://www.curseforge.com/minecraft/mc-mods/wares) | mortuusars |
| [Waystones](https://www.curseforge.com/minecraft/mc-mods/waystones) | BlayTheNinth |
| [What Are They Up To (Watut)](https://www.curseforge.com/minecraft/mc-mods/what-are-they-up-to) | Corosus |
| [Wither Spawn Animation](https://www.curseforge.com/minecraft/mc-mods/wither-spawn-animation) | bo_bo0 |
| [Wither Spawn Fix](https://www.curseforge.com/minecraft/mc-mods/wither-spawn-fix-wsa-compatible) | bo_bo0 |
| [Xenon](https://www.curseforge.com/minecraft/mc-mods/xenon) | Txni |
| [YDM's MobHealthBar](https://www.curseforge.com/minecraft/mc-mods/ydms-mobhealthbar-mod) | YourDailyModderx |
| [YDM's Weapon Master](https://www.curseforge.com/minecraft/mc-mods/ydms-weapon-master) | YourDailyModderx |
| [YetAnotherConfigLib](https://www.curseforge.com/minecraft/mc-mods/yacl) | isXander |
| [You Shall Not Spawn!](https://www.curseforge.com/minecraft/mc-mods/you-shall-not-spawn) | ElocinDev |
| [YUNG's API](https://www.curseforge.com/minecraft/mc-mods/yungs-api) | YUNGNICKYOUNG |
| [YUNG's Better Dungeons](https://www.curseforge.com/minecraft/mc-mods/yungs-better-dungeons) | YUNGNICKYOUNG, EveCommander |
| [YUNG's Better End Island](https://www.curseforge.com/minecraft/mc-mods/yungs-better-end-island) | YUNGNICKYOUNG, EveCommander |
| [YUNG's Better Jungle Temples](https://www.curseforge.com/minecraft/mc-mods/yungs-better-jungle-temples) | YUNGNICKYOUNG, TeraBuildsStuff |
| [YUNG's Better Mineshafts](https://www.curseforge.com/minecraft/mc-mods/yungs-better-mineshafts-forge) | YUNGNICKYOUNG |
| [YUNG's Better Nether Fortresses](https://www.curseforge.com/minecraft/mc-mods/yungs-better-nether-fortresses) | YUNGNICKYOUNG, EveCommander |
| [YUNG's Better Ocean Monuments](https://www.curseforge.com/minecraft/mc-mods/yungs-better-ocean-monuments) | YUNGNICKYOUNG, TeraBuildsStuff |
| [YUNG's Better Strongholds](https://www.curseforge.com/minecraft/mc-mods/yungs-better-strongholds) | YUNGNICKYOUNG, EveCommander |
| [YUNG's Bridges](https://www.curseforge.com/minecraft/mc-mods/yungs-bridges) | YUNGNICKYOUNG |
| [YUNG's Cave Biomes](https://www.curseforge.com/minecraft/mc-mods/yungs-cave-biomes) | YUNGNICKYOUNG, kjpg, LudoCrypt, HellionGames |
| [YUNG's Menu Tweaks](https://www.curseforge.com/minecraft/mc-mods/yungs-menu-tweaks) | YUNGNICKYOUNG |
| [Zeta](https://www.curseforge.com/minecraft/mc-mods/zeta) | Vazkii, quat, Siuolplex, IThundxr |
