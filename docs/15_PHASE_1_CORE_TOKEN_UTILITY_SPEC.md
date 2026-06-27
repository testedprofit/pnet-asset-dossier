# Phase 1 Core Token Utility Specification

Status date: 2026-06-27

Scope: This is a documentation-only implementation specification. It does not contain contract code, deployment scripts, wallet logic, signer logic, frontend code, CLI code, private keys, recovery material, API keys, or `.env` files.

## Objective

Define a safe Phase 1 path for PNET utility on Algorand TestNet before any production deployment. Phase 1 should test whether PNET can support access control, voluntary token locking, tool usage payments, and transparent revenue attribution without using inflation, return promises, user-deposit marketing, or opaque treasury behavior.

## Non-Goals

| Non-goal | Reason |
| --- | --- |
| MainNet launch from this dossier | This repo is documentation and media only |
| Promised reward rates | Would conflict with the public claims policy |
| Income framing | Not allowed by the dossier claims policy |
| User custody or wallet management by the project | Any future contract escrow must be explicit, audited, and TestNet-proven first |
| Transaction submission examples in this repo | Implementation belongs in a separate TestNet codebase |
| Burn routing to an unverified address | Burn mechanics require on-chain and disclosure review first |

## Required Implementation Location

Future Phase 1 code should be created outside this repository.

| Artifact | Required location |
| --- | --- |
| PyTeal / TEAL source | Separate implementation repository or private TestNet workspace |
| ABI contract JSON | Separate implementation repository |
| Deployment scripts | Separate implementation repository |
| Frontend or CLI interaction stubs | Separate implementation repository |
| Wallet setup notes containing sensitive material | Never committed |
| Public deployment records | May be summarized here after review, without secrets |

## Sub-Section 2.1: Staking / Proof-of-Contribution Contract

### Purpose

Create a TestNet-only prototype for voluntary PNET locking and contribution-tier access. The first version should prove state accounting and access flags before any public claims about rewards, revenue, or production availability.

### Design Requirements

| Area | Requirement |
| --- | --- |
| Asset | Use PNET ASA ID `3169177585` on MainNet documentation; use a TestNet test asset for development unless a verified TestNet equivalent is created |
| Staking model | Users voluntarily lock PNET-like TestNet tokens into an audited application escrow or equivalent design |
| Unstake | Users can request release according to clearly documented timing rules |
| Reward claim | Rewards, if tested, must come from a pre-funded treasury allocation and must not rely on inflation or promised rates |
| Tiers | Tiers should unlock access flags, API quotas, dashboard status, or priority queues rather than investment-style returns |
| Treasury | Treasury address must be configurable during TestNet deployment and documented after deployment |
| Admin powers | Any admin role must be narrow, documented, time-limited where practical, and easy to audit |
| Emergency behavior | Pause or migration behavior must be documented before deployment and tested before public use |
| Indexability | Events/state should be readable by Algorand indexers without private infrastructure |

### Suggested Tier Model

| Tier | Example basis | Utility surface | Public-claims boundary |
| --- | --- | --- | --- |
| Observer | No lock required | Public dashboard, public snapshots | No token requirement |
| Contributor | Small voluntary lock or verified contribution | Early data review queue, issue triage, source-review role | No return claim |
| Analyst | Larger voluntary lock or verified work history | Higher API quota, premium analytics, launchpad review priority | Access only, not income |
| Partner | Manual approval plus on-chain proof | Integration support, registry review workflow | Requires human review |

### Security Requirements

| Risk | Required mitigation |
| --- | --- |
| Escrow custody risk | Make custody explicit, TestNet-first, audited, and reversible only through defined methods |
| Reward accounting errors | Use deterministic accounting, unit tests, and edge-case tests for zero stake, partial unstake, and treasury depletion |
| Admin abuse | Minimize privileged methods and publish admin address controls |
| Upgrade/migration risk | Treat migration as a new deployment unless an upgrade pattern is formally reviewed |
| Reward exhaustion | Display treasury-funded reward availability as finite and non-guaranteed |
| Sybil tier gaming | Treat tiers as access-control signals, not proof of identity or trust |
| Legal/listing risk | Avoid rate, income, revenue-share, or investment framing |

### Required Deliverables In The Implementation Repo

| Deliverable | Status gate |
| --- | --- |
| Contract source | Code review complete |
| ABI | Generated from reviewed source |
| Unit tests | Passing locally and in CI |
| TestNet deployment script | Uses no committed secrets |
| TestNet deployment record | App ID, creator, treasury, ASA, and source commit recorded |
| Interaction stub | Clearly marked TestNet-only |
| Security notes | Includes known limitations and audit status |

## Sub-Section 2.2: PNET Payments In AlgoFlow Tools

### Purpose

Test optional PNET payments for tool usage in a way that creates measurable utility without requiring users to transfer custody to an opaque service or implying guaranteed benefits.

### Candidate Integrations

