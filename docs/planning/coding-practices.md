# Coding practices

How the game's code is written, organized, commented, and tested, so it stays easy to read and change as it grows (owner asked, 2026-11-24). The lead and the coder follow it, and the reviewer checks every code step against the checklist at the end. Where folders and assets go is on [Project layout](project-layout.md).

The base is Epic's own C++ coding standard ([Epic](https://dev.epicgames.com/documentation/en-us/unreal-engine/epic-cplusplus-coding-standard-for-unreal-engine)). Epic's reason for having one: most of a program's cost is in maintaining it, and shared conventions let anyone understand new code quickly.

## Naming

- **Prefixes, as Epic uses them:** `A` for actors, `U` for other objects and components, `F` for structs, `E` for enums, `I` for interfaces, `T` for templates. Names are PascalCase with no underscores.
- **Clear over short:** names say what a thing is, without heavy abbreviation. `ReloadSecondsLeft`, not `RldT`.
- **Booleans** start with `b` (`bIsAiming`), and functions that answer yes or no ask a question (`IsDown()`, `CanPickUp()`).
- **The game's own names, not the template's:** new classes start with `BR` (`ABRZone`, `UBRInventoryComponent`). The core classes still named after Unreal's template (`AShooterCharacter`, `AShooterPlayerController`) get renamed when it's convenient, with redirects so Blueprints keep working.

## Comments

- **Say why, not what.** Code shows what it does; comments say why it does it, in plain short sentences. Epic: "Code documents the implementation while comments document the intent."
- **Point to the wiki.** When code follows a design rule, the comment names the wiki section it comes from (`// Wiki Gameplay > Melee: ...`), so anyone can check the rule.
- **Every file starts with a line or two** on what it's for.
- **Every public function in a header** gets a short doc comment (`/** ... */`): what it does, the units of its inputs (meters, seconds, km/h), their valid range, and what it returns.
- **Never let a comment disagree with the code.** Change both together. If code needs a long comment to make sense, rewrite the code instead.
- **No commented-out code** in commits; git keeps the history. `TODO` lines name what's missing and where it's tracked.

## Writing the code

- **Mark what doesn't change:** functions that don't change their object are `const`, and inputs that aren't changed are passed as `const` references.
- **Include what you use** in each file, and forward-declare classes in headers where you can, so builds stay fast.
- **No magic numbers.** A number from the wiki comes from the generated data tables. A number the wiki hasn't set is a named placeholder in Project Settings (BR Gameplay, BR Zone, and so on), with a comment saying it's a placeholder and which wiki section will set it. Other fixed numbers get a named constant.
- **Enums over true/false flags** when a function needs a mode (`EBRDropMode::ToGround`, not `bool bDrop`).
- **`enum class`, `nullptr`, `TObjectPtr`** for object pointers in properties, and Epic's containers (`TArray`, `TMap`).
- **Avoid `auto`** except where Epic allows it, so the type stays visible to the reader.
- **Public first** in a class: what other code uses goes at the top, the inner workings below.

## How the code is organized

- **One job per class.** When a class grows past about 800 lines or does several jobs, split the jobs into components (`UActorComponent`) or subsystems. The character's healing, melee, revives, and vault opening are each a good component.
- **One system, one folder** in `Source/BRGame` (`Weapons/`, `Match/`, `Items/`, `UI/`, `Online/`), matching the content folders on [Project layout](project-layout.md).
- **Gameplay in C++, tuning in Blueprints:** Blueprint subclasses hold numbers, art, and layout; the rules live in C++.
- **No hard-coded asset paths** in C++. Assets are set in Project Settings or Blueprint defaults, so moving an asset in the editor doesn't break the code. Any that remain are listed in the game repo's `CLAUDE.md`.
- **Test commands in one place,** refused on real match servers, as now.
- **Delete what isn't used,** like leftover template code. Git keeps it if it's ever needed.

## Multiplayer

