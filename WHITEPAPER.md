# ProfitNet / PNET Whitepaper

Status date: 2026-06-27

## Abstract

ProfitNet, unit `PNET`, is presented here as a public asset dossier for the testedprofit / Profitnet brand. This whitepaper is a documentation-first reference for asset facts, verification workflows, tokenomics notes, media references, and security posture.

All asset facts in this document are marked `Needs verification` until they are confirmed against authoritative on-chain records and official brand-controlled sources.

## Asset Summary

| Field | Value | Status |
| --- | --- | --- |
| Brand | testedprofit / Profitnet | Needs verification |
| Token name | ProfitNet | Needs verification |
| Unit | PNET | Needs verification |
| ASA ID | 3169177585 | Needs verification |
| Total supply | 100,000,000 | Needs verification |
| Decimals | 6 | Needs verification |
| Website | https://testedprofit.com | Needs verification |
| Tokenomics page | https://testedprofit.com/pages/tokenomics/ | Needs verification |
| PNET page | https://testedprofit.com/pages/PNET/ | Needs verification |
| Vestige page | https://vestige.fi/asset/3169177585 | Needs verification |

## Purpose

This repository is designed to serve three public documentation functions:

1. Whitepaper: a stable, readable overview of the PNET asset and its known public references.
2. Verification hub: a place to record what has been checked, what remains unverified, and how others can reproduce verification.
3. Media archive: a public location for logos, screenshots, brand assets, and supporting media when available.

## Design Boundaries

This dossier is intentionally limited to documentation and media. It does not include application code, wallet integrations, transaction builders, signer behavior, custody services, private credentials, or operational secrets.

## Token Utility

No utility claims are verified in this repository at this time. Any stated or proposed utility for PNET should be supported by official documentation and independently checked. See [docs/02_TOKEN_UTILITY.md](docs/02_TOKEN_UTILITY.md).

## Tokenomics

The 2026-06-27 tokenomics snapshot records page-displayed values from the testedprofit tokenomics page:

| Item | Value | Status |
| --- | --- | --- |
| Total supply | 100,000,000 | Needs verification |
| Burned supply shown | 8,180,000 | Needs on-chain verification |
| Decimals | 6 | Needs verification |
| Founder allocation shown | 25M PNET locked | Needs on-chain lock verification |
| Strategic reserve shown | 15M PNET locked | Needs on-chain lock verification |
| Major unlock shown | 25% supply lock, Sept 2026 | Needs on-chain lock verification |

LP, vault, burn, lock, and partner labels shown on public pages are treated as dated claims only until explorer or indexer evidence is recorded. See [docs/03_TOKENOMICS.md](docs/03_TOKENOMICS.md) and [data/tokenomics/tokenomics-snapshot-2026-06-27.md](data/tokenomics/tokenomics-snapshot-2026-06-27.md).

## Verification Approach

Verification should compare the provided facts against:

- The Algorand asset record for ASA ID `3169177585`
- The official website at https://testedprofit.com
- The tokenomics page at https://testedprofit.com/pages/tokenomics/
- The PNET page at https://testedprofit.com/pages/PNET/
- The Vestige listing at https://vestige.fi/asset/3169177585
- Any other reputable Algorand explorer or indexer

The repository should only move a fact from `Needs verification` to `Verified` when the source, date, method, and result are documented.

## Risks and Limitations

Digital asset information can change, third-party listings can be incomplete, and websites can be updated or compromised. Readers should verify every material fact directly before relying on it.

This whitepaper is informational only and does not provide financial, legal, tax, custody, trading, or security advice.
