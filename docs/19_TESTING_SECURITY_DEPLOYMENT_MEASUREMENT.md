# Testing, Security, Deployment, And Measurement Specification

Status date: 2026-06-27

Scope: This is a documentation-only readiness specification. It does not contain TestNet scripts, deployment scripts, contract code, wallet logic, signer logic, frontend code, CLI code, credentials, private notes, or `.env` files.

## Objective

Define how future PNET implementation work should be tested, reviewed, deployed, and measured before any public claim that utility, governance, receipt anchoring, or treasury-routing systems are live.

## Implementation Boundary

All executable work belongs in a separate implementation repository or private TestNet workspace. This dossier may record reviewed deployment records, test summaries, audit status, public proofs, and KPI snapshots after sensitive material has been excluded.

| Artifact | This dossier | Implementation repo |
| --- | --- | --- |
| Test plan | Yes | Yes |
| Unit test source | No | Yes |
| Contract source | No | Yes |
| ABI files | No | Yes |
| Deployment scripts | No | Yes |
| TestNet deployment records | Summary only | Yes |
| Wallet credentials or signer config | Never | Never committed |
| KPI snapshots | Yes, after review | Yes |

## TestNet Testing Plan

| Area | Required tests |
| --- | --- |
| Staking / proof-of-contribution | Stake, partial unstake, full unstake, zero stake, repeated claim, treasury depletion, tier changes, emergency pause, migration denial, invalid asset, invalid sender |
| Tool payments | Correct payment, missing payment, wrong asset, wrong amount, wrong receiver, duplicate payment, atomic failure, treasury route, burn route disabled |
| Revenue attribution | Treasury inflow capture, outflow labeling, stale-data warning, source-link failure, manual correction, duplicate transaction handling |
| Intelligence receipts | Schema validation, canonical hash stability, source-status handling, stale metrics, content-hash mismatch, correction workflow |
| On-chain hash anchoring | Correct hash note/app state, duplicate anchor, malformed hash, wrong asset ID, indexer query retrieval |
| Governance | Proposal lifecycle, fixed snapshot round, vote weighting, duplicate vote, low turnout, whale concentration display, advisory-only result |
| Operational wallet monitoring | Balance capture, movement detection, source-link persistence, private-note exclusion |

## Security Review Checklist

| Category | Review questions |
| --- | --- |
| Asset validation | Does every contract or module verify the expected ASA and network? |
| Custody surface | Can users recover locked assets according to documented rules? |
| Admin powers | Are privileged methods minimized, documented, and tested? |
| Treasury routing | Are receivers configurable only through reviewed governance/admin flows? |
| Accounting | Can reward, lock, fee, or treasury accounting drift from actual balances? |
| Replays and duplicates | Can the same payment, vote, claim, or receipt be counted twice? |
| Stale data | Does every dashboard metric show capture date and source status? |
| Source integrity | Are source failures, partial reads, and conflicting explorers handled explicitly? |
| Privacy | Are private wallet notes, screenshots, credentials, and identity records excluded? |
| Upgrade/migration | Is migration behavior explicit and tested before deployment? |
| Emergency handling | Is pause, rollback, correction, or deprecation behavior documented? |
| Claims review | Does public copy avoid return, listing, custody, and guarantee framing? |

## Professional Audit Areas

Professional review should be obtained before MainNet deployment for:

| Area | Why it needs review |
| --- | --- |
| Asset escrow / voluntary lock contracts | User funds may be locked by contract rules |
| Reward or allocation accounting | Errors can create unfair claims or treasury loss |
| Tool-payment validation | Atomic transaction checks must be correct |
| Treasury routing | Misrouting can create accounting and trust failures |
| Governance voting | Balance snapshots and vote weighting can be manipulated |
| On-chain hash anchoring | Receipts must be reproducible and tamper-evident |
| Operational-wallet controls | Large holdings create concentration and custody risk |
| Burn accounting methodology | Incorrect methodology can misstate circulating supply |

## Deployment Readiness Plan

### TestNet Gate

