# PNET Community Contribution Protocol Specification

Status date: 2026-06-27
Version: Draft v0.2
Network target: TestNet first
Production status: Not deployed, not audited, not MainNet approved.

## 1. Purpose

The PNET Community Contribution Protocol records app-local contribution, access, and reputation credits for approved ecosystem participation.

Approved framing:

> Users may receive or use app-local contribution/access credits for approved, non-custodial ecosystem participation.

Non-purpose:

The protocol must not custody PNET, require deposits, manage strategies, calculate yield, pay returns, execute trades, route swaps, bridge assets, or create claims on treasury assets.

## 2. Actors

| Actor | Role |
| --- | --- |
| User | Opts in, views credits, gifts credits, uses credits for documented access/reputation purposes |
| Admin | Sets limits, pause status, partner/reviewer status, and deployment parameters |
| Partner/reviewer | Approved account that can assign credits or review contributions within documented limits |
| Public reviewer | Reads app state, logs, ABI, source, and deployment records |

## 3. State Model

### Global State

| Key | Type | Purpose |
| --- | --- | --- |
| `admin` | address | current administrator |
| `asset_id` | uint | referenced PNET or TestNet asset ID |
| `paused` | uint | `0` active, `1` paused |
| `max_grant` | uint | maximum credits per grant |
| `max_gift` | uint | maximum credits per gift |
| `total_credits` | uint | total credits assigned |
| `total_gifts` | uint | total credits gifted |
| `total_redeemed` | uint | total credits used |
| `action_count` | uint | total grant/action count |
| `total_external_reviews` | uint | total reviewed external-activity submissions |
| `total_mining_credits` | uint | credits assigned for compute-participation evidence |
| `total_bandwidth_credits` | uint | credits assigned for bandwidth-sharing evidence |

### Local State

| Key | Type | Purpose |
| --- | --- | --- |
| `credits` | uint | current app-local credits |
| `granted` | uint | lifetime credits assigned |
| `given` | uint | credits gifted out |
| `received` | uint | credits received through gifts |
| `redeemed` | uint | credits used |
| `partner` | uint | partner/reviewer flag |
| `optin_round` | uint | opt-in round |
| `last_action_code` | uint | last documented action code |
| `last_action_round` | uint | last action round |
| `last_receipt_hash` | bytes | 32-byte receipt hash |
| `mining_credits` | uint | lifetime credits assigned for compute-participation evidence |
| `bandwidth_credits` | uint | lifetime credits assigned for bandwidth-sharing evidence |
| `external_reviews` | uint | lifetime reviewed external-activity records |
| `last_external_type` | uint | last external activity type |
| `last_external_hash` | bytes | 32-byte hash for last reviewed external activity |

## 4. Methods

