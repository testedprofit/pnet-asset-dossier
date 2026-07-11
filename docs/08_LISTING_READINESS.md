# Listing Readiness

Status date: 2026-06-27

This document is a public-review package for listing diligence, ecosystem partner review, and community verification. It is not a listing application, exchange endorsement, investment document, trading guide, or guarantee of venue support.

## Readiness Summary

| Area | Current status | Next action |
| --- | --- | --- |
| Asset identity | Page-displayed facts recorded | Confirm against on-chain asset metadata |
| ASA control fields | Not yet verified | Record creator, manager, reserve, freeze, and clawback from explorer/indexer |
| Supply and decimals | Page-displayed facts recorded | Confirm total, raw total, and decimals on-chain |
| Circulating, burned, locked claims | Page-displayed claims recorded | Verify burn and lock mechanics on-chain |
| Liquidity / pool references | Public labels recorded | Verify pool IDs, assets, balances, and venue data |
| Utility summary | No utility claim verified | Keep utility neutral until source evidence is recorded |
| Public links | Recorded in references | Add explorer/indexer evidence links |
| Risk disclosures | Present | Keep disclaimers current |
| Claims policy | Present | Enforce before public claims are added |
| CoinGecko / CoinMarketCap readiness | Build targets documented | Complete gates in [23_COINGECKO_CMC_BUILD_TARGETS.md](23_COINGECKO_CMC_BUILD_TARGETS.md) before submission |
| Human checklist | Present below | Complete before external submission |

## Asset Identity

| Field | Value | Source | Status |
| --- | --- | --- | --- |
| Brand | testedprofit / Profitnet | Provided project brief and public pages | Needs verification |
| Token name | ProfitNet | Public references | Needs on-chain verification |
| Unit | PNET | Public references | Needs on-chain verification |
| Network | Algorand | ASA reference | Needs verification |
| ASA ID | 3169177585 | testedprofit pages and public references | Needs on-chain verification |

## ASA Control Fields

Control fields should be copied from a public Algorand explorer or indexer, not inferred from the website.

| Control field | Status |
| --- | --- |
| Creator address | Needs verification |
| Manager address | Needs verification |
| Reserve address | Needs verification |
| Freeze address | Needs verification |
| Clawback address | Needs verification |
| Default frozen state | Needs verification |
| Asset URL / metadata URL | Needs verification |
| Metadata hash, if present | Needs verification |

## Supply and Decimals

| Field | Page-displayed value | Verification status |
| --- | --- | --- |
| Total supply | 100,000,000 PNET | Needs on-chain verification |
| Decimals | 6 | Needs on-chain verification |
| Derived raw total, if decimals are correct | 100,000,000,000,000 raw units | Derived, Needs on-chain verification |

## Circulating, Burned, and Locked Claims

| Claim | Page-displayed value | Verification status |
| --- | --- | --- |
| Burned supply shown | 8,180,000 PNET | Needs on-chain verification |
| Founder allocation shown | 25M PNET locked | Needs on-chain lock verification |
| Strategic reserve shown | 15M PNET locked | Needs on-chain lock verification |
| Major unlock shown | 25% supply lock, Sept 2026 | Needs on-chain lock verification |
| Circulating supply | Not verified in this repository | Needs verification |

## Liquidity / Pool References

The dossier records LP and vault labels from public pages, but it does not verify pool existence, balances, counterpart assets, lock status, or burn status.

| Reference type | Current status |
| --- | --- |
| ALGO/PNET label | Needs on-chain LP verification |
| DDAO/PNET label | Needs on-chain LP verification |
| Burned LP vault labels | Needs on-chain verification |
| Strategic partnership vault labels | Needs on-chain verification |
| Vestige market page | Snapshot only |
| Allo asset page | Needs manual follow-up |

## Utility Summary

No PNET utility claim is independently verified in this repository. Any future utility summary should cite an official source, avoid investment or income framing, and remain marked `Needs verification` until independently checked.

## Public Links

See [references/public-links.md](../references/public-links.md) and [docs/11_API_AND_DATA_SOURCES.md](11_API_AND_DATA_SOURCES.md).

## Risk Disclosures

- This repository does not provide financial, legal, tax, custody, trading, bridge, or listing advice.
- Public pages and market listings can change.
- Third-party market data is stale immediately after capture.
- Page-displayed locks, vaults, burns, and partner labels are not on-chain verified here.
- Bridge availability does not imply exchange support or Coinbase listing.
- No reader should connect a wallet, sign a transaction, transfer assets, or provide credentials to verify this dossier.

## Claims Policy

Public claims must follow [docs/06_PUBLIC_CLAIMS_POLICY.md](06_PUBLIC_CLAIMS_POLICY.md).

## Human Verification Checklist

| Check | Status |
| --- | --- |
| Confirm ASA ID, asset name, unit, total, decimals, URL, and metadata hash | Needs verification |
| Record creator, manager, reserve, freeze, and clawback addresses | Needs verification |
| Confirm whether manager / freeze / clawback controls are present or empty | Needs verification |
| Verify burned supply from transactions, burn addresses, or explorer records | Needs verification |
| Verify founder allocation lock mechanism and address/account evidence | Needs on-chain verification |
| Verify strategic reserve lock mechanism and address/account evidence | Needs on-chain verification |
| Verify Sept 2026 unlock mechanics and exact date/time, if applicable | Needs on-chain verification |
| Verify LP/vault labels against pool IDs, balances, and asset pairs | Needs on-chain verification |
| Save dated screenshots with source URL and capture time | Needs verification |
| Confirm no exchange, bridge, or Coinbase support is implied | Needs verification |
