# PNET Security Guide

Status date: 2026-06-27

This guide defines the public security posture for the PNET dossier and future protocol components.

## Security Scope

| Area | Current scope |
| --- | --- |
| Dossier | Documentation, media, references, dated review records |
| Whitepaper | Specification and public claims boundaries |
| Contribution protocol | TestNet starter only; not MainNet; not audited |
| Market-intelligence receipts | Planned; not live |
| Treasury, lock, payment, bridge, or trading logic | Not approved in this dossier |

## Sensitive Material Policy

Never publish:

- mnemonics,
- private keys,
- seed phrases,
- wallet recovery files,
- `.env` files,
- API keys,
- bearer tokens,
- session cookies,
- wallet screenshots,
- private wallet notes,
- personal identity notes not required for public review,
- signer configuration,
- deployment automation containing account secrets.

## Public Claims Security

Misleading language is a security risk because it can cause users to misunderstand the system.

Prohibited public framing:

- guaranteed profit,
- risk free,
- passive income,
- deposit and earn,
- copy trading,
- managed strategy,
- Coinbase listing confirmed,
- guaranteed listing,
- staking rewards,
- APY/APR/ROI,
- treasury-backed returns.

Use the safer wording in [../templates/WEBSITE_COPY.md](../templates/WEBSITE_COPY.md) and [../templates/PUBLIC_ANNOUNCEMENTS.md](../templates/PUBLIC_ANNOUNCEMENTS.md).

## Contract Security Gates

No future PNET contract should be described as live until the following are published:

| Evidence | Requirement |
| --- | --- |
| Source | Public repository and exact commit |
| Build artifacts | Approval TEAL, clear TEAL, ABI, and hashes |
| Deployment record | Network, app ID, tx ID, creator, app address |
| Admin policy | Admin, partner, update, delete, pause, and migration rules |
| Non-custodial review | Confirmation that user PNET is not deposited or transferred |
| Tests | Positive, negative, edge, and static-safety tests |
| Monitoring plan | Admin-call, large-action, and anomaly reporting cadence |
| Audit status | Unaudited, internally reviewed, audited, or blocked |

## Lost Creator Wallet and Operational Wallet Risks

| Item | Risk | Required handling |
| --- | --- | --- |
| Lost creator account | May be misrepresented as verified burned supply | Keep as `Needs verification` until methodology and evidence exist |
| Operational wallet | Role, balance, control model, and authority may be misunderstood | Publish only public address and status until verified |
| Inaccessible-account supply | Could be conflated with direct burns | Use separate terminology and dated methodology |
| Wallet screenshots | Could leak balances, accounts, UI context, or personal data | Do not publish |

## Incident Response

If a security issue or misleading claim is found:

1. preserve evidence,
2. stop repeating the claim,
3. mark the affected item `Needs verification` or `Blocked`,
4. open a public-safe issue or private report depending on exploit sensitivity,
5. patch documentation or code in the correct repository,
6. update the changelog,
7. publish a dated correction when safe.

## Audit Readiness

Before professional audit, prepare:

- design document,
- threat model,
- source commit,
- ABI,
- TEAL artifacts,
- test results,
- deployment plan,
- admin and upgrade policy,
- claims policy,
- known limitations,
- monitoring plan.

Current Gate Status: SECURITY GUIDE READY FOR REVIEW; MAINNET CONTRACT CLAIMS BLOCKED UNTIL AUDIT GATES PASS.
