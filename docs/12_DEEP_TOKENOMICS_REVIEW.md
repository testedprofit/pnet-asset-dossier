# Deep Tokenomics and On-Chain Review

Review date: 2026-06-27

Asset: ProfitNet / PNET
ASA ID: `3169177585`

This is a dated, read-only review of public on-chain, website, and market-reference data. It is not financial, legal, trading, bridge, custody, or listing advice. It does not recommend buying, selling, holding, bridging, depositing, or transferring any asset.

Detailed review record: [data/on-chain-review/pnet-review-2026-06-27.md](../data/on-chain-review/pnet-review-2026-06-27.md)
API/source registry: [data/api-sources/pnet-api-sources.md](../data/api-sources/pnet-api-sources.md)

## Source Summary

| Source | URL | Capture date | Use |
| --- | --- | --- | --- |
| Algonode Indexer asset endpoint | https://mainnet-idx.algonode.cloud/v2/assets/3169177585 | 2026-06-27 | ASA metadata and controls |
| Nodely Indexer asset endpoint | https://mainnet-idx.4160.nodely.dev/v2/assets/3169177585 | 2026-06-27 | ASA metadata and controls cross-check |
| Algonode holder balances | https://mainnet-idx.algonode.cloud/v2/assets/3169177585/balances?limit=1000&include-all=false | 2026-06-27 | Holder and concentration review |
| Vestige asset page | https://vestige.fi/asset/3169177585 | 2026-06-27 | Market reference |
| Vestige Labs API | https://api.vestigelabs.org/docs | 2026-06-27 | Asset, price, composition, and pool data |
| testedprofit website | https://testedprofit.com | 2026-06-27 | Public brand/site reference |
| testedprofit tokenomics page | https://testedprofit.com/pages/tokenomics/ | 2026-06-27 | Public tokenomics-page claims |
| testedprofit PNET page | https://testedprofit.com/pages/PNET/ | 2026-06-27 | Public page and claims review |

## 1. ASA Metadata

Algonode and Nodely returned matching ASA metadata on 2026-06-27.

| Field | Observed value | Source | Status |
| --- | --- | --- | --- |
| ASA ID | 3169177585 | Algonode, Nodely | Verified by two public indexers |
| Name | ProfitNet | Algonode, Nodely | Verified by two public indexers |
| Unit | PNET | Algonode, Nodely | Verified by two public indexers |
| Decimals | 6 | Algonode, Nodely | Verified by two public indexers |
| Total raw supply | 100000000000000 | Algonode, Nodely | Verified by two public indexers |
| Display supply | 100,000,000 PNET | Derived from raw supply and decimals | Verified derivation |
| URL | https://testedprofit.com | Algonode, Nodely | Verified by two public indexers |
| Metadata hash | Not returned in observed indexer response | Algonode, Nodely | Needs verification |
| Creator | `7FRTVAZ5KCEF2CDCJACZHLLHH5QF3DTC7R4IV4KJO4K3P7TMD75ADU3Y5E` | Algonode, Nodely | Verified by two public indexers |
| Manager | `AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAY5HFKQ` | Algonode, Nodely | Appears cleared; verify in explorer |
| Reserve | `AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAY5HFKQ` | Algonode, Nodely | Appears cleared; verify in explorer |
| Freeze | `AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAY5HFKQ` | Algonode, Nodely | Appears cleared; verify in explorer |
| Clawback | `AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAY5HFKQ` | Algonode, Nodely | Appears cleared; verify in explorer |
| Default frozen | false | Algonode, Nodely | Verified by two public indexers |

## 2. Supply Review

| Item | Observed value | Source | Capture date | Status |
| --- | --- | --- | --- | --- |
| Total supply | 100,000,000 PNET | Algonode, Nodely | 2026-06-27 | Verified by two public indexers |
| Burned supply claim | 8,180,000 PNET | testedprofit tokenomics page | 2026-06-27 | Needs on-chain verification |
| Vestige burn supply field | 11,951.548223 PNET | Vestige Labs `/assets/list` | 2026-06-27 | Needs methodology review |
| Website circulating / fully diluted text | Page text includes `Circulating` near `100,000,000 Fully Diluted` | testedprofit tokenomics page | 2026-06-27 | Ambiguous; Needs verification |
| Vestige circulating supply field | 57,022,465.072692 PNET | Vestige Labs `/assets/list` | 2026-06-27 | Needs methodology review |
| Founder allocation shown | 25M PNET locked | testedprofit tokenomics page | 2026-06-27 | Needs on-chain lock verification |
| Strategic reserve shown | 15M PNET locked | testedprofit tokenomics page | 2026-06-27 | Needs on-chain lock verification |
| Major unlock shown | 25% supply lock, Sept 2026 | testedprofit tokenomics page | 2026-06-27 | Needs on-chain lock verification |
| Vestige vault supply field | 42,950,000 PNET | Vestige Labs `/assets/list` | 2026-06-27 | Needs methodology review |
| Vestige vault lockup field | 23,804,996.5799 PNET | Vestige Labs `/assets/list` | 2026-06-27 | Needs methodology review |

