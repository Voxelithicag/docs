# Architecture

Voxelithic is a liquidity aggregation layer for Robinhood Chain (EVM, chain id 4663).

## Components

### Contracts (on-chain)

Four stateless contracts:

- **VoxRouter** — multi-hop swaps through concentrated liquidity (v3-style)
- **VoxRouterV4** — execution through Uniswap v4 singleton lock pattern
- **VoxQuoter** — exact on-chain quoting for v3 paths
- **VoxQuoterV4** — quoting for v4 paths via `extsload`

### Book Engine (off-chain)

Client-side aggregation:

1. **Price discovery** — reads pool state via batched `eth_call`
2. **Route finding** — optimal path across venues
3. **Quote verification** — from the pools themselves, not from fitted curves

### App (frontend)

Direct wallet connection (EIP-1193). No backend holds funds.

## Data flow

```
Wallet (EIP-1193) → App → Book Engine
    ├→ eth_call (pool state)
    ├→ VoxQuoter/V4 (exact quotes)
    └→ eth_getLogs (fills)
    → VoxRouter/V4 (execution) → DEX pools (settlement)
```

## Security model

- Contracts are stateless
- `minOut` verified on-chain
- Protocol fee deducted before the check
- No admin keys, no upgradeability, no pause
