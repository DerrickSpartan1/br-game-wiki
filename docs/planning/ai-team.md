# AI team

How the AI helpers split the work, and how to set them up. You talk to two of them: the planner and the lead. The lead hands work to the workers.

| Who | Runs | Does | You reach it |
| --- | --- | --- | --- |
| **Planner** | Claude chat on claude.ai | Design, research, and this wiki: gun pages, systems, decisions, guides, the [To-do](to-do.md) list, and the prompts the lead needs. It can read the game repo to see what's built, but never changes it | The Claude app, as a normal chat |
| **Lead** | Claude Code on your PC, in the game repo | Plans the build work from the wiki, hands each step to one worker, has the reviewer check it, commits, and asks you when something needs your eye or ear | The Claude app's Code tab, through Remote Control |
| **Workers** | Subagents inside the lead's session | One kind of job each (table below) | Through the lead. You see their progress in the lead's session |

Workers are Claude Code subagents: files in the game repo's `.claude/agents/` folder, each with its own instructions, tools, and memory. They report back to the lead, not to each other. If the team later needs workers that talk to each other or run side by side for long stretches, Claude Code's experimental agent teams are the next step ([AI team idea](idea-inbox.md#ai-team-of-workers)).

## How work flows

1. **You and the planner settle a design.** The planner writes it on the wiki and puts anything the lead should do in the To-do page's [For the lead](to-do.md#for-the-lead-claude-code) section, with a prompt where one helps.
2. **You tell the lead** from your phone: "check the planner's list," or give it a task directly.
3. **The lead reads the wiki,** splits the task into steps, and hands each step to a worker.
4. **The reviewer checks each result.** Anything judged by eye or ear comes to your phone as a question.
5. **The lead commits each step** and tells you what's done.
6. **You review it.** Built work comes to you on the lead's playtest checklist; the planner's first passes ("our pick") come on a review page. Nothing counts as done until you've reviewed it (owner, 2026-11-24).
7. **Tell the planner** what you reviewed. The planner checks the game repo's commits and your playtest results, then updates the To-do list: an item is ticked only once you've said it's good, and anything that needs work goes back to the lead or the planner with your note.

## The workers

| Worker | Job | Tools | Owns |
| --- | --- | --- | --- |
| **modeler** | Gun and prop models: blockouts, detail passes, splitting moving parts, and fixes, following the [M16 / M4 model guide](m16-m4-model.md) | Blender connector; files in its folders | `Art/Weapons/<gun>/` models, exports, and previews |
| **materials** | Materials and UVs now; textures and skins later | Blender connector; Unreal MCP for material instances | Material slots in each gun's .blend; Unreal material assets |
| **animator** | Armatures, bones, and points; test animations; reload, equip, and fire animations; hand IK in Unreal | Blender connector; Unreal MCP | The armature in each gun's .blend; `Content/Guns/<gun>/` animation assets |
| **coder** | C++, Blueprints, the wiki data tools, Unreal imports, and builds | Files, shell, Unreal MCP | `BRGame/Source`, `Tools`, `Config`, and Blueprints |
| **sound** | Finds sounds and checks their licenses, trims, imports, and wires them into the shared gunshot MetaSound; you pick by ear | Web search, files, Unreal MCP | Audio assets and the asset log |
| **reviewer** | Checks each result against the wiki, `Art/GunConventions.md`, and the reference photos, and reports problems. Never fixes anything itself, so it judges work it didn't make | Read-only files and previews | Nothing; it writes only review notes |

## Rules the lead follows

- **The wiki is the brief.** Read the wiki page for the task first. When the code and the wiki disagree, ask the owner which is right.
- **One worker at a time in Blender, and one at a time in the Unreal editor,** since each is a single program driven through its connector. Code work can run alongside art work.
- **Art results come with a picture.** Art workers save a preview render or screenshot with each result, and the reviewer checks it before the step counts as done.
- **Ask the owner** about anything judged by eye or ear, and before anything hard to undo. Questions and permission prompts go to the phone and wait for an answer.
- **Commit after each step,** and lock binary files before editing them.
- **Don't do the workers' jobs,** except trivial ones.
- **Write for a phone:** short status messages, with the one thing that needs an answer up top.
- **"Check the planner's list"** means: read the wiki's [To-do](to-do.md) page, work through its For the lead section in order, and say which items are done.
- **Built is not done.** Every finished item goes on the playtest checklist for the owner, and stays open on the To-do page until he says it's good (owner, 2026-11-24). Anything said in a playtest or a report that isn't on a list gets an item, so nothing is lost.

## Setup

### 1. Update and sign in

In a terminal on your PC, run `claude update`. Then start `claude` once and run `/login` if it isn't signed in with your claude.ai account; Remote Control needs that sign-in, not an API key.

### 2. Create the team

Paste this into Claude Code in the game repo:

```text
Read CLAUDE.md, then the wiki page Planning > AI team
(docs/planning/ai-team.md in br-game-wiki). Set up the team it
describes, one commit per step, explaining each step in plain words
first:
1. Write a .claude/agents/ file for each of the six workers in its
   table (modeler, materials, animator, coder, sound, reviewer): a
   description that says when to use it, only the tools and MCP servers
   the table gives it, model inherit, memory set to project, and
   instructions covering its job, the folders it owns, and the shared
   rules: read the wiki page for the task first, follow
   Art/GunConventions.md, save a preview with every art result, never
   edit another worker's folders, and leave commits to the lead. The
   reviewer gets read-only tools.
2. Write .claude/agents/lead.md from the page's "Rules the lead follows"
   and "How work flows," with model opus and memory set to project, and
   set "agent": "lead" in .claude/settings.json so every session in
   this repo starts as the lead.
3. Add a short "AI team" section to CLAUDE.md: who the planner, lead,
   and workers are, and the one-at-a-time rule for Blender and the
   Unreal editor.
4. Pre-approve only the routine commands the team runs (git status,
   diff, add, commit, push, and lfs lock; the Tools generators; claude
   mcp list) in .claude/settings.json, nothing broader.
Then tell me how to start the lead with Remote Control, and stop.
```

**Check:** `/agents` in Claude Code lists the six workers, and a new session in the repo introduces itself as the lead.

### 3. Reach the lead from your phone

1. **Keep the PC awake:** in Windows Settings, under System, then Power & battery, set the PC to never sleep when plugged in. Remote Control reconnects after sleep, but the lead is offline while the PC sleeps.
2. **Open what the workers need:** the Unreal editor and Blender, since their connectors run inside them. Code-only work doesn't need either.
3. **Start the lead** in the game repo folder: `claude --remote-control "BR Lead"`. It runs as a normal terminal session you can also reach from the phone.
4. **Connect it every time:** in Claude Code, run `/config` and turn on "Enable Remote Control for all sessions," so any session you start, or resume with `claude --continue`, connects on its own.
5. **Turn on phone alerts:** in `/config`, turn on "Push when actions required" (permission prompts and questions) and "Push when Claude decides" (finished tasks).
6. **On your phone:** open the Claude app, tap Code, and pick "BR Lead." A computer icon with a green dot means it's online. Messages, questions, and approvals work from there, and you can send photos.

The `claude` process has to keep running on the PC. If the PC restarts, open a terminal in the game repo and run `claude --continue` to bring the lead back with its conversation.

**Check:** from your phone, ask the lead what's on the planner's list. It should read the wiki's To-do page and answer.

### 4. A first job

Start with something small and code-only: "Check the planner's list." Its first item catches the game up with the wiki, which is coder work. Watch the lead hand it to the coder, the reviewer check it, and the lead commit it. The [M16 / M4 model guide](m16-m4-model.md) is the first real art job after that.

## Security

- **Remote Control** makes outbound HTTPS connections only and opens no ports on your PC. While it's connected, the session's transcript is stored on Anthropic's servers to keep your devices in sync; the work itself runs on your PC.
- **The Blender connector runs Claude's code in Blender with no safeguards** ([M16 / M4 model guide](m16-m4-model.md#before-you-start-one-time)). Save and commit before each art step, so any step can be undone.
- **Pre-approve narrowly.** Approve routine commands ahead of time and keep prompts on for everything else, so nothing broad runs from your phone without a tap.
- **Optional:** turn on Require trusted devices in your claude.ai account settings, so only your enrolled phone and browsers can steer Remote Control sessions.

## Sources

- [Claude Code docs: Create custom subagents](https://code.claude.com/docs/en/sub-agents)
- [Claude Code docs: Continue local sessions from any device with Remote Control](https://code.claude.com/docs/en/remote-control)
- [Claude Code docs: Orchestrate teams of Claude Code sessions](https://code.claude.com/docs/en/agent-teams)
- [Claude Code docs: Message your other Claude Code sessions](https://code.claude.com/docs/en/cross-session-messaging)
