---
description: Recruit a Merry Man. Earn 2.5% of everything they loot — forever, every block.
---

# 🔗 Referrals

Every outlaw needs a band, and every band grows by word of mouth. HOODLOOT's referral system — **"Recruit a Merry Man"** — pays you a permanent cut of everyone you bring into Sherwood.

---

## How It Works

When a new player joins HOODLOOT using your wallet address as their referrer, you become their recruiter — permanently. From then on, **you earn 2.5% of everything they loot**, credited automatically every block they mine.

| Property | Detail |
|----------|--------|
| Referral bonus | **2.5%** of the referred player's rewards |
| Duration | **Forever** — for as long as they keep looting |
| Cadence | Credited **every block**, alongside their own accrual |
| Your effort | None — no claiming action on your end beyond your normal claim |
| Cost to them | **Zero** — the 2.5% is paid by the protocol, not skimmed from their loot |

{% hint style="success" %}
The 2.5% is a **bonus on top**, not a tax. Your recruit earns their full share; the referral credit is paid separately. You both come out ahead — the outlaw's creed exactly.
{% endhint %}

---

## The One-Level Model

Referrals in HOODLOOT are **single-level (set once)**:

* You earn only from the players **you directly recruit** — not from the players *they* recruit. There is no multi-tier pyramid.
* A player's referrer is **set once** and cannot be changed afterward. Whoever they join under is their recruiter for good.
* This is enforced by the `ReferralTracker` contract, which the `MiningEngine` credits at claim time.

{% hint style="info" %}
The one-level, set-once design keeps referrals a genuine growth reward rather than a chain letter. You benefit directly from the outlaws you personally bring in — and only them.
{% endhint %}

---

## How It Stacks

Referral income is **additive** to your own looting income. If you have a strong band *and* a network of recruits, both streams flow every block:

```
Your loot per block  =  (your Loot Rate share × emission)
                     +  2.5% × (each recruit's rewards that block)
```

There's no cap on how many Merry Men you can recruit, so a well-shared address can quietly out-earn a bigger band. Recruiting is the cheapest Loot Rate in the game — it costs you nothing and compounds with the network.

---

## How to Share Your Address

1. Copy your **wallet address** — this *is* your referral code. No separate signup.
2. Share it with anyone you want to bring into HOODLOOT.
3. When they connect and enter your address as their referrer, the link is set on-chain, once and forever.

{% hint style="warning" %}
Make sure recruits enter your address **before or at the moment they join** — the referrer is set once and cannot be reassigned later. If they join without it, that link can't be created retroactively.
{% endhint %}

---

## See Also

* [Gameplay Loop](../getting-started/gameplay-loop.md) — the loop referrals plug into
* [$SHARE Token](../game-assets-and-token/share-token.md) — the token your cut is paid in
* [Architecture](../architecture/overview.md) — the `ReferralTracker` contract
