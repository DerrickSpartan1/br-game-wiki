# Chat notes

Short dated notes from each chat with the owner, so the planner, the lead, and every check-in can see what was said without rereading whole conversations (owner asked, 2026-11-24). Newest first.

**How notes work:**

- **Notes, not transcripts.** Each chat gets a short entry: what the owner asked or said (in his own words for anything he decided), what was decided, what changed with links, and what's still open. Whole transcripts are too long to reread at every check-in, and this wiki is public, so everything typed in a chat doesn't belong on it.
- **Game only.** Nothing personal goes here, only what's about the game and how the team works.
- **Who writes them:** the planner after each chat with the owner, under **Planner chat**; the lead after each chat with the owner (phone or PC), under **Lead chat**. Playtest results stay in the game repo's `Docs/Playtest/`, and decisions still get their row on the [Decision log](decisions.md).
- **Who reads them:** every check-in reads the newest entries ([Check-ins](ai-team.md#check-ins)), and a new chat starts by reading the last few days.
- **Earlier chats** (before 2026-11-24) are written up below from the [Decision log](decisions.md), the [Changelog](changelog.md), and the [Picks archive](picks-archive.md), not from the chats themselves, so they carry no quotes. October is one entry.
- **Read only what you need:** the newest day or two at a check-in; older entries when a topic comes back.

## 2026-11-25

### Planner chat

- **Heist picks (00:05):** "i like cash balloon, yes i like gold bars being like extra valuable, those should slow you down but are a big payout. idk if it should show everyone on the map your position, but any sort of heist that shows alarm should show it on the map, i like castle museum and the moving convoy, i like farm, and yeah the robot response makes sense, maybe they come down in like a drop pod and climb out, one drop pod one drone kinda deal." New ideas: "also what about paintings?" and "we can do a diamond store or anything else." He asked to look at ROB RUN for more heistables; eight more ideas drafted from it and our own ([Mini heists](../systems/match-flow.md#mini-heists)).
- **Follow-up (00:12):** "i like your eight ideas, you can close the gold carrier on the map thats a no and maybe we want to up the cost of the cash balloon? that way it cant be spammed? that feels too safe." The eight are kept, carriers stay off the map, and the balloon went from 50 to 150 scrap, with a 45 s rise shown on the map and one a match as our pick.
- **The balloon (00:29):** "it can show on the map like an alarm but no noise, and it takes a little for the balloon to rise but the noise will be a plane coming to get it". It's silent and on the map like an alarm; a plane comes in to snag it, and the plane is the noise. Our pick: about 15 s to rise, the plane 30 s later.
- **Someone else's balloon (00:31):** "make it so it can be either you put your cash in it if its an enemy drop or you can cut the line and take it all, maybe a limit on how many planes?" Either one works on any balloon you reach before the plane. Our pick for the limit: 6 pickup flights a match, one plane at a time, then benches stop making balloons.
- **Still open:** the Exchange office's name, tip-offs, the ferry, the balloon's numbers, and the heist details, all for the next picks page.

## 2026-11-24

### Planner chat

- **Harbors:** "the ports im still not 100% on." Gavansk Port was redone as a round basin with a container quay, and Vetrovo Pier as a curved-breakwater harbor ([Maps](../systems/maps.md)).
- **Backpacks:** three tiers like armor, using Tarkov's real packs and others in their tiers. Picked on the picks page: capacity by tier with a spread, no slowdown, bird names ([Armor > Backpacks](../systems/armor.md#backpacks), [Game names](game-names.md)).
- **Picks:** the edge is the aurora; the menu accent is field lime, with the compass in the same color.
- **Playtest round 6:** the lead's planner items answered: first circles scaled to Teplov, bigger strike zones that shrink with the zone, the care package's plane, crate, parachute, and green smoke, hands that move with you, the throw arc, the interactive map, and a [Project layout](project-layout.md) page. The owner confirmed every round 6 pick.
- **Picks pages:** "When we do these please save a copy and remove the old ones and only post new." Answers now go to the [Picks archive](picks-archive.md), with copies in the repo's `archive/picks/`; the old pages were deleted.
- **Review rule:** "every todo item that gets handed back and forth need me to review." Nothing counts as done until he reviews it. The planner checked every To-do item against the commits and playtests, gave each a status, found twelve things that had no item, and posted a review page of 42 first passes he hadn't confirmed ([To-do](to-do.md)).
- **Check-ins:** the planner at :15 and :45, the lead at :00 and :30. "These check ins arenjust for them to keep updated with decsions questions andninfo and doesntnrequire my input." He chose to run the planner's on his PC ([Check-ins](ai-team.md#check-ins)).
- **Playtest round 7:** a [Sound list](sound-list.md); the parachute opens at 150 m with a switch to turn that off; the freefall readout; the damage flash; parties from the menu; knocked crawl 0.8 m/s. One choice is queued for the next picks page: what happens if you never pull.
- **His PUBG screenshots:** the freefall readout became two gauges either side of the screen's middle, and the full map got a teal wash outside the edge and a match log tab.
- **The lead's afternoon questions:** attachment weights by family, crates stay all match, bodies show worn gear, tap F loots and hold F revives a squadmate's body.
- **Coding practices:** "the lead needs it like coding practices and stuff." A [Coding practices](coding-practices.md) page with a checklist for the reviewer and the planner's read of the code.
- **Check-in problems:** the lead couldn't start its own check-in, so he types one `/loop` line after the lead adds its allow rules. The planner's task kept stopping for approval; the fix is Auto mode on the task.
- **This page:** "we should also have a section for where these chats are saved to file for you guys rto reference."
- **Still open:** the review page of 42 first passes; the never-pull choice; the planner task's Auto mode; the lead's allow rules and the `/loop` line.
- **Evening status check (23:07):** "alright how ar things?" Both check-ins are running and answering each other within minutes. The cloud check-in that makes picks pages was found switched off (since about 15:10), so the queued questions haven't become a page yet; asked him whether to turn it back on. Nothing on the review page is answered yet.
- **The cloud check-in:** he'd turned it off because "i thought its functions would be covered in the twice hourly". It's back on for picks pages only, as he asked: "maybe that one should be hourly?" It runs at :52 every hour from 9 AM to 11 PM.
- **Round 9 picks (23:31):** he ran the picks check-in by hand, and it posted a page with the parachute choice and the newer first passes. He OK'd them all but two. If you never pull: "You hit the ground and die." A part-loaded round: "No if youre part way through it defaults to the last saved reload whether that be the last buller or srep in reloading a mag." On no-gear capacity 70: "we will have a belt item thats customizable and all players get at the start to fix this." Bodies show worn gear "until the body disappears." Filed, archived, and the page deleted.
- **The review page (23:36):** "okay give me those 42." Six were dropped first, already settled: the revolver stop (changed today), med names, the boost pulse, armor durability, and eye height (all good in playtests), and the map colors (OK'd in round 9). 36 are left.
- **The 36 answered (23:45),** for the hourly picks check-in to file. **Cash:** "instead of scrap being the main currency cash is, scrap held at end of match gets converted to cash, but cash can be found in vaults and safes and cash registers and other places for people to loot. this way you can give a heisty type feel to things." Filed on [Cash](../systems/crafting.md#cash); the open calls (losing cash on death, drop-offs, weight, where it's found) were then OK'd in chat: "yeah i like all of this", and cash rides in "a little gym bag they carry on their back under their backpack and you dont have to worry about carry weight." No limit on the bag: "it can carry as much as you want, its that much more of a risk if you dont stash it, and we can do jewerly and stuff too for people to loot." Valuables: "it all gets converted to cash." Quest items: "thats where quest items go and quest items have to bve stashed." "get rid of the 5 minute timer for now, we will make drop offs decently available." "we can look at payday for like mini themed heist on teh map": six mini heists drafted, queued for the next picks page. Drills: "we use scrap to make the drills for a vault heist. or you have a key thats the trade off." Scrap's theme: "scrap to make makeshift stuuff or heist stuff or pay for otherthings in the game for scavenger feel." Timing: "we gotta think about the circle with these times too so 90 seconds might be too long"; the drill is now about 45 s with one stop. Then: "for the port heists maybe multiple crates open but some just have gear and so does the armored truck gear and money", and "feel free to look through other heist stuff or think of other stuff": eight more ideas drafted, all queued for the next picks page.

### Lead chat

- **Playtests:** rounds 6 and 7 answered and saved (game repo `Docs/Playtest/results-2026-11-24.md`); round 8 is on the form, with never-tested items brought back.
- **Review rule:** "every todo item that gets handed back and forth need me to review. and double check that weve done everything thats been reviewed back and forth so nothing is missing." The lead keeps `Docs/Playtest/review-tracker.md` in the game repo, updated after every review, and checked it against the planner's twelve found-missing items.
- **Pushes:** "you cna push once i give th eokay." The owner OK'd pushes after rounds 6 and 7; newer commits wait for his next OK.
- **Built today, waiting on his review (round 8):** bigger first circle and strike zones, backpack odds and carry weights from the wiki, the dotted throw arc, Esc closing screens first, armor worn not carried (defib in slot 4), bodies hold the loot with crates, hands that move with you and the melee ready hold.
- **His PC setup:** Python 3.12 and the wiki's build packages installed with his OK; the planner's check-in task created in `C:\Dev\planner`; he added the lead's allow rules himself and started the lead's `/loop` check-in.
- **Still open for him:** whether moving crouch and prone shots must match the server within 1 cm (they're within 5 cm now; still poses are within about 1 cm); pushing the newest commits.

## 2026-11-23

### Planner chat (rebuilt from the logs)

- **The map, in detail:** towns are dense cores like Erangel's (large towns about 550 to 600 m across) with fields and farmsteads around them; each town's layout gets mocked first, then a building kit of 25 types; the land between towns mixes vineyards, fields, orchards, woods, pine, scrub, and meadow from Ischia's real land cover (owner; the mix our pick); the coast gets cliffs, rocky shore, beaches, and harbor walls ([Maps](../systems/maps.md)).
- **Our own spots in full:** Object 7 is a fenced airbase across the plateau with its bunker linked underground to the road tunnel; the school, prison, port, quarry, spa, hospital, and farm got compound layouts and 15 building types. Then a pass for more curves, so not everything is square (owner asked).
- **Playtest rounds 3 and 4 answered** (his notes are in the game repo's `Docs/Playtest/results-2026-11-23.md`): 29+1 from empty and 30+1 with a round chambered for closed-bolt guns with detachable mags (owner); fists are a melee pick like the others (owner); every melee weapon can be thrown and picked back up (owner), aimed with right mouse and an arc (our pick); a HUD size slider (owner; 75% to 125% our pick); med names start with their slot (owner); iron sights sized like PUBG's M416's, armor durability from PUBG 2018, the boost pulse, the camera at the body's eyes, and the training map write-up (our picks).
- **Also:** the red zone siren carries about 300 m past the circle; lobby rules until bots exist.

## 2026-11-22

### Planner chat (rebuilt from the logs)

- **Four decision batches and the class items page** were answered on picks pages; every answer is on the [Picks archive](picks-archive.md). The big ones below.
- **The first map is named Teplov**, with our own Eastern European town and spot names; real elevation data and real road bends; the v4 mockup became a coordinates file for the lead's map tool.
- **Reloads:** revolvers load one round at a time with speed loaders as attachments; every belt reload is the full reload; mag-fed guns do the full reload only with an empty chamber; a cancelled reload keeps its progress; the old mag drops and disappears after about 10 seconds.
- **Guns:** weapon sway like PUBG's; safe isn't on the fire-mode key; the standard M14 is semi only, and real gas cut-offs go on the selector key; suppressors and the Krummlauf wear out; handling moved back to PUBG's numbers.
- **The comeback:** Warzone-style 1v1 duels, one redeploy (more with scrap), open for the first couple of circles, an underground arena, the same random gun for both, a capture point after 60 seconds. Bodies turn into crates once nobody can revive them.
- **Scrap and crafting:** one kind of scrap and in-match workbenches; everything you carry comes out of a match; quest items count after a few minutes.
- **Class items and special weapons:** twenty more class items approved; pans and breaching tools are class items; rocket launchers and mortars are crate-only class items; new special groups (black powder, underwater, air guns, survival guns, oddities).
- **Hazards and match:** red zone forms 1 in 6 each, including firebombing, creeping barrage, and EMP; a gas mask slot; about 5 care packages and 1 or 2 vehicle drops a match; 5 radar stations.
- **Armor:** leg armor gets its own slot and tiers; vests and helmets roll their real setups.
- **Our own words:** strike zone, the edge, Stim, and "The island is yours".
- **Look and feel:** first person like PUBG's; matte gun materials and plain lighting; low poly is for testing, the final game looks closer to PUBG with our own art; characters are humans you dress up (the robots are saved for something else).
- **Night and sky:** day for night with a locked exposure; five rules keep dark matches fair; the watch sits on the inside of the left wrist.
- **The vehicle lineup:** an Eastern Bloc stand-in for each PUBG vehicle, plus a tractor and a 6x6 truck.
- **Playtest round 1** (his notes in the game repo): the M4A1 squared up, pedestal version picker, Colors A.

## 2026-11-21

### Planner chat (rebuilt from the logs)

- **The AI team was set up:** Claude chat is the planner, Claude Code on his PC is the lead, with subagent workers ([AI team](ai-team.md)).
- **The first map:** Ischia's layout at true scale, 10 × 8 km with ocean around it, heights squashed to 40% and Monte Epomeo flattened to a plateau; a river from a crater lake; a new coastal town (Marina) and farm huts; vaults (4 to 6 a map, the Prison armory the fifth) and 2 or 3 keys a match.
- **Matches like PUBG's:** a random plane path, PUBG-style parachutes, Erangel's zone phases as placeholders, random care packages, red zones in several forms with an air raid siren, a pre-match lobby on the match's map, and time and weather that change during a match.
- **Armor:** three tiers at PUBG's 30%, 40%, and 55%; the crate line is one head shot through a tier 3 helmet, so the .300 Win Mag snipers and the MG 42 family are crate-only.
- **Healing like PUBG's:** six slots with Tarkov's real medical items as variants, bandages and first aid kits up to 80, slow fill.
- **Melee:** owned melee weapons brought into every match, all with the same numbers, lots of kinds; tap X to hit, hold X to run with it.
- **Names and legal:** all 625 gun versions got game names; 49 made-up gun makers approved; anything that could cause legal trouble gets a generic name; no Red Cross emblem; moving away from PUBG specifics in looks and marketing.
- **Art:** low poly for now, shapes from real photos, one model per version on a shared kit; the M4A1's colors approved.
- **Lots of features filed:** dog tags, outfits like PUBG's, ping, proximity chat, death cam, Easy Anti-Cheat, footprints, vehicles and ziplines, radar stations, wanted contracts, self-revive kits, keys and controls like PUBG's with X for melee.
- **The game stays private** for him and friends for now; he wants chances to make things by hand.

## 2026-11-20

### Planner chat (rebuilt from the logs)

- **The engine is Unreal Engine 5.8** in C++, moving to Unreal 6 later; Unity and Godot were compared and passed over.
- **Damage and fire rates follow PUBG:** damage set per gun version from PUBG anchors, real cyclic rates for automatics and PUBG's fixed rates for semi-autos, real bullet speeds and drop, shotguns from PUBG's 2018 pumps, and crate weapons decided by damage.
- **Reloads and ammo like PUBG's:** loose rounds in the backpack; every version gets Reload and Mag columns; tubes load one round at a time; stripper clips like the Kar98k's.
- **Loot like PUBG's,** but only the match's pool spawns; vests roll as combos of carrier, tier, plate, and rig; armor and helmets from Escape from Tarkov's real pieces.
- **Attachments:** PUBG's set, built-in parts stay on, bipods on cover or prone.
- **HUD and inventory** follow PUBG's 2017–2018 layout with our own look; slot 4 is the class item, slot 5 throwables, melee its own button.
- **Sound:** real sound speed and bullet cracks.
- **Art and tuning:** "good enough to get the feel down" for now, free tools first, and gun tuning waits for real models; the target is PUBG's gun feel from 2017–2018.

## October 2026

### Planner chats (rebuilt from the logs)

- **The ideas doc** came first (early October); the wiki was built from it and moved to GitHub (2026-10-12 to 10-14), starting with 67 gun pages, rules, systems, the ammo index, and planning pages.
- **Core gun rules:** no jamming and no overheating (flavor text only); recoil is random every time, with each gun's own personality; versions keep their real fire modes, semi-auto-only ones included; real conversion kits count as versions; en bloc clips ping and can't be topped off; the AUG's progressive trigger and the Mondragón's gas cut-off go on the selector key.
- **Family calls:** the Galil ACE stays with the Galil; the AK-107, AK-108, and AK-109 fold into the AK families; the HK416, AK-12, and CETME stay their own families.
- **Assault rifles were finished** (SCAR-L, HK416, ACR, SIG MCX, AK-12), then **battle rifles and DMRs became one category** and were added through the month: Mondragón, M1 Garand, SVT-40, FG 42, Gewehr 43, SKS, MAS-49, FN FAL, AR-10, SG 510, CETME, M14, HK G3, BM 59, SVD, Mini-14, VSS, SR-25 / M110, QBU-88, Mk 12, SCAR-H, and HK417.
- **Ideas filed:** a robot player character concept (later saved for something else) and wire fences with wire cutters.
