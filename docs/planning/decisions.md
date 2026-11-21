# Decision log

Every design decision, newest first. The decision itself lives on the page linked; this log is the history.

| Date | Decision | Page |
| --- | --- | --- |
| 2026-11-21 | Keys follow PUBG's defaults, except X is melee: tap it to bring out melee, hold it to stow your weapon and run faster | [Gameplay](../systems/gameplay.md#hud-and-inventory) |
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
