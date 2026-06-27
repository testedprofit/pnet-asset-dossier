# Phase 3 Revenue Feedback And Tokenomics Hardening Specification

Status date: 2026-06-27

Scope: This is a documentation-only implementation specification. It does not contain contract code, deployment scripts, multisig setup instructions, wallet logic, signer logic, frontend code, CLI code, credentials, private notes, or `.env` files.

## Objective

Define a safe Phase 3 path for revenue feedback, operational-wallet hardening, and tokenomics methodology improvements. Phase 3 should improve transparency and sustainability without promising returns, implying investment performance, or launching unreviewed value-distribution mechanics.

## Phase 3 Position

Direct distribution of platform revenue to token holders or stakers is not approved by this specification. Any future mechanism that routes revenue to stakers, burns, liquidity, or treasury must pass legal review, governance review, security review, and public-proof review before publication as a live mechanism.

## Design Principles

| Principle | Requirement |
| --- | --- |
| Treasury accounting first | Publish source-linked inflows and outflows before designing allocation mechanics |
| No implied returns | Do not frame any mechanism as income, return, or holder payout |
| TestNet before MainNet | Simulate allocation logic before real funds are routed |
| Public proofs | Every allocation event needs source transaction, amount, asset, date, and policy reference |
| Governance before allocation | Community signaling should precede any non-operational allocation policy |
| Legal review before distribution | Any staker-directed or holder-directed mechanism requires external legal review |

## Revenue Feedback Policy Ladder

| Stage | Revenue routing | Status | Purpose |
| --- | --- | --- | --- |
| 3A: Accounting only | 100% to documented treasury or operating accounts | Recommended first step | Prove reporting, source labels, and audit trail |
| 3B: TestNet simulation | Simulated splits only; no real-value distribution | Future research | Test accounting logic, dashboards, and governance flow |
| 3C: Treasury policy | Defined operating, security, liquidity, and reserve buckets | Needs governance review | Make treasury use predictable and reviewable |
| 3D: Burn or liquidity policy | Optional, policy-governed treasury action | Needs legal/security/governance review | Explore supply or liquidity effects without promises |
| 3E: Staker-directed flow | Not approved | Requires legal, audit, governance, and claims review | High-risk mechanism |

## Candidate Allocation Templates

These templates are research models, not commitments.

| Template | Treasury | Security/audit reserve | Liquidity or burn research | Staker-directed flow | Status |
| --- | --- | --- | --- | --- | --- |
| Conservative accounting | 100% | 0% | 0% | 0% | Recommended initial policy |
| Operating hardening | 80% | 20% | 0% | 0% | Future governance research |
| Liquidity research | 70% | 20% | 10% | 0% | Requires treasury policy |
| Burn research | 70% | 20% | 10% | 0% | Requires burn methodology |
| Direct staker flow | Undefined | Undefined | Undefined | Undefined | Not approved |

## Public Proof Requirements

| Proof item | Requirement |
| --- | --- |
| Source category | Tool fee, referral aggregate, treasury transfer, manual adjustment, or other source |
| Amount | Exact amount and asset |
| Date | Capture date and transaction date where applicable |
| Source transaction | Explorer or indexer reference when on-chain |
| Off-chain evidence | Aggregate-only disclosure for non-chain revenue; no private account screenshots |
| Destination label | Treasury, security reserve, liquidity research, burn research, or other approved label |
| Policy reference | Link to the policy version governing the route |
| Reviewer | Reviewer handle or role |
| Correction path | Dated correction process for errors |

## Operational Wallet Hardening

Operational wallet recommendations are public-safety practices, not proof that the wallet role, balance, or project-control status has been independently verified.

User-provided operational wallet:

`CIVTUU6KLTYO26SPVEBDFBKP3UMZM2DPEO5RINODUVCI5NVIFC6HVNWS7E`

