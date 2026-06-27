# PNET PDF Scan

Review date: 2026-06-27

Reviewed source: `pnet 1.pdf`

Repository action: The raw PDF was not committed. Safe, actionable review items were summarized in [docs/14_PUBLIC_REVIEW_BACKLOG.md](../../docs/14_PUBLIC_REVIEW_BACKLOG.md).

## File Inspection

| Check | Result |
| --- | --- |
| SHA-256 | `C8396E277576CDDD9F98F54E9A0254B5D7B94EF05F8F17F7BBFF1A4B33DFF9C2` |
| File size | 3,630,248 bytes |
| Pages | 6 |
| Producer | jsPDF 4.0.0 |
| Creation date | 2026-06-27 01:21:41 MDT |
| Encrypted | No |
| Attachments | None found |
| External links | None found |
| JavaScript | None reported by Poppler |
| Forms | None |
| Text layer | Minimal/empty; pages are image-based |
| Render review | Pages rendered to PNG and visually reviewed |

## Sensitive Content Scan

Automated text extraction was limited because the PDF is image-based. A visual page review was performed after rendering.

| Check | Result |
| --- | --- |
| Personal email addresses | None observed |
| Phone numbers | None observed |
| Private keys / seed phrases | None observed |
| API keys / bearer tokens | None observed |
| Wallet screenshots | None observed |
| Identity documents | None observed |
| Transaction-signing material | None observed |
| Local filesystem paths | None observed |

## Coverage Review

Most factual items in the PDF were already present in the dossier, including:

- PNET identity as Algorand ASA `3169177585`,
- fixed supply and decimals,
- apparent cleared manager/reserve/freeze/clawback controls,
- holder concentration risk,
- lock, burn, vault, and circulating-supply verification gaps,
- liquidity fragmentation and low-liquidity cautions,
- public claims policy around earning-oriented language,
- GitHub dossier and whitepaper positioning.

## Sanitization Decisions

| Source material type | Handling |
| --- | --- |
| Factual overlap already in dossier | No duplicate fact records added |
| Improvement suggestions | Converted into a cautious public-review backlog |
| Speculative utility/revenue suggestions | Not imported as claims or commitments |
| Promotional or earning-oriented wording | Not imported as PNET positioning |
| Purchase/onboarding suggestions | Not imported |
| MainNet tool availability statements | Treated as `Needs verification` unless independently sourced |

Current Gate Status: PASS for scan; raw PDF not included.
