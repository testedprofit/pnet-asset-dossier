# CoinGecko and CoinMarketCap Build Targets

Status: public-safe build-toward checklist; no listing outcome claimed  
Date: 2026-07-11

## Purpose

This document records CoinGecko and CoinMarketCap as future discovery targets for ProfitNet (`PNET`) without implying that either listing is guaranteed, pending, endorsed, approved, or already submitted.

The current posture:

```text
Build toward CoinGecko and CoinMarketCap.
Do not submit until the evidence is credible.
Do not ask the community to spam listing teams.
```

## Current Status

| Item | Status |
| --- | --- |
| Base ERC-20 deployed | Complete |
| Base ERC-20 source verification | Complete on BaseScan, Blockscout, and Sourcify |
| BaseScan address ownership | Complete |
| BaseScan token profile/logo application | Submitted; external review pending |
| Verified-source contract review | No contract-level honeypot mechanics found |
| Blockaid / wallet warning | Likely heuristic false positive; warning remains displayed pending provider review/update |
| Official website updated for Base ERC-20 | Needed |
| Public Command Center | Planned |
| Active Uniswap market | Very small legacy seed pool plus active CCA; final migrated pool pending |
| Meaningful liquidity and organic volume | Needed |
| Successful buy/sell transaction record | Needed in public evidence packet |
| Auction / LP-lock evidence | CCA address, launcher transaction, strategy, allocation, and configured timelock recorded; final migration/pool/position proof pending |
| Holder/activity snapshots | Needed |
| CoinGecko application | Not submitted |
| CoinMarketCap application | Not submitted |

## CoinGecko Build Target

CoinGecko should be treated as a build target only after PNET has:

- a clean public website,
- a stable logo and token metadata,
- a verified Base contract,
- an active public market route,
- evidence that the market is actively tradable,
- public links that do not conflict,
- and non-spam community behavior.

Internal gate:

```text
Do not apply to CoinGecko until PNET can be reviewed as an active, real public market with consistent metadata and source links.
```

## CoinMarketCap Build Target

CoinMarketCap should be treated as a later build target because it expects stronger structured evidence, market activity, and public credibility.

PNET should prepare:

- functional website,
- direct explorer links,
- direct market/pair links,
- source verification links,
- public contact information,
- logo and metadata,
- evidence of active public trading,
- meaningful volume snapshots,
- holder/activity snapshots,
- and a complete evidence packet.

Internal gate:

```text
Do not apply to CoinMarketCap until PNET has material public trading activity and enough evidence to complete the form without vague or promotional claims.
```

## Readiness Gates

| Gate | Needed for | Status |
| --- | --- | --- |
| BaseScan profile/logo approved | CoinGecko, CMC | Pending external review |
| Wallet-warning remediation packet | CoinGecko, CMC | Verified-source analysis ready; external submission/update pending |
| Official website updated for Base + Algorand | CoinGecko, CMC | Needed |
| Command Center live | CoinGecko, CMC | Planned |
| Official contact email/socials | CoinGecko, CMC | Needed |
| Stable token logo URL | CoinGecko, CMC | Commit-pinned SVG exists |
| Active public pool | CoinGecko, CMC | Legacy seed pool exists; wait for the auction-migrated canonical pool |
| Successful public buy and sell transaction links | CoinGecko, CMC | Needed |
| Auction / LP-lock evidence, if claimed | CoinGecko, CMC | CCA configuration documented; final migration and LP position proof pending |
| Meaningful liquidity | CoinGecko, CMC | Needed |
| Organic swaps over multiple days | CoinGecko, CMC | Needed |
| Dated volume/liquidity snapshots | CoinGecko, CMC | Needed |
| Holder distribution snapshot | CoinGecko, CMC | Needed |
| Honest concentration improvement | CoinGecko, CMC | Needed; no controlled-wallet splitting |
| Product/utility proof | CoinGecko, CMC | Command Center / AI verifier planned |
| No overclaiming | CoinGecko, CMC | Must maintain |

## Evidence Packet

Before any submission, assemble:

