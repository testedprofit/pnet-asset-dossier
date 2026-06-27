# PNET Community Contribution Protocol Threat Model

Version: 1.0
Date: 2026-06-27
Scope: MVP / TestNet candidate. Not MainNet. Not audited.

This document identifies potential threats to the PNET Community Contribution Protocol and describes current mitigations, residual risks, and review gates. It is written for public review and follows the dossier's transparency-first and safe-framing rules.

## Safe Framing Boundary

The protocol records reviewed participation evidence and assigns app-local access/reputation credits.

It must not be described as:

- staking,
- yield,
- passive income,
- profit share,
- investment return,
- token-value support,
- user deposit program,
- managed strategy.

Credits are not PNET tokens. They are app-local access/reputation records with no guaranteed value.

## Assets

| Asset | Description | Protection goal |
| --- | --- | --- |
| App-local access/reputation credits | Local-state credit balances used by the contribution protocol | Prevent unauthorized issuance, theft, or misleading treatment as financial value |
| User-submitted evidence | Redacted screenshots, activity records, account references, or reviewer packages | Keep raw evidence off-chain and out of the public dossier unless explicitly public-safe |
| Evidence hashes | Hashes of submitted evidence, account references, and review records | Preserve auditability without publishing private evidence |
| Review decisions | On-chain records of accepted or rejected evidence | Make reviewer decisions traceable and reproducible |
| Protocol state | Opt-in status, counters, category totals, pause state, partner reviewer status | Prevent unauthorized state changes and inconsistent accounting |
| Public documentation | GitHub dossier, deployment proofs, risk register, claims policy, audit records | Keep public claims accurate, dated, and source-linked |

## Roles And Trust Boundaries

| Role | Capabilities | Trust boundary |
| --- | --- | --- |
| User | Opt in, submit proof off-chain, receive reviewed credits, gift app-local credits | User-provided proof can be incomplete or false until reviewed |
| Admin | Configure protocol controls, approve partner reviewers, pause MVP actions | Admin key control is a critical operational risk until multisig or governance is implemented |
| Partner reviewer | Review approved evidence categories and issue/reject credits within policy | Reviewer discretion can create consistency and abuse risks |
| Public verifier | Recompute hashes where evidence is available, inspect on-chain actions, review dossier proofs | Verifier can only validate public or privately disclosed evidence |
| Maintainer | Updates dossier, deployment records, and public claims status | Documentation can drift unless review cadence is followed |

## Threat Categories And Analysis

| Threat ID | Threat | Likelihood | Impact | Risk Level | Mitigation / Status |
| --- | --- | --- | --- | --- | --- |
| T01 | Unauthorized credit issuance | Low | High | High | Admin/partner access control is required for issuance. App update/delete are disabled for the MVP. Partner reviewer policy must be public before broader testing. |
| T02 | Manipulation or inconsistency in manual review | Medium | Medium | Medium | Accepted and rejected review decisions are recorded on-chain. Verification criteria and reason codes are documented. Future multisig/community review remains planned, not active. |
| T03 | Privacy breach of user activity data | Low | Medium | Low | Raw screenshots, private dashboard data, payout values, and private account details must stay off-chain. Public records use hashes and non-sensitive metadata only. |
| T04 | Smart-contract logic bug | Medium | High | High | Unit tests, static E2E checks, frontend build, dependency audit, and artifact hashes exist for the MVP package. Live TestNet E2E and professional audit remain pending. |
| T05 | Re-entrancy or external-call state manipulation | Low | High | Medium | MVP static checks show no inner transactions, external app calls, payment calls, asset-transfer opcodes, or custody paths. Auditors should confirm final TEAL before MainNet. |
| T06 | Sybil activity or fake proof farming | Medium | Medium | Medium | Credits require manual reviewer approval in the MVP. Rate limits, reviewer caps, duplicate-hash checks, and community review are future hardening items. |
| T07 | Admin or operational wallet compromise | Low | High | Medium | Admin and operational wallet activity should be publicly documented. Multisig or time-locked controls are recommended before MainNet or high-volume use. |
| T08 | Mis-framing or regulatory risk | Medium | High | High | The public claims policy prohibits yield, staking, passive-income, profit-share, and investment-return framing. Legal/public-claims review remains required before public launch. |
| T09 | Low adoption or centralization of credits | Medium | Low | Low | Credits support multiple external participation categories, but category expansion should remain neutral and evidence-based. Publish participation metrics without financial-performance claims. |
| T10 | Dependency on external services or changing evidence formats | Low | Low | Low | The protocol records reviewed evidence hashes only. It does not depend on Kryptex, Honeygain, JumpTask, or similar services for core contract execution. |
| T11 | Dossier evidence drift | Medium | Medium | Medium | Deployment records, artifact hashes, and review summaries should be updated after every release, deployment, and material policy change. |
| T12 | Misinterpretation of credits as transferable financial assets | Medium | High | High | All user-facing copy must state credits are access/reputation records only. Interfaces should avoid balance language that resembles token, yield, or investment dashboards. |

