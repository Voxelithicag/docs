# Supported Venues

| Venue | Type | Reading method |
|-------|------|---------------|
| Uniswap v4 | Concentrated (singleton) | `extsload` on singleton |
| Uniswap v3 | Concentrated | `slot0()` + `liquidity()` |
| Ramses v3 | Concentrated | Same as v3 |
| Giga | Concentrated | Same as v3 |
| Up Exchange | Constant product | `getReserves()` |

All reads are batched into a single JSON-RPC call.

// updated: iteration 15

// updated: iteration 16
