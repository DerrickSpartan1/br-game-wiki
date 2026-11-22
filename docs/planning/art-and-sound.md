# Gun art and sound

How each gun gets a model, animations, and sounds. The bar is "good enough to get the feel down": right size, right shape, moving parts that move, and sounds that tell guns and distances apart. Polished art comes later, with real artists. Gun tuning waits for these models ([decision log](decisions.md)), and each gun can be tuned once its model is in.

## The quality bar

**In scope now:**

- Real size and shape, taken from the gun page's Real-world notes (length, barrel length).
- Moving parts that move: trigger, bolt or slide, charging handle, magazine, selector.
- The low-poly style for testing ([Art style](#art-style-low-poly-for-testing)).
- Plain materials: steel, aluminum, wood, and polymer, with simple color differences.
- Parts split the way skins will split them: main gun, suppressor, and other parts each take their own skin later ([Skins](../systems/skins.md)).
- Sounds that tell each family apart up close and tell you how far away a shot is ([Gameplay: sound is a major focus](../systems/gameplay.md#sound)).

**Not now:** detailed textures, wear, inspect animations, and skins themselves. Inspects come later, including one for every melee weapon ([Melee](../systems/gameplay.md#melee)).

**Never:** logos, maker's marks, serial numbers, or the Red Cross emblem on any model. In game, guns go by their [game names](game-names.md) ([Legal review](legal-review.md)).

**Never needed:** jam-clearing or overheating animations, since guns never jam or overheat ([Rules](../rules.md#no-jamming)).

## Art style: low poly for testing

Guns and characters are low poly while the game is tested. The final game will look closer to PUBG (owner, 2026-11-22).

**Now, for testing:** low poly, quick to make and change.

- **Chunky, flat-sided shapes** with hard edges and clear outlines.
- **The basics right, not ultra realistic:** right size, shape, and proportions, with the detail you'd notice from first person and at a few meters. Small details become a few chunky shapes or are left out.
- **Real photos set the shapes and proportions,** since there won't be low-poly examples of every gun. **The style sets how much detail goes in.**
- **Style examples:** the owner's four examples are in the game repo at `Art/Weapons/M16M4/Reference/Style/`. They're for style only: their source is unknown, so they're never copied, traced, fed to AI tools, or shipped ([Legal review](legal-review.md)).
- **Polygon budget:** the budget in the game repo's `Art/GunConventions.md` is a ceiling; low-poly guns should land well under it.
- **Outside models** (Fab or AI image-to-3D) come out more detailed than this, so they get simplified to the style.
- **Characters** are low poly too: a male and a female body and full customizing ([Your character](../systems/skins.md#your-character)).

**Final product:** closer to PUBG's realistic look, for guns and characters: more detail, real materials, and textures. Still our own models, textures, and colors, never PUBG's ([Legal review](legal-review.md#pubg-look-and-feel)).

**Swapping in later (our pick):** the test models set the real sizes, moving parts, attach points, bones, and animations, so the final models keep those and drop in over the test ones without redoing the code.

## Lighting look

No super realistic lighting or reflections for now: guns looked too shiny under Unreal's default range lighting (owner, 2026-11-22). The aim is closer to PUBG's 2017–2018 look: natural daylight, soft and fairly flat, with haze in the distance, and a world that feels built from real things but abandoned. First pass for the lead (our pick, to tune by eye):

| What | For testing | Why |
| --- | --- | --- |
| Gun materials | Coated parts (black anodized aluminum, Parkerized or blued steel, polymer): Metallic 0, Roughness 0.6 to 0.8. Bare steel that shows (bolt, barrel crown, worn edges): Metallic 1, Roughness 0.4 to 0.6 | Most of the shine comes from low roughness. Epic: Metallic is 0 or 1, and Roughness, not Specular, is what makes a surface matte |
| Reflections | Lumen, the project default, with the rougher materials. If guns still look glassy, try Reflection Method: Screen Space | Fewer sharp reflections |
| Global illumination | Lumen, the default, for now | Its cost with 100 players gets checked later |
| Exposure | A narrow auto exposure range (Min and Max EV100 about 1 stop apart) with slow adaptation. At the range, lock it (Min equal to Max) | Walking in and out of buildings shouldn't swing the brightness far, and a locked exposure keeps material checks fair |
| Sun and shadows | One sun, soft shadow edges, and enough sky light that shadows are never black | Players in shade stay visible |
| Haze | Light exponential height fog, so far hills fade to blue-gray | PUBG's hazy horizon. Heavy fog is a weather type ([Match flow](../systems/match-flow.md#time-of-day-and-weather)) |
| Post effects | Light bloom; no lens flares, film grain, chromatic aberration, or heavy vignette; motion blur off | A clean, readable picture |
| Color | Natural, a little muted | Grounded, like the rest |

**Final product:** realistic lighting closer to PUBG's, set with the final art pass ([Art style](#art-style-low-poly-for-testing)).

## One model per version

Every version looks like its own gun (owner, 2026-11-21), so the M4, M4A1, AR-15, and so on each get their own model instead of sharing a few looks.

- **Shared underneath:** a family's versions reuse a kit of parts where the real guns share them, like the M16 / M4's lower receiver and moving parts, with one armature and Skeleton per family.
- **Different at a glance:** each model shows what sets its version apart: barrel length, upper and sights, handguard, stock, muzzle device, and mag. Where two real versions look alike, the model picks a real configuration that tells them apart, like the M4 with its carry handle and the M4A1 with a flat-top and quad rail ([M16 / M4 model guide](m16-m4-model.md#step-2-the-kit)).
- **One family at a time:** the roster has 120 families and 625 versions, so a family's base model comes first, and each version uses the base model or the gray block gun until its own model is in.

## Reload styles

Animations are shared by reload style, not made per gun. Each version's style is in the Reload column of its Versions table ([template](gun-page-template.md#reading-pages-as-data)), so the game picks the animation set from the weapon data. Box mags cover 359 of the 626 versions; the other 13 styles cover the rest.

A hand-IK rig moves the off hand to each gun's own grip and magazine points, so one rifle reload fits both an M16 and an AK. Reloads follow the [PUBG-style ammo rules](../systems/ammo.md#how-ammo-and-reloading-work): swap the mag, belt, or pan and it comes back full. Tubes, stripper clips, and en bloc clips are the exceptions ([Ammo](../systems/ammo.md#how-ammo-and-reloading-work)).

| Reload | What the hands do | Examples |
| --- | --- | --- |
| `box mag` | Mag out, mag in, under or ahead of the grip; an empty reload also works the bolt or charging handle | [M16 / M4](../weapons/assault-rifles/m16-m4.md), [AK-47 / AKM](../weapons/assault-rifles/ak-47-akm.md), [FN FAL](../weapons/battle-rifles/fn-fal.md), [MP5](../weapons/smgs/mp5.md) |
| `grip mag` | Mag drops from the grip; an empty reload also racks or drops the slide or bolt | [M1911](../weapons/pistols/m1911.md), [Glock 17 / 18](../weapons/pistols/glock-17-18.md), [Uzi](../weapons/smgs/uzi.md), [MAC-10 / 11](../weapons/smgs/mac-10-11.md) |
| `bullpup mag` | The mag sits behind the grip, so the off hand reaches back | [Steyr AUG](../weapons/assault-rifles/steyr-aug.md), [QBZ-95](../weapons/assault-rifles/qbz-95.md), [Tavor](../weapons/assault-rifles/tavor.md), [FAMAS](../weapons/assault-rifles/famas.md), [SA80](../weapons/assault-rifles/sa80.md) |
| `side mag` | Mag goes in from the side | [Sten](../weapons/smgs/sten.md), [Sterling](../weapons/smgs/sterling.md), [MP 18](../weapons/smgs/mp18.md), [FG 42](../weapons/battle-rifles/fg-42.md) |
| `top mag` | Mag goes in from the top | [Bren](../weapons/lmgs/bren.md), [Owen](../weapons/smgs/owen.md), [P90](../weapons/smgs/p90.md) |
| `pan` | Lift the empty pan off and set a full one on | [DP-27](../weapons/lmgs/dp-27.md) |
| `belt` | Open the feed cover, lay the belt in, close it, cock | [MG 42 / MG3](../weapons/crate/mg-42.md), [M60](../weapons/lmgs/m60.md), [PK / PKM](../weapons/lmgs/pk.md), [FN Minimi / M249](../weapons/lmgs/minimi.md), [RPD](../weapons/lmgs/rpd.md) |
| `tube` | One shell at a time, like PUBG; pressing fire stops the reload | [Remington 870](../weapons/shotguns/remington-870.md), [Ithaca 37](../weapons/shotguns/ithaca-37.md), [KSG](../weapons/shotguns/ksg.md), [Winchester 1887](../weapons/shotguns/winchester-1887.md) |
| `stripper clip` | From empty, bolt back and a full clip pushed down into the fixed mag; topping off loads one round at a time, like PUBG's Kar98k | [Kar98k / Gewehr 98](../weapons/snipers/kar98k.md), [Mosin–Nagant](../weapons/snipers/mosin-nagant.md), [SKS](../weapons/battle-rifles/sks.md), [C96](../weapons/pistols/c96.md) |
| `single rounds` | Rounds pushed one at a time into a fixed mag, with no clips; pressing fire stops the reload | [Remington 700 / M24](../weapons/snipers/remington-700.md) |
| `en bloc` | Clip pushed in from the top; it pings out when empty ([Rules](../rules.md#en-bloc-clips)) | [M1 Garand](../weapons/battle-rifles/m1-garand.md) |
| `break action` | Open, swap shells, close | [Garrucha](../weapons/pistols/garrucha.md) |
| `single shot` | Open the breech, swap the round | [FP-45 Liberator](../weapons/pistols/fp-45-liberator.md) |
| `revolver` | Open the cylinder, dump, reload | [Janz](../weapons/pistols/janz.md) |

Some versions take two, like the Minimi's belt or M16 mags, listed as `belt, box mag`; the second comes with another mag tier. Tube and stripper-clip guns need a one-round insert that can stop partway. Every gun also needs equip, holster, and fire-mode switch moves. Versions that cycle by hand (pump, lever, straight-pull, two-pull, and bolt action) add one "work the action" move after each shot.

## Steps for each gun

The [M16 / M4 model guide](m16-m4-model.md) walks through these steps in full, with prompts for Claude Code, for the first pilot gun.

1. **Brief.** The gun's wiki page is the brief: size from Real-world notes, mag type from the spec table, and which versions look different from the Versions table. Reference photos come from public-domain sources, like Wikimedia Commons and US military photos.
2. **Get a model,** cheapest first:
    - A [Fab](https://www.fab.com/) model whose license fits (see [Licenses](#licenses-and-the-asset-log)).
    - An AI image-to-3D model, then cleanup. In one April 2026 test, Rodin Gen-2 handled hard-surface detail like panel lines and bolts best but needed retopology and new textures; Meshy came second with softer detail and cleaner textures; Tripo came out too cartoony for guns. AI models come out as one fused piece, so the moving parts have to be cut out.
    - Built in Blender, with Claude writing the blockout through the Blender connector.
3. **Clean up and rig in Blender:** set real size, put the origin at the right-hand grip like the current block guns, split the moving and skinnable parts, add bones and points (muzzle, ejection port, off-hand grip, optic mount), strip any markings, assign the shared materials, and export.
4. **Hook it up in Unreal:** import, attach it to the gun's Blueprint, give it its reload style's animation set, and check it against the template rifle for size and hand placement.
5. **Sounds:** give it its caliber's shared shot sounds and its own mechanical and reload sounds (see [Sound](#sound)).
6. **Test on the range** (`Content/Range/Lvl_Range` in the game repo): hands line up, moving parts move, it sounds right at 25, 100, and 300 m.
7. **Log every outside asset** in the asset log.

Claude Code keeps the exact bone names, axes, polygon budget, and export settings in the game repo, so every gun matches. The budget starts at whatever the template rifle uses.

## Animation

Three layers, from most feel per hour of work to least:

1. **Procedural, in code.** Claude Code writes these once and every gun uses them: recoil kick (already random, per [Rules](../rules.md#random-recoil)), the bolt and trigger moving with each shot at the gun's real rate, sway, walking bob, aim-down-sights, sprint pose, and the open-bolt delay. This is most of the feel and needs no animator.
2. **Shared, by reload style.** Equip, holster, reload, empty reload, and fire-mode switch, made once per reload style. Start from the First Person template's rifle and pistol animations, already in the project. New ones get keyframed in Blender, with Claude's help through the Blender connector.
3. **Third person,** for what other players see and for parachuting: the template's full-body animations, plus walking and running from Epic's free Game Animation Sample (500+ animations, on Fab). Holstered guns need spots on the back and hip.

In first person, the gun draws with its own field of view so it doesn't poke through walls. That's Unreal's First Person Rendering, already set up in the template.

Cascadeur is an option if hand animation gets slow. Its free plan can't be used commercially and only saves its own file type; the Indie plan ($19 a month or $96 a year, for revenue or funding under $100,000 a year) exports FBX.

## Sound

Claude can't listen to audio, so you pick sounds by ear. Claude finds them, checks licenses, names, sorts, imports, and wires them up.

**Each shot is layered:**

- **Mechanical:** the gun's own action, heard close up. Each family gets its own.
- **Report:** the bang. Shared by caliber, with a small pitch change per family, so a 7.62×39mm RPD and AKM sound related but not the same.
- **Tail:** the echo, set by the surroundings: open ground, forest, town, or indoors.
- **Distant:** separate mid and far recordings that blend in by distance, rather than the close shot turned down. A shot turned down just sounds weak.
- **Crack:** supersonic bullets crack as they fly past you. Sound travels at its real speed, so far shots arrive late and the crack lands before the bang ([Gameplay](../systems/gameplay.md#sound)).
- **Suppressed:** its own report for suppressed versions and attachments.

Each layer gets several takes, and every shot picks one at random with a slight pitch change, so a long burst never repeats the same sound. Claude Code builds one shared gunshot MetaSound that does this, and every gun plugs its sounds into it.

**Other gun sounds:** mag out and in, belt and feed cover, bolt or charging handle, the selector click, dry fire, equip, and the en bloc ping, which has to carry to nearby players ([Rules](../rules.md#en-bloc-clips)). On open-bolt guns, the bolt slams forward before the shot, which sells the delay.

**Where sounds come from,** best first:

- **Sonniss GDC bundles:** free, royalty-free, commercial use allowed, no credit needed. Raw sounds can't be passed on by themselves, only inside the game. Each year's bundle is different, so check its file list for weapons and read the license file that comes with it.
- **Fab sound packs,** under the same license rules as Fab models.
- **Freesound:** CC0 sounds are free to use; CC BY sounds need a credit; skip CC BY-NC, which bans commercial use.
- **AI sound effects,** such as ElevenLabs: commercial use needs a paid plan and rules out beta features; the free plan bans commercial use and requires a credit. Worth trying for foley and UI; judge gunshots by ear.
- **Your own foley:** cloth, gear, and clicks recorded on a phone.

Audacity (free) is enough to trim, fade, and level sounds. Keep raw sound libraries outside the repo; import only the sounds the game uses, since Git LFS space is limited.

## Licenses and the asset log

- Every outside model, animation, or sound gets a row in an asset log in the game repo: what it is, where it came from, its link, its license, and whether it needs a credit.
- **Fab:** the Standard license comes in a Personal tier (under $100,000 gross revenue in the last 12 months) and a Professional tier above that. Some listings use CC BY, which needs a credit. Don't feed listings tagged NoAI into AI tools.
- **Meshy:** free-plan models are CC BY 4.0 and need a credit; paid-plan models are yours outright. Check Rodin's and Tripo's terms before paying.
- **AI inputs:** use public-domain photos, your own renders, or AI concept images, not someone else's photos or models.

## Who does what

| Step | Who | Tools |
| --- | --- | --- |
| Briefs, reference photos, license checks, and filing decisions | Claude chat | Web search, this wiki |
| Blockouts, cleanup, rigging, and export | Claude Code or the Claude desktop app | The Blender connector, from Blender Lab (Blender 5.1 or later) |
| Import, Blueprints, animation setup, procedural animation, and MetaSounds | Claude Code | Unreal MCP |
| Judging how it looks, feels, and sounds | You | Blender, the range |

The [AI team](ai-team.md) page splits Claude Code's part among worker subagents: a modeler, materials, an animator, the coder, sound, and a reviewer.

The Blender connector runs Claude's code in Blender with no safety checks, so save the file before each step, the same way the game repo commits before bulk changes through Unreal MCP. In the Claude desktop app it's under Settings, then Connectors. Claude Code needs one setup command, which it can run for you.

**Cost:** free tools first, with some room for paid tools if a step stalls. Everything above has a free route: Blender, Unreal and its template and sample content, Sonniss, Freesound, and free Fab assets. If paid help is needed: AI 3D generators ran about $20 to $150 a month in April 2026, plus Cascadeur Indie and paid Fab packs.

## Pilot: four guns first

Prove the pipeline on four guns that cover the biggest reload styles and one rule sound before doing the rest:

- [ ] [M16 / M4](../weapons/assault-rifles/m16-m4.md): box mag rifle. It already has its own Blueprint. Step-by-step: [M16 / M4 model guide](m16-m4-model.md).
- [ ] [M1911](../weapons/pistols/m1911.md): grip mag pistol.
- [ ] [FN Minimi / M249](../weapons/lmgs/minimi.md): belt with feed cover, plus its mag fallback.
- [ ] [M1 Garand](../weapons/battle-rifles/m1-garand.md): en bloc clip and its ping.

After that, go one reload style at a time, biggest groups first: box-mag rifles, grip-mag pistols and SMGs, belt-fed LMGs, bullpups, tube shotguns, then the rest.

## Setup prompt for Claude Code

Paste this into Claude Code in the game repo. It does one step at a time and commits after each:

```text
Read CLAUDE.md and the wiki page Planning > Gun art and sound
(docs/planning/art-and-sound.md in br-game-wiki). Set up what it
describes, one commit per step, explaining each step in plain words
before you do it:
1. Add an Art folder for Blender source files (Git LFS) and an asset
   log listing each outside asset, its source, link, license, and
   whether it needs a credit.
2. Write the gun model conventions into this repo: units, origin and
   axes (match BRBlockGun and the template rifle), bone and socket
   names for each reload style in the wiki's Reload column, the polygon budget
   (start from the template rifle), shared materials, and export
   settings.
3. Help me connect the Blender connector to Claude Code.
4. Build one shared gunshot MetaSound: random take, slight pitch
   change, mechanical, report, tail, and distant layers, with the
   distant layers blending in by distance.
5. Plan the four pilot guns and stop for my OK before starting.
```

## Sources

- [Epic: Physically based materials](https://dev.epicgames.com/documentation/en-us/unreal-engine/physically-based-materials-in-unreal-engine) · [Epic: Auto exposure](https://dev.epicgames.com/documentation/en-us/unreal-engine/auto-exposure-in-unreal-engine) · [Epic: Lumen global illumination and reflections](https://dev.epicgames.com/documentation/en-us/unreal-engine/lumen-global-illumination-and-reflections-in-unreal-engine)
- [Green Man Gaming: Interview with PUBG art director Tae-seok Jang](https://www.greenmangaming.com/ru/intel-feature/playerunknowns-battlegrounds/interview-pubg-art-director-tae-seok-jang/) (real-life objects with an abandoned look)
- [Anthropic: Claude for Creative Work (April 28, 2026)](https://www.anthropic.com/news/claude-for-creative-work)
- [Claude: Blender connector](https://claude.com/connectors/blender)
- [Classmethod: Using the Claude Blender connector in Claude Desktop and Claude Code](https://dev.classmethod.jp/en/articles/claude-blender-connector-desktop-and-code/)
- [StraySpark: Generative 3D tools compared, Meshy, Rodin, Tripo, and CSM (April 2026; StraySpark sells Blender and Unreal MCP tools)](https://www.strayspark.studio/blog/generative-3d-tools-comparison-meshy-rodin-tripo-csm-2026)
- [Meshy: Can I use Meshy assets commercially?](https://intercom.help/meshy/en/articles/16102098-can-i-use-meshy-assets-commercially)
- [Epic: Licenses and pricing in Fab](https://dev.epicgames.com/documentation/en-us/fab/licenses-and-pricing-in-fab)
- [Epic: First Person template](https://dev.epicgames.com/documentation/unreal-engine/first-person-template-in-unreal-engine?lang=en-US)
- [Epic: First Person Rendering](https://dev.epicgames.com/documentation/unreal-engine/first-person-rendering?lang=en-US)
- [Epic: Game Animation Sample updated for UE 5.7](https://www.unrealengine.com/tech-blog/explore-the-updates-to-the-game-animation-sample-project-in-ue-5-7)
- [Epic: MetaSounds quick start](https://dev.epicgames.com/documentation/en-us/unreal-engine/metasounds-quick-start)
- [Epic forums: Weapon sounds changing over distance](https://forums.unrealengine.com/t/best-way-to-approach-weapon-sounds-changing-over-distance/107683)
- [Cascadeur: Plans and pricing](https://cascadeur.com/plans)
- [Bedroom Producers Blog: Sonniss GDC 2026 bundle](https://bedroomproducersblog.com/2026/03/16/sonniss-gdc-2026-bundle/)
- [LicenseOrg: Sonniss license summary](https://licenseorg.com/guide/music-audio/sonniss)
- [Freesound: FAQ](https://freesound.org/help/faq)
- [ElevenLabs: Can I publish the content I generate?](https://elevenlabs.io/docs/help-center/legal/can-i-publish-the-content-i-generate-on-the-platform.md)