## Attack Vectors Considered

| Layer | Vectors | Current response |
| --- | --- | --- |
| User level | Fake evidence, duplicate submissions, multiple accounts, pressure on reviewers | Manual review, evidence hashes, reason codes, duplicate-hash checks recommended before MainNet |
| Contract level | Unauthorized method calls, overflow/underflow, inconsistent local state, update/delete abuse | Access checks, safe-add checks, local balance checks, disabled update/delete, static opcode checks |
| Frontend level | Misleading copy, private screenshot leakage, wrong network, unsafe wallet prompts | Safe-framing copy, TestNet-first design, local hashing requirement, no private evidence in dossier |
| Operational level | Admin key compromise, reviewer abuse, stale docs, unrecorded deployments | Public admin/partner policy, deployment proof records, periodic dossier review, multisig recommended |
| Ecosystem level | Credits treated as investment products, exchange/listing implication, third-party service endorsement | Public claims policy, disclaimers, no listing/support promises, neutral external-service references |

## Mitigation Strategy Summary

| Strategy | MVP status |
| --- | --- |
| Immutable app policy | Implemented for MVP; update/delete disabled |
| Non-custodial design | Implemented for MVP; no PNET transfers or deposits |
| Hashed proof model | Implemented in design; raw proofs remain off-chain |
| On-chain review logging | Implemented in design; live TestNet evidence pending |
| Admin/partner access control | Implemented in MVP; policy publication pending |
| Pause control | Implemented in MVP for state-changing participant/reviewer actions |
| Public claims controls | Drafted; legal/public-claims review pending |
| Professional audit | Pending and required before MainNet |

## Incident Response Notes

For the MVP, incident response should prioritize transparency and containment:

1. Pause state-changing participant/reviewer actions if the deployed contract supports pause control.
2. Stop manual approvals and partner review activity while the issue is reviewed.
3. Publish a dated incident note in the dossier with app ID, affected methods, known transactions, and current status.
4. Preserve transaction links and artifact hashes for review.
5. Record remediation decisions and whether a new TestNet deployment is required.

No MainNet deployment should proceed while a High or Critical issue is open without a published mitigation and maintainer go/no-go record.

## Residual Risks

- Manual review remains subjective until reviewer criteria, duplicate handling, appeal process, and escalation rules are tested.
- Admin and partner reviewer keys remain sensitive until multisig or a stronger governance model exists.
- External participation evidence formats may change.
- Credits could be misunderstood as financial value if public copy is not consistently reviewed.
- Live TestNet behavior is not yet proven in the dossier.

## Review Cadence

This threat model should be reviewed:

- before TestNet deployment,
- after TestNet deployment evidence is recorded,
- before any MainNet deployment decision,
- after any method, role, activity category, frontend flow, or public-claims change,
- after any reported security or privacy issue.

Material changes should be recorded in `CHANGELOG.md`.

## MainNet Gate

MainNet remains blocked until:

- live TestNet deployment evidence is recorded,
- live TestNet E2E tests pass,
- admin and partner reviewer policy is published,
- emergency response procedure is finalized,
- legal/public-claims review is complete,
- independent security review or professional audit is complete,
- maintainer go/no-go decision is recorded.

Current Gate Status: THREAT MODEL DRAFTED; LIVE TESTNET EVIDENCE, ADMIN/PARTNER POLICY, EMERGENCY RESPONSE, LEGAL REVIEW, AND SECURITY AUDIT REMAIN BLOCKING FOR MAINNET.
