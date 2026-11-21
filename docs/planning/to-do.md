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

## You: art

- [ ] **Build the M16 / M4 model** with the [M16 / M4 model guide](m16-m4-model.md), starting with its setup prompt.
- [ ] **Then the other three pilot guns:** the [M1911](../weapons/pistols/m1911.md), [Minimi / M249](../weapons/lmgs/minimi.md), and [M1 Garand](../weapons/battle-rifles/m1-garand.md) ([Pilot](art-and-sound.md#pilot-four-guns-first)).
- [ ] **Pick gunshot and gun sounds by ear** as each pilot gun goes in ([Sound](art-and-sound.md#sound)).

## For the lead (Claude Code)

When you tell the lead "check the planner's list," it works through this section in order and tells you what's done.

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

- [ ] **The plane, parachutes, and zone** from [Match flow](../systems/match-flow.md): a random plane path, PUBG-style parachutes in third person, and Erangel's zone phases with the damage that grows outside the zone.
- [ ] **A graybox map:** Ischia's layout in blocks and ramps before art: coastline, squashed hills and the plateau, ring road, town spots, Marina, farm huts and tracks, our own spots, and the vaults ([Maps](../systems/maps.md#the-first-map-ischia)).
- [ ] **A dedicated server build** from the engine source. You'll need the GitHub account linked to your Epic account first ([Getting started](getting-started.md)).
- [ ] **Playtest with friends,** then fix the worst problems before adding more.
- [ ] **Zone events, care packages, and vaults** ([Match flow](../systems/match-flow.md#zone-events)).
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
- [ ] **Prison armory** as a fifth vault, plus the per-map caps for throwables and crate weapons ([Maps](../systems/maps.md#marina-farms-and-vaults)).
- [ ] **In-game names** for guns and armor brands: real, PUBG-style, or fictional. Talk to a lawyer before selling the game.
- [ ] **Server hosting,** once the game runs ([Servers](../systems/servers.md)).

## Planner (Claude chat): wiki work (say the word)

- [ ] **Next guns:** the Madsen ([LMG queue](queue.md#lmgs-in-progress)) and the Arisaka ([sniper queue](queue.md#snipers-in-progress)), then start the special category: bows, crossbows, and mortars.
- [ ] **Lookups:** energies for the rounds behind the 32 versions with no damage yet, each version's real bullet speed, the missing LMG fire rates, and attachment lists for the 5 gun pages without one ([Lookups](open-questions.md#lookups)).
- [ ] **Mockups:** the HUD, inventory, and menus as designs before they're built in Unreal.

## Later

- [ ] Epic Online Services (free): matchmaking, voice, and Easy Anti-Cheat.
- [ ] A Steam page ($100 through Steam Direct).
- [ ] The robot characters, once the mannequins have done their job ([Robot character concept](idea-inbox.md#robot-character-concept)).
