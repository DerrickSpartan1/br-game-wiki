# Maps

## The first map

- **Size:** 8 × 8 km, the size of PUBG's Erangel.
- **Players:** 100, like Erangel (our pick).
- **Setting:** an island, with Erangel's mix of towns, farmland, forest, rivers, a military base, and long sight lines. Its terrain is based on a real island (shortlist below); its towns and buildings are the game's own, in an Eastern European, Soviet-era style.
- **Match flow:** the plane, zone phases, and zone events start from Erangel's ([Match flow](match-flow.md)).
- **Caps:** the per-map max for throwables and crate weapons is TBD ([Weapon pool](weapon-pool.md)).

**Erangel, for reference:** a fictional 8 × 8 km island in the Black Sea near Russia. In its story, Soviet forces occupied it from the 1950s and used it as a military testing site, which explains its military base, hospital, and storage buildings.

## Real islands to base it on

No real island matches Erangel in size, shape, and look all at once. These come closest. An island bigger than 8 × 8 km can be scaled down: a hill 20% smaller still plays the same.

| Island | Where | Area | Fit | Why it works | Catch |
| --- | --- | --- | --- | --- | --- |
| **Russky Island** | Russia, off Vladivostok | 97.6 km² | Scale to about three-quarters | The closest in spirit: a closed Soviet military island and one of the Soviet Navy's largest training areas, with old forts (Fort Russky, Fort Pospelov), a 291 m mountain, and a huge bridge to the mainland | Too big at full size; on the Pacific, not the Black Sea |
| **Lastovo** | Croatia | 46.9 km² (9.8 × 5.8 km) | Nearly true size | A Yugoslav military zone closed to foreigners until 1988 (the army left in 1992); 46 hills, karst fields, 60% forest, and five small villages | Mediterranean stone villages; steep coast |
| **Guernsey** | Channel Islands | 65 km² | About Erangel's whole square | Germany fortified it heavily in 1940–45: 11 batteries, tunnels, and observation towers, on top of older forts and towers; a harbor town, St Peter Port | British look; low and fairly flat (110 m high) |
| **Vis** | Croatia | 89.7 km² | Scale down | A Yugoslav naval base until 1989 | Mountainous (587 m) and Adriatic |
| **Vormsi** | Estonia | 93 km² | Scale down | About a dozen small Baltic villages, closer to Erangel's countryside than the others | Only about 400 people, so few buildings to copy |

**Pick:** Russky Island for the look and story, scaled down to fit 8 × 8 km; Lastovo if real terrain at close to real size matters more. Either way, the towns are built in the game's own Soviet-era style.

### Turning a real island into terrain

1. **Heights:** download free 30 m elevation data for the island (such as NASA's SRTM) and crop and scale it to 8 × 8 km. Check each source's license first.
2. **Landscape:** Epic's largest recommended Unreal landscape is 8,129 × 8,129 vertices, which at 1 m between vertices covers 8.1 km, just over the map. At the default height scale, heights run from −256 m to 256 m, so a 291 m mountain needs a slightly larger scale.
3. **Detail:** 30 m data is smooth, so ditches, roads, and riverbanks are sculpted on top.
4. **Roads and towns:** OpenStreetMap has the island's roads and building footprints as a layout guide. A game world built from a substantial part of OpenStreetMap's data has to credit OpenStreetMap.

## Night maps

Idea for night maps where flashlights and stealth matter. Night scopes like the StG 44's Vampir would shine there, and so would star rounds from grenade launchers, which light an area about 200 m across for about 40 seconds, and infrared star rounds that only show through night vision ([Attachments](attachments.md#ground-rounds-smoke-and-other-non-lethal-rounds)). Matches can now also run from late day into night, all night, or from night into morning ([Match flow](match-flow.md#time-passes)).

## Sources

- [PUBG Wiki: Erangel (Classic)](https://pubg.wiki.gg/wiki/Erangel_(Classic))
- [Wikipedia: Russky Island](https://en.wikipedia.org/wiki/Russky_Island) · [Wikipedia: Lastovo](https://en.wikipedia.org/wiki/Lastovo) · [Wikipedia: Guernsey](https://ipfs.ssi.eecc.de/ipns/en.wikipedia-on-ipfs.org/wiki/Guernsey) · [Wikiwand: Fortifications of Guernsey](https://www.wikiwand.com/en/articles/Fortifications_of_Guernsey) · [Wikiwand: Vis](https://wikiwand.com/EN/Vis_(island)) · [Wikipedia: Vormsi](https://en.wikipedia.org/wiki/Vormsi)
- [Epic: Landscape technical guide](https://dev.epicgames.com/documentation/unreal-engine/landscape-technical-guide-in-unreal-engine)
- [OpenStreetMap wiki: License use cases](https://wiki.openstreetmap.org/wiki/License/Use_Cases)
