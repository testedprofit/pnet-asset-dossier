# Media Guide

This guide defines how media should be added to the PNET dossier.

## Purpose

The media archive is for public, reviewable evidence and brand materials connected to the dossier. It is not a place for private files, wallet screenshots, transaction instructions, credentials, or promotional claims.

## Allowed Media

| Media type | Requirement |
| --- | --- |
| Website screenshot | Include URL, capture date, and page title. |
| Tokenomics screenshot | Include URL, capture date, and fields shown. |
| Market listing screenshot | Include source, capture date, and note that market values are volatile. |
| Logo or icon | Include source, rights/license status, and whether it is official or community-provided. |
| Verification screenshot | Include source, checked field, observed value, date, and reviewer. |

## Contribution Evidence Media

Raw third-party dashboards, mining dashboards, bandwidth-sharing dashboards, payout pages, referral dashboards, and wallet screens should not be committed to this repository.

If a contribution proof requires media review, publish only a sanitized receipt or metadata record. The public record should state the category, review date, reviewer, receipt hash, privacy-review status, and verification status. It should not include user-specific earnings, payout values, device identifiers, private wallet addresses, personal referral identifiers, or account screenshots.

## Required Metadata

Every media file should have a matching note in [media/README.md](../media/README.md) or a neighboring metadata file.

| Field | Required |
| --- | --- |
| File name | Yes |
| Source URL or origin | Yes |
| Capture or creation date | Yes |
| Rights or license status | Yes |
| Description | Yes |
| Verification relevance | Yes |
| Redaction status | Yes |

## Safety Rules

- Do not add screenshots containing private keys, seed phrases, wallet addresses that should remain private, account balances that are not intended for publication, API keys, cookies, session tokens, or admin panels.
- Do not add images that imply investment results, income, or expected returns.
- Do not add QR codes unless their destination has been independently checked and recorded.
- Do not add screenshots that instruct readers to connect a wallet, sign a transaction, transfer assets, or grant account permissions.

## Suggested File Naming

Use dated, descriptive names:

| Example | Purpose |
| --- | --- |
| `2026-06-27-testedprofit-tokenomics-overview.png` | Official tokenomics page screenshot |
| `2026-06-27-vestige-pnet-listing.png` | Third-party market listing screenshot |
| `2026-06-27-allo-pnet-listing.png` | Third-party reference screenshot |
