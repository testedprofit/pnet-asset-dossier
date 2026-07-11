# ProfitNet / PNET Asset Dossier

Public documentation hub for the ProfitNet asset, unit `PNET`, associated with the testedprofit / Profitnet brand.

This repository is documentation and media only. It acts as a whitepaper, verification hub, public claims record, media archive, tokenomics review package, and roadmap index.

GitHub repository: https://github.com/testedprofit/pnet-asset-dossier

## Current Scope

The dossier records public information and review status for:

- ProfitNet / PNET asset identity,
- Base contract `0xe1F7F585f458cB6AFFCEE2286b8482523B19ee5a`,
- ASA ID `3169177585`,
- tokenomics and supply claims,
- source links and market references,
- public claims policy,
- media handling,
- verification procedures,
- listing-readiness materials,
- future market-intelligence and contribution-protocol specifications.

It does not contain code, signer logic, wallet logic, private keys, mnemonics, API keys, `.env` files, deployment automation, trading logic, custody flows, or user-deposit instructions.

## Quick Facts

### Base ERC-20

| Field | Value | Status |
| --- | --- | --- |
| Base token name | ProfitNet | Source verified on BaseScan; token profile submitted and review pending |
| Base token unit | PNET | Source verified on BaseScan; token profile submitted and review pending |
| Base chain ID | `8453` | Public chain reference |
| Base contract | `0xe1F7F585f458cB6AFFCEE2286b8482523B19ee5a` | Source verified on BaseScan/Blockscout/Sourcify |
| Base decimals | `18` | Verified ERC-20 interface/source |
| Base total supply | `100,000,000` PNET | Fixed-supply ERC-20 constructor mint |
| Base initial recipient | `0xd58cc829622c4c988af43028aaa37eda84104649` | Deployment constructor argument |
| Base deployment transaction | https://basescan.org/tx/0x7d6300cb7f84d18fdaeafe3c34195e946ec86e6ce8c91d87d577177873b39fd1 | Public chain reference |
| Base Uniswap CCA | https://app.uniswap.org/explore/auctions/base/0x777900C0FF11845c8e0D6C134b58C695023Aab4e | Active auction reference; migration pending at status date |
| Base Uniswap seed pool | https://app.uniswap.org/explore/pools/base/0xff481004f38fc7db43f3e3b47f6ad3e155482a00866d709d89700d303b0b4f3a | Small legacy seed-liquidity reference; not the final auction-migrated pool |
| Base Uniswap price chart | https://app.uniswap.org/explore/pools/base/0xff481004f38fc7db43f3e3b47f6ad3e155482a00866d709d89700d303b0b4f3a?chart=price | Third-party chart reference |
| Base Uniswap position | https://app.uniswap.org/positions/v4/base/2731162 | Public position reference; not proof of an LP lock or burn |
| Base token logo | [media/pnet-logo-32.svg](media/pnet-logo-32.svg) | Maintainer-provided listing icon |
| Base machine metadata | [data/asset-metadata/pnet-base-token.json](data/asset-metadata/pnet-base-token.json) | Base-specific facts; separate from legacy Algorand metadata |
| Base token list | [tokenlist.json](tokenlist.json) | Uniswap token-list-schema candidate; not a guarantee of interface verification |

### Wallet-Warning Status

PNET is a legitimate project. The verified Base contract does not contain honeypot mechanics. The warning appears to be a third-party heuristic false positive, likely from new-token/tiny-liquidity/not-listed/holder-concentration signals.

The verified source is a minimal OpenZeppelin ERC-20: its fixed supply is minted once in the constructor; it has no owner/admin, post-deployment mint, pause, blacklist/whitelist, tax/fee, transfer override, proxy, exposed `owner()`, or exposed `minter()`. The Blockaid-sourced warning remains displayed in affected Uniswap or wallet surfaces pending third-party review and update. See [docs/24_WALLET_WARNING_BLOCKAID_REMEDIATION.md](docs/24_WALLET_WARNING_BLOCKAID_REMEDIATION.md) for the contract findings, evidence status, official report route, and remediation plan.

### Uniswap Pink-Check Status

The pink check shown beside some Uniswap auctions is a Verified CCA auction/launch designation, not a generic verified-token badge. PNET's configured LP allocation appears sufficient for the numerical liquidity gate after successful migration, but the public record does not yet evidence the required three-of-four founder/social/press/fund criteria. See [docs/25_UNISWAP_CCA_VERIFIED_LISTING_PLAN.md](docs/25_UNISWAP_CCA_VERIFIED_LISTING_PLAN.md) for the exact criteria, scorecard, application worksheet, and truthful build path.

