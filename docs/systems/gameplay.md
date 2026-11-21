# Gameplay and mechanics

Matches favor scavenging and a slower pace over fast action, in a classic battle royale format.

- **Camera:** the game is played in first person, including driving. Parachuting is the only third-person part.
- **Hit zones:** six zones: head, neck, chest and stomach (one zone), groin, arms, and legs, with no lucky one-shots ([Hit zones](ttk.md#hit-zones)).
- **Handling:** spread, ready and ADS times, reloads, and movement speed per category are on [Handling](handling.md).

## HUD and inventory

The layout follows PUBG's from 2017 and 2018, with the game's own look (no PUBG art, icons, or fonts). The mockup is a private Design artifact in the owner's Claude account.

- **Weapon slots:** 1 and 2 hold primaries, 3 is the pistol / 3rd slot ([Rules](../rules.md#3rd-slot)), 4 holds a [class item](class-items.md), and 5 holds a throwable. Melee has its own button instead of a slot.
- **HUD:** a compass at the top with the heading in yellow; players alive and kills at the top right; the crosshair; health, boost, stance, gear durability, ammo, and fire mode at the bottom center; the five slots as weapon silhouettes beside the minimap at the bottom right.
- **Picking up:** look at an item and press F, like PUBG. The prompt names a gun's rolled version, since every gun is one version for the match ([Rules](../rules.md#versions)).
- **Keys:** PUBG's defaults: WASD to move, Shift sprint, Ctrl walk, C crouch, Z prone, Space jump and vault, = auto-run, Alt free look, V perspective, F interact, Tab inventory, left mouse fire, right mouse aim (tap to toggle, hold to hold), R reload, B fire mode, Q and E peek, middle mouse to ping, and 1 to 5 for the slots. The one change is X, which is melee: tap X to bring out the melee weapon, and hold X to stow your weapon and run faster.
- **Ping:** middle mouse marks enemies, loot, and places for your squad, and means different things depending on what you aim at, like Apex's.
- **Inventory (Tab):** vicinity, backpack, gear (helmet, vest, backpack, and outfit slots for skins), and the weapons with their attachment slots. Hovering a gun shows its version: cartridge, fire modes, rate, and mag. You can still move with it open.

## Knockdowns & revives

1. At zero health you're knocked down. You can crawl, but you leave a blood trail.
2. A teammate can pick you up while you're knocked. This is slow without an adrenaline shot.
3. If you bleed out, you can still be revived with a defib, or slowly with CPR.

**Self-revive kits** let you get up on your own, like PUBG's. They spawn more often in solos and less often in duos, trios, and quads.

**Adrenaline shots** are rarer and have two uses: a quick pickup, or maybe a heal like PUBG's adrenaline (replacing the infinite-stamina idea, since original PUBG had no stamina). You don't need one in your hands to use it.

## Comeback fight

When your whole team is wiped out, you're sent to a loser fight as a comeback play. It's a random team fight where players get random weapons, and the format varies:

- A 4v4
- Two 2v2s played side by side
- A 3v3 and a 1v1 played side by side
- Other mixes

Winners redeploy into the main match with the guns and armor they had in the team fight.

**Not final:** the owner wants some kind of Gulag-style comeback, like Warzone's, but isn't sure of the form yet.

**Jailbreak (rare event):** in duos, trios, and quads only, a rare event brings every eliminated player back into the match at once, like Warzone's Jailbreak.

## Vehicles

Cars, boats, and other water vehicles, plus ziplines as part of the map. Trains could run on maps with rail, and a gondola could carry players up a mountain on a future map.

## Tracks and animals

- **Footprints** show in snow, mud, and similar ground, and **tire tracks** show where vehicles went.
- **Animals that give you away (idea, to refine):** birds in trees and on buildings fly off when players get close, like Hunt: Showdown's crows, so a flock taking off tells others someone's there.

## Buildings & materials

Buildings are semi-destructible, kept simple: doors, windows, and specific walls can break. Materials matter too.

Wire fences (possibility): drive straight through them like PUBG, or cut a gap quietly for a stealthier approach. Wire cutters could be a melee item that cuts fences, and the Galil ARM's bipod wire cutter could do the same.

- Wood can be shot through.
- Thin metal can be shot through by some weapons.

## Match setup

- **Modes:** solos, duos, trios, and quads.
- **Player count:** set by each map's size; 100 on the first map ([Maps](maps.md)).
- **Zone:** works like PUBG's, with damage that grows the deeper outside you are, so zone camping doesn't pay ([Match flow](match-flow.md#the-zone)).
- **Zone events:** PUBG's red zone, plus smoke and poison zones ([Match flow](match-flow.md#zone-events)).
- **Plane and parachutes:** a random plane path and PUBG-style parachutes ([Match flow](match-flow.md#the-plane)).
- **Crates:** arrive by air drop at random ([Match flow](match-flow.md#care-packages)).
- **Vaults:** locked vaults opened with rare keys, like Apex's ([Match flow](match-flow.md#vaults-and-keys)).
- **Time and weather:** time passes during a match, from day into night or night into morning, and weather can change ([Match flow](match-flow.md#time-of-day-and-weather)).
- **Wrist watch:** always on the left wrist, showing the in-game time ([Match flow](match-flow.md#wrist-watch)).
- **Hot loot zones:** yes.

## Sound

Sound is a major focus.

- **Real sound travel:** sound moves at its real speed, about 343 m/s, so a shot 300 m away is heard almost a second after it's fired.
- **Bullet crack:** bullets still faster than sound crack as they fly past you. The crack lands before the bang, so the gap between them hints at how far away the shooter is. Subsonic rounds, like .45 ACP and the [VSS](../weapons/battle-rifles/vss.md)'s 9×39mm, don't crack.

- **Proximity chat:** nearby players, enemies included, can hear each other talk, like PUBG.

How gun sounds are layered and sourced is on [Gun art and sound](../planning/art-and-sound.md#sound).

## Death cam and replays

- **Death cam:** after you die, see the moment from the shooter's view, like PUBG's.
- **Replays:** matches can be watched back afterward. Both help players learn and help spot cheaters.

## Anti-cheat

Cheaters are a real problem. The game uses Easy Anti-Cheat, free through Epic Online Services; it gets wired in later in the build ([Getting started](../planning/getting-started.md)).
