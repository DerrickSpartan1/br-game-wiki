# Starting damage and the crate line

How each round gets a starting damage number, and when a gun is too much for ground loot. Starting damage is step 1 of [how damage is set](ttk.md#how-damage-is-set): fire rate, trade-offs, and breakpoints still adjust each gun after.

## The method

1. **A baseline per category:** a PUBG gun and its round, with PUBG's June 2018 damage and head multiplier ([TTK](ttk.md#pubg-in-2018-for-reference)).
2. **Scale by energy:** starting damage = baseline damage × √(round's energy ÷ baseline round's energy). The square root keeps big rounds strong without making them absurd: a .50 BMG has about 4.4 times a 7.62 NATO's energy but gets about 2.1 times the damage.
3. **The crate line:** a version is crate-only if one head shot at its starting damage kills through a tier 4 helmet: damage × head multiplier × 0.4 (the helmet's 60% cut) reaches 100 health. That's where PUBG drew its line: its ground snipers couldn't one-shot a level 3 helmet, and only the crate AWM could.
4. **Crate-only versions** are marked `(crate)` after their name and never spawn on the ground. The rest of their family still does.

Energies are typical full-power loads from Wikipedia's cartridge table; short barrels and subsonic loads hit less. Damage rounds to whole numbers. The method lands close to PUBG on several guns: 7.62×39mm comes out at 48 for assault rifles (PUBG's AKM: 49), and .45 ACP at 41 for SMGs (Tommy Gun: 40).

## Baselines and crate lines

| Category | Baseline | Head multiplier | Crate line | Energy that crosses it | Strongest round now | Crosses? |
| --- | --- | --- | --- | --- | --- | --- |
| [Pistols / 3rd slot](../weapons/pistols/index.md) | P92 35 (9×19mm, 464 J) | 2× | 125 | About 5,900 J | 7.62×51mm, 104 | No |
| [SMGs](../weapons/smgs/index.md) | UMP9 39 (9×19mm, 464 J) | 1.8× | 139 | About 5,900 J | .30 Carbine, 66 | No |
| [Assault rifles](../weapons/assault-rifles/index.md) | M416 43 (5.56×45mm, 1,622 J) | 2.35× | 107 | About 10,000 J | 7.62×51mm, 68 | No |
| [Battle rifles & DMRs](../weapons/battle-rifles/index.md) | SLR 58 (7.62×51mm, 4,063 J) | 2.35× | 107 | About 13,800 J | 9.3×64mm Brenneke, 70 | No |
| [LMGs](../weapons/lmgs/index.md) | M249 45 (5.56×45mm, 1,622 J) | 2.35× | 107 | About 9,200 J | .30-06 Springfield, 73 | No |
| [Snipers](../weapons/snipers/index.md) | M24 79 (7.62×51mm, 4,063 J) | 2.5× | 100 | About 6,500 J | .338 Lapua Magnum, 100 | Yes: the .338 Lapua versions (M24A3, AWM .338) go to crates |

- **Only the .338 Lapua crosses,** and only just: it lands at about 99.6, which rounds to 100. The .300 Winchester Magnum stays on the ground at 90; it one-shots tier 3 helmets but not tier 4.
- **The .50 BMG** would start at 166 as a sniper, far over the line, so .50-caliber rifles are crate weapons.
- **Everything else is well under its line,** so damage alone doesn't push any other ground gun into crates.
- **Watch the rifle-caliber pistols:** the strongest 3rd-slot gun is the [SA58 pistol](../weapons/pistols/sa58-pistol.md) in 7.62×51mm, at 104. That one-shots heads through a tier 3 helmet, still under the line, though its short barrel really loses a lot of energy. The .500 S&W [Janz](../weapons/pistols/janz.md) starts at 95 and one-shots through tier 2, like PUBG's Kar98k did up to level 2.
- **Shotguns** have their own scale, below.
- **A second check comes later** for fast-firing guns, once fire rates are set, since PUBG also crated guns for how fast they killed, like the Groza and the M249.

## Shotguns

Shotguns get their own scale, since their damage is split across pellets. The base is PUBG's June 2018 pump and double-barrel shotguns, the S1897 and S686: 9 pellets of 24 damage, 216 in all. Every shell here fires 9 pellets, as PUBG's do.

1. **By gauge:** per-pellet damage scales by the square root of the shell's standard shot load, like the rest of this page: 12 gauge's 1⅛ oz is the base.
2. **By action:** semi-auto and automatic shotguns hit about 8% lighter per pellet, as PUBG's S12K (22 per pellet in 2018) did next to its pumps. Pumps, levers, and break actions hit full.
3. **Short barrels,** like sawed-offs and the [Ithaca 37 Stakeout](../weapons/pistols/ithaca-37-stakeout.md), hit about 20% lighter, as PUBG's sawed-off (21 per pellet today, against 26 for its full-length guns) does.
4. **Slugs** are one projectile worth a quarter of a full buckshot hit, about one big DMR shot (PUBG's SKS: 53), with much less falloff over range.

| Gauge | Standard shot load | Pump, lever, or break action (per pellet × 9) | Semi or auto (per pellet × 9) | Slug |
| --- | --- | --- | --- | --- |
| 10 gauge | 1¾ oz | 30 × 9 = 270 | 27 × 9 = 243 | 68 |
| 12 gauge | 1⅛ oz | 24 × 9 = 216 | 22 × 9 = 198 | 54 |
| 16 gauge | 1 oz | 23 × 9 = 207 | 21 × 9 = 189 | 52 |
| 20 gauge | ⅞ oz | 21 × 9 = 189 | 19 × 9 = 171 | 47 |
| 28 gauge | ¾ oz | 20 × 9 = 180 | 18 × 9 = 162 | 45 |
| .410 bore | ½ oz | 16 × 9 = 144 | 15 × 9 = 135 | 36 |

Short-barrel versions take 80% of these. Shotgun head shots use PUBG's 2018 multiplier of 1.5. At that multiplier, a full buckshot hit is never crate-level: the crate line would need 167 damage in one projectile. The crate-only FRAG-12 and dragon's breath rounds are TBD.

## Starting damage by category

TBD rounds aren't in the energy table yet; none of them are strong enough to come near a crate line.

### Pistols / 3rd slot

Baseline: PUBG's P92, 35 damage in 9×19mm. Crate line: 125.

| Round | Energy (J) | Starting damage | Versions |
| --- | --- | --- | --- |
| 7.62×51mm | 4,063 | 104 | 1 |
| .500 S&W | 3,434 | 95 | 1 |
| .460 S&W | 2,914 | 88 | 1 |
| .300 Blackout | 2,016 | 73 | 1 |
| 5.56×45mm | 1,622 | 65 | 4 |
| .30 Carbine | 1,325 | 59 | 1 |
| 7.62×25mm Tokarev | 881 | 48 | 1 |
| .400 Corbon | 797 | 46 | 1 |
| .38 Super | 678 | 42 | 1 |
| 7.63×25mm Mauser | 508 | 37 | 11 |
| .45 ACP | 500 | 36 | 8 |
| 9×19mm | 464 | 35 | 20 |
| 7.65×21mm Parabellum | 441 | 34 | 4 |
| 9×18mm Makarov | 287 | 28 | 1 |
| .380 ACP | 271 | 27 | 2 |
| .22 LR | 186 | 22 | 4 |
| .32 ACP | 175 | 21 | 1 |
| .320 Revolver | TBD | TBD | 1 |
| .380 Revolver | TBD | TBD | 1 |
| .455 Webley Auto | TBD | TBD | 1 |
| 8.15×25.2mm Mauser | TBD | TBD | 1 |
| 8mm Gasser (8.11×27mm) | TBD | TBD | 1 |
| 9mm Largo | TBD | TBD | 1 |
| 9mm Steyr | TBD | TBD | 1 |
| 9×21mm | TBD | TBD | 1 |
| 9×25mm Mauser | TBD | TBD | 1 |

### SMGs

Baseline: PUBG's UMP9, 39 damage in 9×19mm. Crate line: 139.

| Round | Energy (J) | Starting damage | Versions |
| --- | --- | --- | --- |
| .30 Carbine | 1,325 | 66 | 1 |
| .351 WSL | 1,330 | 66 | 1 |
| 10mm Auto | 922 | 55 | 3 |
| 7.62×25mm Tokarev | 881 | 54 | 6 |
| .357 SIG | 681 | 47 | 1 |
| .40 S&W | 649 | 46 | 4 |
| .41 AE | 620 | 45 | 1 |
| 4.6×30mm | 542 | 42 | 1 |
| 5.7×28mm | 542 | 42 | 3 |
| 7.63×25mm Mauser | 508 | 41 | 2 |
| .45 ACP | 500 | 40 | 16 |
| 9×19mm | 464 | 39 | 29 |
| 7.65×21mm Parabellum | 441 | 38 | 1 |
| 9mm Browning Long | 407 | 37 | 1 |
| 9×18mm Makarov | 287 | 31 | 2 |
| .380 ACP | 271 | 30 | 2 |
| .22 LR | 186 | 25 | 6 |
| .32 ACP | 175 | 24 | 2 |
| .38 ACP | TBD | TBD | 2 |
| .45 Remington–Thompson | TBD | TBD | 1 |
| 9mm Largo | TBD | TBD | 1 |
| 9×21mm | TBD | TBD | 2 |
| 9×25mm Mauser | TBD | TBD | 1 |

### Assault rifles

Baseline: PUBG's M416, 43 damage in 5.56×45mm. Crate line: 107.

| Round | Energy (J) | Starting damage | Versions |
| --- | --- | --- | --- |
| 7.62×51mm | 4,063 | 68 | 5 |
| .450 Bushmaster | 3,720 | 65 | 1 |
| 6.5×50mm Arisaka | 2,666 | 55 | 1 |
| 6.8mm Remington SPC | 2,187 | 50 | 1 |
| .300 Blackout | 2,016 | 48 | 9 |
| 7.62×39mm | 2,062 | 48 | 20 |
| 5.8×42mm | 1,891 | 46 | 2 |
| 7.92×33mm Kurz | 1,769 | 45 | 2 |
| 5.56×45mm | 1,622 | 43 | 85 |
| .222 Remington | 1,490 | 41 | 1 |
| 5.45×39mm | 1,426 | 40 | 14 |
| .30 Carbine | 1,325 | 39 | 3 |
| 7.62×25mm Tokarev | 881 | 32 | 1 |
| .40 S&W | 649 | 27 | 1 |
| 9×19mm | 464 | 23 | 4 |
| .22 LR | 186 | 15 | 7 |
| 4.85×49mm | TBD | TBD | 1 |
| 5.7mm Johnson | TBD | TBD | 1 |
| 6.5mm Fedorov | TBD | TBD | 1 |
| 9×39mm | TBD | TBD | 4 |

### Battle rifles & DMRs

Baseline: PUBG's SLR, 58 damage in 7.62×51mm. Crate line: 107.

| Round | Energy (J) | Starting damage | Versions |
| --- | --- | --- | --- |
| 9.3×64mm Brenneke | 5,853 | 70 | 1 |
| .30-06 Springfield | 4,309 | 60 | 6 |
| 7.92×57mm Mauser | 4,299 | 60 | 6 |
| 7.62×51mm | 4,063 | 58 | 61 |
| 7.5×55mm Swiss | 3,964 | 57 | 4 |
| 7.62×54mmR | 3,678 | 55 | 12 |
| 6.5mm Creedmoor | 3,380 | 53 | 4 |
| 7.7×58mm Arisaka | 3,403 | 53 | 1 |
| 7×57mm Mauser | 3,188 | 51 | 1 |
| 7.5×54mm French | 3,026 | 50 | 4 |
| .280 British | 2,737 | 48 | 1 |
| 6.8mm Remington SPC | 2,187 | 43 | 1 |
| .300 Blackout | 2,016 | 41 | 1 |
| 7.62×39mm | 2,062 | 41 | 11 |
| 5.8×42mm | 1,891 | 40 | 1 |
| 7.92×33mm Kurz | 1,769 | 38 | 3 |
| 5.56×45mm | 1,622 | 37 | 14 |
| .222 Remington | 1,490 | 35 | 1 |
| .276 Pedersen | TBD | TBD | 1 |
| .366 TKM | TBD | TBD | 2 |
| 6.8×51mm | TBD | TBD | 3 |
| 7.92×41mm CETME | TBD | TBD | 1 |
| 7×49.15mm Optimum 2 | TBD | TBD | 1 |
| 9×39mm | TBD | TBD | 3 |

### LMGs

Baseline: PUBG's M249, 45 damage in 5.56×45mm. Crate line: 107.

| Round | Energy (J) | Starting damage | Versions |
| --- | --- | --- | --- |
| .30-06 Springfield | 4,309 | 73 | 8 |
| 7.92×57mm Mauser | 4,299 | 73 | 6 |
| 7.62×51mm | 4,063 | 71 | 17 |
| 7.62×54mmR | 3,678 | 68 | 6 |
| 6.5mm Creedmoor | 3,380 | 65 | 1 |
| 7.7×58mm Arisaka | 3,403 | 65 | 1 |
| .303 British | 3,255 | 64 | 2 |
| 6.5×55mm Swedish | 3,152 | 63 | 2 |
| 7×57mm Mauser | 3,188 | 63 | 1 |
| .280 British | 2,737 | 58 | 1 |
| 7.62×39mm | 2,062 | 51 | 5 |
| 5.56×45mm | 1,622 | 45 | 9 |
| 5.45×39mm | 1,426 | 42 | 2 |
| 7.65×53mm Mauser | TBD | TBD | 2 |

### Snipers

Baseline: PUBG's M24, 79 damage in 7.62×51mm. Crate line: 100.

| Round | Energy (J) | Starting damage | Versions |
| --- | --- | --- | --- |
| .338 Lapua Magnum | 6,465 | 100 | 2 |
| .300 Winchester Magnum | 5,278 | 90 | 3 |
| .30-06 Springfield | 4,309 | 81 | 6 |
| 7.92×57mm Mauser | 4,299 | 81 | 7 |
| 7.62×51mm | 4,063 | 79 | 12 |
| 7.62×54mmR | 3,678 | 75 | 5 |
| .303 British | 3,255 | 71 | 5 |
| .30-30 Winchester | 2,774 | 65 | 1 |
| .32 Winchester Special | 2,370 | 60 | 1 |
| .38-55 Winchester | 1,580 | 49 | 1 |
| .44 Magnum | 1,354 | 46 | 1 |
| .357 Magnum | 846 | 36 | 1 |
| .45 Colt | 624 | 31 | 1 |
| .22 LR | 186 | 17 | 1 |
| .25-35 Winchester | TBD | TBD | 1 |
| .30-18 Auto | TBD | TBD | 1 |
| .32-40 Winchester | TBD | TBD | 1 |
| 8×50mmR Mannlicher | TBD | TBD | 1 |
| 8×63mm Swedish | TBD | TBD | 1 |

## Sources

- [Wikipedia: Table of handgun and rifle cartridges](https://en.wikipedia.org/wiki/Table_of_handgun_and_rifle_cartridges)
- [Chuck Hawks: Introduction to shotgun gauges and shells](https://chuckhawks.com/intro_gauges.htm)
- [PUBG Wiki: Shotguns](https://pubg.wiki.gg/wiki/Shotguns)
- [LeNutch: PUBG weapon stats, Patch 1.0 #15 (June 2018)](https://docs.google.com/spreadsheets/d/13ZI5GQDbCXl7IlVCVnEA6aZVfC7NFJLBsXPIAGFMNj4/htmlview?sle=true)
