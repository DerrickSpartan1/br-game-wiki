# Time to kill (TTK)

TTK is how long a gun takes to kill a target when every shot lands. The first shot hits instantly, so only the gaps between shots count.

**Goal:** no single gun should win every fight. TTK needs more discussion.

Range is a main balancing tool: damage falloff, recoil, and handling give each gun a distance where it wins, so no single gun is best everywhere.

```text
TTK = (shots to kill - 1) × 60 / RPM
```

- **Shots to kill:** target health divided by damage per hit, rounded up.
- **Damage per hit:** base damage × hit-zone multiplier × armor reduction × range falloff. Shooters commonly multiply these together, as CS2 does.
- **Fire rate (RPM):** rounds per minute. For semi-autos, it's a set max rate.
- **Breakpoints:** a damage change only matters when it changes shots to kill. On 100 health, 33 damage takes 4 shots but 34 takes 3.
- **Theoretical vs. effective TTK:** the formula assumes perfect accuracy. Recoil, spread, and misses make real TTK longer, and a very fast TTK covers up misses, which works against skilled players.
- **Magazine size:** a gun with fewer rounds than shots to kill needs a reload mid-fight, and small mags limit kills per mag.
- **PUBG-style armor:** each vest or helmet level cuts damage by a flat percentage (community-reported as 30%, 40%, and 55% for levels 1 to 3).

Illustrative example with made-up numbers (100 health, chest hits, no armor):

| Gun | Damage | Shots to kill | Fire rate | TTK | Kills per mag |
| --- | --- | --- | --- | --- | --- |
| M17 | 25 | 4 | 400 RPM (0.15 s between shots) | 0.45 s | 4 (17 rounds) |
| Glisenti | 34 | 3 | 240 RPM (0.25 s between shots) | 0.50 s | 2 (7 rounds) |

Higher damage keeps the Glisenti's TTK close to the M17's, while its 7-round mag still holds it back in longer fights.

Sources: [CSDB: CS2 damage calculator](https://csdb.gg/damage-calculator/) · [Insider Gaming: Warzone TTK](https://insider-gaming.com/warzone-devs-address-fast-time-to-kill-concerns-on-verdansk/) · [Steam forum: PUBG armor values](https://steamcommunity.com/app/578080/discussions/1/1471966894874045224)

Reliability: guns never jam or overheat (see [Rules](../rules.md)). Whether some items wear out is still open; the makeshift suppressor and the StG 44's Krummlauf are the current wear ideas.
