# Weapon pool and spawning

Every match rolls a different set of guns and ammo types, so no two games play the same.

- Weapons come from across history, covering all sorts of weapon types.
- Guns should be detailed, not generic.
- The ammo pool changes per match along with the guns.

Nothing is off the table: all sorts of guns go in. Balance is per gun, not per category, and each gun stays as true to the real one as possible, within reason.

**Funny guns:** the pool will include potentially many novelty guns, like the FP-45 Liberator.

Most guns are unloaded when first picked up; a few, like the FP-45 Liberator, come pre-loaded.

Damage is balanced around [time to kill](ttk.md).

## How the randomness works

Each map sets a maximum number of guns per category, and every match randomly picks which guns fill those slots. Themed matches exist but are rare.

| Category | Where it spawns | Example map max |
| --- | --- | --- |
| Pistols / 3rd slot (sawed-offs, other odd pistol-likes, and any gun typically carried in a pistol holster) | Ground | 3 |
| Shotguns | Ground | 2 |
| SMGs | Ground | 2 |
| Assault rifles | Ground | 3 |
| Battle rifles | Ground | 1 |
| LMGs | Ground | 1 |
| DMRs | Ground | 2 |
| Snipers | Ground | 2 |
| Special (launchers, bows/crossbows, mortars, more later) | Ground | 2 |
| Throwables (a good random mix) | Ground | Not set yet |
| Crate weapons | Crates (exclusive list) | Not set yet |

Special never repeats a subcategory in one match: the 2 special slots always come from different subcategories, like a launcher and a bow, never two launchers.

Crate weapons come from an exclusive list of guns too powerful or special for the ground pool. The cartridge weighting might still apply to crate picks.

Lethal grenade launchers are too powerful for the ground pool, so they go in crates; non-lethal ones go in the class item pool.

Rocket launchers stay in special: they're heavy, slow, and take up a primary slot.

Specific guns are listed in the [weapon roster](../weapons/index.md).

**Cartridge weighting:** the randomizer picks one category first, then a gun for it (for example, a 9mm SMG). The remaining slots get a slightly higher chance of rolling guns with the same cartridge, so ammo is easier to share. Example: a 9mm SMG makes a 9mm pistol or a 9mm assault rifle slightly more likely to show up. See also [Ammo](ammo.md).

9mm guns will appear across categories, not just pistols and SMGs. Example: 9mm conversions of the AR-15 platform.

Categories are loose on purpose: a gun doesn't have to fit its category exactly.

**Gun versions:** a gun with several versions, like the C96, is one roster entry. The randomizer picks the gun, then rolls one version for that match.

**Version rarity:** follows how many of each version were actually made, so common versions roll often and rare ones rarely.

**Building versions:** each gun with versions gets one base model with swappable parts, so adding a version stays easy.

**Merging versions:** versions that fire the same round and differ only in small details are cut down to one version, with the differences noted.

Machine pistols that come from a main pistol, like the C96 Schnellfeuer, go in the pistol slot.
