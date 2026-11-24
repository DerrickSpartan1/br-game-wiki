# Maps

## The first map: Ischia

The first map takes its layout from Ischia, an island off Naples: the coastline, hills, ring road, and where the towns sit. Everything is then reskinned in the game's own Eastern European, Soviet-era style, with Erangel's mix of towns, farmland, forest, a military base, and long sight lines. A simplified mockup of the layout is a private Design artifact in the owner's Claude account.

- **Size:** 10 × 8 km, with the island at true scale (9.6 × 7.7 km, about 46 km² of land) and ocean around the edges.
- **Players:** 100, like Erangel (our pick).
- **Match flow:** the plane, zone phases, and red zones start from Erangel's ([Match flow](match-flow.md)).
- **Caps:** 4 throwables (a smoke grenade plus 3 rolled) and 5 crate weapons a match ([Weapon pool](weapon-pool.md#how-the-randomness-works)).

### Place names

In the game the island is **Teplov**, and every town, hill, and spot has our own name ([Places](../planning/game-names.md#places)). The wiki keeps Ischia's real names as layout references, so the tables below still use them.

### What the layout has

| Kind | Places | Where |
| --- | --- | --- |
| Large towns | Ischia Porto, Forio | Ischia Porto on the northeast corner around the harbor; Forio on the west coast |
| Towns | Ischia Ponte, Casamicciola Terme, Lacco Ameno, Barano d'Ischia | Ischia Ponte below Ischia Porto, facing the castle islet; Casamicciola and Lacco Ameno along the north coast; Barano on the southeast slopes |
| Villages | Serrara Fontana, Panza, Sant'Angelo, Monterone, Cuotto | Serrara Fontana and Panza on the high south side; Sant'Angelo on the south coast; Monterone and Cuotto inland from Forio |
| Hills | Monte Epomeo (789 m), Monte Trippodi (503 m), Monte Rotaro (307 m), Montagnone (252 m), Pizzi Bianchi (430 m) | Epomeo fills the middle and west. Trippodi, Rotaro, and Montagnone sit east and north between Barano, Casamicciola, and Ischia. Pizzi Bianchi, white tuff pinnacles, is on the south slope above Sant'Angelo |
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
| Pizzi Bianchi | 430 m | About 170 m, on the south slope above Sant'Angelo |
| The castle islet's rock | About 113 m | About 45 m, with cliffs |

**Getting up Krepost (owner, 2026-11-22):** like the real castle, over the stone causeway, through a ramp cut into the rock, then winding paths up to the top. No lift.

- **Walkable:** no slope steeper than about 37° in the mock-up's terrain.
- **No sniper nest:** a tree line rings the plateau, so the middle doesn't see the whole island.

### The coast

The owner (2026-11-23): in the graybox, the land only dips a little at the shore. Every shore is a 1 m edge with a long, gentle slope into shallow water, so the coast reads as flat. Ischia's isn't: its south is mostly high coast with bays, where the Maronti cliffs run 50 to 120 m high, while the north and east have low waterfronts and harbors. First pass (our pick), with heights squashed to 40% like the land:

| Coast | Where | Shore | Sea floor |
| --- | --- | --- | --- |
| Cliffs | The south coast from Punta Imperatore past Rybatsk and the Maronti bay to Punta San Pancrazio; the Punta Caruso and Monte Vico headlands in the north-west; the Krepost rock | Rock faces 20 to 50 m high, with boulders at the foot | About 8 m deep at the foot, 30 m within 300 m |
| Rocky shore | The Zaro headland and the rest of the west outside the bays | Low rocks 2 to 6 m above the water | About 5 m deep within 50 m |
| Beaches | The Maronti bay under its cliffs, the Citara bay south of Vetrovo, San Montano by Gribovo, and Cartaromana by Mostki | Sand or shingle 20 to 60 m wide | A gentle start, about 3 m deep 50 m out, then steeper |
| Harbors and waterfronts | Gavansk, Mostki, Klyuchi, Gribovo, Rybatsk, and Tikhaya Bukhta | Quay walls about 2 m high, with slipways. Gavansk Port's round basin is cut into the shore, about 8 m deep, centered about (8830, 2440) | About 5 m deep at the quay |

- **Offshore:** past the first few hundred meters, the sea floor keeps falling, to about 60 m deep 1 km out and about 100 m at the map's edge, so open water looks deep and boats never touch bottom.
- **No visible edge:** the sea runs to the horizon, with no line where the landscape ends.
- **Real data later:** when the real heights go in ([Turning Ischia into terrain](#turning-ischia-into-terrain)), the coast comes from them, and the sea floor from EMODnet's free bathymetry (about a 115 m grid), squashed the same way. Check its license first.

### Our own spots

Approved on the v3 mockup.

| Spot | Where | Notes |
| --- | --- | --- |
| Military Outpost | The plateau's center | An airbase across the plateau, fenced, with watchtowers (owner, 2026-11-23). A bunker underneath holds one of the [vaults](match-flow.md#vaults-and-keys), and a passage runs from it to the Tunnel |
| Tunnel | About 1.7 km under the plateau's east edge, from Casamicciola's road to the south road | A shortcut and an ambush spot. The last circles can't end underground; bombardment shells can't reach it, but a gas red zone fills it. A blast door in its west wall opens onto the passage from the Military Outpost's bunker |
| Prison | Alone in the southwest, past Panza | Cut off, like Erangel's |
| Port | Ischia Porto, the real ferry harbor | A round harbor basin like Ischia's, plus a straight container quay with cranes and the ferry, like Georgopol's docks |
| Fishing Dock | Forio's harbor | A small fishing harbor behind a curved breakwater |
| Fortress | The castle islet off Ischia Ponte | Over its stone causeway, then a rock ramp and paths up |
| Quarry | The south slopes above the coast | — |
| Thermal Spa | Just west of Casamicciola Terme | Ischia is known for its hot springs |
| Hospital | East of Lacco Ameno | — |
| School | Between Barano and Ischia | A big Soviet school campus (owner, 2026-11-23) |
| Farm | The fields near Cuotto | — |

**Spot layouts (first pass, our pick, 2026-11-23):** the owner wanted the spots outside the towns laid out properly: an airfield at the military base, fences and towers, the bunker linked underground to the tunnel, and the school as a big Soviet campus. The planner's building canvas draws each spot as a site plan with a numbered key, and the [full-map mock](#the-full-map-mock) places them. Coordinates are meters from the map's north-west corner, x east and y south.

**Object 7, the airbase:**

- **Fence:** a double fence about 1.7 × 1.2 km that wanders along the plateau's rim in long, gentle curves, within (2958, 2866) to (4640, 4046), with a watchtower every 230 m. Roads and farm tracks stop at it.
- **Gates:** the main gate checkpoint on the road up from Verkhovye at (3835, 4030), where that road meets the fence, with a jet on a plinth outside, and the north gate on the track to Gribovo at (3925, 2880).
- **Airfield, the north half:** a 1,500 × 36 m concrete runway (09/27) along y 3000 from x 3050 to 4550, and a 15 m taxiway beside it at y 3110 that curves onto the runway at both ends, with a straight link in the middle. Six hardened aircraft shelters, 30 × 20 m concrete arches in earth berms, each on its own short spur off one of two curved dispersal loops, Soviet style, so no two stand in a row. An apron with two 40 × 30 m glider hangars, where the [Zhuravl](gameplay.md#vehicles-and-water) motor gliders spawn. A four-floor control tower with the flight operations block, the airfield fire station, a fenced fuel depot with four tanks, and a radar dome with a 60 m mast.
- **Ammunition area, the west side:** six earth-covered bunkers around a looping road, each in its own earth mound, inside their own double fence with towers.
- **Base, the south half:** on mown grounds, laid out in a straight grid as army bases are: the headquarters facing the parade ground, four three-floor barracks, the mess hall, a medical post, the motor pool, the boiler house and water tower, three warehouses, officers' housing, an obstacle course, a 350 m shooting range, two helipads, the bathhouse, the guardhouse by the main gate, kennels, garages, and the soldiers' club.
- **Underground (owner, 2026-11-23):** the bunker entrance stands on the vault point at (3758, 3742): a concrete block with a ramp and blast doors down to the bunker, about 18 m down, which holds the vault. From it a passage about 3 m wide and high runs 845 m east, nearly level, to a blast door in the road tunnel's west wall at (4603, 3768). A ladder shaft halfway, at (4180, 3762), is the escape hatch. That makes the tunnel a back way into the base.

**The other spots:**

| Spot | Layout |
| --- | --- |
| School | A fenced campus about 540 × 395 m: the Soviet Ш-shaped main school (three floors, a long front with three wings behind), the assembly hall and canteen, a gym with a 25 m pool, workshops, three four-floor boarding houses for pupils from the villages, a four-floor technical college with a small observatory dome, five-floor teachers' apartments, a stadium with a 400 m track, sports courts, a 50 m rifle range, a greenhouse and garden, the boiler house, the front square with a flagpole and monument, the gate, a primary school, a kindergarten, the library and pioneer house, an old tank on a plinth, a car park and bus stop, garages, and an orchard |
| Ostrog | A walled colony about 340 × 240 m: a 6 m wall, an inner fence, and a raked strip between, with watchtowers every 60 m. Inside, the living zone has four two-floor dormitory blocks in fenced yards, the canteen, bathhouse, club, chapel, and a punishment block; the work zone, behind its own wall, has the sawmill, sewing shop, timber yard, and boiler house. The checkpoint is the only gate. Outside the east wall: the administration, the guard barracks and armory (the vault), the visitors' building, and kennels |
| Gavansk Port | Redone (owner wasn't sure of the first one, 2026-11-24; our pick). A round harbor basin about 245 m across, like Ischia's real harbor, which was a lake until it was opened to the sea in 1854. A 14 m quay rings it, with a 50 m mouth facing northeast and a breakwater with a lighthouse curving round the mouth. Boats moor stern-to all round the basin, and a row of cafés and the three-floor port office face it from the town side. South of the basin, the ferry ties up at its own quay on the coast, and a straight 220 m container quay is built out along the coast: two gantry cranes on rails, a container yard stacked one to three high, three 60 × 24 m warehouses, the customs post and gate, a truck park, and a fuel depot |
| Kamenolom | An open pit of five benches, each about 6 m deep, following the hill's contours rather than a neat oval, with a pond at the bottom and a haul road spiraling down. Farm tracks stop at the rim. At the top: the 16 m stone crusher, conveyors and the screening plant, stockpiles, truck loading bins, the workshop, office and canteen, a weighbridge, an excavator and dump trucks, and a fenced, earth-covered explosives magazine off to the side |
| Sanatorium | The coast road crosses its grounds. On the land side: a four-floor neoclassical main building with a columned portico and two wings, the dining hall, six guest cottages, a club and cinema, a park with radial alleys, a fountain, and a rotunda, a sports ground, the boiler house, and the gate on the access road. On the sea side: the thermal baths over the hot springs and three kidney-shaped outdoor pools, with a crossing over the road and a winding promenade |
| Hospital | A five-floor ward block with a three-floor surgical wing, the outpatient clinic on the road, a maternity building, an infectious diseases pavilion behind its own fence, the morgue, kitchen and laundry, the boiler house, ambulance garages, a helipad, two staff housing blocks, and a park between them. No Red Cross emblem |
| Kolkhoz | Four 72 × 12 m cow sheds, the milking block and calf shed, three silage trenches, a steel water tower on a column, three silos, the machine yard, a grain yard with its drying tower, an earth-covered vegetable store, the office with a board of honor and a worker statue, a club, a short street of workers' houses, and a pond with haystacks |
| Krepost | The causeway and gatehouse at the rock's foot, the covered ramp cut up through the rock, the keep at the top, the roofless cathedral, the convent and cloister, the castle prison cut into the rock, a chapel, terraced olive groves, gun platforms along the walls, and a café terrace |
| Vetrovo Pier | Redone (2026-11-24, our pick). A small fishing harbor behind a breakwater that curves out and back round it, with a lighthouse at its tip and a short west mole narrowing the mouth. Two finger piers with boats, the fish market, a boat repair yard with a slipway, boathouses, net sheds and drying racks, an ice plant, a fuel point at the breakwater's root, the harbor master, and a lane up into Vetrovo |

- **New building types:** the layouts add about 30 types the kit doesn't draw yet, such as hardened aircraft shelters, the control tower, ammunition bunkers, boarding houses, the prison dormitories, the lighthouse, and the thermal baths. They're plain blocks in the mock, sized on the canvas.
- **Curves and straight lines (owner, 2026-11-23):** more curves, so not everything is a square, but not everything curved either. Curved: the taxiway's ends and the dispersal loops, the ammunition road, park paths, the school's and hospital's rounded grounds, the sanatorium's pools and promenade, the quarry's benches, the farm's yard and pond, the breakwaters, and Krepost's ramp. Straight on purpose (our pick): runways, quays, the parade ground and barracks rows, the prison's walls, the cow sheds, and the main axis of the school and the sanatorium.
- **Access roads:** Ostrog gets a short paved road, about 150 m, from its admin area east to the nearest farmstead track, and the Kolkhoz farm track arrives at the admin area. Kamenolom gets a new dirt road, about 1.4 km, north-west to the nearest local road. Neither is in the [layout file](#layout-coordinates) yet.
- **Looks:** the shelters follow Soviet hardened aircraft shelters in earth berms; the colony follows the Soviet corrective colony's zones; the sanatorium follows spa towns like Tskaltubo in Georgia; the Kolkhoz water tower is a Rozhnovsky tower, the steel tank on a column seen on Soviet farms.

### Marina, farms, and vaults

- **Marina:** a new coastal town of our own on the southeast bay, between Barano and the east coast, with a small pier. A side road links it to the ring road near Barano and runs up the east coast to Ischia Ponte.
- **Farms and huts:** about 70 small farmsteads of 1 to 4 huts and barns are scattered across the open ground, each with a dirt track to the nearest road, plus seven longer farm tracks through the fields (game names, from the [layout file](#layout-coordinates)):
    - From the north coast near the Sanatorium up onto the Stolovaya plateau (about 2 km).
    - From Klyuchi up to Sokolinaya (about 2.7 km).
    - Across the west slopes from near Kholmy toward Verkhovye (about 1.9 km).
    - From the Kamenolom quarry north toward Belye Piki (about 1.2 km).
    - From the Kolkhoz to Ostrog (about 0.9 km), and a short link from the ring road to the Kolkhoz (about 0.4 km).
    - From the east slopes near the School down over the river's farm-track bridge to the Kamenolom quarry (about 2.7 km). The part west of the bridge is the planner's pick.
- **Vaults:** five: under the Military Outpost, in Ischia Porto and Forio, on Marina's waterfront, and the Prison armory ([Vaults and keys](match-flow.md#vaults-and-keys)).

With the 12 towns and villages, that's 23 named places, against Erangel's 25.

### Towns and buildings

The plan (owner, 2026-11-23): mock up each town's layout first to learn which buildings the map needs, like generic houses, a police station, and a fire station, then build variants of each and place them around.

**Dense town cores, with fields around them (owner, 2026-11-23):** each town is a tight core, packed about as densely as Erangel's towns, and fields and farmsteads fill the rest of its flat area in the graybox, like Erangel's farmland. Core sizes and building counts are from the second mock (our pick); each core is centered on the town's point in the [layout file](#layout-coordinates):

| Town | Core across | Buildings |
| --- | --- | --- |
| Gavansk | 600 m | 155 |
| Vetrovo | 550 m | 145 |
| Klyuchi | 400 m | 72 |
| Ternovka | 370 m | 68 |
| Mostki, Gribovo | 330 m | 62, 58 |
| Tikhaya Bukhta | 300 m | 44 |
| Verkhovye, Polyanka | 210 m | 22 each |
| Rybatsk, Kholmy, Ovsyanka | 180 m | 17 to 18 |

For scale on Erangel's official map: Pochinki packs about 60 buildings into about 350 m, Yasnaya Polyana is about 400 m, Severny about 200 m, and only Georgopol reaches about 1 km. The first mock spread the towns over the whole pad (Gavansk at 1.1 km), which read as scattered houses.

**The building kit (first pass, our pick):** about 700 buildings in the 12 towns and villages, from 25 town building types and 7 one-off landmarks, plus 18 farmsteads in the fields around them:

| Building | Footprint | Floors | In the mock | Variants |
| --- | --- | --- | --- | --- |
| Two-story house | 11 × 9 m | 2 | 176 | 6 |
| Small house | 9 × 8 m | 1 | 159 | 5 |
| Townhouse row | 18 × 9 m | 3 | 87 | 4 |
| Apartment block, small | 30 × 12 m | 3 | 48 | 3 |
| Apartment block, large | 60 × 12 m | 5 | 12 | 2 |
| Shop | 12 × 10 m | 1 | 47 | 3 |
| Café or canteen | 14 × 10 m | 1 | 26 | 2 |
| Hotel | 40 × 14 m | 4 | 8 | 2 |
| Petrol station | 22 × 14 m lot, 8 × 6 m kiosk under a canopy | 1 | 5 | 1 |
| Market hall | 30 × 20 m, curved roof | 1, tall | 2 | 1 |
| Bus station | 22 × 12 m, 26 m platform canopy | 1 | 2 | 1 |
| Church | 22 × 12 m | 1, tower | 7 | 2 |
| Post office | 16 × 12 m | 1 | 7 | 1 |
| Police station | 26 × 16 m, walled yard | 2 | 5 | 1 |
| Polyclinic | 30 × 14 m | 2 | 4 | 1 |
| School | 40 × 14 m, 18 × 12 m gym | 2 | 4 | 1 |
| Medical post | 12 × 9 m | 1 | 4 | 1 |
| Fire station | 24 × 18 m, three engine bays, 18 m hose tower | 2 | 3 | 1 |
| Town hall | 24 × 16 m, columned porch | 2 | 3 | 1 |
| House of Culture | 32 × 22 m, colonnade, stage tower | 2, tall | 2 | 1 |
| Savings bank (holds a town vault) | 20 × 14 m | 2 | 2 | 1 |
| Garage row | 30 × 6 m, 8 lock-up garages | 1 | 26 | 2 |
| Boathouse | 10 × 14 m, slipway | 1 | 21 | 2 |
| Warehouse | 30 × 18 m, loading dock | 1, tall | 17 | 2 |
| Workshop | 16 × 12 m | 1 | 16 | 2 |
| Farmhouse | 12 × 9 m | 2 | 18 | 3 |
| Barn | 24 × 14 m | 1, tall | 18 | 2 |
| Tool shed | 6 × 5 m | 1 | 18 | 2 |

- **Fields:** vineyards, fields, and orchards, mixed with woods and scrub ([Land around the towns](#land-around-the-towns)), with dirt farm tracks off the roads.
- **Farm buildings** also serve the 70 or so [farmsteads](#marina-farms-and-vaults) elsewhere on the island.
- **Landmarks (one each):** Vetrovo's watchtower and church on the point, Mostki's cathedral, Klyuchi's thermal baths, Gribovo's spa hotel, Tikhaya Bukhta's harbor office with the vault, and Verkhovye's church at the lookout.
- **The kit drawn (2026-11-23, our pick):** the planner's building canvas draws every type in 3D with a floor plan and its variants, about 63 models in all. What sets each apart:
    - **Homes:** plastered walls in pale yellow, cream, blue, pink, white or green, with tile, slate, or asbestos-cement roofs. Variants change the roof shape and color and add shutters, a balcony, a porch, a lean-to, a glassed veranda, or a flat roof terrace like Ischia's old houses.
    - **Apartment blocks:** the large one is the Soviet five-story panel block with four entrances and balconies; the small one is a three-story brick block with two entrances.
    - **Public buildings:** flat-roofed Soviet modern, with strip windows on the polyclinic and school. The town hall has a columned porch and a flagpole, the House of Culture a colonnade and a stage tower, and the fire station a tall hose-drying tower.
    - **Plans:** the front is at the bottom; houses have a hall with the stairs, blocks have a stairwell per entrance with two flats a side, and public buildings have a corridor with rooms off both sides.
    - **Signs:** plain Russian words, such as shop, post office, police, bank, school, and canteen, never brand names. No Red Cross emblem on the medical buildings.
- **On track with Erangel:** about 26 named building types and 25 places there; 28 types plus 7 landmarks and 23 places here. Teplov has more land, about 46 km² against Erangel's 33, which the fields use.
- **Idea:** Gribovo's real town has a mushroom-shaped rock in its bay, which could be a detail off the shore.

### Land around the towns

Not everything is farmland (owner, 2026-11-23): some of it is trees, woods, and scrub, like the real island. A 2025 wildfire study's land cover map of Ischia counts about 1,160 ha of vineyards, 540 ha of chestnut woods, 400 ha of oak woods, 340 ha of crops, 490 ha of scrub, garrigue, and bramble, 65 ha of pine, and 1,460 ha built up, out of about 4,600. So outside the towns, about a third is woods and a sixth is scrub, and vineyards cover more than three times the cropland.

| Cover | Where on Ischia | In a fight |
| --- | --- | --- |
| Vineyards | Terraces on the slopes, most of all around Forio, Panza, Serrara, and Barano | Rows on terraces with low stone walls: cover from one side, open along the rows |
| Fields | The flatter ground, mostly in the west | Open ground with crops, hedges, and walls |
| Orchards and olive groves | Next to the towns | Rows of small trees: some cover, easy to see through |
| Chestnut and oak woods | Higher up Epomeo (the Falanga chestnut wood is at about 600 m above Forio), and the Maddalena wood of holm oak and pine by Casamicciola | Thick trees and undergrowth: lots of cover, short sightlines |
| Pine woods | The old lava flows by Ischia Porto (the Fiaiano pine wood on the Arso flow, and the Mirtina pine wood) | Tall trunks with little undergrowth: long sightlines between the trees |
| Scrub and maquis | Rocky slopes and cliff tops, mostly on the south and west coasts | Waist- to head-high bushes: you can hide in it, but it stops no bullets |

**The third mock (our pick):** each town's surroundings mix these from what really surrounds it. Woods grow on the uphill side toward the mountain and thin out near the core, scrub grows toward rocky coasts, fields keep to the flatter side, orchards sit next to the core, and each kind clumps into patches 100 to 300 m across. The buildings and farmsteads stayed as in the second mock. Percent of the land around each town:

| Town | Vineyards | Fields | Orchards | Chestnut and oak | Pine | Scrub | Meadow |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Gavansk | 23 | 8 | 16 | 13 | 24 | 14 | 2 |
| Vetrovo | 41 | 14 | 19 | 5 | 0 | 16 | 5 |
| Klyuchi | 20 | 5 | 17 | 35 | 8 | 10 | 5 |
| Ternovka | 26 | 11 | 9 | 35 | 0 | 18 | 0 |
| Mostki | 16 | 8 | 22 | 8 | 25 | 20 | 0 |
| Gribovo | 30 | 10 | 16 | 6 | 10 | 28 | 0 |
| Tikhaya Bukhta | 20 | 9 | 10 | 15 | 16 | 30 | 0 |
| Verkhovye | 16 | 5 | 8 | 42 | 0 | 30 | 0 |
| Polyanka | 44 | 22 | 10 | 8 | 0 | 12 | 3 |
| Rybatsk | 20 | 10 | 16 | 0 | 0 | 53 | 0 |
| Kholmy | 39 | 19 | 13 | 22 | 0 | 7 | 0 |
| Ovsyanka | 46 | 25 | 9 | 8 | 0 | 12 | 0 |

- **Between the towns:** the same kinds cover the rest of the island: a belt of chestnut and oak woods around Epomeo below the plateau's tree line ([Heights](#heights-squashed-with-a-plateau)), pine near Gavansk, vineyard terraces on the lower slopes, and scrub along the south and west coasts.

### The full-map mock

**Everything together (2026-11-23):** the planner's building canvas puts the whole island on one 10 × 8 km map: the 12 towns from the third town mock, the 67 farmsteads where the graybox's farm tracks end (1 to 4 buildings each), the [spot layouts](#our-own-spots) above, every road, the river, the lake, and the tunnel from the [layout file](#layout-coordinates), the coast from [The coast](#the-coast), and land cover across the whole island. That's 1,057 buildings: 744 in the towns, 155 on farmsteads, and 158 at the spots, plus 44 containers. Town buildings that fell inside the spots' new grounds were taken out.

- **Land between the towns (our pick):** it follows [Land around the towns](#land-around-the-towns) by height: bare rock, scrub, and meadow on the plateau; chestnut and oak woods on the upper slopes; vineyards with woods lower down; and vineyards, fields, and orchards near the coast. Scrub thickens toward the cliffs, and pine woods grow on the lava flows by Gavansk. Across the island that comes to chestnut and oak woods 25%, vineyards 24%, meadow and grass 18%, scrub 14%, orchards 8%, fields 8%, pine 2%, and bare rock 1%. Inside Object 7's fence, scrub and meadow carry on between the runway, the loops, and the base.
- **Coast:** about 37.5 km around: cliffs 12.6 km, low rocky shore 15.1 km, beaches 4.9 km, and harbors 4.8 km.
- **Gentle curves (owner, 2026-11-23; our pick for how):** field edges and terrace rows bend with the land instead of running ruler-straight. Roads and tracks keep the layout file's route, but each long straight run gets a soft bend of up to about 100 m off the line, a stand-in until the real road bends go in ([Turning Ischia into terrain](#turning-ischia-into-terrain)). They stay exactly on the layout in the towns, at junctions, at the bridges, and at the spots' gates, and roads that share a stretch bend together. The layout file itself is unchanged.

### Layout coordinates

The v4 mockup as data, for the lead's map tool: [teplov-layout.json](../data/teplov-layout.json) (2026-11-22). Coordinates are kilometers from the map's north-west corner, x east (0 to 10) and y south (0 to 8). It holds:

- **Coastline:** the island and the Krepost islet, from NASA's ASTER water body data for Ischia, stretched to the map frame.
- **Places, spots, and vaults:** game and real names, with town radii.
- **Hills:** real and game heights.
- **Water:** the crater lake's outline, the river's centerline (widths 25 m to 60 m), and the three bridges.
- **Roads:** the ring road, secondary roads (including Tikhaya Bukhta's), the tunnel, the causeway, the seven farm tracks, 67 farmstead tracks, and local streets.

It's still the mockup: heights come from the table above, not real elevation data. The ring road here is about 20 km of gentle curves. The owner's picks (2026-11-22): the next pass uses real elevation data squashed to 40%, and the ring road keeps the real road's bends, about 30 km. The ring road through Ovsyanka, with Kholmy on a side road, is fine.

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

## Community maps (later)

Players could build and share their own maps with an add-on map editor and a workshop ([Custom games and mods](gameplay.md#custom-games-and-mods-later)).

## Night maps

Idea for night maps where flashlights and stealth matter. Night scopes like the StG 44's Vampir would shine there, and so would star rounds from grenade launchers, which light an area about 200 m across for about 40 seconds, and infrared star rounds that only show through night vision ([Attachments](attachments.md#ground-rounds-smoke-and-other-non-lethal-rounds)). Matches can now also run from late day into night, all night, or from night into morning ([Match flow](match-flow.md#time-passes)).

## Sources

- [Berardi and others, wildfire forecasting on Ischia (2025, PDF)](https://iris.uniroma1.it/bitstream/11573/1732770/1/Berardi_Forecasting-of-wildfire_2025.pdf) (land cover by hectare) · [Ischia.it: the Falanga wood](https://ischia.it/en/falanga-wood) · [Ischia.it: the Maddalena wood](https://ischia.it/en/maddalena-wood) · [Ischia.it: the Mirtina pine wood](https://ischia.it/en/pineta-mirtina) · [Ischia.it: the pine woods](https://booking.ischia.it/en/tour-services/in-the-green-of-the-pine-forests-2)
- [Geosciences (2023): the Maronti cliffs and beach](https://www.mdpi.com/2076-3263/13/10/313) (cliffs 50 to 120 m) · [EMODnet bathymetry, 2024 release](https://emodnet.ec.europa.eu/en/emodnet-bathymetry-dtm-2024-release) (about a 115 m grid)
- [Yacht Digest: the port of Ischia](https://www.yachtdigest.com/en/ports-campania/porto-di-ischia-porto) (a lake of about 100,000 m² before it was a harbor) · [Earth-prints: the opening of Ischia's natural harbour](https://www.earth-prints.org/entities/publication/7d71a41a-d1b2-4ba6-b82c-d41732cf3370) (1854)
- [Wikipedia: Hardened aircraft shelter](https://en.wikipedia.org/wiki/Hardened_aircraft_shelter) · [Air Power Australia: hardening air bases](https://www.ausairpower.net/APA-2008-02.html) · [Wikiwand: Corrective colony](https://www.wikiwand.com/en/articles/Corrective_colony) · [Atlas Obscura: Tskaltubo](https://www.atlasobscura.com/places/tskaltubo-abandoned-soviet-sanatorium-town) · [FB.ru: the Rozhnovsky water tower (Russian)](https://fb.ru/article/339172)
- [PUBG's official map images (GitHub: pubg/api-assets)](https://github.com/pubg/api-assets) · [PUBG Interactive Map: map comparison](https://pubgmap.io/compare.html) · [Beebom: Erangel's building types](https://beebom.com/everything-you-need-to-know-pubg-locations/amp/)

- [PUBG Wiki: Erangel (Classic)](https://pubg.wiki.gg/wiki/Erangel_(Classic))
- [Liquipedia: Erangel](https://liquipedia.net/pubg/Erangel_Remaster)
- [Wikipedia: Gozo](https://en.wikipedia.org/wiki/Gozo) · [Wikipedia: Ischia](https://en.wikipedia.org/wiki/Ischia) · [Wikipedia: Guernsey](https://ipfs.ssi.eecc.de/ipns/en.wikipedia-on-ipfs.org/wiki/Guernsey) · [Wikipedia (older copy): Guernsey](https://dlab.epfl.ch/wikispeedia/wpcd/wp/g/Guernsey.htm) · [Wikiwand: Fortifications of Guernsey](https://www.wikiwand.com/en/articles/Fortifications_of_Guernsey) · [Wikipedia: Föhr](https://en.wikipedia.org/wiki/F%C3%B6hr) · [Wikipedia: Lastovo](https://en.wikipedia.org/wiki/Lastovo) · [Wikipedia: Russky Island](https://en.wikipedia.org/wiki/Russky_Island)
- Ischia's layout: [Komoot: ring route around Ischia](https://www.komoot.com/it-it/smarttour/e1113852301/giro-dell-isola-di-ischia) (length and high point) · [ISTAT 2019 population, in The Economist's data](https://github.com/TheEconomist/covid-19-excess-deaths-tracker/blob/master/source-data/italy/archive/italy_population_source.csv) · peaks from OpenStreetMap, [via LinkSim](https://github.com/wilhel1812/LinkSim/blob/main/public/peak-tiles/v1/tiles/la_p40_lo_p13.json) · town points from GeoNames, [via vineyardbovines/geojson](https://github.com/vineyardbovines/geojson/tree/main/geojson/cities/ita/04), and [Who's On First](https://github.com/whosonfirst-data/whosonfirst-data-admin-it) · coastline for the mockup from the ASTER Water Body Database, [via is-on-water](https://github.com/NiciusB/is-on-water)
- [Epic: Landscape technical guide](https://dev.epicgames.com/documentation/unreal-engine/landscape-technical-guide-in-unreal-engine)
- [OpenStreetMap wiki: License use cases](https://wiki.openstreetmap.org/wiki/License/Use_Cases)
