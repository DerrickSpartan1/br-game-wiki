# Starting damage and the crate line

How each gun version gets its first-pass damage, how that keeps every gun useful for its job ([Roles by category](ttk.md#roles-by-category)), and when a gun is too much for ground loot. Each version's number is in the Damage column of its gun page's Versions table. Recoil, handling, and play testing still tune them after.

## The method

1. **Pick the table for the round.** Each round class has its own table, whatever category the gun is in, so the same bullet doesn't hit absurdly hard just because it's in an unusual gun. See [Which table a round uses](#which-table-a-round-uses).
2. **Scale by energy:** damage = the table's baseline damage × √(round's energy ÷ baseline round's energy). The square root keeps big rounds strong without making them absurd.
3. **Fit the fire-rate band:** semi-auto and automatic versions keep damage × fire rate inside their category's band, so fast guns hit lighter and slow guns hit harder, as PUBG did ([Fire-rate bands](#fire-rate-bands)).
4. **Pass the role test:** manual-action guns, which the band doesn't cover, must still do their job, like a shotgun one-shotting up close ([Role tests](#role-tests)).
5. **Check the crate line:** a version is crate-only if one head shot kills through a tier 3 helmet, the top tier ([Baselines and crate lines](#baselines-and-crate-lines)), or if it fires too fast to fit its band even after the cut ([Crate check](#crate-check-for-fast-firing-guns)). Crate-only versions are marked `(crate)` and never spawn on the ground; the rest of their family still does. A family that's crate-only as a whole moves to [crate weapons](../weapons/crate/index.md).
6. **Adjust per gun:** a few guns get a hand-set number after review ([Per-gun adjustments](#per-gun-adjustments)).

Energies are typical full-power loads, mostly from Wikipedia's cartridge table. Damage rounds to whole numbers. The method lands close to PUBG on many guns: the AKM 48 (PUBG: 49), the Thompson 40 (Tommy Gun: 40), the Mini-14 45 (Mini 14: 46), the MG3 42 (PUBG today: 42), and the Winchester 1894 in .30-30 65 (Win94: 66).

## Which table a round uses

| Round class | Examples | Table |
| --- | --- | --- |
| Pistol rounds, in the 3rd slot | 9mm, .45 ACP, .500 S&W | Pistol table |
| Pistol rounds, in any other gun | 9mm SMGs, a 9mm AR-15, a .22 LR trainer | SMG table |
| Intermediate rifle rounds (under 2,800 J), outside LMGs and snipers | 5.56mm, 7.62×39mm, 5.45mm, .30 Carbine | Assault rifle table |
| Intermediate rifle rounds, in LMGs | 5.56mm in the M249 | LMG table |
| Full-power rifle rounds (2,800 J or more), outside snipers | 7.62 NATO in battle rifles, ARs, LMGs, and pistols | Battle rifle table |
| Any round in a manual-action sniper | 7.62 NATO in the M24, .45 Colt in a lever rifle | Sniper table |
| Semi-auto or automatic versions of a sniper family | The Pedersen device, the Charlton | Treated as battle rifles & DMRs, with the table for their round |
| Shotgun shells | Buckshot, slugs, crate ammo | [Shotgun tables](#shotguns) |

- **Why:** the old per-category tables stretched one baseline across rounds far from it. A 7.62 NATO pistol came out at 104 and a 5.56 pistol at 65, both stronger than a 5.56 rifle's 43. A .22 LR rifle came out at 15, far weaker than a .22 SMG. Each class now scales from a baseline close to it.
- **LMGs in full-power rounds** use the battle rifle table, not the LMG table: PUBG's DP-28 hit 51, close to the battle rifle table's 55, while the LMG table would give 68.
- **Subsonic 9×39mm** uses PUBG's VSS, 41, since energy undersells its heavy bullet (its 677 J would give 28).
- **.351 WSL** is a rifle round (the Winchester 1907's), so it counts as intermediate.

## Fire-rate bands

PUBG kept each category's damage × fire rate in a band, which is why its Vector hit 34 and its UMP9 39. Semi-auto and automatic versions here do the same.

| Category | Band (damage per minute) | PUBG basis |
| --- | --- | --- |
| Pistols / 3rd slot, semi-auto | 15,000–23,000 | P92: 35 × 450 = 15,750; the top is our pick |
| Pistols / 3rd slot, automatic | 18,000–25,000 | P18C: 23 × 1,000 = 23,000 |
| SMGs | 25,000–37,000 | UMP9 (25,400) to Vector (37,100) |
| Assault rifles | 27,000–37,000 | SCAR-L (26,900) to Groza (36,750) |
| Battle rifles & DMRs | 27,000–37,000 | Mini 14 (27,600) to SKS (35,400); the Mk14 (40,700) was crate-only |
| LMGs | 27,000–40,000 | Our pick, a step above ARs to pay for LMG handling; PUBG's M249 hit 36,000 and its MG3 39,600, both crate-only at the time |

- **Fire rate used:** a range counts as its middle, so the M249's 700–1,150 counts as 925. Semi-only versions count at most 600 (450 for pistols), PUBG's top semi rates and about as fast as anyone clicks, so a semi-only civilian rifle isn't cut for an auto rate it can't use.
- **Limits:** damage moves to the edge of the band, but rises by at most 25% and drops to no less than 60% of its table value. PUBG's deepest cuts were about two thirds: the Micro Uzi does 67% of the UMP9's damage, and the P18C 66% of the P92's.
- **Still under after +25%:** the version gets the lowest recoil in its category, true to life for these small rounds and slow-firing guns, so more of its shots land. That's 28 versions: the .22 LR trainers and conversions, the M3 Grease Gun, the MP 18, the Owen .32 prototype, and the .380 MAC pistol. The .22s are also quiet.
- **Still over at 60%:** a crate candidate ([below](#crate-check-for-fast-firing-guns)).

## Role tests

Manual-action guns aren't limited by fire rate in the same way, so each passes a test for its job instead.

| Guns | Test | Who failed and what changed |
| --- | --- | --- |
| Shotguns (buckshot, any category) | A full hit at point blank kills through a tier 2 vest (167 or more), or the next shot comes within 0.25 s (240 RPM or faster, as PUBG's S12K) | The two .410 pumps (Remington 870 and KSG410): 16 → 19 per pellet (171) |
| Shotguns, the other way | A full hit can't kill through a tier 3 vest (222 or less), since no PUBG ground shotgun one-shot through a level 3 vest | The [Winchester 1887](../weapons/shotguns/winchester-1887.md)'s 10 gauge: 30 → 24 per pellet (216) |
| Snipers: bolt, lever, straight-pull, and single shot | One head shot kills through a tier 1 helmet at 200 m (59 or more), as PUBG's 2018 Win94 did | The Winchester 1894's .25-35, .32-40, .38-55, .357 Magnum, .44 Magnum, and .45 Colt versions and the .22 Mauser KKW go to 59, like PUBG's Win94, which fired .45 ACP but hit 66 |
| 3rd-slot revolvers, single shots, break actions, and two-pulls | One head shot kills an unarmored target (50 or more), since they get few shots before a long reload | The FP-45 Liberator (36 → 50) and the .22 Garrucha (22 → 50) |

Guns raised by a test keep their real handling, bullet speed, and drop, so they still feel different: a .45 Colt lever rifle fires a slow bullet that drops hard at range.

## What the check changed

The table value is the number from steps 1 and 2; the band and tests moved 196 of the 593 versions that have one (the two crate AA-12s are left out below). 32 versions stay TBD: their round's energy or cartridge isn't set yet.

| Category | Unchanged | Raised | Lowered | Examples |
| --- | --- | --- | --- | --- |
| Pistols / 3rd slot | 48 | 7 | 9 | 9mm pistols 35; SA58 pistol 51; C96 machine pistols 26; Škorpion vz. 61 22 |
| Shotguns | 26 | 2 | 0 | 12 gauge pumps 24 × 9; .410 pumps 19 × 9 |
| SMGs | 24 | 37 | 21 | MP5 39; UMP45 40; Uzi 42; MP 40 48; Vector 30; Micro Uzi 30 |
| Assault rifles | 109 | 37 | 15 | M4 and AKM unchanged at 43 and 48; AK-74 42; StG 44 50; FAMAS 37; semi-only civilian 5.56 rifles 45 |
| Battle rifles & DMRs | 108 | 12 | 21 | G3 58; FAL 54; M14 51; FG 42 Type E 41; Mini-14 and Mk 12 45; VSS 41 |
| LMGs | 36 | 5 | 17 | PKM 55; Bren 53; M240 48; MG 34 47; M249 41 (set by hand) |
| Snipers | 44 | 8 | 0 | M24 79; Kar98k 81; Winchester 1894 .30-30 65, handgun calibers 59 |

The five versions of the [MG 42 / MG3](../weapons/crate/mg-42.md) family, all lowered, moved to crate weapons (below). The three .300 Winchester Magnum snipers moved to crates when armor went to three tiers ([Baselines and crate lines](#baselines-and-crate-lines)).

### Crate check for fast-firing guns

Seven versions were still over their band at 60% of their table value. PUBG kept its fastest belt-fed guns out of ground loot: its MG3 is care-package-only, and its M249 was too until 2020, when PUBG cut its damage from 45 to 40 and moved it to the ground. Decided on review:

| Version | Fire rate (RPM) | At 60% | Damage per minute | Band top | Decision |
| --- | --- | --- | --- | --- | --- |
| [MG 42](../weapons/crate/mg-42.md) and its .30-06 version | 900–1,500 | 36 | 43,200 | 40,000 | The whole MG 42 / MG3 family is crate-only, MG3 and MG 74 included, like PUBG's MG3 |
| [MG 34/41](../weapons/lmgs/mg-34.md) | 1,200–1,500 | 36 | 48,600 | 40,000 | Crate-only version; the rest of the MG 34 family stays on the ground |
| [PPSh-41](../weapons/smgs/ppsh-41.md), K-50M, and PPSh-45 | 1,250 | 33 | 41,250 | 37,000 | Ground, cut to 29 (36,250), like PUBG's ground Micro Uzi (26 at 1,250) |
| [Glock 18](../weapons/pistols/glock-17-18.md) | 1,100–1,400 | 21 | 26,250 | 25,000 | Ground, cut to 20 (25,000), like PUBG's ground P18C (23 at 1,000) |

The MG 42 / MG3 family keeps its cut numbers for now; crate guns can earn some back when crates are balanced.

### Per-gun adjustments

Hand-set numbers after review, on top of the band and role tests:

| Gun | Was | Now | Why |
| --- | --- | --- | --- |
| [FN Minimi / M249](../weapons/lmgs/minimi.md), 5.56mm versions | 43 | 41 | PUBG's current M249 number. Through a tier 2 vest it takes 5 chest hits to an M4's 4, a fair trade for the 100-round belt |
| [Janz](../weapons/pistols/janz.md) .460 S&W and .500 S&W | 88 and 95 | 83 | A head shot no longer kills through a tier 2 helmet (99.6), and a tier 2 vest takes 3 body shots: a 3rd-slot gun shouldn't hit like a ground sniper |
| [Winchester 1887](../weapons/shotguns/winchester-1887.md), 10 gauge | 30 × 9 | 24 × 9 | One full hit can't kill through a tier 3 vest (97 instead of 122) |
| [PPSh-41](../weapons/smgs/ppsh-41.md) family | 33 | 29 | Fits the SMG band instead of moving to crates |
| [Glock 18](../weapons/pistols/glock-17-18.md) | 21 | 20 | Fits the 3rd-slot automatic band instead of moving to crates |

## Baselines and crate lines

The crate line: one head shot at starting damage × head multiplier × 0.45 (a tier 3 helmet's 55% cut) reaches 100 health. That's where PUBG drew its line: its ground snipers couldn't one-shot a level 3 helmet, and only the crate AWM could. With armor at PUBG's three tiers ([Armor](armor.md#tiers)), the line is now exactly PUBG's.

| Table | Baseline | Head multiplier | Crate line | Energy that crosses it | Strongest round now | Crosses? |
| --- | --- | --- | --- | --- | --- | --- |
| Pistol | P92 35 (9×19mm, 464 J) | 2× | 111 | About 4,700 J | .500 S&W, 95 (83 after review) | No |
| SMG | UMP9 39 (9×19mm, 464 J) | 1.8× | 124 | About 4,700 J | 10mm Auto, 55 | No |
| Assault rifle | M416 43 (5.56×45mm, 1,622 J) | 2.35× | 95 | About 7,900 J | .276 Pedersen and .280 British, 56 | No |
| Battle rifle | SLR 58 (7.62×51mm, 4,063 J) | 2.35× | 95 | About 10,800 J | 9.3×64mm Brenneke, 70 (61 after the band) | No |
| LMG | M249 45 (5.56×45mm, 1,622 J) | 2.35× | 95 | About 7,200 J | .280 British, 58 | No |
| Sniper | M24 79 (7.62×51mm, 4,063 J) | 2.5× | 89 | About 5,100 J | .338 Lapua Magnum, 100 | Yes: the .338 Lapua and .300 Winchester Magnum versions go to crates (M24A3, AWM .338, M2010, Remington 700 .300, and AWM .300) |

- **Only sniper magnums cross.** The .338 Lapua (100) clears the line easily, and the .300 Winchester Magnum (90) just does: 90 × 2.5 × 0.45 is 101. That matches PUBG, whose crate AWM fired .300 Magnum. The Kar98k and M1903 (81) stop at tier 2 helmets, as PUBG's Kar98k and M24 did.
- **The .50 BMG** would start at 166 as a sniper, far over the line, so .50-caliber rifles are crate weapons.
- **Nothing raised by the band or the tests crosses a line.** The strongest 3rd-slot guns are the .460 and .500 S&W [Janz](../weapons/pistols/janz.md) at 83, trimmed from 88 and 95 so their head shots stop at tier 1 helmets. The [SA58 pistol](../weapons/pistols/sa58-pistol.md) uses the battle rifle table now and lands at 51.

## Shotguns

Shotguns get their own scale, since their damage is split across pellets. The base is PUBG's June 2018 pump and double-barrel shotguns, the S1897 and S686: 9 pellets of 24 damage, 216 in all. Every shell fires 9 pellets, as PUBG's do. Damage cells on gun pages read `24 × 9`: damage per pellet × pellets.

1. **By gauge:** per-pellet damage scales by the square root of the shell's standard shot load: 12 gauge's 1⅛ oz is the base.
2. **By action:** semi-auto and automatic shotguns hit about 8% lighter per pellet, as PUBG's S12K (22 per pellet in 2018) did next to its pumps. Pumps, levers, and break actions hit full.
3. **Short barrels** (14 in or shorter, like sawed-offs, the [Ithaca 37 Stakeout](../weapons/pistols/ithaca-37-stakeout.md), and the 870 breacher) hit about 20% lighter, as PUBG's sawed-off (21 per pellet today, against 26 for its full-length guns) does.
4. **Slugs** are one projectile worth a quarter of a full buckshot hit, about one big DMR shot (PUBG's SKS: 53), with much less falloff ([Damage falloff](ttk.md#damage-falloff)).
5. **The .410 floor:** .410 pumps take 19 per pellet so a full hit still kills through a tier 2 vest ([Role tests](#role-tests)). The full-auto [Saiga-410](../weapons/shotguns/saiga-12.md) keeps 15: its fast follow-up passes the test instead.

| Gauge | Standard shot load | Pump, lever, or break action (per pellet × 9) | Semi or auto (per pellet × 9) | Slug |
| --- | --- | --- | --- | --- |
| 10 gauge | 1¾ oz | 30 × 9 = 270 by load; 24 × 9 = 216 after the tier 3 ceiling | 27 × 9 = 243 by load; 24 × 9 = 216 after the ceiling | 68 |
| 12 gauge | 1⅛ oz | 24 × 9 = 216 | 22 × 9 = 198 | 54 |
| 16 gauge | 1 oz | 23 × 9 = 207 | 21 × 9 = 189 | 52 |
| 20 gauge | ⅞ oz | 21 × 9 = 189 | 19 × 9 = 171 | 47 |
| 28 gauge | ¾ oz | 20 × 9 = 180 | 18 × 9 = 162 | 45 |
| .410 bore | ½ oz | 19 × 9 = 171 (floor; 16 by load) | 15 × 9 = 135 | 36 |

Short-barrel versions take 80% of these. Shotgun head shots use PUBG's 2018 multiplier of 1.5. At that multiplier, a full buckshot hit is never crate-level: the crate line would need 149 damage in one projectile.

### Crate shotgun ammo

Crate shotguns, like the [AA-12](../weapons/crate/aa-12.md), can roll two special ammo types on top of buckshot and slugs. Each is a different job, not a straight upgrade: buckshot stays the best close-range one-shot.

**FRAG-12 (high explosive).** The real round is a 12-gauge shell with a 50 mm metal body, four folding fins, and 3.4 g of high explosive. It arms 3 m from the muzzle, explodes on impact, and reaches 200 m (about 175 m effective). It was made for breaching, light vehicles, and roadside bombs, and sold poorly for its cost. An armor-piercing version can punch through ½ in steel plate.

- **Flight:** one fin-stabilized projectile that flies like a slug, out to about 175 m.
- **Arming:** inside 3 m it doesn't explode; it hits as a plain slug (54). Rushing a FRAG-12 shooter is the counter.
- **Direct hit:** a slug hit (armor applies) plus the blast.
- **Blast:** 50 at the point of impact, falling to 0 at 2 m. Blast damage isn't cut by vests or helmets, like PUBG's grenades.
- **What that does:** a direct hit kills an unarmored target (104). Against a tier 3 vest a direct hit does 74, so two kill, at 300 RPM. A miss by 1 m still does 25.
- **Also:** it breaks doors and light cover and hits vehicles hard (the multiplier is TBD). The blast can hurt the shooter, but the arming distance keeps that rare.

**Dragon's breath (incendiary).** The real round is a 12-gauge shell loaded mostly with magnesium pellets that burn at about 1,650 to 2,200 °C. Its sparks and flames reach about 30 m (some sources claim 91 m), hot enough to set a person or a house on fire. Its combat use is undocumented, and it's banned in several US states.

- **Hit:** 9 burning pellets of 10 (90 at point blank). They fall off faster than buckshot and do nothing past 20 m, though the sparks show out to 30 m.
- **Burning:** any hit sets the target on fire for 10 damage a second over 4 seconds, like PUBG's Molotov burn. Fire isn't cut by armor. New hits restart the 4 seconds instead of stacking.
- **While burning,** you can't ADS, PUBG's Molotov rule.
- **Ground fire:** pellets light grass and bushes for 6 seconds (owner, 2026-11-22), doing 12.5 a second inside, like PUBG's Molotov flames.
- **Tell:** the huge muzzle flame gives the shooter away.
- **What that does:** one close hit on an unarmored target is 90 plus 40 burning, so they die within a second or two. Against a tier 3 vest it's about 40 plus the burn per shot, about three shots against buckshot's two, but the burn keeps hurting through armor and behind cover, and the target can't aim back.

**Weight:** both crate shells weigh 2 per round, against 1.25 for normal shells, so carrying a lot of them costs backpack space ([Ammo](ammo.md#weight)). How many a crate holds is still TBD.

## Starting damage by table

These are the table values from steps 1 and 2, before the fire-rate band and role tests. Each version's final first-pass number is in its gun page's Damage column. "Versions" counts the versions that use that row. TBD rounds don't have an energy yet.

### Pistol table

| Round | Energy (J) | Starting damage | Versions |
| --- | --- | --- | --- |
| .500 S&W | 3,434 | 95 | 1 |
| .460 S&W | 2,914 | 88 | 1 |
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

### SMG table

| Round | Energy (J) | Starting damage | Versions |
| --- | --- | --- | --- |
| 10mm Auto | 922 | 55 | 3 |
| 7.62×25mm Tokarev | 881 | 54 | 7 |
| .357 SIG | 681 | 47 | 1 |
| .40 S&W | 649 | 46 | 5 |
| .41 AE | 620 | 45 | 1 |
| 4.6×30mm | 542 | 42 | 1 |
| 5.7×28mm | 542 | 42 | 3 |
| 7.63×25mm Mauser | 508 | 41 | 2 |
| .45 ACP | 500 | 40 | 16 |
| 9×19mm | 464 | 39 | 33 |
| 7.65×21mm Parabellum | 441 | 38 | 1 |
| .30-18 Auto | 416 | 37 | 1 |
| 9mm Browning Long | 407 | 37 | 1 |
| 9×18mm Makarov | 287 | 31 | 2 |
| .380 ACP | 271 | 30 | 2 |
| .22 LR | 186 | 25 | 13 |
| .32 ACP | 175 | 24 | 2 |
| .38 ACP | TBD | TBD | 2 |
| .45 Remington–Thompson | TBD | TBD | 1 |
| 9mm Largo | TBD | TBD | 1 |
| 9×21mm | TBD | TBD | 2 |
| 9×25mm Mauser | TBD | TBD | 1 |

### Assault rifle table

| Round | Energy (J) | Starting damage | Versions |
| --- | --- | --- | --- |
| .276 Pedersen | 2,790 | 56 | 1 |
| .280 British | 2,737 | 56 | 1 |
| 6.5×50mm Arisaka | 2,666 | 55 | 1 |
| 6.8mm Remington SPC | 2,187 | 50 | 2 |
| 7.62×39mm | 2,062 | 48 | 31 |
| .300 Blackout | 2,016 | 48 | 11 |
| 5.8×42mm | 1,891 | 46 | 3 |
| 7.92×33mm Kurz | 1,769 | 45 | 5 |
| 5.56×45mm | 1,622 | 43 | 103 |
| .222 Remington | 1,490 | 41 | 2 |
| 5.45×39mm | 1,426 | 40 | 14 |
| .351 WSL | 1,330 | 39 | 1 |
| .30 Carbine | 1,325 | 39 | 5 |
| 9×39mm | 677 | 41 (PUBG's VSS) | 7 |
| .366 TKM | TBD | TBD | 2 |
| 4.85×49mm | TBD | TBD | 1 |
| 5.7mm Johnson | TBD | TBD | 1 |
| 6.5mm Fedorov | TBD | TBD | 1 |
| 7.92×41mm CETME | TBD | TBD | 1 |
| 7×49.15mm Optimum 2 | TBD | TBD | 1 |

### LMG table

| Round | Energy (J) | Starting damage | Versions |
| --- | --- | --- | --- |
| .280 British | 2,737 | 58 | 1 |
| 7.62×39mm | 2,062 | 51 | 5 |
| 5.56×45mm | 1,622 | 45 | 9 |
| 5.45×39mm | 1,426 | 42 | 2 |

### Battle rifle table

| Round | Energy (J) | Starting damage | Versions |
| --- | --- | --- | --- |
| 9.3×64mm Brenneke | 5,853 | 70 | 1 |
| .30-06 Springfield | 4,309 | 60 | 14 |
| 7.92×57mm Mauser | 4,299 | 60 | 12 |
| 7.62×51mm | 4,063 | 58 | 84 |
| 7.5×55mm Swiss | 3,964 | 57 | 4 |
| .450 Bushmaster | 3,720 | 55 | 1 |
| 7.62×54mmR | 3,678 | 55 | 18 |
| 6.8×51mm | 3,483 | 54 | 3 |
| 7.65×53mm Mauser | 3,445 | 53 | 2 |
| 7.7×58mm Arisaka | 3,403 | 53 | 2 |
| 6.5mm Creedmoor | 3,380 | 53 | 5 |
| .303 British | 3,255 | 52 | 3 |
| 7×57mm Mauser | 3,188 | 51 | 2 |
| 6.5×55mm Swedish | 3,152 | 51 | 2 |
| 7.5×54mm French | 3,026 | 50 | 4 |

### Sniper table

| Round | Energy (J) | Starting damage | Versions |
| --- | --- | --- | --- |
| .338 Lapua Magnum | 6,465 | 100 | 2 |
| .300 Winchester Magnum | 5,278 | 90 | 3 |
| .30-06 Springfield | 4,309 | 81 | 6 |
| 7.92×57mm Mauser | 4,299 | 81 | 7 |
| 8×63mm Swedish | 4,101 | 79 | 1 |
| 7.62×51mm | 4,063 | 79 | 12 |
| 7.62×54mmR | 3,678 | 75 | 5 |
| .303 British | 3,255 | 71 | 4 |
| 8×50mmR Mannlicher | 3,042 | 68 | 1 |
| .30-30 Winchester | 2,774 | 65 | 1 |
| .32 Winchester Special | 2,370 | 60 | 1 |
| .25-35 Winchester | 1,958 | 55 | 1 |
| .38-55 Winchester | 1,580 | 49 | 1 |
| .44 Magnum | 1,354 | 46 | 1 |
| .32-40 Winchester | 1,030 | 40 | 1 |
| .357 Magnum | 846 | 36 | 1 |
| .45 Colt | 624 | 31 | 1 |
| .22 LR | 186 | 17 | 1 |

## Sources

- [Wikipedia: Table of handgun and rifle cartridges](https://en.wikipedia.org/wiki/Table_of_handgun_and_rifle_cartridges)
- Energies added in this pass: [9×39mm](https://en.wikipedia.org/wiki/9%C3%9739mm) (SP-5), [.25-35 Winchester](https://en.wikipedia.org/wiki/.25-35_Winchester) (117 gr), [.32-40 Ballard](https://en.wikipedia.org/wiki/.32-40_Ballard) (factory 165 gr), [8×50mmR Mannlicher](https://en.wikipedia.org/wiki/8%C3%9750mmR_Mannlicher) (M93), [.277 Fury / 6.8×51mm](https://en.wikipedia.org/wiki/.277_Fury) (113 gr military ball), [.276 Pedersen](https://en.wikipedia.org/wiki/.276_Pedersen), [7.65×53mm Mauser](https://www.wikiwand.com/en/articles/7.65x53mm_Mauser) (spitzer ball), and [.30-18 Auto](https://en.wikipedia.org/wiki/7.65%C3%9720mm_Long) (worked out from its 5.2 g bullet at 400 m/s). The 8×63mm Swedish now uses the table's m/32 load.
- [Chuck Hawks: Introduction to shotgun gauges and shells](https://chuckhawks.com/intro_gauges.htm)
- [PUBG Wiki: Shotguns](https://pubg.wiki.gg/wiki/Shotguns)
- [PUBG Wiki: MG3](https://pubg.wiki.gg/wiki/MG3) · [PUBG Wiki: M249](https://pubg.wiki.gg/wiki/M249) · [PUBG Wiki: Molotov Cocktail](https://pubg.wiki.gg/wiki/Molotov_Cocktail)
- [Sportskeeda: Frag grenades in PUBG](https://www.sportskeeda.com/esports/frag-grenade-how-to-use-them-in-pubg) (armor doesn't reduce grenade damage)
- [LeNutch: PUBG weapon stats, Patch 1.0 #15 (June 2018)](https://docs.google.com/spreadsheets/d/13ZI5GQDbCXl7IlVCVnEA6aZVfC7NFJLBsXPIAGFMNj4/htmlview?sle=true)
- [Wikipedia: FRAG-12](https://en.wikipedia.org/wiki/FRAG-12) · [American Shooting Journal: Frag 12 exploding shotgun shell](https://americanshootingjournal.com/frag-12-exploding-shotgun-shell)
- [Wikipedia: Dragon's breath (ammunition)](https://en.wikipedia.org/wiki/Dragon%27s_breath_(ammunition))
