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
- **PUBG-style armor:** each vest or helmet level cuts damage by a flat percentage (community-reported as 30%, 40%, and 55% for levels 1 to 3).

Illustrative example with made-up numbers (100 health, chest hits, no armor):

| Gun | Damage | Shots to kill | Fire rate | TTK | Kills per mag |
| --- | --- | --- | --- | --- | --- |
| M17 | 25 | 4 | 400 RPM (0.15 s between shots) | 0.45 s | 4 (17 rounds) |
| Glisenti | 34 | 3 | 240 RPM (0.25 s between shots) | 0.50 s | 2 (7 rounds) |

Higher damage keeps the Glisenti's TTK close to the M17's, while its 7-round mag still holds it back in longer fights.

Sources: [CSDB: CS2 damage calculator](https://csdb.gg/damage-calculator/) · [Insider Gaming: Warzone TTK](https://insider-gaming.com/warzone-devs-address-fast-time-to-kill-concerns-on-verdansk/) · [Steam forum: PUBG armor values](https://steamcommunity.com/app/578080/discussions/1/1471966894874045224)

## How damage is set

Damage is set per gun, not per caliber, like PUBG. Two guns firing the same round can hit differently, so each one feels right for its role. PUBG's 5.56mm guns ran from 43 to 46 damage, and its 7.62mm guns from 49 (AKM) to 79 (M24).

Our best guess at PUBG's method, used here:

1. **Start from an anchor:** the PUBG gun closest in class and round (table below), scaled by the round's energy ([Starting damage](starting-damage.md)).
2. **Balance by fire rate:** within a class, damage times fire rate stays in a band, so faster guns hit lighter. In the June 2018 numbers, PUBG's ARs landed between about 27,000 and 37,000 damage per minute (SCAR-L to Groza), and its SMGs between about 25,000 and 37,000 (UMP9 to Vector).
3. **Adjust for trade-offs:** harder recoil, a smaller mag, or slower handling earn a little more damage, and the reverse earns less.
4. **Check breakpoints** at every armor tier and hit zone, so similar guns don't end up identical and each armor tier changes shots to kill.
5. **Per version:** versions can change caliber or barrel, so damage is set per version and goes in its Versions table row once set.

| Class | PUBG anchors (June 2018 damage) |
| --- | --- |
| Pistols | P18C 23 (9mm, auto), P92 35 (9mm), P1911 41 (.45 ACP) |
| SMGs | Micro Uzi 26, Vector 34, UMP9 39, Tommy Gun 40 |
| Shotguns | S12K 198, S1897 and S686 216 (all pellets together) |
| ARs | M416, SCAR-L, and M16A4 43 (5.56mm); AKM and Groza 49 (7.62mm) |
| DMRs | Mini 14 46 (5.56mm); SKS 53, SLR 58, Mk14 61 (7.62mm) |
| LMGs | M249 45 (5.56mm), DP-28 51 |
| Snipers | Win94 66, Kar98k 75, M24 79, AWM 120 |

Crate snipers follow PUBG's AWM, which one-shot level 3 helmets: their head shot kills through any helmet, tier 4 included. That's the crate line for every category ([Starting damage](starting-damage.md#baselines-and-crate-lines)).

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

Sources: [PUBG Wiki: Sniper Rifles](https://pubg.wiki.gg/wiki/Sniper_Rifles) · [Medium: Does bullet velocity really matter in PUBG? (2019)](https://medium.com/@midopooler/does-bullet-velocity-really-matter-in-pubg-cba1d571ce6f) · [LeNutch: PUBG weapon stats, Patch 1.0 #15 (June 2018)](https://docs.google.com/spreadsheets/d/13ZI5GQDbCXl7IlVCVnEA6aZVfC7NFJLBsXPIAGFMNj4/htmlview?sle=true) · [Gamepressure: PUBG assault rifles (2019)](https://www.gamepressure.com/playerunknowns-battlegrounds/assault-rifles-ar/z9a233) · [PUBG Wiki: Assault Rifles](https://pubg.wiki.gg/wiki/Assault_Rifles)

Reliability: guns never jam or overheat (see [Rules](../rules.md)). Whether some items wear out is still open; the makeshift suppressor and the StG 44's Krummlauf are the current wear ideas.
