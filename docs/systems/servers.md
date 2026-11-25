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
- **How other games do it (planner, 2026-11-25, the owner's question):** most shooters rewind and differ mainly in the cap.
    - **Counter-Strike (CS:GO and CS2):** rewinds up to `sv_maxunlag`, 0.2 s (200 ms) by default, settable from 0 to 1 s ([Total CS](https://totalcsgo.com/commands/svmaxunlag)). Valve's older Source games such as Team Fortress 2 rewind the same way and accept being hit behind a wall as "an intentional trade-off" for fair shots; rockets, grenades, and flames there aren't rewound at all ([TF2 Wiki](https://wiki.teamfortress.com/wiki/Lag_compensation)).
    - **Valorant:** launched with a 200 ms cap, then cut it to 140 ms in patch 6.02 (February 2023), because player data showed 200 ms was too generous to high ping and low-ping players kept getting hit after reaching cover. Riot said players in low-ping matches would hardly notice, and high-ping players would have to lead more ([VALORANT Patch Notes 6.02](https://playvalorant.com/en-us/news/game-updates/valorant-patch-notes-6-02/)).
    - **Apex Legends:** rewinds with no stated cap. Respawn's lead engineer calls the server "a sort of time machine" and says being hit after reaching cover "can't be eliminated, only transferred" between the two players ([EA, April 2021](https://www.ea.com/games/apex-legends/apex-legends/news/servers-netcode-developer-deep-dive?setLocale=en-us)).
    - **Overwatch:** "favours the shooter" in laggy situations, except for movement abilities, which Blizzard changed to favor the player escaping more often; no cap was published ([PCGamesN, April 2016](https://www.pcgamesn.com/overwatch/cute-stickers-and-little-cups-help-explain-the-overwatch-netcode)).
    - **PUBG and Call of Duty:** we found no published rewind cap for either.
    - **For us:** 200 ms matches Counter-Strike's default and Valorant's launch number; Valorant's 140 ms is the tighter end. A battle royale has a wider spread of pings than a small competitive match, so 200 ms stays for now, as a setting the lead can tune after internet playtests (queued for the owner on the [To-do](../planning/to-do.md#you-decisions)).
- **Bullets in flight:** a bullet's travel time and drop are worked out on the server from the moment of the shot, with targets rewound only to the moment the shot was fired, so long-range shots still need leading.
- **When:** before the first playtest with friends over the internet ([To-do](../planning/to-do.md#for-the-lead-claude-code)); on the local network it hardly matters.

**Guns on a player (owner OK'd, 2026-11-24):** a bullet that hits the gun someone is holding passes through to the body behind it, as if the gun weren't there. Otherwise a raised rifle would shield the face in every fight, and how much a gun covers would depend on its model. Pans and shields still block ([Class items](class-items.md)).
