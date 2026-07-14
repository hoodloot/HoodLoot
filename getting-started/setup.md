---
description: Connect your EVM wallet, pay your entry toll, and start looting in under five minutes.
---

# ⚡ Setup

Getting into HOODLOOT takes under five minutes. You need a wallet, a small amount of ETH, and the hunger to rob the block.

---

## Requirements

{% hint style="info" %}
Before you begin, make sure you have:

* ✅ A modern web browser (Chrome, Firefox, Brave)
* ✅ **Any EVM wallet** — MetaMask, Rainbow, or any WalletConnect-compatible wallet
* ✅ **\~$30 USD in ETH** on Robinhood Chain for your Forest Hollow entry toll
{% endhint %}

> **Robinhood Chain** is an Arbitrum-based EVM Layer-2 with ~100ms blocks and a native gas token of ETH. Any standard wallet works — HOODLOOT never uses a proprietary wallet. You will need it to sign transactions and claim your $SHARE rewards.

### Add Robinhood Chain to your wallet

Robinhood Chain is not in most wallets' default network list, so you add it manually once. In MetaMask: **Settings → Networks → Add a network → Add a network manually**, then enter the fields below. Any EVM wallet (Rainbow, Phantom, Robinhood Wallet, or any WalletConnect wallet) accepts the same parameters.

{% tabs %}
{% tab title="Testnet (start here)" %}
| Field | Value |
|-------|-------|
| Network name | `Robinhood Chain Testnet` |
| Chain ID | `46630` |
| RPC URL | `https://rpc.testnet.chain.robinhood.com` |
| Currency symbol | `ETH` |
| Block explorer | `https://explorer.testnet.chain.robinhood.com` |

Testnet ETH costs nothing — grab some from the **faucet** (next step). Build and learn here before you spend anything real.
{% endtab %}

{% tab title="Mainnet" %}
| Field | Value |
|-------|-------|
| Network name | `Robinhood Chain` |
| Chain ID | `4663` |
| RPC URL | `https://rpc.mainnet.chain.robinhood.com` |
| Currency symbol | `ETH` |
| Block explorer | `https://robinhoodchain.blockscout.com` |

Mainnet gas is real ETH. Bridge or obtain ETH on Robinhood Chain via the canonical Arbitrum bridge before you play.
{% endtab %}
{% endtabs %}

{% hint style="info" %}
The **chain ID must match exactly** — `46630` for testnet, `4663` for mainnet. A mismatched chain ID causes signature and "wrong network" errors. The public RPCs are rate-limited; for heavy use, an Alchemy `robinhood-testnet` / `robinhood-mainnet` endpoint is smoother.
{% endhint %}

### Get testnet ETH from the faucet

On testnet you need a little ETH to pay for gas and your entry toll — and it's free.

1. Go to **`https://faucet.testnet.chain.robinhood.com/`**
2. Connect your wallet or paste your address
3. Request testnet ETH (the faucet also dispenses test Stock Tokens; you only need the ETH)

{% hint style="warning" %}
Testnet ETH has **no real value** and only works on chain ID `46630`. It cannot be bridged to or spent on mainnet. The faucet is also mirrored on the Chainlink and QuickNode faucets if the primary is dry.
{% endhint %}

---

## Step 1 — Connect Your Wallet

1. Head to **hoodloot.com**
2. Click **CONNECT WALLET** in the top of the interface
3. Approve the connection in your wallet (MetaMask, Rainbow, WalletConnect)

Once connected, your address, $SHARE balance, and looting stats will appear in the dashboard.

---

## Step 2 — Claim the Forest Hollow

Your first hideout tier is the **Forest Hollow** — 4 outlaw slots, 28 U upkeep cap.

1. Click **UPGRADE** to open the hideout upgrade panel
2. Select **Forest Hollow** and approve the transaction
3. Pay the entry toll: **\~$30 USD in ETH** sent to the War Chest treasury

{% hint style="success" %}
Once confirmed on-chain, your Forest Hollow is live. **You are in the game.**
{% endhint %}

---

## Step 3 — Recruit Your First Outlaw

Your first Merry Man — the **Ragged Peasant** — is completely free.

1. Click any empty slot in your Forest Hollow
2. Select **Ragged Peasant** from the roster
3. Confirm — it costs **0 $SHARE** and is placed immediately

{% hint style="success" %}
Your Ragged Peasant starts looting the moment it is placed. Every Robinhood Chain block (\~100ms), you accumulate a share of $SHARE rewards based on your Loot Rate.
{% endhint %}

---

## What's Next

Once you are in and looting, the goal is simple: grow your Loot Rate, upgrade your hideout, and climb the leaderboard.

| Action | Why |
|--------|-----|
| **Claim $SHARE** | Collect your pending rewards any time |
| **Recruit more outlaws** | More Merry Men = more Loot Rate = more $SHARE per block |
| **Upgrade your hideout** | Unlock more slots and a higher upkeep cap |
| **Recruit a Merry Man (referral)** | Earn 2.5% of their rewards forever |

{% hint style="warning" %}
**Halvings matter.** The emission rate halves every 77,760,000 blocks (\~90 days). Outlaws who upgrade early — before each halving cuts emissions — come out ahead. Do not wait.
{% endhint %}

For the full step-by-step growth loop, see [Gameplay Loop](gameplay-loop.md).

---

## 🔧 Troubleshooting

{% tabs %}
{% tab title="Wrong network" %}
**"Wrong network" / signature errors.** Your wallet is on a different chain than the game. Switch to Robinhood Chain and confirm the **chain ID** is exactly `46630` (testnet) or `4663` (mainnet). If you added the network with a wrong chain ID, delete it and re-add it with the correct value.
{% endtab %}

{% tab title="Faucet won't fund me" %}
**Faucet returns nothing.** The primary faucet is rate-limited per address per day. Wait, or use a mirror — the same testnet ETH is available via the Chainlink and QuickNode faucets. Make sure your wallet is actually on the **testnet** (chain ID `46630`); the faucet only funds testnet addresses.
{% endtab %}

{% tab title="Transaction stuck / failed" %}
**A claim or upgrade won't confirm.** The public RPC may be rate-limited or lagging. Give it a moment and retry, switch your RPC URL to an Alchemy endpoint, or check the transaction on the explorer (`explorer.testnet.chain.robinhood.com` / `robinhoodchain.blockscout.com`). If an upgrade reverts, you may be inside the **864,000-block (~24h) cooldown** or missing the ETH toll for that tier.
{% endtab %}

{% tab title="Not enough ETH for gas" %}
**"Insufficient funds."** Gas on Robinhood Chain is paid in **ETH**, not $SHARE. On testnet, top up from the faucet. On mainnet, bridge ETH in via the canonical Arbitrum bridge. Keep a small ETH buffer beyond your toll for gas.
{% endtab %}

{% tab title="Can't recruit an outlaw" %}
**Recruit is blocked.** Your Hideout is out of **slots** or **upkeep capacity**. Upgrade your Hideout, or remove a lower-tier Merry Man to free up the upkeep the new one needs. See [Hideouts](../game-assets-and-token/hideouts.md).
{% endtab %}
{% endtabs %}
