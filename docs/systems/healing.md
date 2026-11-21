# Healing

Healing works like PUBG's: three healing items, three boosts, and the boost bar. On top of that, each item comes in better and worse variants, like Escape from Tarkov's range of medkits, and every match rolls one variant of each item. Numbers marked "our pick" are first passes to tune in play testing.

## Health

- **100 health,** like PUBG. Zone damage is a percent of that ([The zone](match-flow.md#the-zone)).
- **Two caps:** bandages and first aid kits only heal up to 75. Only the med kit and the boost bar take you past 75 to 100.

## The items

PUBG's six items are the standard variant of each:

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

Every item type has three variants: a worse one, PUBG's standard one, and a better one. Names are working names, taken from real kit types.

| Item | Worse (25%) | Standard (50%) | Better (25%) |
| --- | --- | --- | --- |
| **Bandage** | Gauze roll: 5 s, heals 8 | Bandage: 4 s, heals 10 | Emergency bandage: 3 s, heals 12 |
| **First aid kit** | Car first aid kit: 8 s | IFAK: 6 s | Medic pouch: 6 s, two uses |
| **Med kit** | Trauma bag: 10 s | Med kit: 8 s | Combat medic bag: 8 s, two uses |
| **Energy drink** | Soda: boost +30 | Energy drink: boost +40 | Large energy drink: boost +50 |
| **Painkillers** | Aspirin: boost +45 | Painkillers: boost +60 | Morphine auto-injector: boost +60 in 3 s |
| **Adrenaline syringe** | Vial and syringe: 8 s | Adrenaline syringe: 6 s | Adrenaline auto-injector: 3 s |

Anything a cell doesn't mention stays at the standard numbers. Variants with two uses weigh 1.5 times as much (our pick). Every number here is a first pass (our pick).

- **One variant per item per match:** the match rolls each item's variant during the lobby countdown, along with the gun pool ([Pre-match lobby](match-flow.md#pre-match-lobby)). Everyone finds the same bandage, the same first aid kit, and so on, so nobody carries five kinds of med kit.
- **Rolled separately:** each item rolls on its own, so one match might have fast bandages and a slow med kit.
- **Fair inside a match:** everyone is on the same variants; what changes is from one match to the next, like gun versions ([Rules](../rules.md#versions)).
- **Named on pickup:** the pickup prompt and the inventory name the variant, like a gun's version ([HUD and inventory](gameplay.md#hud-and-inventory)).

### Escape from Tarkov's medkits, for reference

Tarkov's medkits each hold a pool of health that's used up over several heals. They range widely:

| Medkit | Health pool | Max per use | Use time | Treats |
| --- | --- | --- | --- | --- |
| AI-2 | 100 | 50 | 2 s | Nothing extra |
| Car first aid kit | 220 | 70 | 3 s | Light bleeding |
| IFAK | 300 | 50 | 3 s | Light and heavy bleeding |
| AFAK | 400 | 60 | 3 s | Light and heavy bleeding |
| Salewa | 400 | 85 | 3 s | Light and heavy bleeding |
| Grizzly | 1,800 | 175 | 5 s | Bleeding, fractures, and contusions |

Ours keep PUBG's simpler health with no bleeding or fractures, so the variants only change use time, how much an item heals or boosts, and how many uses it has.

## Sources

- [Samurai Gamers: PUBG consumable items](https://samurai-gamers.com/playerunknowns-battlegrounds-pubg/consumable-items-list-3/) · [Samurai Gamers: PUBG boost system](https://samurai-gamers.com/playerunknowns-battlegrounds-pubg/boost-system/)
- [Appuals: PUBG healing and boost items guide](https://appuals.com/playerunknowns-battlegrounds-healing-boost-items-guide/) · [Gamepressure: PUBG healing and boosting](https://www.gamepressure.com/playerunknowns-battlegrounds/healing-and-boosting-your-character/zea139) · [Gamepressure: PUBG consumables](https://gamepressure.com/playerunknowns-battlegrounds/items-consumables-healing/z3a93f)
- [PUBG Wiki: Adrenaline Syringe](https://pubg.wiki.gg/wiki/Adrenaline_Syringe) · [PUBG Wiki: Med Kit](https://pubg.wiki.gg/wiki/Med_Kit)
- [Tarkov Forge: medical items](https://tarkovforge.com/meds)
