# Power RP 5.0 — Economy Rebalance V2

**Date:** February 21, 2026  
**Scope:** 13 scripts + 1 external system (qb-pawnsystem)  
**Goal:** Create a balanced income ladder where risk, effort, and player coordination match reward.

---

## Table of Contents

1. [Design Philosophy](#design-philosophy)
2. [Mining — RxMining & pwr-sellmaterials](#1-mining--rxmining--pwr-sellmaterials)
3. [Fishing — 0r-fishingv2](#2-fishing--0r-fishingv2)
4. [Diving — s4-diving](#3-diving--s4-diving)
5. [Legal Jobs — wais-jobpack](#4-legal-jobs--wais-jobpack)
6. [Illegal Labs — 0r-illegalpack](#5-illegal-labs--0r-illegalpack)
7. [Street Drug Selling — op-drugselling](#6-street-drug-selling--op-drugselling)
8. [Truck Robbery — devhub_truckRobbery](#7-truck-robbery--devhub_truckrobbery)
9. [Drywood Cutter — devhub_drywoodCutter](#8-drywood-cutter--devhub_drywoodcutter)
10. [Herbal Alchemist — devhub_herbalAlchemist](#9-herbal-alchemist--devhub_herbalalchemist)
11. [House Robbery Fencing — qb-pawnsystem](#10-house-robbery-fencing--qb-pawnsystem)
12. [Bug Fixes](#bug-fixes)
13. [Economy Ladder Summary](#economy-ladder-summary)
14. [Full Change Log](#full-change-log)

---

## Design Philosophy

The server economy had two core problems:

1. **Some activities paid too much** relative to their effort and risk (mining, corner drug sales, diving Mission 3).
2. **Some activities paid too little** to compete for player attention (fishing, entry-level legal jobs, gang-tier drugs).

The rebalance creates a smooth income ladder:

- **Safe, easy activities** → lowest pay but zero risk
- **Moderate effort activities** → mid-tier pay
- **High-risk or group-required activities** → highest pay

No single grind should dominate. Every step up the ladder demands more risk, more investment, or more player coordination.

---

## 1. Mining — RxMining & pwr-sellmaterials

### Problem

Mining was one of the **highest $/hr activities** on the server with virtually zero risk — no police, no PvP competition, just AFK-style grinding. It was a money printer that made riskier activities feel pointless by comparison.

### Changes

#### Ore Sell Prices (25-40% reduction)

| Ore | Old Price Range | New Price Range | Change |
|-----|----------------|-----------------|--------|
| Coal | $15 – $30 | $10 – $20 | -33% |
| Carbon | $18 – $35 | $12 – $25 | -33% |
| Copper | $25 – $50 | $18 – $35 | -28% |
| Iron | $30 – $60 | $22 – $45 | -27% |
| Aluminum | $40 – $80 | $30 – $55 | -25% |
| Sulfur | $45 – $90 | $32 – $60 | -29% |
| Gold | $50 – $100 | $35 – $70 | -30% |

#### Gem Sell Prices (33-40% reduction)

| Gem | Old Price Range | New Price Range | Change |
|-----|----------------|-----------------|--------|
| Onyx | $75 – $150 | $50 – $100 | -33% |
| Aquamarine | $75 – $150 | $50 – $100 | -33% |
| Citrine | $75 – $150 | $50 – $100 | -33% |
| Jade | $75 – $150 | $50 – $100 | -33% |
| Diamond | $125 – $250 | $75 – $150 | -40% |
| Ruby | $100 – $200 | $60 – $120 | -40% |
| Sapphire | $100 – $200 | $60 – $120 | -40% |
| Tanzanite | $115 – $225 | $70 – $140 | -39% |

#### Ore Drop Rate Adjustments

| Ore | Old Chance | New Chance |
|-----|-----------|------------|
| Coal | 50% | 40% |
| Carbon | 50% | 40% |

#### Uncommon/Rare Ore Quantity

- All uncommon and rare ores: **max item quantity reduced from 4 → 3**

#### Tool Durability (costs more to mine)

| Tool | Old Durability | New Durability | Effect |
|------|---------------|----------------|--------|
| Mining Drill | 200 | 150 | Breaks 25% faster |
| Laser Drill | 300 | 100 | Breaks 67% faster |

#### Foundry Sell Prices — pwr-sellmaterials (raised to compensate)

| Material | Old Base/Min/Max | New Base/Min/Max |
|----------|-----------------|------------------|
| Coal | $6 / $3 / $9 | $12 / $7 / $18 |
| Carbon | $10 / $5 / $14 | $16 / $9 / $24 |

### Why the Foundry Goes Up

Coal and Carbon are the most common ores everyone gets. Raising their foundry value ensures basic mining income stays viable even after the ore price cuts. This shifts value from **rare RNG drops** toward **consistent base income**, making mining more predictable and less slot-machine-like.

### Economy Impact

Mining drops from a top-tier money printer to a **solid mid-tier legal job**. Still profitable, still worth doing — just not dominant over everything else.

---

## 2. Fishing — 0r-fishingv2

### Problem

Fishing was slightly underpaid relative to other legal activities, especially after the mining nerf. Without a bump, it would fall even further behind.

### Changes

| Fish | Old Price | New Price | Change |
|------|----------|-----------|--------|
| Fish/Bluegill | $8 | $10 | +$2 |
| Tuna | $65 | $75 | +$10 |
| Swordfish | $80 | $90 | +$10 |
| Tiger Shark | $100 | $115 | +$15 |
| Killer Whale | $130 | $150 | +$20 |

### Why

The rare, hard-to-catch fish (Shark, Whale) got the biggest bumps because they require skill and luck. Common fish got minimal bumps. This rewards experienced fishers more than AFK ones.

### Economy Impact

Fishing becomes a **slightly better alternative to mining**, giving players variety in legal income without either activity dominating.

---

## 3. Diving — s4-diving

### Problem

Diving had multiple issues:
- A **game-breaking bug** where cash crate drops never worked (the word "money" was missing from all prize lists)
- **Mission 3** was printing both high-value items (rolex, goldbar) AND large cash rewards
- **No cooldown** meant players could chain-run missions indefinitely

### Changes

#### Mission Base Rewards

| Mission | Old Reward | New Reward | Change |
|---------|-----------|------------|--------|
| #1 Saints Airlines | $300 | $500 | +67% |
| #2 Hightable | $450 | $750 | +67% |
| #3 Deep Syndicate | $600 | $1,200 | +100% |
| #4 EMS Plane Crash | $300 | $400 | +33% |

#### Mission 3 Earnings Adjustment

- **Removed** rolex and goldbar from Mission 3 earnings
- **Kept** diamond_ring + $250 cash bonus
- Rationale: $1,200 base + diamond ring + $250 is generous enough without also dropping goldbars

#### Random Crate Cash (reduced across all missions)

| Mission | Old Cash Range | New Cash Range |
|---------|---------------|----------------|
| Lost Treasure | $150 – $400 | $50 – $150 |
| Marine Research | $150 – $400 | $75 – $200 |
| Deep Exploration | $200 – $500 | $100 – $250 |
| EMS Plane Crash | $150 – $400 | $25 – $75 |

#### New: 15-Minute Personal Cooldown

- After completing any diving mission, a player must wait **15 minutes** before starting another
- Cooldown is per-player (doesn't affect other players)
- Cooldown clears if the player disconnects

#### Bug Fix: Cash Crate Drops

- The string `"money"` was missing from all 4 mission prize lists
- Without it, the code that checks for cash drops could never fire
- Added `"money"` to all prize tables: lostTreasure, marineResearch, deepExploration, emsplanecrash

### Economy Impact

Diving is now **more rewarding per-run** but **capped by the cooldown**. Mission 3 is still the best mission but no longer prints goldbars on top of everything else. The bug fix means cash crates actually drop now, making runs more varied.

---

## 4. Legal Jobs — wais-jobpack

### Problem

Three issues:
1. Some jobs were slightly underpaid compared to alternatives
2. UI pay estimates were inaccurate
3. **The entire XP/leveling system was broken** — a critical bug meant no player was earning XP, gaining levels, or completing quests

### Changes

#### Hotdog Vendor

| Stat | Old | New |
|------|-----|-----|
| Min pay | $65 | $70 |
| Max pay | $85 | $90 |

#### Hunter (all 4 hunting zones)

| Animal | Old Pay | New Pay |
|--------|---------|---------|
| Boar | $50 | $60 |
| Deer | $50 | $65 |
| Mountain Lion | $110 | $120 |
| Coyote | $70 | $80 |

*Applied across Zone 1 (4 animals), Zone 2 (deer + mt lion), Zone 3 (deer + boar), Zone 4 (deer + mt lion + coyote)*

#### Fire Department (all 11 fire calls)

Every fire got a flat **+$20** increase:

| Fire | Old Pay | New Pay |
|------|---------|---------|
| Fire 1 | $300 | $320 |
| Fire 2 | $310 | $330 |
| Fire 3 | $340 | $360 |
| Fire 4 | $400 | $420 |
| Fire 5 | $300 | $320 |
| Fire 6 | $340 | $360 |
| Fire 7 | $290 | $310 |
| Fire 8 | $280 | $300 |
| Fire 9 | $350 | $370 |
| Fire 10 | $370 | $390 |
| Fire 11 | $350 | $370 |

#### UI Job Pay Estimates Updated

| Job | Old Estimate | New Estimate |
|-----|-------------|--------------|
| Mobile Hotdog | $750/hr | $800/hr |
| Hunter | $1,700/hr | $750/hr |
| Fire Department | $1,650/hr | $1,800/hr |

*Note: Hunter estimate was wildly inflated at $1,700 — corrected to realistic $750*

#### XP System Bug Fix (Critical)

**Root cause:** The escrowed (locked) server code calls `AddMoney(source, amount)` with only 2 arguments. The function expected a 3rd argument (`comingJob`) to look up the player's job for XP tracking. Since it was never passed, `comingJob` was always `nil`, and XP was never recorded.

**Fix:** Added a server-side `_playerCurrentJob` table that tracks each player's active job when they start work via `SetJob`. The `AddMoney` function now falls back to this tracker when `comingJob` is missing. Also added cleanup on `playerDropped` to prevent memory leaks.

### Economy Impact

Immediate pay is only slightly higher (~5-10%), but the **XP fix** is the most impactful single change. With XP working, players gain levels → level multipliers increase earnings over time → quest rewards become achievable. This rewards long-term dedication rather than just raw time spent.

---

## 5. Illegal Labs — 0r-illegalpack

### Problem

Labs were highly profitable. The original plan considered adding police alert chances, but investigation revealed alerts already fire on **every single action** during a lab run (3+ alerts per cycle per person). Adding more would make labs unplayable.

### Changes

| Lab Job | Old Payout | New Payout | Change |
|---------|-----------|------------|--------|
| Fraud | $4,000 | $3,500 | -12.5% |
| Gun Smuggling | $2,200 | $2,000 | -9% |
| Illegal Delivery | $1,500 | $1,400 | -7% |

Police alert rate: **Unchanged at 0%** (alerts already fire per-action within the lab scripts themselves)

### Economy Impact

Lab income drops ~10% on average. Labs remain among the highest-paying activities, which is appropriate because they require: lab ownership/access, supply costs, and constant police exposure from the built-in per-action alerts.

---

## 6. Street Drug Selling — op-drugselling

### Problem

Two issues:
1. **Public corner drugs** (weed, meth, coke, moonshine) were too profitable for zero-investment solo play
2. **Gang-tier drugs** (Phantom/Exotic/Mythical) underpaid relative to the investment required (gang membership, drug empire, rarity)
3. All drugs used the same flat dispatch chance — selling weed was as risky as selling coke

### Changes

#### Public Drug Prices (lowered 30-50%)

| Drug | Old (Low/Mid/High) | New (Low/Mid/High) | Change |
|------|--------------------|--------------------|--------|
| Moonshine | $40 / $45 / $50 | $20 / $30 / $40 | -40% |
| Rolled Weed | $40 / $50 / $70 | $25 / $35 / $50 | -38% |
| Packed Meth | $150 / $250 / $350 | $100 / $175 / $250 | -33% |
| Packed Coke | $200 / $350 / $500 | $140 / $225 / $320 | -36% |

#### Gang Drug Prices — Phantom Tier (12 variants, buffed)

| Quality | Old | New | Change |
|---------|-----|-----|--------|
| Low | $75 | $85 | +13% |
| Mid | $85 | $110 | +29% |
| High | $100 | $140 | +40% |

#### Gang Drug Prices — Exotic Tier (9 variants, adjusted)

| Quality | Old | New | Change |
|---------|-----|-----|--------|
| Low | $175 | $165 | -6% |
| Mid | $185 | $200 | +8% |
| High | $200 | $240 | +20% |

#### Gang Drug Prices — Mythical Tier (~25 variants, adjusted)

| Quality | Old | New | Change |
|---------|-----|-----|--------|
| Low | $275 | $250 | -9% |
| Mid | $285 | $300 | +5% |
| High | $300 | $360 | +20% |

#### NEW: Per-Drug Police Dispatch Chance

Previously all drugs used a single flat `dispatchCallChance`. Now each drug type has its own risk level:

| Drug | Dispatch Chance | Risk Level |
|------|----------------|------------|
| Moonshine | 20% per sale | Low |
| Rolled Weed | 20% per sale | Low |
| Packed Meth | 30% per sale | Medium |
| Packed Coke | 35% per sale | High |
| Gang drugs | Default rate | Varies |

**Technical implementation:** Modified `client/client.lua` to read `drugCfg.dispatchChance` per drug item and fall back to the global `Config.DrugSelling.dispatchCallChance` if not set.

### Economy Impact

**Corner hustling** with basic drugs is significantly less profitable AND riskier. Selling weed on a corner now pays 40% less and still has a 1-in-5 chance of police showing up.

**Gang drug empires** are more profitable, especially at mid/high quality tiers. This pushes players toward building drug organizations (which creates RP) rather than running solo on corners.

The per-drug dispatch creates a true **risk/reward gradient**: cheap drugs = low risk/low pay, hard drugs = high risk/higher pay. Players make meaningful choices about what to sell and where.

---

## 7. Truck Robbery — devhub_truckRobbery

### Problem

Truck robbery had wildly inconsistent payouts — sometimes 3 goldbars worth a fortune, sometimes $200 in marked bills and nothing else. Too much RNG.

### Changes

#### Loot Table

| Item | Old | New | Change |
|------|-----|-----|--------|
| Marked Bills (min) | $200 | $600 | +200% |
| Marked Bills (max) | $1,000 | $1,500 | +50% |
| Goldbar (chance) | 40% | 25% | -37% |
| Goldbar (max qty) | 3 | 2 | -33% |
| Diamond (chance) | 30% | 20% | -33% |
| Diamond (max qty) | 2 | 1 | -50% |

#### Crime Traders & Cooldown

| Setting | Old | New |
|---------|-----|-----|
| Crime Traders money bonus | $500 | $750 |
| Personal cooldown | 30 min | 20 min |

### Economy Impact

**Higher floor, lower ceiling.** The worst-case payout tripled (from $200 to $600 minimum), while the jackpot scenarios (3 goldbars + 2 diamonds) are gone. The average payout per heist is similar, but the variance is drastically reduced. Fewer "wasted run" frustrations, fewer "I got rich from one truck" windfalls. The shorter cooldown lets you run slightly more often to offset rarer item drops.

---

## 8. Drywood Cutter — devhub_drywoodCutter

### Problem

One of the lowest-paying legal jobs on the server. Not competitive with alternatives.

### Changes

| Setting | Old | New | Change |
|---------|-----|-----|--------|
| Base job money | $250 | $275 | +10% |
| Quest: Cut Branches | $600 | $650 | +8% |
| Quest: Pick Up Wood | $800 | $850 | +6% |
| Quest: Use Saw | $600 | $650 | +8% |

### Economy Impact

~10% pay increase. Keeps drywood cutting as a viable entry-level job without overshooting.

---

## 9. Herbal Alchemist — devhub_herbalAlchemist

### Problem

Same as drywood cutter — underpaid for the time investment required.

### Changes

| Setting | Old | New | Change |
|---------|-----|-----|--------|
| Base job money | $250 | $275 | +10% |
| Quest: Collect Roses | $200 | $250 | +25% |
| Quest: Collect Potentilla | $200 | $250 | +25% |
| Quest: Collect Mushrooms | $300 | $350 | +17% |
| Quest: Collect Medicinal Plantain | $200 | $250 | +25% |
| Quest: Collect Jalapenos | $300 | $350 | +17% |
| Quest: Collect Hedera Helix | $300 | $350 | +17% |
| Quest: Collect Gynura Procumbens | $200 | $250 | +25% |
| Quest: Collect Daisies | $300 | $350 | +17% |
| Quest: Collect Aloe | $300 | $350 | +17% |

### Economy Impact

~10-25% pay increase depending on the quest. Brings herbal alchemist in line with other gathering professions.

---

## 10. House Robbery Fencing — qb-pawnsystem

### Problem

Three issues:
1. Most items had nearly **flat pricing** — a sarcophagus and a bar of soap both paid $5 in the built-in pawn
2. **36 stealable items had no pawn entry at all** — players could steal them from houses but no shop would buy them
3. No meaningful value difference between common and rare items — no reason to prioritize certain loot

### Changes

#### Existing Item Price Adjustments (43 items, 10-17% increases with rarity tiers)

**Junk Tier ($5 – $18)** — Common household items found everywhere:

| Item | Old | New |
|------|-----|-----|
| dh_hr_rope | $5 | $5 |
| dh_hr_plunger | $5 | $5 |
| dh_hr_soap_2 | $5 | $8 |
| dh_hr_pot | $6 | $10 |
| dh_hr_knife | $8 | $12 |
| dh_hr_hard_disc | $10 | $15 |
| dh_hr_toaster | $10 | $15 |
| dh_hr_dress | $10 | $15 |
| dh_hr_headphones | $12 | $18 |

**Low Tier ($20 – $40)** — Slightly valuable, worth grabbing if you have space:

| Item | Old | New |
|------|-----|-----|
| dh_hr_scales_2 | $20 | $25 |
| dh_hr_brush_pot | $20 | $25 |
| dh_hr_soap | $20 | $25 |
| dh_hr_casino_car | $20 | $28 |
| dh_hr_passport | $20 | $30 |
| dh_hr_golf | $30 | $38 |
| dh_hr_plant | $30 | $35 |

**Mid Tier ($40 – $85)** — Clearly valuable finds:

| Item | Old | New |
|------|-----|-----|
| dh_hr_luggage_2 | $40 | $50 |
| dh_hr_speaker | $40 | $50 |
| dh_hr_tablet | $40 | $50 |
| dh_hr_champagne | $50 | $60 |
| dh_hr_bike | $50 | $60 |
| dh_hr_table | $55 | $65 |
| dh_hr_remote | $65 | $75 |
| dh_hr_mug | $65 | $75 |
| dh_hr_hairdryer | $70 | $80 |
| dh_hr_bottle | $70 | $80 |
| dh_hr_gold_cd | $70 | $80 |
| dh_hr_iron | $75 | $85 |

**High Tier ($95 – $165)** — Premium finds, prioritize these:

| Item | Old | New |
|------|-----|-----|
| dh_hr_pestle | $85 | $95 |
| dh_hr_laptop | $85 | $100 |
| dh_hr_tv | $90 | $105 |
| dh_hr_wheel | $90 | $105 |
| dh_hr_radio | $90 | $100 |
| dh_hr_mixer | $95 | $110 |
| dh_hr_drone | $95 | $115 |
| dh_hr_painting | $100 | $115 |
| dh_hr_clock | $100 | $115 |
| dh_hr_statue_4 | $120 | $140 |
| dh_hr_skull | $130 | $150 |
| dh_hr_guitar | $140 | $165 |

**Rare Tier ($190 – $350)** — Jackpot items, grab these first:

| Item | Old | New |
|------|-----|-----|
| dh_hr_statue_2 | $165 | $190 |
| dh_hr_statue_3 | $175 | $200 |
| dh_hr_tiger_2 | $200 | $240 |
| dh_hr_pc | $200 | $240 |
| dh_hr_sarcophagus | $300 | $350 |

#### Newly Added Items (36 items that previously couldn't be pawned)

| Item | Price | Tier |
|------|-------|------|
| dh_hr_rope | $5 | Junk |
| dh_hr_plunger | $5 | Junk |
| dh_hr_shoe_box | $8 | Junk |
| dh_hr_umbrella | $8 | Junk |
| dh_hr_mouse | $10 | Junk |
| dh_hr_doll | $10 | Junk |
| dh_hr_shirt | $10 | Junk |
| dh_hr_shovel | $10 | Junk |
| dh_hr_basket | $10 | Junk |
| dh_hr_toilet_bag | $10 | Junk |
| dh_hr_teddy_bear | $12 | Junk |
| dh_hr_doll_2 | $12 | Junk |
| dh_hr_bong | $15 | Junk |
| dh_hr_bed_dog | $15 | Junk |
| dh_hr_shave_box | $15 | Junk |
| dh_hr_chopboard | $15 | Junk |
| dh_hr_scales | $20 | Low |
| dh_hr_keyboard | $20 | Low |
| dh_hr_plant_2 | $20 | Low |
| dh_hr_iron_2 | $25 | Low |
| dh_hr_fan | $25 | Low |
| dh_hr_desk_lamp | $25 | Low |
| dh_hr_teapot | $25 | Low |
| dh_hr_coffee | $30 | Low |
| dh_hr_tool_box | $30 | Low |
| dh_hr_bedside_clock | $35 | Low |
| dh_hr_luggage | $40 | Mid |
| dh_hr_bike_2 | $45 | Mid |
| dh_hr_perfume | $55 | Mid |
| dh_hr_monitor | $85 | Mid |
| dh_hr_trophy | $100 | High |
| dh_hr_necklace | $120 | High |
| dh_hr_statue | $120 | High |
| dh_hr_sculpture | $130 | High |
| dh_hr_statue_5 | $140 | High |
| dh_hr_tiger | $150 | High |

### Economy Impact

House robbery becomes **strategic** — players should prioritize rare items (tiger rug $240, sarcophagus $350, PC $240) over junk (soap $8, shoe box $8). Previously almost everything paid $5, so there was no reason to be selective.

More importantly, **all stolen items can now be sold**. Previously 36 items had no buyer, meaning a third of a robbery could be wasted inventory.

---

## Bug Fixes

Three bugs were discovered during audit and fixed as part of this rebalance:

### 1. wais-jobpack XP System (Critical)

- **Symptom:** No player was earning XP, gaining levels, or completing quests across ALL wais-jobpack jobs
- **Root cause:** Escrowed server code calls `AddMoney(source, amount)` with only 2 arguments. The function expected a 3rd argument (`comingJob`) to determine which job to credit XP to. Since it was never passed, XP tracking silently failed.
- **Fix:** Added `ConfigSv._playerCurrentJob` server-side tracker. When a player starts a job via `SetJob`, their job name is stored. `AddMoney` now falls back to this tracker when `comingJob` is nil. Cleanup handler added on `playerDropped`.
- **File:** `wais-jobpack/config_sv.lua`

### 2. s4-diving Cash Crate Drops (Game-Breaking)

- **Symptom:** Random crate drops during diving missions never contained cash, only items
- **Root cause:** The word `"money"` was missing from the `prizes` table in all 4 mission files. The code checks `if prize == "money"` to award cash instead of items — but "money" was never in the list to be randomly selected.
- **Fix:** Added `"money"` to all 4 mission prize lists (lostTreasure, marineResearch, deepExploration, emsplanecrash)
- **Files:** `s4-diving/missions/lostTreasure.lua`, `marineResearch.lua`, `deepExploration.lua`, `emsplanecrash.lua`

### 3. qb-pawnsystem Missing Items (Quality of Life)

- **Symptom:** 36 house robbery items could be stolen but not sold at any pawnshop
- **Root cause:** Items existed in devhub_houseRobbery house layouts (House1-House6) but were never added to qb-pawnsystem's `Config.Items` table
- **Fix:** Added all 36 missing items with appropriate rarity-tiered prices
- **File:** `qb-pawnsystem/config.lua`

---

## Economy Ladder Summary

Expected $/hr ranges from lowest to highest. These are estimates based on config values, not guarantees — actual income varies with player skill, RNG, and server conditions.

```
Tier 1: Entry Legal Jobs                    ~$500 – $800/hr
         Hotdog Vendor, Drywood Cutter,
         Herbal Alchemist
         ↳ Zero risk, accessible to new players

Tier 2: Mid Legal Jobs                      ~$800 – $1,200/hr
         Fishing, Hunting, Fire Department
         ↳ More engagement, slightly better pay

Tier 3: Mining                              ~$1,000 – $1,500/hr
         RxMining ore + gem sales
         ↳ Nerfed from top-tier, now balanced mid

Tier 4: Diving                              ~$1,200 – $1,800/hr
         s4-diving missions
         ↳ Cooldown-gated, requires travel + skill

Tier 5: Corner Drug Sales                   ~$1,500 – $2,500/hr
         op-drugselling public drugs
         ↳ Police risk (20-35%), no gang needed

Tier 6: House Robbery → Pawn               ~$2,000 – $3,000/hr
         devhub_houseRobbery + qb-pawnsystem
         ↳ Police risk, lockpicks, item RNG

Tier 7: Truck Robbery                       ~$2,500 – $4,000/hr
         devhub_truckRobbery
         ↳ High risk, 20min cooldown

Tier 8: Gang Drug Empire                    ~$3,000 – $5,000/hr
         op-drugselling gang-tier drugs
         ↳ Requires gang, drug empire, rare drugs

Tier 9: Illegal Labs                        ~$4,000 – $6,000/hr
         0r-illegalpack (fraud, guns, delivery)
         ↳ Requires lab ownership, constant alerts
```

### Design Principles

1. **Risk = Reward** — Safe activities pay less, dangerous ones pay more
2. **Investment = Return** — Activities requiring ownership (labs), organization (gangs), or preparation (lockpicks) pay more than walk-up activities
3. **No Free Money** — Every activity has a limiting factor (cooldowns, tool costs, police, RNG)
4. **Progression Matters** — XP fix means dedicated players earn more over time through level multipliers
5. **Choice Over Grinding** — Drug type selection, item prioritization in house robbery, and mission selection all create meaningful player decisions

---

## Full Change Log

### Files Modified

| Script | File(s) Changed |
|--------|----------------|
| RxMining | `config/tools.lua`, `config/ores.lua` |
| pwr-sellmaterials | `config.lua` |
| 0r-fishingv2 | `config/market.lua` |
| s4-diving | `config.lua`, `missions/lostTreasure.lua`, `missions/marineResearch.lua`, `missions/deepExploration.lua`, `missions/emsplanecrash.lua`, `missions/earns.lua`, `server/server.lua` |
| wais-jobpack | `config.lua`, `config_sv.lua`, `client/editable.lua` |
| 0r-illegalpack | `escrow/jobs/fraud/config.lua`, `escrow/jobs/gun_smuggling/config.lua`, `escrow/jobs/illegal_delivery/config.lua` |
| op-drugselling | `config/MainConfig.lua`, `client/client.lua` |
| devhub_truckRobbery | `configs/shared.lua`, `configs/server.lua` |
| devhub_drywoodCutter | `configs/shared.lua` |
| devhub_herbalAlchemist | `configs/shared.lua` |
| qb-pawnsystem | `config.lua` |

### New Systems Added

| System | Location | Description |
|--------|----------|-------------|
| Diving personal cooldown | `s4-diving/server/server.lua` + `missions/earns.lua` | 15-min per-player cooldown between missions using `PlayerCooldowns` table + `GetGameTimer()` |
| Per-drug dispatch chance | `op-drugselling/client/client.lua` + `config/MainConfig.lua` | Each drug item can have its own `dispatchChance` field; client reads it before dispatch check |
| XP job tracker | `wais-jobpack/config_sv.lua` | `_playerCurrentJob` table + `SetJob` tracking + `playerDropped` cleanup |

### Scripts NOT Modified (unchanged)

| Script | Reason |
|--------|--------|
| mt-restaurants | Not in rebalance scope |
| devhub_racing | Not in rebalance scope |
| devhub_laptop | Not in rebalance scope (Crime Traders UI only) |
| devhub_houseRobbery | Built-in pawnshop disabled (`enabled = false`); fencing handled by qb-pawnsystem |
| plt_drugs | Drug production — not part of selling economy |
| 0r-drugbusiness | Drug empire management — not part of sell prices |
