# PNET Contribution Credit System Methods

Status date: 2026-06-27
Status: MVP ABI summary; TestNet deployment pending.

The PNET Contribution Credit System is an app-local credit system. It does not transfer or custody PNET.

## Admin Methods

| Method | Purpose | Notes |
| --- | --- | --- |
| `set_admin(address)` | Move admin role | Requires current admin |
| `set_paused(uint64)` | Pause or unpause state-changing methods | `0` or `1` only |
| `set_limits(uint64,uint64)` | Set max assignment and gift amounts | Requires current admin |
| `set_partner(account,uint64)` | Enable or disable a partner reviewer role | Partner account must be opted in |

## Contribution Methods

| Method | Purpose | Notes |
| --- | --- | --- |
| `grant(account,uint64,uint64,byte[])` | Admin/partner assigns credits to an opted-in account | Stores last action code and a 32-byte receipt hash |
| `record_verified_activity(account,uint64,uint64,uint64,byte[],byte[],byte[])` | Admin/partner records accepted external activity evidence | Activity type `1` = Kryptex-style compute participation; `2` = Honeygain / JumpTask-style bandwidth sharing |
| `record_kryptex_activity(account,uint64,uint64,byte[],byte[],byte[])` | Admin/partner records accepted Kryptex-style evidence | Stores evidence hash, hashed account reference, review hash, period code, and category counters |
| `record_honeygain_activity(account,uint64,uint64,byte[],byte[],byte[])` | Admin/partner records accepted Honeygain / JumpTask-style evidence | Stores evidence hash, hashed account reference, review hash, period code, and category counters |
| `reject_activity(account,uint64,uint64,byte[],byte[],byte[])` | Admin/partner records a rejected external activity review | Does not assign credits; increments review counters and logs hashes |
| `give(account,uint64)` | User gifts credits to another opted-in account | No token transfer |
| `redeem(uint64,uint64,byte[])` | User consumes credits for an access/reputation purpose | Stores purpose code and a 32-byte receipt hash; no payout |

## Read Methods

| Method | Purpose |
| --- | --- |
| `get_credits(account)` | Current app-local credit balance |
| `get_granted(account)` | Credits assigned by admin/partner |
| `get_given(account)` | Credits gifted by account |
| `get_received(account)` | Credits received from users |
| `get_mining_credits(account)` | Accepted Kryptex-style compute-participation credits |
| `get_bandwidth_credits(account)` | Accepted Honeygain / JumpTask-style bandwidth-sharing credits |
| `get_external_reviews(account)` | Count of reviewed external activity submissions |
| `is_partner(account)` | Partner flag |
| `get_last_receipt_hash(account)` | Last assignment or consumption receipt hash stored for the account |
| `get_last_external_hash(account)` | Last reviewed external activity evidence hash |

## On-Chain Proof Handling

| Field | On-chain treatment |
| --- | --- |
| Redacted dashboard screenshot or proof file | Hash only as `evidence_hash` |
| Wallet/account reference | Hash only as `account_hash` |
| Reviewer decision package | Hash only as `review_hash` |
| Raw screenshot, payout value, private account data | Not stored on-chain and not committed to this dossier |

## Logs

Every state-changing method emits logs prefixed with:

```text
PNET_CC:
```

Indexers can use logs, transaction arguments, sender addresses, account references, and local/global state deltas to reconstruct contribution activity.

## Bare Calls

| Call | Purpose |
| --- | --- |
| Create app | Sets admin, explicit TestNet asset ID, max assignment, and max gift |
| Opt in | Initializes local account state |
| Close out | Allowed; app-local credits do not transfer after close-out |
| Update app | Disabled in MVP |
| Delete app | Disabled in MVP |

Current Gate Status: METHODS DOCUMENTED; ABI HASH RECORDED IN MVP; TESTNET DEPLOYMENT PENDING.
