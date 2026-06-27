# Verification Guide

This guide describes a read-only process for checking PNET asset facts.

## Verification Principles

- Use read-only public sources.
- Do not connect a wallet to verify this dossier.
- Do not sign transactions.
- Do not transfer assets.
- Record the source, date, checked field, observed value, and reviewer.
- Keep a fact marked `Needs verification` until the evidence is documented.

## Step 1: Verify Algorand Asset Metadata

Check ASA ID `3169177585` using a reputable Algorand explorer or indexer.

Record:

| Field | Status |
| --- | --- |
| ASA ID exists | Needs verification |
| Asset name is ProfitNet | Needs verification |
| Unit name is PNET | Needs verification |
| Decimals are 6 | Needs verification |
| Total supply matches 100,000,000 display units | Needs verification |
| Creator address | Needs verification |
| Manager, reserve, freeze, and clawback addresses | Needs verification |

## Step 2: Verify Official Website References

Review:

- https://testedprofit.com
- https://testedprofit.com/pages/tokenomics/

Record whether those pages identify the same brand, token name, unit, ASA ID, supply, decimals, and any stated tokenomics.

## Step 3: Verify Third-Party Listing

Review:

- https://vestige.fi/asset/3169177585

Record whether the listing matches the provided ASA ID and metadata fields.

## Step 4: Compare Sources

Use this table when updating the dossier:

| Field | Algorand source | Official website | Vestige | Final status |
| --- | --- | --- | --- | --- |
| ASA ID | Needs verification | Needs verification | Needs verification | Needs verification |
| Token name | Needs verification | Needs verification | Needs verification | Needs verification |
| Unit | Needs verification | Needs verification | Needs verification | Needs verification |
| Total supply | Needs verification | Needs verification | Needs verification | Needs verification |
| Decimals | Needs verification | Needs verification | Needs verification | Needs verification |
| URL metadata | Needs verification | Needs verification | Needs verification | Needs verification |

## Step 5: Update Status

Only change `Needs verification` to `Verified` after adding:

| Evidence Field | Requirement |
| --- | --- |
| Source | Public URL, chain reference, or dated archive |
| Date | Calendar date of review |
| Method | Plain-language description of how it was checked |
| Result | Exact observed value |
| Reviewer | Name or handle of the reviewer |

