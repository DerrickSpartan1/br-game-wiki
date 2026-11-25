# Servers

Three server types, taking the WARDOGS / Squad / Arma approach:

- **Official servers**
- **Community servers**
- **Private servers**

Seasons and collectibles only count on servers that follow the official ruleset. A server can change the map and a couple of other things and still count.

Hosting is still to be decided.

## Hits and lag

The server decides every hit ([game repo](https://github.com/DerrickSpartan1/br-game)), so at real ping a shot that was on a moving head on your screen can miss on the server, where the target has already moved on. The fix is lag compensation (owner OK'd, 2026-11-24, for the lead to plan):

- **What PUBG did:** in 2017–2018 much of PUBG's hit handling ran on the player's own machine, and players with high ping could gain from it, since they showed up late on everyone else's screen ([PCGamesN, early 2018](https://www.pcgamesn.com/playerunknowns-battlegrounds/pubg-server-tick)). Long-range hits failing to register was a known bug that PUBG was still patching in January 2018 ([PC Gamer, 3 January 2018](https://www.pcgamer.com/pubg-pc-patch-targets-hit-registration-lobby-crashes)). We keep the server in charge instead, so a cheat can't claim hits.
- **Rewind:** the server keeps each player's posed body for about the last half second. When a shot comes in, it rewinds everyone else to where the shooter saw them (the shooter's ping plus the view's interpolation delay) and checks the hit there, so what you aim at is what you hit.
- **A cap:** rewind goes back at most 200 ms. Above that, a high-ping shooter has to lead their shots, so lag never pays.
- **Behind cover:** the price of rewinding is that a target can be hit just after ducking behind a wall on their own screen. The 200 ms cap keeps that short.
- **Bullets in flight:** a bullet's travel time and drop are worked out on the server from the moment of the shot, with targets rewound only to the moment the shot was fired, so long-range shots still need leading.
- **When:** before the first playtest with friends over the internet ([To-do](../planning/to-do.md#for-the-lead-claude-code)); on the local network it hardly matters.

**Guns on a player (owner OK'd, 2026-11-24):** a bullet that hits the gun someone is holding passes through to the body behind it, as if the gun weren't there. Otherwise a raised rifle would shield the face in every fight, and how much a gun covers would depend on its model. Pans and shields still block ([Class items](class-items.md)).