| Gate | Requirement |
| --- | --- |
| Source repository | Separate implementation repository exists |
| Credential handling | No credentials, recovery material, or signer config committed |
| Test suite | Unit and integration tests pass |
| Static review | Contract source and deployment scripts reviewed |
| Deployment record | TestNet app IDs, asset IDs, source commit, creator, and date recorded |
| Public documentation | User-facing docs mark deployment as TestNet-only |
| Security notes | Known limitations and audit status published |
| Claims review | No MainNet/live language until evidence exists |

### MainNet Migration Gate

| Gate | Requirement |
| --- | --- |
| TestNet history | Sufficient TestNet runtime and issue log reviewed |
| Audit | Independent review completed or clearly marked as not completed |
| Governance approval | Advisory or formal approval recorded according to governance policy |
| Treasury policy | Treasury route, labels, and proof workflow approved |
| Operational wallet review | Role, balance, controls, and movement history verified |
| Burn methodology | Direct burn, inaccessible-account, lock, and circulating-supply methodology approved |
| Deployment checklist | MainNet parameters reviewed by at least two reviewers |
| Rollback plan | Pause, deprecation, or migration path documented |
| Public announcement | Includes source links, risk notes, and no return/listing claims |

## Deployment Record Template

```markdown
## Deployment Record

Component:
Network:
App / contract ID:
Asset ID:
Source repository:
Source commit:
Deployer / creator address:
Treasury address:
Deployment date:
Audit / review status:
Known limitations:
Public claim status:
Reviewer:
Correction link:
```

## KPI Dashboard Outline

KPI snapshots should be dated, source-linked, and marked stale after publication. They should measure use and transparency, not promise outcomes.

| KPI | Definition | Source | Status |
| --- | --- | --- | --- |
| Voluntary lock total | Amount of PNET or TestNet equivalent locked in reviewed access-tier contracts | Contract/indexer | Pending implementation |
| Tool usage paid in PNET | Count and amount of tool-payment events by component | Contract/indexer | Pending implementation |
| Treasury-attributed inflows | Source-linked tool fees or approved aggregate inflows routed to treasury | Indexer/accounting record | Pending implementation |
| Approved allocation events | Count and amount of policy-approved allocation events, if ever approved | Treasury proof records | Not active; Phase 3 approval required |
| Governance participation | Proposals, unique voters, weighted participation, and concentration notes | Governance records | Pending implementation |
| Intelligence receipt cadence | Receipts published per period and percent with complete source status | Receipt registry | Pending implementation |
| Verification backlog closure | Number of `Needs verification` items resolved with source-linked evidence | Dossier/backlog | Active docs metric |

## KPI Guardrails

| Guardrail | Requirement |
| --- | --- |
| No investment framing | KPIs should measure system use, transparency, and verification progress |
| No payout projections | Do not publish projected holder or staker payouts |
| No stale dashboards without warning | Every dashboard view needs capture date and source freshness |
| No private data | Do not publish private account screenshots, private revenue accounts, or identity records |
| No MainNet inference from TestNet | TestNet metrics must not be framed as production adoption |

## Measurement Cadence

| Cadence | Measurement |
| --- | --- |
| Weekly during TestNet | Test results, open issues, receipt generation, governance test participation |
| Monthly during public review | KPI snapshot, verification backlog, treasury accounting if applicable |
| Before MainNet migration | Full security checklist, deployment gate review, claims review |
| After any incident | Correction note, affected records, mitigation, and reviewer sign-off |

## Section 6 Codex Prompt Snippet

Use this prompt only inside a future implementation repo or private TestNet workspace.

```text
Provide a full TestNet testing plan, security checklist, deployment-readiness guide, and KPI dashboard outline for PNET implementation components. Include tests for voluntary locking, optional tool payments, treasury attribution, intelligence receipts, on-chain hash anchors, and advisory governance. Do not commit credentials, signer material, or deployment configuration containing private material. Treat any direct holder/staker allocation metric as inactive unless legal, governance, security, and public-claims reviews are complete.
```

Current Gate Status: SECTION 6 SPEC READY FOR REVIEW; TESTNET SCRIPTS AND MAINNET DEPLOYMENT NOT INCLUDED IN THIS REPOSITORY.
