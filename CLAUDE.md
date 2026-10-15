# Wiki maintenance guide

This repo is the design wiki for a PC battle royale (2018 PUBG feel, rotating gun and ammo pools). Claude maintains it from conversations with the owner. Pages live in `docs/` and publish to GitHub Pages through MkDocs Material.

## Layout

- `docs/index.md`: home page and core concept.
- `docs/rules.md`: rules that apply to every gun (fixed versions, fixed triggers, no jamming, no overheating, random recoil, open-bolt delay, 3rd slot, versions).
- `docs/systems/`: one page per game system (weapon pool, ammo, attachments, TTK, gameplay, armor, class items, crafting, skins, seasons, maps, servers).
- `docs/weapons/<category>/`: one page per gun family plus an `index.md` table per category. Categories: `pistols`, `shotguns`, `smgs`, `assault-rifles`, `crate`. Add a folder when a new category starts (`battle-rifles` for battle rifles & DMRs, which are one category, then LMGs, snipers, special).
- `docs/planning/`: gun queue, add-later list, open questions, decision log, idea inbox, changelog, gun page template.
- `mkdocs.yml`: site config and the full nav. Every new page must be added to `nav`.

## Adding a gun

1. Research it (Wikipedia first, then manufacturer or reference pages). Open every page you take numbers from and cite it.
2. Build the page from `docs/planning/gun-page-template.md`. Merge versions that fire the same round and differ only in small details; note what merged and how many were made. Unset numbers stay `TBD`; mag tiers are "best guess, review later" unless all real mags.
3. Tag open-bolt guns and list them on `docs/rules.md`.
4. Update, in the same commit: the category `index.md` table, the caliber table on `docs/systems/ammo.md`, `docs/planning/queue.md`, offshoots on `docs/planning/add-later.md`, the `nav` in `mkdocs.yml`, the entry count on `docs/weapons/index.md`, and `docs/planning/changelog.md`.

## Decisions and ideas

- A decision goes on its rules or systems page and gets a dated row in `docs/planning/decisions.md` (newest first).
- A new idea goes on the page it fits, or in `docs/planning/idea-inbox.md` if it fits nowhere yet. The owner wants every game idea shared in chat filed without being asked.
- Settled open questions come off `docs/planning/open-questions.md`.

## Style

Plain, specific, short sentences. Real-world quirks such as jams or overheating are flavor text only. Gun names link to their pages. No emoji.

## Before pushing

Run `pip install -r requirements.txt` then `mkdocs build --strict`; it must finish with no warnings. Keep `mkdocs` pinned below 2.0.
