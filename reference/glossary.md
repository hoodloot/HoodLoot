---
description: Every HOODLOOT term, defined. Speak like an outlaw.
---

# 📖 Glossary

The language of Sherwood, defined. Terms are grouped, then listed A–Z within each group.

---

## Core Terms

**$SHARE** — HOODLOOT's native token: a fixed-supply, emission-scheduled, deflationary ERC-20 on Robinhood Chain, hard-capped at 21,000,000. Earned by looting, spent on outlaws, upgrades, and Legend ranks. The name puns on a *share* (stock) and *sharing* the wealth. See [$SHARE Token](../game-assets-and-token/share-token.md).

**Merry Man / Merry Men** — Your outlaw(s); the miners. Thirteen of them, from the free Ragged Peasant to Robin Hood, the Golden Arrow. Each has a Loot Rate and an Upkeep. See [The Merry Men](../game-assets-and-token/outlaws.md).

**Hideout** — Your base of operations; a facility. Nine tiers, Forest Hollow → Sherwood Throne. Each tier grants a slot count and an upkeep cap. See [Hideouts](../game-assets-and-token/hideouts.md).

**Loot Rate (LR)** — A Merry Man's contribution to the network (the game's *hashrate*). Your total Loot Rate, relative to the global total, determines your share of each block's emission.

**Upkeep (U)** — The cost of keeping a Merry Man (the game's *power draw*). The sum of your outlaws' Upkeep can't exceed your Hideout's upkeep cap.

---

## Economy & Rewards

**Block Reward / Emission** — The $SHARE the protocol emits each Robinhood Chain block, split across all active players by Loot Rate share. Starts at ~0.135031 $SHARE/block.

**Emission per Block** — The current $SHARE issued per block; halves at each epoch boundary.

**Epoch** — A 77,760,000-block (~90-day) window between halvings. Emission is constant within an epoch and halves at the next.

**Halving** — The 50% cut to emission per block at every epoch boundary (every 77,760,000 blocks). Recalibrated to per-block emission on a fast chain.

**Hard Cap** — The fixed maximum $SHARE supply: **21,000,000**. Enforced in-contract; the halving series sums to exactly this.

**Lazy Accrual** — The model where rewards pile up per block automatically and are only computed and minted when you **claim** (or your Loot Rate changes). No bot, no per-block collection.

**Claim** — The action of minting your accumulated pending $SHARE to your wallet. Minimum 0.001 $SHARE (dust protection); no expiry on pending rewards.

**First-Mover Advantage** — Because emission halves over time and supply thins with the burn, players who loot in earlier epochs earn more per Loot Rate than later joiners. Built into the schedule.

**Loot Rate Share** — Your fraction of the global Loot Rate: `yourLoot / globalLoot`. Multiplied by emission per block to give your per-block reward.

---

## Burn, Treasury & Supply

**Given to the Poor** — The **75%** of every $SHARE spend that is permanently burned at the contract level. HOODLOOT's deflation, and its Robin Hood soul.

**Burn** — Permanent removal of $SHARE from supply. Synonymous here with "Given to the Poor."

**War Chest** — The treasury contract. Receives the **25%** of every $SHARE spend that isn't burned, plus all ETH tolls.

**Total Looted** — All $SHARE ever emitted as block rewards (approaches the 21M cap).

**Total Redistributed** — All $SHARE ever burned (Given to the Poor) through gameplay.

**Circulating Supply** — `Total Looted − Total Redistributed`. The $SHARE actually in players' hands.

**Deflation Flywheel** — The self-reinforcing loop: more players → more spending → more burned → scarcer $SHARE. The burn scales with activity while emission is capped and halving.

---

## Progression

**Legend Rank / Prestige** — A prestige system granting a permanent Loot Rate multiplier in exchange for resetting your run. **Coming soon** — details at launch. See [Legend Ranks](../game-mechanics/legend-ranks.md).

**Ascend / Ascension** — The act of taking a Legend rank: reset your progression, keep a permanent multiplier forever.

**Multiplier** — The permanent factor a Legend rank will apply to your effective Loot Rate. Legend Ranks are coming soon.

**ETH Toll** — A one-time, USD-valued ETH payment charged at milestone Hideout tiers (1, 3, 5, 7, 9) and every Legend rank. Priced via the Chainlink ETH/USD oracle; paid to the War Chest.

**Upgrade Cooldown** — The **864,000-block (~24h)** wait between Hideout upgrades. You can't skip or rush tiers.

**Slot** — A placement position in your Hideout. One Merry Man per slot; the tier sets how many you get (4 → 42).

**Upkeep Cap** — The maximum total Upkeep your Hideout supports. Placing an outlaw over the cap is blocked.

**Recruit a Merry Man / Referral** — Sharing your address so others join under you, earning you **2.5%** of their loot forever. One-level, set-once. See [Referrals](../game-mechanics/referrals.md).

---

## Chain & Tech

**Robinhood Chain** — Robinhood's EVM Layer-2 (Arbitrum Orbit), ETH gas, ~100ms blocks. Where HOODLOOT lives. Chain IDs `46630` (testnet) / `4663` (mainnet). See [Robinhood Chain](../chain/robinhood-chain.md).

**ETH** — The native gas token of Robinhood Chain, and the currency of tolls. Not $SHARE.

**Chainlink ETH/USD** — The price oracle that converts USD-valued tolls into ETH (wei) at transaction time.

**Chain ID** — The network identifier your wallet must match exactly: `46630` testnet, `4663` mainnet.

**Faucet** — The testnet source of free ETH (`faucet.testnet.chain.robinhood.com`).

**Contracts** — The onchain smart contracts that run HoodLoot — the $SHARE token, the mining engine, the outlaws, the hideouts, and more. See [Architecture](../architecture/overview.md).

**Per-block calibration** — Denominating emission per *real chain block* (not per second) and setting the halving interval in blocks, calibrated to the chain's block time — the design HOODLOOT uses for a fast L2.
