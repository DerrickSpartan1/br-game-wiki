# Gameplay and mechanics

Matches favor scavenging and a slower pace over fast action, in a classic battle royale format.

- **Camera:** the game is played in first person, including driving. Parachuting is the only third-person part.
- **Hit zones:** six zones: head, neck, chest and stomach (one zone), groin, arms, and legs, with no lucky one-shots ([Hit zones](ttk.md#hit-zones)).
- **Handling:** spread, ready and ADS times, reloads, and movement speed per category are on [Handling](handling.md).
- **Healing:** PUBG's healing items and boost bar, with six slots filled by Escape from Tarkov's meds, drinks, and stimulants, each a little better or worse than PUBG's numbers, and one item per slot each match ([Healing](healing.md)).

## HUD and inventory

The layout follows PUBG's from 2017 and 2018, with the game's own look (no PUBG art, icons, or fonts). The mockup is a private Design artifact in the owner's Claude account.

- **Weapon slots:** 1 and 2 hold primaries, 3 is the pistol / 3rd slot ([Rules](../rules.md#3rd-slot)), 4 holds a [class item](class-items.md), and 5 holds a throwable. Melee has its own button instead of a slot.
- **HUD:** a compass at the top with the heading in yellow; players alive and kills at the top right; the crosshair; health, boost, stance, gear durability, ammo, and fire mode at the bottom center; the five slots as weapon silhouettes beside the minimap at the bottom right.
- **Picking up:** look at an item and press F, like PUBG. The prompt names a gun's rolled version, since every gun is one version for the match ([Rules](../rules.md#versions)).
- **Keys:** PUBG's defaults: WASD to move, Shift sprint, Ctrl walk, C crouch, Z prone, Space jump and vault, = auto-run, Alt free look, V perspective, F interact, Tab inventory, left mouse fire, right mouse aim (tap to toggle, hold to hold), R reload, B fire mode, Q and E peek, middle mouse to ping, and 1 to 5 for the slots. The one change is X, which is melee: tap X for a quick melee attack, and hold X to stow your guns and pull out the melee weapon so you run faster ([Melee](#melee)).
- **Ping:** middle mouse marks enemies, loot, and places for your squad, and means different things depending on what you aim at, like Apex's.
- **Inventory (Tab):** vicinity, backpack, gear (helmet, vest, backpack, and outfit slots for skins), and the weapons with their attachment slots. Hovering a gun shows its version: cartridge, fire modes, rate, and mag. You can still move with it open.

## Knockdowns & revives

1. At zero health you're knocked down. You can crawl, but you leave a blood trail.
2. A teammate can pick you up while you're knocked. This is slow without an adrenaline syringe.
3. If you bleed out, you can still be revived with a defib, or slowly with CPR.

**Bodies hold the loot:** a dead player's body stays where it fell and holds everything they carried. Anyone can loot it straight from the body while the player can still be revived. If the player leaves the match, the body turns into a loot crate, like PUBG's.

**Self-revive kits** let you get up on your own, like PUBG's. They spawn more often in solos and less often in duos, trios, and quads.

**No knockdown shields.**

**Adrenaline** items are rare and have two uses: PUBG's full boost ([Healing](healing.md#boost-bar)) and a quick teammate pickup. They replace the infinite-stamina idea, since original PUBG had no stamina. You don't need one in your hands to use it.

## Comeback fight

When your whole team is wiped out, you're sent to a loser fight as a comeback play. It's a random team fight where players get random weapons, and the format varies:

- A 4v4
- Two 2v2s played side by side
- A 3v3 and a 1v1 played side by side
- Other mixes

Winners redeploy into the main match with the guns and armor they had in the team fight.

**Not final:** the owner wants some kind of Gulag-style comeback, like Warzone's, but isn't sure of the form yet.

**Breakout (rare event):** in duos, trios, and quads only, a rare event brings every eliminated player back into the match at once, like Warzone's Jailbreak.

## Vehicles and water

Lots of vehicles of our own, picked for what each map needs, with our own names and designs when they're added. PUBG's lineup below is a reference and an idea list for later, not a list to copy. Ziplines are part of the map too. Trains could run on maps with rail, and a gondola could carry players up a mountain on a future map.

| PUBG vehicle | What it is | Seats | Top speed (PUBG) |
| --- | --- | --- | --- |
| **Dacia 1300** | Small sedan | 4 | 139 km/h |
| **UAZ** | Military jeep, open or closed top | 5 | 105 km/h open, 115 km/h closed |
| **Buggy** | Dune buggy | 2 | 100 km/h |
| **Motorcycle** | Road motorcycle | 2 | 152 km/h |
| **Motorcycle with sidecar** | Motorcycle and sidecar | 3 | 130 km/h |
| **Dirt Bike** | Off-road motorcycle | — | — |
| **Scooter** | Scooter | 2 | — |
| **Tukshai** | Three-wheeled taxi | 3 | — |
| **Mirado** | Muscle car | 4 | 152 km/h |
| **Pickup** | Pickup truck | 4 | — |
| **Rony** | Pickup truck | 4 | 110 km/h |
| **Van** | Van | 6 | 110 km/h |
| **Coupe RB** | Sports coupe | — | — |
| **Pony Coupe** | Coupe | — | — |
| **Porter** | Small cab-over truck | — | — |
| **Blanc** | SUV | — | — |
| **Pico Bus** | Minibus | — | — |
| **Quad** | Four-wheeler | — | — |
| **Mountain Bike** | Bicycle | — | — |
| **Zima** | Snow version of the UAZ | — | — |
| **Snowmobile** | Snowmobile | 2 | — |
| **Pillar Security Car** | Security patrol car | — | — |
| **Food Truck** | Food truck | — | — |
| **BRDM-2** | Armored car that swims, called in with a flare gun ([Care packages](match-flow.md#care-packages)) | — | — |
| **Boat (PG-117)** | Motor boat | 5 | 90 km/h |
| **Aquarail** | Jet ski | 2 | 90 km/h |
| **Inflatable Boat** | Inflatable boat | — | — |
| **Airboat** | Airboat | — | — |
| **Motor Glider** | Two-seat powered glider | 2 | — |

Dashes are numbers the sources checked don't give. Which vehicles each map gets is TBD; snow vehicles fit snow maps, for example.


- **Fuel and tires:** like PUBG, vehicles run out of fuel and need refilling, and their tires can be shot out.
- **Swimming:** players can swim and dive underwater to break line of sight, like PUBG.

## Melee

- **Key:** tap X for a quick melee attack. Hold X to stow your guns and pull out your melee weapon, which lets you run faster.
- **Your own melee:** every player brings their own melee weapon into every match, so landings start as knife fights, not fist fights. Players pick it like an outfit and unlock new ones through seasons, challenges, and mastery ([Skins and mastery](skins.md#melee-weapons)), so they can be katana people, scythe people, or knife people. Melee is rarely used in PUBG; owning one gives players something of their own.
- **All the same in a fight:** every owned melee weapon has the same damage, reach, swing speed, and run speed. They differ only in look, sound, and animations, including the inspect, so owning one never gives an edge. First pass (our pick, from PUBG's machete, sickle, and crowbar):

    | | Number | Basis |
    | --- | --- | --- |
    | Damage to the chest and stomach | 60 | PUBG's machete, sickle, and crowbar (its pan does 80) |
    | Head | 90 (×1.5) | Our pick: two head hits, never one, so no lucky one-shots ([Hit zones](ttk.md#hit-zones)) |
    | Neck | 63 (0.7 × the head) | Our hit zone rule |
    | Arms and legs | 36 (×0.6) | Our pick |
    | Armor | Cuts melee like bullets: 60 becomes 42, 36, or 27 through tier 1, 2, or 3 vests | PUBG: vests cut melee the same as bullets |
    | Hits to kill to the body | 2 with no vest, 3 through tier 1 or 2, 4 through tier 3 | Same as PUBG's machete |
    | Time between swings | 0.8 s | Our pick |
    | Reach | 1.5 m | Our pick |
    | Ready time | 0.5 s | PUBG's melee ready delay |
    | Run speed with it out | 6.3 m/s | PUBG's unarmed and melee speed ([Handling](handling.md)) |

- **Inspects:** every melee weapon gets its own inspect animation, and you can inspect while running with it out (hold X), like flipping a butterfly knife open, spinning a karambit, or resting a scythe on your shoulder.
- **The roster:** all sorts, with plain names and no brands. The owner's picks are scythes, knives of different kinds, machetes, and brass knuckles. A starting list:

    | Kind | Weapons |
    | --- | --- |
    | Knives | Combat knife, hunting knife, folding knife, butterfly knife, karambit, kukri, tanto, bayonet |
    | Big blades | Machete, cleaver, hatchet, axe, cavalry sabre, katana |
    | Farm tools | Scythe, sickle, pitchfork |
    | Tools | Crowbar, shovel, entrenching tool, pickaxe, wrench, tire iron |
    | Blunt | Brass knuckles, baseball bat, police baton, lead pipe, rolling pin, trench club |
    | Hammers | Claw hammer, ball-peen hammer, mallet, war hammer |
    | Military | Trench knife, bowie knife, tomahawk |
    | Martial arts | Nunchaku, tonfa, kama, bo staff |
    | Historic | Gladius, cutlass, rapier, mace |
    | Sports | Cricket bat, hockey stick, golf club |
    | Everyday | Umbrella, broom, chair leg, guitar, skateboard |
    | Joke and event rewards | A fish, a rubber chicken, a giant spoon |

- **Pans and breaching tools** are class items, not melee: pans block bullets, and breaching tools (the sledgehammer, bigger hammers, an entry bar, and a door ram) break in. Both hit harder than melee ([Pans](class-items.md#pans), [Breaching tools](class-items.md#breaching-tools)). Owned hammers are the hand-sized ones; the big ones are breaching tools.
- **Bayonets:** a version that really had a bayonet lug has a chance to spawn with a bayonet fitted, for a quicker melee: a stab with the gun still up, instead of switching to your melee. Same damage as any melee hit. First pass (our pick): a 1 in 4 chance, rolled when the gun spawns. The gun pages will need to mark which versions had a lug.
- **Throwing knives** are a throwable you pick back up ([Throwables](weapon-pool.md#throwing-knives)).
- **Throwing your melee (idea):** throw your melee weapon for the same damage, then go pick it back up, like PUBG's thrown melee.

## Built-in tools

Every player carries a few tools that aren't items and take no slot. They're used with the interact key.

- **Wire cutters:** cut a gap in a wire fence quietly, in about 3 seconds (our pick). Driving through a fence is fast but loud.
- **Small hammer:** nails doors shut, so anyone coming in has to shoot or breach their way through, or use a window ([Nailing doors shut](#nailing-doors-shut)). It can't break doors or walls; that takes a [breaching tool](class-items.md#breaching-tools).
- **More tools** can come later.

### Nailing doors shut

First pass (our pick):

- **Boards:** loot found in and around buildings, like sheds, farms, and building sites. One door takes 2 boards.
- **Wood doors only:** metal doors can't be nailed.
- **Nailing:** about 4 seconds per door, from either side. The hammering is loud, so players nearby hear it.
- **Getting through from outside:** shooting the boards out is easy with any gun. Each board breaks after about 60 damage of gunfire: about 2 rifle shots or 3 pistol shots, or one close buckshot blast for both. A [breaching tool](class-items.md#breaching-tools) also works (a nailed door counts as 2 doors of its durability), and so do explosives.
- **From inside:** anyone can pry the boards off with their own hammer in about 3 seconds, quietly, and gets the boards back.
- **Windows stay open:** windows can't be boarded, so there's always a way in.

## Dog tags

Every player wears dog tags that can't be taken off.

- **Collecting:** when you kill someone, you or a teammate can pick up their tags from the body.
- **Confirmed kills:** collected tags give bonus XP and go into your personal collection of players you've confirmed killed. A teammate collecting them still counts as confirmed for you.

## Tracks and animals

- **Footprints** show in snow, mud, and similar ground, and **tire tracks** show where vehicles went.
- **Animals that give you away (idea, to refine):** birds in trees and on buildings fly off when players get close, like Hunt: Showdown's crows, so a flock taking off tells others someone's there.

## Buildings & materials

Buildings are semi-destructible, kept simple: doors, windows, and specific walls can break. Materials matter too.

Wire fences (possibility): drive straight through them like PUBG, or cut a gap quietly for a stealthier approach. Every player carries wire cutters to cut a gap quietly ([Built-in tools](#built-in-tools)), while driving through is fast but loud.

- Wood can be shot through.
- Thin metal can be shot through by some weapons.

## Match setup

- **Modes:** solos, duos, trios, and quads.
- **Ranked:** a separate ranked playlist.
- **Custom matches and fun modes:** private custom matches for friends, streamers, and tournaments, plus rotating fun modes. Later, a full custom rules set ([Custom games and mods](#custom-games-and-mods-later)).
- **Practice lobby:** a private lobby where a player can try every gun, version, and vehicle.
- **Victory line:** the game gets its own line for a win, like PUBG's "Winner winner chicken dinner." The wording is TBD.
- **Player count:** set by each map's size; 100 on the first map ([Maps](maps.md)).
- **Zone:** works like PUBG's, with damage that grows the deeper outside you are, so zone camping doesn't pay ([Match flow](match-flow.md#the-zone)).
- **Red zones:** PUBG's red zone in several forms (bombardment, smoke, gas, and more to come), each announced by an air raid siren ([Match flow](match-flow.md#red-zones)).
- **Plane and parachutes:** a random plane path and PUBG-style parachutes ([Match flow](match-flow.md#the-plane)).
- **Crates:** arrive by air drop at random ([Match flow](match-flow.md#care-packages)).
- **Vaults:** locked vaults opened with rare keys, like Apex's ([Match flow](match-flow.md#vaults-and-keys)).
- **Time and weather:** time passes during a match, from day into night or night into morning, and weather can change ([Match flow](match-flow.md#time-of-day-and-weather)).
- **Wrist watch:** always on the left wrist, showing the in-game time ([Match flow](match-flow.md#wrist-watch)).
- **Hot loot zones:** yes.

## Custom games and mods (later)

- **Custom rules:** a full rules set for custom games, so hosts can change things like the gun pool, loot amounts, zone speed and damage, team size, respawns, and which items spawn.
- **Map editor:** an add-on map editor, so players can build their own maps.
- **Workshop:** players share maps and other content through a workshop, like Steam Workshop.
- **Legal side:** player-made content needs its own terms, covering who owns it and what's allowed, before it's opened up ([Legal review](../planning/legal-review.md#the-list)).

## Sound

Sound is a major focus.

- **Real sound travel:** sound moves at its real speed, about 343 m/s, so a shot 300 m away is heard almost a second after it's fired.
- **Bullet crack:** bullets still faster than sound crack as they fly past you. The crack lands before the bang, so the gap between them hints at how far away the shooter is. Subsonic rounds, like .45 ACP and the [VSS](../weapons/battle-rifles/vss.md)'s 9×39mm, don't crack.

- **Proximity chat:** nearby players, enemies included, can hear each other talk, like PUBG.
- **Suppression (to look into):** near misses could cause a light blur or shake, as in Battlefield and Squad. It has to stay light so it doesn't decide fights by luck.

How gun sounds are layered and sourced is on [Gun art and sound](../planning/art-and-sound.md#sound).

## Death cam and replays

- **Death cam:** after you die, see the moment from the shooter's view, like PUBG's.
- **Replays:** matches can be watched back afterward. Both help players learn and help spot cheaters.

## Anti-cheat

Cheaters are a real problem. The game uses Easy Anti-Cheat, free through Epic Online Services; it gets wired in later in the build ([Getting started](../planning/getting-started.md)).

## Sources

- [PUBG Wiki: Vehicles](https://pubg.wiki.gg/wiki/Vehicles) (seats and top speeds) · [Dexerto: PUBG vehicles](https://www.dexerto.com/wikis/pubg/vehicles/) (the full list)
