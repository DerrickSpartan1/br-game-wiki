# Match flow

How a match runs, from the plane to the last circle: the plane and parachutes, the zone, zone events, care packages, vaults, time of day and weather, and the wrist watch. PUBG's 2017–2018 match is the base. Numbers marked "our pick" are first passes to tune in play testing; TBD numbers aren't set yet.

## The plane

- **Random path:** every match, the plane flies a straight line across the map between two random edges, like PUBG. The path shows on the map before the doors open.
- **Jumping:** jump any time along the path. Anyone still aboard is pushed out near the end.
- **Squads:** teammates can follow one player's jump and land together (our pick).
- **Altitude and speed:** TBD.

## Parachutes

Like PUBG, in third person, the one part of the game that is ([Gameplay](gameplay.md)).

- **Freefall:** up to about 126 km/h forward, or about 232 km/h diving straight down.
- **Opening:** the chute opens on its own at a set height above the ground, earlier over high ground. You can open it sooner by hand.
- **Under the canopy:** about 18 to 27 km/h forward, and up to about 64 km/h spiralling down.
- **Distance vs. speed:** opening the chute at the first chance covers the most ground; diving straight at a close target lands first. Both work like PUBG's.

## The zone

The playzone (blue) shrinks toward the next safe circle (white) in phases, and anyone outside the blue takes damage every second. The first map is Erangel's size ([Maps](maps.md)), so PUBG's Erangel phases are the first pass.

| Phase | Wait before shrinking | White circle diameter | Shrink speed | Base damage per second | Ends at (match clock) |
| --- | --- | --- | --- | --- | --- |
| 1 | 2 min (after the plane), then 5 min | 4,565 m | 22.8 m/s | 0.4% | 12:00 |
| 2 | 3 min 20 s | 2,967 m | 11.4 m/s | 0.6% | 17:40 |
| 3 | 2 min 30 s | 1,484 m | 16.5 m/s | 0.8% | 21:40 |
| 4 | 2 min | 742 m | 12.4 m/s | 1% | 24:40 |
| 5 | 2 min | 371 m | 9.3 m/s | 3% | 27:20 |
| 6 | 1 min 30 s | 185 m | 6.2 m/s | 5% | 29:20 |
| 7 | 1 min 30 s | 93 m | 3.1 m/s | 7% | 31:20 |
| 8 | 1 min | 46 m | 1.5 m/s | 9% | 32:50 |
| 9 | 3 min, then a 15 s countdown | Closes completely | — | 11% | Starts closing at 36:05 |

Damage is a percent of full health, so armor doesn't change it.

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

## Zone events

PUBG's red zone, plus variants. One event at a time, at a random spot on the map once the match starts, including outside the safe circle. Each event rolls its type:

| Event | What happens | How to survive | Odds (our pick) |
| --- | --- | --- | --- |
| **Red zone** | Like PUBG's: the circle shows on the map, and after a short warning, shells land at random spots inside it. A direct hit kills and destroys vehicles | Get inside a solid building away from doors and windows (wooden houses only take one or two barrages), or leave | 60% |
| **Smoke zone** | Thick smoke fills the circle for a while. No damage | Nothing to survive: it hides you, and anyone waiting for you. Good for crossing open ground | 25% |
| **Poison zone** | Gas fills the circle and does damage every second, through armor and indoors | Leave. Gas masks are an idea ([Class items](class-items.md)) | 15% |

The circle's size, warning time, and how long each event lasts are TBD. Poison damage starts at 5 health a second (our pick).

## Care packages

Random, like PUBG's:

- **When and where:** a plane flies over at random times and drops a crate at a random point along its path. You hear the plane before the drop.
- **The crate** comes down on a parachute with a flashing light, and red smoke marks it once it lands. It can land on a roof, in water, or somewhere hard to reach.
- **Inside:** crate weapons with attachments that fit them, tier 3 armor, and crate ammo ([Crate weapons](../weapons/crate/index.md)).
- **How many:** TBD.

**Flare gun (idea):** PUBG's later flare gun called a bigger drop when fired straight up inside the safe zone, and an armored car when fired outside it.

## Vaults and keys

Apex Legends added locked vaults to World's Edge in 2019. Keys came from roaming cargo drones; holding one marked every vault on your map; opening took 3 seconds, and the doors stayed open for anyone after. Vaults held top-tier armor, backpacks, attachments, and heals, but no weapons or ammo.

Ours:

