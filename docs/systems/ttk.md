# Time to kill (TTK)

TTK is how long a gun takes to kill a target when every shot lands. The first shot hits instantly, so only the gaps between shots count.

**Goal:** no single gun should win every fight. TTK needs more discussion.

Range is a main balancing tool: damage falloff, recoil, and handling give each gun a distance where it wins, so no single gun is best everywhere.

```text
TTK = (shots to kill - 1) × 60 / RPM
```

- **Shots to kill:** target health divided by damage per hit, rounded up.
- **Damage per hit:** base damage × hit-zone multiplier × armor reduction × range falloff. Shooters commonly multiply these together, as CS2 does.
- **Fire rate (RPM):** rounds per minute. For semi-autos, it's a set max rate.
- **Breakpoints:** a damage change only matters when it changes shots to kill. On 100 health, 33 damage takes 4 shots but 34 takes 3.
- **Theoretical vs. effective TTK:** the formula assumes perfect accuracy. Recoil, spread, and misses make real TTK longer, and a very fast TTK covers up misses, which works against skilled players.
- **Magazine size:** a gun with fewer rounds than shots to kill needs a reload mid-fight, and small mags limit kills per mag.
- **PUBG-style armor:** each vest or helmet level cuts damage by a flat percentage (community-reported as 30%, 40%, and 55% for levels 1 to 3). Ours uses the same three tiers ([Armor](armor.md#tiers)), and guns are balanced around tier 2.

Illustrative example with made-up numbers (100 health, chest hits, no armor):

| Gun | Damage | Shots to kill | Fire rate | TTK | Kills per mag |
| --- | --- | --- | --- | --- | --- |
| M17 | 25 | 4 | 400 RPM (0.15 s between shots) | 0.45 s | 4 (17 rounds) |
| Glisenti | 34 | 3 | 240 RPM (0.25 s between shots) | 0.50 s | 2 (7 rounds) |

Higher damage keeps the Glisenti's TTK close to the M17's, while its 7-round mag still holds it back in longer fights.

Sources: [CSDB: CS2 damage calculator](https://csdb.gg/damage-calculator/) · [Insider Gaming: Warzone TTK](https://insider-gaming.com/warzone-devs-address-fast-time-to-kill-concerns-on-verdansk/) · [Steam forum: PUBG armor values](https://steamcommunity.com/app/578080/discussions/1/1471966894874045224)

## Roles by category

Every category has a job and a range where it should win, so no gun is worthless at its job and none wins everywhere. Damage, falloff, and handling keep each one there. Handling has a first pass, based on PUBG's numbers, on [Handling](handling.md).

| Category | Job | Where it wins | What keeps it there |
| --- | --- | --- | --- |
| Pistols / 3rd slot | Backup, early fights, finishing | 0–25 m | Fastest draw and swap and the best hip fire on the move; pistol rounds fall off fast |
| Shotguns | One-shot up close | 0–15 m | A full buckshot hit kills through a tier 2 vest; pellets spread and lose damage fast past 15 m. Slugs trade the one-shot for reach to about 100 m |
| SMGs | Close quarters on the move | 0–50 m | The best hip fire and fastest ADS of the primary guns, light recoil, faster movement, and PUBG's bigger limb multiplier (1.2, against 0.9 for ARs); pistol rounds fall off to 60% by 180 m |
| Assault rifles | All-rounder | 25–250 m | The middle of everything; falls off to 75% by 450 m |
| Battle rifles & DMRs | Picks at mid to long range | 100–400 m | One fewer shot to kill than an AR (3 against 4 or 5 through a tier 2 vest), little falloff, and DMR multipliers (body 1.05, limbs 1.15); heavier recoil, slower ADS, and hard-to-control full auto |
| LMGs | Sustained fire: holding angles, suppression, vehicles | 25–250 m, best from a bipod or prone | Big belts and drums and the highest fire-rate band; the slowest ADS and movement, steady only on a bipod, slow belt reloads, and falloff to 75% by 300 m |
| Snipers | One-shot picks at range | 200 m and beyond | A head shot kills through a tier 2 helmet and two body shots through a tier 2 vest, with almost no falloff; slow bolts, slow ADS, and scope sway |

How damage keeps every gun inside its category's job is on [Starting damage](starting-damage.md): fast guns hit lighter, slow guns hit harder, and manual-action guns pass a test for their job.

### Damage falloff

Like PUBG, every bullet loses damage over distance, and each category falls off at its own rate. The base is PUBG's current curve for one gun per category (PUBG doesn't publish its 2018 curves). Damage drops in a straight line between the listed points, and the lowest value holds from there on.

| Category | Full damage to | 50 m | 100 m | 200 m | 300 m | Lowest | Basis |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Shotguns, buckshot (per pellet) | 5 m | 55% (80% at 20 m) | — | — | — | 45% from 70 m | PUBG's DBS |
| Shotguns, slugs | 25 m | 92% | 75% | 60% | 60% | 60% from 150 m | Our pick |
| Pistols, SMGs, and any gun firing a pistol round | 10 m | 79% | 66% | 60% | 60% | 60% from 180 m | PUBG's Vector (PUBG's own revolver barely falls off, but here all pistol rounds share one curve) |
| Assault rifles | 50 m | 100% | 95% | 85% | 78% | 75% from 450 m | Our pick, between the two below; PUBG's M416 stops falling off at 450 m |
| Battle rifles & DMRs | 50 m | 100% | 97% | 91% | 85% | 79% from 420 m | PUBG's Mk12 |
| LMGs | 50 m | 100% | 95% | 82% | 75% | 75% from 300 m | PUBG's DP-28 to 225 m, then our pick |
| Snipers | 100 m | 100% | 100% | 98% | 96% | 85% from 600 m | Our pick |

### Role check

Time to kill through a tier 2 vest with chest hits, at each category's falloff, for one common gun per category with its first-pass damage. Times assume every shot lands; the shot count is in brackets.

| Gun | Damage | RPM | 5 m | 15 m | 25 m | 50 m | 100 m | 200 m | 300 m | 400 m |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| [Remington 870](../weapons/shotguns/remington-870.md), 12 gauge buckshot | 24 × 9 | 80 | Instant (1) | Instant (1) | 0.75 s (2) | 0.75 s (2) | Out of range | Out of range | Out of range | Out of range |
| [Remington 870](../weapons/shotguns/remington-870.md), 12 gauge slug | 54 | 80 | 2.25 s (4) | 2.25 s (4) | 2.25 s (4) | 2.25 s (4) | 3.00 s (5) | 3.75 s (6) | 3.75 s (6) | 3.75 s (6) |
| [Glock 17](../weapons/pistols/glock-17-18.md) | 35 | 450 | 0.53 s (5) | 0.53 s (5) | 0.67 s (6) | 0.80 s (7) | 0.93 s (8) | 0.93 s (8) | 0.93 s (8) | 0.93 s (8) |
| [MP5](../weapons/smgs/mp5.md) | 39 | 800 | 0.30 s (5) | 0.30 s (5) | 0.30 s (5) | 0.38 s (6) | 0.45 s (7) | 0.53 s (8) | 0.53 s (8) | 0.53 s (8) |
| [M4](../weapons/assault-rifles/m16-m4.md) | 43 | 700–970 | 0.22 s (4) | 0.22 s (4) | 0.22 s (4) | 0.22 s (4) | 0.29 s (5) | 0.29 s (5) | 0.29 s (5) | 0.36 s (6) |
| [SR-25](../weapons/battle-rifles/sr-25.md) | 58 | 600 | 0.20 s (3) | 0.20 s (3) | 0.20 s (3) | 0.20 s (3) | 0.20 s (3) | 0.30 s (4) | 0.30 s (4) | 0.30 s (4) |
| [M249](../weapons/lmgs/minimi.md) | 43 | 700–1,150 | 0.19 s (4) | 0.19 s (4) | 0.19 s (4) | 0.19 s (4) | 0.26 s (5) | 0.26 s (5) | 0.32 s (6) | 0.32 s (6) |
| [M24](../weapons/snipers/remington-700.md) | 79 | 32 | 1.88 s (2) | 1.88 s (2) | 1.88 s (2) | 1.88 s (2) | 1.88 s (2) | 1.88 s (2) | 1.88 s (2) | 3.75 s (3) |

- **Shotguns own 0–15 m:** one full hit kills before anything else can fire twice. Past 15 m they need two hits even if every pellet lands, and pellets spread, so in practice it's worse.
- **SMGs trail ARs in perfect-aim time,** as PUBG's did (UMP9 0.37 s against the M416's 0.26 s through a level 2 vest). Up close their edge is everything perfect aim leaves out: hip fire, ADS speed, movement, and recoil, plus limb hits, which vests don't cover. Through a tier 2 vest an SMG's limb hit (39 × 1.2 = 47) does twice its chest hit (23), while an AR's (43 × 0.9 = 39) does 1.5 times.
- **DMRs need one fewer shot than ARs** from 100 m out and stay at 4 to 400 m, while ARs and LMGs climb to 5 and 6. At range, every extra shot is another chance to miss under recoil and bullet drop.
- **Snipers stay at two body shots to 300 m,** and their head shots kill through a tier 2 helmet at any range.
- **Pistols are backups:** close to twice an SMG's time at every range.