| Method | Caller | Behavior | Required checks |
| --- | --- | --- | --- |
| `opt_in` | user | initializes local state | app not required to transfer assets |
| `set_admin(new_admin)` | admin | updates admin | current admin only; logged |
| `set_paused(paused)` | admin | pauses/unpauses state changes | current admin only; `paused` in `{0,1}` |
| `set_limits(max_grant,max_gift)` | admin | updates grant/gift limits | positive values only |
| `set_partner(account,enabled)` | admin | toggles partner/reviewer flag | account opted in; `enabled` in `{0,1}` |
| `grant(recipient,amount,action_code,receipt_hash)` | admin/partner | assigns credits | recipient opted in, amount positive and within limit, 32-byte receipt hash |
| `record_verified_activity(recipient,activity_type,amount,period_code,evidence_hash,review_hash)` | admin/partner | records a reviewed external-activity contribution and assigns app-local credits | recipient opted in, reviewer approved, activity type allowed, amount within limit, 32-byte hashes |
| `record_kryptex_activity(recipient,amount,period_code,evidence_hash,review_hash)` | admin/partner | convenience method for compute-participation evidence | maps to activity type `1`; no raw screenshot or private wallet data on-chain |
| `record_honeygain_activity(recipient,amount,period_code,evidence_hash,review_hash)` | admin/partner | convenience method for bandwidth-sharing evidence | maps to activity type `2`; no raw screenshot or private wallet data on-chain |
| `reject_activity(recipient,activity_type,reason_code,evidence_hash,review_hash)` | admin/partner | logs a reviewed but rejected external-activity submission without issuing credits | recipient opted in, activity type allowed, 32-byte hashes |
| `give(recipient,amount)` | user | transfers app-local credits | both opted in, no self gift, sender has credits |
| `redeem(amount,purpose_code,receipt_hash)` | user | uses credits for documented purpose | sufficient credits, 32-byte receipt hash |
| `get_credits(account)` | read | returns local credit balance | account opted in |
| `get_granted(account)` | read | returns lifetime granted credits | account opted in |
| `get_given(account)` | read | returns lifetime gifted credits | account opted in |
| `get_received(account)` | read | returns lifetime received credits | account opted in |
| `get_mining_credits(account)` | read | returns lifetime compute-participation credits | account opted in |
| `get_bandwidth_credits(account)` | read | returns lifetime bandwidth-sharing credits | account opted in |
| `get_external_reviews(account)` | read | returns lifetime reviewed external-activity count | account opted in |
| `is_partner(account)` | read | returns partner flag | account opted in |
| `get_last_receipt_hash(account)` | read | returns last receipt hash | account opted in |

### External Activity Types

| Type | Label | Action-code range | Initial service reference | Status |
| --- | --- | --- | --- | --- |
| `1` | compute-participation evidence | `700-719` | Kryptex-style mining activity evidence | Needs verification |
| `2` | bandwidth-sharing evidence | `720-739` | Honeygain / JumpTask-style bandwidth-sharing activity evidence | Needs verification |

Service references identify the kind of user-submitted evidence under review. They are not endorsements, partnerships, revenue claims, or guarantees.

## 5. Logs and Receipts

Recommended log prefix:

```text
PNET_CC:
```

Every state-changing action should emit a log containing:

- action name,
- relevant account,
- amount or status,
- action/purpose code,
- activity type for external-activity reviews,
- period code for external-activity reviews,
- receipt hash when available.

Receipt hash requirements:

- 32 bytes,
- derived from canonical JSON,
- full receipt stored off-chain in the public dossier, dashboard, or approved public storage,
- no private data directly on-chain.

External-activity evidence hash requirements:

- 32 bytes,
- derived from a redacted evidence package,
- may include a user-consented public account reference or one-way hash,
- must not include raw screenshots, payout values, personal referral identifiers, emails, usernames, device IDs, IP addresses, or private wallet screenshots in public records.

### External Activity Method Semantics

`record_verified_activity` is the canonical method. The dedicated methods are optional ABI conveniences that call the same internal validation path.

| Step | Requirement |
| --- | --- |
| Validate reviewer | Caller must be admin or approved partner/reviewer |
| Validate recipient | Recipient must be opted into the application |
| Validate activity type | Type must be `1` or `2` until additional types are approved |
| Validate credit amount | Amount must be positive and within `max_grant` |
| Validate hashes | `evidence_hash` and `review_hash` must each be 32 bytes |
| Update credits | Add amount to `credits`, `granted`, and category-specific lifetime counters |
| Update totals | Increment `total_external_reviews`, `total_credits`, `action_count`, and category-specific totals |
| Emit log | Emit action, recipient, activity type, amount, period code, evidence hash, and review hash |

`reject_activity` should update review counters and emit a log, but must not increase credits.

## 6. Action Code Registry

| Range | Meaning |
| --- | --- |
| `100-199` | documentation contribution |
| `200-299` | verification contribution |
| `300-399` | dashboard testing |
| `400-499` | community support |
| `500-599` | security or bug-report activity |
| `600-699` | partner-approved contribution |
| `700-719` | compute-participation evidence; service details need review |
| `720-739` | bandwidth-sharing participation evidence; service details need review |
| `740-759` | referral-campaign participation evidence; public campaign policy required |
| `760-779` | educational proof-of-work evidence |
| `900-999` | administrative correction |

