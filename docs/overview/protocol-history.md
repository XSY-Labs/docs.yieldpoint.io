# Protocol History

## Deployment History

### v1 — XSY (Deprecated)

- **Name:** XSY
- **Status:** Deprecated
- **Launched:** June 2025
- **Chains:** Avalanche, Katana
- **Contracts:** Legacy pre-rebrand contracts, distinct from v2. These contracts are not the same as the v2 deployment.

### v2 — YieldPoint (Current)

- **Name:** YieldPoint
- **Status:** Current
- **Launched:** 2026-03-26
- **Hub Chain:** Base
- **Spoke Chains:** Avalanche, Katana
- **UTY Proxy (Base):** `0xba515304d8153c4b162dc79f867e152df9c127eb`
- **yUTY Proxy (Base):** `0xba515eed0119acb7cfe8fab3acd6b362f3ed5319`

## Migration

The migration exists to move v1 (XSY) token holders into v2 (YieldPoint) tokens. This is facilitated via UTY v1/v2 pools.

## Indexer Coverage & Metrics Caveat

> ⚠️ **Important:** The `stg__donation` table on `chain_id=8453` (Base) covers **v2 only**, starting from **2026-03-26**.
>
> "Since launch" references found in product briefs (e.g. 10.41%, 16.7% strategy returns, June 2025 inception) span **both v1 and v2 deployments** and **cannot be reconstructed from the v2 indexer alone**.
>
> Annualizing v2-only share price growth from inception (~78% as of May 2026) is heavily influenced by early-stage donation seeding and is **not a steady-state figure**. This number should not be presented as a representative ongoing yield.