### Base Holder and Treasury Status

At Base block `48,477,164`, the initial-recipient wallet held `74.747111457500%` of supply. The maintainer confirms that `0x7f97e32af1d2eb65d9d5f5b5ce15048768234a58` is a founder-controlled custodial allocation wallet holding `15,000,000` PNET. On that maintainer-supplied control label, at least `89.747111457500%` of supply was under project/founder beneficial control at the snapshot. The 15,000,000-PNET balance and transfer are on-chain verified; its role and custodial status are maintainer-supplied, and no on-chain vesting, lock, transfer restriction, or custody access is evidenced. Auction, LBP-strategy, and PoolManager balances are contract inventory, not independent owners, and ERC-20 balances do not prove an LP position NFT is locked.

The current decision is **NO-GO on another standard Uniswap CCA** until the active auction resolves, migration and LP custody are proven, a controlled-address registry and allocation/lock status are published, the canonical market meets the written quality gates, and legal review is complete. See the [holder snapshot](data/on-chain-proofs/base-holder-distribution-2026-07-11.md) and [Base treasury and distribution plan](docs/26_BASE_TREASURY_AND_DISTRIBUTION_PLAN.md).

### Legacy Algorand ASA

| Field | Value | Status |
| --- | --- | --- |
| Brand | testedprofit / Profitnet | Needs verification |
| Token name | ProfitNet | Verified in prior dossier indexer review; recheck before external use |
| Unit | PNET | Verified in prior dossier indexer review; recheck before external use |
| Algorand ASA ID | `3169177585` | Verified in prior dossier indexer review; recheck before external use |
| Website | https://testedprofit.com | Public project link |
| Tokenomics page | https://testedprofit.com/pages/tokenomics/ | Public project link |
| PNET page | https://testedprofit.com/pages/PNET/ | Public project link |
| Vestige listing | https://vestige.fi/asset/3169177585 | Public market reference |
| Total supply | `100,000,000` PNET | Verified by public indexers in [asset identity proof](data/on-chain-proofs/asset-identity-proof-2026-06-27.md); recheck before external use |
| Decimals | `6` | Verified by public indexers in [asset identity proof](data/on-chain-proofs/asset-identity-proof-2026-06-27.md); recheck before external use |

## Start Here

| Need | File |
| --- | --- |
| Canonical specification | [WHITEPAPER.md](WHITEPAPER.md) |
| Funny companion whitepaper | [FUNPAPER.md](FUNPAPER.md) |
| Roadmap and implementation gates | [ROADMAP.md](ROADMAP.md) |
| Moonshot runway | [docs/22_MOONSHOT_RUNWAY.md](docs/22_MOONSHOT_RUNWAY.md) |
| CoinGecko / CMC build targets | [docs/23_COINGECKO_CMC_BUILD_TARGETS.md](docs/23_COINGECKO_CMC_BUILD_TARGETS.md) |
| Wallet warning / Blockaid remediation | [docs/24_WALLET_WARNING_BLOCKAID_REMEDIATION.md](docs/24_WALLET_WARNING_BLOCKAID_REMEDIATION.md) |
| Uniswap CCA verified-listing plan | [docs/25_UNISWAP_CCA_VERIFIED_LISTING_PLAN.md](docs/25_UNISWAP_CCA_VERIFIED_LISTING_PLAN.md) |
| Base treasury and distribution plan | [docs/26_BASE_TREASURY_AND_DISTRIBUTION_PLAN.md](docs/26_BASE_TREASURY_AND_DISTRIBUTION_PLAN.md) |
| Base holder-distribution snapshot | [data/on-chain-proofs/base-holder-distribution-2026-07-11.md](data/on-chain-proofs/base-holder-distribution-2026-07-11.md) |
| Documentation index | [docs/README.md](docs/README.md) |
| User guide | [docs/user/USER_GUIDE.md](docs/user/USER_GUIDE.md) |
| Developer guide | [docs/developer/DEVELOPER_GUIDE.md](docs/developer/DEVELOPER_GUIDE.md) |
| Security guide | [docs/security/SECURITY_GUIDE.md](docs/security/SECURITY_GUIDE.md) |
| Contribution protocol guide | [docs/contribution/CONTRIBUTION_PROTOCOL_GUIDE.md](docs/contribution/CONTRIBUTION_PROTOCOL_GUIDE.md) |
| Contribution Credit System MVP | [docs/pnet-contribution-protocol/MVP.md](docs/pnet-contribution-protocol/MVP.md) |
| Verification handbook | [docs/verification/VERIFICATION_HANDBOOK.md](docs/verification/VERIFICATION_HANDBOOK.md) |
| Website copy templates | [docs/templates/WEBSITE_COPY.md](docs/templates/WEBSITE_COPY.md) |
| Announcement templates | [docs/templates/PUBLIC_ANNOUNCEMENTS.md](docs/templates/PUBLIC_ANNOUNCEMENTS.md) |
| Content and marketing system | [docs/marketing/README.md](docs/marketing/README.md) |
| On-chain proof package | [data/on-chain-proofs/README.md](data/on-chain-proofs/README.md) |
| Implementation specifications | [docs/implementation/README.md](docs/implementation/README.md) |
| Audit readiness package | [docs/audit/README.md](docs/audit/README.md) |
| Deployment registry | [docs/DEPLOYMENT_REGISTRY.md](docs/DEPLOYMENT_REGISTRY.md) |

