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

| # | Version | What's different | Cartridge | Made | Merged from | Fire modes | RPM | Open bolt |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | <name> | <differences> | <cartridge> | <numbers made> | <merged models> | <fire modes> | <rate> | <Yes, No, or Auto only> |

## Sources

- [Wikipedia: <Gun>](https://en.wikipedia.org/wiki/<Gun>)
````

## Reading pages as data

The game repo turns these pages into data tables with a script, so every gun page keeps the same shape:

- The spec table always has these seven rows, in this order: Category, Cartridge, History, Magazine (rounds), Fire mode / rate, Damage, Effective range.
- Every gun page, pistol / 3rd-slot pages included, has a `## Versions` table with exactly these nine columns: `#`, `Version`, `What's different`, `Cartridge`, `Made`, `Merged from`, `Fire modes`, `RPM`, `Open bolt`. A gun with one version still gets a one-row table.
- Each Cartridge cell holds exactly one name from the Caliber column on the [Ammo](../systems/ammo.md) page, or `TBD`. Notes about the cartridge go in "What's different", never in the Cartridge cell. Other spellings go in the ammo page's "Also called" column.
- `(rare)` after a version name marks a rare spawn.
- **Fire modes:** a comma-separated list from this set: `semi`, `auto`, `2-round burst`, `3-round burst`, `2-round hyperburst`, `pump`, `lever`, `straight-pull`, `break action`, `single shot`, `revolver`, `two-pull`. A mode can carry a note in brackets: `3-round burst (no reset)` (letting go mid-burst keeps the rest for the next pull), `pump (slam-fire)`, `auto (fires until empty)`. Modes on the same selector key are listed together, like `semi, straight-pull` for the Mondragón's gas cut-off. `TBD` if unknown. "What's different" can still describe fire modes in plain words, but this column is what the game reads.
- **RPM:** one number or a range, like `800` or `700–970`. A special burst rate goes after a semicolon: `600; hyperburst 1,800`. `TBD` if unknown, which includes most semi-auto and manual guns until the max rate is set.
- **Open bolt:** `Yes`, `No`, `Auto only` (open bolt on auto, closed on semi, like the FG 42), or `TBD`. Must match the [Rules](../rules.md#open-bolt-delay) list.
- `TBD` means not set yet, `Unknown` (in Made) means the sources don't say, and `—` means none.
- Pistol / 3rd-slot pages name their parent long gun in their first line.
