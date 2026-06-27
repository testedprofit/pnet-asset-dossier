# PNET Market-Intelligence Snapshot API Specification

Status date: 2026-06-27
Status: Draft v0.1. No production API is claimed.

## Purpose

The market-intelligence API exposes dated, source-linked, reproducible snapshots for asset facts, supply categories, public claims, wallet reviews, and dashboard views.

## Non-Purposes

The API is not:

- a trading API,
- a price prediction API,
- a live investment signal,
- a custody or signer service,
- a source of guaranteed current market data.

## Snapshot Object

```json
{
  "schema": "pnet-snapshot-v1",
  "asset_id": 3169177585,
  "unit": "PNET",
  "network": "mainnet",
  "capture_date": "YYYY-MM-DD",
  "capture_round": 0,
  "sources": [],
  "facts": {},
  "claims": [],
  "verification_status": "Snapshot only",
  "receipt_hash": ""
}
```

## Claim Object

```json
{
  "claim": "",
  "source": "",
  "capture_date": "",
  "observed_value": "",
  "status": "Needs verification",
  "method": "",
  "limitations": ""
}
```

## Recommended Endpoints

| Endpoint | Method | Purpose |
| --- | --- | --- |
| `/api/assets/{asset_id}/latest` | GET | latest public snapshot |
| `/api/assets/{asset_id}/history` | GET | list dated snapshots |
| `/api/assets/{asset_id}/proofs` | GET | proof index and status |
| `/api/receipts/{hash}` | GET | receipt lookup by hash |
| `/api/claims?status=needs-verification` | GET | unresolved claim list |
| `/api/reports/monthly` | GET | monthly transparency reports |

## Data Freshness

Every response must include:

- capture date,
- capture round when available,
- source list,
- stale-data notice,
- status label,
- limitations.

## Hashing

Canonical JSON should:

- sort object keys,
- use UTF-8,
- preserve numeric values exactly as strings where precision matters,
- hash with SHA-256,
- publish the resulting hex digest.

## Security

- No API keys in public examples.
- No transaction submission routes.
- No signer endpoints.
- No wallet recovery or custody endpoints.
- Rate limits recommended before public launch.
- Privacy review required before collecting analytics or user-submitted data.

Current Gate Status: API SPEC DRAFT READY FOR REVIEW; NO PRODUCTION API CLAIMED.