| Recommendation | Requirement |
| --- | --- |
| Verify role and balance | Confirm wallet role, current balance, and movement history from public indexers |
| Publish label only after review | Public label should include date, source, reviewer, and status |
| Segment functions | Separate operating funds, long-term reserves, liquidity actions, and test funds where practical |
| Consider time-locks | Use ProfitLock or another reviewed lock method only after contract/security review |
| Avoid single-person control | Move toward multisig or equivalent reviewed controls for treasury-scale holdings |
| Publish movement notes | Explain large movements with dated, source-linked notes |
| Avoid private operational details | Do not publish recovery details, device details, personal identities, or private custody notes |
| Maintain incident path | Define how corrections, compromised-wallet concerns, or emergency migrations are disclosed |

## Time-Lock Research Criteria

Before any operational-wallet tokens are time-locked, the project should document:

| Gate | Required evidence |
| --- | --- |
| Lock mechanism | Contract/app ID, source code, audit status, and admin powers |
| Amount | Exact asset amount and percentage of verified balance |
| Duration | Start date, unlock date, and any cliff or linear release terms |
| Escape conditions | Whether emergency migration exists and who controls it |
| Public purpose | Reserve, strategic allocation, liquidity policy, or other neutral label |
| Reviewer sign-off | Maintainer and security reviewer approval |

## Lost-Wallet Burn Accounting Methodology

The dossier should distinguish direct burn balances from inaccessible-account accounting. This avoids mixing explorer-visible burn figures with user-provided claims.

| Supply category | Definition | Status requirement |
| --- | --- | --- |
| Total supply | Fixed ASA supply recorded on-chain | Verify from indexer |
| Direct burned supply | Amount held by recognized burn addresses or direct burn mechanisms | Verify from explorer/indexer |
| Inaccessible-account supply | Amount believed inaccessible because account control is unavailable | Needs disclosure and human review |
| Opt-out-to-creator loss | Tokens that may become irrecoverable through opt-out or transfer paths to an unavailable creator account | Needs on-chain and disclosure review |
| Circulating supply | Total supply minus categories excluded by the published methodology | Needs methodology approval |
| Locked supply | Tokens in time-lock, escrow, or other reviewed lock mechanism | Needs on-chain lock verification |

## Sample Tokenomics Documentation Text

The following language is safe to use only after the underlying facts are verified. Until then, keep `Needs verification` labels.

```text
PNET supply accounting separates direct burned supply, reviewed locked supply, and any inaccessible-account supply. Direct burned supply is counted only when supported by explorer or indexer evidence. Inaccessible-account supply is not treated as verified burned supply unless the project publishes a dated methodology, public evidence, and reviewer sign-off. The user-provided claim that the original creator account is unavailable remains Needs verification until the burn-path review is complete.
```

## Phase 3 Codex Prompt Snippet

Use this prompt only inside a future implementation repo or private TestNet workspace.

```text
Design a TestNet-first revenue feedback and treasury accounting prototype for PNET. Begin with public treasury accounting and simulated allocation policies. Do not implement direct staker or holder distributions unless legal, governance, audit, and public-claims reviews are explicitly complete. Include public-proof records for source, amount, date, route, transaction, policy version, and reviewer. Include operational-wallet hardening recommendations for CIVTUU6KLTYO26SPVEBDFBKP3UMZM2DPEO5RINODUVCI5NVIFC6HVNWS7E, marked Needs verification until public indexer review confirms role and balance.
```

## Phase 3 Acceptance Gates

| Gate | Required result |
| --- | --- |
| Treasury accounting template reviewed | Pending |
| Revenue source labels defined | Pending |
| Legal review completed | Pending |
| Governance review completed | Pending |
| Security review completed | Pending |
| Operational wallet role and balance verified | Pending |
| Time-lock mechanism reviewed | Pending |
| Burn accounting methodology approved | Pending |
| Public proof workflow tested | Pending |
| Direct staker flow approved | Not approved |

Current Gate Status: PHASE 3 SPEC READY FOR REVIEW; REVENUE DISTRIBUTION NOT APPROVED; IMPLEMENTATION NOT STARTED IN THIS REPOSITORY.
