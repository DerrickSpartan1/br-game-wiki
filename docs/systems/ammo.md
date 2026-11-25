# Ammo

## How ammo and reloading work

Like PUBG. Ammo is loose rounds of each caliber, carried in the backpack. Reloading pulls rounds from the backpack into the gun's mag, belt, or drum instantly, with no filling one round at a time, and tops off whatever is still in the gun. For example, with 100 rounds of 5.56 in the backpack, emptying a 30-round M4 mag and reloading puts 30 in the gun and leaves 70. With a 100-round belt that has 40 left and 40 more in the backpack, reloading leaves 80 in the gun and none in the backpack.

There are three kinds of exceptions. Each version's reload style is in the Reload column of its gun page ([Gun art and sound](../planning/art-and-sound.md#reload-styles)).

- **[En bloc clips](../rules.md#en-bloc-clips)** can't be topped off, so reloading early ejects the partial clip and its rounds go back to the backpack.
- **Tubes and single-round mags** load one round at a time, like PUBG's shotguns, so a reload adds rounds until the gun is full or the backpack runs out. Single-round mags are fixed mags loaded without clips, like the [M24](../weapons/snipers/remington-700.md)'s.
- **Stripper clips** work like PUBG's Kar98k: from empty, a full clip goes in at once, fast and easy; topping off a partly full gun loads one round at a time.

Pressing fire stops any reload that loads one round at a time (tubes, single-round mags, and stripper-clip guns topping off). The rounds already fully loaded stay in, so you can shoot with only a few loaded; a round partway in goes back to the last saved step ([Staged reloads](handling.md#staged-reloads)). That first click only stops the reload; the next click fires (owner, 2026-11-24; [Staged reloads](handling.md#staged-reloads)).

**The chambered round (owner, 2026-11-23):** a closed-bolt gun with a detachable mag can hold one more than its mag. Reloading from empty fills the mag and charges the gun, so a 30-round mag shows 29+1. Reloading with a round still in the chamber fills the mag and keeps that round, so it shows 30+1, and the reload takes one more round from the backpack. Which guns get it is on [Staged reloads](handling.md#staged-reloads).

## Spawning and special rounds

Ammo spawns with each gun, so only the calibers of the guns in that match appear. With limited guns per match, ammo for them should be plentiful, like original PUBG, where you'd often fill your backpack with 5.56 or 7.62 near where you land.

**Shared ammo:** 7.63mm Mauser ammo also works in 7.62×25mm Tokarev guns, like Germany's captured PPSh-41s. It's one way only: Tokarev ammo doesn't work in 7.63mm guns, since it's the hotter load. That links the PPSh-41, the C96, the M1911 and Thompson Tokarev versions, and a future TT-33, so those calibers are easier to find ammo for. They stay separate rounds, so the randomizer's same-cartridge bonus doesn't count them as a match.

**5.7×28mm:** no armor-penetration trait, since it would be hard to balance. The 5.7 guns (P90, Five-seven, and the others on the add-later list) are balanced through damage instead. The [MP7](../weapons/smgs/mp7.md)'s armor-piercing 4.6×30mm is handled the same way.

**Shotgun ammo:** when a shotgun is rolled, the match also rolls one of its listed gauges and an ammo type for that gauge, such as buckshot or slug. The ammo type mainly changes damage and the shotgun's role, keeping things simple. Special crate shotguns can also roll FRAG-12 high-explosive rounds and dragon's breath ([Crate shotgun ammo](starting-damage.md#crate-shotgun-ammo)). Exception: dual-tube shotguns like the KSG roll two ammo types, one per tube, and switch between them with the select-fire button.

**Cartridge weighting:** once one gun is rolled, the other slots lean slightly toward guns sharing its cartridge. Details on the [weapon pool](weapon-pool.md) page.

How often loose ammo spawns is on [Loot and spawning](loot.md#starting-weights).

## Weight

Ammo weighs per round, in PUBG's capacity units ([Carry weight](armor.md#carry-weight)). PUBG's weights are the first pass. PUBG has one weight per caliber, so each of our rounds takes the PUBG weight of the nearest round by energy (energies are on [Starting damage](starting-damage.md#starting-damage-by-table)).

| Rounds | Weight per round | PUBG basis | Examples |
| --- | --- | --- | --- |
| Under 500 J | 0.375 | 9mm | 9×19mm, .380 ACP, .22 LR |
| 500 to 1,199 J | 0.4 | .45 ACP | .45 ACP, 7.62×25mm Tokarev, .357 Magnum, 9×39mm |
| 1,200 to 1,999 J | 0.5 | 5.56mm | 5.56×45mm, 5.45×39mm, 7.92×33mm Kurz, .30 Carbine |
| 2,000 to 4,999 J | 0.7 | 7.62mm | 7.62×39mm, .300 Blackout, 7.62×51mm, 7.62×54mmR, .460 and .500 S&W |
| 5,000 J and up | 1.0 | .300 Magnum | .300 Winchester Magnum, .338 Lapua Magnum, 9.3×64mm Brenneke |
| Shotgun shells, any gauge | 1.25 | 12 gauge | Buckshot and slugs |
| FRAG-12 and dragon's breath (crate) | 2 | Our pick: PUBG's heaviest round, the crossbow bolt | 10 rounds weigh about as much as a frag grenade (18) |
| Flares | 0.5 | Flare gun | — |
| Grenade launcher rounds | TBD | — | — |

Rounds with no energy yet get their weight when the energy is found. In PUBG, a 12-gauge shell (1.25) already outweighs an AWM round (1.0), so the crate shells go to 2 to stay heavier than normal shells.

Source: [PUBG Wiki: Ammunition](https://pubg.wiki.gg/wiki/Ammunition)

## Calibers in the roster

Every cartridge that at least one roster gun or version fires. Many appear only on one rare version or prototype; each gun page's Versions table says which.

| Caliber | Also called | Type | Guns |
| --- | --- | --- | --- |
| .22 LR | — | Pistol / SMG | [Garrucha](../weapons/pistols/garrucha.md), [Janz revolvers](../weapons/pistols/janz.md), [M1911 / M1911A1](../weapons/pistols/m1911.md), [Thompson](../weapons/smgs/thompson.md), [MP 40](../weapons/smgs/mp40.md), [Owen](../weapons/smgs/owen.md), [Uzi](../weapons/smgs/uzi.md), [MP5](../weapons/smgs/mp5.md), [MP5 pistol](../weapons/pistols/mp5-pistol.md), [KRISS Vector](../weapons/smgs/kriss-vector.md), [StG 44](../weapons/assault-rifles/stg-44.md), [AK-47 / AKM](../weapons/assault-rifles/ak-47-akm.md), [vz. 58](../weapons/assault-rifles/vz-58.md), [Steyr AUG](../weapons/assault-rifles/steyr-aug.md), [SA80 / L85](../weapons/assault-rifles/sa80.md), [SIG SG 550](../weapons/assault-rifles/sg-550.md), [HK416](../weapons/assault-rifles/hk416.md), [HK416 .22 pistol](../weapons/pistols/hk416-22-pistol.md), [Kar98k / Gewehr 98](../weapons/snipers/kar98k.md) |
| .30-18 Auto | 7.65×20mm Longue | Pistol / SMG | [M1903 Springfield](../weapons/snipers/m1903.md) |
| .32 ACP | — | Pistol / SMG | [Thompson](../weapons/smgs/thompson.md), [Owen](../weapons/smgs/owen.md), [Škorpion vz. 61](../weapons/pistols/skorpion-vz61.md) |
| .38 ACP | — | Pistol / SMG | [Thompson](../weapons/smgs/thompson.md), [Owen](../weapons/smgs/owen.md) |
| .38 Super | — | Pistol / SMG | [M1911 / M1911A1](../weapons/pistols/m1911.md) |
| .357 SIG | — | Pistol / SMG | [KRISS Vector](../weapons/smgs/kriss-vector.md) |
| .380 ACP | 9×17mm, 9mm Short | Pistol / SMG | [MAC-10 / MAC-11](../weapons/smgs/mac-10-11.md), [MAC pistol](../weapons/pistols/mac-pistol.md), [Škorpion vz. 61](../weapons/pistols/skorpion-vz61.md), [PP-19 Bizon](../weapons/smgs/pp-19-bizon.md) |
| .40 S&W | — | Pistol / SMG | [Sterling](../weapons/smgs/sterling.md), [MP5](../weapons/smgs/mp5.md), [UMP](../weapons/smgs/ump.md), [KRISS Vector](../weapons/smgs/kriss-vector.md), [Steyr AUG](../weapons/assault-rifles/steyr-aug.md) |
| .400 Corbon | — | Pistol / SMG | [M1911 / M1911A1](../weapons/pistols/m1911.md) |
| .41 AE | — | Pistol / SMG | [Uzi](../weapons/smgs/uzi.md) |
| .45 ACP | — | Pistol / SMG | [FP-45 Liberator](../weapons/pistols/fp-45-liberator.md), [Mauser C96 ("Broomhandle")](../weapons/pistols/c96.md), [M1911 / M1911A1](../weapons/pistols/m1911.md), [Luger (Parabellum, P08)](../weapons/pistols/luger.md), [MP 18 / MP 28 (Bergmann)](../weapons/smgs/mp18.md), [Thompson](../weapons/smgs/thompson.md), [Thompson pistol](../weapons/pistols/thompson-pistol.md), [M3 "Grease Gun"](../weapons/smgs/m3-grease-gun.md), [Owen](../weapons/smgs/owen.md), [Uzi](../weapons/smgs/uzi.md), [MAC-10 / MAC-11](../weapons/smgs/mac-10-11.md), [MAC pistol](../weapons/pistols/mac-pistol.md), [Sterling](../weapons/smgs/sterling.md), [MP5](../weapons/smgs/mp5.md), [UMP](../weapons/smgs/ump.md), [KRISS Vector](../weapons/smgs/kriss-vector.md) |
| .45 Remington–Thompson | — | Pistol / SMG | [Thompson](../weapons/smgs/thompson.md) |
| .455 Webley Auto | — | Pistol / SMG | [M1911 / M1911A1](../weapons/pistols/m1911.md) |
| 4.6×30mm | — | Pistol / SMG | [MP7](../weapons/smgs/mp7.md) |
| 5.7×28mm | — | Pistol / SMG | [P90](../weapons/smgs/p90.md) |
| 7.62×25mm Tokarev | — | Pistol / SMG | [M1911 / M1911A1](../weapons/pistols/m1911.md), [Thompson](../weapons/smgs/thompson.md), [PPSh-41](../weapons/smgs/ppsh-41.md), [Sten](../weapons/smgs/sten.md), [PP-19 Bizon](../weapons/smgs/pp-19-bizon.md), [M1/M2 Carbine](../weapons/assault-rifles/m1-m2-carbine.md) |
| 7.63×25mm Mauser | — | Pistol / SMG | [Mauser C96 ("Broomhandle")](../weapons/pistols/c96.md), [MP 18 / MP 28 (Bergmann)](../weapons/smgs/mp18.md), [Thompson](../weapons/smgs/thompson.md) |
| 7.65×21mm Parabellum | — | Pistol / SMG | [Mauser C96 ("Broomhandle")](../weapons/pistols/c96.md), [M1911 / M1911A1](../weapons/pistols/m1911.md), [Luger (Parabellum, P08)](../weapons/pistols/luger.md), [MP 18 / MP 28 (Bergmann)](../weapons/smgs/mp18.md) |
| 8mm Gasser (8.11×27mm) | — | Pistol / SMG | [Mauser C96 ("Broomhandle")](../weapons/pistols/c96.md) |
| 8.15×25.2mm Mauser | — | Pistol / SMG | [Mauser C96 ("Broomhandle")](../weapons/pistols/c96.md) |
| 9×18mm Makarov | — | Pistol / SMG | [Škorpion vz. 61](../weapons/pistols/skorpion-vz61.md), [PP-19 Bizon](../weapons/smgs/pp-19-bizon.md) |
| 9×19mm | 9mm Parabellum, 9mm Luger, 9mm NATO | Pistol / SMG | [SIG Sauer M17 / M18](../weapons/pistols/m17-m18.md), [Glisenti Model 1910](../weapons/pistols/glisenti-1910.md), [Mauser C96 ("Broomhandle")](../weapons/pistols/c96.md), [M1911 / M1911A1](../weapons/pistols/m1911.md), [Luger (Parabellum, P08)](../weapons/pistols/luger.md), [Glock 17 / Glock 18](../weapons/pistols/glock-17-18.md), [MP 18 / MP 28 (Bergmann)](../weapons/smgs/mp18.md), [Thompson](../weapons/smgs/thompson.md), [MP 40](../weapons/smgs/mp40.md), [MP 40 pistol](../weapons/pistols/mp40-pistol.md), [PPSh-41](../weapons/smgs/ppsh-41.md), [Sten](../weapons/smgs/sten.md), [M3 "Grease Gun"](../weapons/smgs/m3-grease-gun.md), [Owen](../weapons/smgs/owen.md), [Uzi](../weapons/smgs/uzi.md), [Uzi pistol](../weapons/pistols/uzi-pistol.md), [MAC-10 / MAC-11](../weapons/smgs/mac-10-11.md), [MAC pistol](../weapons/pistols/mac-pistol.md), [Sterling](../weapons/smgs/sterling.md), [Sterling Para-pistol](../weapons/pistols/sterling-para-pistol.md), [Škorpion vz. 61](../weapons/pistols/skorpion-vz61.md), [MP5](../weapons/smgs/mp5.md), [MP5 pistol](../weapons/pistols/mp5-pistol.md), [UMP](../weapons/smgs/ump.md), [KRISS Vector](../weapons/smgs/kriss-vector.md), [PP-19 Bizon](../weapons/smgs/pp-19-bizon.md), [M1/M2 Carbine](../weapons/assault-rifles/m1-m2-carbine.md), [vz. 58](../weapons/assault-rifles/vz-58.md), [Steyr AUG](../weapons/assault-rifles/steyr-aug.md), [IWI Tavor (TAR-21)](../weapons/assault-rifles/tavor.md) |
| 9×21mm | 9×21mm IMI | Pistol / SMG | [Glock 17 / Glock 18](../weapons/pistols/glock-17-18.md), [Uzi](../weapons/smgs/uzi.md), [KRISS Vector](../weapons/smgs/kriss-vector.md) |
| 9×25mm Mauser | 9mm Mauser Export | Pistol / SMG | [Mauser C96 ("Broomhandle")](../weapons/pistols/c96.md), [MP 18 / MP 28 (Bergmann)](../weapons/smgs/mp18.md) |
| 9mm Browning Long | — | Pistol / SMG | [MP 18 / MP 28 (Bergmann)](../weapons/smgs/mp18.md) |
| 9mm Largo | — | Pistol / SMG | [Mauser C96 ("Broomhandle")](../weapons/pistols/c96.md), [MP 18 / MP 28 (Bergmann)](../weapons/smgs/mp18.md) |
| 9mm Steyr | — | Pistol / SMG | [M1911 / M1911A1](../weapons/pistols/m1911.md) |
| 10mm Auto | — | Pistol / SMG | [Thompson](../weapons/smgs/thompson.md), [MP5](../weapons/smgs/mp5.md), [KRISS Vector](../weapons/smgs/kriss-vector.md) |
| .45 Colt | — | Revolver | [Winchester Model 1894](../weapons/snipers/winchester-1894.md) |
| .320 Revolver | — | Revolver | [Garrucha](../weapons/pistols/garrucha.md) |
| .357 Magnum | — | Revolver | [Janz revolvers](../weapons/pistols/janz.md), [Winchester Model 1894](../weapons/snipers/winchester-1894.md) |
| .380 Revolver | — | Revolver | [Garrucha](../weapons/pistols/garrucha.md) |
| .44 Magnum | — | Revolver | [Janz revolvers](../weapons/pistols/janz.md), [Winchester Model 1894](../weapons/snipers/winchester-1894.md) |
| .454 Casull | — | Revolver | [Janz revolvers](../weapons/pistols/janz.md) |
| .460 S&W | — | Revolver | [Janz revolvers](../weapons/pistols/janz.md) |
| .500 S&W | — | Revolver | [Janz revolvers](../weapons/pistols/janz.md) |
| 8×50mmR Mannlicher | — | Rifle | [Mosin–Nagant](../weapons/snipers/mosin-nagant.md) |
| 8×63mm Swedish | — | Rifle | [Kar98k / Gewehr 98](../weapons/snipers/kar98k.md) |
| .25-35 Winchester | — | Rifle | [Winchester Model 1894](../weapons/snipers/winchester-1894.md) |
| .30-30 Winchester | .30 WCF | Rifle | [Winchester Model 1894](../weapons/snipers/winchester-1894.md) |
| .32 Winchester Special | — | Rifle | [Winchester Model 1894](../weapons/snipers/winchester-1894.md) |
| .32-40 Winchester | — | Rifle | [Winchester Model 1894](../weapons/snipers/winchester-1894.md) |
| .38-55 Winchester | — | Rifle | [Winchester Model 1894](../weapons/snipers/winchester-1894.md) |
| .222 Remington | — | Rifle | [vz. 58](../weapons/assault-rifles/vz-58.md), [Ruger Mini-14](../weapons/battle-rifles/mini-14.md) |
| .276 Pedersen | — | Rifle | [M1 Garand](../weapons/battle-rifles/m1-garand.md) |
| .280 British | — | Rifle | [FN FAL](../weapons/battle-rifles/fn-fal.md), [Bren / ZB vz. 26](../weapons/lmgs/bren.md) |
| .30 Carbine | — | Rifle | [M3 "Grease Gun"](../weapons/smgs/m3-grease-gun.md), [M1/M2 Carbine](../weapons/assault-rifles/m1-m2-carbine.md), [M1 Carbine Enforcer](../weapons/pistols/m1-carbine-enforcer.md), [Galil (incl. Galil ACE)](../weapons/assault-rifles/galil.md) |
| .30-06 Springfield | — | Rifle | [M1 Garand](../weapons/battle-rifles/m1-garand.md), [SIG SG 510 (Stgw 57)](../weapons/battle-rifles/sg-510.md), [SVD Dragunov](../weapons/battle-rifles/svd.md), [M1918 BAR](../weapons/lmgs/bar.md), [Bren / ZB vz. 26](../weapons/lmgs/bren.md), [MG 34](../weapons/lmgs/mg-34.md), [MG 42 / MG3](../weapons/crate/mg-42.md), [Kar98k / Gewehr 98](../weapons/snipers/kar98k.md), [Mosin–Nagant](../weapons/snipers/mosin-nagant.md), [M1903 Springfield](../weapons/snipers/m1903.md), [Remington 700 / M24](../weapons/snipers/remington-700.md) |
| .300 Blackout | — | Rifle | [M16 / M4](../weapons/assault-rifles/m16-m4.md), [Steyr AUG](../weapons/assault-rifles/steyr-aug.md), [SIG SG 550](../weapons/assault-rifles/sg-550.md), [IWI Tavor (TAR-21)](../weapons/assault-rifles/tavor.md), [FN SCAR-L](../weapons/assault-rifles/scar-l.md), [ACR (Adaptive Combat Rifle)](../weapons/assault-rifles/acr.md), [SIG MCX](../weapons/assault-rifles/sig-mcx.md), [SIG MCX pistol](../weapons/pistols/sig-mcx-pistol.md), [Ruger Mini-14](../weapons/battle-rifles/mini-14.md) |
| .300 Winchester Magnum | 7.62×67mm | Rifle | [Remington 700 / M24](../weapons/snipers/remington-700.md), [Accuracy International AW / AWM](../weapons/snipers/ai-arctic-warfare.md) |
| .303 British | 7.7×56mmR | Rifle | [Bren / ZB vz. 26](../weapons/lmgs/bren.md), [Lee–Enfield](../weapons/snipers/lee-enfield.md) |
| .338 Lapua Magnum | — | Rifle | [Remington 700 / M24](../weapons/snipers/remington-700.md), [Accuracy International AW / AWM](../weapons/snipers/ai-arctic-warfare.md) |
| .351 WSL | — | Rifle | [Thompson](../weapons/smgs/thompson.md) |
| .366 TKM | 9.6×53mm Lancaster | Rifle | [SKS](../weapons/battle-rifles/sks.md), [SVD Dragunov](../weapons/battle-rifles/svd.md) |
| .450 Bushmaster | — | Rifle | [ACR (Adaptive Combat Rifle)](../weapons/assault-rifles/acr.md) |
| 4.85×49mm | — | Rifle | [SA80 / L85](../weapons/assault-rifles/sa80.md) |
| 5.45×39mm | — | Rifle | [Galil (incl. Galil ACE)](../weapons/assault-rifles/galil.md), [AK-74](../weapons/assault-rifles/ak-74.md), [OTs-14 Groza](../weapons/assault-rifles/ots-14-groza.md), [AN-94 "Abakan"](../weapons/assault-rifles/an-94.md), [Beryl wz. 96](../weapons/assault-rifles/beryl.md), [IWI Tavor (TAR-21)](../weapons/assault-rifles/tavor.md), [AK-12](../weapons/assault-rifles/ak-12.md), [RPK](../weapons/lmgs/rpk.md) |
| 5.56×45mm | 5.56 NATO | Rifle | [AK-47 / AKM](../weapons/assault-rifles/ak-47-akm.md), [vz. 58](../weapons/assault-rifles/vz-58.md), [AR-18](../weapons/assault-rifles/ar-18.md), [AR-180SP](../weapons/pistols/ar-180sp.md), [Stoner 63](../weapons/assault-rifles/stoner-63.md), [M16 / M4](../weapons/assault-rifles/m16-m4.md), [HK33](../weapons/assault-rifles/hk33.md), [Galil (incl. Galil ACE)](../weapons/assault-rifles/galil.md), [AK-74](../weapons/assault-rifles/ak-74.md), [Steyr AUG](../weapons/assault-rifles/steyr-aug.md), [FAMAS](../weapons/assault-rifles/famas.md), [SA80 / L85](../weapons/assault-rifles/sa80.md), [SIG SG 550](../weapons/assault-rifles/sg-550.md), [SIG P556](../weapons/pistols/sig-p556.md), [OTs-14 Groza](../weapons/assault-rifles/ots-14-groza.md), [QBZ-95](../weapons/assault-rifles/qbz-95.md), [HK G36](../weapons/assault-rifles/g36.md), [Beryl wz. 96](../weapons/assault-rifles/beryl.md), [IWI Tavor (TAR-21)](../weapons/assault-rifles/tavor.md), [FN SCAR-L](../weapons/assault-rifles/scar-l.md), [FN SCAR 15P](../weapons/pistols/scar-15p.md), [HK416](../weapons/assault-rifles/hk416.md), [ACR (Adaptive Combat Rifle)](../weapons/assault-rifles/acr.md), [SIG MCX](../weapons/assault-rifles/sig-mcx.md), [SIG MCX pistol](../weapons/pistols/sig-mcx-pistol.md), [AK-12](../weapons/assault-rifles/ak-12.md), [Ruger Mini-14](../weapons/battle-rifles/mini-14.md), [QBU-88](../weapons/battle-rifles/qbu-88.md), [Mk 12 SPR](../weapons/battle-rifles/mk-12.md), [FN SCAR-H](../weapons/battle-rifles/scar-h.md), [MG 42 / MG3](../weapons/crate/mg-42.md), [RPK](../weapons/lmgs/rpk.md), [PK / PKM](../weapons/lmgs/pk.md), [FN Minimi / M249](../weapons/lmgs/minimi.md), [IWI Negev](../weapons/lmgs/negev.md) |
| 5.7mm Johnson | .22 Spitfire | Rifle | [M1/M2 Carbine](../weapons/assault-rifles/m1-m2-carbine.md) |
| 5.8×42mm | — | Rifle | [QBZ-95](../weapons/assault-rifles/qbz-95.md), [QBU-88](../weapons/battle-rifles/qbu-88.md) |
| 6.5×50mm Arisaka | — | Rifle | [Fedorov Avtomat](../weapons/assault-rifles/fedorov-avtomat.md) |
| 6.5×55mm Swedish | 6.5mm Swedish Mauser, 6.5×55mm m/94 | Rifle | [M1918 BAR](../weapons/lmgs/bar.md), [FN MAG / M240](../weapons/lmgs/fn-mag.md) |
| 6.5mm Creedmoor | — | Rifle | [AR-10](../weapons/battle-rifles/ar-10.md), [SR-25 / M110](../weapons/battle-rifles/sr-25.md), [FN SCAR-H](../weapons/battle-rifles/scar-h.md), [SIG MCX-SPEAR (M7)](../weapons/battle-rifles/mcx-spear.md), [IWI Negev](../weapons/lmgs/negev.md) |
| 6.5mm Fedorov | — | Rifle | [Fedorov Avtomat](../weapons/assault-rifles/fedorov-avtomat.md) |
| 6.8mm Remington SPC | — | Rifle | [ACR (Adaptive Combat Rifle)](../weapons/assault-rifles/acr.md), [Ruger Mini-14](../weapons/battle-rifles/mini-14.md) |
| 6.8×51mm | .277 SIG Fury (civilian twin) | Rifle | [SIG MCX-SPEAR (M7)](../weapons/battle-rifles/mcx-spear.md) |
| 7×49.15mm Optimum 2 | — | Rifle | [FN FAL](../weapons/battle-rifles/fn-fal.md) |
| 7×57mm Mauser | — | Rifle | [Mondragón rifle](../weapons/battle-rifles/mondragon.md), [Bren / ZB vz. 26](../weapons/lmgs/bren.md) |
| 7.5×54mm French | — | Rifle | [MAS-49](../weapons/battle-rifles/mas-49.md) |
| 7.5×55mm Swiss | — | Rifle | [Mondragón rifle](../weapons/battle-rifles/mondragon.md), [SVT-40](../weapons/battle-rifles/svt-40.md), [SIG SG 510 (Stgw 57)](../weapons/battle-rifles/sg-510.md) |
| 7.62×39mm | — | Rifle | [AK-47 / AKM](../weapons/assault-rifles/ak-47-akm.md), [vz. 58](../weapons/assault-rifles/vz-58.md), [M16 / M4](../weapons/assault-rifles/m16-m4.md), [HK33](../weapons/assault-rifles/hk33.md), [Galil (incl. Galil ACE)](../weapons/assault-rifles/galil.md), [Steyr AUG](../weapons/assault-rifles/steyr-aug.md), [SIG SG 550](../weapons/assault-rifles/sg-550.md), [OTs-14 Groza](../weapons/assault-rifles/ots-14-groza.md), [Beryl wz. 96](../weapons/assault-rifles/beryl.md), [ACR (Adaptive Combat Rifle)](../weapons/assault-rifles/acr.md), [SIG MCX](../weapons/assault-rifles/sig-mcx.md), [AK-12](../weapons/assault-rifles/ak-12.md), [SVT-40](../weapons/battle-rifles/svt-40.md), [SKS](../weapons/battle-rifles/sks.md), [AR-10](../weapons/battle-rifles/ar-10.md), [SIG SG 510 (Stgw 57)](../weapons/battle-rifles/sg-510.md), [M14](../weapons/battle-rifles/m14.md), [HK G3](../weapons/battle-rifles/hk-g3.md), [Ruger Mini-14](../weapons/battle-rifles/mini-14.md), [Bren / ZB vz. 26](../weapons/lmgs/bren.md), [RPD](../weapons/lmgs/rpd.md), [RPK](../weapons/lmgs/rpk.md), [IWI Negev](../weapons/lmgs/negev.md) |
| 7.62×51mm | 7.62 NATO | Rifle | [vz. 58](../weapons/assault-rifles/vz-58.md), [AR-18](../weapons/assault-rifles/ar-18.md), [Stoner 63](../weapons/assault-rifles/stoner-63.md), [Galil (incl. Galil ACE)](../weapons/assault-rifles/galil.md), [M1 Garand](../weapons/battle-rifles/m1-garand.md), [MAS-49](../weapons/battle-rifles/mas-49.md), [FN FAL](../weapons/battle-rifles/fn-fal.md), [DSA SA58 pistol](../weapons/pistols/sa58-pistol.md), [AR-10](../weapons/battle-rifles/ar-10.md), [SIG SG 510 (Stgw 57)](../weapons/battle-rifles/sg-510.md), [CETME](../weapons/battle-rifles/cetme.md), [M14](../weapons/battle-rifles/m14.md), [HK G3](../weapons/battle-rifles/hk-g3.md), [Beretta BM 59](../weapons/battle-rifles/bm-59.md), [SVD Dragunov](../weapons/battle-rifles/svd.md), [Ruger Mini-14](../weapons/battle-rifles/mini-14.md), [SR-25 / M110](../weapons/battle-rifles/sr-25.md), [FN SCAR-H](../weapons/battle-rifles/scar-h.md), [HK417](../weapons/battle-rifles/hk417.md), [IWI Tavor 7](../weapons/battle-rifles/tavor-7.md), [AK-308](../weapons/battle-rifles/ak-308.md), [SIG MCX-SPEAR (M7)](../weapons/battle-rifles/mcx-spear.md), [M1918 BAR](../weapons/lmgs/bar.md), [Bren / ZB vz. 26](../weapons/lmgs/bren.md), [MG 34](../weapons/lmgs/mg-34.md), [MG 42 / MG3](../weapons/crate/mg-42.md), [M60](../weapons/lmgs/m60.md), [FN MAG / M240](../weapons/lmgs/fn-mag.md), [PK / PKM](../weapons/lmgs/pk.md), [FN Minimi / M249](../weapons/lmgs/minimi.md), [IWI Negev](../weapons/lmgs/negev.md), [Kar98k / Gewehr 98](../weapons/snipers/kar98k.md), [Lee–Enfield](../weapons/snipers/lee-enfield.md), [Remington 700 / M24](../weapons/snipers/remington-700.md), [Accuracy International AW / AWM](../weapons/snipers/ai-arctic-warfare.md) |
| 7.62×54mmR | 7.62×53mmR (Finnish) | Rifle | [SVT-40](../weapons/battle-rifles/svt-40.md), [SKS](../weapons/battle-rifles/sks.md), [SVD Dragunov](../weapons/battle-rifles/svd.md), [DP-27](../weapons/lmgs/dp-27.md), [PK / PKM](../weapons/lmgs/pk.md), [Mosin–Nagant](../weapons/snipers/mosin-nagant.md) |
| 7.65×53mm Mauser | 7.65mm Belgian Mauser, 7.65mm Argentine | Rifle | [M1918 BAR](../weapons/lmgs/bar.md), [Bren / ZB vz. 26](../weapons/lmgs/bren.md) |
| 7.7×58mm Arisaka | — | Rifle | [M1 Garand](../weapons/battle-rifles/m1-garand.md), [Bren / ZB vz. 26](../weapons/lmgs/bren.md) |
| 7.92×33mm Kurz | — | Rifle | [StG 44](../weapons/assault-rifles/stg-44.md), [FG 42](../weapons/battle-rifles/fg-42.md), [Gewehr 43](../weapons/battle-rifles/gewehr-43.md), [FN FAL](../weapons/battle-rifles/fn-fal.md) |
| 7.92×41mm CETME | — | Rifle | [CETME](../weapons/battle-rifles/cetme.md) |
| 7.92×57mm Mauser | — | Rifle | [M1 Garand](../weapons/battle-rifles/m1-garand.md), [FG 42](../weapons/battle-rifles/fg-42.md), [Gewehr 43](../weapons/battle-rifles/gewehr-43.md), [M1918 BAR](../weapons/lmgs/bar.md), [Bren / ZB vz. 26](../weapons/lmgs/bren.md), [MG 34](../weapons/lmgs/mg-34.md), [MG 42 / MG3](../weapons/crate/mg-42.md), [Kar98k / Gewehr 98](../weapons/snipers/kar98k.md), [Mosin–Nagant](../weapons/snipers/mosin-nagant.md) |
| 9×39mm | — | Rifle | [AK-74](../weapons/assault-rifles/ak-74.md), [AS Val](../weapons/assault-rifles/as-val.md), [OTs-14 Groza](../weapons/assault-rifles/ots-14-groza.md), [VSS Vintorez](../weapons/battle-rifles/vss.md) |
| 9.3×64mm Brenneke | — | Rifle | [SVD Dragunov](../weapons/battle-rifles/svd.md) |
| 10 gauge | — | Shotgun | [Winchester Model 1887 / 1901](../weapons/shotguns/winchester-1887.md) |
| 12 gauge | — | Shotgun | [AA-12](../weapons/crate/aa-12.md), [Saiga-12](../weapons/shotguns/saiga-12.md), [Franchi SPAS-12](../weapons/shotguns/spas-12.md), [Winchester Model 1887 / 1901](../weapons/shotguns/winchester-1887.md), [KelTec KSG](../weapons/shotguns/ksg.md), [Remington 870](../weapons/shotguns/remington-870.md), [Ithaca 37](../weapons/shotguns/ithaca-37.md), [Ithaca 37 Stakeout](../weapons/pistols/ithaca-37-stakeout.md), [HK G3](../weapons/battle-rifles/hk-g3.md) |
| 16 gauge | — | Shotgun | [Remington 870](../weapons/shotguns/remington-870.md), [Ithaca 37](../weapons/shotguns/ithaca-37.md) |
| 20 gauge | — | Shotgun | [Saiga-12](../weapons/shotguns/saiga-12.md), [Remington 870](../weapons/shotguns/remington-870.md), [Ithaca 37](../weapons/shotguns/ithaca-37.md) |
| 28 gauge | — | Shotgun | [Remington 870](../weapons/shotguns/remington-870.md), [Ithaca 37](../weapons/shotguns/ithaca-37.md) |
| .410 bore | — | Shotgun | [Saiga-12](../weapons/shotguns/saiga-12.md), [KelTec KSG](../weapons/shotguns/ksg.md), [Remington 870](../weapons/shotguns/remington-870.md) |

Not listed: the [UMP pistol](../weapons/pistols/ump-pistol.md) (calibers to confirm) and the [Vector pistol](../weapons/pistols/vector-pistol.md) (follows the KRISS Vector's calibers). Janz revolver frames cover caliber ranges rather than exact lists, so only the end points are listed. Shotgun ammo types (buckshot, slug, and crate-only FRAG-12 and dragon's breath) are rolled on top of the gauge.
