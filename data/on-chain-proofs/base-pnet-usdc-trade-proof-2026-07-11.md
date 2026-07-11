# Base PNET/USDC Trade Proof — 2026-07-11

Status: successful buy verified; successful sell not found in the reviewed history

Capture date: 2026-07-11

Network: Base mainnet, chain ID `8453`

Token: ProfitNet (`PNET`), `0xe1F7F585f458cB6AFFCEE2286b8482523B19ee5a`

Pool: Uniswap v4 PNET/USDC seed pool `0xff481004f38fc7db43f3e3b47f6ad3e155482a00866d709d89700d303b0b4f3a`

Review horizon: all `47` PNET `Transfer` events through block `48,488,235` at `2026-07-11T10:30:17Z`; pool logs checked through block `48,488,596` at `2026-07-11T10:42:19Z`

## Verified Buy Transaction

| Field | Observed value |
| --- | --- |
| Transaction | `0x9dcadf472eb94e69033a40d6b1e2079187ee75c2799819bce1a3e1a79d80f3ab` |
| BaseScan | https://basescan.org/tx/0x9dcadf472eb94e69033a40d6b1e2079187ee75c2799819bce1a3e1a79d80f3ab |
| Blockscout | https://base.blockscout.com/tx/0x9dcadf472eb94e69033a40d6b1e2079187ee75c2799819bce1a3e1a79d80f3ab |
| Status | Success |
| Block | `48,469,204` |
| Timestamp | `2026-07-10T23:55:55Z` |
| Transaction sender | `0x0e77610e9f13062c2eaa709ef1c59B8C22E549c9` |
| Verified router | Uniswap v4 Universal Router, `0x6fF5693b99212Da76ad316178A184AB56D299b43` |
| PoolManager | `0x498581fF718922c3f8e6A244956aF099B2652b2b` |
| Routed input | `0.00000002219 WETH` converted to `39` raw USDC units (`0.000039 USDC`) |
| PNET output | `6.755115987102991431 PNET` |
| PNET recipient | `0xa568a959Aa287F9004DBe9C5402b581083A0dc6f` |

The PoolManager emitted a `Swap` event for the PNET/USDC pool with `amount0 = -39` and `amount1 = 6755115987102991431`. USDC is currency 0 and PNET is currency 1 for this pool. The PNET contract then emitted a `Transfer` of the same PNET amount from the PoolManager to the recipient. Together with the successful transaction status and routed WETH input, these events establish a completed buy-direction swap.

## Sell Search

The review reconstructed all `47` PNET `Transfer` events available through the stated review horizon, isolated `16` transactions involving the Uniswap v4 PoolManager, and decoded the `Swap` events for the specified pool.

The pool emitted `11` decoded `Swap` events:

- `11` had negative USDC delta and positive PNET delta, consistent with USDC input and PNET output;
- `0` had positive USDC delta and negative PNET delta, which would evidence PNET input and USDC output.

Across those events, the observed totals were `0.056660 USDC` input and `10,436.9210527254618683 PNET` output.

No successful sell-direction swap was found in that reviewed history. This is an open evidence item, not evidence that a sell cannot execute.

## Method

1. Retrieved the Base PNET transfer history from Blockscout's public account-token-transfer API.
2. Selected transactions in which the PNET sender or recipient was the Uniswap v4 PoolManager.
3. Retrieved and decoded each transaction's logs from Blockscout.
4. Matched only `Swap` events whose pool ID equals `0xff481004f38fc7db43f3e3b47f6ad3e155482a00866d709d89700d303b0b4f3a`.
5. Classified direction from the USDC/PNET signed deltas and cross-checked the selected buy against its ERC-20 transfers and successful receipt.

Public sources:

- https://base.blockscout.com/api?module=account&action=tokentx&contractaddress=0xe1F7F585f458cB6AFFCEE2286b8482523B19ee5a&page=1&offset=10000&sort=asc
- https://base.blockscout.com/api/v2/transactions/0x9dcadf472eb94e69033a40d6b1e2079187ee75c2799819bce1a3e1a79d80f3ab
- https://base.blockscout.com/api/v2/transactions/0x9dcadf472eb94e69033a40d6b1e2079187ee75c2799819bce1a3e1a79d80f3ab/logs
- https://base.blockscout.com/api/v2/transactions/0x9dcadf472eb94e69033a40d6b1e2079187ee75c2799819bce1a3e1a79d80f3ab/token-transfers

## Interpretation and Limits

This proof supports only the narrow claim that a buy-direction swap completed through the existing PNET/USDC seed pool. It does not establish a successful sell, independent or organic demand, deep liquidity, low price impact, warning removal, auction completion, LP migration, or LP lock execution. The transaction sender's and recipient's beneficial ownership were not established, so the transaction must not be counted as an independent buyer without separate evidence.

The review is bounded by the stated block and timestamp. Later transactions require a refreshed review.
