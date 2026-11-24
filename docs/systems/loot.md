# Loot and spawning

How loot appears on the map. The base is PUBG's system, with changes for this game's rotating guns and layered armor. Every number here is a starting point to tune in playtests.

## PUBG's system, the base

What PUBG did, from its own dev letters and patch notes:

- **Fixed spawn spots, random loot.** Loot spawns at set spots in buildings, and the game "pulls from a master table that distributes the loot differently every single game."
- **Better areas.** Some areas have better odds: community maps of Erangel marked areas with a chance of medium loot, good loot, and military gear.
- **Weapons by type.** On Erangel before its 2019 rebalance, ARs made up 2% of items picked up, DMRs 0.48%, and sniper rifles 0.12%. Sanhok, a smaller and faster map, ran 4.75%, 0.69%, and 0.26%.
- **Top-tier gear is rare.** Vikendi's update 25 cut level 3 helmets by 49% and level 3 vests by 36%.
- **Crates hold the best loot.** Care packages carry crate-only guns and rare attachments. In one 2017 community sample of about 100 crates, 61% had a sniper rifle, 56% had a level 3 vest or helmet, 17% had a ghillie suit, and 6% had a 15x scope.
- **Clutter costs.** In a 2019 test, players picked up only 67.85% of spawned items. PUBG then cut pistols, magazines, and grenades and raised key weapons and gear by about 10–20%.
- **Tuned all the time.** PUBG kept adjusting spawn rates "based on various data analysis and feedback." Update 27 in 2019, for example, raised Erangel's ARs by 12%, DMRs by 16%, and SMGs by 14%.

## How spawning works here

Every spawn spot rolls in steps, and every kind of loot follows the same pattern:

1. **Category:** what kind of item, weighted by the [category table](#starting-weights).
2. **Item:** which item in that category. Guns only come from the match's rolled [weapon pool](weapon-pool.md).
3. **Version, tier, or combo:** a gun rolls its version, rarer for versions that were rarely made ([weapon pool](weapon-pool.md#how-the-randomness-works)). Armor rolls its tier, then its carrier, plates, and rig ([Armor and gear](armor.md#vests)).
4. **Extras:** a gun spawns with some of its ammo next to it ([Ammo](ammo.md#spawning-and-special-rounds)).

## Changes from PUBG

- **The pool sets the guns.** Only the guns rolled for the match can spawn, so each category's share is split among that match's guns in it.
- **Areas have loot levels:** low (lone houses), medium (towns), high (big towns, schools, power plants), and military (bases). Higher levels have more spawn spots and better tier odds. Each map sets its own areas ([Maps](maps.md)).
- **No empty buildings.** Each building cluster rolls at least one gun, which fixes a common PUBG complaint.
- **Less clutter.** Following PUBG's 2019 lesson, pistols, extra mags, and throwables start a little lower, and the game logs what spawns and what players pick up, so spawns can be tuned from real numbers.
- **Crates:** every crate holds the same set: one crate weapon, its ammo, attachments that fit it (the thermal sight and 15x scope are crate-only), one tier 3 vest, one tier 3 helmet, and one class item. That's steadier than PUBG, whose crates varied. Lethal rounds for underbarrel and rifle grenade launchers come only from crates too; how many a crate holds is TBD ([Attachments](attachments.md#crate-rounds-lethal)).

## Starting weights

**Category, per spawn spot:**

| Category | Weight |
| --- | --- |
| Attachments | 18 |
| Weapons | 18 |
| Ammo (loose, on top of what spawns with guns) | 15 |
| Meds | 14 |
| Throwables | 8 |
| Crafting scrap | 8 |
| Vests | 6 |
| Helmets | 5 |
| Backpacks | 4 |
| Class items | 4 |

**Weapons, by category:**

| Weapon category | Weight |
| --- | --- |
| Assault rifles | 30 |
| SMGs | 18 |
| Shotguns | 14 |
| Pistols / 3rd slot | 12 |
| Battle rifles & DMRs | 12 |
| Snipers | 6 |
| LMGs | 5 |
| Special | 3 |

Battle rifles and DMRs sit higher than PUBG's DMRs did, since the category includes the standard rifles of many armies. Crate weapons never spawn on the ground.

**Armor and helmet tiers, by area:**

| Area | Tier 1 | Tier 2 | Tier 3 |
| --- | --- | --- | --- |
| Low | 60% | 40% | 0% |
| Medium | 45% | 52% | 3% |
| High | 30% | 62% | 8% |
| Military | 20% | 65% | 15% |
| Crates | — | — | 100% |

Tier 2 took in what used to be tiers 2 and 3, so its odds are the two added together.

**Backpack tiers, by area (our pick, 2026-11-24):** a little more generous than armor, since a bigger pack carries more but doesn't win a fight on its own ([Backpacks](armor.md#backpacks)).

| Backpacks by area | Tier 1 | Tier 2 | Tier 3 |
| --- | --- | --- | --- |
| Low | 60% | 35% | 5% |
| Medium | 45% | 45% | 10% |
| High | 35% | 50% | 15% |
| Military | 25% | 50% | 25% |
| Vaults | — | — | 100% |

Crates hold no backpack: their set stays the same every time (see Crates above), and PUBG's care packages didn't carry backpacks either.

Backpacks, scopes, and mag tiers follow the same idea: common low tiers everywhere, better ones in better areas, and the best in crates. Makeshift armor tiers are crafted, never spawned ([Crafting](crafting.md)).

## Briefcases

Guns that came in a real carry case, like the [AS Val](../weapons/assault-rifles/as-val.md), [VSS Vintorez](../weapons/battle-rifles/vss.md), and [OTs-14 Groza](../weapons/assault-rifles/ots-14-groza.md), can spawn as a briefcase find (owner, 2026-11-22).

- **Rare,** and locked: you pick the briefcase open to get the gun (owner's idea).
- **The screwdriver** picks small locks ([Built-in tools](gameplay.md#built-in-tools)), so it's what opens a briefcase (our pick). How long picking takes, and which other guns qualify, are TBD.

## Sources

- [Gamer Maps: PUBG dev letter, Erangel loot rebalance (March 2019)](https://www.gamermaps.net/news/pubg-dev-letter-erangel-loot-rebalance)
- [PC Gamer: How PUBG will be changing loot drops (June 2017)](https://www.pcgamer.com/heres-how-playerunknowns-battlegrounds-will-be-changing-loot-drops)
- [Sportskeeda: Vikendi spawn rates after update 25](https://sportskeeda.com/esports/everything-you-need-to-know-about-pubg-snow-map-vikendi-items-spawn-rate-after-being-rebalanced-in-pubg-update-25)
- [Comicbook: PUBG update 27 raises loot spawns (March 2019)](https://comicbook.com/gaming/news/pubg-update-increases-loot-spawn-rates)
- [GitHub: PUBG crate analysis (June 2017)](https://gist.github.com/fu5ha/418be10c8830c375c762c48107901d49)
- [Mein-MMO: PUBG loot map (2017)](https://mein-mmo.de/en/pubg-loot-map,183328/)
