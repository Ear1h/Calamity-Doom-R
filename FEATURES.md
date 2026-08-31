# Calamity Doom Features

The build corresponding to this feature list is based on [Nugget Doom 5.1.0](https://github.com/MrAlaux/Nugget-Doom/releases/tag/nugget-doom-5.1.0).

Most of Calamity Doom's features come from other sources, like source ports and mods;
the initial implementations for some are **ported from (p.f.)** said sources, while others are just **inspired by (i.b.)** them.
These acknowledgements are included in the feature lists below; be aware that some might be inaccurate or outright missing.

A few settings are labeled as **_CFG-only_**: they can only be toggled by editing `calamity-doom.cfg`.
For these settings, their CVAR names are provided alongside the _CFG-only_ label as guidance.

## General

### Advance Custom Skill Drop

**Three new tabs have been added to the Custom Skill menu:**
* Calamity
* Loadouts
* Modificators (currently empty)

#### Powerups
These modifiers give the player powerful abilities that can be used against enemies.

#### Infinite Berserk - Tyson Mode
The player starts every level with Berserk.
Additionally:
* all ammunition is replaced with pistol ammunition depending on the ammo type (clip / clip box);
* all weapons are replaced with Berserk Packs;
* in Arcade Mode, monsters drop health depending on their maximum HP;
* Cyberdemons drop Megaspheres (Doom II only);
* zombies drop small health bottles;
* and other similar changes.

#### Infinite Invisibility
The player remains permanently invisible.
This ability can also be applied to:
* the player only;
* monsters only;
* both the player and monsters.

#### Infinite Quad Damage

The player deals 4× damage to enemies and receives a distinctive sound effect when attacking.
The sound effect can be disabled via:

```Audio → Sound Options → Calamity → Quad Sound Effect → Off```

#### Infinite Haste like Doom 2016
* firing speed is increased by 2×;
* weapon switching is 2× faster;
* player movement speed is increased by 2×.

#### Infinite Vampirism
The player restores 10% of the damage dealt as health.

There are two restrictions:
* the effect cannot restore health after the player has died;
* the player cannot heal themselves from their own explosion damage.
Works together with Quad Damage.

#### Infinite Regeneration

The player restores health when picking up health bonuses, up to their maximum health.
The Partial mode allows health to be restored in specific segments.

For example, if the player has ```13 HP```, healing will restore them to ```20 HP``` .If the player has at least ```21 HP```, the next regeneration segment will restore their health up to ```40 HP```.

#### Infinite Armor Repair

Every 2 seconds, the player regenerates 2% armor.

The **Upgrade** mode allows the player's green armor to be upgraded to **blue** armor after reaching ```200% armor```.

### Gamerules
These modifiers impose additional restrictions on the player.

#### No Saves
The player cannot manually save the game.
**Only autosaves after completing a level are available.**

### No Cheats
The player cannot use cheat codes.

**IDCLEV and IDDT are also disabled.**

#### No Armor / Health

The player must complete the level without using health or armor pickups.
**Exception:** Tyson Mode: Arcade, Regeneration, and Armor Repair do not count toward this restriction.

#### Par Time Limit

The player must complete the level within its specified ```Par Time.```
If the time limit expires, the player dies.

### Monster Behavior
These modifiers change monster behavior and spawning.

#### Duplicate ×2–×8
Monsters are duplicated 2 to 8 times when spawning.
Some monsters may not be duplicated if there is insufficient space for additional copies. The game has built-in protection against potential softlocks.

### Bullet Hell
All **hitscan** monsters (except Arch-vile) use **Imp Fireballs** instead of their normal hitscan attacks.

### Loadouts
Loadouts allow you to select a predefined set of modifiers created by the port developer.

Each Loadout represents a specific combination of Custom Skill settings.
