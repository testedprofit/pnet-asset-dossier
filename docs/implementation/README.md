# PNET Implementation Specifications

Status date: 2026-06-27

This folder bridges the whitepaper and future code repositories. It defines behavior, state, APIs, tests, and security expectations before any production deployment.

## Specifications

| File | Purpose | Status |
| --- | --- | --- |
| [community-contribution-protocol-spec.md](community-contribution-protocol-spec.md) | Detailed contract-level specification for contribution/access credits | Ready for implementation review |
| [smart-contract-design-principles.md](smart-contract-design-principles.md) | Shared contract design rules and safety invariants | Ready for review |
| [market-intelligence-api-spec.md](market-intelligence-api-spec.md) | Snapshot and receipt API model | Draft |
| [algorand-atomic-transaction-groups.md](algorand-atomic-transaction-groups.md) | Algorand atomic-group patterns for PNET receipts, access checks, and future tool integrations | Draft |
| [algolens-legacy-progress.md](algolens-legacy-progress.md) | Legacy AlgoLens standalone HTML prototype scan and progress note | Archived prototype note |

## Rules

- TestNet first.
- No committed private keys, mnemonics, `.env` files, wallet screenshots, or signer configs.
- No custody, managed strategy, copy trading, trading automation, or user-deposit framing.
- No APY/APR/ROI, passive-income, or guaranteed-value logic.
- Atomic transaction groups may be used for all-or-nothing coordination, but not to introduce hidden custody, deposits, trading logic, or yield.
- Every future deployment needs source, ABI, app ID, deployment transaction, tests, audit status, and public claims review.

Current Gate Status: IMPLEMENTATION SPEC LAYER STARTED; PRODUCTION DEPLOYMENT NOT APPROVED.
