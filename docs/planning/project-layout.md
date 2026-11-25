# Project layout

How to organize the game's Unreal project, researched for the owner (2026-11-24). The current layout is in the game repo's `CLAUDE.md` (Content folders). This is the planner's suggestion, owner OK'd, 2026-11-24; the lead decides how and when to move things.

## What the guides say

- **Name assets by type, then name.** Epic's recommended pattern is `Prefix_AssetName_Descriptor_Variant`, such as `SM_Crate_Lid_A`. Prefixes say what an asset is: `SM_` static mesh, `SK_` skeletal mesh, `M_` material, `MI_` material instance, `T_` texture, `BP_` Blueprint, `ABP_` animation Blueprint, `AM_` montage, `AS_` animation sequence, `BS_` blend space, `DT_` data table, `WBP_` widget, `FXS_` Niagara system ([Epic: asset naming](https://dev.epicgames.com/documentation/unreal-engine/recommended-asset-naming-conventions-in-unreal-engine-projects)).
- **Give each thing its own folder, holding everything it needs.** Epic's example sorts content by kind (Vegetation, Rocks, Chr for characters, FX), and inside that each asset has its own folder: `Tree_A` holds `SM_Tree_A`, `MI_Tree_A`, and `T_Tree_A_BaseColor`, and a character's folder holds its Blueprint, meshes, skeleton, animation Blueprints, and animations ([Epic: assets folder structure](https://dev.epicgames.com/documentation/unreal-engine/assets-folder-structure-in-unreal-engine)).
- **No folders named after asset types.** Folders called `Meshes`, `Textures`, or `Materials` only repeat what the prefix and the Content Browser's filters already say, and they invite a texture landing in the wrong one ([Allar's style guide](https://github.com/Allar/ue5-style-guide) 2.6). A very large set used by many things, like animations shared by every character, gets its own folder (2.7).
- **One project folder.** All of the game's own assets under one folder named for the project, so store packs and plugins never mix with ours and moving assets between projects doesn't collide (Allar 2.2).
- **A `Core` folder** for the base game mode, character, and controller Blueprints that everything else builds on (Allar 2.5), **all levels under `Maps`** (2.4), **master materials in a material library** (2.8), and **a `Developers` folder** for experiments, hidden by default, so unfinished work isn't used by accident (2.3).
- **Folder names** in PascalCase, with no spaces or special characters (2.1), and no empty folders (2.9).

## Our layout (suggested)

The current folders already follow most of this: `Core`, `Maps`, `Characters`, `Guns` with one folder per family plus `Shared`, `UI`, `Data`, and `Input`. The suggestion is to finish the job before art production fills the project:

| Folder | Holds |
| --- | --- |
| `BRGame/` | Everything of ours, in one project folder (rename when the game has its name) |
| `BRGame/Core/` | Game modes, the base character and controller, game state |
| `BRGame/Maps/` | `Range/`, `Teplov/`, later `Training/` and each new map |
| `BRGame/Characters/Player/` | The player body, its animation Blueprints, and its control rig |
| `BRGame/Characters/Outfits/` | One folder per outfit or skin set |
| `BRGame/Guns/<Family>/` | One folder per gun family: meshes, material instances, textures, animations, and sounds that only it uses |
| `BRGame/Guns/Shared/` | What every gun shares: the master gun material, anim Blueprints, notifies, projectiles, the shared gunshot MetaSound |
| `BRGame/Attachments/<Kind>/` | Scopes, grips, muzzles, mags, and stocks, one folder per kind |
| `BRGame/Gear/` | `Armor/` (carriers, vests, rigs, plates, helmets), `Backpacks/`, `Meds/`, `Throwables/`, `Melee/`, `ClassItems/` |
| `BRGame/Vehicles/<Vehicle>/` | One folder per vehicle |
| `BRGame/Environment/` | `Buildings/<Type>/` from the building kit, `Props/`, `Foliage/`, `Rocks/`, `Water/`, `Sky/` |
| `BRGame/Match/` | The zone and the edge, strike zones, care packages and the plane, vaults |
| `BRGame/FX/` | Shared effects (impacts, smoke, explosions); one-off effects live with what uses them |
| `BRGame/Audio/` | Shared sounds only: UI, ambience, footsteps, the edge. Gun sounds live with their gun |
| `BRGame/UI/` | HUD, menus, and the map, with `Map/` for the map images |
| `BRGame/Input/` | Input actions and mapping contexts |
| `BRGame/Data/` | The generated data tables (`DT_`) and catalogs |
| `BRGame/MaterialLibrary/` | Master materials, material functions, and shared utility textures; the range's prototype materials move here |
| `Developers/` | Each person's or agent's sandbox, never referenced by the game |
| Store packs | Stay in the folders they install to, never edited. Anything we use from them gets our own material instance or Blueprint in our folders, so swapping the pack later touches one place |

## Moving folders safely

- Do it once, early, in one commit, while there are few assets.
- Move assets inside the editor so references update, then fix up redirectors. Map paths and the paths named in C++ and config don't follow redirectors (`CLAUDE.md` lists them), so change those in the same commit.
- Lock the binary files first (Git LFS), and commit before the move so it can be rolled back.
