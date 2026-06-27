# On-Chain Review Checklist

Status date: 2026-06-27

This checklist is for human reviewers using public read-only explorers, indexers, and market references. It does not require wallet connection, transaction signing, asset transfer, private keys, API keys, or credentials.

## Asset Metadata

| Field | Expected / page-displayed value | Evidence source | Status |
| --- | --- | --- | --- |
| ASA ID | 3169177585 | [asset identity proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) | Verified by public indexers |
| Asset name | ProfitNet | [asset identity proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) | Verified by public indexers |
| Unit name | PNET | [asset identity proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) | Verified by public indexers |
| Total supply | 100,000,000 PNET | [asset identity proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) | Verified by public indexers |
| Decimals | 6 | [asset identity proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) | Verified by public indexers |
| Raw total | 100,000,000,000,000 | [asset identity proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) | Verified by public indexers |
| Asset URL | https://testedprofit.com | [asset identity proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) | Verified as ASA URL field |
| Metadata hash | Not observed in captured indexer params | [asset identity proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) | Snapshot only |

## ASA Controls

| Field | Evidence source | Status |
| --- | --- | --- |
| Creator address | [asset identity proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) | Verified by public indexers |
| Manager address | [asset identity proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) | Verified current value as zero address |
| Reserve address | [asset identity proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) | Verified current value as zero address |
| Freeze address | [asset identity proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) | Verified current value as zero address |
| Clawback address | [asset identity proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) | Verified current value as zero address |
| Default frozen state | [asset identity proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) | Verified as `false` |
| Configuration transaction history | Explorer or indexer | Needs verification |

## Supply, Burns, and Locks

| Claim | Evidence needed | Status |
| --- | --- | --- |
| Burned supply shown as 8,180,000 PNET | Burn address, transaction set, or explorer/indexer evidence | Needs verification |
| Founder allocation shown as 25M PNET locked | Account, escrow, lock mechanism, or public proof | Needs on-chain verification |
| Strategic reserve shown as 15M PNET locked | Account, escrow, lock mechanism, or public proof | Needs on-chain verification |
| Major unlock shown as 25% supply lock, Sept 2026 | Lock mechanism and unlock date evidence | Needs on-chain verification |
| Circulating supply | Reconciled supply calculation and source data | Needs verification |

## Liquidity / Pool Review

| Item | Evidence needed | Status |
| --- | --- | --- |
| ALGO/PNET label | Pool ID, venue, assets, balances, and status | Needs on-chain verification |
| DDAO/PNET label | Pool ID, venue, assets, balances, and status | Needs on-chain verification |
| Burned LP vault labels | Account, pool token, burn transaction, or lock proof | Needs on-chain verification |
| Strategic partnership vault labels | Account, asset, lock proof, and source context | Needs on-chain verification |
| Vestige market snapshot | Dated screenshot or recorded public data | Needs verification |
| Allo asset reference | Dated screenshot or recorded public data | Needs verification |

## Evidence Record Template

| Evidence field | Value |
| --- | --- |
| Reviewer | Needs verification |
| Date and time checked | Needs verification |
| Source URL | Needs verification |
| Field checked | Needs verification |
| Observed value | Needs verification |
| Notes / discrepancy | Needs verification |

## Reviewer Safety

- Use public read-only sources.
- Do not connect a wallet.
- Do not sign transactions.
- Do not transfer assets.
- Do not disclose private screenshots, balances, credentials, session tokens, API keys, or internal dashboards.
