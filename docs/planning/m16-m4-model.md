# M16 / M4 model guide

Step-by-step instructions for the first pilot gun on [Gun art and sound](art-and-sound.md): the [M16 / M4](../weapons/assault-rifles/m16-m4.md). It builds a kit of shared parts and a model for each of the 9 versions, at that page's quality bar: real size and shape, moving parts that move, plain materials, and the [low-poly style](art-and-sound.md#art-style-low-poly-for-testing) used for testing.

How the work splits: Claude Code does most of the Blender and Unreal work, through the Blender connector and Unreal MCP. You judge how it looks at each check, describe fixes in plain words, and do a few hands-on checks in Blender and on the range. Each step ends with a check; don't move on until it passes.

The plan is to take the M4A1 all the way into the game first as the base model, which proves every step of the pipeline on one gun. The other eight versions wait until then and reuse its lower receiver, moving parts, and armature.

## Before you start (one time)

1. **Blender 5.2 LTS** is installed ([Getting started](getting-started.md)). The connector needs Blender 5.1 or later.
2. **Install the Blender connector:**
    1. In the Claude desktop app, open Settings, then Connectors. Search for "blender" and install the Blender connector from the Anthropic & Partners section.
    2. Open Blender Lab's MCP server page (linked from the connector's page) and drag its install link into the Blender window twice: the first drag adds the Blender Lab repository, the second installs the add-on.
    3. In Blender, open Edit, then Preferences, then Add-ons, then MCP. Set the host to `localhost` and the port to `9876`, and turn on Auto Start. It should say "Server is running."
3. **Know the risk.** The connector runs Claude's Python code in Blender with no safeguards, so it could delete or send out data. Blender Lab recommends a virtual machine or a system without sensitive data. At the least, keep work files in the game repo's Art folder, save in Blender before each step, and commit after each step so any step can be undone. A separate Windows account for art work is a cheap middle ground.
4. **Run the setup prompt** below in Claude Code, in the game repo. It's a narrower version of the setup prompt on [Gun art and sound](art-and-sound.md#setup-prompt-for-claude-code); the shared gunshot MetaSound can wait until step 9.

```text
Read CLAUDE.md, then the wiki pages Planning > Gun art and sound and
Planning > M16 / M4 model guide (docs/planning/art-and-sound.md and
docs/planning/m16-m4-model.md in br-game-wiki). Then, one commit per
step, explaining each step in plain words first:
1. Add Art/Weapons/M16M4/ with a Reference folder, for Blender source
   files under Git LFS, and an asset log at Art/AssetLog.md: each
   outside asset, its source, link, license, and whether it needs a
   credit.
2. Inspect the template rifle (Content/Weapons/Rifle: SKM_Rifle and
   SK_Rifle) and BRBlockGun with Unreal MCP: bones, sockets, scale,
   axes (BRBlockGun says forward +Y, up +Z, origin at the right-hand
   grip, in cm), triangle count, and material slots. Write
   Art/GunConventions.md from it: units, axes, origin, the bone and
   socket names from the guide's step 5, the polygon budget (start from
   the template rifle's), material slots, and Blender FBX export
   settings that import at the right size and facing.
3. Register the Blender connector for Claude Code. It was installed
   through the Claude desktop app, and "claude mcp add-from-claude-desktop"
   doesn't pick up connector installs, so add the blender-mcp program the
   desktop app unpacked as a project-scope stdio server. Confirm it shows
   as connected in "claude mcp list".
Stop after step 3 and tell me what you found.
```

**Check:** Claude Code reports the template rifle's size, bones, and triangle count, and `claude mcp list` shows `blender` as connected. Restart Claude Code if it asks.

### Blender basics you'll need

You won't model by hand, but you'll look, measure, and test. These cover it:

