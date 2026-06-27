# API and Data Sources

Status date: 2026-06-27

This file records public data sources that can support manual verification. It is documentation only and does not include implementation code, API keys, credentials, request examples, trading logic, or transaction logic.

## Asset and Explorer References

| Source | Link / endpoint | Use | Status |
| --- | --- | --- | --- |
| Vestige asset page | https://vestige.fi/asset/3169177585 | Market page and third-party asset reference | Snapshot only |
| Allo asset explorer | https://allo.info/asset/3169177585 | Asset explorer reference | Needs manual follow-up |
| Pera Explorer | https://explorer.perawallet.app/asset/3169177585/ | ASA metadata and account/explorer review | Needs verification |
| Lora | https://lora.algokit.io/mainnet/asset/3169177585 | ASA metadata and transaction review | Needs verification |

## Indexer APIs

These endpoints are public references for read-only verification. Do not add API keys or credentials to this repository.

| Source | Link / endpoint | Use | Status |
| --- | --- | --- | --- |
| Algonode Indexer API | https://mainnet-idx.algonode.cloud/v2/assets/3169177585 | ASA metadata lookup | Needs verification |
| Nodely Indexer API | https://mainnet-idx.4160.nodely.dev/v2/assets/3169177585 | ASA metadata lookup | Needs verification |
| Algorand Indexer docs | https://github.com/algorand/indexer | Indexer behavior reference | Reference only |

## Liquidity / Routing / Market Data

| Source | Link / endpoint | Use | Status |
| --- | --- | --- | --- |
| Vestige Labs API docs | https://api.vestigelabs.org/docs | Asset, pool, and market data research | Needs verification |
| Vestige free API docs | https://free-api.vestige.fi/docs | Public API research, if accessible | Needs verification |
| Tinyman docs | https://docs.tinyman.org/ | Tinyman protocol and pool data research | Needs verification |
| Tinyman app | https://tinyman.org/ | Public interface reference only | Needs verification |
| Pact app | https://www.pact.fi/ | Public liquidity venue reference only | Needs verification |
| Pact SDK documentation | https://pactfi.github.io/pact-py-sdk/latest/pactsdk/api.html | Pact pool data research | Needs verification |
| ASA Stats | https://www.asastats.com/ | ASA valuation and portfolio data reference | Needs verification |
| ASA Stats API / docs | https://www.asastats.com/api/ | API reference, if accessible | Needs verification |
| Folks Router docs | https://docs.folks.finance/functionalities/folks-router | Routing data research | Needs verification |
| Folks Finance | https://folks.finance/ | Public protocol reference only | Needs verification |

## Data Handling Rules

- Treat market data as stale immediately after capture.
- Record date, time, timezone, source, and observed value.
- Do not commit API keys, cookies, bearer tokens, session data, or credentials.
- Do not add scripts, SDK integrations, request examples, trading code, or transaction instructions.
- Do not imply venue support from a page, bridge, route, or analytics source.

