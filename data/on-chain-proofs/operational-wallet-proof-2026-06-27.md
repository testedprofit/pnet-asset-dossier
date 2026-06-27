# PNET Operational Wallet Proof Snapshot

Capture date: 2026-06-27
Network: Algorand MainNet
Wallet: `CIVTUU6KLTYO26SPVEBDFBKP3UMZM2DPEO5RINODUVCI5NVIFC6HVNWS7E`
Reviewer: Codex local review
Status: Snapshot only for public account data; role/control model remains `Needs verification`.

## Source

| Source | URL | Capture round |
| --- | --- | --- |
| Algonode Indexer account endpoint | `https://mainnet-idx.algonode.cloud/v2/accounts/CIVTUU6KLTYO26SPVEBDFBKP3UMZM2DPEO5RINODUVCI5NVIFC6HVNWS7E?include-all=true` | `62554271` |
| Algorand address validation | Local `algosdk.encoding.is_valid_address` | N/A |

## Address Validation

| Check | Result |
| --- | --- |
| Valid Algorand address checksum | `true` |
| Account found by indexer | `true` |

## Observed Account Snapshot

| Field | Observed value |
| --- | --- |
| Account status | `Offline` |
| Signature type | `sig` |
| ALGO balance | `15,531,183` microAlgos |
| Total assets opted in | `17` |
| Total apps opted in | `2` |
| Total created apps | `34` |
| Total created assets | `1` |

## Observed PNET Balance

| Field | Observed value |
| --- | --- |
| ASA ID | `3169177585` |
| Raw PNET balance | `15583379085` |
| Display PNET balance | `15,583.379085` PNET |
| Asset deleted flag | `false` |
| Asset frozen flag | `false` |
| PNET opt-in round | `53334143` |

## Interpretation

This snapshot verifies that the user-provided operational wallet is a valid Algorand address and held `15,583.379085` PNET at capture round `62554271`.

This snapshot does not verify:

- who controls the wallet,
- whether it is single-sig or controlled through any external process,
- whether it is the official operational wallet,
- whether its holdings are strategic, treasury, operational, personal, or unrelated,
- whether created applications are official PNET tools,
- whether future movement is restricted.

## Required Human Confirmation

Before public materials describe the wallet as an official operational wallet, record:

| Required item | Status |
| --- | --- |
| Maintainer confirmation of exact address | Needs verification |
| Role description | Needs verification |
| Control model | Needs verification |
| Security policy | Needs verification |
| Movement/disclosure policy | Needs verification |
| Link to public app/deployment relationships, if any | Needs verification |

Current Gate Status: ADDRESS VALIDITY AND DATED PUBLIC BALANCE SNAPSHOT VERIFIED; PROJECT ROLE AND CONTROL MODEL REMAIN NEEDS VERIFICATION.
