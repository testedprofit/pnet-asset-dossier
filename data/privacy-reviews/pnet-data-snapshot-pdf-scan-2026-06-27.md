# PNET Standalone Data Snapshot PDF Scan

Review date: 2026-06-27

Reviewed source: `ProfitNet_PNET_Data_Snapshot_2026-06-27_Standalone.pdf`

Repository action: The raw PDF was not committed. The PDF contains user-provided operational wallet context, stale market ranges, and internal/reference-use wording. Safe findings were converted into backlog items in [docs/14_PUBLIC_REVIEW_BACKLOG.md](../../docs/14_PUBLIC_REVIEW_BACKLOG.md).

## File Inspection

| Check | Result |
| --- | --- |
| SHA-256 | `B392E7EA195FBF559F367E313EF35F70194BB501494351F3C1A8D1C759721F1E` |
| File size | 10,376 bytes |
| Pages | 3 |
| Title metadata | `ProfitNet PNET Data Snapshot June 27 2026` |
| Author metadata | `ProfitNet Team Reference Document` |
| Producer | ReportLab PDF Library |
| Creation date | 2026-06-27 07:32:54 UTC |
| Encrypted | No |
| Attachments | None found |
| External links | None found |
| JavaScript / launch actions | None found |
| Forms | None found |
| Text layer | Present |
| Render review | Pages rendered to PNG and visually reviewed |

## Sensitive Content Scan

| Check | Result |
| --- | --- |
| Personal email addresses | None found |
| Private-key blocks / recovery words | None found |
| API keys / bearer tokens | None found |
| GitHub tokens | None found |
| Wallet screenshots | None found |
| Identity documents | None found |
| Transaction-signing material | None found |
| Local filesystem paths | None imported |
| Operational wallet context | Present in source; exact address not imported |

## Public-Safe Candidate Items

| Candidate item | Handling |
| --- | --- |
| Claimed lost-creator burn path | Added to backlog as `Needs on-chain and disclosure review` |
| Operational wallet label | Added to backlog as a disclosure-review task without publishing the address |
| Creation date and Pera verification status | Already present in backlog from the prior PDF scan |
| Supply-definition methodology | Already present in backlog; reinforced by this snapshot |
| Explorer-difference reconciliation | Already present in backlog through supply/burn/circulation methodology tasks |
| Wallet-movement monitoring | Added to backlog as a future method task only after disclosure approval |
| Stale market ranges | Not imported; market data must remain dated and source-linked |

## Sanitization Decisions

| Source material type | Handling |
| --- | --- |
| User-provided operational address | Not imported until explicitly approved for public disclosure and independently verified |
| Internal/reference-use source wording | Raw PDF not committed |
| Claims marked as verified or authoritative inside the source | Downgraded to review tasks unless already independently sourced |
| Market-cap or upside language | Not imported |
| Tooling, lock, or treasury suggestions | Converted to review tasks only; no implementation added |
| Attached code-generation prompt | Not implemented in this docs-only repository; future code belongs in a separate implementation repository after security review |

Current Gate Status: PASS for scan; raw PDF not included; operational address not published.
