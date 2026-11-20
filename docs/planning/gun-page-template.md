# Gun page template

Every new gun family gets a page built from this template, saved as `docs/weapons/<category>/<slug>.md`. Pistol versions of long guns get their own page in the pistol folder that links back to the parent.

````markdown
# <Gun name>

| Spec | Detail |
| --- | --- |
| Category | <Pistol / 3rd slot, Shotgun, SMG, Assault rifle, ...> |
| Cartridge | <main cartridge, or "Varies by version: X (main), Y, or Z"> |
| History | <country; designer and year; production years; numbers made; main users and wars> |
| Magazine (rounds) | <standard capacity; other real mags> |
| Fire mode / rate | <modes and RPM; open or closed bolt (open-bolt delay or not)> |
| Damage | TBD |
| Effective range | Real-world <x> m; in-game TBD |

## Real-world notes

<weight; barrel length; action; what makes it feel different; famous quirks (flavor only, no jams or overheating)>

## In-game traits

One roster entry that rolls one of <N> versions (see [Versions](#versions) below). <how it should play>

## Attachments

<attachment family>; <scope mount: native rail, adapter mount, or game-version mount>. Unique: <real accessories>. Mag tiers (best guess, review later): <standard>; <makeshift extended and quick>; <extended quick>; <extended>

## Versions

<N> versions after merging. <what became skins; what went to the add-later list>

| # | Version | What's different | Cartridge | Made | Merged from |
| --- | --- | --- | --- | --- | --- |
| 1 | <name> | <differences> | <cartridge> | <numbers made> | <merged models> |

## Sources

- [Wikipedia: <Gun>](https://en.wikipedia.org/wiki/<Gun>)
````

## Reading pages as data

The game repo turns these pages into data tables with a script, so every gun page keeps the same shape:

- The spec table always has these seven rows, in this order: Category, Cartridge, History, Magazine (rounds), Fire mode / rate, Damage, Effective range.
- Every gun page, pistol / 3rd-slot pages included, has a `## Versions` table with exactly these six columns: `#`, `Version`, `What's different`, `Cartridge`, `Made`, `Merged from`. A gun with one version still gets a one-row table.
- Each Cartridge cell holds exactly one name from the Caliber column on the [Ammo](../systems/ammo.md) page, or `TBD`. Notes about the cartridge go in "What's different", never in the Cartridge cell. Other spellings go in the ammo page's "Also called" column.
- `(rare)` after a version name marks a rare spawn.
- Fire modes are written in plain words in "What's different" (for example "semi and auto" or "semi-auto only"). A version that doesn't say uses the page's Fire mode / rate row.
- `TBD` means not set yet, `Unknown` (in Made) means the sources don't say, and `—` means none.
- Pistol / 3rd-slot pages name their parent long gun in their first line.

