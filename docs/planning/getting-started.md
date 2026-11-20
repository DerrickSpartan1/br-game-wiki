# Getting started

A checklist for going from this wiki to a first playable build. It's advice, not a decision log: anything here becomes a decision only once it's on the [decision log](decisions.md). Facts were checked in November 2026; versions and prices change, so recheck before buying anything.

Each step says which parts of Claude help with it. A table of every part is at the [bottom](#claude-parts-at-a-glance).

## What's current

- **Engine (recommended, not decided):** Unreal Engine. Original PUBG was built on Unreal Engine 4, Epic ships a multiplayer shooter sample (Lyra), Unreal supports dedicated servers, and its new Unreal MCP plugin lets Claude Code work inside the editor. The choice is on the [open questions](open-questions.md) page.
- **Version:** Unreal Engine 5.8 (June 2026) is the current release and the last planned major UE5 release. 5.9 is in preview. Unreal Engine 6 is aiming for early access at the end of 2027, with full release 12–18 months after that. Early UE6 keeps Actors and Blueprints, and conversion tools come later, so build on 5.8 now and plan a move to UE6 later.
- **Cost:** Unreal is free until a game earns $1 million gross, then the royalty is 5%. Sales on the Epic Games Store are royalty-free.
- **Servers:** dedicated servers need a source build of the engine, which is free but takes a linked GitHub account and a long compile.

## 1. Check your PC

- [ ] Windows 11 (Windows 10 22H2 is the minimum).
- [ ] 32 GB of RAM.
- [ ] A DirectX 12 graphics card with 8 GB or more of video memory. Lumen lighting's supported cards include the NVIDIA RTX 2000 series and newer.
- [ ] A quad-core 2.5 GHz CPU or better. Epic calls 12–16 cores a practical baseline for compiling the engine.
- [ ] Plenty of free SSD space, since a source build of the engine is big.

**Claude:** ask in chat for a parts check against these numbers.

## 2. Make accounts

- [ ] An Epic Games account.
- [ ] A GitHub account, linked in your Epic account under Connections, then Accounts. Accept the @EpicGames invite email within seven days. This unlocks the engine source code, which dedicated servers need.
- [ ] A Claude plan that includes Claude Code: Pro, Max, Team, or Enterprise. The free plan doesn't include it.
- [ ] Later: the Epic Developer Portal for Epic Online Services (free), and Steamworks ($100 per game, paid back once the game makes $1,000 adjusted gross revenue).

## 3. Download and install

- [ ] **Epic Games Launcher**, then **Unreal Engine 5.8** from it.
- [ ] **Visual Studio 2026**, which Epic recommends for general development, with the C++ game development workload. Rider and VS Code also work.
- [ ] **Git for Windows** with **Git LFS**. Claude Code also uses Git for Windows for its Bash tool.
- [ ] **Blender 5.2 LTS** (supported until July 2028) for models: robot characters, guns, and props.
- [ ] **The Claude desktop app**, which includes Claude Code. The terminal version installs from [Claude Code setup](https://code.claude.com/docs/en/setup); run `claude doctor` to check it.
- [ ] Later: the engine source from GitHub, built in Visual Studio, for the dedicated server.

## 4. Learn from Lyra, then start your own project

- [ ] Add the **Lyra Starter Game** from Fab to your library and create a project from it in the launcher. Epic calls it a learning resource: a multiplayer shooter sample with a weapon system, the Gameplay Ability System, and Epic Online Services support. Play it and read how its weapons and abilities work.
- [ ] Create the game's own project as a **C++ project**, not Blueprint-only. Code lives in text files that Claude Code can read, write, and review. Blueprints are binary assets, though Claude Code can still edit them through Unreal MCP (step 6).
- [ ] Add a `CLAUDE.md` to the project with the code rules, like this wiki has. Claude Code reads it every session.

**Claude:** Claude Code sets up the C++ project files, the `CLAUDE.md`, and the first classes.

## 5. Set up version control

- [ ] Make a **private** GitHub repo for the game, separate from this public wiki.
- [ ] Use Git LFS for `.uasset` and `.umap` files, with file locking. These files are binary and can't be merged, which is why Unreal's own Perforce workflow locks them while you edit. Perforce is the other option if the team grows.
- [ ] Ignore the folders Unreal rebuilds: `Binaries`, `Intermediate`, `Saved`, and `DerivedDataCache`.

**Claude:** Claude Code writes the `.gitignore` and `.gitattributes`, sets up LFS, and makes commits with clear messages.

## 6. Connect Claude Code to the editor

- [ ] In the editor, go to Edit, then Plugins, and turn on **Unreal MCP** and **All Toolsets**. Restart the editor.
- [ ] In Editor Preferences, under Agentic Workflows, then Model Context Protocol, check that the server auto-starts. Under MCP Client, pick Claude Code and click **Generate Client Config**. That writes a `.mcp.json` file into the project.
- [ ] Or install Epic's **Unreal Engine Skills** plugin for Claude Code from Claude's plugin directory. It bundles the MCP server, a startup hook that loads Unreal context, and safety rules.
- [ ] Open Claude Code from the project folder while the editor is running.
- [ ] Keep it local. The server listens only on your own machine and has no password, so never open it to the network. Commit before big changes, since the plugin is experimental.

These steps follow Epic's docs for 5.9, where the feature is newer; 5.8's experimental plugin may name things a little differently.

**Claude:** Claude Code can then place actors, edit Blueprints and materials, build UI widgets, set up Niagara effects, and run automation tests in the editor.

## 7. Build the first playable, in this order

- [ ] **Movement and camera:** first person, with third person only while parachuting ([Gameplay](../systems/gameplay.md)).
- [ ] **One gun, end to end:** pick one family, like the [M16 / M4](../weapons/assault-rifles/m16-m4.md). Build real fire modes, random recoil, reloads, and the selector key from the [Rules](../rules.md).
- [ ] **Weapon data:** turn the wiki's gun pages into an Unreal data table (CSV or JSON) of families, versions, cartridges, fire modes, and mags, so no gun is typed in by hand.
- [ ] **Inventory:** the main weapon slots plus the pistol / 3rd slot ([Rules](../rules.md#3rd-slot)).
- [ ] **Damage, armor, and TTK:** settle the numbers in a spreadsheet first ([TTK](../systems/ttk.md), [Armor](../systems/armor.md)).
- [ ] **Loot:** spawn guns, versions, and ammo from the match's rolled pool ([Weapon pool](../systems/weapon-pool.md), [Ammo](../systems/ammo.md)).
- [ ] **Multiplayer:** get replication working with a listen server first, then build a dedicated server from the engine source. Iris, Unreal's newer replication system, is production-ready in 5.8.
- [ ] **The zone and the plane drop.**
- [ ] **A graybox map:** blocks and ramps before art ([Maps](../systems/maps.md)).
- [ ] **Playtest with friends**, then fix the worst problems before adding more.

**Claude:** Claude Code writes the C++ and converts the wiki into the data table. In chat, Claude answers design questions, researches guns, and files every decision here. A Sheets artifact holds the damage and TTK tables.

## 8. Art and feel

- [ ] Start with Unreal's mannequins, then model the robot characters in Blender ([robot concept](idea-inbox.md#robot-character-concept)).
- [ ] Mock up the HUD, inventory, and menus before building them in Unreal.

**Claude:** the Design artifact type for HUD and menu mockups, the Whiteboard type for map layouts and system diagrams, and Claude Code for Blender Python scripts that batch-export models.

## 9. Online services and release prep

- [ ] **Epic Online Services:** free, including matchmaking, voice, and Easy Anti-Cheat. Extra anti-cheat support needs a paid agreement. It works for games sold on Steam too.
- [ ] **Server hosting:** pick a host for dedicated servers once the game runs ([Servers](../systems/servers.md)).
- [ ] **Steam page:** $100 per game through Steam Direct.
- [ ] **Open questions to settle before release:** in-game gun names and trademarks, and anything else on the [open questions](open-questions.md) page. Talk to a lawyer about names and art before selling the game.

**Claude:** the Docs type for a game design document or store copy, the Slides type for a pitch deck, the Data type for playtest dashboards, and the browser tools for Steamworks or Epic portal setup forms.

## Claude parts at a glance

| Part | What it's for |
| --- | --- |
| Claude chat | Design decisions, gun research, filing ideas, and keeping this wiki up to date |
| Claude Code (desktop app or terminal) | Game C++ code, build scripts, git, the weapon data table, and code reviews |
| Unreal MCP and Epic's Unreal Engine Skills plugin | Letting Claude Code work inside the Unreal editor |
| Sheets | Damage, TTK, armor, and loot-weight tables |
| Design | HUD, inventory, and menu mockups |
| Whiteboard | Map layouts, system diagrams, and brainstorms |
| Docs | A game design document and store copy |
| Slides | A pitch deck |
| Data | Playtest and match-stat dashboards |
| Browser tools | Web setup forms, like Steamworks and the Epic Developer Portal |

## Sources

- [Epic: Hardware and software specifications for Unreal Engine](https://dev.epicgames.com/documentation/unreal-engine/hardware-and-software-specifications-for-unreal-engine?lang=en-US)
- [Epic: State of Unreal 2026, top news](https://www.unrealengine.com/news/state-of-unreal-2026-top-news-from-the-show)
- [Epic: Unreal Engine 5.9 preview release notes](https://dev.epicgames.com/documentation/unreal-engine/unreal-engine-5-9-release-notes)
- [Wccftech: Epic integrates Claude and Gemini into Unreal Engine (June 2026)](https://wccftech.com/epic-games-unreal-engine-6-claude-gemini-developer-control/amp/)
- [Epic: Unreal Engine license](https://www.unrealengine.com/en-US/license)
- [Epic: Setting up dedicated servers](https://dev.epicgames.com/documentation/en-us/unreal-engine/setting-up-dedicated-servers-in-unreal-engine)
- [Epic: Unreal Engine on GitHub](https://www.unrealengine.com/en-US/ue-on-github)
- [Epic: Lyra sample game](https://dev.epicgames.com/documentation/en-us/unreal-engine/lyra-sample-game-in-unreal-engine)
- [Epic: Using Perforce as source control](https://dev.epicgames.com/documentation/en-us/unreal-engine/using-perforce-as-source-control-for-unreal-engine)
- [Epic: Unreal MCP in Unreal Editor](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-mcp-in-unreal-editor)
- [Claude plugins: Unreal Engine Skills (by Epic Games)](https://claude.com/plugins/unreal-engine-skills-for-claude-code)
- [Claude Code: Setup](https://code.claude.com/docs/en/setup)
- [Blender 5.2 LTS](https://www.blender.org/releases/5-2/)
- [Epic Online Services: Licensing](https://onlineservices.epicgames.com/licensing)
- [PC Gamer: Epic has made Easy Anti-Cheat free for game developers (2021)](https://pcgamer.com/epic-has-made-easy-anti-cheat-free-for-game-developers)
- [Steamworks: Steam Direct fee](https://partner.steamgames.com/doc/gettingstarted/appfee)
