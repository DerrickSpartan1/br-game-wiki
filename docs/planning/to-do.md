# To-do

What's left to do, grouped by who does it. Tell Claude in chat when something's done, and it gets ticked here. The full list of undecided questions is on [Open questions](open-questions.md), and the original build order is on [Getting started](getting-started.md#7-build-the-first-playable-in-this-order).

## You: art

- [ ] **Build the M16 / M4 model** with the [M16 / M4 model guide](m16-m4-model.md), starting with its setup prompt.
- [ ] **Then the other three pilot guns:** the [M1911](../weapons/pistols/m1911.md), [Minimi / M249](../weapons/lmgs/minimi.md), and [M1 Garand](../weapons/battle-rifles/m1-garand.md) ([Pilot](art-and-sound.md#pilot-four-guns-first)).
- [ ] **Pick gunshot and gun sounds by ear** as each pilot gun goes in ([Sound](art-and-sound.md#sound)).

## You: hand to Claude Code

- [ ] **Catch the game up with the wiki.** As of 2026-11-21 the game's data still has four armor tiers and the MG 42 as an LMG. Paste this:

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

- [ ] **Set up the AI team,** once you've settled how it should work ([AI team idea](idea-inbox.md#ai-team-of-workers)).

## You: decisions

In rough order of what the game needs first:

- [ ] **Handling numbers:** hip fire, ADS speed, movement, and swap speed per category, including LMGs. The direction is set on [Roles by category](../systems/ttk.md#roles-by-category); the numbers matter as soon as real models are in.
- [ ] **Attachment effects:** how much each muzzle, grip, and stock changes recoil, sway, and aim speed ([Attachments](../systems/attachments.md#attachment-slots)).
- [ ] **Neck and groin:** whether they're hit zones of their own.
- [ ] **Shields:** what you can hold with one, how much damage a normal shield takes, and whether the flash shield uses the class slot ([Class items](../systems/class-items.md)).
- [ ] **Carry space:** how Tarkov's slot counts turn into the game's carry space ([Armor](../systems/armor.md#vests)).
- [ ] **Crate ammo:** how many FRAG-12, dragon's breath, and lethal launcher rounds a crate holds, and FRAG-12's damage to vehicles.
- [ ] **The first map:** size and setting, plus the per-map caps for throwables and crate weapons ([Maps](../systems/maps.md)).
- [ ] **In-game names** for guns and armor brands: real, PUBG-style, or fictional. Talk to a lawyer before selling the game.
- [ ] **Server hosting,** once the game runs ([Servers](../systems/servers.md)).

## Claude Code: build order left

- [ ] **The zone and the plane drop.**
- [ ] **Parachuting,** with the third-person view it uses ([Gameplay](../systems/gameplay.md)).
- [ ] **A graybox map:** blocks and ramps before art.
- [ ] **A dedicated server build** from the engine source. You'll need the GitHub account linked to your Epic account first ([Getting started](getting-started.md)).
- [ ] **Playtest with friends,** then fix the worst problems before adding more.

## Claude chat: wiki work (say the word)

- [ ] **Next guns:** the Madsen ([LMG queue](queue.md#lmgs-in-progress)) and the Arisaka ([sniper queue](queue.md#snipers-in-progress)), then start the special category: bows, crossbows, and mortars.
- [ ] **Lookups:** energies for the rounds behind the 32 versions with no damage yet, each version's real bullet speed, the missing LMG fire rates, and attachment lists for the 5 gun pages without one ([Lookups](open-questions.md#lookups)).
- [ ] **Mockups:** the HUD, inventory, and menus as designs before they're built in Unreal.

## Later

- [ ] Epic Online Services (free): matchmaking, voice, and Easy Anti-Cheat.
- [ ] A Steam page ($100 through Steam Direct).
- [ ] The robot characters, once the mannequins have done their job ([Robot character concept](idea-inbox.md#robot-character-concept)).
