# PNET Smart Contract Design Principles

Status date: 2026-06-27
Status: Draft standard for future implementation work.

## Scope

These principles apply to future PNET contribution, receipt, governance, growth, treasury-accounting, and access-control contracts.

## Core Invariants

| Invariant | Rule |
| --- | --- |
| TestNet first | Every contract begins on TestNet or local simulation |
| No hidden custody | If a contract ever holds assets, that fact must be explicit, audited, and separately approved |
| No return promises | Contracts must not encode or advertise APY/APR/ROI or guaranteed value |
| No trading logic | No swap, route, bridge, arbitrage, copy-trading, or managed-strategy logic |
| Public source | Source, ABI, app ID, deployment tx, and hashes must be published |
| Minimal authority | Admin powers must be narrow, logged, and documented |
| Verifiable logs | Important actions should emit stable prefixes and receipt hashes |
| Upgrade disclosure | Update/delete permissions must be disclosed before public use |
| Explicit group shape | Any atomic transaction group must define exact group size, order, transaction types, senders, receivers, amounts, assets, and safety checks |

## Required Contract Metadata

| Field | Requirement |
| --- | --- |
| Contract name | Human-readable |
| Purpose | One sentence |
| Network | Local, TestNet, MainNet |
| Asset IDs | Explicit, no silent defaults |
| Admin address | Public after deployment |
| Upgrade policy | Immutable, admin-updatable, multisig, or other |
| Pause policy | Present/absent and who controls it |
| ABI | Published |
| TEAL hashes | Published |
| Audit status | Published |

## Review Checklist

- [ ] No inner transaction opcodes unless explicitly required and audited.
- [ ] No asset transfer/payment opcodes unless explicitly required and audited.
- [ ] Any atomic transaction group checks exact group size and transaction order.
- [ ] Grouped transactions reject unexpected rekey, close-out, receiver, amount, asset ID, or app ID values.
- [ ] No hard-coded MainNet deployment assumptions in TestNet scripts.
- [ ] No signer logic in public docs-only dossier.
- [ ] No private keys, mnemonics, API keys, `.env` files, or wallet screenshots.
- [ ] All admin methods logged.
- [ ] All limits documented.
- [ ] Local/global state schema documented.
- [ ] Failure modes documented.
- [ ] Monitoring plan documented.

Current Gate Status: DESIGN PRINCIPLES READY FOR REVIEW.