## Core Review Records

| File | Purpose |
| --- | --- |
| [DEPLOYMENTS.md](DEPLOYMENTS.md) | Deployment and listing-reference cautions |
| [FUNPAPER.md](FUNPAPER.md) | Funny, public-safe companion whitepaper |
| [SECURITY.md](SECURITY.md) | Sensitive-material and reporting policy |
| [DISCLAIMER.md](DISCLAIMER.md) | Risk and non-advice disclaimer |
| [docs/01_ASSET_FACTS.md](docs/01_ASSET_FACTS.md) | Asset facts |
| [docs/03_TOKENOMICS.md](docs/03_TOKENOMICS.md) | Tokenomics and supply-claim status |
| [docs/05_MARKET_SNAPSHOTS.md](docs/05_MARKET_SNAPSHOTS.md) | Market snapshot rules |
| [docs/06_PUBLIC_CLAIMS_POLICY.md](docs/06_PUBLIC_CLAIMS_POLICY.md) | Public claims policy |
| [docs/08_LISTING_READINESS.md](docs/08_LISTING_READINESS.md) | Listing-readiness package |
| [docs/10_ON_CHAIN_REVIEW_CHECKLIST.md](docs/10_ON_CHAIN_REVIEW_CHECKLIST.md) | On-chain review checklist |
| [docs/11_API_AND_DATA_SOURCES.md](docs/11_API_AND_DATA_SOURCES.md) | API and data-source references |
| [docs/12_DEEP_TOKENOMICS_REVIEW.md](docs/12_DEEP_TOKENOMICS_REVIEW.md) | Deep tokenomics review |
| [docs/DEPLOYMENT_REGISTRY.md](docs/DEPLOYMENT_REGISTRY.md) | Deployment, prototype, and evidence registry |
| [docs/LIVE_TESTNET_EVIDENCE.md](docs/LIVE_TESTNET_EVIDENCE.md) | Live/TestNet evidence status |
| [docs/WHITEPAPER_REALITY_MAP.md](docs/WHITEPAPER_REALITY_MAP.md) | Whitepaper claim-to-artifact map |
| [docs/OPERATIONAL_WALLET_TRANSPARENCY.md](docs/OPERATIONAL_WALLET_TRANSPARENCY.md) | Operational wallet public evidence and status |
| [docs/RFC_INDEX.md](docs/RFC_INDEX.md) | Implementation RFC index |
| [docs/implementation/README.md](docs/implementation/README.md) | Implementation specs |
| [docs/implementation/algorand-atomic-transaction-groups.md](docs/implementation/algorand-atomic-transaction-groups.md) | Algorand atomic transaction group patterns for PNET |
| [docs/implementation/algolens-legacy-progress.md](docs/implementation/algolens-legacy-progress.md) | Legacy AlgoLens prototype progress note |
| [docs/audit/README.md](docs/audit/README.md) | Audit tracker, threat model, and review checklist |
| [docs/20_CONTRIBUTION_PROTOCOL_PUBLIC_DISCLOSURE_PLAN.md](docs/20_CONTRIBUTION_PROTOCOL_PUBLIC_DISCLOSURE_PLAN.md) | Contribution protocol disclosure plan |
| [docs/21_CONTRIBUTION_PROTOCOL_FINAL_PACKAGE.md](docs/21_CONTRIBUTION_PROTOCOL_FINAL_PACKAGE.md) | Contribution protocol synthesis |
| [docs/22_MOONSHOT_RUNWAY.md](docs/22_MOONSHOT_RUNWAY.md) | Public-safe growth, legitimacy, and distribution runway |
| [docs/23_COINGECKO_CMC_BUILD_TARGETS.md](docs/23_COINGECKO_CMC_BUILD_TARGETS.md) | CoinGecko and CoinMarketCap build-toward checklist |
| [docs/24_WALLET_WARNING_BLOCKAID_REMEDIATION.md](docs/24_WALLET_WARNING_BLOCKAID_REMEDIATION.md) | Verified-contract wallet-warning analysis and false-positive remediation status |
| [docs/25_UNISWAP_CCA_VERIFIED_LISTING_PLAN.md](docs/25_UNISWAP_CCA_VERIFIED_LISTING_PLAN.md) | Uniswap CCA pink-check criteria, PNET scorecard, and application plan |
| [docs/26_BASE_TREASURY_AND_DISTRIBUTION_PLAN.md](docs/26_BASE_TREASURY_AND_DISTRIBUTION_PLAN.md) | Base custody, beneficial-owner distribution, canonical-pool gates, and 30/60/90 execution plan |
| [data/on-chain-proofs/base-holder-distribution-2026-07-11.md](data/on-chain-proofs/base-holder-distribution-2026-07-11.md) | Block-pinned Base balance and concentration snapshot with ownership cautions |
| [docs/pnet-contribution-protocol/MVP.md](docs/pnet-contribution-protocol/MVP.md) | Contribution Credit System MVP status |
| [docs/pnet-contribution-protocol/METHODS.md](docs/pnet-contribution-protocol/METHODS.md) | Contribution Credit System methods |
| [docs/pnet-contribution-protocol/LEGAL_DISCLAIMER.md](docs/pnet-contribution-protocol/LEGAL_DISCLAIMER.md) | Draft legal disclaimer |
| [docs/pnet-contribution-protocol/PUBLIC_CLAIMS_POLICY.md](docs/pnet-contribution-protocol/PUBLIC_CLAIMS_POLICY.md) | Contribution protocol public claims policy |
| [docs/pnet-contribution-protocol/VERIFICATION_PROCESS.md](docs/pnet-contribution-protocol/VERIFICATION_PROCESS.md) | Contribution protocol verification process |
| [docs/pnet-contribution-protocol/RISK_REGISTER.md](docs/pnet-contribution-protocol/RISK_REGISTER.md) | Contribution protocol risk register |
| [docs/pnet-contribution-protocol/THREAT_MODEL.md](docs/pnet-contribution-protocol/THREAT_MODEL.md) | Contribution protocol threat model |
| [docs/pnet-contribution-protocol/AUDIT_READINESS_CHECKLIST.md](docs/pnet-contribution-protocol/AUDIT_READINESS_CHECKLIST.md) | Contribution protocol audit readiness checklist |
| [docs/marketing/30_DAY_CONTENT_CALENDAR.md](docs/marketing/30_DAY_CONTENT_CALENDAR.md) | 30-day education-first content calendar |
| [docs/marketing/SEO_ARTICLE_TEMPLATES.md](docs/marketing/SEO_ARTICLE_TEMPLATES.md) | SEO article templates |
| [docs/marketing/X_THREAD_TEMPLATES.md](docs/marketing/X_THREAD_TEMPLATES.md) | X/Twitter thread templates |
| [docs/marketing/BRAND_ASSET_USAGE_GUIDE.md](docs/marketing/BRAND_ASSET_USAGE_GUIDE.md) | Brand and jingle asset usage guide |
| [docs/marketing/EMAIL_ONBOARDING_SEQUENCE.md](docs/marketing/EMAIL_ONBOARDING_SEQUENCE.md) | Community onboarding emails |
| [docs/marketing/CCA_PRESS_KIT.md](docs/marketing/CCA_PRESS_KIT.md) | Factual reporter source pack for CCA, contract, and warning evidence |
| [docs/templates/FOUNDER_DISCLOSURE_TEMPLATE.md](docs/templates/FOUNDER_DISCLOSURE_TEMPLATE.md) | Public founder/team disclosure template |
| [docs/templates/UNISWAP_CCA_APPLICATION_WORKSHEET.md](docs/templates/UNISWAP_CCA_APPLICATION_WORKSHEET.md) | Prepared CCA form worksheet; not ready to submit |
| [references/public-links.md](references/public-links.md) | Public links |
| [media/README.md](media/README.md) | Media guide |
| [data/asset-metadata/pnet-asset-facts.json](data/asset-metadata/pnet-asset-facts.json) | Machine-readable asset facts |
| [data/asset-metadata/pnet-base-token.json](data/asset-metadata/pnet-base-token.json) | Machine-readable Base token and auction facts |
| [tokenlist.json](tokenlist.json) | Base PNET token-list candidate |
| [data/on-chain-proofs/README.md](data/on-chain-proofs/README.md) | On-chain proof package |

