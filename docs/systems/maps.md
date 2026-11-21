# Maps

## The first map: Ischia

The first map takes its layout from Ischia, an island off Naples: the coastline, hills, ring road, and where the towns sit. Everything is then reskinned in the game's own Eastern European, Soviet-era style, with Erangel's mix of towns, farmland, forest, a military base, and long sight lines. A simplified mockup of the layout is a private Design artifact in the owner's Claude account.

- **Size:** 10 × 8 km, with the island at true scale (9.6 × 7.7 km, about 46 km² of land) and ocean around the edges.
- **Players:** 100, like Erangel (our pick).
- **Match flow:** the plane, zone phases, and red zones start from Erangel's ([Match flow](match-flow.md)).
- **Caps:** the per-map max for throwables and crate weapons is TBD ([Weapon pool](weapon-pool.md)).

### What the layout has

| Kind | Places | Where |
| --- | --- | --- |
| Large towns | Ischia Porto, Forio | Ischia Porto on the northeast corner around the harbor; Forio on the west coast |
| Towns | Ischia Ponte, Casamicciola Terme, Lacco Ameno, Barano d'Ischia | Ischia Ponte below Ischia Porto, facing the castle islet; Casamicciola and Lacco Ameno along the north coast; Barano on the southeast slopes |
| Villages | Serrara Fontana, Panza, Sant'Angelo, Monterone, Cuotto | Serrara Fontana and Panza on the high south side; Sant'Angelo on the south coast; Monterone and Cuotto inland from Forio |
| Hills | Monte Epomeo (789 m), Monte Trippodi (503 m), Monte Rotaro (307 m), Montagnone (252 m), Pizzi Bianchi | Epomeo fills the middle and west; the smaller hills sit east and north between Barano, Casamicciola, and Ischia |
| Roads | A ring road through every town, about 30 km of bends in real life, climbing to about 450 m; a side road down to Sant'Angelo | — |
| Castle islet | The Aragonese Castle on a rock off Ischia Ponte, joined by a stone bridge | A small fortress spot, like a mini Sosnovka |

People per municipality (2019): Ischia 20,170, Forio 18,005, Barano d'Ischia 9,977, Casamicciola Terme 8,084, Lacco Ameno 4,764, Serrara Fontana 3,126.

**Erangel, for reference:** a fictional 8 × 8 km island in the Black Sea near Russia. In its story, Soviet forces occupied it from the 1950s and used it as a military testing site. It has 25 named places: 5 large towns (Georgopol, Novorepnoye, Primorsk, Yasnaya Polyana, Pochinki), 9 small ones (Gatka, Mylta, Mylta Power, Lipovka, Severny, Rozhok, Zharki, Kameshki, Shooting Range), and 11 other spots, like Sosnovka Military Base, the Prison, School, Quarry, and Hospital. Ischia gives 11 towns and villages, so our own spots, like a military base and a prison, go in the open ground between them.

### Heights: squashed, with a plateau

Ischia is almost all mountain, and a 789 m peak in a 10 km map would let whoever holds it see most of the island, be too steep to climb or drive, and split the map. So every height is squashed to 40%, keeping the shape, and Epomeo's top is flattened into a plateau.

| Hill | Real height | In the game |
| --- | --- | --- |
| Monte Epomeo | 789 m | A plateau about 2 km across, at about 270 m |
| Monte Trippodi | 503 m | About 200 m |
| Monte Rotaro | 307 m | About 120 m |
| Montagnone | 252 m | About 100 m |

- **Walkable:** no slope steeper than about 37° in the mock-up's terrain.
- **No sniper nest:** a tree line rings the plateau, so the middle doesn't see the whole island.

### Our own spots

Approved on the v3 mockup.

| Spot | Where | Notes |
| --- | --- | --- |
| Military Outpost | The plateau's center | A bunker underneath holds one of the [vaults](match-flow.md#vaults-and-keys) |
| Tunnel | About 1.7 km under the plateau's east edge, from Casamicciola's road to the south road | A shortcut and an ambush spot. The last circles can't end underground; bombardment shells can't reach it, but a gas red zone fills it |
| Prison | Alone in the southwest, past Panza | Cut off, like Erangel's |
| Port | Ischia Porto, the real ferry harbor | Containers, cranes, and a ferry, like Georgopol's docks |
| Fishing Dock | Forio's harbor | A small pier and boats |
| Fortress | The castle islet off Ischia Ponte | Over its stone bridge |
| Quarry | The south slopes above the coast | — |
| Thermal Spa | Just west of Casamicciola Terme | Ischia is known for its hot springs |
| Hospital | East of Lacco Ameno | — |
| School | Between Barano and Ischia | — |
| Farm | The fields near Cuotto | — |

### Marina, farms, and vaults

- **Marina:** a new coastal town of our own on the southeast bay, between Barano and the east coast, with a small pier. A side road links it to the ring road near Barano and runs up the east coast to Ischia Ponte.
- **Farms and huts:** about 70 small farmsteads of 1 to 4 huts and barns are scattered across the open ground, each with a dirt track to the nearest road, plus a few longer farm tracks through the fields.
- **Vaults:** five: under the Military Outpost, in Ischia Porto and Forio, on Marina's waterfront, and the Prison armory ([Vaults and keys](match-flow.md#vaults-and-keys)).

With the 12 towns and villages, that's 23 named places, against Erangel's 25.

### River

Erangel's river and bridges make chokepoints that shape every match. Ischia has no river in the sources checked, so ours is made up: a crater lake on the plateau feeds a river down to the south coast. First pass on the v4 mockup, for review:

