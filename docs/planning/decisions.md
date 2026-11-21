# Decision log

Every design decision, newest first. The decision itself lives on the page linked; this log is the history.

| Date | Decision | Page |
| --- | --- | --- |
| 2026-11-21 | Vault keys: one key fits all, it's removed from your inventory when used, it drops on death, and care packages have a very small chance of one on top of the 2 or 3 ground keys. A vault drill is saved for later | [Vaults and keys](../systems/match-flow.md#vaults-and-keys) |
| 2026-11-21 | The first map's spots are approved, plus a new coastal town (Marina) on the southeast bay and farm huts with dirt tracks across the open ground | [Maps](../systems/maps.md#marina-farms-and-vaults) |
| 2026-11-21 | Vaults: 4 to 6 per map, one under the Military Outpost, one in each big town, and one on the coast; only 2 or 3 keys spawn per match, at random | [Vaults and keys](../systems/match-flow.md#vaults-and-keys) |
| 2026-11-21 | The first map's heights are squashed to 40% and Monte Epomeo's top becomes a plateau about 2 km across, so the middle stays playable | [Maps](../systems/maps.md#heights-squashed-with-a-plateau) |
| 2026-11-21 | The first map is 10 × 8 km, with Ischia kept at true scale and ocean added around the edges | [Maps](../systems/maps.md#the-first-map-ischia) |
| 2026-11-21 | The first map's layout comes from Ischia (Italy): its coastline, hills, ring road, and town spots, reskinned in the game's own style. The other shortlisted islands are kept for future maps | [Maps](../systems/maps.md#the-first-map-ischia) |
| 2026-11-21 | Carry space is 6 capacity per Tarkov slot, a third of a frag grenade, so an average rig carries about what PUBG's vest and belt did | [Carry weight](../systems/armor.md#carry-weight) |
| 2026-11-21 | Six hit zones: head, neck, chest and stomach, groin, arms, and legs. No lucky one-shots: one health pool, no armor gaps, no random penetration, and the neck at 0.7 of a head hit so no ground automatic gun kills with one neck hit | [TTK](../systems/ttk.md#hit-zones) |
| 2026-11-21 | The first map takes its layout (terrain, roads, and town spots) from a real island of about Erangel's size, then gets reskinned; the island is still open | [Maps](../systems/maps.md#the-first-map-ischia) |
| 2026-11-21 | The first map is Erangel's size, with terrain based on a real island (which one is still open) and towns in the game's own Soviet-era style | [Maps](../systems/maps.md) |
| 2026-11-21 | Matches run like PUBG's: a random plane path, PUBG-style parachutes, PUBG's Erangel zone phases, and random care packages. Zone damage grows the farther outside the zone you are and the later the phase, so zone camping doesn't pay | [Match flow](../systems/match-flow.md) |
| 2026-11-21 | Zone events: PUBG's red zone plus a smoke zone and a poison zone, one at a time at random | [Match flow](../systems/match-flow.md#zone-events) |
| 2026-11-21 | Locked vaults opened with rare keys, like Apex's World's Edge vaults | [Match flow](../systems/match-flow.md#vaults-and-keys) |
| 2026-11-21 | Time passes during a match (day, late day into night, all night, or night into morning), weather can change mid-match, and every player has an always-visible watch on the left wrist | [Match flow](../systems/match-flow.md#time-of-day-and-weather) |
| 2026-11-21 | Shields are for advancing and breaching and mustn't be overpowered: a ballistic shield breaks after half a belt from a heavy LMG (2,900 damage), and the barricade starts from PUBG's Folded Shield | [Class items](../systems/class-items.md#shields) |
| 2026-11-21 | Carry weight uses PUBG's capacity units and weights as the first pass; FRAG-12 and dragon's breath are heavier than normal shells (2 per round) | [Armor and gear](../systems/armor.md#carry-weight), [Ammo](../systems/ammo.md#weight) |
| 2026-11-21 | The AI helpers work as a team: Claude chat is the planner (design and this wiki), Claude Code on the owner's PC is the lead, and the lead hands work to subagent workers (modeler, materials, animator, coder, sound, reviewer). The owner reaches the lead from his phone through Remote Control | [AI team](ai-team.md) |
| 2026-11-21 | Armor has three tiers, like PUBG, at PUBG's 30%, 40%, and 55%: tier 1 holds Tarkov classes 1–2, tier 2 classes 3–4, and tier 3 classes 5–6. Guns are balanced around tier 2, and crates hold tier 3 | [Armor](../systems/armor.md#tiers) |
| 2026-11-21 | The crate line is one head shot through a tier 3 helmet, PUBG's exact line, so the .300 Winchester Magnum snipers (M2010, Remington 700 .300, AWM .300) are crate-only like PUBG's AWM; the shotgun ceiling is a tier 3 vest, so the Winchester 1887 10 gauge is 24 per pellet | [Starting damage](../systems/starting-damage.md#baselines-and-crate-lines) |
| 2026-11-21 | The whole MG 42 / MG3 family is crate-only and moves to crate weapons, and the MG 34/41 is a crate-only version, as PUBG keeps its MG3 in care packages; the PPSh-41 family (29) and Glock 18 (20) stay on the ground with deeper damage cuts | [Starting damage](../systems/starting-damage.md#crate-check-for-fast-firing-guns) |
| 2026-11-21 | Hand-set damage: the M249's 5.56mm versions 41 (PUBG's current number), the Janz .460 and .500 S&W 83, and the Winchester 1887 10 gauge 27 per pellet, since no ground shotgun's full hit should kill through a tier 4 vest | [Starting damage](../systems/starting-damage.md#per-gun-adjustments) |
| 2026-11-21 | Underbarrel and rifle grenade launchers are ground loot with smoke and other non-lethal rounds (star parachute, star cluster, infrared star, propaganda leaflets); frag, HEDP, anti-tank, buckshot, and thermobaric launcher rounds are crate-only | [Attachments](../systems/attachments.md#grenade-launchers) |
| 2026-11-21 | The AN-94 is a ground spawn, very rare since only about 2,000–2,500 were made | [AN-94](../weapons/assault-rifles/an-94.md) |
| 2026-11-21 | Every category has a job and a range where it wins (shotguns 0–15 m, SMGs 0–50 m, ARs 25–250 m, battle rifles & DMRs 100–400 m, LMGs on a bipod, snipers 200 m and beyond, pistols as backups), kept there by damage falloff per category from PUBG's curves and by handling (numbers TBD) | [TTK](../systems/ttk.md#roles-by-category) |
| 2026-11-21 | Starting damage uses the table for the round's class (pistol rounds use the pistol or SMG table, intermediate rifle rounds the assault rifle or LMG table, full-power rounds the battle rifle table, manual snipers the sniper table); 9×39mm uses PUBG's VSS (41) | [Starting damage](../systems/starting-damage.md#which-table-a-round-uses) |
| 2026-11-21 | Semi-auto and automatic versions keep damage × fire rate in a PUBG-based band per category, moving up to 25% up or 40% down; versions still under get the lowest recoil in their category, and versions still over are crate candidates | [Starting damage](../systems/starting-damage.md#fire-rate-bands) |
| 2026-11-21 | Manual-action guns pass a role test: a full buckshot hit kills through a tier 2 vest or the next shot comes within 0.25 s (.410 pumps go to 19 per pellet); manual snipers one-shot a tier 1 helmet at 200 m (59 or more); 3rd-slot revolvers, single shots, and break actions one-shot an unarmored head (50 or more) | [Starting damage](../systems/starting-damage.md#role-tests) |
| 2026-11-21 | FRAG-12: one fin-stabilized slug that arms at 3 m, with a 50-damage blast out to 2 m that ignores armor; dragon's breath: 9 burning pellets of 10 out to 20 m that set targets on fire (10 a second for 4 seconds, through armor) and stop them aiming down sights | [Starting damage](../systems/starting-damage.md#crate-shotgun-ammo) |
| 2026-11-21 | Aimed rates from sources aren't fire-rate caps: the C96 and Luger play at 450 like other semi-auto pistols, and semi-auto shotguns use 240 in any category (the G12) | [TTK](../systems/ttk.md#fire-rates) |
| 2026-11-21 | Keys follow PUBG's defaults, except X is melee: tap it to bring out melee, hold it to stow your weapon and run faster | [Gameplay](../systems/gameplay.md#hud-and-inventory) |
| 2026-11-20 | Fire rates follow PUBG: automatics use the real cyclic rate, and semi-autos and manual actions get PUBG's fixed fastest rates (450 semi pistols, 600 semi rifles, 240 semi shotguns, 32 bolt actions, 100 levers, 80 pumps, 300 between barrels); first-pass numbers fill every unknown rate | [TTK](../systems/ttk.md#fire-rates) |
| 2026-11-20 | Shotgun damage starts from PUBG's 2018 pumps: 9 pellets of 24 for 12 gauge buckshot, scaled by gauge, about 8% lighter for semi and auto shotguns, 20% lighter for short barrels, and slugs worth a quarter of a full hit | [Starting damage](../systems/starting-damage.md#shotguns) |
| 2026-11-20 | Crate weapons by damage: each category has a PUBG baseline gun, starting damage scales by the square root of the round's energy, and a version is crate-only if one head shot kills through a tier 4 helmet; only the .338 Lapua snipers cross so far, while .300 Winchester Magnum stays on the ground | [Starting damage](../systems/starting-damage.md) |
| 2026-11-20 | Every crate holds one crate weapon, its ammo, attachments that fit it, one tier 4 vest, one tier 4 helmet, and one class item | [Loot and spawning](../systems/loot.md#changes-from-pubg) |
| 2026-11-20 | Crates hold anti-vehicle and heavy snipers (a head shot kills through any helmet, like PUBG's AWM), rocket launchers like the RPG (moved from special), lethal grenade launchers, and a flash shield with 1 to 3 charges that breaks quickly | [Weapon pool](../systems/weapon-pool.md#how-the-randomness-works) |
| 2026-11-20 | Normal ballistic shields spawn in the world and go in the class slot | [Class items](../systems/class-items.md) |
| 2026-11-20 | Heavy and anti-materiel sniper rifles, like .50-caliber ones, are crate-only; lever guns like the Winchester 1894 stay in snipers | [Weapon pool](../systems/weapon-pool.md#how-the-randomness-works) |
| 2026-11-20 | Full-auto and semi-auto conversions of bolt-action rifles, like the Charlton and the Pedersen device, stay as rare versions; guns without a detachable mag load the way the real one did | [Ammo](../systems/ammo.md#how-ammo-and-reloading-work) |
| 2026-11-20 | Bolt-action guns whose fixed mag loads without clips (like the M24) load one round at a time, like tubes, and pressing fire stops the reload | [Ammo](../systems/ammo.md#how-ammo-and-reloading-work) |
| 2026-11-20 | Damage is set per gun version, not per caliber, balanced the way PUBG appears to: start from a PUBG anchor, keep damage times fire rate in a band per class, adjust for trade-offs, and check breakpoints | [TTK](../systems/ttk.md#how-damage-is-set) |
| 2026-11-20 | Like PUBG, every gun has its own bullet speed from the real muzzle velocity, and bullets slow and drop over distance | [TTK](../systems/ttk.md#bullet-speed) |
| 2026-11-20 | Bipods deploy on cover or when prone, with their own deploy button | [Attachments](../systems/attachments.md#bipods) |
| 2026-11-20 | Loot spawning starts from PUBG's system (fixed spots, a master table rolled fresh each match, better areas, crates for the best gear), with changes: only the match's pool spawns, four area loot levels, no empty building clusters, less clutter, and logging to tune from; every spawn follows the same category, item, then version or tier steps, and all numbers tune in playtests | [Loot and spawning](../systems/loot.md) |
| 2026-11-20 | Any plate of a carrier's tier fits it | [Armor and gear](../systems/armor.md#plates) |
| 2026-11-20 | Vests roll in steps: a carrier and tier, then a random compatible plate for that tier (unless its plates are fixed), then a random chest rig (unless it has its own pouches); slowdown adds up from all three, with weight driving movement and coverage driving ADS | [Armor and gear](../systems/armor.md#vests) |
| 2026-11-20 | A vest spawns as a fixed combo of vest and armor tier: plate carriers can roll tier 2, 3, or 4, the model always matches the vest, and the tier's armor adds weight and slowdown; soft armor and armor with its own plates keep their real tiers | [Armor and gear](../systems/armor.md#vests) |
| 2026-11-20 | Armored rigs carry more than plain vests | [Armor and gear](../systems/armor.md#vests) |
| 2026-11-20 | Armor damage reduction starts at 30%, 40%, 50%, and 60% for tiers 1 to 4, to tune later | [Armor and gear](../systems/armor.md#tiers) |
| 2026-11-20 | Visors can't flip up; there's no face hitbox, so a visor stays as it is | [Armor and gear](../systems/armor.md#debuffs) |
| 2026-11-20 | Helmets that cover the ears muffle hearing, more at higher tiers; helmets with a visor or face cover block some vision (never all, amount to balance) and prevent ADS | [Armor and gear](../systems/armor.md#debuffs) |
| 2026-11-20 | Slot 4 holds class items and slot 5 throwables; melee gets its own button instead of a slot | [Gameplay](../systems/gameplay.md#hud-and-inventory) |
| 2026-11-20 | The HUD and inventory follow PUBG's 2017–2018 layout with the game's own look, items are picked up by looking and pressing F, and the inventory shows each gun's rolled version | [Gameplay](../systems/gameplay.md#hud-and-inventory) |
| 2026-11-20 | Armor and helmets come in four tiers, filled with Escape from Tarkov's real-world pieces (57 vests and 26 helmets so far); each piece has its own movement and ADS slowdown, starting from Tarkov's penalties | [Armor and gear](../systems/armor.md) |
| 2026-11-20 | A pistol with an add-on stock stays in the pistol / 3rd slot | [Rules](../rules.md#3rd-slot) |
| 2026-11-20 | Parts a version comes with stay on for the match and fill their slot: a built-in bipod means no foregrip, and a version with a stock (like the Mini Uzi) can't remove or swap it | [Attachments](../systems/attachments.md#built-in-parts) |
| 2026-11-20 | PUBG's attachment set joins the game: compensator, flash hider, and choke; vertical, angled, half, thumb, and light grips and a laser sight; red dot, holographic, 2x, 3x, 4x, 3–6x, 8x, 15x (snipers only), canted, and crate-only thermal sights; tactical stock, cheek pad, add-on stocks, and ammo loops | [Attachments](../systems/attachments.md#attachment-slots) |
| 2026-11-20 | Bipods are built in on guns whose real standard version came with one, like most LMGs; any other gun that can take one, like a sniper rifle, uses a bipod as a foregrip attachment | [Attachments](../systems/attachments.md#bipods) |
| 2026-11-20 | Every version lists the rounds it spawns with in a Mag column (tubes add the chambered round, like `5+1`); only versions that reload with a mag, pan, or belt take mag attachments | [Gun page template](gun-page-template.md#reading-pages-as-data) |
| 2026-11-20 | Stripper-clip guns reload like PUBG's Kar98k: a full clip from empty, fast and easy, or one round at a time to top off a partly full gun | [Ammo](../systems/ammo.md#how-ammo-and-reloading-work) |
| 2026-11-20 | Pressing fire stops any reload that loads one round at a time (tubes, and stripper-clip guns topping off); the rounds already loaded stay in | [Ammo](../systems/ammo.md#how-ammo-and-reloading-work) |
| 2026-11-20 | Tubes load one shell at a time, like PUBG: a reload adds shells until the tube is full or the backpack runs out | [Ammo](../systems/ammo.md#how-ammo-and-reloading-work) |
| 2026-11-20 | Every version gets a reload style in a new Reload column on its Versions table, which picks its animation set | [Gun page template](gun-page-template.md#reading-pages-as-data) |
| 2026-11-20 | Sound travels at its real speed, and bullets still faster than sound crack as they fly past | [Gameplay](../systems/gameplay.md#sound) |
| 2026-11-20 | Art and sound use free tools first, with some room for paid tools if a step stalls | [Gun art and sound](art-and-sound.md#who-does-what) |
| 2026-11-20 | Gun art and sound aim for "good enough to get the feel down" for now (real size and shape, working parts, plain materials, sounds that tell guns and distances apart); polished art comes later | [Gun art and sound](art-and-sound.md) |
| 2026-11-20 | Gun tuning waits until the guns have real models, since recoil is too hard to judge on gray-box placeholders; the target is the gun feel of PUBG in 2017–2018 | [First steps](first-steps.md) |
| 2026-11-20 | Ammo and reloading work like PUBG: loose rounds of each caliber in the backpack, and a reload instantly refills the mag, belt, or drum from the backpack, topping off what's left (a 100-round belt with 40 left plus 40 in the backpack reloads to 80); en bloc clips stay the one exception | [Ammo](../systems/ammo.md#how-ammo-and-reloading-work) |
| 2026-11-20 | The M1918A2 BAR's slow and fast auto and the MG 34's two-part trigger (semi and auto) both go on the fire-mode selector key | [Rules](../rules.md#fixed-triggers) |
| 2026-11-20 | Engine: Unreal Engine 5.8 as a C++ project, moving to Unreal Engine 6 later; Unity and Godot were compared and passed over | [Getting started](getting-started.md#other-engines) |
| 2026-10-22 | Real conversion kits count as versions: a kit-converted gun can spawn as its own version or merge into the matching factory version, but never swaps mid-match | [Rules](../rules.md#spawned-version-is-fixed) |
| 2026-10-15 | En bloc clips ping when they fly out, loud enough for nearby players to hear, and can't be topped off: reloading early ejects the partial clip and its rounds go back to inventory | [Rules](../rules.md#en-bloc-clips) |
| 2026-10-15 | The Mondragón's gas cut-off goes on the selector key: semi-auto or straight-pull manual | [Rules](../rules.md#fixed-triggers) |
| 2026-10-15 | Battle rifles and DMRs are one category (example map max 3, the old 1 + 2) | [Weapon pool](../systems/weapon-pool.md) |
| 2026-10-15 | The CETME stays its own gun, apart from the G3 family | [Queue](queue.md) |
| 2026-10-15 | The AK-12 is its own family, not sharing mastery or cosmetics with the AK-74 | [Rules](../rules.md#versions) |
| 2026-10-15 | Battle rifles are the next category; the possible assault rifle additions wait | [Queue](queue.md) |
| 2026-10-14 | Versions keep their real fire modes: semi-auto-only versions stay in the pool for every gun, including the ACR's four semi-auto calibers | [Rules](../rules.md#versions) |
| 2026-10-14 | The HK416 is its own family, not sharing mastery or cosmetics with the M16 / M4 | [Rules](../rules.md#versions) |
| 2026-10-12 | The wiki moves to GitHub (this repo) | [Home](../index.md) |
| 2026-10-12 | Recoil is random with no learnable spray patterns, but each gun has its own recoil personality (climb, drift, settle) | [Rules](../rules.md#random-recoil) |
| 2026-10-12 | No overheating: sustained fire never costs accuracy | [Rules](../rules.md#no-overheating) |
| 2026-10-12 | AN-94 crate-only vs. rare world spawn left open | [AN-94](../weapons/assault-rifles/an-94.md) |
| 2026-10-11 | No jamming: real reliability problems are flavor text only; the L85A1 stays a normal version | [Rules](../rules.md#no-jamming) |
| 2026-10-11 | The Steyr AUG's progressive trigger plays as a normal semi/auto switch on the selector key | [Rules](../rules.md#fixed-triggers) |
| 2026-10-11 | The balanced-recoil AK-107 and AK-108 fold into the AK-74 family and the AK-109 into the AK-47 family, as rare versions | [AK-74](../weapons/assault-rifles/ak-74.md) |
| 2026-10-11 | Wire fences and wire cutters kept as a possibility | [Gameplay](../systems/gameplay.md#buildings-materials) |
| 2026-10-10 | The Galil ACE stays in the Galil family and shares its mastery and cosmetics | [Galil](../weapons/assault-rifles/galil.md) |

## Before 2026-10-10

These were decided earlier in the ideas doc; their exact dates weren't logged.

| Decision | Page |
| --- | --- |
| Spawned version is fixed: no mid-match conversion kits | [Rules](../rules.md#spawned-version-is-fixed) |
| Fixed triggers for guns with swappable trigger packs | [Rules](../rules.md#fixed-triggers) |
| Open-bolt guns have a slight trigger delay | [Rules](../rules.md#open-bolt-delay) |
| Any gun carried in a pistol holster goes in the 3rd slot | [Rules](../rules.md#3rd-slot) |
| One roster entry per gun family; versions merged and weighted by how many were made | [Weapon pool](../systems/weapon-pool.md) |
| 7.63mm Mauser ammo works in 7.62×25mm Tokarev guns, one way only | [Ammo](../systems/ammo.md) |
| 5.7×28mm gets no armor-penetration trait, and the MP7's 4.6×30mm is balanced the same way, through damage | [Ammo](../systems/ammo.md), [MP7](../weapons/smgs/mp7.md) |
| Four magazine tiers, shared within attachment families | [Attachments](../systems/attachments.md) |
| First person everywhere except parachuting | [Gameplay](../systems/gameplay.md) |
| Early access launch at $30 | [Home](../index.md) |