## Hit zones

Six zones, each with a multiplier on the gun class's damage. The head, body, and limb multipliers are PUBG's 2018 ones ([table](#pubg-in-2018-for-reference)).

| Zone | Multiplier | Armor that covers it |
| --- | --- | --- |
| Head | The class's head multiplier: 2.0 pistols, 1.8 SMGs, 2.35 assault rifles, battle rifles & DMRs, and LMGs, 2.5 snipers, 1.5 shotguns | Helmet |
| Neck | 0.7 × the head multiplier | The helmet, or a vest with neck coverage; the higher tier counts |
| Chest and stomach | The class's body multiplier | Vest |
| Groin | The class's body multiplier | Only vests that cover the groin |
| Arms | The class's limb multiplier | Only vests that cover the arms |
| Legs | The class's limb multiplier | None |

Hands and feet count as arms and legs. Which vests cover the neck, groin, and arms is on [Armor and gear](armor.md#vests).

### No lucky one-shots

The extra zones must never make a stray hit end someone, as in Tarkov. So:

- **One health pool,** like PUBG: no zone has its own health, so no single hit to a small zone kills unless the damage itself reaches 100.
- **No gaps:** no face or eye zone slips past the helmet. The whole head uses the helmet, and the neck uses the helmet or the vest's collar.
- **No dice:** armor cuts damage by a flat percentage every time. There are no penetration rolls and no random critical hits.
- **The neck is 0.7 of the head, not PUBG's 0.75,** so no automatic gun on the ground kills with one neck hit, even with no helmet. At 0.75, thirty full-power automatic versions (the M60, BAR, G3, and others) would.
- **With any helmet on,** the only ground guns that kill with one head shot are snipers, shotguns up close, the [Janz](../weapons/pistols/janz.md) magnum revolvers, and the rare SVDK [SVD](../weapons/battle-rifles/svd.md) (61, like PUBG's Mk14, which also one-shot level 1 helmets). All of them are slow, aimed shots. With no helmet, most rifles kill with one head shot, as in PUBG; that's what helmets are for.
- **The M4 with no helmet (checked 2026-11-24, playtest round 8):** in PUBG in 2018 the M416 did 43 with a 2.35 head multiplier, 101 to an unhelmeted head, so it killed with one head shot ([table](#pubg-in-2018-for-reference)). Ours is the same: our M4 versions do 43 × 2.35 = 101, one head shot up close. Past about 50 m, falloff (0.95 at 100 m) brings it under 100, so it takes two. With any helmet, it takes two.

## How damage is set

Damage is set per gun, not per caliber, like PUBG. Two guns firing the same round can hit differently, so each one feels right for its role. PUBG's 5.56mm guns ran from 43 to 46 damage, and its 7.62mm guns from 49 (AKM) to 79 (M24).

Our best guess at PUBG's method, used here (details and every number on [Starting damage](starting-damage.md)):

1. **Start from an anchor:** the table for the round's class, anchored on the PUBG gun closest in class and round (table below) and scaled by the round's energy.
2. **Balance by fire rate:** within a class, damage times fire rate stays in a band, so faster guns hit lighter. In the June 2018 numbers, PUBG's ARs landed between about 27,000 and 37,000 damage per minute (SCAR-L to Groza), and its SMGs between about 25,000 and 37,000 (UMP9 to Vector).
3. **Pass the role test:** manual-action guns, like pumps and bolt actions, must still do their category's job.
4. **Adjust for trade-offs** in play testing: harder recoil, a smaller mag, or slower handling earn a little more damage, and the reverse earns less.
5. **Check breakpoints** at every armor tier and hit zone, so similar guns don't end up identical and each armor tier changes shots to kill.
6. **Per version:** versions can change caliber or barrel, so damage is set per version, in the Damage column of its Versions table.

| Class | PUBG anchors (June 2018 damage) |
| --- | --- |
| Pistols | P18C 23 (9mm, auto), P92 35 (9mm), P1911 41 (.45 ACP) |
| SMGs | Micro Uzi 26, Vector 34, UMP9 39, Tommy Gun 40 |
| Shotguns | S12K 198, S1897 and S686 216 (all pellets together) |
| ARs | M416, SCAR-L, and M16A4 43 (5.56mm); AKM and Groza 49 (7.62mm) |
| DMRs | Mini 14 46 (5.56mm); SKS 53, SLR 58, Mk14 61 (7.62mm) |
| LMGs | M249 45 (5.56mm), DP-28 51 |
| Snipers | Win94 66, Kar98k 75, M24 79, AWM 120 |

Crate snipers follow PUBG's AWM, which one-shot level 3 helmets: their head shot kills through any helmet, tier 3 included. That's the crate line for every category ([Starting damage](starting-damage.md#baselines-and-crate-lines)).

## Fire rates

PUBG's automatic guns fire close to the real guns' cyclic rates (AKM 600, SCAR-L 625, M416 698, M16A4 800, Micro Uzi 1,250, and M249 800 RPM in June 2018), and its semi-autos and manual guns have a fixed fastest rate. The first pass here follows the same pattern. Each version's RPM column holds its rate; where the real rate wasn't known, the rules below filled it in, and real numbers replace them as they're found.

| Action | First-pass rate (RPM) | PUBG basis |
| --- | --- | --- |
| Automatic and burst | The real cyclic rate; if unknown, a sibling version's; if none, 700 (assault rifles, SMGs), 650 (battle rifles & DMRs, LMGs), 1,000 (machine pistols), or 300 (shotguns) | Real cyclic rates, as above; P18C 1,000 |
| Semi-only version of an automatic gun | The family's auto rate | PUBG's assault rifles fire single shots at their auto rate |
| Semi-auto pistol | 450 | P92: 0.135 s between shots |
| Semi-auto battle rifle, DMR, or sniper | 600 | SKS, SLR, and Mini 14: 0.100 s |
| Semi-auto shotgun | 240 | S12K: 0.25 s |
| Bolt action | 32 (Lee–Enfield 40, for its fast bolt) | Kar98k 1.9 s, M24 1.8 s, AWM 1.85 s |
| Straight-pull | 50 | Our pick: faster than a turned bolt |
| Lever | 100 | Win94: 0.6 s |
| Pump | 80 | S1897: 0.75 s |
| Break action | 300 (between barrels) | S686: 0.2 s |
| Revolver | 240 | Our pick |
| Two-pull | 120 | Our pick |
| Single shot | Stays TBD | Reload-bound |

For semi-autos and manual guns, the rate is the fastest the gun allows; real speed depends on how fast you click. A source's aimed rate isn't the cap: the C96 and Luger, listed at about 120 RPM aimed, play at 450 like other semi-auto pistols. Semi-auto shotguns use 240 in any category, like the G3-based G12.

## Bullet speed

Like PUBG, every gun has its own bullet speed, close to the real gun's muzzle velocity, and bullets slow down and drop over distance. PUBG's AKM fires at 715 m/s and its M416 at 880 m/s. Its AWM leaves the barrel at 945 m/s and is down to about 769 m/s at 500 m.

Here, each version uses its real muzzle velocity, so a long barrel shoots faster than a short one in the same round. [Bullet crack](gameplay.md#sound) uses the same speed: a bullet still faster than sound when it passes you cracks. Drag and drop numbers are TBD.

## PUBG in 2018, for reference

These are PUBG PC's numbers from June 2018 (Patch 1.0 #15), from LeNutch's community spreadsheet. PUBG never published official values, so treat them as close, not exact. Targets have 100 health. Times assume every shot lands on the chest; the shot count is in brackets.

**Hit-zone multipliers:**

| Class | Head | Body | Arms and legs |
| --- | --- | --- | --- |
| Pistols | 2.0 | 1.0 | 1.0 |
| Shotguns | 1.5 | 1.0 | 0.9 |
| SMGs | 1.8 | 1.0 | 1.2 |
| ARs | 2.35 | 1.0 | 0.9 |
| DMRs | 2.35 | 1.05 | 1.15 |
| Snipers | 2.5 | 1.1 | 0.95 |

The sheet also lists arms and legs at 50% damage. Level 1, 2, and 3 vests and helmets cut damage by 30%, 40%, and 55%. Helmets hold 80, 150, and 230 durability; vests hold 200, 220, and 250.

**PUBG's hit zones:** the 2018 sheet only splits head, body, and limbs, but PUBG's body has 13 zones. Each zone's hit-area multiplier stacks with the class multiplier above: head for the head and neck, body for the torso, limbs for the arms and legs. These are today's values (2025–2026 patches), from PUBG Statistics.

| Zone | Hit-area multiplier | Class multiplier it uses | Armor that covers it |
| --- | --- | --- | --- |
| Head | 1.0 | Head | Helmet |
| Neck | 0.75 | Head | Helmet |
| Clavicle | 1.0 | Body | Vest |
| Chest | 1.1 | Body | Vest |
| Upper stomach | 1.0 | Body | Vest |
| Lower stomach | 0.95 | Body | Vest |
| Pelvis | 1.0 | Body (LMGs use 1.0 here) | Vest |
| Upper arm, thigh | 0.6 | Limbs | None |
| Forearm, calf | 0.5 | Limbs | None |
| Hand, foot | 0.3 | Limbs | None |

So a neck hit does three-quarters of a head hit, the chest a little more than the stomach, and a hand or foot under a third of an upper arm or thigh. The game's own six zones are under [Hit zones](#hit-zones).

**Time to kill, chest hits:**

| Gun | Class | Damage | Fire rate (RPM) | No vest | Level 1 vest | Level 2 vest | Level 3 vest | Head shots to kill (no helmet, level 1, 2, 3) |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| M416 | AR | 43 | 698 | 0.17 s (3) | 0.26 s (4) | 0.26 s (4) | 0.43 s (6) | 1, 2, 2, 3 |
| SCAR-L | AR | 43 | 625 | 0.19 s (3) | 0.29 s (4) | 0.29 s (4) | 0.48 s (6) | 1, 2, 2, 3 |
| M16A4¹ | AR | 43 | 800 | 0.15 s (3) | 0.22 s (4) | 0.22 s (4) | 0.38 s (6) | 1, 2, 2, 3 |
| AKM | AR | 49 | 600 | 0.20 s (3) | 0.20 s (3) | 0.30 s (4) | 0.40 s (5) | 1, 2, 2, 2 |
| Groza | AR | 49 | 750 | 0.16 s (3) | 0.16 s (3) | 0.24 s (4) | 0.32 s (5) | 1, 2, 2, 2 |
| AUG A3² | AR | 43 | 700 | 0.17 s (3) | 0.26 s (4) | 0.26 s (4) | 0.43 s (6) | 1, 2, 2, 3 |
| Beryl M762²³ | AR | 47 | 698 | 0.17 s (3) | 0.26 s (4) | 0.26 s (4) | 0.34 s (5) | 1, 2, 2, 3 |
| M249⁴ | AR | 45 | 800 | 0.15 s (3) | 0.22 s (4) | 0.22 s (4) | 0.30 s (5) | 1, 2, 2, 3 |
| UMP9 | SMG | 39 | 652 | 0.18 s (3) | 0.28 s (4) | 0.37 s (5) | 0.46 s (6) | 2, 3, 3, 4 |
| Vector | SMG | 34 | 1,091 | 0.11 s (3) | 0.22 s (5) | 0.22 s (5) | 0.33 s (7) | 2, 3, 3, 4 |
| Micro Uzi | SMG | 26 | 1,250 | 0.14 s (4) | 0.24 s (6) | 0.29 s (7) | 0.38 s (9) | 3, 4, 4, 5 |
| Tommy Gun | SMG | 40 | 698 | 0.17 s (3) | 0.26 s (4) | 0.34 s (5) | 0.43 s (6) | 2, 2, 3, 4 |
| Mini 14¹ | DMR | 46 | 600 | 0.20 s (3) | 0.20 s (3) | 0.30 s (4) | 0.40 s (5) | 1, 2, 2, 3 |
| SKS¹ | DMR | 53 | 667 | 0.09 s (2) | 0.18 s (3) | 0.18 s (3) | 0.27 s (4) | 1, 2, 2, 2 |
| Mk14 EBR | DMR | 61 | 667 | 0.09 s (2) | 0.18 s (3) | 0.18 s (3) | 0.27 s (4) | 1, 1, 2, 2 |
| Kar98k¹ | Sniper | 75 | 32 | 1.90 s (2) | 1.90 s (2) | 3.80 s (3) | 3.80 s (3) | 1, 1, 1, 2 |
| M24¹ | Sniper | 79 | 33 | 1.80 s (2) | 1.80 s (2) | 1.80 s (2) | 3.60 s (3) | 1, 1, 1, 2 |
| AWM¹ | Sniper | 120 | 32 | Instant (1) | 1.85 s (2) | 1.85 s (2) | 1.85 s (2) | 1, 1, 1, 1 |

1. Semi-auto, burst, or bolt-action: the fire rate is the fastest it can shoot, so real times depend on how fast you click.
2. Fire rate from pubg.wiki.gg's current values; the 2018 sheet left it blank.
3. Damage from Gamepressure's 2019 guide; the June 2018 sheet came out before the Beryl.
4. Assumes the AR multipliers; the sheet has no LMG column.

**What stands out:**

- **Armor matters more than the gun.** The M416 kills in 3 chest shots with no vest and 6 against a level 3 vest.
- **Breakpoints decide fights.** The AKM's 49 damage kills through a level 1 vest in 3 shots; the M416's 43 needs 4. That's why the AKM hits harder but the M416 fires faster.
- **Head shots are huge.** Every AR kills an unhelmeted head in one shot. The Kar98k and M24 one-shot heads up to a level 2 helmet, and only the AWM one-shots a level 3 helmet.
- **Close calls:** the Kar98k's chest hit against a level 2 vest does 49.5, so two hits leave 1 health.
- **Perfect hits kill fast.** Against a level 2 vest, the automatic guns kill in about 0.2 to 0.4 seconds of perfect chest hits. Recoil and misses make real fights much longer, which is where gun feel comes in.

Sources: [PUBG Map: DMRs](https://pubgmap.io/weapons/dmr.html) · [PUBG Wiki: Shotguns](https://pubg.wiki.gg/wiki/Shotguns) · [PUBG Wiki: Sniper Rifles](https://pubg.wiki.gg/wiki/Sniper_Rifles) · [Medium: Does bullet velocity really matter in PUBG? (2019)](https://medium.com/@midopooler/does-bullet-velocity-really-matter-in-pubg-cba1d571ce6f) · [LeNutch: PUBG weapon stats, Patch 1.0 #15 (June 2018)](https://docs.google.com/spreadsheets/d/13ZI5GQDbCXl7IlVCVnEA6aZVfC7NFJLBsXPIAGFMNj4/htmlview?sle=true) · [Gamepressure: PUBG assault rifles (2019)](https://www.gamepressure.com/playerunknowns-battlegrounds/assault-rifles-ar/z9a233) · [PUBG Wiki: Assault Rifles](https://pubg.wiki.gg/wiki/Assault_Rifles) · [PUBG Statistics: RPD](https://pubgstatistics.com/weapons/rpd) · [PUBG Statistics: Vector](https://pubgstatistics.com/weapons/vector)

Reliability: guns never jam or overheat (see [Rules](../rules.md)). Some items wear out, like suppressors and the StG 44's Krummlauf ([Wear](attachments.md#wear)).
