# First steps in Unreal

A hands-on walkthrough for the first sessions, written for someone new to Unreal and git. Claude Code does most of the work; your job is to click through Unreal, paste the prompts, read what Claude Code wants to do, and approve it. The tools come from [Getting started](getting-started.md), and Git LFS is already installed.

## How to work with Claude Code

- **One task at a time.** Paste one prompt, let it finish, test the result, then move on.
- **Read before you approve.** Claude Code asks before it runs commands or edits files. If you don't understand a step, ask it "what does this do?" before saying yes.
- **Commit after every working step.** Say "commit this with a clear message and push it." If something breaks later, say "go back to the last commit."
- **Paste errors in full.** When Unreal or Visual Studio shows an error, copy all of it into Claude Code.
- **Ask it to teach you.** "Explain that like I'm new" works any time.
- **Design questions go to Claude chat.** Gun research and design decisions stay in chat, where they get filed on this wiki. Code goes to Claude Code.

## A. Get the repo onto your PC (about 5 minutes)

- [ ] Make a short folder for your projects, like `C:\Dev`. Keep it out of OneDrive and synced Documents folders, since Unreal has trouble with long paths and synced files.
- [ ] Open PowerShell (Start menu, type "PowerShell") and run:

    ```powershell
    cd C:\Dev
    git clone https://github.com/DerrickSpartan1/br-game.git
    ```

- [ ] The first time, a browser window asks you to sign in to GitHub. When it's done, `C:\Dev\br-game` holds four files: `README.md`, `CLAUDE.md`, `.gitignore`, and `.gitattributes`.

## B. Create the Unreal project (15–30 minutes, mostly waiting)

- [ ] Open the Epic Games Launcher, go to Unreal Engine, then Library, and launch 5.8.
- [ ] In the Project Browser, pick **Games**, then **First Person**.
- [ ] Choose **C++**, not Blueprint.
- [ ] Set **Variant** to **Arena Shooter** if it's offered. It adds weapon pickups, bullet types, an ammo display, AI opponents, and a test arena to learn from. If it isn't offered with C++, pick **None**.
- [ ] Leave **Target Platform** on Desktop and **Quality Preset** on Maximum. If you see Starter Content, leave it off to keep the repo small.
- [ ] Set **Project Location** to `C:\Dev\br-game` and the name to `BRGame`, then click **Create**.
- [ ] Wait while Unreal writes the C++ code and compiles it with Visual Studio. Visual Studio may open; you can close it. If an error pops up, copy it and give it to Claude Code in step C.
- [ ] When the editor opens, click **Play** (the green triangle) and walk around. Press Esc to stop.
- [ ] Click **File**, then **Save All**, then close the editor.

## C. Start Claude Code and make the first commit (about 10 minutes)

- [ ] Open Claude Code on the `C:\Dev\br-game` folder, either from the Claude desktop app or in PowerShell with `cd C:\Dev\br-game` and then `claude`.
- [ ] Paste:

    ```text
    I'm new to Unreal and git. Read CLAUDE.md and README.md. I just created
    an Unreal Engine 5.8 C++ First Person project in the BRGame folder. Check
    that git ignores the build folders and stores .uasset and .umap files in
    Git LFS, and tell me if anything looks wrong. Then commit the project and
    push it to GitHub. Explain what you did in plain words.
    ```

- [ ] On GitHub, open the repo. The `BRGame` folder should be there, and `.uasset` files should say "Stored with Git LFS".

## D. Connect Claude Code to the editor (about 10 minutes)

- [ ] Install Epic's **Unreal Engine Skills** plugin for Claude Code with the "Install in Claude Code" button on its [plugin page](https://claude.com/plugins/unreal-engine-skills-for-claude-code). It teaches Claude Code Unreal's conventions and adds safety rules, like saving before and after big changes.
- [ ] Open `BRGame.uproject` to start the editor.
- [ ] Go to **Edit**, then **Plugins**. Search **Unreal MCP** and make sure it's on (it's on by default). Search **All Toolsets** and turn it on. Restart the editor when asked.
- [ ] Go to **Edit**, then **Editor Preferences**, then **Agentic Workflows**, then **Model Context Protocol**. Check that **Auto Start Server** is on. Under **MCP Client**, leave **Client Selection** on Claude Code and click **Generate Client Config**. That writes a `.mcp.json` file in `C:\Dev\br-game\BRGame`.
- [ ] With the editor still open, paste into Claude Code:

    ```text
    The Unreal editor just generated BRGame/.mcp.json for Unreal MCP. Copy
    that server entry into a .mcp.json at the repo root so you can use it
    when you start from here, commit it, and tell me how to restart you so
    the connection loads.
    ```

- [ ] Restart Claude Code as it says, and approve the Unreal MCP server when it asks.
- [ ] Test it: ask "What actors are in the current level?" If it lists them, Claude Code is connected to the editor. If not, start Claude Code after the editor is open, and check the editor's **Output Log** for errors.

The editor's MCP server only listens on your own PC and has no password, so never open it to the network.

## E. Let Claude Code start building

Do these in order, and test and commit after each one.

- [ ] **Get a tour:**

    ```text
    Give me a beginner's tour of this project: what each folder and main C++
    class does, how play-testing works, and how you compile my code.
    ```

- [ ] **Weapon data from the wiki:**

    ```text
    Clone the public wiki repo DerrickSpartan1/br-game-wiki into C:\Dev\br-game-wiki.
    Write a script that reads the M16 / M4 page
    (docs/weapons/assault-rifles/m16-m4.md) and turns its versions into a CSV
    data table: family, version, cartridge, fire modes, magazine sizes, and
    open-bolt or not. Make a matching C++ row struct and import the CSV as an
    Unreal DataTable. Keep numbers marked TBD as clearly named placeholders.
    Once it works, we'll run it on every gun page.
    ```

- [ ] **The first gun:**

    ```text
    Read the wiki's Rules page (docs/rules.md). Build a C++ weapon component
    for the M16 / M4 family that uses the DataTable: real fire modes per
    version with a fire-mode selector key, magazines and reloading, and random
    recoil inside each gun's tendencies (climb, sideways drift, settle speed)
    as placeholder values I can tune. No jamming or overheating. Put it on the
    first-person character in place of the template rifle, and tell me how to
    test it.
    ```

- [ ] **Tune it:** play, then tell Claude Code what feels wrong in plain words ("it climbs too fast", "burst feels slow"). Commit when it feels right.
- [ ] **Two players:**

    ```text
    Make the gun work in multiplayer with a listen server: the server decides
    hits, damage, and ammo. Show me how to test with two players in the editor.
    ```

After that, the build order on [Getting started](getting-started.md#7-build-the-first-playable-in-this-order) takes over: inventory, damage and armor, loot, the zone, and a graybox map.

## Sources

- [Epic: Unreal MCP in Unreal Editor](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-mcp-in-unreal-editor)
- [Claude plugins: Unreal Engine Skills (by Epic Games)](https://claude.com/plugins/unreal-engine-skills-for-claude-code)
- [Epic: First Person template](https://dev.epicgames.com/documentation/en-us/unreal-engine/first-person-template-in-unreal-engine)
- [Epic: Variants in game templates](https://dev.epicgames.com/documentation/unreal-engine/variants-in-game-templates)
- [Claude Code: Setup](https://code.claude.com/docs/en/setup)
