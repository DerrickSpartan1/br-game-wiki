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
- [ ] **A dedicated server build** from the engine source. You'll need the GitHub account linked to your Epic account first ([Getting started](getting-started.md)).
- [ ] **Playtest with friends,** then fix the worst problems before adding more.
- [ ] **Red zones, care packages, and vaults** ([Match flow](../systems/match-flow.md#red-zones)).
- [ ] **Healing:** PUBG's six items become six slots with PUBG's numbers as the middle (bandages and first aid kits stop at 80, med kits heal to 100, and health fills in slowly), and each match rolls one Tarkov item per slot, a little better or worse; plus the boost bar ([Healing](../systems/healing.md)).
- [ ] **Generic names in game:** use the game names from the wiki, not the real ones, in data, menus, and text, and keep logos, maker's marks, and the Red Cross emblem off every model and texture ([Legal review](legal-review.md)).
- [ ] **Game names in the game:** the owner approved them, so read gun, armor, and cartridge names from [Game names](game-names.md) into the data, without changing the tables the tools already read.
- [ ] **Hand-made touches:** when a step has a part the owner can do by hand (in-game text, picking colors, placing things in the map editor, small model edits, recording sounds), offer it to him and log it ([Hand-made touches](legal-review.md#hand-made-touches)).
- [ ] **Time of day, weather, and the wrist watch** ([Match flow](../systems/match-flow.md#time-of-day-and-weather)).

## You: decisions

In rough order of what the game needs first:

- [ ] **Check the handling first pass:** spread, ready and ADS times, reloads, and speed per category, from PUBG's numbers ([Handling](../systems/handling.md)). They matter as soon as real models are in.
- [ ] **Attachment effects:** how much each muzzle, grip, and stock changes recoil, sway, and aim speed ([Attachments](../systems/attachments.md#attachment-slots)).
- [x] **Neck and groin:** both are hit zones now, with rules against lucky one-shots ([Hit zones](../systems/ttk.md#hit-zones)).
- [ ] **Shields:** check the first pass (2,900 damage, half an M60 belt; pistol only) and whether the flash shield uses the class slot ([Shields](../systems/class-items.md#shields)).
- [x] **Carry space:** 6 capacity per Tarkov slot ([Carry weight](../systems/armor.md#carry-weight)).
- [ ] **Crate ammo:** how many FRAG-12, dragon's breath, and lethal launcher rounds a crate holds, and FRAG-12's damage to vehicles.
- [x] **The first map's island:** Ischia ([Maps](../systems/maps.md#the-first-map-ischia)).
- [x] **First map scale:** 10 × 8 km, Ischia at true scale with ocean on the edges ([Maps](../systems/maps.md#the-first-map-ischia)).
- [x] **Monte Epomeo:** squashed to a plateau ([Maps](../systems/maps.md#heights-squashed-with-a-plateau)).
- [x] **Review the map spots:** approved on the v3 mockup ([Maps](../systems/maps.md#our-own-spots)).
- [x] **Vault keys:** one key fits all, used up on opening, dropped on death, with a small chance in care packages ([Vaults and keys](../systems/match-flow.md#vaults-and-keys)).
- [x] **Prison armory:** the first map's fifth vault ([Maps](../systems/maps.md#marina-farms-and-vaults)).
- [ ] **River:** check the first-pass route, crater lake, and three bridges on the v4 mockup ([Maps](../systems/maps.md#river)).
- [x] **Healing variants:** check the Tarkov items in each slot, their numbers, and the odds ([Healing](../systems/healing.md#variants)).
- [ ] **Map caps:** the per-map max for throwables and crate weapons ([Weapon pool](../systems/weapon-pool.md)).
- [ ] **Comeback:** what form a Gulag-style comeback takes ([Gameplay](../systems/gameplay.md#comeback-fight)).
- [ ] **Scrap machine:** whether it replaces in-match crafting, and what it sells ([Crafting](../systems/crafting.md#scrap-machine-idea)).
- [x] **In-game names** for guns and armor brands: our own makers and designations, plain attachment names, and our own armor, vehicle, and term names ([Legal review](legal-review.md#guns)).
- [x] **Game names:** check the 49 first-pass gun makers and the designation rule ([Game names](game-names.md)).
- [x] **Gun names sample:** check the four pilot guns' game names before the rest are done ([Gun names](game-names.md#gun-names)). Talk to a lawyer before selling the game.
- [x] **Armor names:** check the first-pass armor names: fortifications, trees and stones, weather, insects, and historic helmets ([Armor](game-names.md#armor)).
- [ ] **PUBG look and feel:** what to call the red zone, blue zone, and boost bar, and the victory line ([PUBG look and feel](legal-review.md#pubg-look-and-feel)).
- [x] **Frying pan twist:** it wears through after one or two hits, depending on the caliber, then works only as melee ([Melee](../systems/gameplay.md#melee)).
- [ ] **Server hosting,** once the game runs ([Servers](../systems/servers.md)).

## Planner (Claude chat): wiki work (say the word)

- [ ] **Next guns:** the Madsen ([LMG queue](queue.md#lmgs-in-progress)) and the Arisaka ([sniper queue](queue.md#snipers-in-progress)), then start the special category: bows, crossbows, and mortars.
- [ ] **Lookups:** energies for the rounds behind the 32 versions with no damage yet, each version's real bullet speed, the missing LMG fire rates, and attachment lists for the 5 gun pages without one ([Lookups](open-questions.md#lookups)).
- [ ] **Mockups:** the HUD, inventory, and menus as designs before they're built in Unreal.
- [x] **One model per version (owner, 2026-11-21):** every version should look like its own gun, so the M4, M4A1, AR-15, and so on each get their own model instead of sharing four looks. Shared parts (lower receiver, moving parts) can still be reused underneath. Update [One model per family](art-and-sound.md#one-model-per-version) and step 2 of the [M16 / M4 model guide](m16-m4-model.md) with what tells each version apart at a glance, and log the decision. The lead builds the M4A1 base model first and holds the other versions until then.
- [x] **Game names:** all 625 gun versions, plus a first pass at armor names; vehicle names when vehicles are added ([Game names](game-names.md)).
- [ ] **Bayonet lugs:** mark which gun versions really had a bayonet lug, so they can spawn with a bayonet ([Melee](../systems/gameplay.md#melee)).
- [ ] **Bots:** how bots fill the lobby and stay to fill empty slots ([Pre-match lobby](../systems/match-flow.md#pre-match-lobby)): how they move, loot, fight, and how good they are. The lead's lobby code leaves a spot for them.
- [ ] **First-person view and the player character (owner, 2026-11-22):** the M4A1 is in the game and in hand; next the owner wants the character model and how guns are held in first person to look like PUBG's first person (search "pubg first person"): the gun low and to the right, angled in, with the left hand on the handguard from below and the sights close to the screen center. Two PUBG screenshots are in the game repo at `Art/Reference/FirstPerson/` (reference only). Please write up on [Gameplay](../systems/gameplay.md) the first-person look (field of view, where the gun sits at the hip and in ADS, arm and sleeve look) and which character the game uses until the [robot characters](idea-inbox.md#robot-character-concept) (Unreal's mannequins for now?), so the lead can brief the animator.
- [ ] **Lighting look (owner, 2026-11-22):** the owner doesn't want super realistic lighting and reflections for now; guns looked too shiny under Unreal's default range lighting. Please file it with the low-poly style on [Art and sound](art-and-sound.md): how lighting, reflections and shadows should feel (closer to PUBG 2017–2018, softer and flatter?), so the lead can set the project's lighting and reflection settings to match. Meanwhile the lead makes the gun materials more matte (rougher, less metallic).
- [ ] **Healing calls the lead made (2026-11-21), to file or change on [Healing](../systems/healing.md):** placeholders in the game until the wiki sets them: weights of bandages, first aid kits, energy drinks and painkillers (2 / 10 / 4 / 10); which slot a ground med spawn is (bandage 30, first aid 24, med kit 5, energy drink 22, painkillers 16, adrenaline 3) and bandages in stacks of 5; 1 adrenaline-slot item per care package (the Loot page's crate list doesn't have it yet); vault meds (2 first aid kits, 1 med kit, 1 adrenaline). Rules read one way: getting knocked empties the boost bar and stops health filling in; heal items can't be used at their cap even if they also boost; using adrenaline for a quick teammate pickup uses up the item and gives its boost to the teammate; the pocket first aid kit heals 70 points, still capped at 80; only firing, getting knocked, the parachute and vaults cancel healing (should reloading, aiming, switching weapons or jumping cancel it, as in PUBG?); boost speed counts only when running. Still open on the wiki: walking speed while healing, and whether the blood substitute injector cuts gas damage.
- [x] **Art style: low poly (owner, 2026-11-21):** guns (and likely the rest) aim for a low-poly look for now: chunky, flat-sided shapes with hard edges and clear outlines, the basics right but not ultra realistic. There won't be low-poly examples of every gun, so real photos set the shapes and proportions, and the low-poly style sets how much detail goes in. The owner's four style examples are in the game repo at `Art/Weapons/M16M4/Reference/Style/` (style only, source unknown, never copied). File it on [Art and sound](art-and-sound.md) and log the decision.
- [x] **M4A1 materials (owner OK'd, 2026-11-21):** the M4A1's quad rail uses aluminum, like the real KAC rail, not polymer as step 6 of the [M16 / M4 model guide](m16-m4-model.md) says (polymer stays for plastic handguards), and the buffer tube and charging handle are aluminum too. Update step 6's text.

## Later

- [ ] Epic Online Services (free): matchmaking, voice, and Easy Anti-Cheat.
- [ ] A Steam page ($100 through Steam Direct).
- [ ] The robot characters, once the mannequins have done their job ([Robot character concept](idea-inbox.md#robot-character-concept)).
