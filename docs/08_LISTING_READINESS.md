# Listing Readiness

Status date: 2026-07-11

This document is a public-review package for listing diligence, ecosystem partner review, and community verification. It is not a listing application, exchange endorsement, investment document, trading guide, or guarantee of venue support.

PNET is a legitimate project. The verified Base contract does not contain honeypot mechanics. The warning appears to be a third-party heuristic false positive, likely from new-token/tiny-liquidity/not-listed/holder-concentration signals. The warning remains displayed pending Blockaid or wallet-provider review; see [24_WALLET_WARNING_BLOCKAID_REMEDIATION.md](24_WALLET_WARNING_BLOCKAID_REMEDIATION.md).

## Readiness Summary

| Area | Current status | Next action |
| --- | --- | --- |
| Base asset identity | Deployed and source verified | Finish pending BaseScan profile/logo approval |
| Base contract review | No contract-level honeypot mechanics found in verified source | Include review findings and source link in false-positive packet |
| Blockaid / wallet warning | Likely heuristic false positive; still displayed | Submit evidence through Blockaid's official report portal and track provider response |
| Base tradeability evidence | Public v4 pool exists; buy/sell tx evidence not yet recorded here | Record one successful buy tx and one successful sell tx |
| Base liquidity evidence | Very small legacy seed pool recorded; active Uniswap CCA and configuration now documented | Record final migration, canonical pool, position, exact liquidity, and timelock proof after auction completion |
| Uniswap CCA pink-check | LP configuration appears sufficient after successful migration; three-of-four identity/traction criteria not currently evidenced | Complete [CCA verified-listing plan](25_UNISWAP_CCA_VERIFIED_LISTING_PLAN.md) without buying or fabricating eligibility signals |
| Base holder distribution | [Block-pinned snapshot](../data/on-chain-proofs/base-holder-distribution-2026-07-11.md) published; maintainer-reported project/founder control of the top two addresses is at least `89.747111457500%` | Publish custody/vesting status, refresh after settlement, and improve honestly; the founder-control label is maintainer-supplied and no on-chain vesting, lock, or custody access is evidenced |
| Issuer-funded repurchase / market support | This dossier does not approve or authorize a program or sale term | If any program is planned, obtain qualified counsel review and disclose counsel-approved material terms and a truthful non-sensitive funding-source category before any token sale; provide full confidential source details only to counsel/compliance, with public redactions allowed only when counsel approves and the public category/material terms remain truthful and non-misleading |
| Legacy ASA identity | Name, unit, network, and ASA ID verified by public indexers at capture round | Recheck dated proof before external use |
| Legacy ASA control fields | Creator and current zero manager/reserve/freeze/clawback values verified at capture round | Recheck dated proof before external use |
| Legacy ASA supply and decimals | Display total, raw total, and decimals verified by public indexers at capture round | Recheck dated proof before external use |
| Circulating, burned, locked claims | Page-displayed claims recorded | Verify burn and lock mechanics on-chain |
| Liquidity / pool references | Public labels recorded | Verify pool IDs, assets, balances, and venue data |
| Utility summary | No utility claim verified | Keep utility neutral until source evidence is recorded |
| Public links | Recorded in references | Add explorer/indexer evidence links |
| Risk disclosures | Present | Keep disclaimers current |
| Claims policy | Present | Enforce before public claims are added |
| CoinGecko / CoinMarketCap readiness | Build targets documented | Complete gates in [23_COINGECKO_CMC_BUILD_TARGETS.md](23_COINGECKO_CMC_BUILD_TARGETS.md) before submission |
| Human checklist | Present below | Complete before external submission |

## Base ERC-20 Identity

