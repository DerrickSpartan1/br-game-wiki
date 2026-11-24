# Wiki maintenance guide

This repo is the design wiki for a PC battle royale (2017–2018 PUBG feel, rotating gun and ammo pools). Claude maintains it from conversations with the owner. Pages live in `docs/` and publish to GitHub Pages through MkDocs Material. The game's code lives in the private repo `DerrickSpartan1/br-game`, which has its own `CLAUDE.md`; this wiki stays the design source of truth.

## Layout

- `docs/index.md`: home page and core concept.
- `docs/rules.md`: rules that apply to every gun (fixed versions, fixed triggers, no jamming, no overheating, random recoil, open-bolt delay, en bloc clips, 3rd slot, versions).
- `docs/systems/`: one page per game system (weapon pool, loot and spawning, ammo, attachments, TTK, starting damage and the crate line, handling, healing, gameplay, match flow, armor, class items, crafting, skins, seasons, maps, servers).
- `docs/weapons/<category>/`: one page per gun family plus an `index.md` table per category. Categories: `pistols`, `shotguns`, `smgs`, `assault-rifles`, `battle-rifles` (battle rifles & DMRs, one category), `lmgs`, `snipers`, and `crate`. Add a folder when a new category starts (special next).
- `docs/planning/`: to-do list, AI team, gun queue, add-later list, open questions, legal review, game names, decision log, idea inbox, changelog, gun page template, and the art guides. Every item handed between the planner and the lead needs the owner's review: tick a to-do item only once he has said it's good (his playtest results in the game repo's `Docs/Playtest/`, or a review page), and give every open item a status (with the planner, with the lead, waiting on your review, needs work). Check the game repo's commits for the lead's items, and give anything raised in a playtest or report that has no item one, so nothing is lost (owner, 2026-11-24).
- `mkdocs.yml`: site config and the full nav. Every new page must be added to `nav`.

## Roles

Claude in chat is the planner: design, research, and this wiki. Claude Code on the owner's PC is the lead, with subagent workers ([AI team](docs/planning/ai-team.md)). Work for the lead goes in the To-do page's "For the lead" section, with a prompt where one helps. The planner reads the game repo but never changes it.

The planner and the lead check in every half hour (planner at :15 and :45, lead at :00 and :30); a scheduled planner check-in follows the "Planner check-in steps" on `docs/planning/ai-team.md`, and never asks the owner anything: questions for him are queued for the next picks page. At the start of every session, pull this repo and the game repo, then read the To-do page for the lead's reports and planner questions. Do the planner's items without waiting to be asked: answer what the planner can (research, wiki fixes, first-pass picks marked "our pick"), file the answers, and mark each question answered on the To-do page.

## Adding a gun

1. Research it (Wikipedia first, then manufacturer or reference pages). Open every page you take numbers from and cite it.
2. Build the page from `docs/planning/gun-page-template.md`. Merge versions that fire the same round and differ only in small details; note what merged and how many were made. Unset numbers stay `TBD`; mag tiers are "best guess, review later" unless all real mags. Every page gets the twelve-column Versions table, even with one version: each Cartridge cell is exactly a Caliber name from `docs/systems/ammo.md` or `TBD`, and the Fire modes, RPM, Open bolt, Reload, Mag, and Damage columns use the template's fixed wording (see "Reading pages as data" on the template), since the game repo parses these pages.
3. Tag open-bolt guns and list them on `docs/rules.md`.
4. Update, in the same commit: the category `index.md` table, the caliber table on `docs/systems/ammo.md`, `docs/planning/queue.md`, offshoots on `docs/planning/add-later.md`, the `nav` in `mkdocs.yml`, the entry count on `docs/weapons/index.md`, and `docs/planning/changelog.md`.

## Decisions and ideas

- A decision goes on its rules or systems page and gets a dated row in `docs/planning/decisions.md` (newest first).
- A new idea goes on the page it fits, or in `docs/planning/idea-inbox.md` if it fits nowhere yet. The owner wants every game idea shared in chat filed without being asked.
- Settled open questions come off `docs/planning/open-questions.md`.
- Calls that need the owner, when there are more than a few, go on a picks page: an artifact with a choice and a comment box on each item. The answers are read back from the page and filed. Once a page is answered and filed, copy its answers to `docs/planning/picks-archive.md`, save the page's HTML and its saved answers in `archive/picks/`, and delete the page; the next batch goes on a new page with only the questions still open (owner, 2026-11-24).

## Legal review

Anything named after a real brand, company, product, person, or another game's own term gets a generic name for the game and a row on `docs/planning/legal-review.md`. Game names live on `docs/planning/game-names.md`: a new gun goes under its maker's stand-in there (add a stand-in for a new maker). The wiki can keep real names as references. No Red Cross emblem anywhere in the game.

## Style

Plain, specific, short sentences. Real-world quirks such as jams or overheating are flavor text only. Gun names link to their pages. No emoji.

## Before pushing

Run `pip install -r requirements.txt` then `mkdocs build --strict`; it must finish with no warnings. Keep `mkdocs` pinned below 2.0.