| Tool | Candidate payment use | Status |
| --- | --- | --- |
| Token Launchpad | Optional fee payment for project setup or review queue | Needs implementation repo |
| ProfitLock | Optional creation fee or advanced configuration fee | Needs implementation repo |
| MultiSend | Optional advanced-batch fee | Needs implementation repo |
| Wallet Inspector | Optional premium analytics access | Needs implementation repo |
| PNET Genesis | Future research only until bonding-curve mechanics are independently reviewed | Needs verification |

### Payment Routing Policy

| Route | Requirements |
| --- | --- |
| Treasury route | Preferred first route; address, capture date, and policy must be documented |
| Burn route | Do not use until burn address policy and lost-creator burn-path claims are independently verified |
| Split route | Only after treasury policy, accounting method, and legal review exist |
| Partner route | Requires direct partner evidence and public disclosure |

### Implementation Requirements

| Requirement | Rationale |
| --- | --- |
| Atomic payment validation | Tool action should only complete when the required PNET payment is present and correct |
| Configurable treasury in TestNet | Avoid hard-coded operational assumptions before review |
| Clear fee table | Users should see fee amount, route, and purpose before use |
| No silent burns | Every burn or treasury transfer must be visible and auditable |
| No MainNet default | TestNet must be the default implementation phase |
| No purchase guidance in this dossier | The dossier should not become an onboarding or trading guide |

## Sub-Section 2.3: Basic Revenue Attribution View

### Purpose

Provide a public, dated view of protocol-supporting inflows and tool fees. The first version can be indexer-based and read-only. It should explain where funds came from, where they went, and what remains unverified.

### Data Categories

| Category | Inclusion rule |
| --- | --- |
| Tool fees | Include only confirmed TestNet or MainNet transactions with source links |
| Referral revenue | Include only aggregate public accounting approved for disclosure; do not expose private account data |
| Treasury inflows | Include address, amount, asset, source, and capture date |
| Treasury outflows | Include purpose, amount, asset, destination label, and source transaction |
| Rewards funded | Include only actual funded amounts, not projections |
| Manual adjustments | Require dated explanation and reviewer initials or handle |

### Display Requirements

| Requirement | Notes |
| --- | --- |
| Dated snapshots | Every metric must show capture date and source |
| Stale-data warning | Market data and treasury views can become stale |
| No return projections | Do not show rate, return, or holder payout estimates |
| Audit trail | Preserve old snapshots instead of overwriting them silently |
| Read-only examples | Any examples in this dossier must avoid signer or transaction-submission logic |

## Burn Mechanism Documentation Gate

The roadmap includes a user-provided claim that the original creator account is unavailable and that tokens sent there through opt-out or transfer paths may be permanently irrecoverable. This must not be described as a verified burn method until the following are complete:

| Gate | Required evidence |
| --- | --- |
| Account review | Public indexer evidence for creator account state and asset balance changes |
| Control review | Human confirmation that account access is unavailable, without publishing private recovery details |
| Explorer reconciliation | Explanation of why direct burn-address figures may differ from inaccessible-account accounting |
| Disclosure review | Maintainer approval of exact public wording |
| Safety warning | Clear warning that users should not send assets to any address unless they understand the result |

## Phase 1 Codex Prompt Snippets

Use these prompts only inside the future implementation repo or private TestNet workspace.

### Staking / Proof-of-Contribution

```text
Create a secure Algorand TestNet staking/proof-of-contribution contract for a PNET test asset. Include voluntary lock, unlock, and claim methods, plus tier access flags. Rewards must be treasury-funded, finite, and non-promissory. Do not use inflation or promised reward rates. Include ABI generation, unit tests, security notes, and a TestNet deployment script that uses local-only configuration and never commits credentials or signer material.
```

### PNET Payments

```text
Create TestNet modules for optional PNET-like asset payments in Token Launchpad, ProfitLock, and MultiSend flows. Validate payment transfers atomically, route payments to a configurable treasury, and make burn routing disabled by default until burn-policy review is complete. Include tests and an integration guide.
```

### Revenue Attribution

```text
Create a read-only revenue attribution dashboard prototype using Algorand indexer data. Display dated treasury inflows, tool fees, source transactions, and stale-data warnings. Do not show rate, return, or holder-payout projections. Include a static UI stub and data-source documentation.
```

## Phase 1 Acceptance Gates

| Gate | Required result |
| --- | --- |
| Separate repo or workspace created | Pending |
| TestNet asset strategy defined | Pending |
| Contract threat model written | Pending |
| Unit tests passing | Pending |
| TestNet deployment completed | Pending |
| Deployment record reviewed | Pending |
| Treasury route documented | Pending |
| Burn route disabled pending review | Required |
| Public claims review completed | Pending |
| MainNet deployment approved | Not approved |

Current Gate Status: PHASE 1 SPEC READY FOR REVIEW; IMPLEMENTATION NOT STARTED IN THIS REPOSITORY.
