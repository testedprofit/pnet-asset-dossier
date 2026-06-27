# PNET API and Public Data Sources

Review date: 2026-06-27

This registry lists public read-only sources used or identified for PNET diligence. Do not add API keys, secrets, wallet credentials, signing code, transaction-submission code, or trading automation to this repository.

## Used in 2026-06-27 Review

| Source | Link / endpoint | Capture date | Result | Use |
| --- | --- | --- | --- | --- |
| Algonode Indexer asset endpoint | https://mainnet-idx.algonode.cloud/v2/assets/3169177585 | 2026-06-27 | JSON returned | ASA metadata and controls |
| Nodely Indexer asset endpoint | https://mainnet-idx.4160.nodely.dev/v2/assets/3169177585 | 2026-06-27 | JSON returned | ASA metadata and controls cross-check |
| Algonode holder balances | https://mainnet-idx.algonode.cloud/v2/assets/3169177585/balances?limit=1000&include-all=false | 2026-06-27 | JSON returned | Holder and concentration review |
| Algonode creator account | https://mainnet-idx.algonode.cloud/v2/accounts/7FRTVAZ5KCEF2CDCJACZHLLHH5QF3DTC7R4IV4KJO4K3P7TMD75ADU3Y5E | 2026-06-27 | JSON returned | Creator balance and created-asset review |
| Vestige asset API | https://api.vestigelabs.org/assets?asset_ids=3169177585&network_id=0 | 2026-06-27 | JSON returned | Asset metadata cross-check |
| Vestige asset list API | https://api.vestigelabs.org/assets/list?asset_ids=3169177585&network_id=0&extended=true | 2026-06-27 | JSON returned | Market, supply, lockup, volume, and swap fields |
| Vestige price API | https://api.vestigelabs.org/assets/price?asset_ids=3169177585&network_id=0 | 2026-06-27 | JSON returned | ALGO-denominated price and total lockup |
| Vestige price API, USDC denominator | https://api.vestigelabs.org/assets/price?asset_ids=3169177585&network_id=0&denominating_asset_id=31566704 | 2026-06-27 | JSON returned | USDC-denominated price |
| Vestige composition API | https://api.vestigelabs.org/assets/3169177585/composition?network_id=0 | 2026-06-27 | JSON returned | Protocol and pair composition context |
| Vestige pools API, PNET as asset 1 | https://api.vestigelabs.org/pools?asset_1_id=3169177585&network_id=0 | 2026-06-27 | JSON returned | Pool review |
| Vestige pools API, PNET as asset 2 | https://api.vestigelabs.org/pools?asset_2_id=3169177585&network_id=0 | 2026-06-27 | JSON returned | Pool review |
| Vestige protocols API | https://api.vestigelabs.org/protocols?network_id=0 | 2026-06-27 | JSON returned | Protocol id mapping |
| Vestige OpenAPI docs | https://api.vestigelabs.org/docs | 2026-06-27 | Swagger page returned | Endpoint reference |
| testedprofit tokenomics page | https://testedprofit.com/pages/tokenomics/ | 2026-06-27 | HTML returned | Public tokenomics claims and claims review |
| testedprofit PNET page | https://testedprofit.com/pages/PNET/ | 2026-06-27 | HTML returned | Public claims review |
| Lora | https://lora.algokit.io/mainnet/asset/3169177585 | 2026-06-27 | Page returned | Explorer reference for manual review |
| Allo | https://allo.info/asset/3169177585 | 2026-06-27 | Page returned | Explorer reference for manual review |
| Vestige web page | https://vestige.fi/asset/3169177585 | 2026-06-27 | Page returned | Market page reference |

## Identified for Follow-Up

| Source | Link | Suggested use | Status |
| --- | --- | --- | --- |
| Pera Explorer | https://explorer.perawallet.app/asset/3169177585/ | Manual ASA metadata/control review | Automated request returned 403; manual review recommended |
| Tinyman docs | https://docs.tinyman.org/ | Protocol and pool interpretation | Needs protocol-specific review |
| Tinyman app | https://tinyman.org/ | Manual pool review | Needs manual review |
| Pact app | https://www.pact.fi/ | Manual pool review | Needs manual review |
| Pact SDK docs | https://pactfi.github.io/pact-py-sdk/latest/pactsdk/api.html | Public Pact data reference | Needs review |
| ASA Stats | https://www.asastats.com/ | Holder/valuation cross-check | Needs review |
| ASA Stats API / docs | https://www.asastats.com/api/ | Public API research, if accessible | Needs review |
| Folks Router docs | https://docs.folks.finance/functionalities/folks-router | Routing context, if relevant | Needs review |
| Folks Finance | https://folks.finance/ | Protocol reference, if relevant | Needs review |

## Read-Only Endpoint Notes

These links are safe as documentation references because they are public read-only URLs and do not require secrets:

| Purpose | Endpoint |
| --- | --- |
| ASA metadata, Algonode | https://mainnet-idx.algonode.cloud/v2/assets/3169177585 |
| ASA metadata, Nodely | https://mainnet-idx.4160.nodely.dev/v2/assets/3169177585 |
| Holder balances, Algonode | https://mainnet-idx.algonode.cloud/v2/assets/3169177585/balances?limit=1000&include-all=false |
| Vestige asset metadata | https://api.vestigelabs.org/assets?asset_ids=3169177585&network_id=0 |
| Vestige extended asset data | https://api.vestigelabs.org/assets/list?asset_ids=3169177585&network_id=0&extended=true |
| Vestige PNET pools where PNET is asset 1 | https://api.vestigelabs.org/pools?asset_1_id=3169177585&network_id=0 |
| Vestige PNET pools where PNET is asset 2 | https://api.vestigelabs.org/pools?asset_2_id=3169177585&network_id=0 |

## Safety Rules

- Do not include private API keys.
- Do not include bearer tokens, cookies, session data, or wallet credentials.
- Do not add code that signs, submits, constructs, or automates transactions.
- Do not add trading bots, routing automation, bridge automation, or deployment automation.
- Treat market, TVL, volume, price, and route data as stale snapshots.
- Record capture date, source URL, observed value, and reviewer for future updates.
