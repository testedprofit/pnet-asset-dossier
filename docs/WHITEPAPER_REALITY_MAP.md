# PNET Whitepaper Reality Map

Status date: 2026-06-27

This file maps whitepaper claims to current artifacts and evidence.

| Whitepaper area | Claim or design target | Current artifact | Evidence status | Gap |
| --- | --- | --- | --- | --- |
| Asset identity | PNET is ASA `3169177585` | [asset identity proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) | Verified by public indexers | Recheck before external use |
| Fixed supply and decimals | `100,000,000` PNET, `6` decimals | [asset identity proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) | Verified by public indexers | None for baseline supply |
| Control fields | Manager/reserve/freeze/clawback are zero address at capture round | [asset identity proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) | Verified current value | Historical control review optional |
| Burn accounting | Burned supply can be calculated from on-chain proof | [supply methodology](../data/on-chain-proofs/supply-methodology.md) | Needs on-chain verification | Burn transaction set missing |
| Locked supply | Locked allocations require app/escrow proof | [burn/lock/vault worklist](../data/on-chain-proofs/burn-lock-vault-worklist.md) | Needs on-chain verification | Lock/vault proof missing |
| Operational wallet | User-provided wallet can be disclosed with proof | [operational wallet proof](../data/on-chain-proofs/operational-wallet-proof-2026-06-27.md) | Balance snapshot only | Role/control model missing |
| Contribution Credit System MVP | MVP implementation package has source/TEAL/ABI hashes and static checks | [pnet-contribution-protocol/MVP.md](pnet-contribution-protocol/MVP.md) | Ready for TestNet deployment | App ID, deployment tx, live test report, audit missing |
| Contribution protocol | App-local access/reputation credits | [implementation spec](implementation/community-contribution-protocol-spec.md) | Spec/prototype only | TestNet deployment record and audit missing |
| Market-intelligence receipts | Dated snapshots and hashes | [API spec](implementation/market-intelligence-api-spec.md) | Draft | Public API/dashboard deployment missing |
| Governance | Advisory signaling possible | Existing prototype docs; deployment pending | Prototype only | Policy, deployment, audit missing |
| Treasury transparency | Accounting ledger possible | Existing prototype docs; deployment pending | Prototype only | Legal/accounting review missing |

Current Gate Status: REALITY MAP STARTED; WHITEPAPER CLAIMS NOW HAVE STATUS LINKS, BUT PROTOCOL CLAIMS REMAIN SPECIFICATION OR PROTOTYPE ONLY.
