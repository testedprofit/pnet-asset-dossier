# PNET On-Chain Review Record

Review date: 2026-06-27

Asset: ProfitNet / PNET
ASA ID: `3169177585`

This record contains dated observations from public read-only sources. It does not contain code, secrets, wallet logic, signing logic, transaction submission logic, or investment recommendations.

## Sources Used

| Source | URL | Capture date | Access result |
| --- | --- | --- | --- |
| Algonode asset endpoint | https://mainnet-idx.algonode.cloud/v2/assets/3169177585 | 2026-06-27 | JSON returned |
| Nodely asset endpoint | https://mainnet-idx.4160.nodely.dev/v2/assets/3169177585 | 2026-06-27 | JSON returned |
| Algonode balances endpoint | https://mainnet-idx.algonode.cloud/v2/assets/3169177585/balances?limit=1000&include-all=false | 2026-06-27 | JSON returned |
| Algonode creator account endpoint | https://mainnet-idx.algonode.cloud/v2/accounts/7FRTVAZ5KCEF2CDCJACZHLLHH5QF3DTC7R4IV4KJO4K3P7TMD75ADU3Y5E | 2026-06-27 | JSON returned |
| Vestige API docs | https://api.vestigelabs.org/docs | 2026-06-27 | OpenAPI docs returned |
| Vestige asset API | https://api.vestigelabs.org/assets?asset_ids=3169177585&network_id=0 | 2026-06-27 | JSON returned |
| Vestige asset list API | https://api.vestigelabs.org/assets/list?asset_ids=3169177585&network_id=0&extended=true | 2026-06-27 | JSON returned |
| Vestige price API | https://api.vestigelabs.org/assets/price?asset_ids=3169177585&network_id=0 | 2026-06-27 | JSON returned |
| Vestige price API, USDC denominator | https://api.vestigelabs.org/assets/price?asset_ids=3169177585&network_id=0&denominating_asset_id=31566704 | 2026-06-27 | JSON returned |
| Vestige pools API | https://api.vestigelabs.org/pools?asset_1_id=3169177585&network_id=0 and https://api.vestigelabs.org/pools?asset_2_id=3169177585&network_id=0 | 2026-06-27 | JSON returned |
| Vestige protocols API | https://api.vestigelabs.org/protocols?network_id=0 | 2026-06-27 | JSON returned |
| testedprofit tokenomics page | https://testedprofit.com/pages/tokenomics/ | 2026-06-27 | HTML returned |
| testedprofit PNET page | https://testedprofit.com/pages/PNET/ | 2026-06-27 | HTML returned |
| Vestige web page | https://vestige.fi/asset/3169177585 | 2026-06-27 | Page returned |
| Lora | https://lora.algokit.io/mainnet/asset/3169177585 | 2026-06-27 | Page returned |
| Allo | https://allo.info/asset/3169177585 | 2026-06-27 | Page returned |
| Pera Explorer | https://explorer.perawallet.app/asset/3169177585/ | 2026-06-27 | Automated request returned 403; manual browser review recommended |

## ASA Metadata

| Field | Observed value | Source | Status |
| --- | --- | --- | --- |
| ASA ID | 3169177585 | Algonode, Nodely, Vestige asset API | Verified by public sources |
| Name | ProfitNet | Algonode, Nodely, Vestige asset API | Verified by public sources |
| Unit / ticker | PNET | Algonode, Nodely, Vestige asset API | Verified by public sources |
| Decimals | 6 | Algonode, Nodely, Vestige asset API | Verified by public sources |
| Total raw supply | 100000000000000 | Algonode, Nodely, Vestige asset API | Verified by public sources |
| Display supply | 100,000,000 PNET | Derived from raw supply and decimals | Verified derivation |
| URL | https://testedprofit.com | Algonode, Nodely, Vestige asset API | Verified by public sources |
| Creator | `7FRTVAZ5KCEF2CDCJACZHLLHH5QF3DTC7R4IV4KJO4K3P7TMD75ADU3Y5E` | Algonode, Nodely, Vestige asset API | Verified by public sources |
| Manager | zero address / null in Vestige | Algonode, Nodely, Vestige asset API | Appears cleared; verify in explorer |
| Reserve | zero address / null in Vestige | Algonode, Nodely, Vestige asset API | Appears cleared; verify in explorer |
| Freeze | zero address / null in Vestige | Algonode, Nodely, Vestige asset API | Appears cleared; verify in explorer |
| Clawback | zero address / null in Vestige | Algonode, Nodely, Vestige asset API | Appears cleared; verify in explorer |
| Default frozen | false | Algonode, Nodely | Verified by public sources |
| Metadata hash | Not returned in observed responses | Algonode, Nodely, Vestige asset API | Needs verification |