The tokenomics-page burn claim and the Vestige API burn-supply field do not match. That does not prove either value is wrong, but it does mean burn methodology and burn addresses must be verified before making public supply statements.

## 3. Holder and Wallet Review

Algonode balances returned 278 balance rows and 164 positive-balance rows on 2026-06-27. Positive balances summed to the full 100,000,000 PNET display supply.

| Concentration metric | Observed value | Source | Capture date | Status |
| --- | --- | --- | --- | --- |
| Top holder | 25.0000% of supply | Algonode balances | 2026-06-27 | Verified balance; label needs confirmation |
| Top 5 holders | 53.3871% of supply | Algonode balances | 2026-06-27 | Verified balances; labels need confirmation |
| Top 10 holders | 67.4709% of supply | Algonode balances | 2026-06-27 | Verified balances; labels need confirmation |
| Top 25 holders | 88.7874% of supply | Algonode balances | 2026-06-27 | Verified balances; labels need confirmation |
| Creator balance | 11,876.211725 PNET | Algonode account endpoint | 2026-06-27 | Verified balance |

Top observed holders:

| Rank | Address | PNET | % total supply | Preliminary note |
| --- | --- | --- | --- | --- |
| 1 | `SOXJ2B22OCMO6SQ6LXXP6ENU4GEIYXRV2BYGLO2BXVIGR6CVCVUYHPEUM4` | 25,000,000.000000 | 25.0000% | Matches page-displayed founder allocation size; label Needs verification |
| 2 | `VUD4HX4NJMZK4RRVMRPWVI6Q5GVRUAJKTI6EMPC3DIP35RVY3XTGCKG6H4` | 13,950,000.000000 | 13.9500% | Large holder; label Needs verification |
| 3 | `JBRJ6OMCEQ53LDCSVYUYE2O2JU5KEKWVMOTYQDX4JYWS6VVDHAZYZFRCEY` | 6,226,322.543084 | 6.2263% | Label Needs verification |
| 4 | `KOQ2VGDA2D5CXTDRVVZJTF444KYC4GWSB4O63NOWMROZHOQQTFXHXIUC5Y` | 4,125,415.000000 | 4.1254% | Label Needs verification |
| 5 | `ZV3BXXH5RGT6VJ7XYR23A2WUJZJDMDUR3DLFWI3DGOA3XOG63L67H737KQ` | 4,085,412.000000 | 4.0854% | Label Needs verification |
| 6 | `ANESQRCMZ5KWZFKDGESLJEWQLRCVUZU725FJL7NO3BMKJEYMAB3TR56R3E` | 3,540,992.280511 | 3.5410% | Vestige shows this address as a Tinyman v2 pool address; verify manually |
| 7 | `Z73MIT3H2VL5LR7DVLVI3QKOSVTNWQQXLC2PXHU7NBYGFYCQPOHOL4GJBA` | 2,784,301.387036 | 2.7843% | Vestige shows this address as a Pact pool address; verify manually |
| 8 | `DBPWDV5337ESJ632GN5BONBO6AFUV3MRBSVZTTDCL6HM3LNVC2YPRAVCD4` | 2,691,859.483721 | 2.6919% | Label Needs verification |
| 9 | `F474OPCGUA2VWTFRLPOMQLFYX7Q7BXSEGO4NJ3H772DWZPQTQ75GE4JBIQ` | 2,551,106.783673 | 2.5511% | Vestige shows this address as a Tinyman v2 pool address; verify manually |
| 10 | `CRHTZABNJDTFNCZGSMNZ6LOADANPQA4YMUGXH3JKZLKKU276IXAFTAPGGY` | 2,515,534.640664 | 2.5155% | Label Needs verification |

Concentration risk is material. Some large holders appear to be pool addresses, but wallet labels need human confirmation before using them in public summaries.

## 4. Liquidity Review

Vestige public API data captured on 2026-06-27 reported:

| Metric | Observed value | Source | Status |
| --- | --- | --- | --- |
| PNET-related pool records | 110 | Vestige `/pools` for asset_1 and asset_2 | Snapshot only |
| Pools with nonzero PNET supply | 50 | Vestige `/pools` | Snapshot only |
| Tinyman v2 PNET pool records | 81 total, 26 nonzero | Vestige `/pools`, protocol id 2 | Snapshot only |
| Pact PNET pool records | 29 total, 24 nonzero | Vestige `/pools`, protocol id 3 | Snapshot only |
| PNET in nonzero pools | 30,459,748.478779 PNET | Vestige `/pools` | Snapshot only |
| Vestige total lockup | 30,459,748.478779 PNET | Vestige `/assets/price` and `/assets/list` | Snapshot only |
| Vestige price in ALGO | 0.000065844 ALGO | Vestige `/assets/list` | Volatile snapshot only |
| Vestige price in USDC | 0.000005677841937429975 USDC | Vestige `/assets/price?denominating_asset_id=31566704` | Volatile snapshot only |
| Vestige 1d volume | 46.996801 | Vestige `/assets/list` | Volatile snapshot only; denomination requires source review |
| Vestige 1d swaps | 32 | Vestige `/assets/list` | Volatile snapshot only |
| Vestige TVL | 3159.8930732080294 | Vestige `/assets/list` | Volatile snapshot only; denomination requires source review |

