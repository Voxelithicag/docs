# Integration Guide

## Reading prices

```javascript
import { createEngine } from '@voxelithic/book-engine'

const engine = createEngine({ rpcUrl: 'https://rpc.mainnet.chain.robinhood.com' })
const book = await engine.readBook('SPY')
// book.venues — array of { venue, price, depth, liquidity }
// book.best — best bid and ask
```

## Finding routes

```javascript
import { bestRoute } from '@voxelithic/book-engine/route'

const route = await bestRoute({
  tokenIn: TOKENS.USDG.address,
  tokenOut: TOKENS.SPY.address,
  amountIn: 100_000000n, // 100 USDG (6 decimals)
})
// route.family — 'v3' or 'v4'
// route.hops — execution path
```

## Executing swaps

```javascript
import { execute } from '@voxelithic/app/swap'
const txHash = await execute(route, tokenInAddr, tokenOutAddr)
```

## Verifying fills

```bash
node node_modules/@voxelithic/verify/src/verify-fill.js 0x<hash>
```

// updated: iteration 20
