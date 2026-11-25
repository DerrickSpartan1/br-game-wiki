# Class items

A 4th slot holds class items: limited-use gadgets found randomly as loot during a match. There are no player classes.

- **Defibs:** uses limited by batteries or something similar.
- **Bulletproof barricade:** a deployable cover piece, like the one in Rainbow Six Siege ([Shields](#shields)).
- **Rangefinder binoculars:** spot enemies at a distance and read the range for bullet drop. The [spotter scope](#more-class-items) builds on them.
- **Door wedge or door alarm:** lock down a building while you loot it. The wedge stays now that anyone can [nail a door shut](gameplay.md#nailing-doors-shut) (owner, 2026-11-22): it works on metal doors too, where nails only go into wood, and it could be quicker than nailing.
- **Tripwire alarm:** a noise trap that warns you when someone enters your area.
- **Recon drone:** short battery life; scouts one building or compound.
- **Bomb drone:** one-time use. Reviving exists, so being taken out by a bomb drone shouldn't feel like a total game over.
- **Non-lethal grenade launchers:** these go in the class item pool; lethal ones are crate-only.
- **Mortars:** indirect fire, the one lethal launcher in the ground class pool ([Mortars](#mortars)).
- **Rocket launchers (crate-only):** like the RPG-7, in the class slot, found only in crates (owner, 2026-11-22).
- **Ballistic shield:** a handheld shield that spawns in the world ([Shields](#shields)).
- **Flash shield (crate-only):** a ballistic shield with flashbangs on the front, like Blitz's in Rainbow Six Siege. It has 1 to 3 flash charges, isn't indestructible, and breaks quickly. It uses the class slot, like the normal shield (owner, 2026-11-22).
- **Gas mask (owner, 2026-11-22):** not a class item. It has its own slot, and you put it on as soon as you pick it up, but your character never shows it; it's just something you have. It keeps out the gas in [gas red zones](match-flow.md#red-zones), tear gas traps, and tear gas rounds. Its one cost: you can't aim down sights while you're in gas (owner, 2026-11-22). It wears out in gas, losing durability the longer you're in it, and lasts 2 minutes of gas in all (owner, 2026-11-22).
- **Emergency redeploy:** a balloon that lifts you out and drops you elsewhere on the map, like PUBG's Emergency Pickup. Our pick: the small [pickup plane](match-flow.md#aircraft) that snags cash balloons snags this one too, under the same one-plane-at-a-time limit.
- **Deployable zipline:** place a zipline anywhere, like Apex's Pathfinder's zipline gun.
- **Fortifications:** a light version of building: placeable cover like the [barricade](#barricade) and movable shields. Which pieces exist is TBD.
- **Pans:** a pan as a small shield that also hits hard ([Pans](#pans)).
- **Breaching tools:** the sledgehammer, bigger hammers, an entry bar, and a door ram. They break doors and walls until they wear out, and hit hard ([Breaching tools](#breaching-tools)).

- **More class items:** scouting, traps, getting around, support, and breaching ([More class items](#more-class-items)).

**No hero abilities,** but an ability from a hero shooter can become a class item, like the deployable zipline.

## Shields

Shields are for advancing and breaching: crossing open ground, pushing a doorway, holding a stairwell for a teammate. They shouldn't win fights alone, so a heavy LMG breaks one with half its belt. First pass, to tune in play testing.

| | Ballistic shield | Flash shield (crate) | Barricade |
| --- | --- | --- | --- |
| **Gunfire it takes** | 2,900 | 1,450 | 1,800 |
| **Basis** | Half a belt from the hardest-hitting ground LMGs: 50 rounds from an [M60](../weapons/lmgs/m60.md) or [M240B](../weapons/lmgs/fn-mag.md) at 58 | Half the ballistic shield, since it breaks quickly | PUBG's Folded Shield |
| **Explosives** | 9 times their damage | 9 times their damage | 9 times their damage |
| **Setup** | 0.5 s to raise or lower (our pick) | Same | 1.5 s to set down, like PUBG's |

- **Damage counts before armor and hit zones,** after range falloff. The explosive rule is PUBG's ratio: its Folded Shield takes 1,800 gunfire damage but only 200 from grenades.
- **What breaks one:** about 68 rounds from an [M4](../weapons/assault-rifles/m16-m4.md) (43), 50 from an [SR-25](../weapons/battle-rifles/sr-25.md) (58), 37 hits from an [M24](../weapons/snipers/remington-700.md) (79), or 14 full buckshot hits (216), against much less from grenades and launchers. Flanking still beats it, since it only covers the front.

### Ballistic shield

- **Guns:** only the 3rd slot ([Rules](../rules.md#3rd-slot)), fired one-handed around the shield's edge.
- **Cover:** from the front, head to knees while standing and everything while crouched. Sides and back are open.
- **Movement:** no sprinting while it's raised; walking and running at 80% speed (our pick). Lowered, it hangs on your back, covers your back, and you can sprint and use any gun.
- **Breaching:** the melee key bashes, knocking a door open or staggering a player, with no damage (our pick).
- **Sound:** bullets hitting it clang loudly, so everyone nearby knows a shield is pushing.
- **When it breaks,** it's gone for the match; there are no repairs.

### Barricade

PUBG's Folded Shield is the first pass: 1,800 gunfire damage or 200 from explosives, 1.5 s to set down, and it can be folded back up and carried, keeping its damage. PUBG's weighs 30 in the backpack; here it takes the class slot.

## Pans

Pans are class items: small shields you can also fight with. They're the only pans in the game; they're not melee weapons ([Melee](gameplay.md#melee)).

- **Rare:** pans show up in about 1 match in 5. In those matches one kind is rolled, like healing items, and about 20 spawn on the first map, in kitchens and houses, more in the towns (our pick).
- **Raise it to block:** it stops bullets only while held up, which also sets it apart from PUBG's pan. While raised it covers your head and upper chest (our pick). Like the [ballistic shield](#ballistic-shield), the other hand can fire a 3rd-slot gun around it.
- **Ours, not PUBG's:** our own models and sounds ([Legal review](../planning/legal-review.md#pubg-look-and-feel)).
- **The trade-off:** carrying a pan means giving up the class slot, so it blocks more than a quick bullet or two.

### How much a pan takes

Like the shields, a pan takes a set amount of gunfire before it's holed, counted before armor and hit zones and after range falloff, with explosives at 9 times their damage. A holed pan stops blocking, and the hole shows, but it still works as a weapon. First pass (our pick):

| Pan | Gunfire it takes | What holes it | Covers when raised |
| --- | --- | --- | --- |
| Frying pan | 350 | About 8 [M4](../weapons/assault-rifles/m16-m4.md) hits (43), 6 from an [SR-25](../weapons/battle-rifles/sr-25.md) (58), or 2 full buckshot blasts (216) | Head and upper chest |
| Cast-iron skillet | 500 | About 12 M4 hits | Head and upper chest; heavier to carry |
| Wok | 250 | About 6 M4 hits | A wider area, down to the stomach |
| Saucepan | 300 | About 7 M4 hits | The head only |

For scale, the [ballistic shield](#shields) takes 2,900.

### Hitting with it

Class weapons hit harder than owned melee (our pick, from PUBG's pan):

| | Pan | Breaching tools | Owned melee, for comparison |
| --- | --- | --- | --- |
| Chest and stomach | 80 | 80 | 60 |
| Head | 95 (never a one-shot) | 95 | 90 |
| Neck | 67 | 67 | 63 |
| Arms and legs | 48 | 48 | 36 |
| Through tier 1, 2, 3 vests | 56, 48, 36 | 56, 48, 36 | 42, 36, 27 |
| Time between swings | 0.8 s | 1.0 to 1.5 s, by tool ([Breaching tools](#breaching-tools)) | 0.8 s |

Hits to kill to the body: 2 with no vest or through tier 1, and 3 through tier 2 or 3, the same as PUBG's pan.

## Breaching tools

Class items for breaking in, and last-ditch weapons when the chance comes. Bigger hammers and other breaching tools all work like the sledgehammer. Owned melee weapons and the built-in small hammer can't breach ([Melee](gameplay.md#melee), [Built-in tools](gameplay.md#built-in-tools)).

- **What they break:** doors (nailed or not, [Nailing doors shut](gameplay.md#nailing-doors-shut)) and the breakable walls ([Buildings](gameplay.md#buildings-materials)). Not vaults: those still need a key ([Vaults and keys](match-flow.md#vaults-and-keys)).
- **Durability:** each one wears out after a number of breaches, with a wall counting as about 3 doors. Hitting players doesn't wear them down.
- **Hit hard:** all but the door ram hit for 80 to the body, like the pan, with a swing time set by the tool's weight ([Hitting with it](#hitting-with-it)).
- **The roll:** like pans, each match rolls which kinds spawn (our pick: one or two kinds).

First pass (our pick):

| Tool | Breaks | Lasts | Noise | Swing | Notes |
| --- | --- | --- | --- | --- | --- |
| Sledgehammer | Doors and walls | 8 doors or 3 walls | Loud | 1.2 s | The baseline |
| Demolition hammer | Doors and walls, a wall in fewer swings | 6 doors or 4 walls | Very loud | 1.5 s | The biggest hammer; slows you a little while held |
| Club hammer | Doors only | 6 doors | Loud | 1.0 s | A short, heavy hammer; the quickest swing |
| Entry bar | Doors only | 12 doors | Quiet: pries a door open in about 2 s instead of smashing it | 1.0 s | Based on the Halligan bar; the quiet way in |
| Door ram | Doors only, in one hit | 10 doors | Loud | None | Two hands on the ram, so it shoves instead: staggers a player, no damage, like the [shield](#ballistic-shield) bash |

**Ideas:** bolt cutters for padlocked gates and sheds, if locked rooms come in.

## More class items

Approved by the owner on 2026-11-22, with his notes. Each is something real, inspired by an ability in another game. Numbers are TBD.

| Item | Inspired by | What it does |
| --- | --- | --- |
| **Through-wall radar** | Rainbow Six Pulse's heartbeat sensor; police use real ones | A small screen like Pulse's heartbeat sensor that shows people behind a wall within about 15 m. Limited battery, and it beeps |
| **Spotter scope** | PUBG's Spotter Scope | The rangefinder binoculars as a 4x scope that also marks enemies for your squad, with range to 600 m. Limited battery |
| **Sticky camera** | Rainbow Six Valkyrie | Throw a small camera onto a wall and watch it later. One or two out at a time, picked back up after, with a limited battery |
| **Motion sensor** | Call of Duty and Battlefield | Put it on the ground; it pings when someone walks past. Limited battery |
| **Signal jammer** | Rainbow Six Mute | Blocks drones, cameras, radars, and motion sensors nearby, and scrambles nearby enemies' minimap and compass while they're close (owner, 2026-11-22) |
| **Barbed wire roll** | Rainbow Six barbed wire | Slows anyone crossing it, and it rattles |
| **Spike strip** | PUBG's Spike Trap | Pops the tires of anything that drives over it |
| **Leg trap** | Rainbow Six Frost | A hidden trap that holds a player for a few seconds, with a loud snap |
| **Tear gas trap** | Apex Caustic | Lets out gas when someone gets close. It stays in (owner, 2026-11-22); its numbers are TBD |
| **Mines (crate-only)** | Rainbow Six claymore | The claymore, the bouncing betty, and other mines. Extremely powerful, so crate-only |
| **Grapple and rappel kit** | Apex Pathfinder; Rainbow Six rappelling | One item: grapple up to a roof or a window, or anchor it at the top of a building to rappel down or swing in a side window |
| **Emergency parachute** | PUBG's Haven map | Jump from somewhere high safely, but you're easy to spot |
| **Field medic bag** | PUBG's EMT Gear | Faster healing and revives, and you can heal squadmates |
| **Self-revive kit** | PUBG's Self-AED | Pick yourself up once when knocked |
| **Tactical pack** | PUBG's Tactical Pack | Holds one more gun, with its attachments (owner, 2026-11-22). You can't fire it from the pack; swapping it with a gun you're carrying takes a few seconds (our pick) |
| **Ammo bag** | Battlefield's support class | Refills your squad's guns once, whatever the caliber |
| **Vehicle repair kit** | Many games | Fixes a damaged vehicle |
| **Breaching charge** | Rainbow Six breach charge and Thermite | Blows a hole in a breakable wall or door, very loudly |
| **Cutting torch** | Rainbow Six Maverick | Cuts a hole slowly and fairly quietly, metal doors included |
| **Decoy dummy** | Apex Mirage; WWII inflatable decoys | An inflatable dummy wearing your outfit |

## Mortars

Mortars are class items, not special weapons (owner, 2026-11-22).

| Mortar (real basis) | What it's like |
| --- | --- |
| 60 mm light mortar (like PUBG's) | Set the range from the map; fires in a high arc; loud |
| 2-inch mortar (British, WWII) | Lighter, shorter range |
| Knee mortar (Japanese Type 89, 50 mm) | Fired from the ground at a steep angle, out to about 670 m with its shell |
| Spade mortar (Soviet 37 mm, 1939–42) | A shovel that's also a mortar: 1.5 kg, up to 250 m, no sight. A funny one |

- **Shells:** loot of their own, like PUBG's 60 mm shells; a mortar spawns with a few (our pick: 4).
- **Lethal, as an exception:** other lethal launchers stay crate-only, rocket launchers as crate-only class items ([Crate weapons](weapon-pool.md#how-the-randomness-works)).
- **Numbers** (range, blast, set-up time) are TBD.

## Sources

- [Wikipedia: Type 89 grenade discharger](https://en.wikipedia.org/wiki/Type_89_grenade_discharger) · [Wikipedia: 37 mm spade mortar](https://en.wikipedia.org/wiki/37_mm_spade_mortar)
- [Gamertag Mythras: PUBG utility items (Folded Shield)](https://gamertagmythras.com/blog/pubg-battlegrounds/pubg-utility-items-guide)