Largest PNET pool balances observed through Vestige:

| Pool address | Venue / protocol id | Pair asset IDs | PNET in pool | Status |
| --- | --- | --- | --- | --- |
| `ANESQRCMZ5KWZFKDGESLJEWQLRCVUZU725FJL7NO3BMKJEYMAB3TR56R3E` | Tinyman v2 / 2 | PNET-ALGO | 3,319,006.606261 | Snapshot only |
| `Z73MIT3H2VL5LR7DVLVI3QKOSVTNWQQXLC2PXHU7NBYGFYCQPOHOL4GJBA` | Pact / 3 | PNET-1290751153 | 2,778,291.618672 | Snapshot only |
| `F474OPCGUA2VWTFRLPOMQLFYX7Q7BXSEGO4NJ3H772DWZPQTQ75GE4JBIQ` | Tinyman v2 / 2 | 3214347764-PNET | 2,508,577.195565 | Snapshot only |
| `JXXGCSQUUUGISZA5HKPWZMDLSMT5YHNW2LRHCO3V7IKSHTLH4PUPVBDRZ4` | Tinyman v2 / 2 | PNET-1115850955 | 1,991,889.369629 | Snapshot only |
| `SDLBQ3NACLCSJ5T574FIWIEH5G5VXWMN3BGMJHKDEUAUIGUB2N23ERDRKA` | Pact / 3 | 3436365167-PNET | 1,965,831.502951 | Snapshot only |

Liquidity risks:

- Many pools are small or paired with long-tail assets, which can increase slippage and price-impact risk.
- Pool count alone does not prove robust liquidity.
- One-sided PNET depth can make pair quality look stronger than it is if the counter-asset side is weak.
- Market and routing data changes quickly; all values here are stale after capture.

## 5. Control-Risk Review

The strongest on-chain trust point is that Algonode and Nodely both returned the Algorand zero address for manager, reserve, freeze, and clawback on 2026-06-27.

| Control | Observed value | Risk interpretation | Status |
| --- | --- | --- | --- |
| Manager | Zero address | Appears no active manager is set | Verify in explorers |
| Reserve | Zero address | Appears no active reserve is set | Verify in explorers |
| Freeze | Zero address | Appears no active freeze authority is set | Verify in explorers |
| Clawback | Zero address | Appears no active clawback authority is set | Verify in explorers |
| Default frozen | false | New holders are not default frozen per indexers | Verified by two indexers |

Listing-readiness improvements:

- Add explorer screenshots for the control fields.
- Add a reviewer-signed record that manager, reserve, freeze, and clawback were checked.
- Add transaction references showing when controls were set or cleared.
- Reconcile burn, vault, and lock claims against concrete accounts and transaction history.

## 6. Public Claims Review

The testedprofit tokenomics and PNET pages contain earning-oriented partner language. This dossier should not reuse that language as token utility or investment framing.

| Public-page wording type | Observed source | Review status | Safer replacement |
| --- | --- | --- | --- |
| Passive-income phrase | testedprofit tokenomics page and PNET page | Avoid in dossier except QA note | `third-party partner offer` |
| Earning-oriented partner wording | testedprofit PNET page | Avoid as token utility | `external partner links; not a PNET return claim` |
| `secured on-chain locked` style wording | testedprofit tokenomics page | Needs on-chain verification before repeating as fact | `page-displayed lock claim; Needs on-chain verification` |
| `forever locked` LP vault wording | testedprofit tokenomics page | Needs on-chain verification before repeating as fact | `page-displayed vault label; Needs on-chain verification` |

Do not make outcome guarantees, passive-income claims, copy-trading claims, managed-strategy claims, Coinbase-listing claims, exchange-support claims, custody claims, or asset-transfer workflow claims.

## 7. API and Data Sources

See [data/api-sources/pnet-api-sources.md](../data/api-sources/pnet-api-sources.md) for source links, endpoint notes, access status, and allowed read-only usage.

## Review Conclusion

Strong trust points:

- Asset identity, decimals, total supply, URL, creator, and default frozen state are consistent across Algonode and Nodely.
- Manager, reserve, freeze, and clawback fields appear cleared to the zero address in both indexers.
- Vestige API asset metadata matches the core ASA identity fields.

Key risks:

- Holder concentration is high.
- Burned supply and circulating supply claims need reconciliation.
- Lock/vault labels are not independently verified in this review.
- Market liquidity is fragmented across many pools and likely includes micro-pool risk.
- Public pages include income-oriented wording that should not be reused as PNET positioning.
