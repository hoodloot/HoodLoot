---
description: Fixed supply. Emission-scheduled. 75% given to the poor on every spend. This is $SHARE.
---

# 🪙 $SHARE Token

$SHARE is the native currency of HOODLOOT. You earn it by looting. You spend it to upgrade your hideout and recruit new Merry Men. And every time you spend it, **most of it is given to the poor — gone forever.**

The name is a double meaning: shares (the loot you take) and sharing (the wealth you redistribute).

---

## What It Is

$SHARE is a fixed-supply, emission-scheduled, deflationary **ERC-20 token** issued on **Robinhood Chain** (an EVM Layer-2).

{% hint style="success" %}
**No presale. No VC allocation. No team salary reserve.**

**95%** of the supply is emitted as block rewards to players. The remaining **5% (1,050,000 $SHARE)** is minted once at genesis to seed on-chain liquidity — fully disclosed, minted in a single transparent event, and paired into a locked liquidity pool so the market has depth from day one.
{% endhint %}

You earn $SHARE by looting — placing Merry Men in your hideout and accumulating rewards every Robinhood Chain block. You can also acquire $SHARE on secondary markets (Uniswap is integrated on Robinhood Chain from launch).

---

## Fixed Supply

$SHARE has a hard cap of **21 million tokens**. No more will ever be created once the cap is reached.

This is not adjustable. It is enforced at the contract level.

The deflationary redistribution mechanics mean the circulating supply is always less than — and trending further below — the total ever emitted.

---

## 📊 Tokenomics

| Mechanism | Details |
|-----------|---------|
| **Total Supply Cap** | 21,000,000 $SHARE |
| **Mined by players** | 19,950,000 $SHARE (95%) — via block-reward emission |
| **Genesis liquidity** | 1,050,000 $SHARE (5%) — one-time mint to seed the locked DEX pool |
| **Emission Schedule** | Halves every 77,760,000 blocks (~90 days) |
| **Initial Emission** | ~0.135031 $SHARE per block |
| **Given to the Poor** | 75% of all $SHARE spent on outlaws and upgrades |
| **War Chest Cut** | 25% of all $SHARE spent goes to the treasury contract |
| **Referral Bonus** | 2.5% of a recruited player's rewards |
| **ETH Tolls** | Milestone tiers require ETH (valued via Chainlink ETH/USD) to the War Chest |

---

## 🕊️ Given to the Poor (Burn Mechanics)

Every time a player spends $SHARE — whether recruiting a new outlaw or upgrading their hideout — **75% of those tokens are permanently given to the poor (burned)**. This is not optional. It is enforced at the contract level on every transaction.

The remaining 25% goes to the HOODLOOT War Chest treasury contract.

{% hint style="danger" %}
The total supply started at 21 million. Every upgrade, every recruit, every Legend burn makes that number smaller. **It never goes back up.**
{% endhint %}

As the network grows and more players upgrade, the circulating supply of $SHARE shrinks. A growing player base combined with a shrinking supply creates the deflationary flywheel at the heart of HOODLOOT.

### The Deflation Flywheel

```
More players join → more $SHARE spent on outlaws & upgrades →
      ↑                                    ↓
scarcer, more valuable $SHARE  ←  75% of every spend Given to the Poor (burned)
```

Each turn of the flywheel removes $SHARE from circulation. Emission from mining tops the supply up, but it is capped and halving — every ~90 days the tap runs half as fast — while the burn scales with *activity*, which grows with the player base. The two forces pull in opposite directions, and by design the burn is the one that compounds. The players who accumulate early, before the supply thins and before the halvings bite, sit on the scarcer side of the curve.

---

## 📈 Supply Breakdown

At any point in time, the three key supply figures are:

| Metric | Description |
|--------|-------------|
| **Total Looted** | All $SHARE ever emitted as block rewards (approaches 21M cap) |
| **Total Redistributed** | All $SHARE permanently given to the poor through gameplay |
| **Circulating Supply** | Total Looted minus Total Redistributed |

```
Circulating Supply = Total Looted − Total Redistributed
```

Both Total Looted and Total Redistributed are visible in real time on the game's global stats dashboard.

---

## 💰 Earning $SHARE

The only way to earn $SHARE natively is through looting. Place Merry Men in your hideout. They contribute Loot Rate every Robinhood Chain block. You earn a proportional share of the network's block emission.

{% hint style="warning" %}
There is no other emission mechanism. **No airdrops. No staking yield. No inflation.**

Loot it, earn it, spend it wisely — because 75% of every spend goes to the poor.
{% endhint %}

For exactly how much you earn per block, see [Virtual Mining](../game-mechanics/virtual-mining.md). For what you spend it on, see [The Merry Men](outlaws.md) and [Hideouts](hideouts.md).

---

## ⚙️ On the Chain

$SHARE is the `SHARE` ERC-20 contract on Robinhood Chain. A few properties worth knowing:

| Property | Detail |
|----------|--------|
| Standard | ERC-20, 18 decimals |
| Hard cap | 21,000,000 $SHARE (enforced in-contract) |
| Minter | The `MiningEngine` contract mints all 95% of player rewards at claim time; the only other mint is the one-time genesis liquidity allocation |
| Burn | 75% of every in-game spend is burned; 25% routes to the War Chest treasury |
| Allocation | 5% (1,050,000) genesis liquidity mint, disclosed and LP-locked; no presale, no VC, no team salary reserve |
| Tradeable | Yes — Uniswap is integrated on Robinhood Chain from launch |

See [Architecture](../architecture/overview.md) for how the contracts fit together.
