# Contract Reference

## Deployed addresses

| Contract | Address | Verified |
|----------|---------|----------|
| VoxRouter | `0x87cD7EbE8c213455e5e5a8554657D5f294a82e64` | [Blockscout](https://robinhoodchain.blockscout.com/address/0x87cD7EbE8c213455e5e5a8554657D5f294a82e64) |
| VoxQuoter | `0x9616627E871c96e38cb21b9551F62Ed93366bE1B` | [Blockscout](https://robinhoodchain.blockscout.com/address/0x9616627E871c96e38cb21b9551F62Ed93366bE1B) |
| VoxRouterV4 | `0x290b9b46308f7a3B80A5F62214B426d3bfAfaab5` | [Blockscout](https://robinhoodchain.blockscout.com/address/0x290b9b46308f7a3B80A5F62214B426d3bfAfaab5) |
| VoxQuoterV4 | `0x5858F06894623eF4862103A747074E5AA3436d4F` | [Blockscout](https://robinhoodchain.blockscout.com/address/0x5858F06894623eF4862103A747074E5AA3436d4F) |

## Error codes

| Error | Meaning |
|-------|---------|
| `VoxSlippage(got, minOut)` | Output less than signed minimum |
| `VoxFeeTooHigh(bps)` | Fee exceeds 30 bps ceiling |
| `PartialFill(taken, requested)` | Pool did not consume full input |
| `HopCountExceeded` | More than 3 hops in a single route |
