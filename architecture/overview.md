---
description: HoodLoot runs entirely onchain on Robinhood Chain — a set of smart contracts, fully verifiable.
---

# 🏗️ Architecture

HoodLoot runs **entirely onchain** on Robinhood Chain. There's no server holding your balance and no database anyone can quietly edit — the game *is* a set of smart contracts. Every recruit, deploy, claim, upgrade, and burn is a transaction you can see and verify onchain.

---

## The contracts

A handful of contracts run the whole game. Each is themed to what it does:

| Contract | What it does |
|---|---|
| **$SHARE** | The token (ERC-20, 21,000,000 hard cap). Only the mining engine can mint it, and 75% of every in-game spend is burned. |
| **Mining Engine** | The heart of the economy — accrues each block's $SHARE emission to every player by their share of the network Loot Rate, applies the halving schedule, and pays out claims. The only contract that can mint $SHARE. |
| **Outlaws (ERC-1155)** | The Merry Men as tokens — one per outlaw type. Yours to hold, trade, or deploy. |
| **Outlaw Registry** | Recruiting, staking outlaws onto hideout tiles, and each player's Loot Rate & Upkeep. Holds deployed outlaws in custody while they mine. |
| **Hideout Manager** | The nine hideouts — slots, upkeep caps, the upgrade cooldown, and the ETH tolls at milestone tiers. |
| **Price Oracle** | Reads the Chainlink ETH/USD feed so USD-valued tolls are charged in the right amount of ETH. |
| **Referrals** | One-level, set-once — routes 2.5% of a recruit's claims to whoever brought them in. |
| **Leaderboard** | The top players by Loot Rate. |

---

## Built to be trusted

- **Fully onchain & verifiable.** The contracts are verified on the block explorer — anyone can read the code and the live state. Nothing about the economy is hidden on a private server.
- **Fixed 21M supply.** The cap and the emission curve are hardcoded and immutable. No function can change them, and the token's `mint` is itself capped — nothing can inflate past 21,000,000 $SHARE.
- **No rug levers.** Prices, loot, upkeep, and emission are all immutable. The only owner control is an **emergency pause** (to freeze the game if an exploit appears) — it can't mint, move funds, or change a single number, and you can always withdraw your outlaws back to your wallet even while paused.
- **You custody your assets.** Outlaws are ERC-1155 tokens in your wallet; deploying one places it in the game's custody to mine, and you can pull it back any time.

---

## The chain

HoodLoot lives on **Robinhood Chain** — an EVM Layer-2 with **ETH gas**, **~100ms blocks**, and **Chainlink** price feeds from day one. It behaves like any standard EVM chain, so any normal wallet just works. See [Robinhood Chain](../chain/robinhood-chain.md).

---

## See Also

* [Virtual Mining](../game-mechanics/virtual-mining.md) — the reward math the mining engine implements
* [$SHARE Token](../game-assets-and-token/share-token.md) — the token, the burn, the cap
* [Robinhood Chain](../chain/robinhood-chain.md) — the chain HoodLoot runs on
* [Disclaimer](../reference/disclaimer.md) — HoodLoot is experimental software; play for the loot, not the ladder
