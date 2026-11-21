# Maps

## The first map

- **Size:** Erangel's, about 64 km² of island.
- **Players:** 100, like Erangel (our pick).
- **Layout from a real island:** the terrain, roads, and where the towns sit come from a real island (shortlist below). Everything is then reskinned in the game's own Eastern European, Soviet-era style, with Erangel's mix of towns, farmland, forest, a military base, and long sight lines.
- **Match flow:** the plane, zone phases, and zone events start from Erangel's ([Match flow](match-flow.md)).
- **Caps:** the per-map max for throwables and crate weapons is TBD ([Weapon pool](weapon-pool.md)).

**Erangel, for reference:** a fictional 8 × 8 km island in the Black Sea near Russia. In its story, Soviet forces occupied it from the 1950s and used it as a military testing site. It has 25 named places: 5 large towns (Georgopol, Novorepnoye, Primorsk, Yasnaya Polyana, Pochinki), 9 small ones (Gatka, Mylta, Mylta Power, Lipovka, Severny, Rozhok, Zharki, Kameshki, Shooting Range), and 11 other spots, like Sosnovka Military Base, the Prison, School, Quarry, and Hospital.

## Real islands to base it on

Only the layout matters, so the look of each island doesn't. What counts is the size, enough towns and villages spread out, and hills for cover.

| Island | Where | Size | Places to copy | Terrain | Fit |
| --- | --- | --- | --- | --- | --- |
| **Gozo** | Malta | 67 km², 14 × 7 km | Victoria, the central town, and 13 villages; a ferry harbor (Mġarr) and two resort bays (Marsalforn, Xlendi). About 39,000 people | Very hilly (at least 31 hills) and rural | Erangel's area, but long: the map becomes about 14 × 8 km instead of 8 × 8 |
| **Ischia** | Italy | 47 km², 10 × 7 km | Six towns, with about 62,000 people, so bigger, denser towns; a castle on a rock, joined to the island by a stone bridge | Almost all mountain, with a 789 m peak in the middle | Fits 8 × 8 at about 80% scale; a bit smaller than Erangel |
| **Guernsey** | Channel Islands | 63–65 km² | St Peter Port and nine more parishes, about 65,000 people; German WWII bunkers, batteries, and towers | Mostly level, with low hills in the southwest | Right size, but built up nearly everywhere, with no open ground between towns |
| **Föhr** | Germany | 83 km², 12 × 6.8 km | Wyk and 16 small villages | Flat: 13 m at its highest | Good village spread, but flat ground leaves no cover |
| **Lastovo** | Croatia | 47 km², 9.8 × 5.8 km | One small town (about 350 people) and four hamlets, about 790 people in all | 46 hills, karst fields, and 60% forest | Good terrain, but almost nothing to copy |
| **Russky Island** | Russia | 97.6 km² | A former Soviet military island with old forts | A 291 m mountain | Too big, and its Soviet history doesn't matter now that the look is reskinned |

**Pick: Gozo.** Its central town and 13 villages line up with Erangel's 14 large and small towns almost one for one, its hills give cover between them, and its area matches. The catch is the shape: a 14 × 8 km map instead of a square. If the map has to stay square, Ischia is the pick, with fewer but bigger towns around a mountain.

### Turning a real island into terrain

1. **Heights:** download free 30 m elevation data for the island (such as NASA's SRTM). Check each source's license first.
2. **Landscape:** Epic's largest recommended Unreal landscape is 8,129 × 8,129 vertices, which at 1 m apart covers 8.1 km. A 14 km map like Gozo needs the vertices about 1.75 m apart, or more than one landscape. At the default height scale, heights run from −256 m to 256 m, so higher peaks need a larger scale.
3. **Detail:** 30 m data is smooth, so ditches, roads, and riverbanks are sculpted on top.
4. **Roads and towns:** OpenStreetMap has the island's roads and building footprints as the layout guide. Towns get the game's own buildings on those footprints. A game world built from a substantial part of OpenStreetMap's data has to credit OpenStreetMap.

## Night maps

Idea for night maps where flashlights and stealth matter. Night scopes like the StG 44's Vampir would shine there, and so would star rounds from grenade launchers, which light an area about 200 m across for about 40 seconds, and infrared star rounds that only show through night vision ([Attachments](attachments.md#ground-rounds-smoke-and-other-non-lethal-rounds)). Matches can now also run from late day into night, all night, or from night into morning ([Match flow](match-flow.md#time-passes)).

## Sources

- [PUBG Wiki: Erangel (Classic)](https://pubg.wiki.gg/wiki/Erangel_(Classic))
- [Liquipedia: Erangel](https://liquipedia.net/pubg/Erangel_Remaster)
- [Wikipedia: Gozo](https://en.wikipedia.org/wiki/Gozo) · [Wikipedia: Ischia](https://en.wikipedia.org/wiki/Ischia) · [Wikipedia: Guernsey](https://ipfs.ssi.eecc.de/ipns/en.wikipedia-on-ipfs.org/wiki/Guernsey) · [Wikipedia (older copy): Guernsey](https://dlab.epfl.ch/wikispeedia/wpcd/wp/g/Guernsey.htm) · [Wikiwand: Fortifications of Guernsey](https://www.wikiwand.com/en/articles/Fortifications_of_Guernsey) · [Wikipedia: Föhr](https://en.wikipedia.org/wiki/F%C3%B6hr) · [Wikipedia: Lastovo](https://en.wikipedia.org/wiki/Lastovo) · [Wikipedia: Russky Island](https://en.wikipedia.org/wiki/Russky_Island)
- [Epic: Landscape technical guide](https://dev.epicgames.com/documentation/unreal-engine/landscape-technical-guide-in-unreal-engine)
- [OpenStreetMap wiki: License use cases](https://wiki.openstreetmap.org/wiki/License/Use_Cases)
