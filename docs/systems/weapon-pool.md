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
| Special (bows, crossbows, black powder, underwater guns, air guns, survival guns, oddities, slingshots) | Ground | 2 |
| Throwables (the smoke grenade always, plus 3 rolled) | Ground | 4 |
| Crate weapons | Crates (exclusive list) | 5 |

Lots of throwables, starting with every one PUBG has ([Throwables](#throwables)).

**Map caps (2026-11-22):**

- **Throwables:** 4 per match. The smoke grenade is in every match, and 3 more are rolled from the rest (owner). PUBG in 2017–2018 had four throwables, the frag, smoke, stun grenade, and Molotov, all in every match.
- **Crate weapons:** 5 per match (our pick, from PUBG). PUBG's crate guns in 2017–2018 were the AWM, Groza, AUG A3, M249, and Mk14, plus the M24 until mid-2018. Crate-only class items (rocket launchers, mines, the flash shield) aren't counted in the 5.

Special never repeats a subcategory in one match: the 2 special slots always come from different subcategories, like a bow and a musket, never two bows ([Special weapons](#special-weapons)). Mortars are class items ([Mortars](class-items.md#mortars)).

Crate weapons come from an exclusive list of guns too powerful or special for the ground pool. Crate picks use plain odds, with no cartridge weighting, since crate guns are special finds (our pick, from the lead's question, 2026-11-25). What goes in crates:

- **Anti-vehicle and heavy snipers:** anti-materiel rifles like .50-caliber ones, and other heavy sniper rifles. Like PUBG's crate AWM, which one-shot level 3 helmets, a crate sniper's head shot kills through any helmet, tier 3 included. Any version whose starting damage crosses that line is crate-only, like the .300 Winchester Magnum and .338 Lapua snipers ([Starting damage](starting-damage.md#baselines-and-crate-lines)).
- **Rocket launchers,** like the RPG, as crate-only class items: they take the class slot, not a primary (owner, 2026-11-22). They're heavy and slow ([Class items](class-items.md)).
- **Lethal grenade launchers,** which are too powerful for the ground pool. Non-lethal ones go in the [class item](class-items.md) pool.
- **Lethal rounds for underbarrel and rifle grenade launchers,** like frag, HEDP, and anti-tank grenades. The launchers themselves are ground loot, with smoke, star, and other non-lethal rounds ([Attachments](attachments.md#grenade-launchers)).
- **Belt-fed guns too fast for the ground,** like the [MG 42 / MG3](../weapons/crate/mg-42.md) family, as PUBG did with its MG3 ([Starting damage](starting-damage.md#crate-check-for-fast-firing-guns)).
- **The flash shield,** a ballistic shield with flashbangs on the front ([Class items](class-items.md)).
- **Mines,** like the claymore and the bouncing betty, as crate-only class items ([More class items](class-items.md#more-class-items)).
- **A minigun and a flamethrower** (owner, 2026-11-22). The Darne portable punt gun comes later ([Add later](../planning/add-later.md)).

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

## Special weapons

The owner's list, approved 2026-11-22. Each gets a gun page when it's added ([Gun queue](../planning/queue.md#special)). Arrows and bolts are quiet and can be picked back up after, like [throwing knives](#throwing-knives) (our pick).

| Subcategory | Weapon (real basis) | How it plays |
| --- | --- | --- |
| Bows | Recurve bow (modern hunting bow) | Quiet; arrows picked back up |
| Bows | Compound bow | Easier to hold drawn, faster arrows |
| Bows | Longbow (English war bow) | Heavy draw, hits hard, can't hold drawn long |
| Bows | Horse bow (short composite bow) | Quick draw, light arrows |
| Crossbows | Hunting crossbow (like PUBG's) | One bolt, slow reload, takes a scope |
| Crossbows | Pistol crossbow | Small and weak; pistol / 3rd slot |
| Crossbows | Repeating crossbow (Chinese, 4th century BC to the 1800s) | 7 to 10 bolts in 15 to 20 seconds from a top magazine; weak, about 70 m. A funny one |
| Crossbows | Arbalest (medieval steel crossbow) | Hardest-hitting bolt, very slow crank reload |
| Slingshots | Hunting slingshot | Steel balls, quiet, weak. A funny one |
| Black powder | Brown Bess (British flintlock musket) | Slow ramrod reload and a big smoke puff |
| Black powder | Kentucky long rifle | More accurate than a musket, just as slow to load |
| Black powder | Blunderbuss | A short-range spray of shot |
| Black powder | Nock volley gun (1780s British naval gun) | Seven barrels fired at once |
| Black powder | Duck's foot pistol | Several barrels fanned out, fired together |
| Black powder | Flintlock pistol | One shot, then a long reload |
| Underwater guns | APS underwater rifle (Soviet, fires darts) | Strong underwater, weak in air |
| Underwater guns | SPP-1 underwater pistol (Soviet, four barrels, darts) | Strong underwater, weak in air |
| Underwater guns | Band and pneumatic spearguns | Strong underwater, weak and short above it |
| Air guns | Girardoni air rifle (1780, carried by Lewis and Clark) | A quiet repeater with no smoke |
| Survival guns | AR-7 | Comes apart and stows in its own stock, which floats |
| Survival guns | M6 aircrew survival gun | A rifle barrel over a shotgun barrel |
| Survival guns | Drilling (German hunting gun) | Two shotgun barrels and a rifle barrel |
| Oddities | Gyrojet (1960s rocket pistol) | Small rockets that speed up after leaving the barrel |
| Oddities | Harmonica pistol (Jarre, France) | A sliding bar of chambers |
| Oddities | Apache revolver (France, 1800s) | A revolver, knuckle duster, and folding knife in one |
| Oddities | LeMat revolver (1850s) | A revolver with a shotgun barrel under it |

- **Underwater guns** are saved for maps with more water than the first one (owner, 2026-11-22).
- **The new gun groups** (black powder, underwater, air, survival, oddities) were approved on 2026-11-22. They follow every gun rule: one version per match, real fire modes, and misfires only as flavor text. Each needs its round on the [Ammo](ammo.md) page.
- **Maybe elsewhere:** a signal flare pistol that lights an area at night (maybe a class item), and a blowgun. The flamethrower is a crate weapon now.

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
| **Throwing knives** | A stack of 3, thrown one at a time and picked back up after ([Throwing knives](#throwing-knives)) | TBD |
| **Blue zone grenade** | Makes a small blue zone circle, up to about 10 m in radius, doing about 10 damage a second for about 10 seconds | TBD |

- **Weights TBD:** PUBG's weights for the sticky bomb, C4, decoy, and blue zone grenade weren't found yet.
- **Our own ideas:** an EMP grenade and a gas grenade.
- **From other games:** to add later.
- **Map max:** 4 per match, the smoke grenade plus 3 rolled ([Map caps](#how-the-randomness-works)).

### Throwing knives

Good for stealth when you have the upper hand, so they need limits to stay fair. First pass (our pick, damage the owner's):

- **A stack of 3,** thrown one at a time, about 0.6 s per throw.
- **Pick them back up:** off the ground, or by looting whoever they hit ([Bodies hold the loot](gameplay.md#knockdowns-revives)).
- **Damage:** 20 to the body, 30 to the head, 20 to the neck, and 12 to arms and legs; armor cuts it like bullets. All three landing on the body do 60 in all, so a full stack never kills a healthy player on its own (owner, 2026-11-22). They finish off a hurt player or soften one up before a fight.
- **Short range:** they drop fast and fly about 25 m/s, so they're reliable out to about 15 m, and a far throw can be dodged.
- **Quiet:** no gunshot, so only players nearby hear the throw and the hit.
- **Rare:** they spawn less often than grenades.

## Sources

- [PUBG Wiki: Airdrop](https://pubg.wiki.gg/wiki/Airdrop) (crate weapons over time) · [Samurai Gamers: PUBG thrown weapons](https://samurai-gamers.com/playerunknowns-battlegrounds-pubg/thrown-weapons-list/)
- [Wikipedia: Repeating crossbow](https://en.wikipedia.org/wiki/Repeating_crossbow)
- [PUBG Wiki: Grenades](https://pubg.wiki.gg/wiki/Grenades) (weights) · [PUBG Wiki: C4](https://pubg.wiki.gg/wiki/C4)
- [Gamertag Mythras: PUBG throwables and utility](https://gamertagmythras.com/blog/pubg-battlegrounds/pubg-throwables-utility-guide)
- [Dexerto: PUBG throwables](https://www.dexerto.com/wikis/pubg/weapons/throwable/)
