# Contract Reference

## Deployed addresses

| Contract | Address | Verified |
|----------|---------|----------|
| VoxRouter | `0x87cD…2e64` | [Blockscout](https://robinhoodchain.blockscout.com/address/0x87cD67C1C4adFac2BF8e1B2f30f3802a70712e64) |
| VoxQuoter | `0x9616…bE1B` | [Blockscout](https://robinhoodchain.blockscout.com/address/0x9616D53a9B55d82e56c6c08Ca7E2beD6D7e1bE1B) |
| VoxRouterV4 | `0x290b…aab5` | [Blockscout](https://robinhoodchain.blockscout.com/address/0x290b9b46308f7a3B80A5F62214B426d3bfAfaab5) |
| VoxQuoterV4 | `0x5858…d4F` | [Blockscout](https://robinhoodchain.blockscout.com/address/0x5858F06894623eF4862103A747074E5AA3436d4F) |

## Error codes

| Error | Meaning |
|-------|---------|
| `VoxSlippage(got, minOut)` | Output less than signed minimum |
| `VoxFeeTooHigh(bps)` | Fee exceeds 30 bps ceiling |
| `PartialFill(taken, requested)` | Pool did not consume full input |
| `HopCountExceeded` | More than 3 hops in a single route |

// updated: iteration 8

// updated: iteration 12
