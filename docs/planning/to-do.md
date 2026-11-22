# To-do

What's left to do, grouped by who does it ([AI team](ai-team.md)). Tell the planner (Claude chat) when something's done, and it gets ticked here. The full list of undecided questions is on [Open questions](open-questions.md), and the original build order is on [Getting started](getting-started.md#7-build-the-first-playable-in-this-order).

## You: setup (do this first)

Set up the [AI team](ai-team.md): the workers, the lead, and reaching the lead from your phone.

- [ ] **Update and sign in:** in a terminal on your PC, run `claude update`, then make sure Claude Code is signed in with your claude.ai account (`/login`), not an API key.
- [ ] **Create the team:** paste the setup prompt from [Create the team](ai-team.md#2-create-the-team) into Claude Code in the game repo. Check that `/agents` lists the six workers.
- [ ] **Keep the PC awake:** in Windows Settings, under System, then Power & battery, set it to never sleep when plugged in.
- [ ] **Start the lead:** in the game repo folder, run `claude --remote-control "BR Lead"`. Open the Unreal editor and Blender too when there's art or editor work.
- [ ] **Turn on in `/config`:** "Enable Remote Control for all sessions," "Push when actions required," and "Push when Claude decides."
- [ ] **Connect your phone:** in the Claude app, tap Code and pick "BR Lead" (green dot means online). After a restart, run `claude --continue` in the game repo to bring it back.
- [ ] **Optional:** turn on Require trusted devices in your claude.ai account settings.
- [ ] **First job:** from your phone, tell the lead "check the planner's list."
- [x] **Accept the Epic Games invite on GitHub:** done 2026-11-21; the lead can see the Unreal source now.

## You: art

- [ ] **Build the M16 / M4 model** with the [M16 / M4 model guide](m16-m4-model.md), starting with its setup prompt. Started 2026-11-21: the lead runs the steps with its workers; you judge each check by eye and OK the reference downloads.
- [ ] **Then the other three pilot guns:** the [M1911](../weapons/pistols/m1911.md), [Minimi / M249](../weapons/lmgs/minimi.md), and [M1 Garand](../weapons/battle-rifles/m1-garand.md) ([Pilot](art-and-sound.md#pilot-four-guns-first)).
- [ ] **Pick gunshot and gun sounds by ear** as each pilot gun goes in ([Sound](art-and-sound.md#sound)).

## For the lead (Claude Code)

When you tell the lead "check the planner's list," it works through this section in order and tells you what's done.

**Lead's report, 2026-11-21** (for the planner to check against the game repo's commits and tick):

- Done: catching the game up with the wiki (`f5dbd13`, `6cf8d67`); handling, weights, and hit zones (`c2b386b`, `cac2e83`); the plane, parachutes, and zone (`b3aeab8`, `932027f`, data tables imported in `c7dffc8`); red zones, care packages, and vaults (`d85b077`, `1df5faf`).
- Done: the pre-match lobby and its countdown, and the game caught up with the red zones redesign (Bombardment, Smoke, Gas, and a slot for the air raid siren sound) (`3d749f5`). With that, "the lobby, plane, parachutes, and zone" is complete.
- Lobby calls the lead made that aren't on the wiki yet, for the planner to file or change: until bots exist, the countdown starts once everyone the matchmaker sent has joined, or after a 60-second no-show wait (owner OK'd 60 s, 2026-11-21); a running countdown keeps going if players leave; nobody takes damage before the plane; anything picked up in the lobby is taken away at boarding. The siren plays from the red zone's center; the wiki doesn't say how far it carries.
- M4A1 blockout done (`4276bb5`). Open question for the owner and planner: should each version share the M4A1's lower receiver and moving parts (fix once, fixes all), or be a full copy? The lead recommends sharing them.
- Next for the lead, in order: the graybox map, healing with variants, then time of day and weather.
- Pushed 2026-11-21: all the commits above are on GitHub. The Epic invite is accepted, so the dedicated server build is unblocked (engine source 5.8.4, to match the installed editor; the lead asks the owner before the big download). The M4 model has started (see You: art): the base M4A1 first, then the other versions once the planner sets how each one looks.
- Waiting on the planner: how bots fill empty slots (see Planner).

**Lead's report, 2026-11-22** (game repo commits are local, not pushed yet):

- Done: **healing** with match-rolled variants and the boost bar (`fc9e273`, `0d3c9bb`, `8f6d827`, review fixes `50ad786`, `3b48581`). Its placeholders are in the Planner item "Healing calls the lead made".
- Done: **the dedicated server build.** Engine source 5.8.4 built with MSVC 14.44 (14.52 breaks it), the game packages as `BRGameServer.exe` and runs a full match with two clients joining (`202f7c8`, `5845830`, `4f2cbd4`, `a712046`). `Start-LocalMatch.ps1 -PackagedServer` runs it. Clients from the launcher editor need a network version override until clients are packaged from the same engine.
- M4A1, steps 4 to 8 of the model guide: detail pass, materials and UVs, rig with a folding rear sight, export, import, Unreal materials, moving parts in game (bolt, trigger, selector, bolt catch, dust cover, rear sight), the box mag anim set with left-hand IK in both views, the mag leaving with the hand and the bolt slamming forward on empty reloads. Still open in step 8: muzzle flash and shells, and a proper first-person reload animation (the template reload reads as a hand wave in first person).
- Done in part: **first person and lighting.** The field of view setting (`FOV`, 80–103, default 90), ADS that centers the sight, the PUBG-style hip hold, and the lighting look on the range (Metallic 0 gun materials, soft sun, haze, locked exposure, no motion blur). Left: a slider once there's a settings menu, the arms and sleeves, and the bare-steel material slot.
- Reloads are built so staged reloads can resume from a saved step; the rule waits for the Planner item "Staged reloads".
- Next for the lead: muzzle flash and shells, or the first-person reload animation (owner to pick), then the graybox map, then time of day and weather.

**Lead's report, 2026-11-22, evening** (all pushed to GitHub, up to `5eb6444`):

- Done: **step 8 of the M4 model guide.** Muzzle flash and spent cases on every gun (`2deac9b`); a first-person reload layer and authored first-person M4A1 reloads, where the gun tilts, the old mag drops, a fresh mag comes from the chest pouch, and the thumb presses the bolt catch on empty reloads (`62ca327`, `27d4b90`, `a955aad`, grips set by the owner in `5eb6444`). Also: the first-person reload follows view pitch, and the first-person arms got their own materials so hands near the eye no longer tear (`7853f89`, `e3ba167`).
- Done: **dropped mags and casings** (owner, logged in [Staged reloads](../systems/handling.md#staged-reloads)). They stay about 10 s, even after you switch guns, and a reload cancelled before the mag comes out drops nothing (`7853f89`). Until staged reloads are built, a reload cancelled after the drop shows the gun with a mag again.
- **First playtest, 2026-11-22.** The owner tests with a checklist page after each stretch of work, about once a day. Good: range start, lighting, ADS, moving parts, recoil, flash, shells, reloads with rounds left, the reload staying put while looking around. "Good enough for now": mag drop, the empty reload, others' reloads. Not tested yet: healing, armor, dummies, knockdowns, zone, red zone, attachments, the local match. Fixes the lead takes on:
    - The M4A1 reads too rounded; go back to a squarer low-poly shape, then redo its colors (they look too alike in hand).
    - A gun on the ground loses its materials; it must keep them.
    - The range's gun pedestals should let you pick a specific weapon, not only roll one.
    - The empty reload's bolt-catch press looks odd; change it to a clean press or the M4 "slap" on the bolt catch.
    - Clearer steps for starting a local match, and a way to slow the game down for checks (the owner didn't know `slomo`).
    - Fresh guns spawn unloaded with the bolt forward, and the first reload still plays the bolt-catch press; the owner is fine with that.
- **For the planner (owner, 2026-11-22):**
    - **A semi-playable test mode**, for later: a way to enter a small arena and fight a bot, so armor and healing can be tested in a real fight. Please write it up (how you get in, what the bot does, what loadouts you get), and how it connects to the bots design.
    - **Weapon sway:** research whether PUBG (2017–2018) has weapon sway at the hip and in ADS, how much, and whether it changes with stance, breathing, or holding breath, so the handling page can say what ours does.
    - **The player character:** the white Unreal mannequin makes it hard to judge how the gun is held. The owner wants a real player model in before judging the hold. Which character, and in what order (arms and sleeves first?), per [Your character](../systems/skins.md#your-character).
    - **A settings menu**, so the field of view (and later keys and sensitivity) can be changed in game. The owner will test the FOV there.
- Next for the lead: the fixes above (M4A1 squarer, materials on dropped guns, pedestal picker, bolt-catch press, test instructions), then the graybox map, then time of day and weather.
- **Two staged-reload questions for the planner (lead, 2026-11-22):**
    - **Revolvers:** the game used to load them one round at a time; the Staged reloads table gives `revolver` a whole reload in three stages (cylinder out 35%, new rounds in 50%, closed 15%), and the lead's build follows the table. The owner says revolvers keep their progress either way. Should gate-loaded revolvers (no swing-out cylinder) load one round at a time while swing-out or break-top ones use the stages? If so, mark which revolvers are which, or add a reload style for them.
    - **Belt "from empty":** the lead read "the last 15% is charging the gun" as stages of 40% / 45% / 15% (the new belt's stage gives up its last 15%). Please confirm or correct it on the page.
    - **When does a reload count as done?** Staged reloads are built (`c76dcab`): the server takes the old mag out at the end of stage 1 and loads the new rounds at the end of the last loading stage, so a box mag reload with rounds left only counts at 100%. But the animations seat the new mag earlier (60% in third person, 82% in first person), so sprinting right after the mag seats makes the seated mag vanish again. Should a reload count as done once the new mag seats, with a short "back to ready" stage that can be cancelled for free (PUBG's feel)? Or only at the very end (then the lead retimes the clips so the mag seats at the end)? Until you answer, it counts only at the end.
- **Game names questions for the planner (lead, 2026-11-22):** the data tools now read [Game names](game-names.md) into the weapon and armor tables (all 625 versions and 133 armor pieces named). Open:
    - **Family names:** the game shows a family label (e.g. "AK-47 / AKM") on gun cards and prompts, but the page only names versions. Should each family get a game name, or should the game show only the version's game name?
    - **Two cartridges are TBD:** ".45 Remington–Thompson" (Thompson v5) and "6.5mm Fedorov" (Fedorov Avtomat v2). Until named, those show the version name with no cartridge label rather than the real one.
    - **Names the review flagged against the page's own rules:** "Oka Buran" (SR-3 Vikhr) uses "Buran", which the Vehicles section lists as a real brand to avoid; "Pichler P-19" and "P-20" (Glock 17 / 18) use numbers that are real Glock models; "Northway NW-45 Liberator" keeps the real nickname. Keep or rename?
    - **Real names inside the data:** even once every screen shows game names, the game's gun and armor tables keep the real names as internal keys (row names like `glock_17_18_04`, version, family, cartridge and armor names). OK for the private build, with a note for the lawyer pass ([Legal review](legal-review.md))?

- [ ] **Catch the game up with the wiki.** As of 2026-11-21 the game's data still has four armor tiers and the MG 42 as an LMG. The prompt:

```text
Wiki changes to pick up, then regenerate the weapon and armor data tables:
1. Armor now has three tiers at 30/40/55% (Systems > Armor). Update
   Tools/ArmorData/build_armor_data.py for the current plate carrier,
   fixed vest, plate, chest rig, and helmet tables, whose tier cells now
   run 1-3 (fixed vests can read "2 or 3" or "2-3"), and set the
   placeholder reductions to 30/40/55.
2. The MG 42 / MG3 page moved from weapons/lmgs to weapons/crate, so that
   family is now the Crate category.
3. More versions are crate-only now: the MG 34/41, M2010, Remington 700
   .300, and AWM .300, on top of the M24A3 and AWM .338.
4. Damage changed on the PPSh-41 family, Glock 18, M249, Janz, and
   Winchester 1887 10 gauge.
```

- [ ] **Handling, weights, and hit zones into the game.** The prompt:

```text
Wiki additions to pick up: Systems > Handling, Ammo > Weight,
Armor and gear > Carry weight, and TTK > Hit zones.
1. Extend the weapon data generator so each version gets its category's
   hip spread, ready time, ADS time, and sprint speed, and its reload
   times from the style in its Reload column, all from the Handling
   page's tables.
2. Add ammo weight per round (by round energy, from the Ammo page's
   Weight table) and the backpack, rig, and throwable numbers from
   Carry weight, as placeholders in Project Settings until the owner
   confirms them.
3. Damage now has six hit zones: head, neck, chest and stomach, groin,
   arms, and legs. The neck is 0.7 x the head multiplier and takes the
   higher tier of the helmet and the vest's neck coverage; the groin
   uses the body multiplier and only vests that cover the groin. Hands
   and feet count as arms and legs.
```

Then the build order that's left:

- [ ] **The lobby, plane, parachutes, and zone** from [Match flow](../systems/match-flow.md): the pre-match lobby and countdown, a random plane path from off the map, PUBG-style parachutes in third person, and Erangel's zone phases with the damage that grows outside the zone.
- [ ] **A graybox map:** Ischia's layout in blocks and ramps before art: coastline, squashed hills and the plateau, ring road, town spots, Marina, farm huts and tracks, the river and crater lake with their bridges, our own spots, and the vaults ([Maps](../systems/maps.md#the-first-map-ischia)).
- [x] **A dedicated server build** from the engine source. You'll need the GitHub account linked to your Epic account first ([Getting started](getting-started.md)).
- [ ] **Playtest with friends,** then fix the worst problems before adding more.
- [ ] **Red zones, care packages, and vaults** ([Match flow](../systems/match-flow.md#red-zones)).
- [x] **Healing:** PUBG's six items become six slots with PUBG's numbers as the middle (bandages and first aid kits stop at 80, med kits heal to 100, and health fills in slowly), and each match rolls one Tarkov item per slot, a little better or worse; plus the boost bar ([Healing](../systems/healing.md)).
- [ ] **Generic names in game:** use the game names from the wiki, not the real ones, in data, menus, and text, and keep logos, maker's marks, and the Red Cross emblem off every model and texture ([Legal review](legal-review.md)).
- [ ] **Game names in the game:** the owner approved them, so read gun, armor, cartridge, vehicle, and place names from [Game names](game-names.md) into the data, without changing the tables the tools already read.
- [ ] **Hand-made touches:** when a step has a part the owner can do by hand (in-game text, picking colors, placing things in the map editor, small model edits, recording sounds), offer it to him and log it ([Hand-made touches](legal-review.md#hand-made-touches)).
- [ ] **Time of day, weather, and the wrist watch** ([Match flow](../systems/match-flow.md#time-of-day-and-weather)).
- [ ] **HUD fixes (planner's review of the pushed HUD, 2026-11-22; skip any already done):**
    - **Names over heads for squadmates only.** Right now every player's name shows within 100 m, through walls, which gives enemies away.
    - **Minimap from a fixed map image,** with icons for you, your squad, pings, and the zone. The live top-down camera shows enemies from above and costs frames.
    - **Players alive from the server** (the game state), since a client only knows the players near it.
    - **Melee in hand** shows the owned melee weapon's name, not "FISTS" ([Melee](../systems/gameplay.md#melee)).
    - **Still to add from PUBG's layout:** the squad panel at the bottom left (names, colors, health, knocked); the zone timer and distance, with a run line on the minimap; the full map on M with a grid and the plane's path; the kill feed at the top right and a "you killed" line in the center; hit markers; the throwable count in slot 5; and vehicle speed and fuel once vehicles are in.
    - **Our own look:** our own fonts, icons, and colors, never PUBG's ([Legal review](legal-review.md#pubg-look-and-feel)).
- [ ] **Menus:** PUBG's layout with our art: Play, Wardrobe, Career, Replays, and Settings, with the character and squad in the middle ([HUD and inventory](../systems/gameplay.md#hud-and-inventory)).
- [ ] **First person and lighting:** set the field of view slider, the hip and ADS gun positions, and the arms from [First person](../systems/gameplay.md#first-person), and the materials, exposure, haze, and post effects from the [Lighting look](art-and-sound.md#lighting-look). Show the owner the M4A1 at the range before and after.

## You: decisions

In rough order of what the game needs first:

- [x] **Check the handling first pass:** spread, ready and ADS times, reloads, and speed per category, from PUBG's numbers ([Handling](../systems/handling.md)). They matter as soon as real models are in.
- [x] **Attachment effects:** how much each muzzle, grip, and stock changes recoil, sway, and aim speed ([Attachments](../systems/attachments.md#attachment-slots)).
- [x] **Neck and groin:** both are hit zones now, with rules against lucky one-shots ([Hit zones](../systems/ttk.md#hit-zones)).
- [x] **Shields:** check the first pass (2,900 damage, half an M60 belt; pistol only) and whether the flash shield uses the class slot ([Shields](../systems/class-items.md#shields)).
- [x] **Carry space:** 6 capacity per Tarkov slot ([Carry weight](../systems/armor.md#carry-weight)).
- [ ] **Crate ammo:** how many FRAG-12, dragon's breath, and lethal launcher rounds a crate holds, and FRAG-12's damage to vehicles.
- [x] **The first map's island:** Ischia ([Maps](../systems/maps.md#the-first-map-ischia)).
- [x] **First map scale:** 10 × 8 km, Ischia at true scale with ocean on the edges ([Maps](../systems/maps.md#the-first-map-ischia)).
- [x] **Monte Epomeo:** squashed to a plateau ([Maps](../systems/maps.md#heights-squashed-with-a-plateau)).
- [x] **Review the map spots:** approved on the v3 mockup ([Maps](../systems/maps.md#our-own-spots)).
- [x] **Vault keys:** one key fits all, used up on opening, dropped on death, with a small chance in care packages ([Vaults and keys](../systems/match-flow.md#vaults-and-keys)).
- [x] **Prison armory:** the first map's fifth vault ([Maps](../systems/maps.md#marina-farms-and-vaults)).
- [x] **River:** check the first-pass route, crater lake, and three bridges on the v4 mockup ([Maps](../systems/maps.md#river)).
- [x] **Healing variants:** check the Tarkov items in each slot, their numbers, and the odds ([Healing](../systems/healing.md#variants)).
- [x] **Map caps:** the per-map max for throwables and crate weapons ([Weapon pool](../systems/weapon-pool.md)).
- [ ] **Comeback:** what form a Gulag-style comeback takes ([Gameplay](../systems/gameplay.md#comeback-fight)).
- [x] **Scrap machine:** it's in-match crafting, done at workbenches with scrap ([Workbenches](../systems/crafting.md#workbenches)).
- [x] **In-game names** for guns and armor brands: our own makers and designations, plain attachment names, and our own armor, vehicle, and term names ([Legal review](legal-review.md#guns)).
- [x] **Game names:** check the 49 first-pass gun makers and the designation rule ([Game names](game-names.md)).
- [x] **Gun names sample:** check the four pilot guns' game names before the rest are done ([Gun names](game-names.md#gun-names)). Talk to a lawyer before selling the game.
- [x] **Armor names:** check the first-pass armor names: fortifications, trees and stones, weather, insects, and historic helmets ([Armor](game-names.md#armor)).
- [ ] **PUBG look and feel:** what to call the red zone, blue zone, and boost bar, and the victory line ([PUBG look and feel](legal-review.md#pubg-look-and-feel)).
- [x] **Frying pan twist:** pans are class items that block only while raised and get holed after a set amount of gunfire ([Pans](../systems/class-items.md#pans)).
- [ ] **Server hosting,** once the game runs ([Servers](../systems/servers.md)).

## Planner (Claude chat): wiki work (say the word)

- [ ] **Next guns:** the Madsen ([LMG queue](queue.md#lmgs-in-progress)) and the Arisaka ([sniper queue](queue.md#snipers-in-progress)), then start the special category ([Special queue](queue.md#special)).
- [ ] **Lookups:** energies for the rounds behind the 32 versions with no damage yet, each version's real bullet speed, the missing LMG fire rates, and attachment lists for the 5 gun pages without one ([Lookups](open-questions.md#lookups)).
- [ ] **Mockups:** the HUD, inventory, and menus as designs before they're built in Unreal.
- [x] **One model per version (owner, 2026-11-21):** every version should look like its own gun, so the M4, M4A1, AR-15, and so on each get their own model instead of sharing four looks. Shared parts (lower receiver, moving parts) can still be reused underneath. Update [One model per family](art-and-sound.md#one-model-per-version) and step 2 of the [M16 / M4 model guide](m16-m4-model.md) with what tells each version apart at a glance, and log the decision. The lead builds the M4A1 base model first and holds the other versions until then.
- [x] **Game names:** all 625 gun versions, plus a first pass at armor names; vehicle names when vehicles are added ([Game names](game-names.md)).
- [ ] **Bayonet lugs:** mark which gun versions really had a bayonet lug, so they can spawn with a bayonet ([Melee](../systems/gameplay.md#melee)).
- [x] **Staged reloads (owner, 2026-11-22):** a reload keeps its progress. If you cancel partway (switch weapons, sprint, get knocked) after the old mag is out, the gun stays without a mag, and the next reload picks up from that point instead of starting over. Please write up on [Handling](../systems/handling.md) (reloads) and [Gameplay](../systems/gameplay.md): the stages per reload style (for a box mag: old mag out, new mag in, bolt released on an empty reload; also tubes, belts, en bloc clips, stripper clips, revolvers), what the gun can do between stages (can a chambered round still fire with the mag out?), where the rounds in a pulled mag go (back to the backpack, PUBG-style, or kept in that mag), how each stage's time is split from the version's reload time, and what cancels a reload. The lead's reload code already marks the mag-out, mag-in and bolt-release moments, so it can save the stage when a reload is cancelled.
- [ ] **Bots:** how bots fill the lobby and stay to fill empty slots ([Pre-match lobby](../systems/match-flow.md#pre-match-lobby)): how they move, loot, fight, and how good they are. The lead's lobby code leaves a spot for them.
- [x] **First-person view and the player character (owner, 2026-11-22):** the M4A1 is in the game and in hand; next the owner wants the character model and how guns are held in first person to look like PUBG's first person (search "pubg first person"): the gun low and to the right, angled in, with the left hand on the handguard from below and the sights close to the screen center. Two PUBG screenshots are in the game repo at `Art/Reference/FirstPerson/` (reference only). Please write up on [Gameplay](../systems/gameplay.md) the first-person look (field of view, where the gun sits at the hip and in ADS, arm and sleeve look) and which character the game uses until the [robot characters](idea-inbox.md#robot-character-concept) (Unreal's mannequins for now?), so the lead can brief the animator.
- [x] **Lighting look (owner, 2026-11-22):** the owner doesn't want super realistic lighting and reflections for now; guns looked too shiny under Unreal's default range lighting. Please file it with the low-poly style on [Art and sound](art-and-sound.md): how lighting, reflections and shadows should feel (closer to PUBG 2017–2018, softer and flatter?), so the lead can set the project's lighting and reflection settings to match. Meanwhile the lead makes the gun materials more matte (rougher, less metallic).
- [x] **Safe is for stowing only (owner, 2026-11-22):** there's no safe on the fire-mode key. A gun goes to safe only when it's stowed (for example, holding X to bring out melee), and when it comes back out it returns to the last fire mode chosen. That switch doesn't need animating yet; one day the draw animation will show the selector going from safe back to that mode. Please file it on [Gameplay](../systems/gameplay.md) (fire modes) and fix the step 8 check in the [M16 / M4 model guide](m16-m4-model.md), which says to switch the M4A1 "through safe, semi, and auto". The game already works this way: the selector sits at safe only while the gun is put away.
- [ ] **Test arena (owner, 2026-11-22):** a semi-playable mode for later: a small arena where you fight a bot, so armor and healing get tested in a real fight. How you get in, what the bot does, which loadouts you get, and how it ties into the bots design ([Lead's report](#for-the-lead-claude-code)).
- [ ] **Weapon sway (owner, 2026-11-22):** whether PUBG (2017–2018) had sway at the hip and in ADS, how much, and whether stance, breathing, or holding breath change it, so [Handling](../systems/handling.md) can say what ours does.
- [ ] **The player character (owner, 2026-11-22):** which model replaces the white mannequin, and in what order (arms and sleeves first?), so the gun hold can be judged ([Your character](../systems/skins.md#your-character)).
- [ ] **Settings menu (owner, 2026-11-22):** field of view first, then keys and sensitivity ([Menus](../systems/gameplay.md#hud-and-inventory)).
- [ ] **Staged reload questions (lead, 2026-11-22):** whether gate-loaded revolvers load one round at a time while swing-out and break-top ones use stages, and whether a belt reload from empty splits 40% / 45% / 15% ([Staged reloads](../systems/handling.md#staged-reloads)).
- [ ] **Healing calls the lead made (2026-11-21), to file or change on [Healing](../systems/healing.md):** placeholders in the game until the wiki sets them: weights of bandages, first aid kits, energy drinks and painkillers (2 / 10 / 4 / 10); which slot a ground med spawn is (bandage 30, first aid 24, med kit 5, energy drink 22, painkillers 16, adrenaline 3) and bandages in stacks of 5; 1 adrenaline-slot item per care package (the Loot page's crate list doesn't have it yet); vault meds (2 first aid kits, 1 med kit, 1 adrenaline). Rules read one way: getting knocked empties the boost bar and stops health filling in; heal items can't be used at their cap even if they also boost; using adrenaline for a quick teammate pickup uses up the item and gives its boost to the teammate; the pocket first aid kit heals 70 points, still capped at 80; only firing, getting knocked, the parachute and vaults cancel healing (should reloading, aiming, switching weapons or jumping cancel it, as in PUBG?); boost speed counts only when running. Still open on the wiki: walking speed while healing, and whether the blood substitute injector cuts gas damage.
- [x] **Art style: low poly (owner, 2026-11-21):** guns (and likely the rest) aim for a low-poly look for now: chunky, flat-sided shapes with hard edges and clear outlines, the basics right but not ultra realistic. There won't be low-poly examples of every gun, so real photos set the shapes and proportions, and the low-poly style sets how much detail goes in. The owner's four style examples are in the game repo at `Art/Weapons/M16M4/Reference/Style/` (style only, source unknown, never copied). File it on [Art and sound](art-and-sound.md) and log the decision.
- [x] **M4A1 materials (owner OK'd, 2026-11-21):** the M4A1's quad rail uses aluminum, like the real KAC rail, not polymer as step 6 of the [M16 / M4 model guide](m16-m4-model.md) says (polymer stays for plastic handguards), and the buffer tube and charging handle are aluminum too. Update step 6's text.

## Later

- [ ] Epic Online Services (free): matchmaking, voice, and Easy Anti-Cheat.
- [ ] A Steam page ($100 through Steam Direct).
- [ ] The robots as PvE enemies, starting with vault guards ([Robot guards](../systems/match-flow.md#robot-guards-idea)).
