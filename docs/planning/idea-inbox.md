# Idea inbox

Ideas that don't fit a section yet land here until they're sorted.

| Date | Idea | Move to |
| --- | --- | --- |
| 2026-11-22 | Some sort of PvE in the game, maybe with the robots as enemies. See [Robot character concept](#robot-character-concept) | TBD |
| 2026-11-21 | Run the game's AI helpers as a team of workers: a 3D modeler, a texture artist, an animator, and a coder, with a group leader the owner talks to, who plans the work and hands it out. See [AI team of workers](#ai-team-of-workers) below | Decided: [AI team](ai-team.md) (2026-11-21) |
| 2026-10-07 | Make a wiki for all of this at some point, probably on GitHub | Done: this wiki (2026-10-14) |
| 2026-11-20 | Armor goes up to level 4, with more vest and helmet types beyond the level number, such as heavier pieces, modeled on Escape from Tarkov's armor and helmets, which have already done the real-world research. Keep it balanced and realistic. Needs research into which real pieces to use and how levels map to PUBG-style damage reduction. | Done: [Armor and gear](../systems/armor.md) (2026-11-20) |
| 2026-10-20 | Concept thought: player characters could be robots instead of humans, in the style of small, highly articulated military mecha model kits. The owner thinks the look is great. See [Robot character concept](#robot-character-concept) below. | Set aside for player characters (2026-11-22); maybe PvE enemies later ([Robot character concept](#robot-character-concept)) |

## AI team of workers

Decided on 2026-11-21: see [AI team](ai-team.md) for the setup. The notes below are how the idea started. The owner talks to one lead, who plans the work and hands it to specialists. The coder already works in Claude Code in the game repo.

Claude Code supports this two ways:

- **Subagents (the simpler start):** each worker is a file in the game repo's `.claude/agents/` folder with its own instructions, tools, and model, and the lead is the main session run as an agent (`claude --agent lead`, or `"agent": "lead"` in `.claude/settings.json`). The lead hands out work and gets results back. Subagents can keep their own project memory, so each worker remembers its lessons.
- **Agent teams (experimental):** the lead and each worker are full Claude Code sessions with a shared task list, and they message each other. You can talk to any worker directly. They use more tokens, can't be resumed, and on Windows run inside one terminal window.

Workers to start with: a lead (plans from the wiki, splits work, asks the owner to judge looks and sounds), a modeler (Blender), a materials and texture worker, a rigger and animator, the coder (C++ and Unreal), a sound worker, and a reviewer who checks each result against the wiki and the gun conventions without having made it.

Things that shape it:

- **One Blender and one Unreal editor** are shared, so only one worker can drive each at a time. The lead runs art jobs one after another while the coder works on code.
- **Workers need eyes:** art workers render a preview image and look at it before reporting, and the reviewer compares it to the reference photos.
- **Files are the contract:** the wiki, the gun conventions file, each gun's brief, and the asset log. Each worker owns its own folders, so two never edit the same file.

## Robot character concept

Not for player characters (owner, 2026-11-22): this game has PUBG-like human characters you dress up, since that makes the most sense ([Your character](../systems/skins.md#your-character)). The robots are saved for something else, maybe enemies in some sort of PvE in the game. Inspiration only, not decided. The owner's reference is SHEIK MAINLAND's FENRIR A6 Assault Type, a 1/18-scale mecha model kit (11.2 cm tall), seen in shop videos and photos from ToyForge. Search "Sheik Mainland Fenrir A6" to find the photos again; they aren't stored here, since they're someone else's product images and this wiki is public. Some of the shop posts are tagged as containing AI-generated media, so the real kit may differ. Any robot in the game needs its own original design, not a copy of this kit.

What stands out in the references:

- **Soldier, not superhero:** they read as infantry. Boxy chest armor built like a plate carrier, with rows of vertical magazine pouches, thigh panels, and pouches on the hips.
- **Head and sensors:** a small box head with red sensor dots, a sight or periscope block, and tall whip antennas like a radioman's.
- **Shoulders and back:** big slab shoulder armor, plus a backpack frame that carries a spare rifle or launcher.
- **Legs and stance:** thin, mechanical legs with exposed joints and wide flat feet, posed in a low, planted stance.
- **Colorways:** black with tan, black with blue, black with olive green, and all black; the same frame looks very different in each.
- **Guns:** they carry normal-sized rifles in human-style poses: a suppressed marksman rifle, an AR-style carbine, and a launcher. That fits a real-gun roster with no changes.

**As PvE enemies (idea):** robot soldiers that fight players in a PvE mode, or that guard spots on the map. What kind of PvE, and how robots fight, is TBD.

How it could have fit as player characters (set aside):

- **Wardrobe:** the human wardrobe slots (hats, shirts, pants, shoes) could become robot slots, like colorway, shoulder plates, chest rig, head unit, antennas, and backpack frame.
- **Gear:** armor, helmets, and backpacks could still drop as loot and mount onto the frame, the same way they do now.

