# PNET Contribution Credit System MVP

Status date: 2026-06-27
Status: MVP implementation package prepared; TestNet deployment pending.
Network target: Algorand TestNet first.
MainNet status: Blocked.

## Safe Framing

Use only this framing:

> Users may receive app-local PNET access and reputation credits after verified non-custodial participation. No custody, no guaranteed value, no investment claims.

Contribution credits are app-local access/reputation records. They are not PNET tokens, not deposits, not yield, not passive income, not guaranteed value, and not investment returns.

## What Was Built

The MVP implementation package contains:

| Area | Status | Notes |
| --- | --- | --- |
| PyTeal contract | Built | App-local contribution/access/reputation credits |
| Kryptex-style activity review | Built | Records accepted compute-participation evidence using hashes only |
| Honeygain / JumpTask-style activity review | Built | Records accepted bandwidth-sharing evidence using hashes only |
| Rejection logging | Built | Records reviewed rejected activity without assigning credits |
| Credit gifting | Built | Opted-in users can gift app-local credits to opted-in users |
| Credit consumption | Built | Users can consume credits for access/reputation purposes |
| Pause control | Built | Admin can pause state-changing participant/reviewer actions |
| Partner reviewer role | Built | Admin can enable/disable partner reviewers |
| Update/delete policy | Built | App update and delete are disabled in MVP |
| Frontend demo | Built | Next.js/Pera TestNet review flow |
| Tests | Built | Unit tests, static E2E checks, frontend typecheck/build |
| TestNet deployment | Pending | Requires funded TestNet deployer account controlled by maintainer |
| Professional audit | Pending | No professional audit report included |

## Contract Safety Summary

| Check | Result |
| --- | --- |
| Custodies user PNET | No |
| Transfers PNET | No |
| Uses inner transactions | No |
| Uses asset transfer/payment opcodes | No |
| Requires user deposits | No |
| Calculates yield/APY/APR/ROI | No |
| App update enabled | No |
| App delete enabled | No |
| Admin can claw back credits | No clawback method exists |
| Admin can assign credits | Yes, within published limits |
| Approved partner can assign credits | Yes, within published limits |
| User can gift credits | Yes, app-local credits only |

## MVP Methods

See [METHODS.md](METHODS.md).

## Supporting Policy Documents

| File | Purpose |
| --- | --- |
| [LEGAL_DISCLAIMER.md](LEGAL_DISCLAIMER.md) | Draft legal disclaimer and user acknowledgement copy |
| [PUBLIC_CLAIMS_POLICY.md](PUBLIC_CLAIMS_POLICY.md) | Public wording rules and website tokenomics copy |
| [VERIFICATION_PROCESS.md](VERIFICATION_PROCESS.md) | MVP verification and privacy process |
| [RISK_REGISTER.md](RISK_REGISTER.md) | Risk register and MainNet gate |
| [THREAT_MODEL.md](THREAT_MODEL.md) | Threat model and residual-risk summary |
| [AUDIT_READINESS_CHECKLIST.md](AUDIT_READINESS_CHECKLIST.md) | Audit readiness checklist |
| [METHODS.md](METHODS.md) | ABI method summary and proof-handling model |

## Proof Model

External evidence is not placed on-chain directly.

| Evidence | Public handling |
| --- | --- |
| Redacted dashboard screenshot or proof file | Hash only |
| Wallet/account reference | Hash only |
| Reviewer decision package | Hash only |
| Raw screenshot, payout value, private account data | Not published in dossier |

## Current Artifact Evidence

Generated local artifact hashes from the implementation package:

| Artifact | SHA-256 |
| --- | --- |
| Contract source | `236eae414acaae6e68dc51987318a483f34991230c5745bdda916b297768dae8` |
| Approval TEAL | `bfb65b671d0651813adeaa83254da98f230f348d48a2028264fcb12b2605d290` |
| Clear TEAL | `f1ed5f2a5843e27469f19d72f430e69fe67aee6746578bbaa7c9097c637a6ffc` |
| ABI JSON | `9133c917c5e1ce7527d138e8f6ee8d3cb7b9868f65cb3db399939e742d9eb586` |

Static checks passed:

- no custody/transfer opcodes,
- no yield/staking language in contract source/ABI/TEAL,
- `PNET_CC:` logs present.

## TestNet Deployment Gate

Before public TestNet claim:

- deploy to Algorand TestNet,
- record app ID,
- record deployment transaction ID,
- record confirmed round,
- record creator/admin address,
- record state schema,
- record source and artifact hashes,
- publish static and live TestNet test report,
- update [deployment-testnet.md](../../data/on-chain-proofs/contribution-protocol/deployment-testnet.md),
- update [DEPLOYMENT_REGISTRY.md](../DEPLOYMENT_REGISTRY.md),
- update [LIVE_TESTNET_EVIDENCE.md](../LIVE_TESTNET_EVIDENCE.md).

Current Gate Status: MVP READY FOR TESTNET DEPLOYMENT; NO TESTNET APP ID OR DEPLOYMENT TRANSACTION RECORDED YET.
