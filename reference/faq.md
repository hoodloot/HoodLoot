---
description: The common questions about HOODLOOT, $SHARE, halvings, and the chain — answered.
---

# ❓ FAQ

Quick answers to the questions outlaws ask most. For deeper detail, each answer links onward.

---

### What is HOODLOOT?

An onchain arcade mining game on [Robinhood Chain](../chain/robinhood-chain.md). You recruit **Merry Men**, place them in a **Hideout**, and they loot **$SHARE** every block in proportion to your share of the network's Loot Rate. No hardware — just a wallet. Start at [About](../about.md).

### What is $SHARE?

The game's native token: a fixed-supply, emission-scheduled, deflationary **ERC-20** on Robinhood Chain, hard-capped at **21,000,000**. You earn it by looting and spend it on outlaws, upgrades, and Legend ranks. The name is a double meaning — a *share* (stock) and *sharing* the wealth. See [$SHARE Token](../game-assets-and-token/share-token.md).

### Is $SHARE real money? Is this financial advice?

$SHARE is an in-game token. It's tradeable (Uniswap is on Robinhood Chain from launch), but HOODLOOT is a game, not an investment product, and nothing here is financial advice. On testnet, everything — including test ETH — has **no real value**.

### Do I need to buy $SHARE to start?

No. Your first Hideout (**Forest Hollow**) and first Merry Man (**Ragged Peasant**) are free of $SHARE. You only need a little **ETH** for gas and the entry toll. You earn your first $SHARE by looting, then spend it from there.

### Do I need ETH?

Yes — gas on Robinhood Chain is paid in **ETH**, not $SHARE, and milestone Hideout tiers and Legend ranks charge USD-valued **ETH tolls**. On testnet, get free ETH from the [faucet](../getting-started/setup.md). On mainnet, bridge ETH in.

### How much does it cost to start?

On testnet: nothing (faucet ETH). On mainnet: roughly **~$30 USD in ETH** for the Forest Hollow entry toll, plus a little extra ETH for gas. See [Setup](../getting-started/setup.md).

### How do I earn $SHARE?

Place Merry Men in your Hideout. Every Robinhood Chain block, you accrue $SHARE equal to `(yourLoot / globalLoot) × emissionPerBlock`. It piles up automatically; you **claim** it whenever you like. See [Virtual Mining](../game-mechanics/virtual-mining.md).

### How do halvings work on a fast chain?

Emission is denominated **per real chain block**, not per second. It starts at **~0.135031 $SHARE/block** and **halves every 77,760,000 blocks (~90 days)** at Robinhood Chain's ~100ms block time. The engine reads `block.number` directly, so no scheduler is involved. See [Virtual Mining](../game-mechanics/virtual-mining.md).

### Why 21 million? Won't emission run out?

The **21,000,000** cap matches Bitcoin's. The initial emission rate was chosen so the infinite geometric halving series sums to exactly 21M — the emission schedule *is* the cap. Emission approaches zero but never quite issues past 21M.

### What happens to burned $SHARE?

It's gone — permanently removed from supply at the contract level. **75% of every $SHARE you spend** (recruits, upgrades) is *Given to the Poor* (burned); the other **25%** goes to the [War Chest](../game-assets-and-token/share-token.md) treasury. Burned tokens never return, so circulating supply trends down as the network grows.

### Is my progress onchain?

Yes — your Hideout, Merry Men, Loot Rate, and pending rewards are all on-chain state, owned by your wallet. Nothing sits on a private server that can be quietly edited. See [Architecture](../architecture/overview.md).

### What's the upgrade cooldown?

There's a **24-hour cooldown (864,000 blocks)** between Hideout upgrades. You can't rush multiple tiers in one session, so upgrading is a timing decision — start each cooldown the moment you can afford the next tier. See [Hideouts](../game-assets-and-token/hideouts.md).

### Can I lose my Merry Men?

Not by accident — no one can take them from you. The only thing that clears your run is **ascending a Legend rank**, which deliberately resets your progression in exchange for a permanent multiplier. That's your choice, not a risk. See [Legend Ranks](../game-mechanics/legend-ranks.md).

### What's Loot Rate, and why does mine change without me doing anything?

Loot Rate (LR) is your band's contribution to the network. Your *earnings* depend on your **share** of the global total — so when other players grow their bands, your share (and your per-block loot) shrinks even if your own LR is unchanged. This is the race.

### Why can't I recruit another outlaw?

Your Hideout is out of **slots** or **upkeep capacity**. Upgrade your Hideout, or remove a lower-tier Merry Man to free upkeep. See [Hideouts](../game-assets-and-token/hideouts.md).

### Should I stack one high-tier outlaw or diversify?

Stack. Higher tiers are more upkeep-efficient (more Loot Rate per unit of Upkeep), so filling a big Hideout with the best outlaw you can afford beats spreading across tiers. See the efficiency table in [The Merry Men](../game-assets-and-token/outlaws.md).

### What are ETH tolls, and are they recurring?

**One-time** payments at milestone Hideout tiers (1, 3, 5, 7, 9) and at every Legend rank. They're valued in USD via the **Chainlink ETH/USD** oracle and paid to the War Chest. Not subscriptions — you pay a toll once when you cross that milestone.

### How do referrals work?

Share your wallet address. Anyone who joins under it earns you **2.5% of their loot, forever, every block** — paid by the protocol, not skimmed from them. It's one-level and set-once. See [Referrals](../game-mechanics/referrals.md).

### What are Legend Ranks?

A **prestige** system — reset your run for a **permanent Loot Rate multiplier** that carries across every future run. **Legend Ranks are coming soon**; the full ranks, costs, and multipliers are revealed at launch. See the [Legend Ranks](../game-mechanics/legend-ranks.md) intro.

### Is there a premine, team allocation, or airdrop?

**One disclosed allocation:** 5% (1,050,000 $SHARE) is minted once at genesis to seed on-chain liquidity, and the LP is locked. The other **95% is mined by players** as block rewards at claim time. **No presale, no VC allocation, no team salary reserve, no airdrop, no staking yield, no inflation** — and the 21M hard cap covers both, so nothing mints past it.

### Which wallets work?

Any EVM wallet — MetaMask, Rainbow, Phantom, Robinhood Wallet, or any WalletConnect-compatible wallet. HOODLOOT never uses a proprietary wallet. See [Setup](../getting-started/setup.md).

### Is the block time really 100ms?

It's **reported** as ~100ms by secondary press and is consistent with the chain's Arbitrum Orbit stack, but isn't explicitly confirmed on official docs. HOODLOOT's emission is denominated in *blocks*, so the economics hold regardless — only the day/epoch estimates shift if the real block time differs. See [Robinhood Chain](../chain/robinhood-chain.md).

### Are the contracts audited?

An independent **security review is planned before mainnet launch**. Until then, treat HoodLoot as experimental software and never risk more than you're comfortable with. See the [Disclaimer](disclaimer.md).

### Where can I see network stats?

The global stats dashboard shows **Total Looted** (all $SHARE ever mined) and **Total Redistributed** (all $SHARE burned) in real time; `Circulating Supply = Total Looted − Total Redistributed`. See [$SHARE Token](../game-assets-and-token/share-token.md).