| Field | Value | Source | Status |
| --- | --- | --- | --- |
| Name | ProfitNet | Verified deployed source | Verified source |
| Symbol | PNET | Verified deployed source | Verified source |
| Network | Base mainnet, chain ID `8453` | Public chain reference | Verified chain |
| Contract | `0xe1F7F585f458cB6AFFCEE2286b8482523B19ee5a` | [BaseScan source](https://basescan.org/address/0xe1F7F585f458cB6AFFCEE2286b8482523B19ee5a#code) | Source verified |
| Total supply | `100,000,000` PNET | Constructor mint in verified source | Fixed at deployment |
| Deployment | `0x7d6300cb7f84d18fdaeafe3c34195e946ec86e6ce8c91d87d577177873b39fd1` | [BaseScan transaction](https://basescan.org/tx/0x7d6300cb7f84d18fdaeafe3c34195e946ec86e6ce8c91d87d577177873b39fd1) | Public chain reference |
| BaseScan profile/logo | Application submitted | BaseScan workflow | External approval pending |

## Base Contract Review

The verified deployment is a minimal OpenZeppelin ERC-20 with a fixed supply minted once in the constructor. Review found no `Ownable`, owner/admin, post-deployment mint, pause, blacklist/whitelist, tax/fee, transfer override, or proxy. It does not expose `owner()` or `minter()`.

No code path was found that selectively blocks sells or lets a privileged account enable sell-blocking behavior later. This supports the conclusion that the displayed warning is a third-party heuristic false positive rather than a contract-level honeypot finding. This code review does not establish liquidity depth, distribution quality, market value, or listing eligibility.

## Base Market and Warning Evidence

| Evidence | Public reference | Current status |
| --- | --- | --- |
| PNET/USDC pool | [Uniswap v4 pool](https://app.uniswap.org/explore/pools/base/0xff481004f38fc7db43f3e3b47f6ad3e155482a00866d709d89700d303b0b4f3a) | Exists; very small seed liquidity |
| Liquidity position | [Uniswap v4 position 2731162](https://app.uniswap.org/positions/v4/base/2731162) | Position reference only; not proof of a lock or burn |
| Successful buy | Transaction link not yet recorded | Needs on-chain evidence |
| Successful sell | Transaction link not yet recorded | Needs on-chain evidence |
| Auction | [PNET CCA](https://app.uniswap.org/explore/auctions/base/0x777900C0FF11845c8e0D6C134b58C695023Aab4e); launcher tx `0xcaca93427d8d2a3c29704373e2906ca8e8ce5c84fe5198ce48e9b5726951cb54` | Active; scheduled to end 2026-07-18 02:59:59 UTC |
| LP configuration | Approximately 3,559,314 PNET / 75% of auctioned PNET configured for LP; recipient `0xe684c6a25fcced415a5b503bf9738abf7873d023` | Configuration recorded; final LP-addition transaction and position pending |
| LP timelock | Configured through 2026-08-17 02:59:59 UTC | Final migrated LP proof pending; do not call the seed position locked |
| Uniswap CCA verification | [Readiness plan](25_UNISWAP_CCA_VERIFIED_LISTING_PLAN.md) | No badge claimed; three-of-four public identity/traction requirements not currently evidenced |
| Holder distribution | [Block `48,477,164` snapshot](../data/on-chain-proofs/base-holder-distribution-2026-07-11.md) recorded | Maintainer-reported project/founder control of the top two addresses is at least `89.747111457500%`; custody/vesting proof and genuine improvement remain open |
| Blockaid false-positive submission | Not evidenced in this dossier | Submit verified-source packet and record date/ticket status |
| Warning cleared | Not complete | Warning remains displayed pending provider update |

Remediation must strengthen the evidence for the existing v4 market. Do not create a duplicate v2 pool merely to burn its LP token. Do not wash trade, self-trade for appearance, buy fake volume, or split balances across controlled wallets to manufacture holder count.

## Legacy Algorand Asset Identity

| Field | Value | Source | Status |
| --- | --- | --- | --- |
| Brand | testedprofit / Profitnet | Provided project brief and public pages | Needs verification |
| Token name | ProfitNet | [Dated public-indexer proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) | Verified by public indexers at capture round; recheck before external use |
| Unit | PNET | [Dated public-indexer proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) | Verified by public indexers at capture round; recheck before external use |
| Network | Algorand MainNet | [Dated public-indexer proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) | Verified at capture round; recheck before external use |
| ASA ID | 3169177585 | [Dated public-indexer proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) | Verified by public indexers at capture round; recheck before external use |

## ASA Control Fields

The [dated public-indexer proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) records the following capture-round values. Recheck them before external use.

| Control field | Status |
| --- | --- |
| Creator address | Verified by public indexers at capture round |
| Manager address | Verified current zero address at capture round |
| Reserve address | Verified current zero address at capture round |
| Freeze address | Verified current zero address at capture round |
| Clawback address | Verified current zero address at capture round |
| Default frozen state | Verified `false` at capture round |
| Asset URL / metadata URL | Verified as the ASA URL field at capture round |
| Metadata hash, if present | No metadata hash observed in the captured parameters |

## Supply and Decimals

| Field | Page-displayed value | Verification status |
| --- | --- | --- |
| Total supply | 100,000,000 PNET | Verified by public indexers at capture round; recheck before external use |
| Decimals | 6 | Verified by public indexers at capture round; recheck before external use |
| Raw total | 100,000,000,000,000 raw units | Verified by public indexers at capture round; recheck before external use |

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
- The verified Base contract has no contract-level honeypot mechanics, but the third-party warning remains visible until Blockaid or downstream wallet surfaces update.
- Very small liquidity and holder concentration are real market-risk and diligence issues even when contract-level honeypot mechanics are absent.
- Any issuer-, founder-, treasury-, affiliate-, or related-party-funded repurchase, liquidity-support, or market-support program requires qualified counsel review and counsel-approved material disclosure before a token sale. It must not be described as a price floor, guaranteed liquidity, appreciation mechanism, or return promise.
- Bridge availability does not imply exchange support or Coinbase listing.
- No reader should connect a wallet, sign a transaction, transfer assets, or provide credentials to verify this dossier.

## Claims Policy

Public claims must follow [docs/06_PUBLIC_CLAIMS_POLICY.md](06_PUBLIC_CLAIMS_POLICY.md).

## Human Verification Checklist

| Check | Status |
| --- | --- |
| Finish BaseScan token profile/logo approval and record approval date | Pending external review |
| Include verified Base source and deployment transaction in remediation packet | Ready to assemble |
| Record a successful Base buy transaction with date, amount, and outcome | Needs on-chain evidence |
| Record a successful Base sell transaction with date, amount, and outcome | Needs on-chain evidence |
| Document auction evidence if an auction was used; otherwise state none was used | Needs verification |
| Document any LP lock/burn mechanism without treating the v4 position page as lock proof | Needs on-chain evidence |
| Publish dated Base holder-concentration snapshots and improve distribution honestly | Initial block-pinned snapshot and maintainer-supplied founder-control label published; custody/vesting evidence, periodic refresh, and genuine improvement remain open |
| If a repurchase or market-support program is planned, complete counsel review and counsel-approved sale disclosure before any token sale | This dossier does not approve or authorize a program or sale term; full confidential funding-source details belong only in private counsel/compliance records |
| Submit false-positive evidence through Blockaid's report portal; reference its ticket in any optional Uniswap support follow-up | Needs external submission evidence |
| Confirm warning removal on each affected surface before marking resolved | Pending external update |
| Recheck ASA ID, asset name, unit, total, decimals, URL, and metadata-hash presence | Verified at capture round; refresh before external submission |
| Recheck creator, manager, reserve, freeze, and clawback addresses | Verified at capture round; refresh before external submission |
| Recheck whether manager / freeze / clawback controls remain zeroed | Verified at capture round; refresh before external submission |
| Verify burned supply from transactions, burn addresses, or explorer records | Needs verification |
| Verify founder allocation lock mechanism and address/account evidence | Needs on-chain verification |
| Verify strategic reserve lock mechanism and address/account evidence | Needs on-chain verification |
| Verify Sept 2026 unlock mechanics and exact date/time, if applicable | Needs on-chain verification |
| Verify LP/vault labels against pool IDs, balances, and asset pairs | Needs on-chain verification |
| Save dated screenshots with source URL and capture time | Needs verification |
| Confirm no exchange, bridge, or Coinbase support is implied | Needs verification |
