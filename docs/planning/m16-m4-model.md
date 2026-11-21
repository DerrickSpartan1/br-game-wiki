# M16 / M4 model guide

Step-by-step instructions for the first pilot gun on [Gun art and sound](art-and-sound.md): the [M16 / M4](../weapons/assault-rifles/m16-m4.md). It builds one kit of parts that covers all 9 versions, at that page's quality bar: real size and shape, moving parts that move, and plain materials.

How the work splits: Claude Code does most of the Blender and Unreal work, through the Blender connector and Unreal MCP. You judge how it looks at each check, describe fixes in plain words, and do a few hands-on checks in Blender and on the range. Each step ends with a check; don't move on until it passes.

The plan is to take the M4 all the way into the game first, which proves every step of the pipeline on one gun. The variants come after, reusing the M4's lower receiver and moving parts.

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
- **Variants, for later:** side views of an M16A2 and a Colt Commando (XM177 or Model 733) from Commons, and a curved 7.62×39mm AR magazine.

Sizes to build to (from Wikipedia):

| Version look | Overall length | Barrel |
| --- | --- | --- |
| M4 | 838 mm with the stock out, 756 mm with it in | 14.5 in (368 mm) |
| M16 (A2 look) | 1,007 mm | 20 in (508 mm) |
| Commando | Follows from its barrel and stock | 11.5 in (292 mm), from the XM177E2 |
| M231 | From the M231 manual | From the M231 manual |

**Check:** the folder holds at least the M4A1 side view and the manual, and the asset log lists them.

## Step 2: The kit

One lower receiver and one set of moving parts serve every version. A version gets its own parts only where you'd spot the difference at a glance ([One model per family](art-and-sound.md#one-model-per-family)), so the 9 versions come down to 4 looks:

| Look | Versions | Upper | Barrel | Handguard | Stock | Mag |
| --- | --- | --- | --- | --- | --- | --- |
| M4 | M4, M4A1, AR-15, .300 Blackout, 7.62x39 AR | Flat-top rail with a folding rear sight | 14.5 in | Quad rail | Collapsible | 30-round STANAG (the 7.62x39 AR takes a curved 7.62×39mm mag) |
| M16 | M16A1, M16A2 | Carry handle with the A2 rear sight | 20 in | Round, ribbed rifle length | A2 fixed | 30-round STANAG |
| Commando | Commando | Carry handle | 11.5 in | Short round | Collapsible | 30-round STANAG |
| M231 | M231 FPW (funny version) | Carry handle with no rear sight | Its own, from the manual | Its own | None | 30-round STANAG |

**Shared by every look:** the lower receiver with its pistol grip and trigger guard, the buffer tube, the birdcage flash hider (except where the M231 manual shows otherwise), and the moving parts: trigger, selector, bolt carrier, charging handle, bolt catch, and dust cover.

**Calls already made here,** which you can change:

- **The M4 gets a quad rail,** so foregrips and underbarrel launchers have somewhere to mount ([Attachments](../systems/attachments.md#grenade-launchers)). PUBG's M416 has one too.
- **The M16A1 and M16A2 share the A2 look,** as [Gun art and sound](art-and-sound.md#one-model-per-family) already decided.
- **The AR-15 shares the M4 look:** 16 in against 14.5 in isn't visible at a glance.
- **The Commando is a Colt 733:** carry-handle upper, 11.5 in barrel, short round handguard, collapsible stock, and a plain birdcage.
- **Mags are separate meshes,** so the hand can carry one during a reload and the bigger mag tiers (40, 60, and the 100-round C-Mag) can swap in later.

## Step 3: Blockout of the M4

Paste this into Claude Code:

```text
Using the Blender connector, start Art/Weapons/M16M4/M16M4.blend and
save it before changing anything. Follow Art/GunConventions.md. Build a
blockout of the M4A1 look from step 2 of the M16 / M4 model guide, at
real size: 838 mm long with the stock extended and a 14.5 in (368 mm)
barrel, matched to the side view in Art/Weapons/M16M4/Reference. Put
every part in an "M4" collection as its own named object: lower
receiver with pistol grip and trigger guard, flat-top upper with rail
and folding rear sight, quad-rail handguard, barrel with front sight
base, birdcage flash hider, buffer tube, collapsible stock, 30-round
magazine, and the moving parts on their own: trigger, selector, bolt
carrier, charging handle, bolt catch, and dust cover. Simple shapes
only for now. Add the side view as a reference image behind the model,
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
Detail pass on the M4 in M16M4.blend (save first). Keep the polygon
budget in Art/GunConventions.md. Add the details you'd notice from
first person and at 2 m: ejection port with brass deflector, forward
assist, mag well and mag release, bolt catch paddle, selector lever,
trigger, trigger guard, pistol grip, charging handle latch, rail slots
on the upper and handguard, front sight post and its ears, the folding
rear sight's aperture, the birdcage's slots, the stock's adjustment
notches, and the magazine's ribs. Small bevels on hard edges and
weighted normals so it shades cleanly without textures. No logos,
maker's marks, serial numbers, or lettering of any kind. Save, tell me
the triangle count, and commit.
```

**Check:**

- **From the side and at an angle,** it reads as an M4 at a glance.
- **From the shooter's view:** put the view behind the rear sight. The rear sight's aperture and the front post line up along the barrel, since that's what you'll aim through.
- **The triangle count** is inside the budget.

## Step 5: Moving parts and rig

```text
Rig the M4 in M16M4.blend (save first), following Art/GunConventions.md.
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
Art/GunConventions.md: black anodized aluminum for the receivers, rails,
and magazine; dark parkerized steel for the barrel, front sight, and
small parts; black polymer for the grip, stock, and handguard. Split
the material slots the way skins will split them: the main gun and the
magazine. Unwrap UVs with a simple automatic projection so skins can
be painted later. Save and commit.
```

**Check:** in Material Preview (press Z, then Material Preview), steel, aluminum, and polymer look different from each other, and there's no lettering anywhere.

## Step 7: Export and import the M4

```text
Export the M4 look from M16M4.blend as a skeletal mesh and the 30-round
magazine as a static mesh, with the export settings in
Art/GunConventions.md. Commit the .blend and exports (lock the .blend
with git lfs lock first). Then commit the Unreal project and, with
Unreal MCP, import them under Content/Guns/M16M4: one Skeleton for the
whole family (later looks reuse it), the M4 look as its own skeletal
mesh, and the mag as a static mesh. Assign the shared materials, add
the sockets on the conventions' bones and points, and point the M4,
M4A1, AR-15, .300 Blackout, and 7.62x39 AR versions in BP_Gun_M16M4 at
the M4 look instead of the gray block model. Stop and show me before
wiring animation.
```

**Check, in Unreal:**

1. Open the skeletal mesh. It's the right size next to the template rifle (SKM_Rifle), it faces forward, and the sockets sit where they should.
2. On the range (`Content/Range/Lvl_Range`), spawn the M4 with the range console commands (`SpawnTest`, `RollGun`). Your right hand holds the grip, and the gun isn't sideways, backward, or a hundred times too big or small.

## Step 8: Hook up the M4

```text
Hook up the M4 look in BP_Gun_M16M4, one commit per item:
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

**Check on the range:** fire, reload with rounds left, reload from empty, switch fire modes, and aim down the sights. The hands sit on the gun, parts move at the right moments, the flash comes from the muzzle, shells leave the port, and the irons line up when you aim. Fire the M4 (burst) and the M4A1 (auto) to see the selector settle in different places.

**At this point the pipeline works end to end.** Tick nothing yet: the variants come next, and the M4's sounds come in step 10.

## Step 9: Variant parts

```text
In M16M4.blend (save first), build the other looks from step 2 of the
M16 / M4 model guide, reusing the M4's lower receiver, moving parts,
and armature: the M16 look (carry-handle upper with A2 rear sight, 20 in
barrel, round ribbed rifle handguard, A2 fixed stock; 1,007 mm long),
the Commando look (carry-handle upper, 11.5 in barrel, short round
handguard, collapsible stock), the M231 look (no stock, no rear sight,
and its own barrel and handguard, from the M231 manual in Reference),
and the curved 7.62x39mm magazine. Each look gets its own collection.
Same detail level, materials, and points as the M4; the muzzle, sight,
and off-hand points move to suit each look. One look per commit.
```

**Check:** each look against its reference photo and length, the same way as steps 3 and 4. The moving parts work on every look (play the test animation with each).

## Step 10: Variants into the game, plus sounds

```text
Export and import the M16, Commando, and M231 looks the same way as the
M4: their own skeletal meshes on the family's shared Skeleton, and the
curved mag as its own static mesh. Point each version in BP_Gun_M16M4
at its look, using the table in step 2 of the M16 / M4 model guide, and
give the 7.62x39 AR the curved mag. Then build the shared gunshot
MetaSound from Planning > Gun art and sound (setup step 4) if it isn't
built yet, and give the family its sounds: the 5.56mm report shared by
caliber, plus the family's own mechanical, mag, charging handle,
selector, and dry-fire sounds. Log every outside sound in the asset
log. One commit per item.
```

You pick the sounds by ear; Claude finds candidates, checks licenses, and wires them up ([Sound](art-and-sound.md#sound)).

**Check on the range:** roll each of the 9 versions (`RollGun`). Each shows its look, the M231 has no stock, the 7.62x39 AR has the curved mag, and the hands sit right on every look, especially the long M16 and the stockless M231. Then listen at 25, 100, and 300 m.

## Step 11: Wrap up

- Tick the M16 / M4 box in the [pilot list](art-and-sound.md#pilot-four-guns-first).
- Make sure the asset log is complete.
- Note anything slow or confusing, so this guide gets better before the [M1911](../weapons/pistols/m1911.md), [Minimi](../weapons/lmgs/minimi.md), and [M1 Garand](../weapons/battle-rifles/m1-garand.md).

## If a step stalls

- **The blockout still looks wrong after a few rounds:** start from an outside model instead, then pick this guide up at step 5. Try a [Fab](https://www.fab.com/) model whose license fits first, then an AI image-to-3D model ([Steps for each gun](art-and-sound.md#steps-for-each-gun)). Either way, check the license and log it.
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
