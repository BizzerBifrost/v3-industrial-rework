# Rail Freight — Factory Transport for Industry
### A Victoria 3 Mod | v1.1.1 | Compatible with 1.13.x (Matcha)

---

## What This Mod Does

In vanilla Victoria 3, Railways only matter for resource extraction states — mines, logging camps, and plantations consume transportation, but **factories consume none at all**. This means a highly industrialized state with no raw resource buildings has almost no reason to build Railways, and Railways built there are barely profitable.

This mod fixes that by giving every factory a **Transportation dropdown**, identical to what resource buildings already have. Build Railways in your industrial heartland, connect your factories to the rail network, and watch both your production output and your Railway profits grow.

---

## Features

- **16 factory buildings** get a new Transportation production method group
- **Two options per factory:** No Rail (default, no effect) or Rail Transportation (requires Railways tech)
- **Rail Transportation** consumes transportation tickets and boosts factory output — shown as concrete goods quantities in the tooltip (e.g. "+9 clothes", "+10 steel")
- **Railways become profitable** in purely industrial states — factories now generate real transportation demand
- **Fully compatible with AI** — all countries benefit, ensuring a consistent world economy
- **Save-game friendly** — factories default to No Rail when the mod is first loaded

---

## Balance

| Factory tier | Transportation consumed / level | Output bonus |
|---|---|---|
| Light industry | 5 / level | +20% of base output |
| Heavy industry | 8 / level | +15% of base output |
| Military industry | 6 / level | +15% of base output |

### Net profit per level (at base transportation price £30)

| Building | Bonus goods | Net gain |
|---|---|---|
| Food Industry | +9 groceries | +£120 |
| Textile Mills | +9 clothes | +£120 |
| Furniture Manufacturies | +9 furniture | +£120 |
| Glassworks | +6 glass | +£90 |
| Tooling Workshops | +6 tools | +£90 |
| Paper Mills | +8 paper | +£90 |
| Chemical Plants | +14 fertilizer | +£180 |
| Explosives Factory | +8 explosives | +£160 |
| Synthetics Plants | +12 dye | +£240 |
| Steel Mills | +10 steel | +£260 |
| Motor Industry | +6 engines | +£120 |
| Automotive Industry | +5 automobiles | +£160 |
| Electrics Industry | +9 telephones | +£390 |
| Arms Industries | +5 small arms | +£120 |
| Artillery Foundry | +4 artillery | +£100 |
| Munition Plants | +8 ammunition | +£220 |

Rail Transportation is always net positive even when transportation prices rise above base — the output bonus comfortably covers the cost.

---

## How It Works

The mod reuses Victoria 3's existing transportation mechanics — the same system already used by Logging Camps, Mines, and Plantations — and extends it to manufacturing buildings. No new mechanics are invented.

- `transportation` is a **local good** (cannot be traded between states). Your factories will only benefit if Railways in the **same state** are producing enough transportation to supply them.
- The output bonus **scales with employment** — at 50% staffing you get roughly 50% of the bonus. No employment = no benefit, so there is no free lunch.
- The Railways technology unlocks the Rail Transportation option. You cannot select it before then.

---

## Excluded Buildings

- Shipyards (coastal buildings — rail logistics don't apply)
- All resource extraction buildings (mines, farms, plantations, logging camps, oil rigs) — these already have vanilla transportation PMs

---

## Known Limitations

Some buildings can switch their primary output good via other production method groups (e.g. Textile Mills producing luxury clothes instead of regular clothes, Automotive Industry producing aeroplanes or tanks instead of automobiles). The output bonus from Rail Transportation applies to the **base/primary good only** and does not adjust when you switch variants. This is consistent with how vanilla automation production methods work.

---

## Compatibility

- **Game version:** 1.13.x (Matcha)
- **DLC required:** None
- **Save games:** Fully supported on new games — all factories default to No Rail automatically. On existing saves, the Transportation dropdown may appear uninitialized (blank icon) when first loaded. Simply open each factory and select No Rail or Rail Transportation manually once. New factories built after loading will default correctly.
- **Other mods:** Compatible with any mod that does not also override `common/buildings/01_industry.txt`. Conflicts with mods that modify the same file — load order may help depending on the other mod's changes.
