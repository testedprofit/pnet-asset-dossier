# Multichain Migration and Website Plan

Status date: 2026-07-11

Status: public-safe planning record; no Algorand <-> Base migration portal or production bridge is live

This document explains how ProfitNet / PNET can present its Algorand, Base, and planned Robinhood Chain surfaces without confusing supply, bridge, listing, or holder-risk claims.

## Current Positioning

Recommended short website positioning:

> ProfitNet / PNET is becoming a multichain project: rooted on Algorand, expanded to Base, and preparing a supply-backed Robinhood Chain path through Chainlink CCIP/CCT. Existing Algorand PNET remains part of the project history and support plan. Base PNET is the verified EVM token. Robinhood Chain support is not live yet.

This phrasing is intentionally careful. It presents momentum without claiming that every bridge or network is already live.

## Network Status

| Network | Current status | Public claim allowed now |
| --- | --- | --- |
| Algorand | Legacy/root ASA `3169177585` | PNET began on Algorand; the ASA remains part of the public project record |
| Base | Verified ERC-20 `0xe1F7F585f458cB6AFFCEE2286b8482523B19ee5a` | Base PNET is deployed, fixed-supply, source verified, and used for the current EVM market |
| Robinhood Chain | Chainlink token-admin request submitted; no deployment live | PNET is preparing a possible supply-backed Robinhood Chain representation through Chainlink CCIP/CCT |

Do not claim PNET is live on three networks until the Robinhood Chain representation is deployed, verified, and publicly documented.

## Why A 5M Algorand <-> Base Migration Reserve Makes Sense

There are two existing fixed public PNET supplies in the record:

| Network | Supply | Constraint |
| --- | ---: | --- |
| Algorand ASA `3169177585` | `100,000,000` PNET, 6 decimals | Legacy/root asset; control fields recorded as zeroed in the proof package |
| Base ERC-20 | `100,000,000` PNET, 18 decimals | Fixed supply minted at deployment; no owner/admin or post-deploy mint |

Because Base PNET is already fixed supply, an Algorand holder migration cannot mint new Base PNET. The Base side must be funded from an existing reserve. Because the legacy Algorand ASA is recorded as immutable/zeroed-control, the project should not assume it can add bridge mint/burn permissions to ASA `3169177585`.

A first migration reserve capped at `5,000,000` PNET is a cleaner starting point than an unlimited bridge claim:

- it is measurable;
- it supports existing Algorand holders;
- it gives the project time to prove demand;
- it avoids confusing total effective supply;
- it can be audited with transaction-pair proofs;
- it does not require a new mint function or duplicate Base supply.

## Phase 1: Reserve-Backed Swap

Recommended first public mechanism:

```text
Algorand PNET deposit -> verified reserve receipt -> Base PNET release
Base PNET deposit -> verified reserve receipt -> Algorand PNET release
```

This should be described as a migration/swap reserve unless and until a reviewed protocol bridge is live.

Minimum public terms before launch:

- exact Algorand ASA ID;
- exact Base contract;
- conversion rate after decimal normalization;
- starting cap;
- reserve/escrow addresses;
- minimum and maximum swap sizes;
- fees, if any;
- expected processing time;
- failed-transfer/refund policy;
- jurisdiction/sanctions restrictions if required;
- support channel;
- proof index for completed swaps.

## Phase 2: Automated Escrow Or Protocol Bridge

After the 5M reserve proves demand and accounting, the project can evaluate:

- Algorand smart-contract escrow for ASA `3169177585`;
- Base ERC-20 escrow;
- Wormhole support for existing immutable ASAs;
- a new NTT-managed Algorand representation, if required;
- external review, rate limits, emergency controls, and public proof.

The key open technical question is:

```text
Can Wormhole NTT on Algorand bridge existing immutable ASA 3169177585 through escrow/lock-unlock, or does it require a new NTT-managed Algorand asset?
```

Until this is proven, Wormhole NTT should remain a research track for the existing Algorand PNET ASA.

## Website Layout Recommendation

The website should stop feeling Algorand-only. Add a multichain section with three cards:

| Card | Label | Status line | Primary link |
| --- | --- | --- | --- |
| Algorand | Legacy/root PNET | ASA `3169177585`; migration support planned | Vestige / explorer / dossier proof |
| Base | Verified EVM PNET | Fixed-supply ERC-20; source verified | BaseScan / Uniswap / warning remediation |
| Robinhood Chain | Planned CCT path | Chainlink request submitted; not live | Robinhood readiness doc |

Also add a "Bridge / Migration Status" block:

```text
Algorand <-> Base: planned capped migration reserve; not live yet.
Base <-> Robinhood Chain: Chainlink token-admin request submitted; not live yet.
```

## Public Copy Blocks

### Hero / Intro

```markdown
ProfitNet / PNET is a multichain Web3 project rooted on Algorand and expanded to Base.

The Base ERC-20 contract is source verified, fixed supply, and designed with no owner/admin mint, pause, blacklist, transfer tax, transfer override, or proxy. A future Robinhood Chain representation is being prepared through Chainlink CCIP/CCT, but is not live yet.
```

### Network Status

```markdown
## PNET Network Status

| Network | Status |
| --- | --- |
| Algorand | Legacy/root PNET ASA `3169177585`; holder migration support is planned but not live |
| Base | Verified ERC-20 PNET at `0xe1F7F585f458cB6AFFCEE2286b8482523B19ee5a` |
| Robinhood Chain | Planned supply-backed representation through Chainlink CCIP/CCT; not deployed |
```

### Migration Status

```markdown
## Algorand <> Base Migration Status

ProfitNet is evaluating a capped migration reserve so existing Algorand PNET holders can swap into Base PNET and Base holders can swap back into Algorand PNET. The first proposed cap is 5,000,000 PNET.

This migration path is not live yet. The project will publish reserve addresses, terms, limits, proof links, and support instructions before accepting any migration transfers.
```

## Claims To Avoid

Do not say:

- "PNET is live on three networks" before Robinhood deployment;
- "fully bridged" before an actual bridge is live;
- "trustless bridge" for a manual or operator-reviewed reserve swap;
- "burned" unless tokens are sent to an unrecoverable address;
- "locked" unless an enforceable lock exists;
- "Robinhood listed" or "Robinhood app support";
- "guaranteed swap" without published reserves, limits, terms, and support.

## Related Records

- [Robinhood Chain CCT readiness](27_ROBINHOOD_CHAIN_CCT_READINESS.md)
- [Exchange and bridge notes](09_EXCHANGE_AND_BRIDGE_NOTES.md)
- [Wallet warning and Blockaid remediation](24_WALLET_WARNING_BLOCKAID_REMEDIATION.md)
- [Base treasury and distribution plan](26_BASE_TREASURY_AND_DISTRIBUTION_PLAN.md)
- [Website copy templates](templates/WEBSITE_COPY.md)

## Current Gate Status

- Gate name: Multichain migration and website positioning
- Status: `PLANNING`; website copy ready for review; no migration/bridge live
- Evidence produced: network-status language, 5M reserve-backed migration model, website-card plan, claims guardrails
- Human review required: reserve cap, reserve wallets, swap terms, support workflow, legal/compliance review, website publication, and any transfer/escrow action
- Stop conditions: no user deposits, no live-bridge claims, no three-network-live claim, no lock/burn claims without evidence, no Robinhood listing claims
- Next safe action: update testedprofit.com with multichain status language after maintainer review, then publish reserve terms before any Algorand <-> Base migration transfer