Zero address observed for Algonode/Nodely control fields: `AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAY5HFKQ`.

## Supply Claims

| Claim | Observed value | Source | Capture date | Status |
| --- | --- | --- | --- | --- |
| Total supply | 100,000,000 PNET | Algonode, Nodely | 2026-06-27 | Verified |
| Tokenomics-page total supply | 100,000,000 | testedprofit tokenomics page | 2026-06-27 | Matches on-chain display supply |
| Tokenomics-page burned supply | 8,180,000 | testedprofit tokenomics page | 2026-06-27 | Needs on-chain verification |
| Tokenomics-page burn percentage | ~8.18% of supply | testedprofit tokenomics page | 2026-06-27 | Arithmetic matches page claim, burn evidence Needs verification |
| Vestige burn supply | 11,951.548223 PNET | Vestige asset list API | 2026-06-27 | Needs methodology review |
| Vestige circulating supply | 57,022,465.072692 PNET | Vestige asset list API | 2026-06-27 | Needs methodology review |
| Vestige vault supply | 42,950,000 PNET | Vestige asset list API | 2026-06-27 | Needs methodology review |
| Vestige vault lockup | 23,804,996.5799 PNET | Vestige asset list API | 2026-06-27 | Needs methodology review |
| Founder allocation | 25M PNET locked | testedprofit tokenomics page | 2026-06-27 | Needs on-chain lock verification |
| Strategic reserve | 15M PNET locked | testedprofit tokenomics page | 2026-06-27 | Needs on-chain lock verification |
| Major unlock | 25% supply lock, Sept 2026 | testedprofit tokenomics page | 2026-06-27 | Needs on-chain lock verification |

## Holder Review

| Metric | Value | Source | Capture date |
| --- | --- | --- | --- |
| Balance rows | 278 | Algonode balances | 2026-06-27 |
| Positive-balance rows | 164 | Algonode balances | 2026-06-27 |
| Positive-balance sum | 100,000,000 PNET | Algonode balances | 2026-06-27 |
| Top 1 concentration | 25.0000% | Algonode balances | 2026-06-27 |
| Top 5 concentration | 53.3871% | Algonode balances | 2026-06-27 |
| Top 10 concentration | 67.4709% | Algonode balances | 2026-06-27 |
| Top 25 concentration | 88.7874% | Algonode balances | 2026-06-27 |

| Rank | Address | PNET | % total supply | Label status |
| --- | --- | --- | --- | --- |
| 1 | `SOXJ2B22OCMO6SQ6LXXP6ENU4GEIYXRV2BYGLO2BXVIGR6CVCVUYHPEUM4` | 25,000,000.000000 | 25.0000% | Needs human confirmation |
| 2 | `VUD4HX4NJMZK4RRVMRPWVI6Q5GVRUAJKTI6EMPC3DIP35RVY3XTGCKG6H4` | 13,950,000.000000 | 13.9500% | Needs human confirmation |
| 3 | `JBRJ6OMCEQ53LDCSVYUYE2O2JU5KEKWVMOTYQDX4JYWS6VVDHAZYZFRCEY` | 6,226,322.543084 | 6.2263% | Needs human confirmation |
| 4 | `KOQ2VGDA2D5CXTDRVVZJTF444KYC4GWSB4O63NOWMROZHOQQTFXHXIUC5Y` | 4,125,415.000000 | 4.1254% | Needs human confirmation |
| 5 | `ZV3BXXH5RGT6VJ7XYR23A2WUJZJDMDUR3DLFWI3DGOA3XOG63L67H737KQ` | 4,085,412.000000 | 4.0854% | Needs human confirmation |
| 6 | `ANESQRCMZ5KWZFKDGESLJEWQLRCVUZU725FJL7NO3BMKJEYMAB3TR56R3E` | 3,540,992.280511 | 3.5410% | Vestige pool address; verify manually |
| 7 | `Z73MIT3H2VL5LR7DVLVI3QKOSVTNWQQXLC2PXHU7NBYGFYCQPOHOL4GJBA` | 2,784,301.387036 | 2.7843% | Vestige pool address; verify manually |
| 8 | `DBPWDV5337ESJ632GN5BONBO6AFUV3MRBSVZTTDCL6HM3LNVC2YPRAVCD4` | 2,691,859.483721 | 2.6919% | Needs human confirmation |
| 9 | `F474OPCGUA2VWTFRLPOMQLFYX7Q7BXSEGO4NJ3H772DWZPQTQ75GE4JBIQ` | 2,551,106.783673 | 2.5511% | Vestige pool address; verify manually |
| 10 | `CRHTZABNJDTFNCZGSMNZ6LOADANPQA4YMUGXH3JKZLKKU276IXAFTAPGGY` | 2,515,534.640664 | 2.5155% | Needs human confirmation |

