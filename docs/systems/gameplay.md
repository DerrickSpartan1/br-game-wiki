# Gameplay and mechanics

Matches favor scavenging and a slower pace over fast action, in a classic battle royale format.

- **Camera:** the game is played in first person, including driving. Parachuting is the only third-person part.
- **Hit zones:** damage differs across four zones: head, chest and stomach (one zone), arms, and legs.

## HUD and inventory

The layout follows PUBG's from 2017 and 2018, with the game's own look (no PUBG art, icons, or fonts). The mockup is a private Design artifact in the owner's Claude account.

- **Weapon slots:** 1 and 2 hold primaries, 3 is the pistol / 3rd slot ([Rules](../rules.md#3rd-slot)), 4 holds a [class item](class-items.md), and 5 holds a throwable. Melee has its own button instead of a slot.
- **HUD:** a compass at the top with the heading in yellow; players alive and kills at the top right; the crosshair; health, boost, stance, gear durability, ammo, and fire mode at the bottom center; the five slots as weapon silhouettes beside the minimap at the bottom right.
- **Picking up:** look at an item and press F, like PUBG. The prompt names a gun's rolled version, since every gun is one version for the match ([Rules](../rules.md#versions)).
- **Keys:** PUBG's defaults: WASD to move, Shift sprint, Ctrl walk, C crouch, Z prone, Space jump and vault, = auto-run, Alt free look, V perspective, F interact, Tab inventory, left mouse fire, right mouse aim (tap to toggle, hold to hold), R reload, B fire mode, Q and E peek, and 1 to 5 for the slots. The one change is X, which is melee: tap X to bring out the melee weapon, and hold X to stow your weapon and run faster.
- **Inventory (Tab):** vicinity, backpack, gear (helmet, vest, backpack, and outfit slots for skins), and the weapons with their attachment slots. Hovering a gun shows its version: cartridge, fire modes, rate, and mag. You can still move with it open.

## Knockdowns & revives

1. At zero health you're knocked down. You can crawl, but you leave a blood trail.
2. A teammate can pick you up while you're knocked. This is slow without an adrenaline shot.
3. If you bleed out, you can still be revived with a defib, or slowly with CPR.

**Adrenaline shots** are rarer and have two uses: a quick pickup, or maybe a heal like PUBG's adrenaline (replacing the infinite-stamina idea, since original PUBG had no stamina). You don't need one in your hands to use it.

## Comeback fight

When your whole team is wiped out, you're sent to a loser fight as a comeback play. It's a random team fight where players get random weapons, and the format varies:

- A 4v4
- Two 2v2s played side by side
- A 3v3 and a 1v1 played side by side
- Other mixes

Winners redeploy into the main match with the guns and armor they had in the team fight.

## Buildings & materials

Buildings are semi-destructible, kept simple: doors, windows, and specific walls can break. Materials matter too.

Wire fences (possibility): drive straight through them like PUBG, or cut a gap quietly for a stealthier approach. Wire cutters could be a melee item that cuts fences, and the Galil ARM's bipod wire cutter could do the same.

- Wood can be shot through.
- Thin metal can be shot through by some weapons.

## Match setup

- **Modes:** solos, duos, and quads.
- **Player count:** set by each map's size.
- **Zone:** works like PUBG's.
- **Red zone:** yes.
- **Crates:** arrive by air drop.
- **Hot loot zones:** yes.

## Sound

Sound is a major focus.

- **Real sound travel:** sound moves at its real speed, about 343 m/s, so a shot 300 m away is heard almost a second after it's fired.
- **Bullet crack:** bullets still faster than sound crack as they fly past you. The crack lands before the bang, so the gap between them hints at how far away the shooter is. Subsonic rounds, like .45 ACP and the [VSS](../weapons/battle-rifles/vss.md)'s 9×39mm, don't crack.

How gun sounds are layered and sourced is on [Gun art and sound](../planning/art-and-sound.md#sound).

## Anti-cheat

Cheaters are a real problem, but anti-cheat comes much later.
