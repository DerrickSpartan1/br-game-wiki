# Contributors

How other people help build the game with their own Claude, without two people doing the same work. The owner asked for it on 2026-11-25: "something we also need to work on is like a contributor system where other people could help me work on the game with their claude", "we wanna make sure that overlapping work isn't done", and "i would invite the people specifically".

Status: first pass by the planner (2026-11-25). The owner's calls are marked; the rest is our pick, for the owner's review ([To-do](to-do.md#you-decisions)). Nothing here is set up yet.

## In short

- **Invite only (owner):** the owner invites each person by their GitHub username. Nobody joins on their own, and the game repo stays private.
- **Their own Claude:** each contributor runs Claude Code on their own PC, on their own Claude plan. The game repo's `CLAUDE.md` and its agent files guide their Claude the same way they guide the lead ([AI team](ai-team.md)).
- **One task at a time, claimed first:** every piece of work is a task on one shared board. A contributor claims a task before starting, works on it in its own branch, and sends it back as a pull request. The lead reviews it and the owner approves it before it joins the game.
- **The wiki stays the design:** contributors and their Claudes read the wiki; design ideas go to the owner, who passes them to the planner, so the wiki keeps one author.

## No overlapping work

The owner's rule: nobody does work someone else is already doing. Seven guards, from the board down to single files (our pick):

1. **One board.** Every task is a GitHub issue in the game repo, shown on a GitHub Project board (both free). An issue with someone assigned to it is taken. The lead turns the wiki To-do's items into issues and keeps them in step; the To-do stays the planner's and lead's list. Issues rather than the wiki, because claiming has to be instant and one person at a time, and the wiki is public.
2. **Claim before you start.** Assign yourself the issue first, then start. Each person holds at most 2 claims at once. A claim with no commits for 3 days goes back on the board, after a note to the person.
3. **Each task names its area and folders.** Code, art, animation, sound, map, UI, or tools, and the folders it may touch, the same way the lead's workers each own folders ([AI team](ai-team.md)). Work stays inside them; anything outside needs its own task.
4. **Lock binary files.** Unreal assets and maps can't be merged, so the repo already marks them lockable in Git LFS. Lock a file before editing it (`git lfs lock`), and unlock it when the pull request is in. A file someone else has locked is theirs until it's unlocked, and Claude checks `git lfs locks` before touching one.
5. **Small branches, merged often.** One branch per task, named `<github-name>/<issue number>-<short-name>`. Pull the main branch every day, and keep pull requests small, one task each.
6. **Check before every session.** A contributor's Claude starts each session by pulling the main branch, reading `CLAUDE.md` and this page, then checking the board, the lock list, and open pull requests that touch the same files. It works only on its claimed issue.
7. **The lead watches for overlap.** At each check-in the lead also reads the open issues, branches, and pull requests, and flags any two that touch the same thing.

## Access and safety

- **What GitHub allows today:** the game repo is on the owner's personal account with GitHub Free. Anyone invited gets full write access, and the main branch can't be protected: asked for branch protection, GitHub answers "Upgrade to GitHub Pro or make this repository public to enable this feature" (checked 2026-11-25).
- **Our pick, GitHub Pro (about $4 a month):** it adds protected branches, required pull request reviewers, and code owners to private repositories, so nobody, the lead included, can push straight to the main branch, and every change needs the owner's approval ([GitHub's plans](https://docs.github.com/en/get-started/learning-about-github/githubs-plans), [GitHub changelog, 2020](https://github.blog/changelog/2020-04-14-private-repositories-with-unlimited-collaborators-available-to-all-github-accounts-and-changes-to-github-paid-plans/)).
- **The bigger option, an organization on GitHub Team ($4 per person a month):** moving the repo into a GitHub organization adds roles (read, triage, write) and teams, even on the free plan; Team adds the same protections as Pro and 250 GB of LFS storage and downloads instead of 10 ([GitHub's plans](https://docs.github.com/en/get-started/learning-about-github/githubs-plans), [GitHub pricing](https://github.com/pricing)). Worth it once there are several regular contributors.
- **Two-factor sign-in for everyone,** the least access each person needs, and access removed the day someone stops.
- **No secrets in the repo.** Each contributor's Unreal MCP server stays on their own PC and is never opened to the network, the same rule as the lead's.
- **Claude reviewing pull requests on GitHub (later):** Claude Code GitHub Actions can review every pull request or answer `@claude` in issues and pull requests. It follows the repo's `CLAUDE.md`, only runs for people with write access, and costs GitHub Actions minutes plus a Claude API key or a subscription token ([Claude Code docs: GitHub Actions](https://code.claude.com/docs/en/github-actions)). Our pick: not yet; the lead's reviewer checks pull requests for now.

## Storage

- **Git LFS limits:** GitHub Free and Pro include 10 GB of LFS storage and 10 GB of downloads a month; Team includes 250 GB of each. Contributors' downloads count against the repository owner. Over the limit with no payment method set, LFS stops until the next month ([GitHub docs: Git LFS billing](https://docs.github.com/en/billing/concepts/product-billing/git-lfs)).
- **What that means now:** the files in LFS today come to about 1.2 GB (1,236 files), so each new contributor's first download uses about 1.2 GB. About 8 fresh downloads a month fit in 10 GB, fewer as the game grows.
- **Our pick:** before inviting anyone, set a small monthly budget on LFS, or move to Team, so nobody is cut off mid-month.

## Legal

- **A contributor agreement before access (our pick):** everything a contributor makes belongs to, or is licensed to, the owner, so he can ship and sell the game; the private repo stays confidential; and contributors are credited. A lawyer should write it; it ties into [Copyright and AI](legal-review.md#copyright-and-ai). We're not lawyers.
- **Unreal Engine:** each contributor accepts Epic's license themselves, and links their own Epic and GitHub accounts if they need the engine source for the dedicated server.
- **Same rules as ours:** no real brands, nothing copied from PUBG or other games, and every number keeps its source ([Legal review](legal-review.md)).

## Who does what

| Who | Does |
| --- | --- |
| Owner | Invites people, approves pull requests, and makes design calls |
| Planner (Claude chat) | Design and the wiki; writes tasks into the To-do |
| Lead (Claude Code on the owner's PC) | Turns tasks into issues, reviews pull requests with its reviewer, watches for overlap, and merges once the owner approves |
| Contributor and their Claude | One claimed issue at a time, in its own branch, following `CLAUDE.md`, [Coding practices](coding-practices.md), and the reviewer's checklist, then a pull request |

## For the lead, when the owner says go

- A `CONTRIBUTING.md` in the game repo that sums up this page.
- A `contributor` agent file in `.claude/agents/`: works only on its claimed issue, never pushes to the main branch, checks the board, locks, and open pull requests at the start of each session.
- Issue templates (task, bug, playtest note), area labels, the Project board, and a pull request template with the reviewer's checklist.
- Branch protection and code owners, if the owner moves to Pro or Team.

## Open

The owner's calls, for the next picks page:

1. The board: GitHub Issues and a Project board (our pick), or the wiki To-do.
2. GitHub Pro (our pick), an organization on Team, or staying on Free.
3. A contributor agreement before anyone gets access (our pick: yes).
4. Claims: at most 2 at once, and back on the board after 3 quiet days (our pick).
5. Claude reviewing pull requests on GitHub: later (our pick) or now.
6. An LFS budget, or Team's bigger storage, before the first invite.
