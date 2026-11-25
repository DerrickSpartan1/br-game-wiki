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

## Check-ins

The planner and the lead check in every half hour, taking turns, so each one works from the other's latest notes (owner, 2026-11-24). A check-in only keeps them up to date with decisions, questions, and notes. It never asks you anything. Your input comes from two places only:

- **The planner's picks and review pages,** for design decisions and notes.
- **The lead's playtest checklist,** for testing and notes.

| Who | When | Where it runs | What it does |
| --- | --- | --- | --- |
| **Lead** | :00 and :30 | Inside the lead's own session, as a recurring task (`0,30 * * * *`) | Reads the planner's new answers and statuses on the To-do page, files its own questions and reports there, and puts anything built on the playtest checklist |
| **Planner** | :15 and :45 | A local scheduled task in the Claude desktop app on your PC, in its own folder (`C:\Dev\planner`) | Answers the lead's questions, updates the statuses and the review rule's ticks, and queues anything that needs you for the next picks page |
| **Planner (cloud)** | :52 every hour, 9 AM to 11 PM | A cloud scheduled task | Picks pages only (owner, 2026-11-24): files your answers, archives and deletes answered pages, and posts a new page when questions are queued. Nothing else, so it never repeats the half-hourly work |

- **Why two kinds of planner check-in:** a cloud task can run at most once an hour, and a plan allows only 5 to 25 cloud runs a day, so the half-hourly ones run on your PC, which is on for the lead anyway. Only the cloud planner can make picks pages, so it does just that, once an hour while you're awake: 15 runs a day, inside the daily cloud limit on a Max plan (Pro allows 5, Team 25). Overnight, questions wait for the morning.
- **Why the lead's check-in runs inside its own session:** a separate session would work in the same folder and the same Unreal editor at the same time as the lead. A recurring task in the lead's session fires between its turns instead, and keeps what the lead already knows. It may start up to 15 minutes late, and it stops when the session closes and after 7 days, so the lead recreates it after a restart and every Monday.
- **Questions for you wait in a queue:** the planner adds them under the To-do page's You: decisions, marked "for the next picks page"; the lead adds testing questions to its playtest checklist. Neither check-in waits for an answer.
- **Staying in step:** each check-in pulls first and pulls again (`git pull --rebase`) right before it pushes. A check-in that finds nothing new changes nothing and makes no commit.
- **Never in each other's folders:** the planner's check-in keeps its own clones of both repos in `C:\Dev\planner` and never touches the lead's folder. The game repo clone there skips the big art files (`GIT_LFS_SKIP_SMUDGE=1`), since the planner only reads code, docs, and data.

### Planner check-in steps

The planner's scheduled tasks follow these steps each time, so changing them here changes every later check-in.

1. **Get up to date.** In the check-in's own folder, pull the wiki, and fetch and fast-forward the read-only game repo clone. Read the wiki's `CLAUDE.md` and follow it exactly, including the "Before pushing" steps.
2. **See what's new** since the last commit whose message starts with "Planner check-in" (or the last 24 hours if there isn't one): new commits in both repos, new playtest results in the game repo's `Docs/Playtest/`, and new reports and questions on the To-do page, and new entries on [Chat notes](chat-notes.md). If nothing is new and no planner question is unanswered, stop and say so in one line.
3. **Answer the lead's questions** that you can: research (open and cite every page you take numbers from), wiki fixes, data the lead needs, and first passes marked "our pick". File each on its page, add rows to the decision log and changelog, and mark the question answered on the To-do page.
4. **Keep the review rule:** update each item's status on the To-do page from the commits and the playtest results. Tick an item only once the owner has said it's good. Give anything raised in a playtest or report that has no item one.
5. **Queue what needs the owner:** any call that's truly his goes under You: decisions as a short line marked "for the next picks page", with the choices and our suggestion. Never ask him anything during a check-in, and never wait for an answer.
6. **Push:** build with `mkdocs build --strict`, pull with rebase, commit with a message starting "Planner check-in:", and push. Never change the game repo, never commit secrets, and never delete anything.
7. **Cloud check-in only, picks pages:** read the answers on each open picks or review page linked under You: decisions, file them, and once a page is fully answered, archive it as `CLAUDE.md` says and delete it (if the delete needs a confirmation nobody can give, leave it and note on the To-do page that it's archived and ready to delete). If questions are queued, post them on one new page with only open questions, link it under You: decisions, and start the summary with "New picks page".
8. **Finish** with a short summary: what you answered, filed, and queued.

### Lead check-in steps

The lead couldn't start its own recurring task (2026-11-24), so you start it. First ask the lead to add the allow rules its check-in needs to its `.claude/settings.json` (pulling, committing, and pushing the wiki at `C:/Dev/br-game-wiki`, and editing files there), so the check-in never stops to ask you. Then on the PC, type this one line into the lead's session (in its terminal, not from the phone). `30m` runs it every half hour, on the hour and the half hour:

```text
/loop 30m Lead check-in: pull the wiki and follow the "Lead check-in steps" on docs/planning/ai-team.md exactly.
```

It stops when that session closes and after 7 days, so type it again after a restart and every Monday. As a backstop either way, the lead pulls the wiki and reads the To-do page at the start of every task and after every step it finishes.

The check-in runs this:

```text
Lead check-in. Pull the wiki (DerrickSpartan1/br-game-wiki), then read its
To-do page (new planner answers in For the lead, each item's status, and the
Review status) and the newest entries on its Chat notes page. Update your plan from them. File any new question for the
planner under your latest report on the To-do page, and put anything built
since your last check-in on the playtest checklist for the owner. Push your
wiki notes (pull --rebase first). Don't ask the owner anything here and don't
start new build work in the check-in itself, unless the owner told you to keep
working through the list. If nothing changed, say so in one line.
```

### Setting up the planner's check-in on your PC

**If runs stop to ask you for approval (2026-11-24):** the task is in Manual mode, where every tool it hasn't been allowed stops the run until you answer. Fix it once: in the Claude desktop app's Code tab, click **Scheduled**, open **planner-check-in**, click the pencil (Edit), and in the instructions box's toolbar change the permission mode from **Manual** to **Auto**, then save. Click **Run now**, and if anything still asks, choose **Always allow**, which the task remembers ([Claude Code docs](https://code.claude.com/docs/en/desktop-scheduled-tasks.md#permissions-for-scheduled-tasks)). If Auto isn't in the list, pick **Accept edits** and use Always allow the same way.

The first setup:

Once, in the Claude desktop app's Code tab, start a session and paste this:

```text
Set up a local scheduled task for me (only on this computer):
- Name: planner-check-in
- Folder: C:\Dev\planner. Create it if needed, and clone
  https://github.com/DerrickSpartan1/br-game-wiki into it as br-game-wiki.
  Also clone https://github.com/DerrickSpartan1/br-game into it as br-game
  with GIT_LFS_SKIP_SMUDGE=1 set, so the big art files aren't downloaded.
  Don't use the lead's own folders.
- Schedule: custom cron 15,45 * * * * (every half hour at :15 and :45, my time).
- Permission mode: auto, so it never stops to ask me.
- Instructions: "You are the planner's half-hourly check-in for Derrick's
  battle royale. Work only in C:\Dev\planner. Pull br-game-wiki, fetch and
  fast-forward br-game, then follow the 'Planner check-in steps' in
  br-game-wiki/docs/planning/ai-team.md exactly. Skip step 7, which is for the
  cloud check-in."
Then check that Python 3 is installed (the wiki's build needs it), click
Run now once, and allow anything it asks for so later runs don't stop.
```

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
