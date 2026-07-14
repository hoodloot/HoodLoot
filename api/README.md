# 🔌 HoodLoot API

The HoodLoot backend exposes a small read-only REST API over Robinhood Chain data — network state, per-wallet stats, the leaderboard, and the ETH/USD price used for tolls.

## Public endpoints

| Method | Path | Returns |
|---|---|---|
| `GET` | `/health` | Liveness, mock/live mode, last block seen |
| `GET` | `/api/global` | Emission, halving, supply, burn, network Loot Rate |
| `GET` | `/api/stats/{address}` | A wallet's tier, Loot Rate, pending $SHARE, roster |
| `GET` | `/api/leaderboard` | Top-20 wallets by Loot Rate |
| `GET` | `/api/price` | ETH/USD (Chainlink) used to value the tolls |

All responses are JSON. Large integers (wei, block numbers) are returned as **strings** to preserve precision.

### Example

```bash
curl https://hoodloot.com/api/global
```

```json
{
  "blockNumber": "888210",
  "emissionPerBlockWei": "405092592592592640",
  "totalSupplyWei": "8625000000000000000000000",
  "totalBurnedWei": "10125000000000000000000000",
  "ethPriceUsd": 3000
}
```

## Machine-readable spec

The full contract — every endpoint, parameter, and response schema — lives in the OpenAPI 3.0 spec: [`hoodloot-api.yaml`](hoodloot-api.yaml).
