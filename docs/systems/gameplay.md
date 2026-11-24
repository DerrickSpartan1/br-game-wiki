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
- **Accent (owner, 2026-11-24):** field lime (#A8C34B), a military olive bright enough to read on dark panels, for the Play button, the open tab, toggles, selected items, your squad's highlights, and the HUD compass heading. Warnings and damage keep their own red, and no PUBG yellow is left ([PUBG look and feel](../planning/legal-review.md#pubg-look-and-feel)).
- **HUD:** a compass at the top with the heading in the lime accent; players alive and kills at the top right ("1 killed"); an optional network readout at the top left (packets a second and packet loss, like PUBG's; off by default, turned on in Settings, our pick); the crosshair; health, boost, stance, gear durability, ammo, and fire mode at the bottom center; the five slots as weapon silhouettes beside the minimap at the bottom right.
- **Picking up:** look at an item and press F, like PUBG. The prompt names a gun's rolled version, since every gun is one version for the match ([Rules](../rules.md#versions)).
- **Keys:** PUBG's defaults: WASD to move, Shift sprint, Ctrl walk, C crouch, Z prone, Space jump and vault, = auto-run, Alt free look, V perspective, F interact, Tab inventory, left mouse fire, right mouse aim (tap to toggle, hold to hold), R reload, B fire mode, Q and E peek, middle mouse to ping, and 1 to 5 for the slots. The one change is X, which is melee: tap X for a quick melee attack, and hold X to stow your guns and pull out the melee weapon so you run faster ([Melee](#melee)).
- **Reloads keep their progress:** a cancelled reload picks up where it stopped next time, and if the old mag was already out, the gun stays without one until you finish ([Staged reloads](handling.md#staged-reloads)).
- **Safe is for stowing only:** there's no safe on the fire-mode key. A gun goes to safe only when it's stowed, such as when you hold X for melee, and goes back to the last fire mode you picked when you draw it. The draw animation will show the selector coming off safe later (owner, 2026-11-22).
- **Ping:** middle mouse marks enemies, loot, and places for your squad, and means different things depending on what you aim at, like Apex's.
- **Taking damage (owner asked, 2026-11-24; numbers our pick):** the screen shows each hit without hiding the fight. As far as we found, PUBG's 2017–2018 damage effects aren't written down anywhere to copy, so these are ours.
    - **Every hit:** a red tint at the screen's edges comes in at once and fades over half a second. It's stronger the more damage the hit did, so a 5-health tick is a faint blush and a 50-health hit is a strong flash.
    - **Where it came from:** bullets, melee, and explosions also show a short red arc around the crosshair, pointing at the source, for 2 seconds.
    - **Inside the edge:** the edge's own tint stays, and each damage tick makes it swell for about a third of a second and ease back, with a faint red flash and the soft thump on [The edge](../systems/match-flow.md#the-edge-how-it-looks).
    - **Fire and gas:** the same flash on each tick, with an orange flicker while you're burning.
    - **Falls:** the flash, with no arc.
    - **Low health:** under 20 health, a faint red stays at the edges until you heal above it.
    - **A setting:** damage flash strength from 0 to 100% in Settings > Gameplay, for players who find it too much.
- **The map (owner asked for it to work like PUBG's, 2026-11-24; details our pick):** M opens the full map over the game, which keeps running.
    - **Zoom and pan:** the scroll wheel zooms toward the cursor, from the whole island to about 200 m across the screen. Drag with the left mouse to pan. Space centers it on you.
    - **The grid:** 1 km squares with letters across the top (A to J for Teplov's 10 km) and numbers down the side (1 to 8), so a call like "D5" means one square. Lines every 100 m fade in as you zoom, and a scale bar in the corner shows distance.
    - **Your marker:** right click places your marker, and right click on it or Delete removes it; Insert marks where you're standing. One marker each, in your squad color, like PUBG. Squadmates see it on their map, minimap, and compass with the distance, and as a small marker on screen.
    - **Marker wheel:** hold right click for a wheel of six quick markers (attack, danger, defend, loot, regroup, vehicle), the way PUBG added them later. They replace your one marker.
    - **Route:** Shift and right click add up to five route points, drawn as a line from you through them, for your squad to see. Shift and right click on a point removes it.
    - **What it shows:** the plane's path before and during the jump, the blue and white circles, strike zones, your squad with their numbers and colors, vehicles your squad is in, and vaults you hold a key for. Never enemies, care packages, or loot.
    - **How it looks (from the owner's PUBG screenshot, 2026-11-24; our own art):** everything outside the edge is washed in see-through teal, so the safe area stands out; the next safe circle is a thin white ring; strike zones are see-through red discs; the plane's path is a thin straight line from a dot where it comes in. Tabs along the top switch between the map and a match log (your kills, knocks, and damage this match, in order). PUBG letters both its grid's columns and rows; ours keeps numbers for the rows, so a call like "D5" can't be misheard.
    - **Colors (our pick, 2026-11-24):** the edge is a solid ring in the wall's bottom teal, the next safe circle a thin white ring, and strike zones red, so none of them look alike ([The edge](match-flow.md#the-edge-how-it-looks)).
    - **Minimap:** bottom right, turned with you, with your squad, markers, circles, and strike zones. N zooms it between about 400 m and 1 km across.
- **Inventory (Tab):** vicinity, backpack, gear (helmet, vest, backpack, and outfit slots for skins), and the weapons with their attachment slots. Hovering a gun shows its version: cartridge, fire modes, rate, and mag. You can still move with it open.

## First person

The view and the way guns are held look like PUBG's first person (owner, 2026-11-22). Two PUBG screenshots are in the game repo at `Art/Reference/FirstPerson/`, for reference only.

- **Hands that move with you (owner, 2026-11-24, like Call of Duty's fists):** empty hands, fists, and melee weapons sit in view and move with your body, the same way a held gun does:
    - **Standing still:** raised near the bottom of the view at chest height, with a slow breathing rise and fall of about 0.5 cm every 4 seconds.
    - **Walking and running:** a figure-eight bob in step with the footsteps: about 1 cm up and down and 0.6 cm side to side when walking, about 2 cm and 1.2 cm at a run.
    - **Sprinting:** the arms pump, swinging forward and back in turn with the strides, and drop a little lower so they don't block the view.
    - **Turning:** the hands lag a little behind the view and catch up in about a tenth of a second, so turning feels heavy, not glued on.
    - **Jumping and landing:** they lift on the jump, float in the air, and dip about 4 cm on landing before settling, more after a long fall.
    - **Crouching and prone:** lower and closer to the body when crouched. Prone, they're out of view while crawling and come up when you stop.
    - **Free look (Alt):** they stay where they are while the view turns.

- **Field of view:** a slider from 80 to 103, with 90 as the default, like PUBG's first person. Both are horizontal, measured on a 16:9 screen, so the numbers carry straight over to Unreal's camera. Parachuting is third person, with a fixed view.
- **Eye height (our pick, 2026-11-23):** the first-person camera sits at the player body's eyes, not below them. Shots and pickups trace from the camera, so they come from the eyes too. When the body changes, the camera moves with its eyes and the hip hold is retuned to match.
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

1. At zero health you're knocked down. You can crawl, but you leave a blood trail. You crawl at 0.8 m/s, two thirds of a prone crawl (our pick, 2026-11-24). PUBG publishes no number for it; [its wiki](https://pubg.wiki.gg/wiki/DBNO) only notes that a 2022 update made it 10% faster.
2. A teammate can pick you up while you're knocked. This is slow without an adrenaline syringe.
3. If you bleed out, you can still be revived with a defib, or slowly with CPR.

**Kill credit (planner's picks, 2026-11-22, for the lead):**

- **The knocker gets the kill** when a knocked player bleeds out, finishes themselves, or is finished by their own squadmate.
- **A player brought back is a live player again:** killing them a second time counts as a new kill for whoever does it.
- **A knocker who leaves the match** still gets the kill in the match results.

**Bodies hold the loot:** a dead player's body stays where it fell and holds everything they carried. While a squadmate could still revive them, it stays a body: anyone can loot it straight from the body, and a looted body can still be revived, with whatever is left on it (owner, 2026-11-22). Once nobody can revive them anymore, or they go to the [comeback duel](#comeback-fight), the body turns into a loot crate right away, like PUBG's. It does the same if the player leaves the match.

- **Crates stay all match (our pick, 2026-11-24):** emptied ones too, shown open and empty, so they still mark where a fight happened. On the range, a crate clears after 2 minutes.
- **A living player who quits** for good drops everything as a crate where they stood. A dropped connection is different: the character stays where it is for 2 minutes so the player can come back, and it can be shot meanwhile; after that, it's a crate (our pick).
    - **The 2 minutes count from when the server notices the drop (our pick, 2026-11-24),** not from the last packet, so the player really gets 2 minutes to come back whatever the engine's own timeout is.
    - **Coming back after the character died (our pick, 2026-11-24):** the player is out, the same as any dead player: the death screen, then spectating as under [Death cam and replays](#death-cam-and-replays) (squadmates first, then enemies once the squad is out), or the menu if they choose.
    - **A returning player keeps their kills and damage (our pick, 2026-11-24)** in the match results, whether or not their character survived the hold.
    - **A squad player whose held character went down for good but can still be revived (our pick, 2026-11-24):** the body stays a body, not a crate, the same as any squadmate's. A returning player waits on it like any dead squad player: the death screen, then spectating their squad, and back in the body if a squadmate revives them. It turns into a crate only once nobody can revive them.
    - **A held body revived after its 2 minutes ran out (our pick, 2026-11-24)** gets a fresh 2 minutes from the revive, since a player brought back is a live player again. If they still aren't back by then, it's a crate.
    - **Quitting and losing the connection get different menu lines (our pick, 2026-11-24):** a player who quits on purpose sees "You left the match"; one who was lost sees "Connection lost", with the option to rejoin while the hold lasts.
    - **Coming back after a crash (our pick, 2026-11-24):** logging in again while held in a match takes over the old session instead of being refused as already online, and sends the player straight back to that match server. Once the hold is over, a login goes to the menu as usual.
- **A body shows what it still holds (our pick):** its vest, helmet, backpack, and guns stay visible until someone takes them, and each disappears as it's taken.
- **Swapping from a body or crate (our pick):** taking a vest, helmet, or backpack from a body or crate puts your old one into that body or crate, so the loot stays in one place. Swapping from the ground drops your old one on the ground, as on [Carry weight](armor.md#carry-weight).
- **Looting a squadmate's body (our pick):** tap F opens its loot, and hold F revives them (with your defib if you carry one, CPR if not). A knocked squadmate is still alive, so F on them only picks them up; they can't be looted.

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
- **Your body when you go:** going to the duel turns your body into a loot crate at once, as on [Bodies hold the loot](#knockdowns-revives). If you win, you redeploy with only the duel's gun and what the arena gives you.

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

Dashes are numbers the sources checked don't give. Each map gets the vehicles that fit it (owner, 2026-11-22): boats on the coast, cars in towns, police vehicles near the police station, and so on. Snow vehicles fit snow maps. On Teplov, the Zhuravl motor gliders spawn at Object 7's airfield, by its glider hangars and on the apron (our pick, 2026-11-23; [Our own spots](maps.md#our-own-spots)).


- **Fuel and tires:** like PUBG, vehicles run out of fuel and need refilling, and their tires can be shot out.
- **Rain (owner, 2026-11-24):** vehicles grip less and take longer to stop on wet ground, during rain and for 2 minutes after ([Weather](match-flow.md#weather)).
- **Swimming:** players can swim and dive underwater to break line of sight, like PUBG.

## Melee

- **Key:** tap X for a quick melee attack. Hold X to stow your guns and pull out your melee weapon, which lets you run faster.
- **Quick hit timing (planner's pick, 2026-11-22):** the hit lands 0.3 s after the tap, faster than pulling the melee weapon out (0.5 s), then the gun comes back with its own ready time. A gun with a bayonet stabs at once, without putting the gun away.
- **Empty hands:** running with nothing out is the same 6.3 m/s as melee out, PUBG's unarmed speed.
- **How melee is held (owner, 2026-11-24):** ready to use, raised in front of you with the watch showing, like you're about to swing. The one exception is free look (Alt), when the hands stay where they were while you look around. Inspect animations can wait.
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

- **Inspects:** every melee weapon gets its own inspect animation, and you can inspect while running with it out (hold X; no separate inspect key, our pick 2026-11-23), like flipping a butterfly knife open, spinning a karambit, or resting a scythe on your shoulder.
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
    - **How to throw (our pick, 2026-11-23):** with the melee weapon out, hold right mouse to aim, which shows an arc like a grenade's, and press left mouse to throw. This is PUBG's way ([ComicBook.com](https://comicbook.com/gaming/news/pubg-throw-items-weapons)).
    - **The throw arc (owner, 2026-11-24):** while you aim a throw (right mouse with a melee weapon or a throwable out), a thin dotted white line shows the path the throw will take, from your hand to where it lands, and a small flat ring marks the landing spot on whatever it hits first. The line stops there, so a wall or a ceiling in the way is plain to see. It updates as you look around, fades out toward the far end, and only you see it. Grenades use the same arc; their bounces aren't shown. As far as we found, PUBG on PC didn't draw an arc in 2017–2018 (throws were learned by feel); PUBG Mobile and later shooters do. It's on by default, with a switch in Settings > Gameplay for players who want it off.
    - **Flight (our pick, 2026-11-23):** thrown at 20 m/s with normal gravity, which carries about 40 m at most, PUBG's longest melee throw ([ComicBook.com](https://comicbook.com/gaming/news/pubg-throw-items-weapons)). PUBG cuts thrown damage past 15 m; ours keeps the same damage at any range, as the owner set.
    - **Who picks it up (our pick, 2026-11-23, waiting on the owner):** only the player who threw it. Your melee is something you own, so nobody else walks off with it. If you die before picking it up, it stays where it landed.

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

- **Parties (owner asked, 2026-11-24; details our pick):** you build your squad in the menu before you press Play, the way PUBG's lobby does ([PUBG support](https://support.pubg.com/hc/en-us/articles/115004169853-How-do-I-play-in-Duo-or-Squad-modes)).
    - **Inviting:** a plus button next to your squad in the menu opens your friends list (who's online first) and a search by player name. Invites show as a pop-up with Accept and Decline, and run out after 60 seconds.
    - **In the menu:** everyone in your party stands beside you in the middle of the menu, with their name, their squad color, and a Ready tick. The one who made the party leads it (a crown by their name); they pick the mode, region, and fill, and only they can press Play.
    - **Queuing together:** Play works once everyone has ticked Ready. The matchmaker puts the whole party in one squad. If the party is smaller than the mode, Fill adds strangers to make it up, and No fill plays short. A party bigger than the mode can't press Play for it.
    - **In the match:** the party is one squad, in the pre-match lobby too, with its colors and numbers on the map.
    - **After a match:** everyone goes back to the menu still in the party. Anyone can leave; the leader can remove someone, and if the leader leaves, the next to join leads.
    - **For the backend:** parties live in the backend (create, invite, accept, leave, remove, hand over the lead, ready), and the matchmaker takes a party as one ticket. A match server gets each squad's members at join. Until then, the `Squad` test command stands in.
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

How gun sounds are layered and sourced is on [Gun art and sound](../planning/art-and-sound.md#sound). Every sound the game needs, and how far each carries, is on the [Sound list](../planning/sound-list.md) (owner asked, 2026-11-24).

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
