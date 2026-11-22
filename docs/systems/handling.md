# Handling

How fast a gun comes out, aims, reloads, and moves, and how much it spreads and sways. Gun handling should feel as close to PUBG's as we can get (owner, 2026-11-22), so the first pass below uses PUBG's numbers wherever PUBG has them. Our own picks fill only what PUBG's data doesn't cover, such as ADS times and LMG speed, ordered by [Roles by category](ttk.md#roles-by-category). Everything here gets tuned in play testing.

PUBG never published these values. The numbers below come from data-mined community tables, so treat them as close, not exact. Spread and sway are in PUBG's own units, so read them as ratios between guns.

## First pass

Per category. Each version uses its category's numbers until play testing says otherwise; heavier and longer versions may later get slower ADS inside their category.

| Category | Hip spread (PUBG units) | Ready time | ADS time | Sprint speed | Basis |
| --- | --- | --- | --- | --- | --- |
| Pistols / 3rd slot | 3 | 0.5 s | 0.15 s | 6.3 m/s | P1911 spread; PUBG's ready time |
| SMGs | 4.5 | 0.5 s | 0.20 s | 6.15 m/s | Vector, Tommy Gun, and Uzi spread; PUBG's ready time and SMG speed |
| Shotguns | Pellets: 5.5 | 0.5 s | 0.25 s | 5.9 m/s | S1897 pellet spread; PUBG's shotgun speed |
| Assault rifles | 4 (5.56mm and smaller), 6 (7.62×39mm and bigger) | 0.5 s | 0.25 s | 6.0 m/s | M416 and AKM; the M416's ready time (the AKM's is 0.4 s) and PUBG's rifle speed |
| Battle rifles & DMRs | 7 | 0.4 s | 0.30 s | 6.0 m/s | SKS and Mk14; their 0.4 s ready time and PUBG's DMR speed |
| LMGs | 8 | 0.5 s | 0.40 s | 5.85 m/s | M249 spread and ready time (the DP-28's is 0.4 s); slowest ADS and speed, per their role (PUBG doesn't list LMG speed) |
| Snipers | 8 | 0.5 s | 0.35 s | 6.0 m/s | Kar98k; PUBG's sniper speed |

