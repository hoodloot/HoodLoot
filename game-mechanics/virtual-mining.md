---
description: How block rewards are calculated, how halvings work, and why the 21M cap matters.
---

# 💰 Virtual Mining

HOODLOOT replaces the exclusionary, capital-intensive world of physical mining with a **fully virtualised, onchain system**. No ASICs. No electricity bills. No shipping containers full of hardware. Just your wallet, a hideout, and a band of Merry Men doing the work.

Every outlaw you place in your hideout contributes Loot Rate to the global HOODLOOT network. Your share of that Loot Rate determines your share of the $SHARE emitted every Robinhood Chain block.

---

## How It Works

Virtual mining mirrors the economics of real proof-of-work mining — without the hardware barrier. The same proportional reward logic applies: the more Loot Rate you contribute relative to the network total, the more you earn.

Rewards accrue lazily, per block, based on your share of the global Loot Rate. You do not need to do anything to accumulate them. You only need to **claim**.

{% hint style="info" %}
HOODLOOT uses a fixed-supply, per-block, emission-scheduled design — calibrated to Robinhood Chain's ~100ms block time. Emission is denominated per real chain block, with the halving interval set in blocks tuned to the block time.
{% endhint %}

### Why per-block on a fast L2

Bitcoin emits per block. HOODLOOT denominates emission per *real chain block* rather than per second — and setting the halving interval in blocks, calibrated to Robinhood Chain's block time.

Robinhood Chain targets **~100ms blocks**, so a day is **864,000 blocks** and a ~90-day epoch is **77,760,000 blocks**. Emitting per real block on a chain this fast means loot lands in tiny, near-continuous increments — the arcade "numbers-go-up" feel — while the *economics* stay identical to a slow-block chain, because the per-block rate and the halving interval were both scaled to the block time. (A faster ~30-day cadence would instead use a 25,920,000-block interval.)

{% hint style="warning" %}
**~100ms is a reported figure.** Robinhood Chain's block time is cited by secondary press and is consistent with its Arbitrum Orbit stack, but is not explicitly confirmed on official docs. The emission model is denominated in *blocks*, so the game stays correct regardless — the day/epoch estimates in this page are what shift if the real block time differs. See [Robinhood Chain](../chain/robinhood-chain.md).
{% endhint %}

---

## ⚙️ Reward Formula

Rewards are distributed every Robinhood Chain block, proportional to your share of the global Loot Rate.

**Let:**

* **yourLoot** = your total Loot Rate (LR) — the sum of all Merry Men placed in your hideout
* **globalLoot** = total network Loot Rate: `globalLoot = Σ yourLoot` across all active players
* **emissionPerBlock** = $SHARE emitted per Robinhood Chain block (see halving schedule)

**Your reward per block:**

$$R_i = \frac{yourLoot}{globalLoot} \times emissionPerBlock$$

{% hint style="info" %}
**Example:** If your Merry Men contribute 500,000 LR to a network running 50,000,000 LR total, your share is 1%. If emissionPerBlock = 0.135031 $SHARE, you earn **0.00135031 $SHARE that block** — distributed every Robinhood Chain block (~100ms), so it adds up fast.
{% endhint %}

Your share grows as you recruit more Merry Men and upgrade your hideout. It shrinks when other players upgrade faster. **This is the race.**

{% hint style="info" %}
**Worked example, in full.** Suppose your band totals **500,000 LR** and the whole network is running **50,000,000 LR**. Your share is 500,000 ÷ 50,000,000 = **1%** (0.01). At the launch emission of **0.135031 $SHARE/block**:

- Per block: 0.01 × 0.135031 = **0.00135031 $SHARE**
- Blocks per day: **864,000** → per day: 0.00135031 × 864,000 ≈ **1,167 $SHARE/day**

If you then double your Loot Rate to 1,000,000 LR while the network holds steady, your share becomes 2% and your daily loot roughly doubles — until other players grow and dilute you back down. Nothing is fixed; the share is always *relative*.
{% endhint %}

---

## ♻️ Lazy Accrual

