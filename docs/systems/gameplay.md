# Gameplay and mechanics

Matches favor scavenging and a slower pace over fast action, in a classic battle royale format.

- **Camera:** the game is played in first person, including driving. Parachuting is the only third-person part.
- **Hit zones:** six zones: head, neck, chest and stomach (one zone), groin, arms, and legs, with no lucky one-shots ([Hit zones](ttk.md#hit-zones)).
- **Handling:** spread, ready and ADS times, reloads, and movement speed per category are on [Handling](handling.md).
- **Healing:** PUBG's healing items and boost bar, with six slots filled by Escape from Tarkov's meds, drinks, and stimulants, each a little better or worse than PUBG's numbers, and one item per slot each match ([Healing](healing.md)).

## HUD and inventory

The layout follows PUBG's from 2017 and 2018, with the game's own look (no PUBG art, icons, or fonts). The mockup is a private Design artifact in the owner's Claude account.

- **Weapon slots:** 1 and 2 hold primaries, 3 is the pistol / 3rd slot ([Rules](../rules.md#3rd-slot)), 4 holds a [class item](class-items.md), and 5 holds a throwable. Melee has its own button instead of a slot.
- **Menus:** laid out like PUBG's, with our own art, the same way as the HUD (owner, 2026-11-22). Your character, with your squad beside you, stands in the middle; tabs run across the top; Play and the mode picker sit top left; friends and invites on the right. Tabs (our pick):
    - **Play:** solo, duo, trio, or quad, the region, and whether to fill the squad with other players. Custom games go here too, with bigger squads.
    - **Wardrobe:** your character, outfit, gun and gear skins, melee weapon, and emotes ([Skins](skins.md)).
    - **Career:** stats, weapon mastery, and good fight thumbs up ([Good fight](#good-fight)).
    - **Replays** ([Death cam and replays](#death-cam-and-replays)).
    - **Settings (owner, 2026-11-22):** Gameplay (the field of view slider, [First person](#first-person)) and Controls first; Graphics and Audio after. Sensitivity works like PUBG's: general, aim, ADS, one per scope from 2x to 15x, and a vertical multiplier. Every key can be rebound. HUD size (owner, 2026-11-23): a slider in Gameplay from 75% to 125%, 100% by default (our pick). It scales the compass, health and boost, ammo, slots, minimap, and kill feed together; the crosshair stays the same size.
    - **No store** while the game is private.
- **HUD:** a compass at the top with the heading in yellow; players alive and kills at the top right; the crosshair; health, boost, stance, gear durability, ammo, and fire mode at the bottom center; the five slots as weapon silhouettes beside the minimap at the bottom right.
- **Picking up:** look at an item and press F, like PUBG. The prompt names a gun's rolled version, since every gun is one version for the match ([Rules](../rules.md#versions)).
- **Keys:** PUBG's defaults: WASD to move, Shift sprint, Ctrl walk, C crouch, Z prone, Space jump and vault, = auto-run, Alt free look, V perspective, F interact, Tab inventory, left mouse fire, right mouse aim (tap to toggle, hold to hold), R reload, B fire mode, Q and E peek, middle mouse to ping, and 1 to 5 for the slots. The one change is X, which is melee: tap X for a quick melee attack, and hold X to stow your guns and pull out the melee weapon so you run faster ([Melee](#melee)).
- **Reloads keep their progress:** a cancelled reload picks up where it stopped next time, and if the old mag was already out, the gun stays without one until you finish ([Staged reloads](handling.md#staged-reloads)).
- **Safe is for stowing only:** there's no safe on the fire-mode key. A gun goes to safe only when it's stowed, such as when you hold X for melee, and goes back to the last fire mode you picked when you draw it. The draw animation will show the selector coming off safe later (owner, 2026-11-22).
- **Ping:** middle mouse marks enemies, loot, and places for your squad, and means different things depending on what you aim at, like Apex's.
- **Inventory (Tab):** vicinity, backpack, gear (helmet, vest, backpack, and outfit slots for skins), and the weapons with their attachment slots. Hovering a gun shows its version: cartridge, fire modes, rate, and mag. You can still move with it open.

## First person

The view and the way guns are held look like PUBG's first person (owner, 2026-11-22). Two PUBG screenshots are in the game repo at `Art/Reference/FirstPerson/`, for reference only.

- **Field of view:** a slider from 80 to 103, with 90 as the default, like PUBG's first person. Both are horizontal, measured on a 16:9 screen, so the numbers carry straight over to Unreal's camera. Parachuting is third person, with a fixed view.
- **The gun's own view:** the gun draws with its own field of view and scale, so it never pokes through walls and stays the same size whatever the slider says (our pick). That's Unreal's First Person Rendering, already set up from the template ([Animation](../planning/art-and-sound.md#animation)).

### At the hip

- **Low and right:** the gun sits in the lower right of the screen, angled in toward the center, with the stock at the shoulder.
- **Hands:** the right hand on the grip, and the left hand under the handguard from below.
- **Clear center:** the top of the gun stays below the crosshair, so the middle of the screen is open.
- **Hip fire** goes toward the crosshair, with the category's hip spread ([Handling](handling.md#first-pass)).

### Aiming down sights

- **Centered:** the gun comes up and the sight lines up with the exact center of the screen, so you aim where the crosshair was.
- **Speed:** each category's ADS time ([Handling](handling.md#first-pass)).
- **Zoom:** iron sights and 1x sights zoom in a little (our pick; how much is TBD, matched by eye to the PUBG reference below). Scopes zoom to their power ([Attachments](attachments.md)).
- **Iron sight size (owner's references, 2026-11-23):** the owner sent three screenshots for the lead. They're described here and not kept:
    - **PUBG, the M416 at 100 m zeroing:** the rear sight sits low and fairly small, across about the middle third of the screen's width and mostly below the center. The front post's tip is exactly at the center, and most of the screen around the sight stays clear.
    - **A recent Call of Duty:** the rear ring is big and close, about 40% of the screen's width, with the front post inside it.
    - **Call of Duty: Modern Warfare 2 (2009):** in between, with a compact rear sight and the front sight's round hood at the center.
- **The target (our pick):** PUBG's look, the first one: a small, low sight with the front post at the center and a clear view around it, at the default field of view of 90. The Call of Duty shots show how big is too big.

### Arms and sleeves

- **Your outfit shows:** the arms wear the jacket or shirt sleeves and gloves from your wardrobe slots, and show bare arms in your skin tone when those are off ([Wardrobe](skins.md#wardrobe), [Your character](skins.md#your-character)).

### The character for now

1. **Now:** the template's mannequin, already in the project.
2. **Next:** the full low-poly male and female test bodies, one standard face each, made in Blender on Unreal's mannequin skeleton so every animation works on them. The first-person arms come from these bodies (owner, 2026-11-22) ([Your character](skins.md#your-character)).
3. **Final:** characters closer to PUBG's ([Art style](../planning/art-and-sound.md#art-style-low-poly-for-testing)).

Both bodies share one skeleton, one hitbox, and the same first-person arm setup, so every gun and animation works on either (our pick).

## Knockdowns & revives

1. At zero health you're knocked down. You can crawl, but you leave a blood trail.
2. A teammate can pick you up while you're knocked. This is slow without an adrenaline syringe.
3. If you bleed out, you can still be revived with a defib, or slowly with CPR.

**Kill credit (planner's picks, 2026-11-22, for the lead):**

- **The knocker gets the kill** when a knocked player bleeds out, finishes themselves, or is finished by their own squadmate.
- **A player brought back is a live player again:** killing them a second time counts as a new kill for whoever does it.
- **A knocker who leaves the match** still gets the kill in the match results.

**Bodies hold the loot:** a dead player's body stays where it fell and holds everything they carried. While a squadmate could still revive them, it stays a body: anyone can loot it straight from the body, and a looted body can still be revived, with whatever is left on it (owner, 2026-11-22). Once nobody can revive them anymore, or they go to the [comeback duel](#comeback-fight), the body turns into a loot crate right away, like PUBG's. It does the same if the player leaves the match.

**Self-revive kits** let you get up on your own, like PUBG's. They spawn more often in solos and less often in duos, trios, and quads.

**No knockdown shields.**

**Adrenaline** items are rare and have two uses: PUBG's full boost ([Healing](healing.md#boost-bar)) and a quick teammate pickup. They replace the infinite-stamina idea, since original PUBG had no stamina. You don't need one in your hands to use it.

## Comeback fight

Warzone-style 1v1 duels (owner, 2026-11-22):

- **The duel:** when you're out, you go to the comeback arena and fight another player 1v1. The winner redeploys into the match.
- **One redeploy:** each player gets one comeback per match. Winning, redeploying, and dying again ends your match, unless you've made another comeback at a [workbench](crafting.md#what-a-workbench-makes) with scrap.
- **Only early:** the arena is open for the first couple of circles (first pass: until phase 2 ends). When it closes, anyone still waiting or fighting there redeploys for free.
- **Loadouts (owner, 2026-11-22):** both players get the same random gun from the match's pool, and the winner keeps it when they redeploy.
- **The arena** is hidden underground, so it never gets in the way of the match (owner). It has several small layouts, and each duel rolls one (owner, 2026-11-22).
- **Timer:** after 60 seconds a capture point opens, and whoever takes it wins (owner), like the flag in Warzone's Gulag.

**Breakout (rare event):** in duos, trios, and quads only, a rare event brings every eliminated player back into the match at once, like Warzone's Jailbreak.

## Vehicles and water

Lots of vehicles of our own, picked for what each map needs. Ziplines are part of the map too. Trains could run on maps with rail, and a gondola could carry players up a mountain on a future map.

The lineup (owner, 2026-11-22): each PUBG vehicle gets a stand-in based on a similar real vehicle, with an Eastern Bloc look to fit the first map. Names are Russian nature and animal words, the way Soviet cars had names like Volga and Niva ([Game names](../planning/game-names.md#vehicles)). Seats and top speeds start at PUBG's, where known.

| Ours | Based on | Replaces (PUBG) | Seats | Top speed (PUBG) |
| --- | --- | --- | --- | --- |
| **Vesna 12** | Lada 2101-style sedan | Dacia 1300 | 4 | 139 km/h |
| **Barsuk 4** | UAZ-469-style jeep, open or closed top | UAZ | 5 | 105 km/h open, 115 km/h closed |
| **Barsuk 4 Winter** | The same jeep on snow tires | Zima | — | — |
| **Peschanka** | Dune buggy | Buggy | 2 | 100 km/h |
| **Strizh 350** | Jawa 350-style road motorcycle | Motorcycle | 2 | 152 km/h |
| **Sever S-650** | Ural-style sidecar motorcycle | Motorcycle with sidecar | 3 | 130 km/h |
| **Tushkan** | Enduro dirt bike | Dirt Bike | — | — |
| **Pchelka** | Vyatka-style scooter | Scooter | 2 | — |
| **Kuznechik** | Three-wheeled cargo scooter | Tukshai | 3 | — |
| **Yastreb 24** | The Volga sedan with the KGB's V8 | Mirado | 4 | 152 km/h |
| **Burlak** | Small pickup | Pickup and Rony (merged) | 4 | 110 km/h |
| **Karavai** | UAZ-452 "loaf" van | Van | 6 | 110 km/h |
| **Molniya GT** | Sports coupe | Coupe RB | — | — |
| **Zayats** | Zaporozhets-style small car | Pony Coupe | — | — |
| **Bobr** | Small cab-over truck | Porter | — | — |
| **Lis** | Niva-style small 4x4 | Blanc | — | — |
| **Gus** | Soviet minibus | Pico Bus | — | — |
| **Kaban** | Four-wheeler | Quad | — | — |
| **Purga** | Soviet snowmobile | Snowmobile | 2 | — |
| **Ezh** | Amphibious scout car, called in with a flare gun ([Care packages](match-flow.md#care-packages)) | BRDM-2 | — | — |
| **Baklan** | Motorboat | Boat (PG-117) | 5 | 90 km/h |
| **Tyulen** | Jet ski | Aquarail | 2 | 90 km/h |
| **Veter** | Propeller airboat | Airboat | — | — |
| **Zhuravl** | Two-seat motor glider | Motor Glider | 2 | — |
| Patrol car | A Vesna 12 in police colors | Pillar Security Car | 4 | — |
| Kvass truck | A Soviet street kvass barrel truck | Food Truck | — | — |
| Mountain bike | Bicycle | Mountain Bike | 1 | — |
| Inflatable boat | Rubber boat | Inflatable Boat | — | — |
| **Pakhar** (new) | Belarus-style farm tractor | — | — | — |
| **Mamont** (new) | Ural-style 6x6 army truck: slow but tough | — | — | — |

Dashes are numbers the sources checked don't give. Each map gets the vehicles that fit it (owner, 2026-11-22): boats on the coast, cars in towns, police vehicles near the police station, and so on. Snow vehicles fit snow maps.


- **Fuel and tires:** like PUBG, vehicles run out of fuel and need refilling, and their tires can be shot out.
- **Swimming:** players can swim and dive underwater to break line of sight, like PUBG.

## Melee

- **Key:** tap X for a quick melee attack. Hold X to stow your guns and pull out your melee weapon, which lets you run faster.
- **Quick hit timing (planner's pick, 2026-11-22):** the hit lands 0.3 s after the tap, faster than pulling the melee weapon out (0.5 s), then the gun comes back with its own ready time. A gun with a bayonet stabs at once, without putting the gun away.
- **Empty hands:** running with nothing out is the same 6.3 m/s as melee out, PUBG's unarmed speed.
- **Fists (owner, 2026-11-23):** a melee pick like all the others, with the same numbers. They're for players who just want to punch and show off their gloves and watch: the inspect holds up both hands to show the gloves from your wardrobe and the wrist watch ([Wrist watch](match-flow.md#wrist-watch)). With no melee weapon in hand, such as after throwing yours, you fight with your fists the same way.
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
    | Unarmed | Fists, taped fists |
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
- **Throwing your melee (owner, 2026-11-23):** every melee weapon can be thrown for the same damage, like PUBG's thrown melee. It lands where it hits, and you go pick it back up; until then you fight with your fists. Fists can't be thrown (our pick).

## Built-in tools

Every player carries a few small tools for in-game actions. They aren't items or melee weapons, take no slot, and are used with the interact key.

- **Wire cutters:** cut a gap in a wire fence quietly, in about 3 seconds (our pick). Driving through a fence is fast but loud.
- **Small hammer:** nails doors shut, so anyone coming in has to shoot or breach their way through, or use a window ([Nailing doors shut](#nailing-doors-shut)). It can't break doors or walls; that takes a [breaching tool](class-items.md#breaching-tools).
- **Small crowbar (idea):** pries open wooden boxes. Where wooden boxes show up is left for later (owner, 2026-11-22). It's not the crowbar melee look or the entry bar breaching tool, and it can't open doors.
- **Screwdriver (owner, 2026-11-22):** switches a building's lights off at its fuse box at night ([Time of day](match-flow.md#time-of-day-and-weather)), unscrews vent covers for a quiet way in, and picks small locks, like a [briefcase](loot.md#briefcases)'s.
- **More tools** can come later.

### Nailing doors shut

The hammer drives nails through the door into its frame, so there's nothing to carry (owner, 2026-11-22). First pass (our pick, timing the owner's):

- **Wood doors only:** metal doors can't be nailed, and a door that's been destroyed can't be nailed shut.
- **Nailing:** about 4 seconds per door, from either side. The hammering is loud, so players nearby hear it.
- **Getting through from outside:** break the door. Shooting it is easy with any gun: a wood door breaks after about 120 damage of gunfire, about 3 rifle shots, 4 pistol shots, or one close buckshot blast. A [breaching tool](class-items.md#breaching-tools) or explosives also work. A broken door is gone for the match.
- **From inside:** pull the nails with the hammer's claw in about 3 seconds, quietly, and the door works again.
- **Windows stay open:** windows can't be nailed, so there's always a way in.

## Dog tags

Every player wears dog tags that can't be taken off.

- **Collecting:** when you kill someone, you or a teammate can pick up their tags from the body.
- **Confirmed kills:** collected tags give bonus XP and go into your personal collection of players you've confirmed killed. A teammate collecting them still counts as confirmed for you.

## Tracks and animals

- **Footprints** show in snow, mud, and similar ground, and **tire tracks** show where vehicles went.
- **Birds give you away (owner, 2026-11-22):** birds in trees and on buildings fly off when players get close, like Hunt: Showdown's crows, so a flock taking off tells others someone's there. Birds are the only animals for now: no farm dogs or livestock, since the owner isn't sure other animals belong.
- **Noise makers:** the birds, [robot guards](match-flow.md#robot-guards-idea), and other things that react to players are player locators more than threats, like Hunt's crows, barking dogs, and spooked horses.

## Buildings & materials

Buildings are semi-destructible, kept simple: doors, windows, and specific walls can break. Materials matter too.

Wire fences (owner, 2026-11-22): drive straight through them like PUBG, fast but loud, or cut a quiet gap with the wire cutters every player carries ([Built-in tools](#built-in-tools)).

- Wood can be shot through.
- Thin metal can be shot through by some weapons.

## Match setup

- **Modes:** official matchmaking is solos, duos, trios, and quads. Custom game lobbies can have bigger squads, and so can special game modes that need them (owner, 2026-11-22).
- **Ranked:** a separate ranked playlist.
- **Custom matches and fun modes:** private custom matches for friends, streamers, and tournaments, plus rotating fun modes. Later, a full custom rules set ([Custom games and mods](#custom-games-and-mods-later)).
- **Practice lobby:** a private lobby where a player can try every gun, version, and vehicle.
- **Victory line:** the game gets its own line for a win, like PUBG's "Winner winner chicken dinner." Ours is "The island is yours" (owner, 2026-11-22). The line is rolled from a few, with different lines for solo and squads (owner). First lines (our pick): solo gets "The island is yours" or "Last one standing", and squads "The island is yours" or "Last squad standing".
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
- **No suppression effect (owner, 2026-11-22):** near misses only make noise, like PUBG's, with no blur or shake.

How gun sounds are layered and sourced is on [Gun art and sound](../planning/art-and-sound.md#sound).

## Death cam and replays

- **Death cam:** after you die, see the moment from the shooter's view, like PUBG's.
- **Spectating squadmates:** once you're out, watch your squadmates who are still alive, switching between them.
- **Spectating enemies:** once your whole squad is out, watch other players still in the match, starting with whoever finished your squad, until the match ends.
- **Replays:** matches can be watched back afterward. Death cams, spectating, and replays help players learn and help spot cheaters.
- **Spectating delay (our pick):** what you see runs a few seconds behind, so a squad that's out can't call out live positions to anyone.

## Bots

The owner's picks (2026-11-22). First pass for how they play (our pick):

- **Where:** bots fill the lobby and any empty slots in a match, so games feel full ([Pre-match lobby](match-flow.md#pre-match-lobby)).
- **Not marked:** like PUBG, nothing shows that a player is a bot.
- **Skill:** three levels, easy, normal, and hard, set per match. The level sets how fast they react, how far away they notice players, and how well they aim and control recoil.
- **How they play (our pick):** they jump from the plane like players, loot the buildings near where they land, move in with the zone, heal when hurt, and fight players they see or hear.

## Training map

A practice map, like PUBG's Training Mode (owner, 2026-11-22). PUBG added it in 2018 on its own 2 × 2 km map for 5 to 20 players, and later added a list of stations you teleport between. The owner's screenshot of the current one is the reference; it's described here and not kept. Write-up for the lead (2026-11-23), first pass (our pick):

- **Getting in:** a Training button on the menu's Play tab, next to the modes. It puts you straight into a training server, with no queue and no plane. Up to 20 players, solo or with your squad.
- **The map:** its own small island, about 2 × 2 km, in the game's look. Players can't hurt each other outside the arena, there's no zone, and ammo and meds are free from the tables.
- **Getting around:** open the map (M) and pick a station to teleport there, like the current PUBG one. You can also walk or drive between them.
- **Stations:**

    | Station | What's there |
    | --- | --- |
    | Firing range | Open ground with distance boards every 50 m out to 200 m, then targets at 400 m and 800 m and one at 1 km. Standing targets, targets that slide left and right, and a board that shows where each shot hit |
    | Gun tables | Every gun version, attachment, armor piece, med, throwable, and melee weapon, not only the current pool. Ammo for every caliber |
    | Close quarters | An indoor range with pop-up targets, and a town block built from the [building kit](maps.md#towns-and-buildings) |
    | Grenade pit | Throwables, with distance marks and targets in trenches and windows |
    | Driving | A ring road, a race track, an off-road course, stunt ramps, a bridge, a parking lot with every vehicle, and docks with boats and water ramps |
    | Drive-by range | A loop where one player drives and the others shoot at targets from the seats |
    | Jump tower | Parachute practice: a tower and a plane loop over landing circles, to practice landing far and landing fast |
    | Movement course | Vaulting, climbing, windows, fences, and swimming |
    | Aim and hearing drills | Aim drills, and drills for telling where footsteps and gunshots come from |
    | Arena | Fights against a bot that always fights back ([Bots](#bots)), or one on one against another player. You set how many rounds outside the arena; a run against the bot ends if you die |

- **The training panel:** a key (T, our pick) opens a panel to spawn any item or vehicle at your feet, set the time of day and weather, and reset the targets. It's the lead's test bench and sky panel, built for players.
- **For now:** the lead's range map is the start of it. The test bench, sky panel, and fly mode stay test tools, refused on real match servers like the other test commands.

## Good fight

A positive play rating: give a player a thumbs up for a good fight (owner, 2026-11-22). First pass (our pick):

- **When:** from the death screen, the spectating view, or the end-of-match screen, for anyone you fought or watched.
- **One each:** one thumbs up per player per match.
- **Positive only:** no thumbs down, so it can't be used to pile on anyone.
- **Shown** as a total on the player's profile, with the most recent fights.

## Anti-cheat

Cheaters are a real problem. The game uses Easy Anti-Cheat, free through Epic Online Services; it gets wired in later in the build ([Getting started](../planning/getting-started.md)).

## Sources

- [Esports Tales: PUBG field of view](https://www.esportstales.com/pubg/the-best-fov-field-of-view) (80 to 103, default 90, horizontal)
- [PC Gamer: PUBG's Training Mode (2018)](https://www.pcgamer.com/pubgs-training-mode-will-feature-a-shooting-range-racetracks-parachute-practice-and-more) (2 × 2 km, 5 to 20 players, ranges to 1 km, driving, parachute practice, item tables)
- [PUBG Wiki: Vehicles](https://pubg.wiki.gg/wiki/Vehicles) (seats and top speeds) · [Dexerto: PUBG vehicles](https://www.dexerto.com/wikis/pubg/vehicles/) (the full list)
