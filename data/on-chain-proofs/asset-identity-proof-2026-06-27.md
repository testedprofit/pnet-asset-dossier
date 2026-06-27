# PNET Asset Identity Proof

Capture date: 2026-06-27
Network: Algorand MainNet
ASA ID: `3169177585`
Reviewer: Codex local review
Status: Verified by public indexers at capture round; recheck before external publication.

## Sources

| Source | URL | Capture round |
| --- | --- | --- |
| Algonode Indexer | `https://mainnet-idx.algonode.cloud/v2/assets/3169177585` | `62554271` |
| Nodely Indexer | `https://mainnet-idx.4160.nodely.dev/v2/assets/3169177585` | `62554271` |
| Algonode transaction query | `https://mainnet-idx.algonode.cloud/v2/transactions?asset-id=3169177585&tx-type=acfg&limit=10` | `62554262` |

## Observed Asset Parameters

| Field | Observed value | Status |
| --- | --- | --- |
| Asset ID | `3169177585` | Verified |
| Name | `ProfitNet` | Verified |
| Unit | `PNET` | Verified |
| Decimals | `6` | Verified |
| Raw total | `100000000000000` | Verified |
| Display total | `100,000,000` PNET | Verified |
| URL | `https://testedprofit.com` | Verified as ASA URL field |
| Created at round | `52678300` | Verified |
| Creator | `7FRTVAZ5KCEF2CDCJACZHLLHH5QF3DTC7R4IV4KJO4K3P7TMD75ADU3Y5E` | Verified |
| Default frozen | `false` | Verified |

## Current Control Fields

The current control fields are the Algorand zero address:

`AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAY5HFKQ`

| Field | Observed value | Status |
| --- | --- | --- |
| Manager | `AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAY5HFKQ` | Verified current value |
| Reserve | `AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAY5HFKQ` | Verified current value |
| Freeze | `AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAY5HFKQ` | Verified current value |
| Clawback | `AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAY5HFKQ` | Verified current value |

Interpretation: At the capture round, public indexers reported no nonzero manager, reserve, freeze, or clawback address. This supports the narrow statement that current ASA control fields are zeroed. It does not by itself verify any broader tokenomics, lock, vault, or burn claim.

## Asset Creation Transaction

| Field | Observed value |
| --- | --- |
| Transaction ID | `WZJQENKDUTA36XE3SKYZD37D45NFP4WXWHP5LGRPVSNKNGGZJMJA` |
| Confirmed round | `52678300` |
| Sender / creator | `7FRTVAZ5KCEF2CDCJACZHLLHH5QF3DTC7R4IV4KJO4K3P7TMD75ADU3Y5E` |
| Transaction type | `acfg` |
| Created asset index | `3169177585` |
| Raw total | `100000000000000` |
| Decimals | `6` |
| URL | `https://testedprofit.com` |

Explorer link:

`https://lora.algokit.io/mainnet/transaction/WZJQENKDUTA36XE3SKYZD37D45NFP4WXWHP5LGRPVSNKNGGZJMJA`

## Limits of This Proof

This proof does not verify:

- burned supply,
- locked supply,
- circulating supply,
- LP/vault labels,
- founder or strategic reserve lock status,
- creator wallet access status,
- operational wallet role or control model,
- any exchange/listing/bridge support.

Current Gate Status: ASA IDENTITY, TOTAL SUPPLY, DECIMALS, CREATION TRANSACTION, AND CURRENT CONTROL FIELDS VERIFIED BY PUBLIC INDEXERS; TOKENOMICS CLAIMS REMAIN SEPARATE.
