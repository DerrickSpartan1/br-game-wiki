# Healing

Healing works like PUBG's: three healing items, three boosts, and the boost bar. PUBG's six items are six roles, and Escape from Tarkov's meds, drinks, and stimulants fill them as variants. Every match rolls one item per role. Numbers marked "our pick" are first passes to tune in play testing.

## Health

- **100 health,** like PUBG. Zone damage is a percent of that ([The zone](match-flow.md#the-zone)).
- **Two caps:** bandages and first aid kits only heal up to 75. Only the med kit and the boost bar take you past 75 to 100.

## The items

PUBG's six items set the six roles. The real items that fill each role are under [Variants](#variants).

| Item | Use time | Effect | Weight |
| --- | --- | --- | --- |
| **Bandage** | 4 s | Heals 10 over 3 s, up to 75 | TBD |
| **First aid kit** | 6 s | Heals to 75 at once; can't be used at 75 or more | TBD |
| **Med kit** | 8 s | Heals to 100 at once | 20 |
| **Energy drink** | 4 s | Boost +40 | TBD |
| **Painkillers** | 7.5 s | Boost +60 | TBD |
| **Adrenaline syringe** | 6 s | Boost +100, a full bar | 20 |

- **Weights** use PUBG's, like ammo and throwables ([Carry weight](armor.md#carry-weight)). PUBG's weights for the bandage, first aid kit, energy drink, and painkillers aren't confirmed yet.
- **Adrenaline** also speeds up picking up a knocked teammate ([Knockdowns and revives](gameplay.md#knockdowns-revives)). You don't need it in your hands to use it.
- **Where they spawn:** bandages, first aid kits, energy drinks, and painkillers on the ground; med kits rare on the ground; adrenaline syringes mostly in care packages and rarely on the ground, like PUBG since its Update 12. Vaults hold meds too ([Vaults and keys](match-flow.md#vaults-and-keys)).
- **PUBG's times changed:** some guides list slower times (first aid kit 7 s, med kit 10 s, adrenaline 10 s). The adrenaline syringe went from 8 s to 6 s in PUBG's Update 12.

## Boost bar

PUBG's boost bar, as is. Boosts fill a bar of 100 points that drains over time. While it has points, you heal a little every 8 seconds, and the top of the bar makes you run faster.

| Part of the bar | Points | Heals every 8 s | Run speed | Time in this part |
| --- | --- | --- | --- | --- |
| 1 | 1 to 20 | 1 | Normal | 60 s |
| 2 | 21 to 60 | 2 | Normal | 120 s |
| 3 | 61 to 90 | 3 | +2.5% | 90 s |
| 4 | 91 to 100 | 4 | +6.2% | 30 s |

- **Draining:** the times per part work out to one point every 3 seconds, so a full bar lasts 5 minutes. The point ranges come from that.
- **What each boost gives:** an energy drink works out to about 23 health over 2 minutes, painkillers about 38 over 3 minutes, and an adrenaline syringe about 86 over 5 minutes.
- **Stacking:** boosts add up, to a cap of 100.

## Variants

Each of PUBG's six items is a role, and Tarkov's items fill those roles, loosely. A role has as many variants as fit it, from two to nine. Where Tarkov has too few, PUBG's own item stays in the roll.

### How the blend works

- **Role:** PUBG's item sets what a variant does. Bandages heal a little over time up to 75, first aid kits heal up to 75 at once, med kits heal to 100, and the other three add boost.
- **Loose fit:** each item goes in the role that plays closest to it, even where real life differs. Tarkov's drinks are energy drinks, its stimulants are adrenaline, and its antibiotic is a painkiller.
- **Use time:** Tarkov's use time, doubled. That lands on PUBG's own times: Tarkov's 2-second bandages become 4 s like PUBG's bandage, and its 3-second medkits become 6 s like PUBG's first aid kit.
- **Strength:** comes from how the item ranks in Tarkov, kept near PUBG's numbers: health per use for kits, what a bandage stops, how long a painkiller or stimulant lasts, and how much a drink restores.
- **Uses:** one, like PUBG, or two when the Tarkov item has several uses or a health pool of 300 or more. Two-use items weigh 1.5 times as much; everything else weighs what its role does.
- **Health stays simple:** no bleeding, fractures, or lost limbs, so Tarkov's treatments only show up as strength.

Every number below is a first pass (our pick). Tarkov's numbers are from Tarkov Forge and change between patches.

### Bandages

PUBG's bandage heals 10 over 3 s, up to 75. Items that stop heavy bleeding in Tarkov heal 15.

| Item | Tarkov | Ours | Uses |
| --- | --- | --- | --- |
| **Aseptic bandage** | 2 s, light bleeding | 4 s, heals 10 | 1 |
| **Army bandage** | 2 s, light bleeding, 2 uses | 4 s, heals 10 | 2 |
| **CAT tourniquet** | 3 s, heavy bleeding | 6 s, heals 15 | 1 |
| **Esmarch tourniquet** | 5 s, heavy bleeding | 10 s, heals 15 | 1 |
| **Celox applicator** | 3 s, heavy bleeding, 3 uses | 6 s, heals 15 | 2 |

Tarkov calls the Celox applicator the CALOK-B, a parody of the real Celox-A.

### First aid kits

PUBG's first aid kit heals to 75 at once. Kits that heal 70 or more per use in Tarkov do the same. Kits that heal 50 per use heal 50, still only up to 75.

| Item | Tarkov | Ours | Uses |
| --- | --- | --- | --- |
| **AI-2** | 2 s, 50 per use, pool of 100 | 4 s, heals 50 | 1 |
| **Car first aid kit** | 3 s, 70 per use, pool of 220 | 6 s, heals to 75 | 1 |
| **IFAK** | 3 s, 50 per use, pool of 300 | 6 s, heals 50 | 2 |
| **Salewa first aid kit** | 3 s, 85 per use, pool of 400 | 6 s, heals to 75 | 2 |

### Med kits

PUBG's med kit heals to 100 at once. Tarkov has only one real kit this big, so PUBG's med kit stays in the roll.

| Item | Tarkov | Ours | Uses |
| --- | --- | --- | --- |
| **Med kit** | PUBG's | 8 s, heals to 100 | 1 |
| **Grizzly medical kit** | 5 s, 175 per use, pool of 1,800 | 10 s, heals to 100 | 2 |

The Grizzly is based on Adventure Medical Kits' Sportsman Series Grizzly.

### Energy drinks

PUBG's energy drink gives boost +40. Tarkov's drinks restore hydration and energy; here the boost is 20 plus a third of the two added together, rounded to 5. Every drink takes 4 s, like PUBG's. Tarkov's brands are its own parodies, so ours use plain names: cola, not TarCola.

| Item | Tarkov | Ours | Uses |
| --- | --- | --- | --- |
| **Energy drink** | PUBG's | 4 s, boost +40 | 1 |
| **Energy drink can** | Max Energy and Hot Rod: hydration 20, energy 10 to 12 | 4 s, boost +30 | 1 |
| **Cola** | TarCola: hydration 15, energy 5 | 4 s, boost +25 | 1 |
| **Iced green tea** | Hydration 15 | 4 s, boost +25 | 1 |
| **Milk** | Hydration 30, energy 20 | 4 s, boost +35 | 1 |
| **Juice pack** | Grand, Vita, and apple juice: hydration 25 to 30, energy 5 to 8, many sips | 4 s, boost +30 | 2 |
| **Water bottle** | Hydration 60, many sips | 4 s, boost +40 | 2 |
| **Kvass** | Hydration 65, energy 15, many sips | 4 s, boost +45 | 2 |
| **Mineral water** | Aquamari: hydration 100, energy 20, many sips | 4 s, boost +60 | 2 |

### Painkillers

PUBG's painkillers give boost +60. Here the boost comes from how long the item kills pain in Tarkov, with Tarkov's morphine (300 s) matching PUBG's +60, rounded to 5.

| Item | Tarkov | Ours | Uses |
| --- | --- | --- | --- |
| **Analgin** | 3 s, 80 s of pain relief, 4 uses | 6 s, boost +15 | 2 |
| **Ibuprofen** | 5 s, 280 s, 8 uses | 10 s, boost +55 | 2 |
| **Vaseline balm** | 6 s, 300 s, 3 uses | 12 s, boost +60 | 2 |
| **Golden Star balm** | 7 s, 350 s, 5 uses | 14 s, boost +70 | 2 |
| **Morphine injector** | 2 s, 300 s, 1 use | 4 s, boost +60 | 1 |
| **Augmentin** | 5 s, 150 s, 1 use | 10 s, boost +30 | 1 |

Augmentin is an antibiotic, but Tarkov treats it as pain relief, so it's a painkiller here too.

### Adrenaline

PUBG's adrenaline syringe fills the boost bar, and Tarkov's stimulants join it here. Every Tarkov stimulant takes 2 s, so 4 s here. Ones whose effects last 120 s or more in Tarkov fill the bar; 60-second ones give +80. Everything in this role also speeds up picking up a teammate.

| Item | Tarkov | Ours | Uses |
| --- | --- | --- | --- |
| **Adrenaline syringe** | PUBG's | 6 s, boost +100 | 1 |
| **Adrenaline injector** | 60 s: endurance and strength, kills pain | 4 s, boost +80 | 1 |
| **Perfotoran** | 60 s: stops bleeding, antidote | 4 s, boost +80 | 1 |
| **L1 (norepinephrine)** | 120 s: strength, endurance, and stamina, kills pain | 4 s, boost +100 | 1 |
| **Tramadol** | 180 s: endurance, strength, and focus, kills pain | 4 s, boost +100 | 1 |
| **Meldonin** | 900 s: endurance, strength, and stamina | 4 s, boost +100 | 1 |

Tarkov calls its tramadol Trimadol. Perfotoran could also cut gas damage for a while, as an antidote (idea, [Red zones](match-flow.md#red-zones)).

### The roll

- **One item per role per match:** the match rolls each role's item during the lobby countdown, along with the gun pool ([Pre-match lobby](match-flow.md#pre-match-lobby)). Everyone finds the same bandage, the same first aid kit, and so on, so nobody carries five kinds of med kit.
- **Rolled separately:** each role rolls on its own, so one match might have Esmarch tourniquets and a Grizzly.
- **Odds:** equal within a role for now (our pick).
- **Fair inside a match:** everyone is on the same items; what changes is from one match to the next, like gun versions ([Rules](../rules.md#versions)).
- **Named on pickup:** the pickup prompt and the inventory name the item, like a gun's version ([HUD and inventory](gameplay.md#hud-and-inventory)).

### Left out of Tarkov's list

- **AFAK:** its real-life basis isn't confirmed.
- **Splints and surgical kits** (aluminum and immobilizing splints, Tigzresq, CMS, Surv12): there are no fractures or lost limbs here.
- **Made-up stimulants** (Propital, eTG-change, the SJ series, Zagustin, and others): Tarkov's own inventions, so they'd need our own names. Not in yet.
- **Alcohol** (beer, vodka, whiskey, moonshine) and Tarkov's rarer branded waters: left out.
- **Portable defibrillator:** Tarkov's is a parody of the Philips HeartStart FRx. Ours is a [class item](class-items.md) and could be based on it.

## Sources

- [Samurai Gamers: PUBG consumable items](https://samurai-gamers.com/playerunknowns-battlegrounds-pubg/consumable-items-list-3/) · [Samurai Gamers: PUBG boost system](https://samurai-gamers.com/playerunknowns-battlegrounds-pubg/boost-system/)
- [Appuals: PUBG healing and boost items guide](https://appuals.com/playerunknowns-battlegrounds-healing-boost-items-guide/) · [Gamepressure: PUBG healing and boosting](https://www.gamepressure.com/playerunknowns-battlegrounds/healing-and-boosting-your-character/zea139) · [Gamepressure: PUBG consumables](https://gamepressure.com/playerunknowns-battlegrounds/items-consumables-healing/z3a93f)
- [PUBG Wiki: Adrenaline Syringe](https://pubg.wiki.gg/wiki/Adrenaline_Syringe) · [PUBG Wiki: Med Kit](https://pubg.wiki.gg/wiki/Med_Kit)
- [Tarkov Forge: medical items](https://tarkovforge.com/meds) and [food and drink](https://tarkovforge.com/provisions) (Tarkov's numbers) · [Escape from Tarkov Wiki: Medical](https://escapefromtarkov.fandom.com/wiki/Medical)
- [Escape from Tarkov Wiki: Easter eggs and references](https://escapefromtarkov.fandom.com/wiki/Easter_eggs_and_References) (CALOK-B, Grizzly, Augmentin, Vaseline balm, and defibrillator parodies) · [Escape from Tarkov Wiki: Grizzly medical kit](https://escapefromtarkov.fandom.com/wiki/Grizzly_medical_kit)