## Verification Model

Facts are treated as unresolved until the dossier records public evidence, capture date, method, observed value, and status.

Accepted status labels:

- `Verified`
- `Verified by public indexers`
- `Snapshot only`
- `Needs verification`
- `Needs on-chain verification`
- `Needs methodology review`
- `Not claimed`

The preferred review path is in [docs/verification/VERIFICATION_HANDBOOK.md](docs/verification/VERIFICATION_HANDBOOK.md).

## Public Claims Policy

The dossier must not claim or imply:

- guaranteed profit,
- risk-free participation,
- passive income,
- deposit and earn,
- copy trading,
- managed strategy,
- Coinbase listing confirmed,
- guaranteed listing,
- guaranteed value,
- APY/APR/ROI,
- exchange or bridge support unless official and sourced.

Contribution credits, if deployed, must be described only as app-local access/reputation records. They are not PNET tokens, not deposits, not yield, not passive income, not profit share, not guaranteed value, and not investment returns.

## Operational Context

The project context includes a user-provided disclosure that the original creator wallet may be unavailable and a user-provided operational wallet:

`CIVTUU6KLTYO26SPVEBDFBKP3UMZM2DPEO5RINODUVCI5NVIFC6HVNWS7E`

Both remain public-review topics:

| Topic | Status |
| --- | --- |
| Lost creator wallet | Needs on-chain and methodology verification |
| Lost-wallet burn-accounting treatment | Needs on-chain and methodology verification |
| Operational wallet role, balance, and control status | Needs verification |

