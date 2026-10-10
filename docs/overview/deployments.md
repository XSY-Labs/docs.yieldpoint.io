# Contract Deployments

## v2 — YieldPoint (Current)

| Contract | Chain | Proxy Address |
|---|---|---|
| UTY | Base | `0xba515304d8153c4b162dc79f867e152df9c127eb` |
| yUTY | Base | `0xba515eed0119acb7cfe8fab3acd6b362f3ed5319` |

- **Hub Chain:** Base
- **Spoke Chains:** Avalanche, Katana
- **Launch Date:** 2026-03-26

## v1 — XSY (Deprecated)

- **Chains:** Avalanche, Katana
- **Launch Date:** June 2025
- **Status:** Deprecated. v1 contracts are legacy pre-rebrand contracts and are distinct from all v2 contracts.
- **Migration Path:** v1 token holders should migrate to v2 tokens via the UTY v1/v2 pools.

## Indexer Coverage Note

The `stg__donation` indexer on Base (`chain_id=8453`) covers **v2 transactions only**, from **2026-03-26** onwards. Historical v1 activity on Avalanche and Katana is not reflected in this dataset. Any performance metrics referencing a June 2025 inception date incorporate data from both v1 and v2 deployments and cannot be reproduced from the v2 indexer alone.
