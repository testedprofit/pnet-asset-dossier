# Public Links

Snapshot date: 2026-07-11

This file records public references used by the dossier. Links are source references only and do not imply endorsement, verification, liquidity, availability, or future support.

## Official / Brand-Controlled Pages

| Reference | URL | Snapshot note | Dossier status |
| --- | --- | --- | --- |
| testedprofit website | https://testedprofit.com | Public website reference | Needs verification |
| testedprofit tokenomics page | https://testedprofit.com/pages/tokenomics/ | Displayed PNET supply, burn, allocation, vault, and unlock claims | ASA identity/supply separately verified; burn, allocation, vault, and unlock claims need on-chain verification |
| testedprofit PNET page | https://testedprofit.com/pages/PNET/ | Displayed ASA ID and decimals, plus public site navigation | ASA ID and decimals verified by public indexers; page content remains a changeable public reference |
| PNET asset dossier | https://github.com/testedprofit/pnet-asset-dossier | Public documentation and media hub | Maintainer-controlled reference |
| Wallet-warning remediation record | ../docs/24_WALLET_WARNING_BLOCKAID_REMEDIATION.md | Verified-contract findings, evidence gaps, and current provider-remediation status | Maintainer-controlled reference; warning still displayed |
| 32x32 SVG token logo | https://raw.githubusercontent.com/testedprofit/pnet-asset-dossier/376be2dada8af8f8371bfc45516ca16be594060f/media/pnet-logo-32.svg | Commit-pinned token logo URL for explorer/wallet submissions | Maintainer-controlled reference |

## Base Public References

| Reference | URL | Snapshot note | Dossier status |
| --- | --- | --- | --- |
| Base ERC-20 token | https://basescan.org/token/0xe1f7f585f458cb6affcee2286b8482523b19ee5a | ProfitNet `PNET` token contract on Base | Source verified; token profile submitted and review pending |
| Base contract source | https://basescan.org/address/0xe1F7F585f458cB6AFFCEE2286b8482523B19ee5a#code | BaseScan source verification reference | Verified source |
| Base deployment tx | https://basescan.org/tx/0x7d6300cb7f84d18fdaeafe3c34195e946ec86e6ce8c91d87d577177873b39fd1 | Base deployment transaction | Public chain reference |
| Uniswap PNET/USDC v4 pool | https://app.uniswap.org/explore/pools/base/0xff481004f38fc7db43f3e3b47f6ad3e155482a00866d709d89700d303b0b4f3a | Small seed-liquidity pool | Third-party UI reference |
| Uniswap PNET/USDC v4 price chart | https://app.uniswap.org/explore/pools/base/0xff481004f38fc7db43f3e3b47f6ad3e155482a00866d709d89700d303b0b4f3a?chart=price | Pool chart view for price snapshots | Third-party UI reference |
| Uniswap PNET/USDC v4 position | https://app.uniswap.org/positions/v4/base/2731162 | Liquidity position reference | Third-party UI reference |

## Wallet-Warning and False-Positive References

| Reference | URL | Snapshot note | Dossier status |
| --- | --- | --- | --- |
| Uniswap token-warning explanation | https://support.uniswap.org/hc/en-us/articles/8723118437133-What-are-token-warnings | Explains that Uniswap token warnings are supplied by Blockaid and that disputes should be directed to Blockaid | Official Uniswap support reference |
| Blockaid report portal | https://report.blockaid.io/ | Includes the route to report a mistake or false-positive result | Official remediation route; PNET submission not evidenced in this dossier |

## Third-Party Public References

| Reference | URL | Snapshot note | Dossier status |
| --- | --- | --- | --- |
| Vestige asset page | https://vestige.fi/asset/3169177585 | Displayed ProfitNet / PNET listing and market metrics | Third-party snapshot only |
| Allo asset page | https://allo.info/asset/3169177585 | Page reachable, detailed static asset data not captured during review | Needs manual follow-up |

## Explorer / Data Source References

| Reference | URL | Snapshot note | Dossier status |
| --- | --- | --- | --- |
| Pera Explorer | https://explorer.perawallet.app/asset/3169177585/ | ASA explorer reference | Needs verification |
| Lora | https://lora.algokit.io/mainnet/asset/3169177585 | ASA explorer reference | Needs verification |
| Algonode Indexer API | https://mainnet-idx.algonode.cloud/v2/assets/3169177585 | Public read-only indexer endpoint | Used in dated capture proof; recheck for current state |
| Nodely Indexer API | https://mainnet-idx.4160.nodely.dev/v2/assets/3169177585 | Public read-only indexer endpoint | Used in dated capture proof; recheck for current state |
| Additional API/data source registry | ../docs/11_API_AND_DATA_SOURCES.md | Diligence source registry | Reference only |

## Verification Follow-Up

| Task | Status |
| --- | --- |
| Refresh the direct Algorand indexer capture for ASA metadata | Dated capture proof exists; refresh before external use |
| Reconfirm asset name, unit, decimals, and total supply from public indexers | Verified at capture round; refresh before external use |
| Confirm founder allocation, strategic reserve, LP vaults, and partner vaults from on-chain records | Needs verification |
| Capture dated screenshots for official pages and third-party listings | Needs verification |
| Finish BaseScan profile/logo approval and record the result | Pending external review |
| Record successful Base buy and sell transaction links | Needs on-chain evidence |
| Document any auction and LP-lock/burn evidence without treating the v4 position as lock proof | Needs verification |
| Publish a dated Base holder-distribution snapshot and improve concentration honestly | Needs verification |
| Submit the verified-source false-positive packet through Blockaid's report portal; reference its ticket in any optional Uniswap support follow-up | Needs external submission evidence |
| Confirm warning removal before marking the remediation complete | Pending external provider update |
