# Healing

Healing works like PUBG's: three healing items, three boosts, and the boost bar. PUBG's six items are six slots, and Escape from Tarkov's meds, drinks, and stimulants fill them, each a little better or a little worse than PUBG's numbers. Every match rolls one item per slot. Numbers marked "our pick" are first passes to tune in play testing.

## Health

- **100 health,** like PUBG. Zone damage is a percent of that ([The zone](match-flow.md#the-zone)).
- **Heal to 80, boost the rest:** bandages and first aid kits only heal up to 80 (PUBG's cap is 75). Past that, you boost the rest with energy drinks, painkillers, or adrenaline.
- **Med kits get you to full,** but they're rare and take up more room in the backpack (20, PUBG's weight), like PUBG's.
- **Healing is slow:** once an item is used, its health fills into the bar a little at a time instead of jumping, like PUBG's bandage. Bandages fill over 3 s (PUBG's), first aid kits over 3 s, and med kits over 5 s (our pick). Boosts heal slowly over minutes ([Boost bar](#boost-bar)).

## The items

PUBG's six items are the six slots. Their numbers are the middle that every item in the slot is compared with. PUBG's items themselves aren't in the game; the items that fill each slot are under [Variants](#variants).

| Slot | Use time | Effect | Weight |
| --- | --- | --- | --- |
| **Bandage** | 4 s | Heals 10 over 3 s, up to 80 | 2 |
| **First aid kit** | 6 s | Heals to 80, filling over 3 s; can't be used at 80 or more | 10 |
| **Med kit** | 8 s | Heals to 100, filling over 5 s | 20 |
| **Energy drink** | 4 s | Boost +40 | 4 |
| **Painkillers** | 7.5 s | Boost +60 | 10 |
| **Adrenaline** | 6 s | Boost +100, a full bar | 20 |

- **Weights** use PUBG's, like ammo and throwables, and every item weighs what its slot does ([Carry weight](armor.md#carry-weight)). The lead's placeholders for the bandage, first aid kit, energy drink, and painkillers (2, 10, 4, 10) are kept (owner, 2026-11-22).
- **Adrenaline slot:** everything in it also speeds up picking up a knocked teammate ([Knockdowns and revives](gameplay.md#knockdowns-revives)). You don't need it in your hands to use it.
- **Where they spawn:** bandages, first aid kits, energy drinks, and painkillers on the ground; med kits rare on the ground; adrenaline mostly in care packages and rarely on the ground, like PUBG since its Update 12. Vaults hold meds too ([Vaults and keys](match-flow.md#vaults-and-keys)).
- **PUBG's times changed:** some guides list slower times (first aid kit 7 s, med kit 10 s, adrenaline 10 s). PUBG's adrenaline syringe went from 8 s to 6 s in its Update 12.

## Rules

Settled by the owner on 2026-11-22, from the lead's placeholders and the planner's questions.

- **Ground spawns:** of every ground med spawn, bandages 30%, first aid kits 24%, energy drinks 22%, painkillers 16%, med kits 5%, and adrenaline-slot items 3%. Bandages come in stacks of 5.
- **Care packages:** 1 adrenaline-slot item each, plus a chance of a med kit.
- **Vaults:** 2 first aid kits, 1 med kit, and 1 adrenaline-slot item ([Vaults and keys](match-flow.md#vaults-and-keys)).
- **Getting knocked** empties the boost bar and stops any healing that's filling in.
- **At the cap:** a heal item can't be used at its cap, even if it also boosts.
- **Quick teammate pickup:** using an adrenaline-slot item for it uses the item up, and the teammate gets its boost.
- **The pocket first aid kit** heals 70, still capped at 80.
- **What cancels using a med:** firing, getting knocked, the parachute, vaulting, reloading, aiming, switching weapons, and jumping, as in PUBG.
- **Moving while using a med:** a slow walk, like PUBG.
- **Boost speed** counts only when running.
- **Item names (owner, 2026-11-23):** every med shows its slot first, then its own name, like "Med kit: Large medical bag", on pickup prompts and in the inventory.
- **Gas and fire:** gas damage doesn't stop a boost's healing; burning does, while you burn. The blood substitute injector only does what its slot does; it doesn't cut gas damage.

## Boost bar

PUBG's boost bar, as is. Boosts fill a bar of 100 points that drains over time. While it has points, you heal a little every 8 seconds, and the top of the bar makes you run faster.

| Part of the bar | Points | Heals every 8 s | Run speed | Time in this part |
| --- | --- | --- | --- | --- |
| 1 | 1 to 20 | 1 | Normal | 60 s |
| 2 | 21 to 60 | 2 | Normal | 120 s |
| 3 | 61 to 90 | 3 | +2.5% | 90 s |
| 4 | 91 to 100 | 4 | +6.2% | 30 s |

- **Draining:** the times per part work out to one point every 3 seconds, so a full bar lasts 5 minutes. The point ranges come from that.
- **What each boost gives:** at PUBG's numbers, an energy drink works out to about 23 health over 2 minutes, painkillers about 38 over 3 minutes, and an adrenaline syringe about 86 over 5 minutes.
- **Stacking:** boosts add up, to a cap of 100.
- **Checked against PUBG (2026-11-23):** the numbers above are PUBG's, from 2017 guides, and the game's code matches them. One energy drink puts you in part 2, so its first heal is 2 health, 8 s after you drink, then 2 more every 8 s. That's slow to notice, in PUBG too. The fourth part heals the most and runs the fastest, but it's the shortest, at 30 s.
- **Showing the heal (our pick):** the health bar pulses briefly each time a boost heal lands, so it's easy to see the boost working.

## Variants

Each slot holds Tarkov's items, loosely, from three to eight per slot. They stay close to PUBG's middle: some are a little better, some a little worse, and some trade speed for strength. This is real gameplay, not skins: the small differences are what change from match to match.

### How it works

- **Close to the middle:** every item is within about 1 s and 10% of its slot's PUBG numbers. A few slower kits also add a small boost.
- **Caps hold:** every bandage and first aid kit stops at 80, and every med kit heals to 100.
- **Ranked by Tarkov:** Tarkov's better items land on the better side: more health per use, stopping heavy bleeding, lasting longer, or restoring more.
- **Loose fit:** each item goes in the slot that plays closest to it, even where real life differs. Tarkov's drinks are energy drinks, its stimulants and injectors are adrenaline, and its antibiotic is a painkiller.
- **One use each,** like PUBG.
- **Generic names:** items use plain names, never brands or product names. The Tarkov column keeps Tarkov's names for reference only ([Legal review](../planning/legal-review.md)).
- **Health stays simple:** no bleeding, fractures, or lost limbs, so Tarkov's treatments only show up as small differences in strength.

Every number below is a first pass (our pick). Tarkov's numbers are from Tarkov Forge and change between patches.

### Bandages

Middle: 4 s, heals 10 over 3 s, up to 80.

| Item | Tarkov | Ours | Compared with the middle |
| --- | --- | --- | --- |
| **Aseptic bandage** | 2 s, light bleeding | 3.5 s, heals 9 | Faster, a bit less |
| **Army bandage** | 2 s, light bleeding, 2 uses | 4 s, heals 10 | The middle |
| **Hemostatic applicator** | CALOK-B: 3 s, heavy bleeding, 3 uses | 4 s, heals 11 | A little better |
| **Windlass tourniquet** | CAT: 3 s, heavy bleeding | 4.5 s, heals 11 | Slower, a bit more |
| **Rubber tourniquet** | Esmarch: 5 s, heavy bleeding | 5 s, heals 10 | A little worse |

### First aid kits

Middle: 6 s, heals to 80, filling over 3 s.

| Item | Tarkov | Ours | Compared with the middle |
| --- | --- | --- | --- |
| **Pocket first aid kit** | AI-2: 2 s, 50 per use, pool of 100 | 5 s, heals up to 70, still stopping at 80 | Faster, a bit less |
| **Car first aid kit** | 3 s, 70 per use, pool of 220 | 6 s, heals to 80 | The middle |
| **Individual first aid kit** | IFAK: 3 s, 50 per use, pool of 300, stops heavy bleeding | 7 s, heals to 80, boost +10 | Slower, a bit more |

### Med kits

Middle: 8 s, heals to 100, filling over 5 s. Every med kit gets you to full; they differ in speed.

| Item | Tarkov | Ours | Compared with the middle |
| --- | --- | --- | --- |
| **Tactical trauma kit** | AFAK: 3 s, 60 per use, pool of 400 | 8 s, heals to 100 | The middle |
| **Hiking first aid kit** | Salewa: 3 s, 85 per use, pool of 400 | 7.5 s, heals to 100 | A little better |
| **Large medical bag** | Grizzly: 5 s, 175 per use, pool of 1,800 | 9 s, heals to 100, boost +20 | Slower, a bit more |

### Energy drinks

Middle: 4 s, boost +40. Tarkov's drinks restore hydration and energy; the ones that restore more land higher. Tarkov's brands are its own parodies, so ours use plain names: cola, not TarCola.

| Item | Tarkov | Ours | Compared with the middle |
| --- | --- | --- | --- |
| **Iced green tea** | Hydration 15 | 3.5 s, boost +35 | Faster, a bit less |
| **Cola** | TarCola: hydration 15, energy 5 | 4 s, boost +35 | A little worse |
| **Energy drink can** | Max Energy and Hot Rod: hydration 20, energy 10 to 12 | 4 s, boost +40 | The middle |
| **Juice pack** | Grand, Vita, and apple juice: hydration 25 to 30, energy 5 to 8 | 4 s, boost +40 | The middle |
| **Milk** | Hydration 30, energy 20 | 4 s, boost +45 | A little better |
| **Water bottle** | Hydration 60 | 4.5 s, boost +45 | Slower, a bit more |
| **Kvass** | Hydration 65, energy 15 | 4.5 s, boost +45 | Slower, a bit more |
| **Mineral water** | Aquamari: hydration 100, energy 20 | 4 s, boost +45 | A little better |

### Painkillers

Middle: 7.5 s, boost +60. Ones that kill pain longer in Tarkov land higher.

| Item | Tarkov | Ours | Compared with the middle |
| --- | --- | --- | --- |
| **Metamizole pills** | Analgin: 3 s, 80 s of pain relief | 6.5 s, boost +55 | Faster, a bit less |
| **Antibiotic pills** | Augmentin: 5 s, 150 s | 7.5 s, boost +55 | A little worse |
| **Ibuprofen pills** | Ibuprofen: 5 s, 280 s | 7 s, boost +60 | A little better |
| **Warming balm** | Vaseline balm: 6 s, 300 s | 8 s, boost +60 | A little worse |
| **Menthol balm** | Golden Star balm: 7 s, 350 s | 8 s, boost +65 | Slower, a bit more |

Antibiotics don't kill pain in real life, but Tarkov's Augmentin works as pain relief, so they're a painkiller here too.

### Adrenaline

Middle: 6 s, boost +100. Tarkov's real stimulants and injectors go here, including morphine. Its made-up stimulants don't. Ones whose effects last longer in Tarkov land higher.

| Item | Tarkov | Ours | Compared with the middle |
| --- | --- | --- | --- |
| **Adrenaline injector** | Adrenaline, 60 s: endurance and strength, kills pain | 5.5 s, boost +95 | Faster, a bit less |
| **Blood substitute injector** | Perfotoran, 60 s: stops bleeding, antidote | 6 s, boost +90 | A little worse |
| **Norepinephrine injector** | L1, 120 s: strength, endurance, and stamina, kills pain | 5.5 s, boost +100 | A little better |
| **Tramadol injector** | Trimadol, 180 s: endurance, strength, and focus, kills pain | 6 s, boost +100 | The middle |
| **Morphine injector** | Morphine, 300 s of pain relief | 6 s, boost +100 | The middle |
| **Meldonium injector** | Meldonin, 900 s: endurance, strength, and stamina | 6.5 s, boost +100 | A little worse |

The blood substitute injector could also cut gas damage for a while, as an antidote (idea, [Red zones](match-flow.md#red-zones)).

### The roll

- **One item per slot per match:** the match rolls each slot's item during the lobby countdown, along with the gun pool ([Pre-match lobby](match-flow.md#pre-match-lobby)). Everyone finds the same bandage, the same first aid kit, and so on, so nobody carries five kinds of med kit.
- **Rolled separately:** each slot rolls on its own, so one match might have rubber tourniquets and a large medical bag.
- **Odds:** equal within a slot for now (our pick).
- **Fair inside a match:** everyone is on the same items; what changes is from one match to the next, like gun versions ([Rules](../rules.md#versions)).
- **Named on pickup:** the pickup prompt and the inventory name the item and its use time, like a gun's version ([HUD and inventory](gameplay.md#hud-and-inventory)).

### Left out of Tarkov's list

- **Splints and surgical kits** (aluminum and immobilizing splints, Tigzresq, CMS, Surv12): there are no fractures or lost limbs here.
- **Made-up stimulants** (Propital, eTG-change, the SJ series, Zagustin, and others): not used. Only real drugs go in.
- **Alcohol** (beer, vodka, whiskey, moonshine) and Tarkov's rarer branded waters: left out.
- **Portable defibrillator:** Tarkov's is a parody of a real brand's defibrillator. Ours is a [class item](class-items.md) with a generic name and look.

## Sources

- [Samurai Gamers: PUBG consumable items](https://samurai-gamers.com/playerunknowns-battlegrounds-pubg/consumable-items-list-3/) · [Samurai Gamers: PUBG boost system](https://samurai-gamers.com/playerunknowns-battlegrounds-pubg/boost-system/)
- [Appuals: PUBG healing and boost items guide](https://appuals.com/playerunknowns-battlegrounds-healing-boost-items-guide/) · [Gamepressure: PUBG healing and boosting](https://www.gamepressure.com/playerunknowns-battlegrounds/healing-and-boosting-your-character/zea139) · [Gamepressure: PUBG consumables](https://gamepressure.com/playerunknowns-battlegrounds/items-consumables-healing/z3a93f)
- [PUBG Wiki: Adrenaline Syringe](https://pubg.wiki.gg/wiki/Adrenaline_Syringe) · [PUBG Wiki: Med Kit](https://pubg.wiki.gg/wiki/Med_Kit)
- [Tarkov Forge: medical items](https://tarkovforge.com/meds) and [food and drink](https://tarkovforge.com/provisions) (Tarkov's numbers) · [Escape from Tarkov Wiki: Medical](https://escapefromtarkov.fandom.com/wiki/Medical)
- [Escape from Tarkov Wiki: Easter eggs and references](https://escapefromtarkov.fandom.com/wiki/Easter_eggs_and_References) (CALOK-B, Grizzly, Augmentin, Vaseline balm, and defibrillator parodies) · [Escape from Tarkov Wiki: Grizzly medical kit](https://escapefromtarkov.fandom.com/wiki/Grizzly_medical_kit)