- project name: `ProfitNet`;
- symbol: `PNET`;
- Base contract: `0xe1F7F585f458cB6AFFCEE2286b8482523B19ee5a`;
- chain: Base mainnet;
- chain ID: `8453`;
- BaseScan token page;
- BaseScan source page;
- Blockscout source page;
- Sourcify source page;
- deployment transaction: `0x7d6300cb7f84d18fdaeafe3c34195e946ec86e6ce8c91d87d577177873b39fd1`;
- official website;
- public dossier;
- whitepaper;
- token logo;
- official contact;
- official socials, if any;
- Uniswap pool URL;
- Uniswap price chart URL;
- Uniswap swap URL;
- Uniswap v4 position URL, clearly labeled as a position reference rather than LP-lock proof;
- successful buy transaction and successful sell transaction links;
- CCA auction page, launcher transaction, final migration transaction, and final canonical pool;
- actual LP-lock/burn evidence if claimed, including mechanism, transaction, amount, duration, authority, and beneficiary;
- liquidity snapshots;
- volume snapshots;
- holder snapshots;
- wallet-warning remediation record and current provider status;
- Blockaid false-positive report date, ticket, and public-safe status, plus any optional Uniswap support follow-up;
- Command Center URL;
- AI verifier or AutoDev page, if shipped;
- clear disclaimer that PNET is not presented as investment, yield, hashrate, or future-value product;
- clear note that Wormhole NTT is not production-live until proven.

## Wallet-Warning Gate

PNET is a legitimate project. The verified Base contract does not contain honeypot mechanics. The warning appears to be a third-party heuristic false positive, likely from new-token/tiny-liquidity/not-listed/holder-concentration signals.

The contract is a minimal OpenZeppelin ERC-20 with a one-time fixed constructor mint and no owner/admin, post-deployment mint, pause, blacklist/whitelist, tax/fee, transfer override, proxy, exposed `owner()`, or exposed `minter()`. The warning nevertheless remains displayed pending Blockaid or downstream wallet-provider review.

Before a CoinGecko or CoinMarketCap submission, complete the evidence and remediation steps in [24_WALLET_WARNING_BLOCKAID_REMEDIATION.md](24_WALLET_WARNING_BLOCKAID_REMEDIATION.md): finish BaseScan profile/logo approval, record successful buy and sell transactions, document any auction and LP-lock evidence accurately, publish holder-distribution snapshots, and submit the false-positive packet through Blockaid's official report portal. Reference the Blockaid ticket in any optional Uniswap support follow-up.

## Submission Rules

- Use official forms only.
- Do not use unofficial listing brokers.
- Do not pay anyone claiming guaranteed listing access.
- Do not ask the community to spam listing teams.
- Do not submit duplicate applications.
- Do not create a duplicate v2 pool merely to burn LP; strengthen and document the existing v4 market.
- Do not inflate or fake volume.
- Do not wash trade.
- Do not manufacture holder count by distributing balances among controlled wallets.
- Do not submit unverified burn, lock, hashrate, bridge, or endorsement claims.
- Save a copy of every submitted answer.
- Update this dossier after any application or response.

## Build Path

1. Finish BaseScan profile/logo review and record the approval.
2. Record one successful buy and one successful sell transaction from the existing v4 pool.
3. Finish the active CCA and document the final migration, canonical pool, liquidity provenance, position, and actual timelock mechanism.
4. Publish a dated holder-distribution snapshot and improve concentration through genuine participation.
5. Submit the verified false-positive evidence packet through Blockaid's official report portal, reference its ticket in any optional Uniswap support follow-up, and track the warning status.
6. Update official website and public links.
7. Launch the no-wallet ProfitNet Command Center.
8. Add liquidity according to a written plan without creating a misleading duplicate pool.
9. Track weekly holders, organic swaps, volume, TVL, and slippage.
10. Publish the AI verifier or AutoDev concept as a product direction.
11. Prepare the listing evidence packet and review all public claims.
12. Keep the separate Uniswap CCA badge plan in [25_UNISWAP_CCA_VERIFIED_LISTING_PLAN.md](25_UNISWAP_CCA_VERIFIED_LISTING_PLAN.md); token metadata/listing readiness does not guarantee that badge.
12. Submit CoinGecko only after active-market prerequisites are credible.
13. Submit CoinMarketCap only after market activity and evidence are materially stronger.

## Source Notes

| Topic | Source |
| --- | --- |
| CoinGecko listing guide | https://support.coingecko.com/hc/en-us/articles/7291312302617-How-to-List-a-New-Cryptocurrency-on-CoinGecko |
| CoinMarketCap listing criteria | https://support.coinmarketcap.com/hc/en-us/articles/360043659351-Listings-Criteria |
| CoinMarketCap request form information | https://support.coinmarketcap.com/hc/en-us/articles/360018997951-Link-to-Request-Form |
