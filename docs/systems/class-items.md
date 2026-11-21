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
- **Gas mask (idea):** keeps out the gas in [poison zones](match-flow.md#zone-events) and from tear-gas rounds.

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

## Sources

- [Gamertag Mythras: PUBG utility items (Folded Shield)](https://gamertagmythras.com/blog/pubg-battlegrounds/pubg-utility-items-guide)
