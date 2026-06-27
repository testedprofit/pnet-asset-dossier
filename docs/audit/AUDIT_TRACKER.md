# PNET Audit Tracker

Status date: 2026-06-27

## Audit Scope Candidates

| Component | Scope | Current version/source | Status | Required before MainNet |
| --- | --- | --- | --- | --- |
| Community Contribution Protocol | app-local contribution/access credits, admin/partner controls, logs, receipt hashes | Spec in [community-contribution-protocol-spec.md](../implementation/community-contribution-protocol-spec.md); prototype outside dossier | Pre-audit | Yes |
| Market-intelligence receipt anchor | canonical hash anchoring, receipt schema, no private data | Spec in [market-intelligence-api-spec.md](../implementation/market-intelligence-api-spec.md) | Spec draft | Yes if deployed |
| Growth registry | partner/content/referral/social proof receipts | Prototype outside dossier | Pre-audit | Yes if deployed |
| Governance signaling | proposal/vote state and advisory limits | Prototype outside dossier | Pre-audit | Yes if deployed |
| Treasury ledger | accounting-only records and no custody assumptions | Prototype outside dossier | Pre-audit | Yes if deployed |
| Dashboard/API | data correctness, privacy, frontend dependency risk, read-only guarantees | Spec draft | Security review needed | Before public production |

## Audit Provider Tracker

| Provider | Contact date | Scope sent | Quote received | Selected | Notes |
| --- | --- | --- | --- | --- | --- |
| TBD |  |  |  |  |  |

## Findings Tracker

| Finding ID | Component | Severity | Summary | Status | Fix reference | Retest |
| --- | --- | --- | --- | --- | --- | --- |
| TBD |  |  |  |  |  |  |

## Required Audit Inputs

- source code repository,
- commit hash,
- generated ABI,
- approval/clear TEAL or compiled artifacts,
- deployment plan,
- admin/update/delete policy,
- state schema,
- method descriptions,
- action-code registry,
- threat model,
- test report,
- known limitations,
- public claims policy.

Current Gate Status: AUDIT TRACKER CREATED; AUDITOR NOT SELECTED; NO AUDIT REPORT EXISTS.