Creator account observed PNET balance: 11,876.211725 PNET. Source: Algonode account endpoint, captured 2026-06-27.

## Liquidity Review

| Item | Observed value | Source | Capture date | Status |
| --- | --- | --- | --- | --- |
| Vestige rank | 518 | Vestige asset list API | 2026-06-27 | Snapshot only |
| Vestige confidence | 0.787770787681174 | Vestige asset list API | 2026-06-27 | Snapshot only |
| Vestige price, ALGO denominator | 0.000065844 ALGO | Vestige asset list API | 2026-06-27 | Snapshot only |
| Vestige price, USDC denominator | 0.000005677841937429975 USDC | Vestige price API | 2026-06-27 | Snapshot only |
| Vestige market cap | 3754.5871902463323 | Vestige asset list API | 2026-06-27 | Snapshot only; denomination/methodology Needs review |
| Vestige FDMC | 6584.400000000001 | Vestige asset list API | 2026-06-27 | Snapshot only; denomination/methodology Needs review |
| Vestige TVL | 3159.8930732080294 | Vestige asset list API | 2026-06-27 | Snapshot only; denomination/methodology Needs review |
| Vestige 1h volume | 22.006414000000003 | Vestige asset list API | 2026-06-27 | Snapshot only; denomination/methodology Needs review |
| Vestige 1d volume | 46.996801 | Vestige asset list API | 2026-06-27 | Snapshot only; denomination/methodology Needs review |
| Vestige 7d volume | 310.0676459999999 | Vestige asset list API | 2026-06-27 | Snapshot only; denomination/methodology Needs review |
| Vestige 1h swaps | 10 | Vestige asset list API | 2026-06-27 | Snapshot only |
| Vestige 1d swaps | 32 | Vestige asset list API | 2026-06-27 | Snapshot only |
| Vestige 7d swaps | 388 | Vestige asset list API | 2026-06-27 | Snapshot only |

| Protocol | Vestige protocol id | Pool records | Nonzero PNET pools | PNET supply in pools | Source |
| --- | --- | --- | --- | --- | --- |
| Tinyman v2 | 2 | 81 | 26 | 15,819,129.189921 PNET | Vestige protocols and pools APIs |
| Pact | 3 | 29 | 24 | 14,640,619.288858 PNET | Vestige protocols and pools APIs |
| Total | 2 and 3 | 110 | 50 | 30,459,748.478779 PNET | Vestige pools API |

## Control-Risk Notes

| Field | Observed state | Review note |
| --- | --- | --- |
| Manager | Zero address / null | Strong trust point; verify in explorers |
| Reserve | Zero address / null | Strong trust point; verify in explorers |
| Freeze | Zero address / null | Strong trust point; verify in explorers |
| Clawback | Zero address / null | Strong trust point; verify in explorers |
| Default frozen | false | Strong trust point |

The manager, reserve, freeze, and clawback status improves listing-readiness if independently confirmed and documented with explorer screenshots or archived source records.

## Unknowns and Human Follow-Up

| Item | Status |
| --- | --- |
| Exact burn wallets and burn transaction set | Needs verification |
| Why tokenomics page burn claim differs from Vestige burn supply field | Needs verification |
| Circulating supply methodology | Needs verification |
| Founder allocation account and lock mechanism | Needs on-chain verification |
| Strategic reserve account and lock mechanism | Needs on-chain verification |
| Sept 2026 unlock mechanics | Needs on-chain verification |
| LP/vault wallet labels from tokenomics page | Needs human confirmation |
| Pool quality and counter-asset risk | Needs human review |
| Pera Explorer manual check | Needs verification |

## Public Claims Review

| Risky wording observed | Source | Safer wording |
| --- | --- | --- |
| Passive-income phrase | testedprofit tokenomics page and PNET page | `third-party partner offer; not a PNET return claim` |
| Earning-oriented partner copy | testedprofit PNET page | `external partner links; no token-return claim` |
| Secured / on-chain locked wording | testedprofit tokenomics page | `page-displayed lock claim; Needs on-chain verification` |
| Forever-locked vault wording | testedprofit tokenomics page | `page-displayed vault label; Needs on-chain verification` |

Do not convert partner offers, pool labels, or market pages into PNET return claims, passive-income claims, managed-strategy claims, copy-trading claims, exchange-listing claims, or Coinbase claims.
