# Tokenomics

Snapshot date: 2026-06-27

This file records tokenomics claims as dated public-page snapshots. It does not treat page-displayed lock, vault, allocation, or market information as on-chain verified unless a public explorer, indexer, or other auditable source is recorded with the observed value.

Primary snapshot: [data/tokenomics/tokenomics-snapshot-2026-06-27.md](../data/tokenomics/tokenomics-snapshot-2026-06-27.md)

## Page-Displayed Asset Facts

| Field | Page-displayed value | Source | Dossier status |
| --- | --- | --- | --- |
| ASA ID | 3169177585 | testedprofit tokenomics page, PNET page; public indexers | Verified by public indexers in [asset identity proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) |
| Total supply | 100,000,000 PNET | testedprofit tokenomics page; public indexers | Verified by public indexers in [asset identity proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) |
| Burned supply shown | 8,180,000 PNET | testedprofit tokenomics page | Needs on-chain verification |
| Decimals | 6 | testedprofit tokenomics page; public indexers | Verified by public indexers in [asset identity proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) |
| Founder allocation shown | 25M PNET locked | testedprofit tokenomics page | Needs on-chain lock verification |
| Strategic reserve shown | 15M PNET locked | testedprofit tokenomics page | Needs on-chain lock verification |
| Major unlock shown | 25% supply lock, Sept 2026 | testedprofit tokenomics page | Needs on-chain lock verification |

## Supply Snapshot

| Item | Page-displayed value | Dossier status |
| --- | --- | --- |
| Total supply | 100,000,000 PNET | Verified by public indexers |
| Burned supply shown | 8,180,000 PNET | Needs on-chain verification |
| Remaining supply after displayed burn | 91,820,000 PNET | Derived from page-displayed values, Needs on-chain verification |
| Decimals | 6 | Verified by public indexers |
| Raw total | 100,000,000,000,000 raw units | Verified by public indexers |

## Allocation and Lock Snapshot

These rows are page-displayed claims only. They should not be described as verified lockups until the underlying accounts, escrow mechanisms, pool records, or explorer/indexer data have been recorded.

| Label shown | Page-displayed amount / description | Page-displayed status | Dossier status |
| --- | --- | --- | --- |
| Founder Allocation | 25M PNET | Locked | Needs on-chain lock verification |
| Strategic Reserve | 15M PNET | Locked | Needs on-chain lock verification |
| ALGO/PNET Liquidity Pool | Label shown; amount not captured in accessible page text | Liquidity pool | Needs on-chain LP verification |
| DAO LP DDAO/PNET Ecosystem Pair | Label shown; amount not captured in accessible page text | Liquidity pair | Needs on-chain LP verification |
| MAX 1 Partner Allocation | Partner allocation label shown; amount not captured in accessible page text | Locked | Needs on-chain lock verification |
| MAX 2 Partner Allocation | Partner allocation label shown; amount not captured in accessible page text | Locked | Needs on-chain lock verification |

## Vault and Partner Labels

The testedprofit tokenomics page displays LP/vault and partner labels. This dossier records the labels for reference only. Each listed lock, vault, burn, LP position, or partnership status remains `Needs on-chain verification`.

| Group | Label shown | Dossier status |
| --- | --- | --- |
| Burned LP vault | PNET-ELESQ | Needs on-chain verification |
| Burned LP vault | PNET-JIM | Needs on-chain verification |
| Burned LP vault | PNET-THC | Needs on-chain verification |
| Burned LP vault | USDC-PNET | Needs on-chain verification |
| Burned LP vault | BLOB-PNET | Needs on-chain verification |
| Burned LP vault | DERS-PNET | Needs on-chain verification |
| Burned LP vault | PNET-AURA | Needs on-chain verification |
| Burned LP vault | PNET-CRASHOUT | Needs on-chain verification |
| Burned LP vault | PNET-XDB | Needs on-chain verification |
| Strategic partnership vault | Public-page partner lock label | Needs on-chain verification |
| Strategic partnership vault | BONEZ Liquidity | Needs on-chain verification |
| Strategic partnership vault | 69420 Liquidity | Needs on-chain verification |
| Strategic partnership vault | DeckardCain Partner | Needs on-chain verification |
| Strategic partnership vault | AETF Partner | Needs on-chain verification |
| Strategic partnership vault | Tife Partner | Needs on-chain verification |

## Verification Requirements

Before any row is upgraded from `Needs on-chain verification`, add evidence that includes:

| Evidence field | Requirement |
| --- | --- |
| Source | Explorer, indexer, official page, dated archive, or transaction reference |
| Date checked | Calendar date of review |
| Observed value | Exact value observed at source |
| Method | Plain-language verification method |
| Reviewer | Name or handle of reviewer |

## Supply Methodology Addendum

Future tokenomics snapshots should separate direct burns, reviewed locks, and inaccessible-account claims. These categories should not be merged unless a methodology, public evidence, and reviewer sign-off are recorded.

| Category | Treatment | Dossier status |
| --- | --- | --- |
| Direct burned supply | Count only when supported by public explorer or indexer evidence | Needs on-chain verification |
| Inaccessible-account supply | Track separately from direct burn amounts when an account is claimed to be unavailable | Needs disclosure and human review |
| Opt-out-to-creator loss | Do not describe as a verified burn method until chain behavior, account status, and disclosure wording are reviewed | Needs on-chain and disclosure review |
| Locked supply | Count only when lock address, escrow, app, or contract evidence is recorded | Needs on-chain lock verification |
| Circulating supply | Calculate only from the approved methodology version and source records | Needs methodology approval |

Related hardening spec: [docs/17_PHASE_3_REVENUE_TOKENOMICS_HARDENING_SPEC.md](17_PHASE_3_REVENUE_TOKENOMICS_HARDENING_SPEC.md).

Current supply methodology: [data/on-chain-proofs/supply-methodology.md](../data/on-chain-proofs/supply-methodology.md).

## Public Claims Guardrails

Tokenomics pages can contain marketing language. This repo should only preserve neutral, dated facts and should not frame PNET as an investment, income source, managed strategy, or expected-return product.

See [docs/06_PUBLIC_CLAIMS_POLICY.md](06_PUBLIC_CLAIMS_POLICY.md).