- **Vaults:** 4 to 6 per map, spread out. On the first map: one under the Military Outpost, one in each big town (Ischia Porto and Forio), and one on the coast (Marina's waterfront); the Prison armory is a suggested fifth ([Maps](maps.md#marina-farms-and-vaults)).
- **Keys:** only 2 or 3 per match, spawning at random, so most vaults stay shut in any given match.
- **Opening:** 3 seconds. The key is used up, the door stays open, and an alarm sounds nearby, so others know.
- **Inside:** like Apex, no weapons: tier 3 armor and helmets, the best backpacks, scopes, and mag tiers, meds, and throwables. Crate weapons stay crate-only.

**How keys could work (first pass, for review):**

- **One kind of key:** any key opens any vault once, and holding one shows every vault on your map, like Apex.
- **Where they spawn:** each match picks 2 or 3 spots at random from a longer list of possible key spots (desks, lockers, and safes in offices, the Hospital, the Port, the Prison, and similar), at least 2 km apart. Players learn the likely places but can't farm one spot.
- **Dropped on death:** a key drops with your loot, so a key holder is worth hunting.

**Other ideas, not decided:** keys that each open only one named vault; a drill that opens any vault in about 45 seconds but loudly; or one key in a care package instead of on the ground.

## Time of day and weather

### Time passes

Every match rolls a time of day, and the sky moves through it, about four in-game hours over the match (our pick):

| Match | Clock | Odds (our pick) |
| --- | --- | --- |
| Day | 10:00 to 14:00 | 50% |
| Late day into night | 17:30 to 21:30 | 20% |
| Night | 23:00 to 03:00 | 15% |
| Night into morning | 03:30 to 07:30 | 15% |

Night is where flashlights, night scopes like the StG 44's Vampir, and star rounds earn their place ([Maps](maps.md)). A dark match needs rules against brightness and gamma cheats, which PUBG's developers raised when they prototyped night in 2017.

### Weather

Clear, overcast, rain, fog, and thunderstorms, and weather can change during a match:

- **Rain** adds noise that covers footsteps a little.
- **Fog** shortens sight lines, which helps SMGs and shotguns and hurts snipers.
- **Thunder** can briefly cover gunshots, which matters in a game built around sound ([Gameplay](gameplay.md#sound)).
- **Wind** doesn't move bullets, to keep shooting simple.

**PUBG's lesson:** in 2017, an Erangel match could be cloudy, clear, sunset, rainy, or foggy. In January 2018, PUBG removed rain and fog because too many players quit those matches. Weather came back in August 2019 as dynamic weather that changes during a round. So no match starts in thick fog: heavy weather rolls in and clears during the match.

## Wrist watch

Every player wears a watch on the left wrist, visible in first person whenever the left hand is on the gun, like Modern Warfare's. Modern Warfare's (2019) read the time from your console or PC; ours shows the in-game time, so you can tell when night is coming without the HUD. Whether a digital face also shows the zone timer is TBD. Watch faces can be skins later ([Skins and mastery](skins.md)).

## Sources

- [PUBG fandom wiki: Blue Zone](https://pubg.fandom.com/wiki/Blue_Zone) (Erangel phases, distance-based damage)
- [PUBG fandom wiki: Parachute](https://pubg.fandom.com/wiki/Parachute) · [PC Gamer: How to land fast in PUBG](https://www.pcgamer.com/pubg-how-to-land-fast-battlegrounds)
- [Gamepressure: PUBG red zone](https://www.gamepressure.com/playerunknowns-battlegrounds/red-zone/zba136) · [PUBG support: What is the red zone?](https://support.pubg.com/hc/en-us/articles/115004198974-What-is-the-red-zone) · [Samurai Gamers: PUBG battle area](https://samurai-gamers.com/playerunknowns-battlegrounds-pubg/pubg-battle-area-intro/)
- [PUBG Wiki: Airdrop](https://pubg.wiki.gg/wiki/Airdrop)
- [PC Gamer: Apex Legends vault keys (2019)](https://www.pcgamer.com/how-to-open-apex-legends-vaults-locations-key) · [GameSpot: Apex Legends vaults](https://www.gamespot.com/articles/apex-legends-golden-vaults-where-to-find-keys-and-/1100-6470435/) · [Apex Legends Wiki: Vault Key](https://apexlegends.wiki.gg/wiki/Vault_Key)
- [PUBG Wiki: Weather](https://pubg.wiki.gg/wiki/Weather) · [Thumbsticks: PUBG removes rain and fog (2018)](https://www.thumbsticks.com/pubg-lost-rain-fog-conditions-01032018/)
- [Charlie Intel: Modern Warfare watches show real-world time](https://www.charlieintel.com/modern-warfare/watches-in-game-in-call-of-duty-modern-warfare-showcase-real-world-time-55492/)
