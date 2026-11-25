# Armor and gear

Armor varies by more than tier: each piece trades protection against speed and aim, and helmets can also cost hearing or vision. The pieces are real-world armor, taken from Escape from Tarkov's list, which already did the real-world research.

## Tiers

Vests, helmets, and leg armor all come in the same three tiers, like PUBG's three levels, which keeps balancing simple: guns are balanced around tier 2. Every piece is fit into one of the three, the same way for all three kinds of armor (owner, 2026-11-22). Each tier holds a band of Tarkov's armor classes:

| Tier | Tarkov class | What's in it | Damage reduction (starting point) |
| --- | --- | --- | --- |
| 1 | 1–2 | Soft armor, riot helmets | 30% |
| 2 | 3–4 | Heavier soft armor, light rifle plates, steel pots, and modern ballistic helmets | 40% |
| 3 | 5–6 | Heavy rifle plates and full-face assault helmets | 55% |

- **Damage reduction:** like PUBG: a piece's tier sets how much damage it stops. The numbers are PUBG's 2018 values for levels 1 to 3, as a starting point to tune. There are no loose plates to find or swap.
- **Durability (planner's pick, 2026-11-23):** PUBG's 2018 numbers as a starting point: vests 200, 220, and 250 for tiers 1, 2, and 3; helmets 80, 150, and 230; leg armor 100, 110, and 125, half a vest's (the game reads the leg numbers once leg armor has its own slot; until then they wait, our pick, 2026-11-24). Each hit takes the damage it would have done with no armor off the piece's durability (our pick). A piece stops its full share until it reaches 0, like PUBG's, then it breaks and stops nothing.
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
| 6B45, light | 1 | Chest, stomach | 2 | 1 | Random rig | Soft armor only (owner, 2026-11-22; numbers our pick). The armored rig version carries 16–19 |
| 6B45, medium | 2 | Chest, stomach | 5 | 2 | Random rig | Hard plates front and back, soft side and shoulder armor (numbers our pick) |
| 6B45, heavy | 3 | Chest, stomach, neck, groin | 8 | 4 | Random rig | Two plates front and back, soft neck and groin armor; for assault troops (numbers our pick) |
| BNTI Gzhel-K | 3 | Chest, stomach, neck | 1.5 | 0 | Random rig |  |
| BNTI Zhuk | 2 or 3 | Chest, stomach, neck | 1.5 | 0 | Random rig | Zhuk-3 Press is tier 2, Zhuk-6a tier 3 |
| 6B11 | 1 | Chest, stomach, neck, groin | 0 | 1 | Random rig | The Zabralo family's soft vest (owner, 2026-11-22; numbers our pick) |
| 6B12 | 2 | Chest, stomach, neck, groin | 1 | 1 | Random rig | One front plate, in steel, ceramic, or titanium |
| 6B13 | 3 | Chest, stomach, neck, groin | 2 | 1 | Random rig | The assault vest: ceramic plates front and back (movement our pick) |
| 6B23, plain | 1 | Chest, stomach, neck, groin | 0 | 2.5 | Random rig | Soft armor only, 4 kg (owner, 2026-11-22; movement our pick) |
| 6B23 | 2 | Chest, stomach, neck, groin | 1 | 2.5 | Random rig | Covers both the 6B23-1 (steel chest plate) and 6B23-2 (ceramic) |
| 6B3TM-01 | 2 | Chest, stomach, groin | 5 | 7 | 12 | Titanium plates. The older 6B3T and 6B3TM are left out: they're heavier with the same front plates (owner, 2026-11-22) |
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
- **The real 6B45:** it comes in three setups, light, medium, and heavy, and only the heavy one covers the groin. They're three [fixed vests](#fixed-vests) now (owner, 2026-11-22).

## Helmets

"Back" is the back of the head; a helmet that lists ears muffles hearing. Helmet movement and ADS numbers come from an older Tarkov table, so they're rougher than the vests'; the TBD rows came out after it.

| Helmet | Tier | Covers | Movement (%) | ADS (%) | Notes |
| --- | --- | --- | --- | --- | --- |
| Vulkan-5 (LShZ-5) | 3 | Top, back, ears | 7 | 20 | Visor: blocks some vision and ADS |
| Altyn | 3 | Top, back, ears | 7 | 6 | Visor: blocks some vision and ADS |
| Rys-T | 3 | TBD | TBD | TBD | Visor: blocks some vision and ADS |
| DEVTAC Ronin | 2 | Top, back, ears, face | 5 | 5 | Face cover: blocks some vision and ADS |
| BNTI LShZ-2DTM | 2 | Top, back, ears | 3 | 10 |  |
| Maska-1SCh | 2 | Top, back, ears | 3 | 7 | Steel visor with a slit |
| Maska-1 | 2 | Top, back, ears | 3 | 7 | Clear bulletproof glass visor: the same protection, easier to see through (owner, 2026-11-22) |
| ZSh-1-2M | 2 | Top, back, ears | 3 | 2 |  |
| Highcom Striker ULACH | 2 | Top, back, ears | 2 | 4 |  |
| Highcom Striker ACHHC | 2 | Top, back | 2 | 2 |  |
| MSA TC-2001 / TC-2002 (ACH) | 2 | Top, back | 2 | 2 |  |
| MSA Gallet TC 800 | 2 | Top, back | 2 | 1 |  |
| Team Wendy EXFIL | 2 | Top, back | 1 | 4 |  |
| Diamond Age Bastion | 2 | Top, back | 1 | 2 |  |
| Ops-Core FAST MT | 2 | Top, back | 1 | 0 |  |
| Ops-Core FAST Bump | 1 | Top, back | 0 | 0 | Non-ballistic bump helmet (owner, 2026-11-22; numbers our pick) |
| Team Wendy EXFIL bump (LTP, Carbon) | 1 | Top, back | 0 | 4 | Non-ballistic bump helmets (owner, 2026-11-22; numbers our pick) |
| Crye Precision AirFrame | 2 | Top, back | 0 | 3 |  |
| SSh-68 | 1 | Top, back | 2 | 13 | Soviet steel helmet; stops fragments, not bullets (owner, 2026-11-22) |
| SSh-68M / SSh-68N | 2 | Top, back | 3 | 13 | With an aramid liner that stops pistol rounds; heavier (movement our pick) |
| SSSh-95 Sfera-S | 2 | Top, back, ears | 2 | 3 | Steel |
| STSh-81 Sfera | 2 | Top, back, ears | 1 | 3 | Titanium: the same protection, lighter (owner, 2026-11-22; movement our pick) |
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

## Backpacks

Backpacks work like armor (owner, 2026-11-24): three tiers, like PUBG's three levels, and every pack is a real one from Escape from Tarkov's list, plus a few more we found, sorted into its tier by size. The owner's picks (2026-11-24): the tier sets about how much a pack holds, with a small spread inside it; no slowdown; bird names.

| Tier | Holds, about | Tarkov size | What's in it |
| --- | --- | --- | --- |
| 1 | 150 | Up to 20 slots, or about 20 L | Sling bags, kit bags, and small day packs |
| 2 | 200 | 24 to 32 slots | Assault packs, about 25 to 35 L |
| 3 | 250 | 35 slots and up | Big raid packs and frame rucksacks |

- **Capacity (owner, 2026-11-24):** the tier sets about how much a pack holds, PUBG's 150, 200, and 250, with a small spread inside it: each pack is within 10% of its tier's number, the smallest pack lowest and the biggest highest (spread by size, our pick). So balancing stays simple, the way a vest's tier sets its damage reduction ([Carry weight](#carry-weight)).
- **No slowdown (owner, 2026-11-24):** like PUBG, a pack only changes how much you carry. It doesn't slow running or aiming, whatever its size.
- **Looks:** the model shows the pack you found, so two tier 2 packs in one match can look different.
- **Spawning:** loot rolls a tier first, by area, from its own table ([Loot](loot.md#starting-weights)), then a random pack of that tier. Each vault holds 2 tier 3 packs, so a duo can both leave with one; crates hold none (owner OK'd, 2026-11-24; [Vaults and keys](match-flow.md#vaults-and-keys)).
- **Left out:** Tarkov's fictional and boss bags, such as the Scav backpack, Sanitar's and Partisan's bags, Santa's bag, the LolKek 3F Transfer, and the Transformer bag. Color variants are skins.

| Backpack | Tier | Size | Holds | Notes |
| --- | --- | --- | --- | --- |
| Tactical sling bag | 1 | 6 slots | 135 |  |
| VKBO army bag | 1 | 8 slots | 140 | Russian army kit bag |
| RD-54 | 1 | about 10 L | 145 | Soviet paratroopers' assault pack, worn on the webbing. Not in Tarkov |
| Duffle bag | 1 | 12 slots | 150 |  |
| Veshmeshok (sidor) | 1 | small | 145 | The Soviet soldier's canvas sack, a 19th-century design; small and uncomfortable. Not in Tarkov |
| Mystery Ranch NICE COMM 3 BVS | 1 | 14 slots | 150 | A radio frame |
| Vertx Ready Pack | 1 | 16 slots | 155 |  |
| Flyye MBSS | 1 | 16 slots | 155 |  |
| Czechoslovak M60 backpack | 1 | about 20 L | 165 | Warsaw Pact day pack. Not in Tarkov |
| Hazard 4 Pillbox | 1 | 20 slots | 165 |  |
| LBT-8005A Day Pack | 1 | 20 slots | 165 |  |
| WARTECH Berkut BB-102 | 1 | 20 slots | 165 |  |
| Hazard 4 Takedown sling | 2 | 24 slots | 180 | A long sling pack that can carry a rifle |
| Direct Action Dragon Egg Mk II | 2 | 25 slots | 185 |  |
| Tehinkom RK-PT-25 | 2 | 25 slots | 185 | Russian patrol pack |
| LBT-1476A 3Day Pack | 2 | 25 slots | 185 |  |
| Gruppa 99 T20 | 2 | 25 slots | 185 |  |
| Hazard 4 Drawbridge | 2 | 25 slots | 185 |  |
| Mystery Ranch 2 Day Assault | 2 | 30 slots | 210 |  |
| Mystery Ranch Terraframe | 2 | 30 slots | 210 |  |
| Gruppa 99 T30 | 2 | 30 slots | 210 |  |
| Eberlestock F5 Switchblade | 2 | 30 slots | 210 |  |
| ANA Tactical Beta 2 | 2 | 30 slots | 210 |  |
| CamelBak Tri-Zip | 2 | 30 slots | 210 |  |
| Oakley Mechanism | 2 | 32 slots | 220 |  |
| Mystery Ranch NICE Frame Load Sling | 3 | 35 slots | 225 |  |
| Tasmanian Tiger Trooper 35 | 3 | 35 slots | 225 |  |
| Eberlestock G2 Gunslinger II | 3 | 35 slots | 225 | Carries a rifle in its own sleeve |
| 3V Gear Paratus 3-Day | 3 | 35 slots | 225 |  |
| SSO Attack 2 | 3 | 35 slots | 225 | Russian raid pack |
| Pilgrim tourist backpack | 3 | 35 slots | 225 | A big old civilian hiking pack |
| Mystery Ranch SATL Bridger | 3 | 36 slots | 230 |  |
| Medium ALICE pack | 3 | about 40 L | 235 | US Army, 1970s on, with its frame; 2,412 cubic inches with its pouches. Not in Tarkov |
| Tasmanian Tiger Modular Pack 45 Plus | 3 | 40 slots | 240 |  |
| Eberlestock F4 Terminator | 3 | 40 slots | 240 |  |
| Mystery Ranch Blackjack 50 | 3 | 42 slots | 245 |  |
| 5.11 RUSH100 | 3 | 45 slots | 255 |  |
| LBT-2670 Slim Field Med Pack | 3 | 48 slots | 265 |  |
| 6Sh118 raid backpack | 3 | 48 slots | 265 | The Russian Ratnik kit's raid pack |
| MOLLE II large rucksack | 3 | about 65 L, 80 with its side pouches | 270 | US Army, 2000s. Not in Tarkov |
| Kolobok | 3 | about 80 L | 275 | Soviet rucksack of the Afghan war, huge by Soviet standards. Not in Tarkov |
| Ermak | 3 | large | 270 | Soviet frame rucksack on a light aluminum frame. Not in Tarkov |

Sizes in slots are Tarkov's grid; the rest are the real pack's volume.

## Carry weight

Like PUBG, every item has a weight and your gear sets how much you can carry. PUBG's capacity units and numbers are the first pass.

| Gear | Capacity | Basis |
| --- | --- | --- |
| Backpack, tiers 1, 2, 3 | 135 to 165, 180 to 220, 225 to 275 | PUBG's 150, 200, and 250, with a spread by size ([Backpacks](#backpacks)) |
| Rig, or a carrier's own pouches | 6 per Tarkov slot: 36 to 156, about 96 for an average rig | Decided: a third of a frag grenade per slot |
| No gear | 70 | PUBG's 20 for pockets plus the 50 of the utility belt every PUBG player starts with ([PUBG Wiki: Utility Belt](https://pubg.wiki.gg/wiki/Utility_Belt)) (owner, 2026-11-24, raised from 20 after playtest round 8; the 50 comes from the starting belt below). It holds 60 rounds of 5.56 (30) and a few meds, such as 5 bandages, a first aid kit, and an energy drink (24), as the owner remembers from PUBG |

| Item | Weight | Basis |
| --- | --- | --- |
| Frag grenade | 18 | PUBG |
| Molotov | 16 | PUBG |
| Smoke grenade | 14 | PUBG |
| Stun grenade | 12 | PUBG |
| Other throwables | TBD | [Throwables](weapon-pool.md#throwables) |
| Med kits, adrenaline | 20 each | PUBG ([Healing](healing.md#the-items)) |
| Ammo | Per round, by energy | [Ammo](ammo.md#weight) |

Attachments and the rest (owner OK'd, 2026-11-24; attachment weights are PUBG's from 2017, [Samurai Gamers](https://samurai-gamers.com/playerunknowns-battlegrounds-pubg/attachments-list)):

| Other item | Weight | Basis |
| --- | --- | --- |
| Red dot or holographic sight | 10 | PUBG |
| Scope, 2x to 4x | 15 | PUBG |
| Scope, 6x and up | 20 | PUBG. A variable scope goes by its top power, so a 3–6x is 20 (our pick, 2026-11-24) |
| Thermal scope | 20 | Our pick (2026-11-24): heavier than a 2x–4x for its battery and housing |
| Canted iron sights | 5 | Owner OK'd (2026-11-24) |
| Suppressor | 15 pistol and SMG, 20 rifle, 23 DMR and sniper, 15 shotgun | PUBG's, one item per attachment family (our pick, 2026-11-24; below) |
| Flash hider, compensator, or muzzle brake | 8 pistol and SMG, 10 rifle, 12 DMR and sniper | PUBG's, one item per attachment family (our pick, 2026-11-24) |
| Shotgun choke or duckbill | 5 | PUBG's choke |
| Grip | 10 | PUBG |
| Bipod (as an attachment) | 10 | Our pick (2026-11-24): the same as a grip, since it takes the foregrip slot |
| Stock | 12 | PUBG's tactical stock |
| Cheek pad | 17 | PUBG |
| Bullet loops | 15 | PUBG |
| Mag tier | 10 pistol and SMG, 15 everything else | PUBG's extended and quickdraw mags, rounded; one item per attachment family (our pick, 2026-11-24) |
| Laser or light | 8 | Our pick |
| Shotgun tube extension | 15 | Our pick (2026-11-24): the same as a mag tier for long guns, which it stands in for on tube-fed shotguns |
| Revolver speed loader | 10 | Owner OK'd (2026-11-24): the same as a pistol mag tier, which it stands in for on revolvers |
| Vault key | 1 | Owner OK'd (2026-11-24) |
| Crafting scrap | 0 | Our pick: scrap is a counter, like money, not an item in the bag |
| Armor, helmets, leg armor, class items | — | Our pick: worn in their own slots, never carried in the bag, like PUBG's vests and helmets. Picking up another swaps it and drops the old one |

**Weights go by attachment family (owner, 2026-11-24):** attachments are one item per family ([Universal attachments](attachments.md#universal-attachments)): pistol and SMG, rifle (assault rifles, LMGs, and battle rifles), DMR and sniper, and shotgun. Each item weighs its family's number above, whatever gun it ends up on. Pistols and SMGs share one family, so their mag tier and suppressor are one item each, at 10 and 15.

**A starting belt (owner, 2026-11-24):** "we will have a belt item thats customizable and all players get at the start." Every player starts each match wearing a belt, and it's where the 50 of the no-gear 70 comes from, like PUBG's utility belt. It's customizable; what that covers (its look, or pouch layouts too), and whether it can be taken off or dropped, is still open.

**How capacity adds up (owner, 2026-11-24):** no gear + the vest's or rig's pouches + the pack, added together.

- **Over capacity:** you can't pick anything up until you're under it again. Nothing slows you down.
- **Taking off a vest, rig, or pack** that would leave you over capacity is allowed, the same for all three (owner, 2026-11-24): what no longer fits drops on the ground, ammo first, then whatever else it takes to get under capacity. So when your rig's armor is broken and you just need some armor, you can take it off without sorting your bag first.
- **Rounds coming back to you** (a reload's leftovers, an en bloc clip ejected early) always go in, even over capacity, so nothing lands on the ground in a fight.
- **A carrier with a range of slots** (the LV-119's 24–28, the ANA M1 / M2's 18–20) uses the middle: 26 slots, 156, for the LV-119. That's why the rig row's top is 156, not the biggest chest rig's 150 (owner OK'd, 2026-11-24).

**Why 6 per slot:** a rig stands in for PUBG's vest and utility belt, which added 50 each in 2017, so the average rig (16 slots) should carry about 100. One slot per frag grenade (18) would give the average rig 288 and the biggest 450, more than PUBG's best backpack. At 6, a slot is a third of a grenade, and backpacks stay the main storage.

## Sources

- [United24: Ukraine's full-body protective suit (2025)](https://united24media.com/defense-tech/ukraine-develops-full-body-protective-armor-that-nato-armies-do-not-currently-field-23518) · [US Army: "Kevlar underpants" protect pelvic region (2012)](https://www.army.mil/article/74306/) · [UARM: TAM thigh armor module](https://uarmprotection.com/product/thight-armor-module/) · [UARM: ITAM inner thigh armor module](https://uarmprotection.com/product/inner-thigh-armor-module/) · [Ukrainian Armor: thigh protectors](https://ukrainianarmor.com/en/?p=2504) · [Med-Eng: EOD 10 bomb suit](https://med-eng.com/product/eod-10-suit-helmet)
- Real versions: [Wikipedia: 6B23](https://en.wikipedia.org/wiki/6B23_ballistic_vest) · [Wikipedia: Zabralo vests](https://en.wikipedia.org/wiki/Zabralo_ballistic_vests) · [Wikipedia: 6B3](https://en.wikipedia.org/wiki/6B3_ballistic_vest) · [Wikipedia: SSh-68](https://en.wikipedia.org/wiki/SSh-68) · [Wikipedia: Sfera](https://en.wikipedia.org/wiki/Sfera_(helmet)) · [Equipment Wiki: Maska](https://equipment.fandom.com/wiki/MASKA) · [TNVC: FAST Bump](https://tnvc.com/shop/ops-core-helmet-fast-bump-sf-super-high-cut-helmet-non-ballistic/) · [Soldier Systems: EXFIL Carbon](https://soldiersystems.net/2012/09/17/team-wendy-exfil-carbon-fiber-helmet-in-stock-now-at-gss-gear/)
- [Wikipedia: 6B45 ballistic vest](https://en.wikipedia.org/wiki/6B45_ballistic_vest)
- [Gamepressure: PUBG vests and helmets](https://gamepressure.com/playerunknowns-battlegrounds/vests-and-helmets/zea940) (durability) · [PUBG Wiki: Vests](https://pubg.wiki.gg/wiki/Vests) (full protection until 0)
- [Tarkov Forge: Armor chart](https://tarkovforge.com/armor) (vest classes, coverage, and penalties)
- [Tarkov Forge: Helmet chart](https://tarkovforge.com/helmets) (helmet classes)
- [Escape from Tarkov Wiki: Armor plates](https://escapefromtarkov.fandom.com/wiki/Armor_plates) (plate weights and penalties)
- [Tarkov Forge: Chest rigs](https://tarkovforge.com/rigs) (carry space and rig penalties)
- [Escape from Tarkov Wiki (Bilibili): Headwear](https://wiki.biligame.com/eft/Headwear) (helmet coverage and penalties, older patch)
- [Tarkov Forge: Backpacks](https://tarkovforge.com/backpacks) (slots) · [Equipment Wiki: RD-54](https://equipment.fandom.com/wiki/RD-54_Airborne_Assault_Backpack) · [Equipment Wiki: Veshmeshok](https://equipment.fandom.com/wiki/Veshmeshok) · [Safar Publishing: Soviet backpacks of the Afghan war](https://www.safar-publishing.com/post/top-5-backpacks-used-by-soviet-army-in-soviet-afghan-war) (veshmeshok, RD-54, Kolobok, Ermak) · [AllOutdoor: medium ALICE](https://www.alloutdoor.com/?p=167258) · [AllOutdoor: large ALICE and MOLLE II](https://www.alloutdoor.com/?p=164377) · [Varusteleka: Czechoslovak M60 backpack](https://varusteleka.com/en/product/czechoslovakian-m60-backpack-with-straps-surplus/76751)
- [Samurai Gamers: PUBG equipment list](https://samurai-gamers.com/playerunknowns-battlegrounds-pubg/equipment-list/) (backpack, vest, and belt capacity)
- [PUBG Wiki: Grenades](https://pubg.wiki.gg/wiki/Grenades) (throwable weights)
- [PUBG Wiki: Ammunition](https://pubg.wiki.gg/wiki/Ammunition) (ammo weights)
