---
description: Loot. Claim. Upgrade. Repeat. Every action compounds — this is how the loop works.
---

# 🔄 Gameplay Loop

HOODLOOT is built around a tight, rewarding loop. Every action feeds back into the system and compounds over time.

```
Recruit Merry Men → Earn $SHARE per block → Claim Rewards
      ↑                                          ↓
 Upgrade Hideout ←——————— Spend $SHARE (75% given to the poor)
      ↑
 Become a Legend (optional) → Permanent multiplier applied forever
```

---

## 🏹 Recruit Merry Men

The Merry Men are your outlaws. Place them in open slots inside your hideout and they begin contributing to the global HOODLOOT Loot Rate immediately.

Each outlaw has two key stats:

| Stat | Description |
|------|-------------|
| **Loot Rate (LR)** | Your contribution to the global network. Higher share = more $SHARE per block. |
| **Upkeep (U)** | The draw against your hideout's upkeep cap. Cannot exceed your total. |

{% hint style="info" %}
Merry Men loot every Robinhood Chain block — approximately every 100ms. Rewards accumulate automatically. Claim whenever you are ready.
{% endhint %}

You can place multiple outlaws of any tier. Filling your hideout with the highest-tier Merry Men you can afford is always the goal.

{% hint style="success" %}
**Worked example — your first band.** You start with a free **Forest Hollow** (4 slots, 28 U cap) and a free **Ragged Peasant** (100 LR, 1 U). Save a few blocks of loot, then recruit a **Village Poacher** (180 LR, 6 U, 10 $SHARE) and two **Barefoot Archers** (420 LR, 8 U, 20 $SHARE each). That fills all 4 slots for 100 + 180 + 420 + 420 = **1,120 LR** at 1 + 6 + 8 + 8 = **23 U** — safely under the 28 U cap. Your Loot Rate just went up 11× from where you started, and you've spent 50 $SHARE (of which ~37.5 was Given to the Poor).
{% endhint %}

See the full roster and efficiency notes in [The Merry Men](../game-assets-and-token/outlaws.md).

---

## 🌲 Upgrade Your Hideout

Your hideout is your ceiling. Without upgrading it, you run out of slots and upkeep before you can deploy the outlaws that matter.

Each upgrade increases:
* **Slot count** — how many Merry Men you can place simultaneously
* **Upkeep cap (U)** — the maximum total upkeep of all placed outlaws

{% hint style="warning" %}
Upgrades cost **$SHARE** and have a **24-hour cooldown** (864,000 blocks) between each tier. You cannot skip tiers. Plan your timing around the cooldown.
{% endhint %}

### ETH Tolls

Every other tier requires an ETH payment alongside the $SHARE cost. These are **one-time milestone payments** — not recurring — valued in USD via the Chainlink ETH/USD oracle and paid to the War Chest treasury.

| ETH Toll | Tier | ETH Required |
|----------|------|:------------:|
| Forest Hollow | T1 | ~$30 USD |
| Greenwood Camp | T3 | ~$50 USD |
| Sherwood Stronghold | T5 | ~$70 USD |
| Nottingham Safehouse | T7 | ~$100 USD |
| Sherwood Throne | T9 | ~$150 USD |

Tiers 2, 4, 6, and 8 are **$SHARE-only** — no ETH. See the complete tier table in [Hideouts](../game-assets-and-token/hideouts.md).

{% hint style="info" %}
**Why the cooldown matters.** Because you can only upgrade once per ~24 hours, upgrading is a *timing* decision, not a spending one. Start each cooldown the moment you can afford the next tier — a day spent capped-out is a day of loot you can't get back. Plan your $SHARE so it's ready when the cooldown clears.
{% endhint %}

---

## 💰 Claim Your Rewards

Your $SHARE accumulates in a pending balance every Robinhood Chain block. There is no automatic distribution — you claim it manually, directly to your wallet.

{% hint style="info" %}
* No expiry on pending rewards
* Minimum claim threshold: **0.001 $SHARE** (dust protection)
* Rewards calculated from your Loot Rate share at each block
{% endhint %}

---

## ⭐ Become a Legend *(coming soon)*

Once you've climbed as far as a single run allows, **Legend Ranks** will offer a path beyond the ceiling: reset your progression in exchange for a **permanent Loot Rate multiplier** that follows you across every future run.

{% hint style="info" %}
**Legend Ranks are coming soon.** The ranks, costs, and multipliers are revealed at launch — see the [Legend Ranks](../game-mechanics/legend-ranks.md) intro.
{% endhint %}

---

## 🔗 Recruit a Merry Man

Share your wallet address. If anyone joins using your referral, you earn **2.5% of their rewards** in perpetuity — automatically, every block they loot.

No claiming required on your end. It stacks on top of your own looting income. See [Referrals](../game-mechanics/referrals.md) for how it works in detail.

---

## The Redistribution Flywheel

{% hint style="danger" %}
Every $SHARE spent on an upgrade or a new outlaw removes **75%** of it from circulation permanently — given to the poor. The band grows. The supply shrinks. The loop continues.

This is not optional. It is baked into every transaction at the contract level. The remaining 25% goes to the War Chest treasury.
{% endhint %}

---

## 🧭 The Loop, End to End

Here is one full turn of the wheel, in order:

1. **Recruit** a Merry Man from the roster (costs $SHARE; 75% is Given to the Poor).
2. **Deploy** them into an open Hideout slot — they start looting instantly, no staking step.
3. **Mine** — every ~100ms block, you accrue $SHARE proportional to your Loot Rate share.
4. **Claim** your pending $SHARE to your wallet whenever you like (min 0.001 $SHARE).
5. **Upgrade** your Hideout when the ~24h cooldown clears, unlocking more slots and upkeep.
6. **Ascend** to a Legend rank when you've maxed a run, banking a permanent multiplier.

Then repeat — bigger band, higher ceiling, more loot per block. Every step compounds the next.

{% hint style="success" %}
**Worked example — one week in.** You've upgraded to **Greenwood Camp** (T3, 12 slots, 420 U) and filled it with **Elf Scout of Sherwood** outlaws (5,000 LR, 30 U each). Twelve of them would be 360 U — over cap — so you run 14 slots' worth of upkeep across a mix: say 12 outlaws totaling ~410 U for ~65,000 LR. If the network is running 6,500,000 LR total, that's a **1% share** — at 0.135031 $SHARE/block you're pulling ~0.00135 $SHARE per block, ~1,167 $SHARE/day at that emission. You reinvest into the next Hideout tier, and the loop tightens.
{% endhint %}