| To | Do this |
| --- | --- |
| Orbit, pan, zoom | Drag with the middle mouse button; Shift + middle mouse; scroll wheel |
| Look from the front, side, or top | Numpad 1, 3, or 7; add Ctrl for the opposite side |
| Flat view for comparing to a photo | Numpad 5 switches between perspective and orthographic |
| Zoom to what's selected | Numpad . (period) |
| Show one part alone | Select it, then Numpad / (press again to come back) |
| Hide and unhide | H hides what's selected; Alt + H shows everything |
| Measure a part | Press N for the side panel; the Item tab shows Dimensions |
| Test a moving part | Select the armature, press Ctrl + Tab for Pose mode, click a bone, press G to move or R to rotate it, then right-click to cancel |
| Undo, save | Ctrl + Z, Ctrl + S |

## Step 1: Reference

Download these into `Art/Weapons/M16M4/Reference`. All are US government works, so they're public domain. Log each one in the asset log anyway, so you know where it came from.

- **M4A1 side view:** [M4 PEO Soldier.jpg](https://commons.wikimedia.org/wiki/File:M4_PEO_Soldier.jpg) on Wikimedia Commons, a clean side shot of a flat-top M4A1. Add a top view and a front view if you find public-domain ones (US military photo sites mark theirs).
- **Drawings of the parts:** an [Army M16A2 and M4 manual](https://archive.org/download/a2-m4-m4a1-technical/Army%20M16A2%20and%20M4%20manual.pdf) on the Internet Archive, and the [M231's maintenance manual](https://commons.wikimedia.org/wiki/File:TM-9-1005-309-23-and-P.pdf) on Commons for the funny version.
- **The other versions, for later:** side views of an M16A1, an M16A2, an M4 with its carry handle, a civilian AR-15, a Colt Commando (XM177 or Model 733), and a Colt M5 in .300 Blackout from Commons, plus a curved 7.62×39mm AR magazine.
- **Style:** the owner's style examples in `Reference/Style/`, for how much detail goes in, never copied ([Art style](art-and-sound.md#art-style-low-poly-for-testing)).

Sizes to build to (from Wikipedia):

| Version | Overall length | Barrel |
| --- | --- | --- |
| M4 and M4A1 | 838 mm with the stock out, 756 mm with it in | 14.5 in (368 mm) |
| AR-15 | Follows from its barrel and stock | Usually 16 in (406 mm) |
| M16A1 and M16A2 | 1,007 mm (A2) | 20 in (508 mm) |
| Commando | Follows from its barrel and stock | 11.5 in (292 mm), from the XM177E2 |
| M231 | From the M231 manual | From the M231 manual |

**Check:** the folder holds at least the M4A1 side view and the manual, and the asset log lists them.

## Step 2: The kit

Every version gets its own model ([One model per version](art-and-sound.md#one-model-per-version)), built on a shared kit.

**The shared kit:** the lower receiver with its pistol grip and trigger guard, the buffer tube, the moving parts (trigger, selector, bolt carrier, charging handle, bolt catch, and dust cover), and one armature for the family.

**What tells each version apart at a glance:**

| Version | Upper and sights | Barrel | Handguard | Stock | Mag and muzzle |
| --- | --- | --- | --- | --- | --- |
| M4A1 (base model, built first) | Flat-top rail with a folding rear sight | 14.5 in | Aluminum quad rail | Collapsible | 30-round STANAG; birdcage |
| M4 | Detachable carry handle, as first issued | 14.5 in | Round two-piece carbine handguard | Collapsible | 30-round STANAG; birdcage |
| AR-15 | Flat-top | 16 in | Slim free-float handguard | Collapsible | 30-round STANAG |
| 7.62x39 AR | Flat-top | Like the AR-15 | Like the AR-15 | Collapsible | Curved 7.62×39mm mag |
| .300 Blackout | Flat-top | Its own, from a Colt M5 reference | Its own, from the reference | Collapsible | 30-round STANAG; its own muzzle device |
| M16A2 | Carry handle with the A2 rear sight, brass deflector | 20 in | Round, ribbed rifle length | A2 fixed | 30-round STANAG; birdcage |
| M16A1 | Carry handle with the simpler A1 rear sight, no brass deflector | 20 in | Triangular rifle length | Shorter A1 fixed | 30-round STANAG |
| Commando | Carry handle | 11.5 in | Short round | Collapsible | 30-round STANAG; plain birdcage |
| M231 FPW (funny version) | Carry handle with no rear sight | Its own, from the manual | Its own | None | 30-round STANAG |

**Calls already made here,** which you can change:

- **The M4A1 is the base model** and goes all the way into the game first. The other versions keep the gray block model until theirs are in.
- **The M4A1 gets an aluminum quad rail,** like the real KAC rail, so foregrips and underbarrel launchers have somewhere to mount ([Attachments](../systems/attachments.md#grenade-launchers)).
- **The M4 and M4A1 look alike in real life,** so the M4 gets the carry handle and round handguard it was first issued with.
- **The Commando is a Colt 733:** carry-handle upper, 11.5 in barrel, short round handguard, collapsible stock, and a plain birdcage.
- **Mags are separate meshes,** so the hand can carry one during a reload and the bigger mag tiers (40, 60, and the 100-round C-Mag) can swap in later.

## Step 3: Blockout of the M4A1

Paste this into Claude Code:

```text
Using the Blender connector, start Art/Weapons/M16M4/M16M4.blend and
save it before changing anything. Follow Art/GunConventions.md. Build a
blockout of the M4A1 from step 2 of the M16 / M4 model guide, at
real size: 838 mm long with the stock extended and a 14.5 in (368 mm)
barrel, matched to the side view in Art/Weapons/M16M4/Reference. Put
every part in an "M4A1" collection as its own named object: lower
receiver with pistol grip and trigger guard, flat-top upper with rail
and folding rear sight, quad-rail handguard, barrel with front sight
base, birdcage flash hider, buffer tube, collapsible stock, 30-round
magazine, and the moving parts on their own: trigger, selector, bolt
carrier, charging handle, bolt catch, and dust cover. Simple shapes
only for now, in the low-poly style. Add the side view as a reference image behind the model,
scaled so the gun in the photo is 838 mm long. Save, then tell me the
overall length, height, and width you measured, and commit.
```

**Check, in Blender:**

1. Press Numpad 3 (or 1) for the side view and Numpad 5 for orthographic. The model's outline should sit on the photo: grip angle, stock, magazine, front sight, and muzzle all in the right places.
2. Select everything (A) and check Dimensions in the side panel (N): about 83.8 cm long.
3. The origin (the small orange dot) sits at the pistol grip, where the right hand holds it.

Send fixes in plain words, like "the magazine hangs too far forward" or "the stock is about 2 cm too long." Expect two or three rounds.

## Step 4: Detail pass

Paste this, then go through as many fix rounds as it takes:

```text
Detail pass on the M4A1 in M16M4.blend (save first), in the low-poly
style from Planning > Gun art and sound: chunky, flat-sided shapes with
hard edges and clear outlines. Shapes and proportions come from the
reference photos; how much detail goes in comes from the style examples
in Art/Weapons/M16M4/Reference/Style (style only; never copy them).
Model what you'd notice from first person and at a few meters:
ejection port with brass deflector, forward assist, mag well and mag
release, bolt catch, selector lever, trigger and trigger guard, pistol
grip, charging handle, front sight post, the folding rear sight, the
birdcage, the stock, and the quad rail as a few chunky ridges rather
than every slot. Land well under the polygon budget in
Art/GunConventions.md. No logos, maker's marks, serial numbers, or
lettering of any kind. Save, tell me the triangle count, and commit.
```

**Check:**

- **From the side and at an angle,** it reads as an M4A1 at a glance, in the same style as the examples.
- **From the shooter's view:** put the view behind the rear sight. The rear sight's aperture and the front post line up along the barrel, since that's what you'll aim through.
- **The triangle count** is well under the budget.

## Step 5: Moving parts and rig

```text
Rig the M4A1 in M16M4.blend (save first), following Art/GunConventions.md.
One armature for the whole family, with a root bone at the grip and
one bone per moving part, each part fully bound to its own bone:
- trigger: rotates back around its pin
- selector: rotates around its pin; safe points forward, semi points
  up (90 degrees), auto or burst points back (180 degrees)
- bolt carrier: slides straight back and forward
- charging handle: slides back with the carrier when pulled, then
  returns on its own
- bolt catch: tips up when the gun runs empty
- dust cover: swings open on its hinge (it pops open on the first
  shot and stays open, like the real one)
- magazine: slides straight down out of the mag well
Add the points the game needs as empties with the conventions' names:
muzzle, ejection port, rear sight (for aiming through the irons),
optic rail, underbarrel rail, off-hand grip on the handguard, and the
magazine's seat. Make a short test animation that moves each bone
through its full range one after another. Save and commit.
```

**Check:** play the test animation (Spacebar in Blender). Every part moves the right way and no further than the real one: the bolt carrier doesn't leave the receiver, the mag clears the well cleanly, and nothing else moves with them. Then try a few bones by hand in Pose mode.

## Step 6: Materials and UVs

```text
In M16M4.blend (save first): assign the shared materials from
Art/GunConventions.md: black anodized aluminum for the receivers, the
quad rail, the buffer tube, the charging handle, and the magazine; dark
parkerized steel for the barrel, front sight, and small parts; black
polymer for the grip, the stock, and plastic handguards on the
versions that have them. Split
the material slots the way skins will split them: the main gun and the
magazine. Unwrap UVs with a simple automatic projection so skins can
be painted later. Save and commit.
```

**Check:** in Material Preview (press Z, then Material Preview), steel, aluminum, and polymer look different from each other, and there's no lettering anywhere.

## Step 7: Export and import the M4A1

```text
Export the M4A1 from M16M4.blend as a skeletal mesh and the 30-round
magazine as a static mesh, with the export settings in
Art/GunConventions.md. Commit the .blend and exports (lock the .blend
with git lfs lock first). Then commit the Unreal project and, with
Unreal MCP, import them under Content/Guns/M16M4: one Skeleton for the
whole family (every version reuses it), the M4A1 as its own skeletal
mesh, and the mag as a static mesh. Assign the shared materials, add
the sockets on the conventions' bones and points, and point the M4A1
version in BP_Gun_M16M4 at it instead of the gray block model; the
other versions keep the block model until their own models are in.
Stop and show me before wiring animation.
```

**Check, in Unreal:**

1. Open the skeletal mesh. It's the right size next to the template rifle (SKM_Rifle), it faces forward, and the sockets sit where they should.
2. On the range (`Content/Range/Lvl_Range`), spawn the M4A1 with the range console commands (`SpawnTest`, `RollGun`). Your right hand holds the grip, and the gun isn't sideways, backward, or a hundred times too big or small.

## Step 8: Hook up the M4A1

```text
Hook up the M4A1 in BP_Gun_M16M4, one commit per item:
1. The box mag animation set from the template's rifle animations
   (MM_Rifle_Equip, MM_Rifle_Reload, MM_Rifle_DryFire), with the off
   hand reaching the handguard and magazine points by IK.
2. In code: the bolt carrier and trigger move with each shot at the
   version's real fire rate, the dust cover pops open on the first
   shot, the bolt catch tips up and the bolt stays back when empty, and
   the selector turns when the fire mode changes.
3. Reloads: the magazine leaves with the hand and a full one comes
   back. An empty reload ends with the bolt slamming forward off the
   bolt catch.
4. Muzzle flash at the muzzle point, shells out of the ejection port,
   and aiming down sights lines the camera up behind the rear sight.
Tell me what to look at after each one.
```

**Check on the range:** fire, reload with rounds left, reload from empty, switch fire modes, and aim down the sights. The hands sit on the gun, parts move at the right moments, the flash comes from the muzzle, shells leave the port, and the irons line up when you aim. Switch the M4A1 between semi and auto to see the selector settle in each place. Safe is only for a stowed gun, and that switch isn't animated yet ([Gameplay](../systems/gameplay.md#hud-and-inventory)).

**At this point the pipeline works end to end.** Tick nothing yet: the other versions come next, and sounds come in step 10.

## Step 9: The other eight versions

```text
In M16M4.blend (save first), build a model for each of the other
eight versions in the table in step 2 of the M16 / M4 model guide,
reusing the M4A1's lower receiver, moving parts, and armature: M4,
AR-15, 7.62x39 AR (with the curved 7.62x39mm magazine), .300 Blackout,
M16A2 (1,007 mm long), M16A1, Commando, and the M231 (from the M231
manual in Reference). Each version gets its own collection. Same style,
materials, and points as the M4A1; the muzzle, sight, and off-hand
points move to suit each one. One version per commit.
```

**Check:** each version against its reference photo and length, the same way as steps 3 and 4, and side by side, every version is easy to tell apart at a glance. The moving parts work on every one (play the test animation with each).

## Step 10: Variants into the game, plus sounds

```text
Export and import each of the other eight versions the same way as the
M4A1: its own skeletal mesh on the family's shared Skeleton, and the
curved mag as its own static mesh. Point each version in BP_Gun_M16M4
at its own model and give the 7.62x39 AR the curved mag. Then build the shared gunshot
MetaSound from Planning > Gun art and sound (setup step 4) if it isn't
built yet, and give the family its sounds: the 5.56mm report shared by
caliber, plus the family's own mechanical, mag, charging handle,
selector, and dry-fire sounds. Log every outside sound in the asset
log. One commit per item.
```

You pick the sounds by ear; Claude finds candidates, checks licenses, and wires them up ([Sound](art-and-sound.md#sound)).

**Check on the range:** roll each of the 9 versions (`RollGun`). Each shows its own model, the M231 has no stock, the 7.62x39 AR has the curved mag, and the hands sit right on every version, especially the long M16 and the stockless M231. Then listen at 25, 100, and 300 m.

## Step 11: Wrap up

- Tick the M16 / M4 box in the [pilot list](art-and-sound.md#pilot-four-guns-first).
- Make sure the asset log is complete.
- Note anything slow or confusing, so this guide gets better before the [M1911](../weapons/pistols/m1911.md), [Minimi](../weapons/lmgs/minimi.md), and [M1 Garand](../weapons/battle-rifles/m1-garand.md).

## If a step stalls

- **The blockout still looks wrong after a few rounds:** start from an outside model instead, simplified to the low-poly style, then pick this guide up at step 5. Try a [Fab](https://www.fab.com/) model whose license fits first, then an AI image-to-3D model ([Steps for each gun](art-and-sound.md#steps-for-each-gun)). Either way, check the license and log it.
- **The connector misbehaves:** stop, reopen the saved .blend, and tell Claude Code what happened instead of retrying in a loop, the same rule as Unreal MCP.
- **Hands don't line up in Unreal:** usually the origin or the off-hand point is off. Fix it in Blender and re-export rather than nudging it in Unreal, so the source stays right.

## Sources

- [Wikipedia: M4 carbine](https://en.wikipedia.org/wiki/M4_carbine) (lengths, barrel, flat-top and carry handle)
- [Wikipedia: M16 rifle](https://en.wikipedia.org/wiki/M16_rifle) (M16 lengths, A1 and A2 differences, XM177 barrels)
- [Wikimedia Commons: M4 PEO Soldier.jpg](https://commons.wikimedia.org/wiki/File:M4_PEO_Soldier.jpg) (public domain, PEO Soldier)
- [Internet Archive: Army M16A2 and M4 manual](https://archive.org/download/a2-m4-m4a1-technical/Army%20M16A2%20and%20M4%20manual.pdf)
- [Wikimedia Commons: TM 9-1005-309-23&P, M231 maintenance manual](https://commons.wikimedia.org/wiki/File:TM-9-1005-309-23-and-P.pdf) (public domain)
- [Claude: Blender connector](https://claude.com/connectors/blender)
- [Blender Lab: MCP server](https://www.blender.org/?p=96198) (Blender 5.1 or later; the safety warning)
- [Classmethod: Using the Claude Blender connector in Claude Desktop and Claude Code](https://dev.classmethod.jp/en/articles/claude-blender-connector-desktop-and-code/) (desktop setup, port 9876, registering it in Claude Code)
