# yUTY Overview

yUTY is the yield-bearing vault token of the YieldPoint protocol. Depositing UTY into the yUTY vault entitles holders to a share of the delta-neutral basis trade returns.

## APY at a Glance

| Metric | Value | Description |
|---|---|---|
| **Strategy APY** | 16.7 % | Gross basis trade return on Trade NAV (off-chain, June 2025 – Feb 2026), before insurance fund retention |
| **Distributed APY** | 9 % (as of 2026-05-18) | Share price growth received by yUTY holders, verifiable on-chain |

> ⚠️ **These two figures are not interchangeable.** Strategy APY (16.7 %) reflects gross hedge performance. Distributed APY (9 %) is what yUTY holders actually earn. The gap is retained by the insurance fund from PnL on UTY that is not staked into yUTY (e.g. held as xUTY for points or raw UTY for collateral). This is by design and strengthens protocol safety.

## How yUTY Works

- Deposit UTY → receive yUTY vault shares.
- Share price grows over time, tracked via `convertToAssets()` on-chain.
- Yield derives from the protocol's delta-neutral basis trade strategy.
- Not all UTY is staked: holders may instead use **xUTY** (points programme) or hold raw UTY for collateral purposes. PnL attributable to unstaked UTY flows to the insurance fund.

## Further Reading

- [APY Methodology](./apy-methodology.md) — full explanation of Strategy APY vs Distributed APY and the gap between them.
- [xUTY](../xuty/overview.md) — points-based alternative to yUTY staking.
- [Insurance Fund](../insurance-fund/overview.md) — how retained PnL scales protocol TVL safely.
