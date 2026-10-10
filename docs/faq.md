# Frequently Asked Questions

## General

### What is YieldPoint?

YieldPoint is a delta-neutral yield protocol built around UTY, xUTY, and yUTY.

---

## APY & Yield

### Why do I see different APY numbers quoted for yUTY (e.g. 16 % vs 9–10 %)?

There are **two distinct APY figures** for yUTY, and they are frequently confused:

| Figure | Name | Value | What it represents |
|---|---|---|---|
| ~16.7 % | **Strategy APY** | 16.7 % (June 2025 – Feb 2026) | Gross basis trade return on Trade NAV, computed off-chain before insurance fund retention |
| ~9 % | **Distributed APY** | 9 % (as of 2026-05-18) | Share price growth actually received by yUTY vault holders, verifiable on-chain |

These numbers **should never be averaged or used interchangeably**.

### Why is the Distributed APY lower than the Strategy APY?

Not all UTY is staked into yUTY. Some holders use **xUTY** (to earn points) or hold raw UTY for collateral utility. PnL earned on unstaked UTY is retained by the **insurance fund**, which allows the protocol to scale TVL more safely. The gap is intentional — it is not a fee leak or inefficiency.

```
Strategy APY (16.7 %)  =  Distributed APY (9 %)  +  Insurance Fund Retention
```

### How can I verify the Distributed APY on-chain?

Call `yUTY.convertToAssets(1e18)` to read the current share price, or inspect the `stg__donation.new_share_price` event progression in the vault contract's history.

---

## Tokens

### What is the difference between UTY, xUTY, and yUTY?

- **UTY** — base token; can be used as collateral or staked.
- **xUTY** — points-accruing alternative; holders forgo Distributed APY in favour of protocol points.
- **yUTY** — yield-bearing vault; holders earn Distributed APY (currently 9 %) as share price appreciation.
