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
| Battle rifles & DMRs (one category) | Ground | 3 |
| LMGs | Ground | 1 |
| Snipers | Ground | 2 |
| Special (bows/crossbows, mortars, more later) | Ground | 2 |
| Throwables (a good random mix) | Ground | Not set yet |
| Crate weapons | Crates (exclusive list) | Not set yet |

Lots of throwables, starting with every one PUBG has ([Throwables](#throwables)).

Special never repeats a subcategory in one match: the 2 special slots always come from different subcategories, like a bow and a mortar, never two bows.

Crate weapons come from an exclusive list of guns too powerful or special for the ground pool. The cartridge weighting might still apply to crate picks. What goes in crates:

- **Anti-vehicle and heavy snipers:** anti-materiel rifles like .50-caliber ones, and other heavy sniper rifles. Like PUBG's crate AWM, which one-shot level 3 helmets, a crate sniper's head shot kills through any helmet, tier 3 included. Any version whose starting damage crosses that line is crate-only, like the .300 Winchester Magnum and .338 Lapua snipers ([Starting damage](starting-damage.md#baselines-and-crate-lines)).
- **Rocket launchers,** like the RPG. They're heavy, slow, and take up a primary slot.
- **Lethal grenade launchers,** which are too powerful for the ground pool. Non-lethal ones go in the [class item](class-items.md) pool.
- **Lethal rounds for underbarrel and rifle grenade launchers,** like frag, HEDP, and anti-tank grenades. The launchers themselves are ground loot, with smoke, star, and other non-lethal rounds ([Attachments](attachments.md#grenade-launchers)).
- **Belt-fed guns too fast for the ground,** like the [MG 42 / MG3](../weapons/crate/mg-42.md) family, as PUBG did with its MG3 ([Starting damage](starting-damage.md#crate-check-for-fast-firing-guns)).
- **The flash shield,** a ballistic shield with flashbangs on the front ([Class items](class-items.md)).

Specific guns are listed in the [weapon roster](../weapons/index.md). Where they spawn on the map, and how often, is on [Loot and spawning](loot.md).

**Cartridge weighting:** the randomizer picks one category first, then a gun for it (for example, a 9mm SMG). The remaining slots get a slightly higher chance of rolling guns with the same cartridge, so ammo is easier to share. Example: a 9mm SMG makes a 9mm pistol or a 9mm assault rifle slightly more likely to show up. See also [Ammo](ammo.md).

9mm guns will appear across categories, not just pistols and SMGs. Example: 9mm conversions of the AR-15 platform.

Categories are loose on purpose: a gun doesn't have to fit its category exactly.

**Battle rifles & DMRs:** one category. Battle rifles are a soldier's main rifle in a full-power round (FAL, M14, G3), usually with an auto mode and iron sights. DMRs are semi-auto marksman rifles for longer range, often built from those same battle rifles (the M14 into the Mk 14, the HK417 into the G28) and in the same rounds. They overlap too much to split, and original PUBG grouped them the same way (its SLR is a FAL, its Mk14 an M14). Bolt-action and precision rifles stay in snipers, except heavy and anti-materiel ones, which are crate-only.

**Gun versions:** a gun with several versions, like the C96, is one roster entry. The randomizer picks the gun, then rolls one version for that match.

**Version rarity:** follows how many of each version were actually made, so common versions roll often and rare ones rarely.

**Building versions:** each gun with versions gets one base model with swappable parts, so adding a version stays easy.

**Merging versions:** versions that fire the same round and differ only in small details are cut down to one version, with the differences noted.

Machine pistols that come from a main pistol, like the C96 Schnellfeuer, go in the pistol slot.

## Throwables

Lots of throwables: PUBG's list is the starting point, more come from other games later, and each match rolls a random mix. Each gets our own name and look. Carry weights are PUBG's ([Carry weight](armor.md#carry-weight)).

| Throwable | What it does (PUBG) | Weight |
| --- | --- | --- |
| **Frag grenade** | Explodes after about a 5-second fuse; cooking it first lets it burst behind cover | 18 |
| **Molotov cocktail** | Bursts into fire on impact and burns an area, blocking paths and revives | 16 |
| **Smoke grenade** | A smoke screen for crossing open ground, reviving, or resetting a fight | 14 |
| **Stun grenade** | A flashbang: blinds and deafens anyone facing it, on a short fuse | 12 |
| **Sticky bomb** | Sticks to a surface and blows a hole in walls | TBD |
| **C4** | Too heavy to throw far or carry many. It beeps and goes off 16 seconds after it's thrown, killing within about 15 m and hurting out to about 25 m, even through cover | TBD |
| **Decoy grenade** | Makes fake gunfire to draw attention (PUBG removed it in Update 35.1) | TBD |
| **Blue zone grenade** | Makes a small blue zone circle, up to about 10 m in radius, doing about 10 damage a second for about 10 seconds | TBD |

- **Weights TBD:** PUBG's weights for the sticky bomb, C4, decoy, and blue zone grenade weren't found yet.
- **Our own ideas:** an EMP grenade and a gas grenade.
- **From other games:** to add later.
- **Map max:** how many throwables a match can roll is still TBD (see the table above).

## Sources

- [PUBG Wiki: Grenades](https://pubg.wiki.gg/wiki/Grenades) (weights) · [PUBG Wiki: C4](https://pubg.wiki.gg/wiki/C4)
- [Gamertag Mythras: PUBG throwables and utility](https://gamertagmythras.com/blog/pubg-battlegrounds/pubg-throwables-utility-guide)
- [Dexerto: PUBG throwables](https://www.dexerto.com/wikis/pubg/weapons/throwable/)