- **The server decides** hits, damage, loot, and the zone. Clients ask; the server checks and answers.
- **Every server request checks its inputs on the server:** the player is alive and able, the thing is in reach, it's theirs to use, and it isn't too soon. Epic calls this "trust and verify" ([Epic: RPCs](https://dev.epicgames.com/documentation/en-us/unreal-engine/remote-procedure-calls-in-unreal-engine)). A check that can only fail for a cheater can use `WithValidation`, which disconnects that player.
- **Reliable only when it must arrive:** a state change the player can't lose (fire start and stop, reload, pick up). Sounds, effects, and other cosmetic calls are unreliable, since reliable calls cost bandwidth and hold up the calls behind them.
- **State that lasts is replicated,** not sent as a one-off call, so a player who joins late or misses a packet still sees it.

## Logging

- **Each system has its own log category** (`LogBRZone`, `LogBRLoot`), never `LogTemp`, so the logs can be filtered by system.
- **Log** for normal events, **Warning** for wrong or missing data the game can carry on from, **Error** for something broken.
- Messages say what happened and what to do, as the data readers' errors already do.

## Tests

- **Automation tests for rules that could break quietly:** damage by hit zone and armor tier, reload counts (30+1, 29+1), carry capacity, loot and version rolls, the zone's phases, and the healing caps. Write them as Automation Specs (`.spec.cpp` files with `Describe` and `It`), which run from the editor's Session Frontend or the command line ([Epic: Automation Spec](https://dev.epicgames.com/documentation/en-us/unreal-engine/automation-spec-in-unreal-engine)).
- **Run them before every push,** with the build.
- **The data readers** get a small test each: a copy of a wiki page's table that must read, and one with a broken cell that must fail with a clear message.

## The Python tools

- **Shared helpers in one module.** The table-reading helpers (`split_row` and friends) are copied into nine scripts today; they go in one shared file the readers import.
- **Fail loudly, with the wiki section's name,** as they do now, and never guess a number.
- **Plain Python style** (PEP 8), short functions, and a docstring at the top of each script saying which wiki pages it reads and what it writes.

## Commits

- **One feature or fix per commit,** with a message that says what changed and why.
- **Build with no new warnings and pass the tests** before pushing.
- **Generated files** (data tables, CSVs) are committed in the same commit as the reader change that made them.

## The reviewer's checklist

The reviewer checks each code step for these, and fails the step if any is missing:

1. Names follow Epic's prefixes and say what things are; new classes start with `BR`.
2. New files start with a comment on what they're for; public functions have doc comments with units.
3. Comments say why, point to the wiki where a rule comes from, and match the code.
4. No magic numbers: wiki numbers from data tables, placeholders named in Project Settings.
5. Server requests check their inputs on the server; cosmetic calls are unreliable.
6. Its own log category, not `LogTemp`.
7. No hard-coded asset paths, commented-out code, or unused leftovers.
8. No class or file grew past about 800 lines without a reason; a new job went into a component.
9. Tests cover any rule the step changed, and they pass.
10. It builds with no new warnings.

## The planner's check of the code (2026-11-24)

The planner read the game repo's source (it can't build it), so the lead should confirm each point.

**What's already good:**

- Comments say why and name the wiki rule they follow, in plain words.
- Every number the wiki sets comes from a generated data table, and the readers stop with a clear message when a page changes.
- Server requests checked so far test reach and state on the server, and test commands are refused on real match servers.
- Most object properties already use `TObjectPtr` (151), there's only one `TODO`, and the character's code is already split into files by feature.

**What to fix, in this order, one commit each:**

1. **Template leftovers:** the Horror template's code (`Variant_Horror`, 569 lines) is still compiled though nothing uses it, and the template's AI enemies (`Variant_Shooter/AI`) aren't used outside their own folder either. Check no Blueprint uses them, then delete them.
2. **Log categories:** `LogTemp` is used 38 times; give each system its own category.
3. **Tests:** there are no automation tests yet. Start with damage, reloads, and carry capacity.
4. **Shared Python helpers:** move the table helpers copied into nine readers into one module.
5. **Raw pointers:** 23 object properties still use raw pointers; switch them to `TObjectPtr`.
6. **Asset paths:** 23 hard-coded `/Game/...` paths in C++ (most in constructors); move them into settings or Blueprint defaults as each file is touched.
7. **Big files:** `BRGun.cpp` (2,255 lines), `ShooterPlayerController.cpp` (2,196), `BRInventoryComponent.cpp` (1,234), `BRSky.cpp` (1,218), and the character (`ShooterCharacter.h` is 1,170 lines on its own). Split them into components as they're worked on, not all at once.
8. **Names and folders:** rename the core `Shooter*` classes to `BR*` and move them out of `Variant_Shooter` when there's a quiet moment, with class redirects so Blueprints keep working.
9. **Reliable calls:** 37 of the 41 network calls are reliable. Most are state changes that should be; check that the cosmetic ones (sounds, alarms, effects) are unreliable.

## Sources

- [Epic: C++ coding standard for Unreal Engine](https://dev.epicgames.com/documentation/en-us/unreal-engine/epic-cplusplus-coding-standard-for-unreal-engine)
- [Epic: Remote procedure calls](https://dev.epicgames.com/documentation/en-us/unreal-engine/remote-procedure-calls-in-unreal-engine) (reliable and unreliable, trust and verify)
- [Epic: Automation Spec](https://dev.epicgames.com/documentation/en-us/unreal-engine/automation-spec-in-unreal-engine)
