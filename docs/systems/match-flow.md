# Match flow

How a match runs, from the lobby to the last circle: the pre-match lobby, the plane and parachutes, the zone, red zones, care packages, vaults, time of day and weather, and the wrist watch. PUBG's 2017–2018 match is the base. Numbers marked "our pick" are first passes to tune in play testing; TBD numbers aren't set yet.

## Pre-match lobby

There's no separate lobby island: players spawn on the match's own map and wait there.

- **Filling up:** the lobby fills with bots, and real players take their places as they join. Bots stay in the match to fill any empty slots.
- **Countdown:** once 10 players have joined, a 60-second countdown starts.
- **Until bots exist (lead, owner OK, 2026-11-21):** the countdown starts once everyone the matchmaker sent has joined, or after a 60-second wait for no-shows. A running countdown keeps going if players leave.
- **No damage** in the lobby, before the plane.
- **Lobby pickups:** anything picked up in the lobby is taken away at boarding.
- **Rolling the match:** the countdown gives the server time to make the match's random choices: the gun pool and versions, vault keys, time of day, and weather.
- **Loot:** ground loot only loads once everyone is moved into the plane.
- **What you have:** only your outfit and your own melee weapon ([Skins and mastery](skins.md#wardrobe), [Melee](gameplay.md#melee)).

## The plane

- **Random path:** every match, the plane flies in from off the map and crosses it in a straight line between two random edges, like PUBG. The path shows on the map before the doors open.
- **Jumping:** jump any time along the path. Anyone still aboard is pushed out near the end.
- **Squads:** teammates can follow one player's jump and land together (our pick).
- **Altitude and speed:** TBD.

## Parachutes

Like PUBG, in third person, the one part of the game that is ([Gameplay](gameplay.md)).

- **Freefall:** up to about 126 km/h forward, or about 232 km/h diving straight down.
- **Opening:** the chute opens on its own at a set height above the ground, earlier over high ground. You can open it sooner by hand.
- **Opening height (owner, 2026-11-24):** 150 m above the ground under you, as in the game now. PUBG's is a set height too; one guide puts it at 300 m ([Appuals](https://appuals.com/playerunknowns-battlegrounds-skydiving-parachuting-guide/)), and it opens earlier over hills.
- **Turning automatic opening off (owner, 2026-11-24):** a switch in Settings > Gameplay, "Open my parachute automatically," on by default. With it off, the chute doesn't open at 150 m, so you can fall lower and land sooner. You open it by hand any time down to 40 m, the last moment. If you never pull, you hit the ground at freefall speed and die (owner, 2026-11-24). The switch only changes your own jump.
- **The freefall readout (owner, 2026-11-24; laid out like his PUBG screenshot of the same day):** two thin gauges either side of the middle of the screen, the way PUBG shows them now. PUBG's 2017–2018 version was a single height bar in the lower left with a white line where the chute would open; a later update split it into a height gauge and a speed gauge ([PC Gamer](https://www.pcgamer.com/uk/pubg-how-to-land-fast-battlegrounds), [PUBG fandom wiki](https://pubg.fandom.com/wiki/Parachute)). Ours uses our own lines, font, and colors.
    - **Height, on the left:** a tall scale labeled ALT, with a marker at your height above the ground under you and the number in meters in a box beside it ("1103 m"). It counts the ground, not the sea, so it drops fast over hills, and a small wave mark at the foot of the scale shows when you're over water.
    - **Marks on it:** a white line where the chute opens by itself (150 m, or not shown with automatic opening off) and an amber line at 40 m, the last moment to pull.
    - **Speed, on the right:** a scale labeled SPD, with a tick every 10 km/h and numbers every 100, and your speed in km/h beside its marker ("147 km/h"): up to 126 forward, 232 diving, and 18 to 64 under the canopy.
    - **Where you're headed:** your squad's map markers show on screen and on the compass with their distance in meters, and so do your squadmates, so you can steer to them.
    - **Under the canopy:** the gauge and speed stay up until you land.
- **Under the canopy:** about 18 to 27 km/h forward, and up to about 64 km/h spiralling down.
- **Distance vs. speed:** opening the chute at the first chance covers the most ground; diving straight at a close target lands first. Both work like PUBG's.

## Aircraft

Everything that flies over a match, in one place (owner, 2026-11-25): "we need to make note of other plane related things going on, maybe this one is like a small plane? and stuff like that, like how pubgs chopper is used for redeploys". Each one has its own shape and engine sound, so you can tell by ear what's coming and why (our pick). PUBG does the same: a transport plane for the jump, a cargo plane for care packages, a plane that catches the Emergency Pickup balloon and carries the squad toward the safe zone, a plane for Recall's returning teammates, and on Taego a helicopter that brings Comeback Arena survivors back to the mainland ([PC Gamer: Emergency Pickup](https://www.pcgamer.com/playerunknowns-battlegrounds-now-lets-you-fulton-your-friends-metal-gear-style), [Dot Esports: Blue Chip Transmitter](https://dotesports.com/pubg/news/how-to-get-and-use-the-blue-chip-transmitter-in-pubg), [GameSpot: Taego's Comeback BR](https://www.gamespot.com/articles/pubgs-12-2-patch-notes-reveal-new-map-that-adds-second-chance-system/1100-6493437/)).

| Aircraft | What it does | Looks like (our pick unless marked) | Heard | Shot down? |
| --- | --- | --- | --- | --- |
| Jump plane | Carries everyone in at the start ([The plane](#the-plane)) | A four-engine jet transport like an Il-76, high and fast, a different shape from the package plane so nobody mixes them up | Everyone near its path | No |
| Care package plane | Drops care packages and the vehicle drops ([Care packages](#care-packages)) | A four-engine turboprop like an An-12, about 300 m up (owner OK'd, 2026-11-24) | 1,500 m | No |
| Money drop | The [money drop](#more-ideas)'s crate rides the care package plane, alone or with other drops (owner, 2026-11-25) | Its own crate and smoke color | 1,500 m (the plane) | No |
| Pickup plane | Snags [cash balloons](#mini-heists), with a limit on how many are out at once (owner, 2026-11-25); more than one can be (owner: "we might want more than one biplane is all"), up to 3 (our pick). Our pick: it also picks up the [emergency redeploy](class-items.md) balloon, under the same limit | A small plane (owner, 2026-11-25: "maybe this one is like a small plane?"): a single-engine biplane like an An-2, slow and low, with a rattling radial engine | 1,000 m (our pick) | The balloon can be; the plane can't (our pick) |
| Comeback helicopter | Brings [comeback duel](gameplay.md#comeback-fight) winners back into the match, like PUBG's helicopter on Taego (owner, 2026-11-25) | A twin-engine transport helicopter like a Mi-8. It flies over the safe area and the winners jump out with parachutes, as from the jump plane | 1,000 m, with a rotor thump you feel more than hear | No |
| Bombers | Fly the [firebombing](#red-zones) strike zone's pass | A pair of jet bombers like the Su-24, low and fast | The siren first, then the jets across the circle | No |
| Robot drop pods | Bring robots to loud heists ([Robot response](#mini-heists)) | No aircraft is seen: the pods fall from high up with a whistle and a smoke trail and land with a thud | 300 m | No |
| [Zhuravl](gameplay.md#vehicles-and-water) | The motor glider, a player vehicle | A two-seat motor glider | Like a vehicle | Like any vehicle |

- **On the map:** the jump plane's path shows before the doors open; cash balloons show like alarms (owner). The other aircraft don't show; you hear them and see where they drop (our pick).
- **One of each (owner, 2026-11-25):** "im assuming since the different planes fly at different levels they can be out at the same time but only one of each?" Each kind flies at its own height, so different kinds can be out at the same time, but never two of the same kind, except the pickup plane: more than one biplane can be out (owner: "we might want more than one biplane is all"), up to 3 (our pick). A drop or balloon that needs a kind already in the sky waits for it to leave. The emergency redeploy shares the pickup planes, so it waits its turn behind cash balloons.
- **Shared flights (owner, 2026-11-25):** "we may need to piggy back the cash drop and vehicle drop on the planes sometimes so that they all get dropped but not at the same point and spot but may need to fly on the same plane". The package plane carries care packages, vehicle drops, and the money drop, and when more than one is due, one flight can carry them together, so none of them waits or gets skipped. Each load drops at its own point along the path. Up to 3 loads a flight, dropped at least 800 m apart, each under its own parachute and smoke, and a match's number of drops stays the same (owner OK'd, 2026-11-25: "that works").
- **Heights (our pick), top to bottom:** the jump plane highest (its exact height is still TBD on [The plane](#the-plane)), the bombers about 600 m, the package plane about 300 m (owner OK'd), the helicopter about 200 m, and the pickup plane about 100 m, low enough to snag a balloon's line.
- **Names and looks:** shapes only, from real aircraft. No maker names, markings, or real designations in the game ([Legal review](../planning/legal-review.md)).

## The zone

The playzone (blue) shrinks toward the next safe circle (white) in phases, and anyone outside the blue takes damage every second. The first map is Erangel's size ([Maps](maps.md)), so PUBG's Erangel phases are placeholders to test in game; our own numbers get tuned from play tests ([PUBG look and feel](../planning/legal-review.md#pubg-look-and-feel)).

| Phase | Wait before shrinking | White circle diameter | Shrink speed | Base damage per second | Ends at (match clock) |
| --- | --- | --- | --- | --- | --- |
| 1 | 2 min (after the plane), then 5 min | 5,100 m | 25.7 m/s | 0.4% | 12:00 |
| 2 | 3 min 20 s | 3,315 m | 12.8 m/s | 0.6% | 17:40 |
| 3 | 2 min 30 s | 1,484 m | 20.3 m/s | 0.8% | 21:40 |
| 4 | 2 min | 742 m | 12.4 m/s | 1% | 24:40 |
| 5 | 2 min | 371 m | 9.3 m/s | 3% | 27:20 |
| 6 | 1 min 30 s | 185 m | 6.2 m/s | 5% | 29:20 |
| 7 | 1 min 30 s | 93 m | 3.1 m/s | 7% | 31:20 |
| 8 | 1 min | 46 m | 1.5 m/s | 9% | 32:50 |
| 9 | 3 min, then a 15 s countdown | Closes completely | — | 11% | Starts closing at 36:05 |

Damage is a percent of full health, so armor doesn't change it.

**Scaled to Teplov (owner, 2026-11-24):** PUBG's first circle is 4,565 m across on Erangel's 8 × 8 km map, about a quarter of its area. Teplov's play area is 10 × 8 km, a quarter bigger, so phases 1 and 2 grow by the same factor (about 1.12) to 5,100 and 3,315 m, and phase 3 on keeps PUBG's sizes. The shrink speeds are worked out from the new sizes: shrink speed is how fast the circle's diameter closes while it shrinks, as on PUBG's table, and the first blue circle starts round the whole 10 × 8 km play area (12.8 km across).

**Circles stay over land (owner OK'd, 2026-11-24):** from phase 4 on, each new white circle's center is on land, and the last circles keep at least about three quarters of their area on land, so a match can't end on open water.

### The edge: how it looks

The owner asked for the wall's look and picked everything here on a picks page (2026-11-24; his answers are on the [Picks archive](../planning/picks-archive.md)):

- **Color: aurora (owner, 2026-11-24):** like northern lights, teal at the bottom shifting to violet at the top, not PUBG's blue ([Legal review](../planning/legal-review.md#pubg-look-and-feel)). It can't be mixed up with the white safe circle or a red strike zone, and no shooter we know of uses it.
- **See-through:** a tall curtain you see through like tinted glass. Players, buildings, and land behind it show, dimmed by about a third. Thin bright lines of static crawl up it.
- **Height:** from the ground and the sea up past the highest hill, fading out about 600 m up, so it shows from a parachute and from the Zhuravl.
- **From far away:** a faint teal and violet band on the horizon from anywhere on the map. The static shows within about 300 m, and you hear it within about 50 m.
- **Moving or not:** while it shrinks, the static sweeps toward the center, so you can tell at a glance that it's moving. Between shrinks it hangs still.
- **Where it cuts through things:** a thin glowing line where it meets the ground, walls, and water. It passes through buildings and rocks and never stops shots, sound, or movement.
- **Inside the edge:** a light teal-to-violet tint and faint grain at the screen's edges, stronger the deeper you are, with a short pulse on each damage tick. How far you can see doesn't change, so a fight across the edge stays fair.
- **Sound:** a low electric hum near it on the safe side. Inside, a dry crackle like a radio between stations, and a soft thump on each damage tick. When a shrink starts, a short low tone plays and the HUD says "The edge is moving".
- **Night and fog:** it glows enough to see across the map at night but doesn't light the ground. In fog it shows through to 500 m, so nobody walks into it blind.
- **The white circle:** the next safe area shows only on the map and minimap, as a thin white ring, never in the world. While you're outside it, a dashed white line on the minimap runs from you to its nearest edge, with the distance. The HUD shows the countdown to the next shrink.

### No zone camping

Damage grows with how deep you are outside the zone and with how far into the match it is, so hiding in the blue to heal or flank doesn't pay. PUBG did this too: since October 2017, every circle after the first hurts more the farther outside you are. PUBG doesn't publish its formula; ours:

```text
damage per second = phase base damage × distance factor
distance factor   = 1 + (meters outside the blue ÷ 100), up to 4 at 300 m
```

- **Match progress:** the phase base climbs from 0.4% to 11% a second, so the same spot hurts far more late.
- **Phase 1 is flat** (factor 1 anywhere), so a bad plane path or a long drive in isn't a death sentence.

Time from full health to dead, with no healing:

| Phase | Just outside | 100 m out | 300 m out |
| --- | --- | --- | --- |
| 1 | 250 s | 250 s | 250 s |
| 3 | 125 s | 63 s | 31 s |
| 5 | 33 s | 17 s | 8 s |
| 8 | 11 s | 6 s | 3 s |

If camping still pays in play tests, the next lever is weaker healing outside the zone.

### Radar stations

Spend scrap at a radar station to see the next circle early. It costs 50 scrap (our pick; [Crafting](crafting.md#what-a-workbench-makes)). Each match puts 5 stations at random spots, and no spot is sure to have one (owner, 2026-11-22). Each station works once: after someone uses it, nobody else can. Robot sentries guard them ([Robot guards](#robot-guards-idea)).

## Red zones

PUBG's red zone, in several forms. One at a time, at a random spot on the map once the match starts, including outside the safe circle. Each one rolls its form:

- **Air raid siren:** before any form starts, an air raid siren sounds over the area through the warning, and the circle shows on the map, so nobody nearby is caught by surprise. It plays from the circle's center and carries through the circle and about 300 m past its edge (owner OK'd, 2026-11-24).

| Form | What happens | How to survive | Odds (our pick) |
| --- | --- | --- | --- |
| **Bombardment** | Like PUBG's red zone: after the warning, shells land at random spots inside the circle. A direct hit kills and destroys vehicles | Get inside a solid building away from doors and windows (wooden houses only take one or two barrages), or leave | 1 in 6 |
| **Smoke** | Thick smoke fills the circle for a while. No damage | Nothing to survive: it hides you, and anyone waiting for you. Good for crossing open ground | 1 in 6 |
| **Firebombing** | Bombers drop incendiaries in a line across the circle, leaving fires that burn for a while and cut off paths | Stay out of the line, or wait for the fires to burn out | 1 in 6 |
| **Creeping barrage** | Shells walk across the circle in a line instead of landing at random, so players can see it coming | Watch which way it walks and get out of its path | 1 in 6 |
| **EMP** | Vehicles stall and electronics stop working inside the circle for a while: drones, scopes with batteries, and radars, like the [EMP grenade](weapon-pool.md#throwables) idea | Leave, or fight on iron sights until it passes | 1 in 6 |
| **Gas** | Gas fills the circle and does damage every second, through armor and indoors | Leave, or put on a [gas mask](class-items.md) | 1 in 6 |

The warning, how long each form lasts, and how far you can see in it are under [Hazards: timing and sight](#hazards-timing-and-sight) (our pick, 2026-11-24). Gas damage starts at 5 health a second (our pick).

**Odds (owner, 2026-11-22):** every form is equally likely, 1 in 6 each.

### Hazards: timing and sight

The owner asked how long each hazard lasts, how it comes and goes, and what you can see in it (2026-11-24). First pass, our pick; the owner OK'd the bombardment, barrage, fire, gas, and shelter rules below (2026-11-24). Every strike zone gives a 20-second warning first (owner, 2026-11-24): the siren sounds and the circle shows on the map.

| Hazard | Comes in | Lasts | Goes | How far you can see in it |
| --- | --- | --- | --- | --- |
| Bombardment | Shells start after the warning | 60 s of shelling | At once | Each shell's dust hides about 10 m around it for 5 s |
| Smoke | 15 s, spreading from the center | 2 min | 30 s | About 10 m inside, thinning over the last 30 m to the circle's edge |
| Firebombing | The bombers' pass takes about 10 s | The fires burn 60 s | Their smoke drifts 20 s more | About 30 m in the smoke downwind of the fires |
| Creeping barrage | Shells start after the warning | The line takes 2 min to cross the circle | At once | A moving wall of dust, about 10 m deep |
| EMP | At once, with a crackle and a flicker | 60 s | At once | Unchanged; scopes with batteries and drones go dark |
| Gas | 20 s, spreading from the center | 2 min, the same as one [gas mask](class-items.md) lasts | 20 s | About 60 m, in a yellow-green haze |
| Smoke grenade | 3 s | 40 s | 10 s | About 2 m inside a cloud about 8 m across. A real M18 smokes for 50 to 90 s; ours is shorter so one grenade covers a crossing or a revive, not a whole fight |
| Inside the edge | — | — | — | Unchanged ([The edge](#the-edge-how-it-looks)) |

**Owner's picks (2026-11-24):** every timing and sight above as suggested, except the warning, which is 20 seconds instead of 30.

**The barrage's dust (owner OK'd, 2026-11-24):** its shells fall in a band about 30 m deep ([Sizes and damage](#hazards-timing-and-sight) below); inside that band the dust hides all but about 10 m, and each shell's dust hangs 5 s, as in a bombardment.

**Sizes and damage (our pick, 2026-11-24, answering the lead; the bigger sizes owner, 2026-11-24):**

| Strike zone | Circle across | Details |
| --- | --- | --- |
| Bombardment | 600 m | 600 shells over the 60 s. A shell kills within 3 m, and its blast falls off to 20 health at 8 m. Someone standing in the open through all of it has about a 1 in 16 chance of a direct hit and about a 1 in 3 chance of being wounded, so staying out in it is a real risk but not certain death |
| Smoke | 600 m | |
| Firebombing | 600 m | One line of fire about 600 m long and 20 m wide across the circle |
| Creeping barrage | 600 m | A band about 30 m deep walking across at 5 m/s, so it crosses in 120 s. That's slower than a sprint (6.3 m/s), so you can outrun it if you see it coming |
| EMP | 600 m | |
| Gas | 400 m | |

- **Bigger, and shrinking with the zone (owner, 2026-11-24):** the sizes above are for phases 1 to 3. They're twice as wide as before, with four times the shells, so a spot in a bombardment is shelled as hard as it was. Gas stays smaller than the rest: at a sprint you get out from the middle in about 32 s, inside the warning and the roll-in. A strike zone is never wider than half the current white circle, so in phase 4 it's about 370 m, with shells and fire cut down in the same proportion. No new strike zones start from phase 5 on, when the white circle is under 400 m.
- **Where they land (owner, 2026-11-24):** the owner remembered them landing in the white circle. PUBG's could land anywhere, even outside the white circle and far from players ([Gamepressure](https://www.gamepressure.com/playerunknowns-battlegrounds/red-zone/zba136)). Ours aim at the fight: 7 times in 10 the center is inside the current white circle, otherwise anywhere in the blue, and never outside the blue.
- **Fire:** standing in firebombing's flames burns like a Molotov or dragon's breath: 10 health a second through armor, and you keep burning 4 seconds after you step out ([Dragon's breath](starting-damage.md)).
- **Gas coming and going:** gas hurts at half its rate while it rolls in and while it thins out, and at the full rate while it holds. It stops when it's gone.
- **Shelter from shells:** for now any solid roof over your head shelters you, doorways and windows included, and wooden houses never give way. Both wait for building materials, when doorways and windows should count as outside for a shell landing within about 5 m.
- **Smoke's look:** thick white-gray banks about 15 to 20 m tall that roll slowly. From outside it looks like a solid wall of smoke; inside you see about 10 m, and it thins over the last 30 m to the edge. At night it's dark gray and catches lamps, flashlights, and flares. It's drawn the same on every setting, like fog ([Fair in the dark](#fair-in-the-dark)).

## Care packages

Random, like PUBG's:

- **When and where:** a plane flies over at random times and drops a crate at a random point along its path. You hear the plane before the drop.
- **The crate** comes down on a parachute and is marked with smoke once it lands. It can land on a roof, in water, or somewhere hard to reach. Our own look and signal, not PUBG's (owner, 2026-11-24, including the green smoke and how long it lasts; the plane, crate, and parachute details owner OK'd, 2026-11-24):
    - **The plane:** a four-engine turboprop cargo plane, like a Soviet An-12, flying low, about 300 m up. You hear its deep drone from about 1.5 km away, loudest straight overhead, so you can tell which way it's going before you see it. A thump and a rush of air when the crate falls out the back.
    - **The crate:** an olive-drab military crate about 1.2 m on each side, with steel corners, stenciled numbers, and no emblems. A small green strobe blinks on top while it falls, so you can follow it against the sky.
    - **Its parachute:** one big round cargo parachute in olive and white panels. It opens a moment after the drop and brings the crate down at about 5 m/s, about a minute from the plane to the ground. It collapses over the crate when it lands.
    - **The smoke:** green signal smoke, starting when it lands and lasting 60 seconds, about as long as a real signal smoke grenade burns (50 to 90 s). Green can't be mixed up with PUBG's red, a red strike zone, or the aurora edge. After the smoke, the strobe keeps blinking until the crate is opened.
- **Inside:** crate weapons with attachments that fit them, tier 3 armor, crate ammo, 1 adrenaline-slot item, and a chance of a med kit ([Crate weapons](../weapons/crate/index.md), [Healing rules](healing.md#rules)).
- **Crate ammo (owner, 2026-11-22):** 20 FRAG-12 or dragon's breath rounds with a shotgun that takes them, and 3 rounds for a lethal launcher. FRAG-12 is strong against vehicles: about 5 hits wreck a car.
- **How many (owner, 2026-11-22):** one per zone phase from phase 2 to 6, about 5 a match.
- **Late phases (owner OK'd, 2026-11-24):** packages are timed by the match clock, so in the short late phases one can land a phase after the one it's counted for. That's fine, but the last one lands before phase 7 starts.
- **Landing early (owner OK'd, 2026-11-24):** a phase early is fine too. A package plane takes about 5 minutes from take-off to a landed crate, so the phase 5 and 6 packages land around phases 4 and 5. What counts is about one package per phase from 2 to 6, all landed before phase 7.
- **Med kit chance (owner OK'd, 2026-11-24):** 30%, about one package in three.
- **Vehicle drops:** 1 or 2 more fly-ins a match drop a special vehicle instead of a crate (owner): armored or special vehicles only, since gliders and the rest spawn normally. For now that's the [Ezh](gameplay.md#vehicles-and-water) armored scout car (owner, 2026-11-22). A vehicle drop can share a flight with a care package or the money drop, each dropped at its own point along the path (owner, 2026-11-25; [Shared flights](#aircraft)).

**Flare gun (idea):** PUBG's later flare gun called a bigger drop when fired straight up inside the safe zone, and an armored car when fired outside it.

**Satellite crashes (idea, later):** a satellite comes down somewhere during the match, with rewards that carry out of the match.

## Moving loot

Loot that moves around the map, like PUBG's loot truck or Apex's train: a supply truck that drives the ring road and can be stopped for what it carries. One supply truck a match (owner, 2026-11-22): hard to stop, and full of guns with attachments, like PUBG's Sanhok loot truck. Trains can do the same on maps with rail.

## Wanted players

Contracts like Warzone's Most Wanted: a player gets marked on the map, and if they survive a set time, their team gets a reward. The reward is scrap only (owner, 2026-11-22); the rest gets worked out later.

## Mini heists

Small themed heists on the map, taking ideas from Payday 2 (owner asked, 2026-11-24): "we can look at payday for like mini themed heist on the map." Payday 2's heists are "get in, get out, get paid": crack something that takes time (a drill that has to be restarted when it stops, thermite through a floor), grab the loot, and get it to the getaway while the police keep coming ([Nintendo Life](https://www.nintendolife.com/news/2018/02/guide_payday_2_heist_tips_-_how_to_grab_loot_escape_and_get_paid), [Payday Wiki: First World Bank](https://payday.fandom.com/wiki/First_World_Bank/Walkthrough)). In a battle royale the police are the other players: a heist is loud, takes time, and pays well, so it pulls a fight to you. The loot goes in the [cash bag](crafting.md#cash) and only counts once it's banked at a drop-off. Nothing is named after Payday; the ideas are generic.

The heists (first pass, our pick, with the owner's calls marked):

| Heist | Where | How it goes | Pays |
| --- | --- | --- | --- |
| Jewelry store | A shop in a big town or town | Smash the display cases (loud glass) and grab what's inside. An alarm rings for 60 s. In and out in under a minute | Valuables |
| Diamond store | Gavansk's main street, one store (owner's idea, 2026-11-25: "we can do a diamond store") | A step up from the jewelry store: smash the front cases for loose stones, then cut the back room's safe in about 30 s with a [cutting torch](crafting.md#what-a-workbench-makes). The alarm rings from the first broken case. Diamonds are tiny and weigh nothing, unlike gold bars (our pick) | The most valuable loot for its size |
| Bank job | Gavansk and Vetrovo's banks | The vault opens with a vault key, quick and quiet, or with a [vault drill](crafting.md#what-a-workbench-makes) made from scrap at a workbench: about 45 seconds, loud, and it stops once and has to be restarted by hand (owner, 2026-11-24: the key or the drill is the trade-off). Robot guards stand inside | The most cash and valuables, including the [gold bars](#gold-bars), and a small chance of a crate weapon |
| Castle museum | Krepost's keep (owner OK, 2026-11-25) | Smash the glass cases for antique silver, medals, and old jewelry, and cut the [paintings](#paintings) out of their frames. One causeway in and out makes it easy to hold and hard to leave | Valuables and paintings |
| Deposit boxes | The post office in each big town | Cut boxes open one at a time with a breaching tool or a [box saw](crafting.md#what-a-workbench-makes) made from scrap, about 5 s each, loud. Each box rolls something | Cash, valuables, quest items, rarely a vault key |
| Armored van | Broken down on a road, rolled each match | Blow the back doors with a breaching charge, or cut them in about 30 s with a [cutting torch](crafting.md#what-a-workbench-makes) made from scrap, then grab what's inside. The van's alarm wails the whole time | Cash and gear: cash sacks and the guards' locker of guns and armor (owner, 2026-11-24) |
| Moving convoy | Later, with vehicles (owner OK, 2026-11-25): an armored van drives the ring road during one zone phase | Stop it by shooting its tires, then open it like the broken-down van. Its alarm starts when it stops | Cash and gear, like the van |
| Farm payroll | The Kolkhoz office (owner OK, 2026-11-25) | The farm's payroll safe: crack it in about 10 s with your built-in tools. Quiet and small, in the middle of nowhere | A little cash |
| Exchange office | A storefront in a big town (name open: PUBG's Payday mode has a heist called The Exchange) | Cash registers ring open; the back-room safe takes about 10 s to crack with your built-in tools | Cash |
| Sealed containers | Gavansk Port's container quay | Several sealed containers can be opened each match (owner, 2026-11-24): cut a seal with your wire cutters in about 5 s and open the doors. Each one rolls its contents, so most hold gear and a few hold the real prize (our pick: 5 a match, 1 or 2 with valuables) | Gear (guns, armor, attachments), sometimes valuables or a crate weapon |

- **Timed to the circle (owner, 2026-11-24):** "we gotta think about the circle with these times too so 90 seconds might be too long." Every heist step stays under a minute (the drill about 45 s, the van about 30 s, a deposit box about 5 s), so a heist fits inside a zone phase's wait even late on: phase 3 waits 2 min 30 s and phase 4 waits 2 min ([The zone](#the-zone)). Early on, a heist is a safe bet; late, one outside the next circle is a gamble against the edge (our pick).
- **How many:** each match rolls 3 or 4 of the big heists to be live (our pick); the rest stay locked and dark. The small scores (ATMs, the courier car, villas, and the farm payroll) are always there. A live heist isn't marked on the map until its alarm goes off, so finding one is part of it.
- **Alarms show on the map (owner, 2026-11-25):** "any sort of heist that shows alarm should show it on the map." While a heist's alarm rings, its spot shows on everyone's map, and the alarm is heard about 300 m away. The loud heists ring: the jewelry and diamond stores, the bank job with a drill, the museum, the deposit boxes, both vans, the police evidence room, ATMs, and the show car. The quiet ones don't: a vault opened with a key, the exchange office's safe, the farm payroll, the sealed containers, the courier car, the yacht safe, the paymaster's safe, and villas (our pick), so a key stays the quiet way in. How long: the drill's and the vans' alarms ring until the heist is done; the others ring 60 s from the last loud thing (our pick).
- **Robot response (owner OK, 2026-11-25):** the big loud heists (the bank job, the diamond store, and the museum, our pick) call robots about 60 s after the alarm starts. They come down in drop pods and climb out, one robot to a pod (owner: "maybe they come down in like a drop pod and climb out, one drop pod one drone kinda deal"). Like the [robot guards](#robot-guards-idea) they're easy to fight but loud, and the pods coming down tell everyone nearby where the heist is. Our pick: 2 pods for the bank, 1 for the others.
- **The drill stopping** is part of the heist, like Payday's: it's a tool, not a gun, so the no-jamming rule doesn't touch it. Drills are made from scrap, never found (owner, 2026-11-24).
- **Getting away:** a drop-off is never right next to a heist, so the loot has to be carried a little way in the open, or sent up in a cash balloon.
- **Cash balloon (owner OK, 2026-11-25):** made from scrap at a [workbench](crafting.md#what-a-workbench-makes): it banks your whole cash bag from anywhere, but everyone can find it, and if it's shot down the bag drops where it falls, for anyone to take. From Warzone's deposit balloons, picked up like the real-world Fulton balloon pickup, where a plane snags the balloon's line in flight ([Wikipedia: Fulton surface-to-air recovery system](https://en.wikipedia.org/wiki/Fulton_surface-to-air_recovery_system)). It was too safe at 50 scrap (owner, 2026-11-25: "maybe we want to up the cost of the cash balloon? that way it cant be spammed? that feels too safe"), so it costs 150, the most of anything at a workbench.
    - **How it goes (owner, 2026-11-25):** "it can show on the map like an alarm but no noise, and it takes a little for the balloon to rise but the noise will be a plane coming to get it". The balloon is silent and shows on everyone's map like an alarm, from the moment it's set up until the plane takes it. It takes a little while to rise, then a plane comes in low to snag it, and the plane is what everyone hears.
    - **Our pick:** it rises in about 15 s, and the plane snags it about 30 s later, so it can be shot down for about 45 s in all; the plane is a small one (owner, 2026-11-25), heard about 1,000 m away ([Aircraft](#aircraft)). Each player can send up one a match.
    - **Someone else's balloon (owner, 2026-11-25):** "make it so it can be either you put your cash in it if its an enemy drop or you can cut the line and take it all, maybe a limit on how many planes?" Anyone who reaches a balloon before the plane can do one of two things: put their own cash in it, so the plane banks theirs too, or cut the line and take the whole bag. Our pick: each player's cash banks to whoever put it in; cutting the line takes about 10 s with the wire cutters everyone carries (owner, 2026-11-25: "it should maybe take 10 seconds to cut the wire?"; [Built-in tools](gameplay.md#built-in-tools)), long enough to get caught at it, and the balloon comes down where it is. Squadmates' balloons work the same way.
    - **A limit on planes out at once (owner, 2026-11-25):** "by limit i mean how many planes out at once." There's no cap on pickups a match, only on planes in the sky together. More than one biplane can be out (owner, 2026-11-25: "we might want more than one biplane is all"); our pick: up to 3 at once. A balloon set up while all 3 are out waits its turn, so it stays up longer, and the wait shows at the workbench and on the balloon.

### Gold bars

The owner, 2026-11-25: gold bars are "extra valuable, those should slow you down but are a big payout." They're the bank vault's top prize and the most valuable loot in the game. They go in the cash bag like other valuables, but they're the one valuable with weight: each bar slows you while you carry it, so a carrier is easy to chase and has to choose between more gold and getting away.

- **How many and how slow (our pick):** 4 bars in each bank vault; each makes you 5% slower, so all four is 20% slower. Banking a bar, or dropping it, takes the slowdown off.
- **Not marked on the map (owner, 2026-11-25):** "you can close the gold carrier on the map thats a no." The bank's alarm already shows where the gold is, and a slowed carrier is easy to find.

### Paintings

The owner's idea, 2026-11-25: "also what about paintings?" Paintings hang in the castle museum, and in a few villas if those are kept (below). Cut one out of its frame in about 5 s with the utility knife every player carries ([Built-in tools](gameplay.md#built-in-tools)), and it rolls up into the cash bag with no weight. Each painting rolls its worth; the museum's best one is the masterpiece, worth about as much as a gold bar (our pick). Cutting is quiet; the museum's alarm comes from its glass cases.

### More ideas

The owner asked for more ("feel free to look through other heist stuff or think of other stuff"; "look at rob run game any other heistables?"). These borrow from other games, always under our own names:

- **Warzone's Plunder:** cash from loot, bank vaults whose alarms alert nearby squads, deposit balloons that can be shot down, and players dropping cash on death ([Activision: Plunder](https://blog.activision.com/call-of-duty/2020-03/Warzone-Mode-Recon-Plunder)).
- **Fortnite's Getaway:** jewels in slow safes, the carrier revealed for 30 seconds ([Mein-MMO: Getaway](https://mein-mmo.de/en/fortnite-neue-spielmodus-flucht,266716)).
- **ROB RUN** (PC, 2026), set in a city called Looty Bay. Its gold vault opens with a slow, loud drill that alerts the whole city, and there's a police station armory of confiscated gear, an exhibition car at a hotel, and an art gallery robbed with a glass cutter and a vault keycard. ATMs and car trunks hold smaller scores. Every heist is announced to the whole city when it starts and when it succeeds ([Wikily: ROB RUN heists](https://wikily.gg/rob-run/heists), [PowerUp Gaming: beginner guide](https://powerupgaming.co.uk/2026/11/05/rob-run-beginner-guide-survive-your-first-hour/)).
- **PUBG's own PvE Payday mode** of May 2026 had Diamond District, The Exchange, Nightclub, and Road Rage, on its own map ([PUBG: New Mode: PAYDAY](https://pubg.com/news/10009)). Our diamond store keeps its plain name, never "Diamond District".

Kept (owner, 2026-11-25: "i like your eight ideas"; the details are our pick):

| Idea | What it is |
| --- | --- |
| Police evidence room | Each big town's police station keeps confiscated guns and armor behind a cage: cut it in about 20 s with a cutting torch, and its alarm rings. Pays gear, sometimes a crate weapon. From ROB RUN's police armory |
| ATMs | Cash machines on town streets: blow one open with a breaching charge for a small stack of cash. Loud, with an alarm. Many small scores instead of one big one. From ROB RUN |
| Courier car | A parked car, rolled each match, with a locked case in the trunk: pry the trunk open and crack the case in about 10 s. Quiet. From ROB RUN's trunk cargo |
| Show car | Later, with vehicles: a rare car on display in the Sanatorium's main hall. Break the glass and drive it out; leaving it at a drop-off banks it as a big payout. From ROB RUN's exhibition car |
| Yacht safe | A yacht moored at Marina's pier with its owner's wall safe and a painting or two, reached only from the pier or the water |
| Paymaster's safe | Object 7's headquarters keeps the base's payroll. Quiet, but deep inside the fence and towers |
| Villas | A few hillside villas with a wall safe and paintings, the safe opened with a [box saw](crafting.md#what-a-workbench-makes) |
| Money drop | A match event like the care package: a plane drops a crate of cash and valuables, with its own smoke color. Everyone sees it fall |

Still open (our picks, 2026-11-24, for the owner's review):

| Idea | What it is |
| --- | --- |
| Tip-offs | Notes found as loot that mark one live heist on your map, like Payday's intel |
| Ferry strongroom | The ferry at Gavansk's ferry quay has a purser's strongroom: a safe and the passengers' valuables lockers |

- **The map needs** these places in the building kit: a jewelry store, a diamond store, a bank interior with a vault, the castle museum in Krepost's keep, a post office with deposit boxes, the Kolkhoz office, an exchange office, the armored van, the sealed containers, a police evidence room in each big town's police station, ATMs, the Sanatorium's show car hall, a yacht at Marina, the paymaster's office at Object 7, and a few hillside villas; and the ferry, if its strongroom is kept ([Buildings](maps.md)).

## Vaults and keys

Apex Legends added locked vaults to World's Edge in 2019. Keys came from roaming cargo drones; holding one marked every vault on your map; opening took 3 seconds, and the doors stayed open for anyone after. Vaults held top-tier armor, backpacks, attachments, and heals, but no weapons or ammo.

Ours:

- **Vaults:** 4 to 6 per map, spread out. On the first map, five: one under the Military Outpost, one in each big town (Ischia Porto and Forio), one on the coast (Marina's waterfront), and the Prison armory ([Maps](maps.md#marina-farms-and-vaults)).
- **Keys:** only 2 or 3 per match, spawning at random, so most vaults stay shut in any given match.
- **Opening:** 3 seconds with a key. The key is used up, the door stays open, and an alarm sounds nearby, so others know.
- **Or drill it (owner, 2026-11-24):** "we use scrap to make the drills for a vault heist. or you have a key thats the trade off." A [vault drill](crafting.md#what-a-workbench-makes) made from 100 scrap at a workbench opens any vault without a key, in about 45 seconds of noise, stopping once to be restarted, so every vault can be a heist.
- **Inside:** like Apex, no weapons: tier 3 armor and helmets, the best backpacks, scopes, and mag tiers, meds, and throwables. Crate weapons stay crate-only.

**How keys work:**

- **One key fits all:** any key opens any vault, and holding one shows every vault on your map, like Apex. Without a key, the map, the full map on M included, doesn't mark them, like PUBG's secret rooms (planner, 2026-11-23).
- **Used up:** opening a vault removes the key from your inventory.
- **Dropped on death:** a key drops with your loot, so a key holder is worth hunting.
- **Where they spawn:** anywhere loot spawns. When the match starts, it rolls how many keys there are (2 or 3) and spreads them across the map, never near each other (at least 2 km apart, our pick).
- **Away from the vaults:** a key lands in the same named place as a vault only about 1% of the time, so a place like the Farm is more likely to hold a key than the Prison is. Finding the key and reaching a vault are two separate trips.
- **Care packages:** a 5% chance of a key per package, on top of the ground keys, to tune later.

### Robot guards (idea)

PvE for the vaults (owner, 2026-11-22): a robot guard inside each vault, from the [robot concept](../planning/idea-inbox.md#robot-character-concept). PUBG's Haven map (2020) had an AI faction, Pillar, whose guards and commanders protected supply caches.

- **Easy to fight:** a few hits take one down, it turns slowly, and its aim is poor (our pick). It's no threat to a squad that's ready.
- **A noise maker:** when it sees or hears a player it calls out and fires, so everyone nearby knows someone is at the vault, like Hunt: Showdown's crows ([Tracks and animals](gameplay.md#tracks-and-animals)).
- **Loot:** nothing of its own (our pick); the vault is the prize.
- **More PvE (owner, 2026-11-22):** robot sentries at the [radar stations](#radar-stations), and robot patrols too, like ones guarding a loot room at the Military Outpost.
- **Drop pods (owner, 2026-11-25):** robots called to a loud heist come down in drop pods and climb out, one robot to a pod ([Robot response](#mini-heists)).

**Later:** a drill that opens any vault in about 45 seconds, but loudly. It's an expensive item at [workbenches](crafting.md#what-a-workbench-makes).

## Time of day and weather

### Time passes

Every match rolls a time of day, and the sky moves through it, about four in-game hours over the match (our pick):

| Match | Clock | Odds (our pick) |
| --- | --- | --- |
| Day | 10:00 to 14:00 | 50% |
| Late day into night | 17:30 to 21:30 | 20% |
| Night | 23:00 to 03:00 | 15% |
| Night into morning | 03:30 to 07:30 | 15% |

**The sun (owner OK'd, 2026-11-24):** the sky follows Ischia's sun on June 1, in summer time (UTC+2): sunrise at 05:35, sunset at 20:28, and highest at 13:01, about 71° up. First light (civil dawn) is at 05:02 and full dark (civil dusk) at 21:00, so both dusk and dawn matches cross from light to dark. Worked out from NOAA's sun equations for 40.7° N, 13.9° E, and close to Gaisma's Naples table (05:31 and 20:38 at the June solstice).

Night is where flashlights, night scopes like the StG 44's Vampir, and star rounds earn their place ([Maps](maps.md)). A dark match needs rules against brightness and gamma cheats, which PUBG's developers raised when they prototyped night in 2017 ([Fair in the dark](#fair-in-the-dark)).

- **Moonlight (owner OK'd, 2026-11-24):** every night is a bright moonlit night. In the open you can make out a standing player to about 100 m without a night scope; inside buildings it's dark enough to need a light.

#### Night look

Night uses day for night, the film trick: the same scene shot darker with a cool blue tint, rather than a real night that a screen shows as black (owner OK'd, 2026-11-24). It's the night version of the [Lighting look](../planning/art-and-sound.md#lighting-look) rule that shade is never black. First pass for the lead, to tune by eye:

| What | Night look (our pick) |
| --- | --- |
| Exposure | Locked at night (Min equal to Max EV100), set from the server's time of day; it blends to the day range over dusk and dawn |
| Moonlit open ground | A dark blue-gray, about 20 to 25% brightness on screen |
| Shade and the far side of buildings | About half that, around 10%, never black |
| Inside buildings | Dark enough to want a light, but door frames, windows, and a standing player's outline still show against them |
| Lights | Lamps, flashlights, muzzle flashes, and fires stand out clearly, so a light gives you away |
| Color | Cool and low in saturation; the blue tint is in the grade, not the sky light alone |

**The check:** in the open, a standing player is easy to make out at about 100 m without a night scope (see Moonlight above). If the owner can't, night is too dark.

#### Fair in the dark

Night and fog are drawn on each player's own machine, so a cheat or a setting could turn them off. The rules (owner OK'd, 2026-11-24):

1. **Same picture on every setting.** No graphics setting turns off or thins fog, night darkness, the grade, shadows, or the grass and bushes near players. In 2017 PUBG's players ran low settings because some foliage didn't show there, and PUBG raised shadows to 450 m on Low to keep low and high fair. Settings only change how sharp things look.
2. **No gamma slider or filters.** Only a small brightness range for setting up the screen. Nvidia's game filters aren't supported, as in ARC Raiders, where they could turn dark rooms close to gray. Programs that inject their own color tables, like DWM_lut, are banned, as Escape from Tarkov did.
3. **The server sets the look.** The time of day, weather, fog distance, and night exposure come from the server each match, never from the player's files. Shipping builds have no console, config files are packed into the game and not read from the player's Saved folder, pak files are signed, and Easy Anti-Cheat checks the game's files ([Later](../planning/to-do.md#later)). Unreal lets a loose config file override packed values unless the build is set up against it, so the lead checks this when packaging.
4. **No positions behind thick fog.** While fog is thicker than 250 m, the server doesn't send a player's position to anyone more than twice the current fog distance away, so a fog-removal cheat has nothing to show. Their sounds still go out by the normal hearing rules. This doesn't apply at night, where scopes and lights see farther.
5. **Moonlit, not pitch black.** A monitor's own settings can't be stopped, so night is never so dark that turning up the monitor wins fights.

### Weather

Clear, overcast, rain, fog, and thunderstorms, and weather can change during a match:

- **Rain** adds noise that covers footsteps a little.
- **Fog** shortens sight lines, which helps SMGs and shotguns and hurts snipers.
- **Thunder** can briefly cover gunshots, which matters in a game built around sound ([Gameplay](gameplay.md#sound)).
- **Wind** doesn't move bullets, to keep shooting simple.

First-pass numbers (our pick):

| Weather | When | What it does |
| --- | --- | --- |
| Clear | 60% of matches start clear | Full sun, sharp shadows |
| Overcast | 40% start overcast | Sunlight about half as bright, soft shadows |
| Rain | 50% of heavy spells | Footsteps carry 25% less far |
| Fog | 30% of heavy spells | Sight closes in from 1,000 m to about 150 m at its thickest |
| Thunderstorm | 20% of heavy spells | Rain, plus a lightning strike every 20 to 60 seconds; each rumble lasts about 3 seconds and halves how far gunshots carry. Lightning lights up a night match for a moment |

- **Heavy spells:** one match in three gets one, at a random time in zone phases 2 to 5. Each one gives a warning, rolls in, holds, and clears, so nobody is caught by a wall of fog all at once (owner asked, 2026-11-24; numbers owner OK'd, 2026-11-24):

| Spell | Warning | Rolls in | Holds | Clears |
| --- | --- | --- | --- | --- |
| Rain | The light flattens and the clouds darken for 60 s | 90 s, from drizzle to full rain | 4 to 8 min | 90 s; puddles and wet shine stay 2 min more |
| Fog | Mist gathers in the valleys and over the sea for 60 s | 2 min | 3 to 6 min | 2 min |
| Thunderstorm | Distant thunder with no rain for 60 s | 2 min: wind and dark clouds, then heavy rain | 5 to 8 min | 90 s; puddles and wet shine stay 2 min more |

#### How far you can see

How far you can make out a standing player in the open (our pick, 2026-11-24). Players draw out to 1 km in every weather, so the weather sets the limit, not the draw distance.

| Condition | Sight | How it looks |
| --- | --- | --- |
| Clear | 1 km | A light haze past 1.5 km |
| Overcast | 1 km | Flat light, haze past 1 km |
| Rain | 600 m at full rain | A gray veil from 300 m, wet shine on the ground |
| Thunderstorm | 400 m in the downpour | A heavy veil from 200 m; each lightning flash lights everything for about a fifth of a second |
| Fog | 150 m at its thickest, closing in from 1,000 m as it rolls in | White-gray from 60 m, flat light, no shadows |
| Dusk and dawn | 300 m from sunset to full dark (20:28 to 21:00), and from first light to sunrise (05:02 to 05:35). Each is about 5 real minutes (owner OK'd, 2026-11-24) | Low sun glare in one direction, long shadows |
| Moonlit night | 100 m from full dark to first light ([Moonlight](#time-passes)) | Lamps, flashlights, muzzle flashes, and fires show from 1 km; a night scope sees about 300 m |
| Night with rain, fog, or a storm | The shorter of the two | |

**Owner's picks (2026-11-24):** every spell, sight, and dusk choice as suggested.

- **The warning:** the sky and the light change about 15% of the way, but no rain falls and sight doesn't shrink until the spell rolls in. A fog warning's mist lies only in valleys and over the sea (owner OK'd, 2026-11-24). For now the low height fog thickening is enough, since it collects low anyway; true valley-only mist waits for an art effect.
- **When a spell can run (owner OK'd, 2026-11-24):** it starts in phases 2 to 5 and can run past phase 5, but it has cleared before phase 7 starts, shortening its hold if it must, so the last circles are fought in normal sight.
- **The spell's clock (owner OK'd, 2026-11-24):** "starts" means the warning starts. A storm clears with the thunder moving away, and leaves the same 2 minutes of puddles and wet shine as rain.
- **Distant thunder (owner OK'd, 2026-11-24):** only the storm's own thunder halves how far gunshots carry. The distant rumble of its warning doesn't.
- **Rain and vehicles (owner, 2026-11-24):** rain changes how vehicles handle. Our numbers: on wet roads tires grip about 20% less and braking takes about 30% longer; on wet dirt and grass, grip drops about 35%. It lasts while it rains and 2 minutes after, while the ground is still wet. Thunderstorms count as rain ([Vehicles and water](gameplay.md#vehicles-and-water)).

For scale, weather services call fog with about 200 m of sight thick fog, and under 50 m dense fog. Gas and smoke are under [Hazards: timing and sight](#hazards-timing-and-sight).

**PUBG's lesson:** in 2017, an Erangel match could be cloudy, clear, sunset, rainy, or foggy. In January 2018, PUBG removed rain and fog because too many players quit those matches. Weather came back in August 2019 as dynamic weather that changes during a round. So no match starts in thick fog: heavy weather rolls in and clears during the match.

## Wrist watch

Every player wears a watch on the left wrist, visible in first person whenever the left hand is on the gun, like Modern Warfare's. Modern Warfare's (2019) read the time from your console or PC; ours shows the in-game time, so you can tell when night is coming without the HUD. The default face is analog (owner OK'd, 2026-11-24), and digital faces can come as skins. Every face shows only the in-game time, never the zone timer, so a watch skin never gives an edge. It sits on the inside of the left wrist, military style, so the face points up at you while the support hand is palm-up under the handguard (owner OK'd, 2026-11-24). On the back of the wrist it would face the ground. Watch faces can be skins later ([Skins and mastery](skins.md)).

## Sources

- [PUBG fandom wiki: Blue Zone](https://pubg.fandom.com/wiki/Blue_Zone) (Erangel phases, distance-based damage)
- [The Loadout: Sanhok loot truck](https://www.theloadout.com/pubg/sanhok-loot-truck) · [Activision: Most Wanted](https://blog.activision.com/call-of-duty/2020-04/Call-of-Duty-Warzone-Contracts-Most-Wanted)
- [Gaisma: Naples sun times](https://www.gaisma.com/en/location/naples.html) · [All Things How: ARC Raiders blocks Nvidia game filters](https://allthings.how/arc-raiders-has-blocked-nvidia-game-filters-what-that-means-and-what-you-can-do/) · [Insider Gaming: Tarkov devs block filters](https://insider-gaming.com/tarkov-devs-block-filters/)
- [PUBG fandom wiki: Parachute](https://pubg.fandom.com/wiki/Parachute) · [PC Gamer: How to land fast in PUBG](https://www.pcgamer.com/pubg-how-to-land-fast-battlegrounds)
- [Gamepressure: PUBG red zone](https://www.gamepressure.com/playerunknowns-battlegrounds/red-zone/zba136) · [PUBG support: What is the red zone?](https://support.pubg.com/hc/en-us/articles/115004198974-What-is-the-red-zone) · [Samurai Gamers: PUBG battle area](https://samurai-gamers.com/playerunknowns-battlegrounds-pubg/pubg-battle-area-intro/)
- [PUBG Wiki: Airdrop](https://pubg.wiki.gg/wiki/Airdrop)
- [PC Gamer: Apex Legends vault keys (2019)](https://www.pcgamer.com/how-to-open-apex-legends-vaults-locations-key) · [GameSpot: Apex Legends vaults](https://www.gamespot.com/articles/apex-legends-golden-vaults-where-to-find-keys-and-/1100-6470435/) · [Apex Legends Wiki: Vault Key](https://apexlegends.wiki.gg/wiki/Vault_Key)
- [Met Office: How fog affects travel](https://weather.metoffice.gov.uk/warnings-and-advice/seasonal-advice/travel/how-fog-affects-travel) (thick fog about 200 m, dense fog under 50 m) · [FAS: M18 colored smoke grenade](https://man.fas.org/dod-101/sys/land/m18.htm) (50 to 90 seconds of smoke)
- [PUBG fandom wiki: Blue Zone](https://pubg.fandom.com/wiki/Blue_Zone) (Erangel's phases) · [Gamepressure: Red zone](https://www.gamepressure.com/playerunknowns-battlegrounds/red-zone/zba136) · [PUBG Wiki: Airdrop](https://pubg.wiki.gg/wiki/Airdrop) (the C-130's sound, the parachute, the flashing light, and the red smoke)
- [PUBG Wiki: Weather](https://pubg.wiki.gg/wiki/Weather) · [Thumbsticks: PUBG removes rain and fog (2018)](https://www.thumbsticks.com/pubg-lost-rain-fog-conditions-01032018/)
- [Wikipedia: Day for night](https://en.wikipedia.org/wiki/Day_for_night) · [Player.One: PlayerUnknown on parity between low and high settings (2017)](https://www.player.one/playerunknown-interview-parity-low-high-graphics-battlegrounds-121445) · [PC Gamer: PUBG settings guide](https://www.pcgamer.com/best-pubg-settings/) · [Unreal forums: stopping players changing ini files](https://forums.unrealengine.com/t/can-we-prevent-users-from-changing-ini-config-files/467236)
- [Charlie Intel: Modern Warfare watches show real-world time](https://www.charlieintel.com/modern-warfare/watches-in-game-in-call-of-duty-modern-warfare-showcase-real-world-time-55492/)
