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
