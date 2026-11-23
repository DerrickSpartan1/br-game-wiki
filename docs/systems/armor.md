# Armor and gear

Armor varies by more than tier: each piece trades protection against speed and aim, and helmets can also cost hearing or vision. The pieces are real-world armor, taken from Escape from Tarkov's list, which already did the real-world research.

## Tiers

Vests and helmets both come in three tiers, like PUBG's three levels, which keeps balancing simple: guns are balanced around tier 2. Each tier holds a band of Tarkov's armor classes:

| Tier | Tarkov class | What's in it | Damage reduction (starting point) |
| --- | --- | --- | --- |
| 1 | 1–2 | Soft armor, riot helmets | 30% |
| 2 | 3–4 | Heavier soft armor, light rifle plates, steel pots, and modern ballistic helmets | 40% |
| 3 | 5–6 | Heavy rifle plates and full-face assault helmets | 55% |

- **Damage reduction:** like PUBG: a piece's tier sets how much damage it stops. The numbers are PUBG's 2018 values for levels 1 to 3, as a starting point to tune. There are no loose plates to find or swap.
- **Legs:** leg armor has its own slot (owner, 2026-11-22; [Leg armor](#leg-armor-idea)).
- **Makeshift upgrades:** armor can be upgraded half a tier, like a tier 1 helmet to a makeshift tier 1.5 or a tier 2 vest to a makeshift tier 2.5. Makeshift tiers have lower durability but can take one extra bullet. Upgrades are crafted in-match from scrap.
- Players recover by [healing](healing.md).

## Debuffs

Every piece has its own movement and ADS (aim down sights) slowdown, as a percentage. The starting numbers below are Tarkov's speed and ergonomics penalties, to tune later.

- **Coverage costs speed.** A light plate carrier covers only the chest and barely slows you; a full kit covers the chest, stomach, arms, neck, and groin and slows you down. The neck, groin, and arms are hit zones of their own, so that coverage matters ([Hit zones](ttk.md#hit-zones)).
- **Arm armor slows ADS the most,** so a light vest keeps ADS quick but leaves the arms open.
- **Hearing:** a helmet that covers the ears muffles sound, and the higher its tier, the more it muffles: a tier 2 helmet over the ears muffles less than a tier 3. Helmets that leave the ears open don't muffle anything. How much each tier muffles is TBD.
- **Vision:** a helmet with a visor or face cover blocks some of your view, but never all of it, and you can't ADS while wearing it. Higher tiers block more; the amounts are TBD. That's the tier 3 helmets and the DEVTAC Ronin. Visors can't flip up: there's no separate face hitbox, so a visor stays as it is.

## Vests

A vest spawns as a combo, built in four steps, and stays that combo for the match, like a gun's [version](../rules.md#spawned-version-is-fixed):

1. **Carrier and tier:** a carrier and a tier it can have.
2. **Plates:** a carrier that takes plates gets a random front and back plate of that tier. Fixed vests skip this, since their plates can't change.
3. **Rig:** a carrier with no pouches of its own gets a random chest rig for carrying ammo and gear. Carriers with pouches skip this.
4. **Slowdown:** the carrier's, plus its plates', plus its rig's.

- **Weight slows running, coverage slows aiming.** Movement slowdown comes mostly from weight, so heavy steel plates slow running the most. ADS slowdown comes mostly from coverage, with arm armor costing the most; plates and rigs add only a little. A tier 2 carrier with steel plates and no arm armor aims with only a slight penalty but runs noticeably slower.
- **Example:** a tier 2 US Army OTV (2% movement, 0% ADS) with a 6B33 steel front plate and a 6B13 steel back plate comes to 7% movement and 1.5% ADS before its rig. With a pair of lighter Monoclete polyethylene plates instead, it's 4% and 2%.
- **Looks:** the model shows the carrier and its rig, so two tier 2 vests in one match can look different, and a tier 2 and a tier 3 can look the same.
- **Carry space** comes from the carrier's pouches or its rig. The numbers below are Tarkov's slot counts; each slot holds 6 capacity in the game ([Carry weight](#carry-weight)).
- **No loose plates** to find or swap.
- **Fixed vests** are soft armor and armor built around its own plates. They spawn only at their real tiers, and their numbers already include their armor.

### Plate carriers

Tiers 2–3. The slowdown here is the carrier alone; its plates and rig add to it.

| Carrier | Covers | Movement (%) | ADS (%) | Carry space |
| --- | --- | --- | --- | --- |
| NFM THOR Integrated Carrier | Chest, stomach, arms, neck, groin | 8 | 6 | Random rig |
| FirstSpear Siege-R | Chest, stomach, arms, neck, groin | 6 | 5 | 25 |
| IOTV Gen4, Full Protection kit | Chest, stomach, arms, neck, groin | 7 | 6 | Random rig |
| IOTV Gen4, Assault kit | Chest, stomach, arms, neck | 5 | 5 | Random rig |
| IOTV Gen4, High Mobility kit | Chest, stomach, neck, groin | 2 | 4 | Random rig |
| Osprey Mk4A | Chest, stomach, arms, neck | 3 | 2 | 24 |
| Gladiator-S | Chest, stomach, neck | 3 | 2 | Random rig |
| Bagariy | Chest, stomach | 4 | 2 | 25 |
| US Army OTV | Chest, stomach | 2 | 0 | Random rig |
| Crye Precision AVS | Chest, stomach, groin | 2 | 0 | 23 |
| RBAV-AF | Chest, stomach | 2 | 1 | 19 |
| SP PC V2 | Chest, stomach | 2 | 1 | 20 |
| ANA M1 / M2 | Chest, stomach | 2 | 0 | 18–20 |
| Highcom Trooper TFO | Chest, stomach | 1 | 0 | Random rig |
| Strandhogg | Chest, stomach | 1 | 0 | 17 |
| NFM THOR CRV | Chest, stomach | 0 | 0 | Random rig |
| Ferro Concepts FCPC V5 | Chest | 4 | 1 | 14 |
| SD mod.2 | Chest | 3 | 1 | 14 |
| A18 Skanda | Chest | 1 | 3 | 25 |
| LV-119 | Chest | 1 | 0 | 24–28 |
| Tasmanian Tiger SK | Chest | 1 | 0 | 8 |
| Tasmanian Tiger MKIII | Chest | 1 | 0 | 15 |
| 5.11 TacTec | Chest | 1 | 0 | 18 |
| Hexgrid | Chest | 1 | 1 | Random rig |
| Banshee | Chest | 1 | 1 | 16 |
| MMAC | Chest | 1 | 1 | 14 |
| TV-110 | Chest | 1 | 0 | 23 |
| Crye Precision JPC | Chest | 0.5 | 0.5 | 24 |
| Crye Precision CPC | Chest | 0 | 1 | 18–23 |
| PlateFrame | Chest | 0 | 1 | 10 |
| MBSS | Chest | 0 | 1 | 12 |
| LBT-6094A Slick | Chest | 0 | 0 | Random rig |
| HPC | Chest | 0 | 0 | Random rig |
| TV-115 | Chest | 0 | 0 | 13 |

### Fixed vests

| Vest | Tiers | Covers | Movement (%) | ADS (%) | Carry space | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| 6B43 Zabralo-Sh | 3 | Chest, stomach, arms, neck, groin | 9 | 7 | Random rig |  |
| FORT Redut-T5 | 3 | Chest, stomach, arms, neck, groin | 8 | 5 | Random rig |  |
| FORT Redut-M | 3 | Chest, stomach, neck, groin | 3 | 3 | Random rig |  |
| NPP Klass Korund-VM | 3 | Chest, stomach, neck, groin | 5 | 3 | Random rig |  |
| FORT Defender-2 | 3 | Chest, stomach, neck, groin | 1 | 1 | Random rig | Steel |
| 6B45 | 3 | Chest, stomach, neck | 5 | 3 | Random rig | The armored rig version carries 16–19 |
| BNTI Gzhel-K | 3 | Chest, stomach, neck | 1.5 | 0 | Random rig |  |
| BNTI Zhuk | 2 or 3 | Chest, stomach, neck | 1.5 | 0 | Random rig | Zhuk-3 Press is tier 2, Zhuk-6a tier 3 |
| 6B13 | 2–3 | Chest, stomach, neck, groin | 1 | 1 | Random rig | Tarkov has a basic and a heavier assault version |
| 6B23 | 2 | Chest, stomach, neck, groin | 1 | 2.5 | Random rig | Covers both the 6B23-1 and 6B23-2 |
| 6B3TM-01 | 2 | Chest, stomach, groin | 5 | 7 | 12 | Titanium plates |
| 6B5-15 Uley | 2 | Chest, stomach, neck, groin | 2 | 1 | 10 |  |
| 6B5-16 | 2 | Chest, stomach, neck, groin | 4 | 6 | 10 |  |
| NPP Klass Kirasa-N | 2 | Chest, stomach, neck | 0 | 1 | Random rig |  |
| DRD | 2 | Chest, stomach | 1 | 1 | Random rig |  |
| Kora-Kulon | 2 | Chest, stomach | 1 | 1 | Random rig | Steel |
| 6B2 | 1 | Chest, stomach | 1 | 1 | Random rig |  |
| PACA | 1 | Chest, stomach | 1 | 1 | Random rig |  |
| Module-3M | 1 | Chest, stomach | 1 | 0 | Random rig |  |
| PLATEminus V2 | 1 | Chest | 0 | 0 | 20–23 | The light version gets a random rig |

### Plates

Each plate below is one plate; a carrier gets a front and a back. Plates marked front or back only fill that side. Any plate of the carrier's tier fits it. Movement and ADS are the slowdown each plate adds.

| Plate | Tier | Material | Weight (kg) | Movement (%) | ADS (%) |
| --- | --- | --- | --- | --- | --- |
| PRTCTR Lightweight | 2 | Polyethylene | 0.43 | 1 | 1 |
| Zhuk-3 (front) | 2 | Polyethylene | 2.4 | 2 | 1 |
| AR500 Legacy | 2 | Composite | 3.85 | 2 | 1 |
| 6B12 (front) | 2 | Steel | 4.6 | 3 | 1.5 |
| Monoclete level III PE | 2 | Polyethylene | 1.35 | 1 | 1 |
| SPRTN Elaphros | 2 | Ceramic | 1.6 | 1 | 1.5 |
| NewSphereTech level III | 2 | Aluminum | 2.15 | 1 | 1 |
| Global Armor steel | 2 | Steel | 3.4 | 1.5 | 1 |
| 6B23-2 (back) | 2 | Steel | 3.5 | 1.5 | 0.5 |
| 6B33 (front) | 2 | Steel | 3.7 | 2.5 | 1 |
| 6B13 custom (back) | 2 | Steel | 4.1 | 2.5 | 0.5 |
| SPRTN Omega | 2 | Composite | 4.39 | 1.5 | 0.5 |
| GAC 3s15m | 3 | Polyethylene | 0.97 | 1 | 1 |
| SAPI level III+ | 3 | Ceramic | 1.82 | 1 | 1.5 |
| Korund-VM (back) | 3 | Steel | 2.3 | 1 | 1 |
| KITECO SC-IV SA | 3 | Polyethylene | 2.45 | 1.5 | 1.5 |
| GAC 4sss2 | 3 | Polyethylene | 2.7 | 1.5 | 1.5 |
| Korund-VM-K (back) | 3 | Ceramic | 2.7 | 1.5 | 1 |
| Granit Br4 | 3 | Ceramic | 2.9 | 1.5 | 1 |
| Granit 4 (front) | 3 | Ceramic | 3.05 | 2 | 1 |
| ESAPI level IV | 3 | Ceramic | 3.2 | 1.5 | 1.5 |
| Granit 4 (back) | 3 | Ceramic | 3.3 | 1 | 1 |
| Granit Br5 | 3 | Ceramic | 3.3 | 2 | 1.5 |
| Korund-VM (front) | 3 | Steel | 3.4 | 2 | 1 |
| Granit 4RS (front) | 3 | Ceramic | 3.5 | 2.5 | 1.5 |
| TallCom Guardian | 3 | Composite | 3.5 | 2 | 1.5 |
| NESCO 4400-SA-MC | 3 | Composite | 3.6 | 2.5 | 1 |
| Granit 4RS (back) | 3 | Ceramic | 3.8 | 2 | 1 |
| Korund-VM-K (front) | 3 | Ceramic | 4 | 3 | 2 |

Left out for now: side plates, and Tarkov's fictional Kiba Arms and Cult plates.

### Chest rigs

The random rigs for carriers without pouches. Color variants are skins.

| Rig | Carry space | Movement (%) | ADS (%) |
| --- | --- | --- | --- |
| Poyas combo | 25 | 1 | 2 |
| MPPV | 24 | 0 | 0 |
| Ten-Speed SF | 24 | 0 | 1 |
| BlackRock | 20 | 1 | 1 |
| Alpha | 20 | 0 | 0 |
| MK3 TV-104 | 20 | 0 | 0 |
| Zhuk chest rig | 20 | 2 | 2 |
| LBCR | 18 | 0 | 0 |
| CR MK2 | 18 | 0 | 0 |
| D3CRX | 18 | 0 | 1 |
| Commando | 16 | 0 | 0 |
| Triton | 16 | 0 | 1 |
| Thunderbolt | 16 | 0 | 0 |
| BSS-MK1 | 16 | 0 | 0 |
| Umka | 16 | 1 | 2 |
| Tarzan | 14 | 1 | 2 |
| 6Sh112 | 12 | 0 | 0 |
| Khamelion | 12 | 0 | 0 |
| TV-106 + TV-109 | 10 | 0 | 0 |
| CSA | 10 | 0 | 0 |
| Type 56 Chicom | 10 | 0 | 1 |
| Micro Rig | 8 | 0 | 0 |
| Bank Robber | 8 | 0 | 0 |
| M4 RSCR | 6 | 0 | 0 |

### Leg armor (idea)

The owner's idea (2026-11-22): armor for the hips, groin, and thighs, worn with a vest. The owner calls it pants armor.

- **Owner's framing:** some vests on the lists above already cover the groin, like the IOTV Gen4 kits and the 6B23. Leg armor covers the thighs or the skirt area below the vest, and works as pants armor. The owner wants more variety than one or two pieces.

- **Real examples:** in 2025 Ukraine bought its first full-body fragmentation suits, about 2 kg, with "pteruges": a skirt-like belt of seven soft ballistic sections over the pelvis and upper thighs, made for drone and artillery fragments. The US Army's Pelvic Protection System (2011) paired Kevlar underwear covering the groin and inner thighs with a stiffer outer layer as strong as the soft parts of its vest. Medieval armor had tassets, plates hanging from the waist over the thighs.
- **More kinds found (2026-11-22), for the owner to pick from:** groin protectors that hang from the vest, like Russia's 6B45 flap; ballistic underwear; pelvic outer garments, armored shorts over the pants; ballistic skirts; inner thigh modules and full thigh modules that strap to a vest, like UARM's ITAM and TAM; femoral plates, soft or hard; fragmentation trousers, as in Ukraine's full-body suit; riot leg guards against melee and thrown things; arterial stab protection, prison-guard gear that stops knives at the inner thighs; bomb suit trousers, very heavy; and historic tassets, cuisses, and samurai thigh guards.
- **Its own slot (owner, 2026-11-22):** leg armor is found as its own loot and worn in its own slot, like a helmet or vest, with a small slowdown like every other piece.
- **No doubling up (owner, 2026-11-22):** two pieces that cover the same spot can't be worn together, like a vest with a groin flap and a battle skirt.
- **Tiers 1 to 3,** like vests: soft panels at tiers 1 and 2, which stop fragments, buckshot, and pistol rounds, and hard thigh plates at tier 3. The numbers are TBD.
- **Kinds (owner, 2026-11-22):** in are the ballistic skirt, groin flaps, inner thigh modules, thigh modules, femoral plates, fragmentation trousers, arterial stab protection, bomb suit trousers (crate-only or a rare, funny find), and historic tassets (a rare or event find). Out are ballistic underwear, pelvic outer garments, and riot leg guards. The garments are hardly armor, but they might make good clothing skins ([Skins](skins.md#wardrobe)).
- **Groin flaps that take a plate:** the hard plate comes separately, found as its own loot (owner, 2026-11-22). That's unlike vests, whose plates come with them.
- **The real 6B45 (to check, owner):** it comes in three setups. Light has no hard plates (NIJ II). Medium adds Granit plates front and back, with soft side and shoulder armor (NIJ III). Heavy, for assault troops, carries two plates front and back plus soft neck and groin protection (NIJ IV). Our [6B45](#fixed-vests) is one tier 3 vest without groin cover; whether it rolls its real setups is open.

## Helmets

"Back" is the back of the head; a helmet that lists ears muffles hearing. Helmet movement and ADS numbers come from an older Tarkov table, so they're rougher than the vests'; the TBD rows came out after it.

| Helmet | Tier | Covers | Movement (%) | ADS (%) | Notes |
| --- | --- | --- | --- | --- | --- |
| Vulkan-5 (LShZ-5) | 3 | Top, back, ears | 7 | 20 | Visor: blocks some vision and ADS |
| Altyn | 3 | Top, back, ears | 7 | 6 | Visor: blocks some vision and ADS |
| Rys-T | 3 | TBD | TBD | TBD | Visor: blocks some vision and ADS |
| DEVTAC Ronin | 2 | Top, back, ears, face | 5 | 5 | Face cover: blocks some vision and ADS |
| BNTI LShZ-2DTM | 2 | Top, back, ears | 3 | 10 |  |
| Maska-1SCh | 2 | Top, back, ears | 3 | 7 |  |
| ZSh-1-2M | 2 | Top, back, ears | 3 | 2 |  |
| Highcom Striker ULACH | 2 | Top, back, ears | 2 | 4 |  |
| Highcom Striker ACHHC | 2 | Top, back | 2 | 2 |  |
| MSA TC-2001 / TC-2002 (ACH) | 2 | Top, back | 2 | 2 |  |
| MSA Gallet TC 800 | 2 | Top, back | 2 | 1 |  |
| Team Wendy EXFIL | 2 | Top, back | 1 | 4 |  |
| Diamond Age Bastion | 2 | Top, back | 1 | 2 |  |
| Ops-Core FAST MT | 2 | Top, back | 1 | 0 |  |
| Crye Precision AirFrame | 2 | Top, back | 0 | 3 |  |
| SSh-68 | 2 | Top, back | 2 | 13 | Soviet steel helmet |
| SSSh-95 Sfera-S | 2 | Top, back, ears | 2 | 3 |  |
| Kiver-M | 2 | Top, back, ears | 3 | 1 |  |
| 6B47 Ratnik-BSh | 2 | Top, back, ears | 1 | 2 |  |
| LShZ | 2 | Top, back | 1 | 1 |  |
| NFM HJELM | 2 | TBD | TBD | TBD |  |
| Galvion Caiman | 2 | TBD | TBD | TBD |  |
| PSh-97 Djeta | 1 | Top, back, ears | 0 | 14 | Riot helmet |
| ShPM Firefighter | 1 | Top, back, ears | 0 | 10 | Firefighter's helmet |
| Kolpak-1S | 1 | Top | 2 | 5 | Riot helmet |
| TSh-4M-L | 1 | Top, back, ears | 0 | 0 | Soft tank crew helmet |

Left out: Tarkov's fictional and joke pieces, like the UNTAR gear, boss editions, the pumpkin helmet, the Tac-Kek replica, and the IDEA and Scav rigs. Color variants are skins.

## Carry weight

Like PUBG, every item has a weight and your gear sets how much you can carry. PUBG's capacity units and numbers are the first pass.

| Gear | Capacity | Basis |
| --- | --- | --- |
| Backpack, levels 1, 2, 3 | 150, 200, 250 | PUBG's backpacks |
| Rig, or a carrier's own pouches | 6 per Tarkov slot: 36 to 150, about 96 for an average rig | Decided: a third of a frag grenade per slot |
| No gear | TBD | — |

| Item | Weight | Basis |
| --- | --- | --- |
| Frag grenade | 18 | PUBG |
| Molotov | 16 | PUBG |
| Smoke grenade | 14 | PUBG |
| Stun grenade | 12 | PUBG |
| Other throwables | TBD | [Throwables](weapon-pool.md#throwables) |
| Med kits, adrenaline | 20 each | PUBG ([Healing](healing.md#the-items)) |
| Ammo | Per round, by energy | [Ammo](ammo.md#weight) |

**Why 6 per slot:** a rig stands in for PUBG's vest and utility belt, which added 50 each in 2017, so the average rig (16 slots) should carry about 100. One slot per frag grenade (18) would give the average rig 288 and the biggest 450, more than PUBG's best backpack. At 6, a slot is a third of a grenade, and backpacks stay the main storage.

## Sources

- [United24: Ukraine's full-body protective suit (2025)](https://united24media.com/defense-tech/ukraine-develops-full-body-protective-armor-that-nato-armies-do-not-currently-field-23518) · [US Army: "Kevlar underpants" protect pelvic region (2012)](https://www.army.mil/article/74306/) · [UARM: TAM thigh armor module](https://uarmprotection.com/product/thight-armor-module/) · [UARM: ITAM inner thigh armor module](https://uarmprotection.com/product/inner-thigh-armor-module/) · [Ukrainian Armor: thigh protectors](https://ukrainianarmor.com/en/?p=2504) · [Med-Eng: EOD 10 bomb suit](https://med-eng.com/product/eod-10-suit-helmet)
- [Wikipedia: 6B45 ballistic vest](https://en.wikipedia.org/wiki/6B45_ballistic_vest)
- [Tarkov Forge: Armor chart](https://tarkovforge.com/armor) (vest classes, coverage, and penalties)
- [Tarkov Forge: Helmet chart](https://tarkovforge.com/helmets) (helmet classes)
- [Escape from Tarkov Wiki: Armor plates](https://escapefromtarkov.fandom.com/wiki/Armor_plates) (plate weights and penalties)
- [Tarkov Forge: Chest rigs](https://tarkovforge.com/rigs) (carry space and rig penalties)
- [Escape from Tarkov Wiki (Bilibili): Headwear](https://wiki.biligame.com/eft/Headwear) (helmet coverage and penalties, older patch)
- [Samurai Gamers: PUBG equipment list](https://samurai-gamers.com/playerunknowns-battlegrounds-pubg/equipment-list/) (backpack, vest, and belt capacity)
- [PUBG Wiki: Grenades](https://pubg.wiki.gg/wiki/Grenades) (throwable weights)
- [PUBG Wiki: Ammunition](https://pubg.wiki.gg/wiki/Ammunition) (ammo weights)
