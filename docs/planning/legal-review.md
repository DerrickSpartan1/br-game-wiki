# Legal review

Anything in the game that could cause legal trouble gets a generic name or a new look before it ships. This page is the process and the running list. It catches problems early; it isn't legal advice. Before the game is sold or shown publicly, a lawyer who works on game IP goes through this list.

**For now:** the game is private, for the owner and friends. If it grows past that, the owner will look at hiring people and at a lawyer.

## The process

1. **When something is added,** the planner checks it against [What to check](#what-to-check). If it uses a real brand, company, product name, person, or another game's own name, it gets a generic name on its page and a row in [The list](#the-list).
2. **Wiki and game names:** the wiki can keep real names as references, so a page says which real gun or Tarkov item something is based on. The game only uses the generic names. Pages show both where it matters, like the Tarkov column on [Healing](../systems/healing.md#variants).
3. **The lead** uses only the generic names in game data, menus, and text, and never puts a real logo, maker's mark, or protected emblem on a model or texture.
4. **Before release:** a full pass over the list with a lawyer, and anything still open gets settled.

## What to check

| Kind | Examples | Rule |
| --- | --- | --- |
| **Brands and companies** | Colt, Glock, Heckler & Koch, FN, SIG Sauer, Salewa, Dacia | No maker or brand names in the game |
| **Product names** | Glock 17, HK416, ACOG, Grizzly medical kit | Generic or changed names. Military designations like M16 are a separate case for the lawyer ([Guns](#guns)) |
| **Other games' names** | PUBG's Mirado and Tukshai, Tarkov's CALOK-B and TarCola, Warzone's Gulag, Counter-Strike's StatTrak | Our own names. Borrowing a mechanic is fine; names, art, sounds, and text aren't |
| **Logos and emblems** | Maker logos and markings on guns, the Red Cross | None on models or textures ([Red Cross emblem](#red-cross-emblem)) |
| **Real people** | Public figures, gun designers whose names are trademarks | No real people's names or likenesses |
| **Real places** | Ischia's towns | The layout is fine; in-game place names are our own (TBD) |
| **Patents** | Unusual mechanics. Nintendo's 2024 suit against Palworld's maker was over Japanese patents on catching and riding creatures | The lawyer checks for patents on any mechanic that isn't a genre staple |
| **Art, sound, and music** | Photos, models, and sounds made by others | Covered by the asset log ([Gun art and sound](art-and-sound.md#licenses-and-the-asset-log)) |

### Red Cross emblem

The red cross on white is a protected emblem under the Geneva Conventions, not a general health symbol. The British Red Cross asked Prison Architect's developers to remove it in late 2016, and they changed it to green. Halo 2 and a later release of Doom also dropped it.

- **Our rule:** no red cross (or red crescent or red crystal) on med items, vehicles, buildings, or the HUD. Med items use another mark, such as a green cross or a plain medical bag.

## Guns

Decided: our own makers and designations, so guns feel real without using real names. Each real maker gets a made-up stand-in, and designations mix real numbers with new letters and names. The makers, the designation rule, and the other game names are on [Game names](game-names.md). The wiki keeps real names either way, and the lawyer checks the final list.

## The list

| What | Where | Problem | Game name | Status |
| --- | --- | --- | --- | --- |
| Meds and drinks | [Healing](../systems/healing.md#variants) | Brand and Tarkov names (Salewa, Grizzly, Celox, CAT, Vaseline, Golden Star, Augmentin, Analgin, Perfotoran, Meldonin, TarCola, and others) | Plain names, on the page | Done |
| Defibrillator | [Class items](../systems/class-items.md) | Tarkov's is a parody of a real brand's | Portable defibrillator | Done |
| Med item art | [Healing](../systems/healing.md) | Red Cross emblem | Another mark | Rule set |
| Guns | Every gun page | Maker names (Colt, Glock, Heckler & Koch, FN, SIG Sauer, Beretta, Steyr, IWI, and others) and trademarked model names | Our own makers and designations ([Game names](game-names.md#gun-makers)) | All 625 versions named ([Gun names](game-names.md#gun-names)) |
| Attachments | [Attachments](../systems/attachments.md) | Brand and model names such as ACOG, Leupold, and PSO-1 | Plain descriptions: 2x scope, vertical foregrip | Rule set |
| Armor | [Armor](../systems/armor.md) | Brand names such as Crye Precision and Ops-Core | Our own names ([Armor](game-names.md#armor)) | Done |
| Breaching tools | [Class items](../systems/class-items.md#breaching-tools) | The Halligan bar is named after a person | Entry bar | Done |
| Vehicles | [Gameplay](../systems/gameplay.md#vehicles-and-water) | Real makes (Dacia, UAZ) and PUBG's own vehicle names | Our own names ([Vehicles](game-names.md#vehicles)) | Named |
| Cartridges | [Ammo](../systems/ammo.md) | Names with a company or person in them, like .338 Lapua Magnum, .308 Winchester, and 7.62×25mm Tokarev | Caliber only ([Cartridges](game-names.md#cartridges)) | Done; two sizes still TBD |
| Other games' terms | [Gameplay](../systems/gameplay.md), [Match flow](../systems/match-flow.md), [Skins](../systems/skins.md#kill-counters) | Gulag, Jailbreak, Most Wanted, StatTrak, and PUBG's "Winner winner chicken dinner" | Our own names ([Game names](game-names.md#other-games-terms)) | First pass |
| First map | [Maps](../systems/maps.md) | Real island and town names | Teplov and our own place names ([Places](game-names.md#places)) | Done |
| PUBG look and feel | Several pages | Specifics copied from PUBG that, together, look like PUBG ([PUBG look and feel](#pubg-look-and-feel)) | Our own versions | Open |
| Hidden data keys | The game's data tables | Real gun, version, cartridge, and armor names stay as hidden row keys, never shown on screen | Fine for the private build (owner, 2026-11-22) | Review before release; replace if the lawyer says so |
| Player-made content | [Custom games and mods](../systems/gameplay.md#custom-games-and-mods-later) | Maps and content made by players need terms on who owns them and what's allowed | Workshop terms | Later |

## PUBG look and feel

Battle royale basics (a plane drop, parachutes, a shrinking zone, airdrops, looting) are shared by the whole genre, and game rules aren't protected. The risk is copying PUBG's specific choices together: in 2022, PUBG's maker sued over Free Fire, claiming it copied the opening, the game structure, the selection of weapons, armor, and objects, the locations, and the color schemes and textures.

| PUBG specific | Ours | Status |
| --- | --- | --- |
| Frying pan that blocks bullets | Back as a class item with our own models and sounds: raised to block, and holed after a set amount of gunfire ([Pans](../systems/class-items.md#pans)) | Decided |
| PUBG's realistic art style | The final look is closer to PUBG's, with our own models, textures, and colors. Krafton's Free Fire suit named color schemes and textures | Decided |
| Care package with a flashing light and red smoke | Our own look and signal | Decided |
| Every PUBG vehicle | Our own vehicles, picked per map; PUBG's lineup is an idea list | Decided |
| PUBG's name in marketing | Never used | Decided |
| Erangel's zone phase numbers | Placeholders to test in game; our own numbers come from play tests | Later |
| PUBG's 2017–2018 HUD | Our own look; the layout can stay similar where it's practical | To do with the HUD mockups |
| Boost bar | Its own name and look | To do |
| "Red zone," "blue zone," and the victory line | Our own words | Open |

## Copyright and AI

Not legal advice; background for when the owner talks to a lawyer.

- **Copyright needs a human author.** The D.C. Circuit held in 2025 that AI can't be an author, and the Supreme Court declined to review it on March 2, 2026. The Copyright Office's 2025 report says prompts alone don't make someone the author; human selection, arrangement, and edits can be protected.
- **What that means here:** untouched AI-made art, sound, and text probably can't be copyrighted. What the owner makes, edits, or arranges by hand can be, and so can the game as a whole, for its human parts.
- **Stronger protection that doesn't depend on authorship:** a trademark on the game's name and logo, trade secrets (the source code stays private and ships compiled), and work-for-hire contracts with anyone hired later.
- **Anthropic's terms** assign to the user whatever rights Anthropic has in Claude's outputs.
- **Steam:** since January 2026, games disclose AI-made content that players see or hear (art, sound, writing). AI tools used behind the scenes, like coding assistants, aren't the focus.
- **Before release:** register the copyright (US works must be registered before suing), file a trademark for the game's name, and keep records of the owner's own choices: the decision log, git history, Blender files, and the asset log.

### Hand-made touches

The owner wants chances to make things by hand so they're clearly his. Easy ones, no experience needed:

- Writing in-game text: item descriptions, the victory line, lore, and tips.
- Picking colors and looks for skins, the HUD, and the crate.
- Placing things in the map editor: buildings, loot spots, and cover.
- Small edits to models and textures in Blender.
- Recording his own sounds on a phone.

## Sources

- [PC Gamer: How the Prison Architect developers broke the Geneva Conventions](https://www.pcgamer.com/how-the-prison-architect-developers-broke-the-geneva-conventions/)
- [US Copyright Office: Copyright and AI, Part 2](https://www.copyright.gov/newsnet/2025/1060.html) · [Mayer Brown: Supreme Court denies review in Thaler v. Perlmutter](https://www.mayerbrown.com/en/insights/publications/2026/03/supreme-court-denies-review-in-ai-authorship-case)
- [PC Gamer: Steam's updated AI disclosure (2026)](https://www.pcgamer.com/software/ai/steam-updates-ai-disclosure-form-to-specify-that-its-focused-on-ai-generated-content-that-is-consumed-by-players-not-efficiency-tools-used-behind-the-scenes/)
- [TechCrunch: Krafton sues Garena, Apple, and Google (2022)](https://techcrunch.com/2022/01/13/pubg-mobile-maker-krafton-sues-apple-google-and-rival-game-developer-garena-over-clones/) · [Game Developer: Krafton and NetEase settle](https://www.gamedeveloper.com/business/krafton-and-netease-settle-over-i-pubg-i-i-knives-out-i-copyright-quarrel)
- [Anthropic Consumer Terms](https://www.anthropic.com/legal/consumer-terms)
- [PC Gamer: Nintendo's patent suit against Palworld's maker (2024)](https://www.pcgamer.com/games/survival-crafting/palworld-developer-reports-nintendos-suing-over-3-pokemon-patents-for-only-usd66-000-in-damages-but-a-videogame-ip-lawyer-says-fighting-the-lawsuit-could-mean-burning-millions-of-dollars)