No private custody notes, recovery details, signer locations, personal data, or wallet screenshots should be published.

## Current Gate Status

| Gate | Status | Notes |
| --- | --- | --- |
| Documentation-only scope | PASS | Repository contains documentation, metadata, references, and media only |
| Whitepaper v1.1 | READY FOR REVIEW | Structure updated around specification, utility, roadmap, verification, and risks |
| On-chain proof package | STARTED | ASA identity/current controls and a block-pinned Base holder snapshot are recorded; the founder-control label is maintainer-supplied, while burn/lock/vesting/vault and custody-access proofs remain incomplete |
| Implementation specs | STARTED | Contribution protocol, contract design principles, and snapshot API specs added |
| Audit readiness | STARTED | Audit tracker, threat model, and review checklist added |
| Documentation structure | READY FOR REVIEW | User, developer, security, contribution, verification, and template guides added |
| Content and marketing system | READY FOR REVIEW | Education-first calendar, article templates, social templates, brand guide, and email sequence added |
| Sensitive-material policy | PASS | No secrets, wallet files, signer logic, or private data should be committed |
| Public claims policy | PASS WITH WATCHLIST | Risky terms allowed only in disclaimers or avoided-claims context |
| Tokenomics claims | PARTIAL | Baseline ASA supply/decimals verified; burns, locks, vaults, allocations, and circulating methodology require evidence |
| Lost creator wallet | NEEDS VERIFICATION | Do not treat as verified burned supply without methodology and evidence |
| Operational wallet | SNAPSHOT ONLY | Address validity and current PNET balance snapshot recorded; role and control model not verified |
| Contribution protocol | MVP READY FOR TESTNET DEPLOYMENT | Local implementation package prepared; TestNet app ID and deployment tx pending; not MainNet, not audited |
| Base wallet warning | REMEDIATION OPEN | Verified source review found no contract-level honeypot mechanics; third-party warning remains displayed pending Blockaid/wallet update |
| Base holder concentration | ACTION REQUIRED | Maintainer-reported project/founder control of the top two addresses was at least 89.7471% at block 48,477,164; no on-chain vesting, lock, or custody access for the 15,000,000-PNET founder allocation is evidenced |
| Additional standard CCA | NO-GO | Finish the current auction, prove migration/LP custody, preserve one canonical market, and pass the published distribution gates before reconsideration |
| Exchange / bridge support | NOT CLAIMED | No venue support or listing outcome is implied |
