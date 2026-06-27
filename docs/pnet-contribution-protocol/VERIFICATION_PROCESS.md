# Verification Process: PNET Community Contribution Protocol

Status date: 2026-06-27
Status: MVP process draft. TestNet deployment pending.

## Overview

Contribution claims go through review before app-local access/reputation credits are recorded on-chain.

The process is designed to preserve privacy while keeping final review actions publicly verifiable.

## Current MVP Process

1. User opts into the contribution application.
2. User submits redacted activity evidence through the contribution frontend.
3. Evidence files are hashed locally before public recording.
4. Account or wallet references are hashed before public recording.
5. A reviewer validates the submission.
6. If accepted, app-local access/reputation credits are recorded for the user.
7. If rejected, the rejection can be recorded without assigning credits.
8. Review decisions are recorded on-chain through app calls and `PNET_CC:` logs.

## Supported MVP Categories

| Activity type | Category | Status |
| --- | --- | --- |
| `1` | Kryptex-style compute participation | Draft; service/evidence rules need review |
| `2` | Honeygain / JumpTask-style bandwidth-sharing evidence | Draft; service/evidence rules need review |

Service references are evidence categories only. They do not imply partnership, endorsement, expected outcome, or financial return.

## Privacy

Original screenshots and files are never stored on-chain.

The public on-chain record should include only:

- recipient account,
- activity type,
- credit amount if accepted,
- period code,
- evidence hash,
- account-reference hash,
- review hash,
- reviewer transaction,
- app state updates,
- `PNET_CC:` logs.

Do not publish:

- raw screenshots,
- private dashboards,
- private wallet screenshots,
- payout values,
- earnings values,
- emails or usernames,
- IP addresses,
- device identifiers,
- cookies or sessions,
- private account details.

## Reviewer Roles

MVP:

- manual reviewer,
- admin or approved partner account records the decision on-chain.

Future candidates:

- community verification,
- multi-reviewer approval,
- multisig review policy,
- appeal process for rejected submissions,
- automated checks for specific activity types.

All future changes require updated documentation, tests, claims review, and security review.

## Dossier Publication

All public on-chain review transactions should be published in the public dossier under:

```text
data/on-chain-proofs/contribution-protocol/
```

Deployment proof should be recorded in:

```text
data/on-chain-proofs/contribution-protocol/deployment-testnet.md
```

## Minimum Evidence For A Public Review Record

| Field | Required |
| --- | --- |
| Network | Yes |
| App ID | Yes |
| Transaction ID | Yes |
| Confirmed round | Yes |
| Activity type | Yes |
| Decision | Yes |
| Evidence hash | Yes |
| Account-reference hash | Yes |
| Review hash | Yes |
| Reviewer | Yes |
| Privacy review status | Yes |
| Raw screenshot | No |
| Payout or earnings value | No |

Current Gate Status: VERIFICATION PROCESS DRAFTED; LIVE TESTNET REVIEW RECORDS PENDING DEPLOYMENT.
