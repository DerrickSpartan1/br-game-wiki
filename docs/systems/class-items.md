# Class items

A 4th slot holds class items: limited-use gadgets found randomly as loot during a match. There are no player classes.

- **Defibs:** uses limited by batteries or something similar.
- **Bulletproof barricade:** a deployable cover piece, like the one in Rainbow Six Siege ([Shields](#shields)).
- **Rangefinder binoculars:** spot enemies at a distance and read the range for bullet drop.
- **Door wedge or door alarm:** lock down a building while you loot it.
- **Tripwire alarm:** a noise trap that warns you when someone enters your area.
- **Recon drone:** short battery life; scouts one building or compound.
- **Bomb drone:** one-time use. Reviving exists, so being taken out by a bomb drone shouldn't feel like a total game over.
- **Non-lethal grenade launchers:** these go in the class item pool; lethal ones are crate-only.
- **Ballistic shield:** a handheld shield that spawns in the world ([Shields](#shields)).
- **Flash shield (crate-only):** a ballistic shield with flashbangs on the front, like Blitz's in Rainbow Six Siege. It has 1 to 3 flash charges, isn't indestructible, and breaks quickly. It's assumed to use the class slot like the normal shield.
- **Gas mask (idea):** keeps out the gas in [gas red zones](match-flow.md#red-zones) and from tear-gas rounds.
- **Emergency redeploy:** a balloon that lifts you out and drops you elsewhere on the map, like PUBG's Emergency Pickup.
- **Deployable zipline:** place a zipline anywhere, like Apex's Pathfinder's zipline gun.
- **Fortifications:** a light version of building: placeable cover like the [barricade](#barricade) and movable shields. Which pieces exist is TBD.
- **Pans:** a pan as a small shield that also hits hard ([Pans](#pans)).
- **Breaching sledgehammer:** breaks doors and walls until it wears out, and hits hard ([Breaching sledgehammer](#breaching-sledgehammer)).

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

| | Pan | Sledgehammer | Owned melee, for comparison |
| --- | --- | --- | --- |
| Chest and stomach | 80 | 80 | 60 |
| Head | 95 (never a one-shot) | 95 | 90 |
| Neck | 67 | 67 | 63 |
| Arms and legs | 48 | 48 | 36 |
| Through tier 1, 2, 3 vests | 56, 48, 36 | 56, 48, 36 | 42, 36, 27 |
| Time between swings | 0.8 s | 1.2 s (heavy) | 0.8 s |

Hits to kill to the body: 2 with no vest or through tier 1, and 3 through tier 2 or 3, the same as PUBG's pan.

## Breaching sledgehammer

A class item for breaking in, and a last-ditch weapon when the chance comes.

- **Breaks** doors and breakable walls fast, but loudly ([Buildings](gameplay.md#buildings-materials)).
- **Durability:** it wears out after a number of breaches. First pass (our pick): 8 doors, or 3 walls, or a mix (a wall counts as about 3 doors). Hitting players doesn't wear it down.
- **Hits hard:** 80 to the body, like the pan, but with a slow 1.2 s swing ([Hitting with it](#hitting-with-it)).

## Sources

- [Gamertag Mythras: PUBG utility items (Folded Shield)](https://gamertagmythras.com/blog/pubg-battlegrounds/pubg-utility-items-guide)
