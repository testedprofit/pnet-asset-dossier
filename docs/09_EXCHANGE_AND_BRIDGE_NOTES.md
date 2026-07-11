# Exchange and Bridge Notes

Status date: 2026-07-11

This document is for diligence only. It does not claim that PNET is listed, supported, integrated, bridged, or approved by any exchange, bridge, custodian, market maker, or ecosystem partner.

## Core Position

| Topic | Repository position |
| --- | --- |
| Coinbase | No Coinbase listing or support is claimed. |
| Centralized exchanges | No centralized exchange listing or support is claimed. |
| Decentralized exchange pages | Public market pages are treated as third-party references only. |
| Base / EVM strategy | Base ERC-20 is live and source verified; no Algorand <-> Base bridge or migration portal is live. |
| Wormhole / cross-chain strategy | Research only for existing Algorand ASA `3169177585`; no Wormhole route is claimed live. |
| Chainlink / Robinhood Chain strategy | Chainlink token-admin registration request submitted for a future Base -> Robinhood Chain CCT route; no Robinhood deployment or listing is claimed. |
| Bridged assets | A bridged asset would not prove exchange support, liquidity, custody support, or Coinbase listing. |

## Bridge Strategy Status

Any bridge, wrapped asset, Wormhole route, Chainlink route, or cross-chain representation of PNET is `Not live` unless a separate verification package records:

| Required evidence | Status |
| --- | --- |
| Chain and contract / asset identifier | Needs verification |
| Bridge provider and route | Needs verification |
| Mint / burn / lock mechanics | Needs verification |
| Canonical asset relationship | Needs verification |
| Risk disclosures | Needs verification |
| Explorer links | Needs verification |
| Official announcement or governance approval, if applicable | Needs verification |

## Algorand <-> Base Migration Research

The current recommended first mechanism is a capped, reserve-backed migration/swap path rather than an unlimited bridge claim:

```text
Algorand PNET deposit -> verified reserve receipt -> Base PNET release
Base PNET deposit -> verified reserve receipt -> Algorand PNET release
```

The proposed first cap is `5,000,000` PNET, subject to project-owner approval, reserve inventory, public terms, and qualified review.

Because both Algorand PNET and Base PNET already have fixed public supplies of `100,000,000`, the migration design must not imply new minting or hidden supply. Base-side output must come from an existing Base reserve, and Algorand-side output must come from an existing Algorand reserve unless a later reviewed protocol bridge proves another mechanism.

See [28_MULTICHAIN_MIGRATION_AND_WEBSITE_PLAN.md](28_MULTICHAIN_MIGRATION_AND_WEBSITE_PLAN.md).

## Exchange Diligence Notes

Any listing-readiness packet should separate:

| Category | Handling |
| --- | --- |
| Asset identity | Verify from Algorand asset metadata. |
| Market references | Treat as dated snapshots only. |
| Liquidity references | Verify pool IDs and balances on-chain. |
| Utility claims | Require source evidence and claims-policy review. |
| Compliance / legal claims | Do not include unless supplied by qualified counsel. |
| Exchange support | Do not imply without direct evidence from the named venue. |

## Prohibited Wording

Do not use language that suggests:

- A Coinbase listing is expected or implied.
- A bridge makes Coinbase support more likely.
- A Base, Wormhole, or EVM representation is equivalent to a venue listing.
- PNET is live on three networks before Robinhood Chain deployment is verified.
- A manual migration reserve is a trustless bridge.
- A market page is an exchange endorsement.
- Users should move assets, connect wallets, or sign transactions to support a listing.