Specific codes must be published before use.

For real-world contribution evidence, follow [REAL_WORLD_CONTRIBUTION_EVIDENCE.md](../contribution/REAL_WORLD_CONTRIBUTION_EVIDENCE.md). Public app logs should record action codes and receipt hashes only. They should not expose private screenshots, payout values, personal referral identifiers, device data, or private wallet details.

## 7. Security Requirements

| Requirement | Rationale |
| --- | --- |
| No inner transactions | Keeps contract non-custodial and avoids hidden value movement |
| No asset transfers | Credits are app-local records, not PNET transfers |
| Pause switch | Allows response to bad review policy or bug |
| Grant/gift limits | Limits abuse and accidental credit inflation |
| Partner opt-in requirement | Ensures reviewer status is visible in local state |
| 32-byte receipt hashes | Standardizes public verification |
| Overflow checks | Prevents state wraparound |
| Admin policy documented | Makes trust assumptions explicit |
| No raw evidence on-chain | Prevents irreversible publication of personal data |
| Rejection logging | Makes reviewer decisions auditable without issuing credits |
| Category-specific counters | Allows public monitoring without exposing user activity details |

## 8. Integration Points

| System | Integration |
| --- | --- |
| Dossier | stores source, ABI, deployment record, action-code registry, public claims policy |
| Market-intelligence dashboard | reads app state and receipt records |
| Community growth system | can reference contribution status and receipt hashes |
| Governance prototype | may use credits for advisory participation context only after review |
| AlgoFlow tools | may check access/reputation status; no custody or deposit framing |
| External evidence review UI | submits redacted activity packages for manual review; only hashes and decisions reach chain |

### Atomic Transaction Group Integration

Algorand atomic transaction groups may be used to bind related actions together when the protocol needs all-or-nothing execution.

Allowed MVP-adjacent examples:

- user app opt-in plus reviewer decision app call,
- user acknowledgement plus reviewer decision app call,
- app-local credit consumption plus a tool-access receipt,
- fee sponsorship for a user app call.

Rejected for the MVP:

- user deposit plus credit issuance,
- PNET transfer plus credit issuance,
- DEX trade plus contribution action,
- automatic financial reward after a contribution record.

Any grouped transaction design must follow [algorand-atomic-transaction-groups.md](algorand-atomic-transaction-groups.md), publish exact group shape, and complete separate TestNet/security/public-claims review before use.

## 9. Test Plan

Required tests:

- compile approval/clear programs,
- ABI method presence,
- opt-in initialization,
- admin-only methods reject unauthorized callers,
- partner grant flow,
- non-partner grant rejection,
- verified Kryptex-style compute activity records credits and category counters,
- verified Honeygain-style bandwidth activity records credits and category counters,
- external-activity methods reject unsupported activity types,
- external-activity methods reject non-32-byte evidence/review hashes,
- rejected external activity does not issue credits,
- external-activity methods do not expose raw evidence fields,
- gift positive flow,
- self-gift rejection,
- insufficient-credit gift rejection,
- redeem positive flow,
- invalid receipt hash rejection,
- paused state blocks state-changing methods,
- no inner transaction opcodes,
- no asset transfer/payment opcodes,
- no risky public-claims wording in docs/frontend.

## 10. Publication Gate

Before public TestNet announcement:

- source published,
- ABI published,
- approval/clear hashes published,
- app ID published,
- deployment tx ID published,
- admin address and policy published,
- test report published,
- audit status published,
- known limitations published,
- public claims review complete.

Before MainNet:

- professional audit or equivalent reviewed scope,
- legal/public-claims review,
- admin/update/delete policy finalized,
- emergency response process,
- monitoring plan,
- MainNet deployment checklist,
- explicit go/no-go decision.

Current Gate Status: SPEC READY FOR IMPLEMENTATION REVIEW; TESTNET DEPLOYMENT ONLY AFTER PUBLICATION GATE; MAINNET BLOCKED.
