---
description: Robinhood's own EVM Layer-2 — fast, ETH-gassed, and the natural home for $SHARE.
---

# ⛓️ Robinhood Chain

HOODLOOT lives on **Robinhood Chain**, Robinhood's own Ethereum Layer-2. This page covers what the chain is, who's behind it, why the game runs here, and the exact network parameters you need to connect.

{% hint style="info" %}
Some of what's publicly known about Robinhood Chain is well-sourced (official docs and newsroom); a few widely-cited details come from secondary press and are flagged **UNCERTAIN** below. We keep those flags so you know what's confirmed and what's directional.
{% endhint %}

---

## What It Is

Robinhood Chain is a **permissionless, EVM-compatible Ethereum Layer-2**, built on the **Arbitrum Orbit / "Arbitrum Dedicated Blockchains"** stack operated by **Offchain Labs**. It settles to Ethereum L1, uses **Ethereum blobs** for data availability, and — crucially for a game — uses **ETH as its native gas token**. Contracts deploy unmodified in Solidity or Vyper, exactly as on any EVM chain.

Its purpose is to bring Robinhood's brokerage-style assets — especially **tokenized stocks and real-world assets (RWAs)** — onchain for **24/7 trading, self-custody, and DeFi composability** across 120+ countries (the tokenized-stock product excludes US persons for regulatory reasons). The chain itself, however, is open: anyone can connect an EVM wallet and deploy — which is exactly what HOODLOOT does.

---

## Who's Behind It

| Party | Role |
|-------|------|
| **Robinhood Markets, Inc.** | Issuer / sponsor of the chain. Mission: *"democratize finance for all."* |
| **Vlad Tenev** | Chairman & CEO, co-founder; principal voice of Robinhood's tokenization thesis. |
| **Johann Kerbrat** | SVP & GM, Crypto and International; primary spokesperson for Robinhood Chain. |
| **Offchain Labs** | Builder of Arbitrum; provides the Orbit stack the chain runs on. |
| **Robinhood Digital Assets, LLC (RHDA)** | The entity that offers the chain (a software provider, not a regulated financial service). |
| **Robinhood Assets (Jersey) Limited ("RHJ")** | Issuer of the tokenized Stock Tokens. |

The public **testnet launched February 2026** (chain ID `46630`); the **mainnet launched July 1, 2026** (chain ID `4663`), announced at Robinhood's *"The World is Flat"* keynote in London.

---

## The Mission & Vision

Robinhood's stated mission is to **"democratize finance for all."** Robinhood Chain extends that from democratized *access to investing* into democratized *ownership and participation in open, onchain finance*, along three linked ideas:

1. **Tokenization thesis** — most financial instruments will migrate onchain as tokenized assets.
2. **"The world is flat"** — removing geographic barriers so anyone (outside the US, for stock tokens) can access US-equity exposure and DeFi.
3. **Onchain finance** — merging traditional finance and DeFi into one always-on, composable, self-custodial system.

> *"We're bringing the best of traditional finance and DeFi together, and in doing so, expanding financial ownership to every corner of the globe."*
> — **Johann Kerbrat**, Robinhood Chain mainnet launch, July 1, 2026

---

## Why HOODLOOT Lives Here

The pun is the thesis. **$SHARE** is both a *share* (a stock) and *sharing* the wealth — and Robinhood's *"democratize finance for all"* mission is the Robin Hood folk tale in a fintech suit. HOODLOOT is the native, playable expression of "take from the concentrated, give to the many."

Beyond theme, the chain is a great technical fit:

* **ETH gas + full EVM compatibility** — any standard wallet (MetaMask, Rainbow, Phantom, Robinhood Wallet, any WalletConnect wallet) works out of the box.
* **Fast blocks** — the per-block loot loop feels arcade-instant. HOODLOOT's emission is denominated *per real chain block*, calibrated to the chain's block time (see [Virtual Mining](../game-mechanics/virtual-mining.md)).
* **Chainlink from launch** — the ETH tolls in HOODLOOT are USD-valued and priced via the Chainlink ETH/USD feed.
* **Uniswap from launch** — $SHARE can trade on the chain's native AMM.

---

## Network Parameters

Add the network to your wallet with these exact values. Gas is paid in **ETH** on both networks.

{% tabs %}
{% tab title="Testnet" %}
| Field | Value | Confidence |
|-------|-------|:----------:|
| Network name | `Robinhood Chain Testnet` | FACT |
| Chain ID | `46630` | FACT |
| RPC URL | `https://rpc.testnet.chain.robinhood.com` | FACT |
| WebSocket feed | `wss://feed.testnet.chain.robinhood.com` | FACT |
| Currency symbol | `ETH` | FACT |
| Block explorer | `https://explorer.testnet.chain.robinhood.com` | FACT |
| Faucet | `https://faucet.testnet.chain.robinhood.com/` | FACT |

The faucet dispenses free testnet ETH (and test Stock Tokens); it's also mirrored on the Chainlink and QuickNode faucets.
{% endtab %}

{% tab title="Mainnet" %}
| Field | Value | Confidence |
|-------|-------|:----------:|
| Network name | `Robinhood Chain` | FACT |
| Chain ID | `4663` | FACT |
| RPC URL | `https://rpc.mainnet.chain.robinhood.com` | FACT |
| WebSocket feed | `wss://feed.mainnet.chain.robinhood.com` | FACT |
| Currency symbol | `ETH` | FACT |
| Block explorer | `https://robinhoodchain.blockscout.com` | FACT |

Obtain ETH on mainnet via the canonical Arbitrum bridge. Public RPCs are rate-limited; Alchemy `robinhood-mainnet` endpoints are recommended for heavy use.
{% endtab %}
{% endtabs %}

---

## What's Confirmed vs. Uncertain

| Detail | Status |
|--------|:------:|
| EVM-compatible Ethereum L2 on Arbitrum Orbit, settling to Ethereum | **FACT** |
| Native gas token is ETH; data availability via Ethereum blobs | **FACT** |
| Chain IDs `46630` (testnet) / `4663` (mainnet), RPCs, explorer, faucet | **FACT** |
| Chainlink, Uniswap, Alchemy, BitGo, Blockscout, Morpho integrations | **FACT** |
| Tokenized stocks issued by RHJ; excludes US persons | **FACT** |
| **~100 ms block time** | **UNCERTAIN** — reported by secondary press (thirdweb), consistent with Orbit, but not explicitly confirmed on official docs |
| Early metrics ($570M launch-day volume, ~4M first-week txns, TVL figures) | **UNCERTAIN** — recent crypto press, lightly cross-checked |
| ERC-4337 account abstraction, first-come-first-served sequencing | **UNCERTAIN** — press |
| Agentic "Trading MCP" AI trading | **FORWARD-LOOKING** — announced "coming soon" |

{% hint style="warning" %}
HOODLOOT's emission math is denominated in **blocks**, not seconds — so the game stays economically correct even if the real block time differs from the reported ~100ms. Only the day/epoch *estimates* in the docs shift if the block time is different. See [Virtual Mining](../game-mechanics/virtual-mining.md).
{% endhint %}

---

## See Also

* [Setup](../getting-started/setup.md) — add the network and get testnet ETH
* [Virtual Mining](../game-mechanics/virtual-mining.md) — how the block time feeds emission
* [Architecture](../architecture/overview.md) — how HOODLOOT deploys onto the chain