You never have to "collect" rewards block by block, and there's no bot to run. The `MiningEngine` contract records your Loot Rate and the block you last touched. Whenever you **claim** (or your Loot Rate changes), it computes everything you're owed since your last checkpoint in a single calculation and mints it — this is **lazy accrual**.

{% hint style="success" %}
* Rewards pile up automatically every block whether or not you're online.
* There is **no expiry** — pending $SHARE waits for you indefinitely.
* Minimum claim is **0.001 $SHARE** to avoid dust transactions.
* $SHARE is only ever created at claim time, never before — the supply is minted into existence exactly as it's earned.
{% endhint %}

---

## 📉 Halving Schedule

HOODLOOT follows Bitcoin's own halving ethos, recalibrated to per-block emission on a fast chain. Emissions start at approximately **0.135031 $SHARE per block** and halve every **77,760,000 blocks** — approximately every 90 days.

| Epoch | Block Range | Emission per Block | Approx. Days |
|:-----:|-------------|--------------------|:------------:|
| 0 | 0 – 77.76M | 0.135031 $SHARE | ~90 (Launch) |
| 1 | 77.76M – 155.52M | 0.067515 $SHARE | ~90 |
| 2 | 155.52M – 233.28M | 0.033758 $SHARE | ~90 |
| 3 | 233.28M – 311.04M | 0.016879 $SHARE | ~90 |
| 4 | 311.04M – 388.8M | 0.008439 $SHARE | ~90 |
| 5 | 388.8M – 466.56M | 0.004220 $SHARE | ~90 |
| … | … | halving each epoch → 0 | … |

Each epoch lasts **77,760,000 blocks ≈ 90 days** at 100ms/block, and the emission halves at every boundary. The engine reads `block.number` directly, so which epoch you're in is a pure function of the chain's own block height — no scheduler, no keeper, no trust assumption.

### Why the initial rate is what it is

The launch emission of **0.135031 $SHARE/block** isn't arbitrary. A halving series that starts at rate `R` and lasts `N` blocks per epoch sums (geometrically, `R·N·2` as epochs → ∞) to a finite total. That total was pinned to exactly **21,000,000 $SHARE** — so 0.135031 is the rate that makes the whole infinite halving series add up to the hard cap and no more. The cap isn't enforced by cutting emission short; the emission schedule *is* the cap.

{% hint style="danger" %}
**Every halving permanently reduces future emissions.** Outlaws who loot in earlier epochs earn more $SHARE per block than those who join later at the same Loot Rate. There is a real, compounding first-mover advantage built into the protocol. **Do not wait.**
{% endhint %}

---

## 🔒 The Hard Cap

$SHARE has a fixed supply of **21 million tokens** — matching Bitcoin's own legendary limit. No more will ever be created once the cap is reached.

The deflationary redistribution mechanics (75% of every $SHARE spent is permanently given to the poor) mean the circulating supply is always **less than** — and trending further below — the total ever emitted.

```
Circulating Supply = Total Looted − Total Redistributed
```

Both figures are visible in real time on the global stats dashboard.

---

## 🌐 Why Virtual Mining

Traditional proof-of-work mining is inaccessible to most people. It requires:

* Expensive, specialised hardware (ASICs)
* Cheap industrial electricity
* Technical expertise to operate
* Geographic advantages for cheap power

HOODLOOT removes **every one of those barriers**. Virtual mining delivers the same economic model — Loot Rate proportional rewards, fixed supply, deflationary pressure, halving schedule — in a format anyone with an EVM wallet can access.

{% hint style="success" %}
**No hardware. No barriers. Just Loot Rate, blocks, and $SHARE.**
{% endhint %}

---

## ⏱️ Block Time Reference

HOODLOOT runs on Robinhood Chain block time. The game ticks every time a new block is produced.

| Stat | Value |
|------|-------|
| Avg block time | ~0.1 s (100ms) |
| Blocks per day | 864,000 |
| Blocks per halving | 77,760,000 |
| Days per halving | ~90 |
| Upgrade cooldown | 864,000 blocks (~24h) |
