# PNET Threat Model

Status date: 2026-06-27
Status: Draft threat model for future review.

## Assets to Protect

| Asset | Threat |
| --- | --- |
| Public trust record | false claims, stale facts, unsupported tokenomics |
| Contract state | unauthorized admin/partner actions, bad upgrades, incorrect accounting |
| Receipt integrity | mismatched hashes, private data in receipts, unverifiable sources |
| User wallets | misleading transaction prompts, phishing, private data leakage |
| Operational wallet disclosures | mislabeling, overstatement, privacy/security leakage |
| Dashboard/API data | stale, wrong, manipulated, or misunderstood data |
| Community channels | hype, scam links, unsupported partner/listing claims |

## Threat Categories

| Threat | Severity | Mitigation |
| --- | --- | --- |
| Unauthorized admin action | High | narrow admin powers, logs, monitoring, multisig/timelock review before MainNet |
| Bad partner/reviewer grant | Medium | partner registry, limits, reason codes, public correction process |
| Receipt hash mismatch | Medium | canonical JSON, hash verification UI, stored source records |
| Private data committed | High | secret scans, contributor guidelines, no wallet screenshots |
| Misleading yield/investment framing | High | claims matrix, scanner, legal review |
| Contract upgrade risk | High | publish update/delete policy and audit before MainNet |
| Frontend dependency vulnerability | Medium | dependency audit, pin versions, security review |
| Indexer/API inconsistency | Medium | cross-check Algonode/Nodely/explorer sources |
| Burn/lock misclassification | High | proof packets and methodology review |
| Operational wallet misinterpretation | High | clear status labels and maintainer disclosure |

## Trust Assumptions

- Public indexers can lag or disagree.
- Repository maintainers can make mistakes.
- Admin keys may be compromised if not secured.
- Community submissions can contain false claims.
- Wallet ownership cannot be proven by address balance alone.
- Lost-wallet claims cannot be verified solely from chain state.

## Required Before MainNet

- professional audit or documented equivalent security review,
- admin/control policy,
- deployment registry,
- monitoring,
- emergency pause/response plan,
- legal/public-claims review,
- public known-limitations section.

Current Gate Status: THREAT MODEL DRAFTED; PROFESSIONAL REVIEW REQUIRED BEFORE MAINNET.