- **Crater lake:** about 300 m across, on the plateau's south edge, about 800 m southeast of the Military Outpost.
- **Route:** about 3.6 km down the south slopes along the mock-up terrain's downhill path, through the forest and across the ring road between Serrara Fontana and Barano, out to sea on the bay east of the Quarry.
- **Width:** about 25 m below the lake, widening to about 60 m at the mouth. Players can swim it ([Vehicles and water](gameplay.md#vehicles-and-water)).
- **Three bridges:** the tunnel road just south of the tunnel, the ring road (the main one), and a farm track near the mouth.
- **Why there:** the ring road between Serrara Fontana and Barano is its longest stretch without a town, so the bridge gives it a landmark and a chokepoint, and the river splits the south side in two.

### Turning Ischia into terrain

1. **Heights:** download free 30 m elevation data for the island (such as NASA's SRTM). Check each source's license first.
2. **Landscape:** Epic's largest recommended Unreal landscape is 8,129 × 8,129 vertices, which at 1 m apart covers 8.1 km. The 10 km map needs the vertices about 1.25 m apart. At the default height scale, heights run from −256 m to 256 m, so Epomeo's 789 m needs a height scale of at least about 310.
3. **Detail:** 30 m data is smooth, so ditches, roads, and riverbanks are sculpted on top.
4. **Roads and towns:** OpenStreetMap has the island's roads and building footprints as the layout guide. Towns get the game's own buildings on those footprints. A game world built from a substantial part of OpenStreetMap's data has to credit OpenStreetMap.

## Future maps

Islands kept for later maps. Only the layout matters, so the look of each doesn't.

| Island | Where | Size | Places to copy | Terrain | Notes |
| --- | --- | --- | --- | --- | --- |
| **Gozo** | Malta | 67 km², 14 × 7 km | Victoria, the central town, and 13 villages; a ferry harbor (Mġarr) and two resort bays (Marsalforn, Xlendi). About 39,000 people | Very hilly (at least 31 hills) and rural | The best match for Erangel's town spread; a long 14 × 8 km map |
| **Guernsey** | Channel Islands | 63–65 km² | St Peter Port and nine more parishes, about 65,000 people; German WWII bunkers, batteries, and towers | Mostly level, with low hills in the southwest | Built up nearly everywhere, so towns would need thinning out |
| **Föhr** | Germany | 83 km², 12 × 6.8 km | Wyk and 16 small villages | Flat: 13 m at its highest | Good village spread; would need hills added |
| **Lastovo** | Croatia | 47 km², 9.8 × 5.8 km | One small town (about 350 people) and four hamlets, about 790 people in all | 46 hills, karst fields, and 60% forest | Good terrain for a map whose towns are mostly our own |
| **Russky Island** | Russia | 97.6 km² | A former Soviet military island with old forts (Fort Russky, Fort Pospelov) and a huge bridge to the mainland | A 291 m mountain | Bigger than Erangel; would need scaling down |

## Night maps

Idea for night maps where flashlights and stealth matter. Night scopes like the StG 44's Vampir would shine there, and so would star rounds from grenade launchers, which light an area about 200 m across for about 40 seconds, and infrared star rounds that only show through night vision ([Attachments](attachments.md#ground-rounds-smoke-and-other-non-lethal-rounds)). Matches can now also run from late day into night, all night, or from night into morning ([Match flow](match-flow.md#time-passes)).

## Sources

- [PUBG Wiki: Erangel (Classic)](https://pubg.wiki.gg/wiki/Erangel_(Classic))
- [Liquipedia: Erangel](https://liquipedia.net/pubg/Erangel_Remaster)
- [Wikipedia: Gozo](https://en.wikipedia.org/wiki/Gozo) · [Wikipedia: Ischia](https://en.wikipedia.org/wiki/Ischia) · [Wikipedia: Guernsey](https://ipfs.ssi.eecc.de/ipns/en.wikipedia-on-ipfs.org/wiki/Guernsey) · [Wikipedia (older copy): Guernsey](https://dlab.epfl.ch/wikispeedia/wpcd/wp/g/Guernsey.htm) · [Wikiwand: Fortifications of Guernsey](https://www.wikiwand.com/en/articles/Fortifications_of_Guernsey) · [Wikipedia: Föhr](https://en.wikipedia.org/wiki/F%C3%B6hr) · [Wikipedia: Lastovo](https://en.wikipedia.org/wiki/Lastovo) · [Wikipedia: Russky Island](https://en.wikipedia.org/wiki/Russky_Island)
- Ischia's layout: [Komoot: ring route around Ischia](https://www.komoot.com/it-it/smarttour/e1113852301/giro-dell-isola-di-ischia) (length and high point) · [ISTAT 2019 population, in The Economist's data](https://github.com/TheEconomist/covid-19-excess-deaths-tracker/blob/master/source-data/italy/archive/italy_population_source.csv) · peaks from OpenStreetMap, [via LinkSim](https://github.com/wilhel1812/LinkSim/blob/main/public/peak-tiles/v1/tiles/la_p40_lo_p13.json) · town points from GeoNames, [via vineyardbovines/geojson](https://github.com/vineyardbovines/geojson/tree/main/geojson/cities/ita/04), and [Who's On First](https://github.com/whosonfirst-data/whosonfirst-data-admin-it) · coastline for the mockup from the ASTER Water Body Database, [via is-on-water](https://github.com/NiciusB/is-on-water)
- [Epic: Landscape technical guide](https://dev.epicgames.com/documentation/unreal-engine/landscape-technical-guide-in-unreal-engine)
- [OpenStreetMap wiki: License use cases](https://wiki.openstreetmap.org/wiki/License/Use_Cases)