- **Hip spread** is multiplied by stance and movement, like PUBG: crouched 0.5, prone 0.2, walking 2, running 5, jumping 15. ADS spread is tiny on every gun, as in PUBG.
- **Ready time** is the time from pressing the slot key until the gun can fire. PUBG's ready delay was 0.4 s for the AKM, Groza, SKS, Mk14, and DP-28 and 0.5 s for everything else in the table, pistols included.
- **ADS time** isn't in PUBG's data. These are our picks, ordered by the roles: pistols and SMGs fastest, LMGs slowest.
- **Sprint speed** is with that gun in hand, before [armor](armor.md#vests) slowdown. Running, walking, crouching, and crawling scale the same way as PUBG's (table below).
- **Recoil** stays random every shot ([Rules](../rules.md)); each gun's climb, drift, and settle speed come later, gun by gun.

### Reload times

By reload style, the same styles the animations use ([Reload styles](../planning/art-and-sound.md#reload-styles)). "With rounds left" is a reload that tops off; "From empty" also works the bolt or charging handle.

| Reload | With rounds left | From empty | Basis |
| --- | --- | --- | --- |
| `box mag` | 2.2 s | 2.9 s | AKM (M416 2.1 s, SLR 3.7 s from empty) |
| `grip mag` | 1.8 s | 2.1 s | P1911; grip-mag SMGs and machine pistols take the Uzi's 2.5 s and 3.1 s |
| `bullpup mag` | 3.0 s | 3.7 s | AUG and QBZ |
| `side mag` | 2.5 s | 3.1 s | Our pick, like the Uzi |
| `top mag` | 2.8 s | 3.5 s | Our pick, between a box mag and a pan |
| `pan` | 4.5 s | 5.5 s | DP-28 |
| `belt` | 8.2 s | Same | M249's full reload; every belt reload is the full one, rounds left or not (owner, 2026-11-22) |
| `tube` | 0.7 s per shell | Same | S1897 |
| `stripper clip` | 0.75 s per round | 4.0 s for a full clip | Kar98k (its first round takes 1.7 s) |
| `single rounds` | 0.75 s per round | Same | Kar98k's one-round load |
| `en bloc` | Can't top off | 2.5 s | Our pick |
| `break action` | 3.0 s | 3.0 s | S686 |
| `single shot` | — | 3.0 s | Our pick |
| `revolver` | 0.75 s per round | Same | One round at a time (owner, 2026-11-22), like the Kar98k's one-round load. A [speed loader](attachments.md) fills every chamber at once in 3.2 s, PUBG's R45 reload |

PUBG's quickdraw mags and shotgun bullet loops cut reload time by 30%, a starting point for the quick mag tiers ([Attachments](attachments.md)).

### Staged reloads

A reload keeps its progress (owner, 2026-11-22). Each reload is split into stages, and a cancelled reload saves the last stage it finished, on the gun itself. The next reload picks up from there instead of starting over. If the old mag is already out, the gun stays without a mag until you finish. First pass (our pick):

| Reload style | Stages, with each one's share of the reload time | Can it fire between stages? |
| --- | --- | --- |
| `box mag`, `grip mag`, `bullpup mag`, `side mag`, `top mag`, `pan` | Old mag out (40%), new mag in (60%). From empty: old mag out (30%), new mag in (45%), bolt or charging handle (25%) | With the mag out, only a round already in the chamber fires. Open-bolt guns have none, so they can't |
| `belt` | Always the full reload (owner, 2026-11-22): cover up and old belt out (40%), new belt in and cover down (45%), charging the gun (15%), with rounds left or not | No, while the cover is up |
| `tube`, `single rounds` | Each round is its own stage, as now | Yes; pressing fire already stops the reload |
| `stripper clip` | A full clip from empty is one stage; topping off is one round at a time | Yes, between rounds |
| `en bloc` | Partial clip out (35%), new clip in (65%). It can't be topped off ([Rules](../rules.md#en-bloc-clips)) | No, with the clip out |
| `break action`, `single shot` | Open and empties out (35%), new rounds in (45%), closed (20%) | No, while it's open |
| `revolver` | One round at a time (owner, 2026-11-22): cylinder out or loading gate open, with the empties out; then each round is its own stage; then closed. With a [speed loader](attachments.md): cylinder out and empties out (35%), every round in at once (50%), closed (15%) | No, while the cylinder is out or the gate is open |

- **Mags and belts (owner, 2026-11-22):** a mag-fed gun does the full reload only when its chamber is empty; otherwise it just changes mags. A belt-fed gun always does the full reload.
- **Where pulled rounds go:** like PUBG, back to the backpack as loose rounds when the old mag or belt comes out, since mags aren't items ([Ammo](ammo.md#how-ammo-and-reloading-work)).
- **The old mag drops (owner, 2026-11-22):** the empty or partial mag falls to the ground and disappears after about 10 seconds. It's only for looks, so other players see the reload; you can't pick it up. Spent casings also stay on the ground about 10 seconds.
- **What cancels a reload:** switching weapons, sprinting, holding X for melee or tapping it for a quick hit, getting knocked, vaulting or climbing, getting in a vehicle, starting a heal, and dropping the gun. Pressing fire only stops one-at-a-time loads ([Reloads work like PUBG](#reload-times)).
- **The saved stage stays with the gun:** a gun dropped with its mag out lies on the ground with no mag, and whoever picks it up starts from "new mag in."
- **The HUD** shows a gun with no mag as the chambered round only, like 0+1.

## PUBG's numbers

### Spread, sway, and delays

From the community table on the PUBG fandom wiki, from PUBG's early release.

| Gun | Class | Hip spread | Aim | ADS | Bloom per shot | Sway (pitch, yaw) | Pickup delay | Ready delay |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| P92 | Pistol | 2.5 | 0.20 | 0.05 | 10 | 2, 15 | 150 ms | 500 ms |
| P1911 | Pistol | 3 | 0.20 | 0.05 | 10 | 2, 15 | 150 ms | 500 ms |
| R1895 | Pistol | 3.5 | 0.20 | 0.05 | 20 | 2, 15 | 150 ms | 500 ms |
| Micro Uzi | SMG | 4.5 | 0.10 | 0.04 | 17 | 1, 1 | 150 ms | 500 ms |
| Vector | SMG | 4.5 | 0.14 | 0.05 | 10 | 1, 1 | 150 ms | 500 ms |
| Tommy Gun | SMG | 4.5 | 0.14 | 0.05 | 10 | 1, 1 | 150 ms | 500 ms |
| UMP45 | SMG | 5.5 | 0.20 | 0.05 | 20 | 2, 10 | 150 ms | 500 ms |
| S686 | Shotgun | 5 | 0.10 | 0.75 | 0 | 1, 1 | 150 ms | 500 ms |
| S1897 | Shotgun | 5.5 | 0.05 | 0.25 | 0 | 1, 1 | 150 ms | 500 ms |
| S12K | Shotgun | 6 | 0.05 | 0.03 | 0 | 1, 1 | 150 ms | 500 ms |
| M416 | AR | 4 | 0.14 | 0.02 | 8.5 | 1, 1 | 150 ms | 500 ms |
| SCAR-L | AR | 4 | 0.13 | 0.02 | 9 | 1, 1 | 150 ms | 500 ms |
| M16A4 | AR | 5 | 0.15 | 0.02 | 8.5 | 1, 1 | 150 ms | 500 ms |
| AKM | AR | 6 | 0.15 | 0.025 | 9 | 1, 1 | 150 ms | 400 ms |
| Groza | AR | 6 | 0.15 | 0.025 | 9 | 1, 1 | 150 ms | 400 ms |
| Mini 14 | DMR | 5 | 0.15 | 0.02 | 8.5 | 1, 1 | 150 ms | 500 ms |
| SKS | DMR | 7 | 0.15 | 0.01 | 9 | 1, 1 | 150 ms | 400 ms |
| Mk14 EBR | DMR | 7 | 0.15 | 0.01 | 9 | 1, 1 | 150 ms | 400 ms |
| DP-28 | LMG | 6 | 0.15 | 0.025 | 9 | 1, 1 | 150 ms | 400 ms |
| M249 | LMG | 8 | 0.15 | 0.05 | 10 | 1, 10 | 150 ms | 500 ms |
| Kar98k | Sniper | 8 | 0.10 | 0.007 | 13.5 | 1, 1 | 150 ms | 500 ms |
| AWM | Sniper | 7.5 | 0.40 | 0.004 | 12.5 | 1, 1 | 150 ms | 500 ms |

- **Aim and ADS** multiply the hip spread: holding aim (PUBG's third-person over-the-shoulder aim) and aiming down sights. An M416's ADS spread is 4 × 0.02.
- **Stance and movement** multiply it again: crouched 0.5, prone 0.2, walking 2, running 5, jumping 15. Sway is cut the same way crouched (0.5) and prone (0.2), and moving raises it by 1.5 (the M249's by 2).
- **Pickup delay** was 150 ms in this table and 200 to 250 ms in later data.

### Reloads

From pubgmap.io's data (PUBG version 5.0, 2019). "Tactical" is with rounds left; "empty" includes working the bolt.

| Gun | Class | Tactical | Empty |
| --- | --- | --- | --- |
| P92, P18C | Pistol | 1.7 s | 2.0 s |
| P1911 | Pistol | 1.8 s | 2.1 s |
| R45 | Pistol | 3.2 s | 3.2 s |
| R1895 | Pistol | 0.75 s per round | — |
| Vector | SMG | 2.1 s | 2.2 s |
| Micro Uzi | SMG | 2.5 s | 3.1 s |
| UMP | SMG | 2.55 s | 3.1 s |
| Tommy Gun | SMG | 2.85 s | 3.45 s |
| S1897 | Shotgun | 0.715 s per shell | — |
| S686 | Shotgun | 3.0 s | 3.0 s |
| S12K | Shotgun | 2.4 s | 3.0 s |
| M416, SCAR-L | AR | 1.9 s | 2.1 s, 2.2 s |
| M16A4 | AR | 1.9 s | 2.2 s |
| AKM, Beryl | AR | 2.25 s | 2.9 s |
| Groza | AR | 2.25 s | 3.0 s |
| AUG, QBZ | AR | 3.0 s | 3.67 s |
| Mini 14 | DMR | 2.7 s | 3.6 s |
| SKS | DMR | 2.35 s | 2.9 s |
| SLR, Mk14 EBR | DMR | 2.78 s | 3.68 s |
| DP-28 | LMG | 4.5 s | 5.5 s |
| M249 | LMG | 7.1 s | 8.2 s |
| M24 | Sniper | 1.8 s | 4.2 s |
| AWM | Sniper | 2.3 s | 4.6 s |
| Kar98k | Sniper | 0.75 s per round (1.69 s for the first) | 4.0 s for a full clip |

### Movement

PUBG's speeds by stance, and by what's in your hands while sprinting.

| Stance | Speed |
| --- | --- |
| Sprint | 6.3 m/s |
| Crouched sprint | 4.8 m/s |
| Run | 4.7 m/s |
| Crouched run | 3.4 m/s |
| Walk | 1.7 m/s |
| Crouched walk | 1.3 m/s |
| Crawl | 1.2 m/s |
| Swim | 2.9 m/s |

| In hand | Speed |
| --- | --- |
| Pistol | 6.32 m/s |
| Unarmed or melee | 6.3 m/s |
| SMG | 6.15 m/s |
| Rifle | 6.01 m/s |
| Sniper or DMR | 5.99 m/s |
| Shotgun | 5.91 m/s |

Sources: [PUBG fandom wiki: Weapon stats](https://pubg.fandom.com/wiki/Weapon_Stats_for_PLAYERUNKNOWN%27s_BATTLEGROUNDS) · [PUBG Map: Rifles](https://pubgmap.io/weapons/rifles.html) · [PUBG Map: SMGs](https://pubgmap.io/weapons/smg.html) · [PUBG Map: DMRs](https://pubgmap.io/weapons/dmr.html) · [PUBG Map: Sniper rifles](https://pubgmap.io/weapons/sniper.html) · [PUBG Map: Pistols](https://pubgmap.io/weapons/pistols.html) · [PUBG Map: Shotguns](https://pubgmap.io/weapons/shotguns.html) · [PUBG Map: LMGs](https://pubgmap.io/weapons/lmg.html) · [PUBG Wiki: Kar98k](https://pubg.wiki.gg/wiki/Kar98K) · [PUBG Wiki: M249](https://pubg.wiki.gg/wiki/M249) · [PUBG Wiki: Movement speed](https://pubg.wiki.gg/wiki/Movement_Speed) · [Samurai Gamers: PUBG shotguns](https://samurai-gamers.com/playerunknowns-battlegrounds-pubg/shotgun-stats-guide/)
