# Attachments

Attachments are a core part of the loot hunt, as in original PUBG. If a gun can't normally take a scope, like a WWI SMG, look for a way to fit one if possible.

## Scope mounts

Mounts never depend on crafting.

- **Native rail:** modern guns; any scope fits normally.
- **Adapter mount:** older guns that historically took clamp-on rails or side mounts, like the Mosin, M1 Garand, or AK. The scope sits higher or off to the side, so it's a bit clunkier.
- **No historical mount:** guns like a WWI SMG just come with a mount in the game's version, trading a little realism.

## Attachment slots

Every gun has up to five slots: muzzle, foregrip, sight, stock, and magazine. The set below comes from PUBG. Each attachment fits by family (see [Universal attachments](#universal-attachments)), and each gun page lists what it can take. How much each one helps starts from PUBG's numbers ([Effects](#effects-first-pass-from-pubg)).

**Muzzle** (the "barrel attachments" in the families below):

- **Suppressor:** quieter shots.
- **Compensator:** less recoil.
- **Flash hider:** hides your muzzle flash, with slightly less recoil.
- **Choke:** shotguns only; tighter spread.
- **Duckbill:** shotguns only; a flatter, wider spread (see below).

**Foregrip.** Grips shift a gun's recoil tendencies from the [Rules](../rules.md#random-recoil): climb, sideways drift, and how fast it settles.

- **Vertical grip:** less climb.
- **Angled grip:** less drift and faster aim down sights.
- **Half grip:** less climb and drift, and settles faster.
- **Thumb grip:** less climb, but more drift and slower settling.
- **Light grip:** settles faster, but kicks harder.
- **Laser sight:** tighter hip fire; also fits pistols.
- **Bipod:** see [Bipods](#bipods).

**Sight.** Generic names, with no brands. Every sight needs a mount (see [Scope mounts](#scope-mounts)).

- **Red dot** and **holographic:** 1x.
- **2x, 3x, and 4x** scopes.
- **3–6x:** variable.
- **8x** and **15x:** the 15x is for snipers only.
- **Canted iron sights:** a second sight set off to the side for close range.
- **Thermal:** crate-only.

**Stock:**

- **Tactical stock:** less recoil and sway. It fits both the pistol/SMG family and the AR/LMG/battle rifle family, as in PUBG, where it went on ARs (M416, M16A4), SMGs (Vector, MP5K), and the M249 ([PUBG Wiki: Attachments](https://pubg.wiki.gg/wiki/Attachments)). A gun takes it only if its page lists it: stockless guns take add-on stocks instead, and DMRs and snipers take the cheek pad (our pick, 2026-11-25).
- **Cheek pad:** DMRs and snipers; steadier aim.
- **Add-on stocks:** for stockless guns, like the [Uzi](../weapons/smgs/uzi.md) or [Skorpion](../weapons/pistols/skorpion-vz61.md), and the [C96](../weapons/pistols/c96.md)'s shoulder stock (see below). A pistol with an add-on stock stays in the pistol / 3rd slot ([Rules](../rules.md#3rd-slot)).
- **Ammo loops:** faster one-round-at-a-time reloads, for tubes and stripper-clip guns ([Ammo](ammo.md#how-ammo-and-reloading-work)).

**Magazine:** the four tiers below.

### Effects (first pass, from PUBG)

The owner's call (2026-11-22): PUBG's attachment effects are the base. These are PUBG's 2017–2018 numbers. Our grips shift recoil tendencies rather than a fixed pattern ([Rules](../rules.md#random-recoil)), so "recoil pattern" here means how strong the gun's random climb and drift are.

| Attachment | Effect | Notes |
| --- | --- | --- |
| Compensator (rifles) | Recoil pattern −25%, sideways −10%, climb −15%, base spread −10% | Loud, like no muzzle |
| Compensator (SMGs) | Recoil pattern −25%, sideways −20%, climb −25% | |
| Compensator (DMRs and snipers) | Recoil pattern −25%, sideways −20%, climb −20% | |
| Flash hider | Recoil pattern −10%, sideways −10%, climb −10% | Hides your muzzle flash |
| Suppressor | Spread −5% | Quieter shots and no flash |
| Choke | Pellet spread −18.2% | Shotguns. It doesn't change pellet speed: PUBG's choke page lists only spread ([PUBG Wiki: Choke](https://pubg.wiki.gg/wiki/Choke_(SG))) (our pick, 2026-11-25) |
| Duckbill | Narrower up and down, wider side to side | Shotguns; PUBG gives no numbers |
| Vertical grip | Climb −15%, recoil pattern −20% | Fixed 2026-11-25: PUBG's vertical grip cuts vertical recoil, not sideways ([PUBG Wiki: Vertical Foregrip](https://pubg.wiki.gg/wiki/Vertical_Foregrip)) |
| Angled grip | Sideways −20%, recoil pattern −20%, aim down sights 10% faster | |
| Half grip | Less climb and drift, settles faster | PUBG gives no numbers; TBD |
| Thumb grip | Less climb, more drift, settles slower | PUBG gives no numbers; TBD |
| Light grip | Settles faster, more climb and drift | PUBG gives no numbers; TBD |
| Laser sight | Tighter hip fire | TBD |
| Tactical stock | Kick −10%, sway −10%, recoil pattern −20%, settles 15% faster | |
| Cheek pad | Kick −20%, sway −15%, climb −20% | DMRs and snipers |
| Add-on stock (Uzi-style) | Climb −20%, recoil pattern −20%, settles 15% faster | From PUBG's Micro Uzi stock |
| Ammo loops | Reload −30% | Kar98k-style loops also cut base spread 50% in PUBG |
| Quick mag | Reload −30% | ([Handling](handling.md#reload-times)) |
| Extended quick mag | Reload −15% | Half the quick mag's cut, since it's the middle ground between the quick and extended mags ([Magazines](#universal-attachments)) (our pick, 2026-11-25) |

**Reading the table (our picks, 2026-11-25, from the lead's questions):**

- **Recoil pattern** scales how strong the gun's random climb and drift are overall. A row that also names climb or sideways multiplies them: the rifle compensator's climb is 0.75 × 0.85 = 0.6375 of the gun's own.
- **Kick** is the size of each shot's visual jump of the gun and view, which then settles back. It isn't the random climb and drift, and it doesn't change how long settling takes ("settles faster" does that). PUBG calls it "Animation Kick" and calls its cheek pad's effect a weaker "recoil animation" ([PUBG Wiki: Tactical Stock](https://pubg.wiki.gg/wiki/Tactical_Stock), [PUBG Wiki: Cheek Pad](https://pubg.wiki.gg/wiki/Cheek_Pad_(DMR,_SR))).
- **"Aim down sights 10% faster"** means 10% more speed, so the time is divided by 1.1, as PUBG's "+10% ADS Speed" ([PUBG Wiki: Angled Foregrip](https://pubg.wiki.gg/wiki/Angled_Foregrip)).
- **Suppressor "Spread −5%"** cuts all spread, hip and aimed: PUBG's stat is plain "Deviation" ([PUBG Wiki: Suppressor](https://pubg.wiki.gg/wiki/Suppressor_(AR,_DMR,_S12K))).
- **Ammo loops "Reload −30%"** makes each round load 30% faster, since loops only fit one-at-a-time reloads.
- **Pistols:** pistols and SMGs share one attachment family ([Universal attachments](#universal-attachments)), so a pistol whose page lists a compensator gets the SMG compensator's numbers. PUBG later merged its pistol and SMG attachments the same way ([PUBG Wiki: Attachments](https://pubg.wiki.gg/wiki/Attachments)).
- **Rows marked TBD** (half, thumb, and light grips, the laser, the duckbill) and numbers the table doesn't give (suppressor loudness, scope aim-down-sights times) stay named placeholders until the owner sets them.

**Canted iron sights (our pick, 2026-11-25):** a separate key switches between the main sight and the canted irons while aiming, Alt + right mouse by default like PUBG, and rebindable. Aiming through them rolls the gun 45° so the side sight lines up; shooting works the same ([PUBG Wiki: Canted sight](https://pubg.wiki.gg/wiki/Canted_sight)). Build it now, with the attachments.

## Wear

Some items wear out with use (owner, 2026-11-22). Guns themselves never jam or overheat ([Rules](../rules.md)).

- **Suppressors:** every suppressor wears out. The [improvised suppressor](crafting.md#what-a-workbench-makes) goes after about 60 shots; real ones last much longer. Their numbers, and what wearing does before one breaks, are TBD.
- **The StG 44's Krummlauf:** the curved barrel wears out, after about 300 rounds in real life ([StG 44](../weapons/assault-rifles/stg-44.md)).

## Bipods

- **Built in:** a gun whose real standard version came with a bipod, like most LMGs, has it built in.
- **Attachment:** any other gun that can take one, like a sniper rifle, uses a bipod as a foregrip attachment, in the foregrip's place.
- A built-in bipod fills the foregrip slot, so that gun can't take a foregrip (see [Built-in parts](#built-in-parts)).
- **Deploying:** a bipod deploys on cover or when lying prone, with its own deploy button.

## Built-in parts

A version that comes with an attachment already on it keeps it for the match. The part fills its slot, so it can't be removed or swapped for another:

- A gun with a built-in bipod can't take a foregrip.
- A [Mini Uzi](../weapons/smgs/uzi.md) comes with its folding stock, so it can't drop it or take a different stock.
- The [AS Val](../weapons/assault-rifles/as-val.md)'s built-in suppressor fills its muzzle slot.

This follows the rule that the [spawned version is fixed](../rules.md#spawned-version-is-fixed).

## Universal attachments

Attachments are universal within weapon families instead of gun-specific, to keep things simple.

- **Pistols & SMGs:** shared silencer and barrel attachments.
- **ARs, LMGs & battle rifles:** shared silencer and barrel attachments.
- **Shotguns:** shared barrel and silencer attachments.
- **DMRs & snipers:** shared silencer and barrel attachments.

Battle rifles and DMRs share one roster category, but each gun uses the family that fits it: battle rifles (a soldier's main rifle, select-fire or not) take the AR family, and scoped marksman rifles take the DMR family. Each gun page says which.

Some pistols, like the C96, also have a shoulder stock slot that takes the gun's real stock or a makeshift one.

**Revolvers:** revolvers load one round at a time ([Staged reloads](handling.md#staged-reloads)). Instead of mag tiers, they get reload attachments like speed loaders (and similar, such as speed strips and moon clips) that fill every chamber at once, at the same capacity. A speed loader spawns only in matches where a revolver that can use one spawns (owner, 2026-11-22). If a revolver has a real higher-capacity cylinder, like 10 rounds where the normal one holds 8, that cylinder counts as its extended mag. This goes by whatever the real-world info supports.

Magazines follow the same families, in four tiers:

| Tier | Capacity | Notes | Example: M17/M18 (rounds) |
| --- | --- | --- | --- |
| Standard | Base |  | 17 |
| Makeshift extended | Small boost |  | 21 |
| Quick mag | Same as makeshift extended | Fastest reload | 21 |
| Extended quick mag | Between quick and extended | Middle ground between extended and quick | 31 |
| Extended | Biggest feasible | Heavier, slower ADS, and slower reload; for pistols, a round drum (real 50-round P320 drums exist) | 50 |

Bigger mags are balanced by weight, ADS speed, and reload time. Source: [ProMag SIG P320 50-round drum](https://gunmagwarehouse.com/promag-sig-sauer-p320-9mm-50-round-drum-magazine.html)

**Mag-fed shotguns:** they use the assault rifle family's magazine attachments. On a shotgun, the extended mag is a round drum and the extended quick mag is a bigger box with a few more rounds and a faster reload; each tier is set per gun.

**Pistols and SMGs share one attachment family:** a pistol/SMG mag, silencer, or barrel attachment works on any pistol or SMG, since many calibers overlap. Each gun's mag tiers are set per gun; for example, the snail drum is the extended mag for both the MP 18 and the Luger LP08.

**Mag tier review:** every gun's mag tiers will be reviewed later; current numbers are best guesses.

**Tube-fed shotguns:** tube extensions are their own attachment, separate from magazines.

**Duckbill shot diverter:** a shotgun barrel attachment that spreads shot into a flatter, wider pattern, like the one Navy SEALs used on the Ithaca 37 (the SPAS-12 also had a factory shot diverter).

## Grenade launchers

Two kinds, both attachments that spawn as ground loot. A gun takes one only if its page lists one under its unique attachments. Launcher rounds are their own ammo, separate from the gun's.

- **Underbarrel launchers** fill the foregrip slot: 40mm launchers like the M203 and M320 on AR-15-family rifles, the GP-25, GP-30, and GP-34 on Kalashnikovs, the HK79 on the G3, and the [OTs-14 Groza](../weapons/assault-rifles/ots-14-groza.md)'s grip module. A gun with a built-in bipod can't take one, since the bipod already fills that slot ([Built-in parts](#built-in-parts)). They load one round at a time.
- **Rifle grenade launchers** fill the muzzle slot: cups like the [Kar98k](../weapons/snipers/kar98k.md)'s Schiessbecher (up to about 280 m), launchers like the [M1 Garand](../weapons/battle-rifles/m1-garand.md)'s M7, and NATO 22mm grenades that fit straight onto many rifles' flash hiders. Each grenade brings its own launching blank, so there's no extra item. Some guns have one built in, like the [SKS](../weapons/battle-rifles/sks.md) M59/66 and the [MAS-49](../weapons/battle-rifles/mas-49.md).

### Ground rounds: smoke and other non-lethal rounds

| Round | Real example | In game |
| --- | --- | --- |
| Smoke | 40mm ground markers in red, green, and yellow (at least 17 seconds of smoke); Russia's GRD-50, GRD-100, and GRD-200, each a 20 m³ cloud lasting a minute; rifle smoke grenades | A smoke screen at range, like a smoke grenade thrown much farther. Colored smoke also marks a spot for the team |
| Star parachute | M583A1 white, M661 green, M662 red: bursts about 180 m up and lights a circle about 200 m across with 90,000 candlepower for about 40 seconds as it drifts down | Lights an area on [night maps](maps.md); a signal flare by day. Colors work as team signals |
| Star cluster | M585 white, M663 green, M664 red: five stars that burn about 7 seconds | A quick signal, and a brief light at night |
| Infrared star parachute | M992: like the M583A1, but visible only through night vision | Lights an area only for players with a night-vision scope, like the [StG 44](../weapons/assault-rifles/stg-44.md)'s Vampir |
| Propaganda leaflets | Germany's WWII Propaganda-Gewehrgranate: 200 g of leaflets, scattered after about 9 seconds, out to 460 m | A funny round for the Schiessbecher: no damage, just a burst of leaflets |

Left out for now: **CS gas** (the US M651 makes a 120 m² cloud for about 25 seconds) is non-lethal but needs its own gas effect, so it comes later, once gas is in the game (owner, 2026-11-22), and **sponge and rubber-ball rounds** (M1006, M1029) can still kill under 10 m, so they'd count as damage rounds.

### Crate rounds: lethal

Lethal launcher rounds come only from crates, like lethal grenade launchers ([Weapon pool](weapon-pool.md#how-the-randomness-works)). How many a crate holds is TBD. Blast damage is set with the throwables, TBD.

| Round | Real example | In game |
| --- | --- | --- |
| Frag | 40mm M406 HE (kill radius 5 m) and Russia's VOG-25 (lethal radius 6 m); rifle frag grenades like the German Gewehr-Sprenggranate | A frag blast at range. 40mm rounds arm only after 14 m (M406) or 10 m (VOG-25); closer, they're duds that only hit as a solid projectile |
| Bouncing frag | VOG-25P: pops 0.5 to 1.5 m up before it bursts | Reaches players behind low cover or lying prone |
| HEDP | M433: a small shaped charge in a frag sleeve that punches through 50 mm of armor plate; arms after 14 m | Frag plus extra damage to vehicles |
| Anti-tank rifle grenades | Germany's Gewehr-Panzergranate; the US M9A1 (100 mm of armor, 100 m effective); Belgium's ENERGA (200 mm) | Strong against vehicles, with a small blast against players |
| Buckshot | M576: 20 pellets, out to 30 m | A one-shot shotgun blast from the launcher |
| Thermobaric | 40mm M1060, made for bunkers, houses, and masonry | Big damage inside rooms |

Sources: [Wikipedia: United States 40 mm grenades](https://en.wikipedia.org/wiki/United_States_40_mm_grenades) · [Inetres: 40mm low-velocity ammunition](https://inetres.com/gp/military/infantry/grenade/40mm_ammo.html) · [Wikipedia: GP-25](https://en.wikipedia.org/wiki/GP-25) · [Wikipedia: Rifle grenade](https://en.wikipedia.org/wiki/Rifle_grenade) · [Wikipedia: Schiessbecher](https://en.wikipedia.org/wiki/Schiessbecher) · [Lone Sentry: German rifle grenades](https://www.lonesentry.com/articles/ttt/german-rifle-grenades.html) · [Wikipedia: Propaganda-Gewehrgranate](https://en.wikipedia.org/wiki/Propaganda-Gewehrgranate)

Attachment effects: [RankedBoost: PUBG attachments](https://rankedboost.com/playerunknowns-battlegrounds/attachments/) (2017–2018 numbers) · [PUBG Wiki: Mods](https://pubg.wiki.gg/wiki/Mods) (grip effects from Update 12)
