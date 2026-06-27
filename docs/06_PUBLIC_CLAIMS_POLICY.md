# Public Claims Policy

This policy defines how public claims about ProfitNet / PNET should be written in this repository.

## Core Rule

Use neutral, dated, source-linked statements. Do not use investment framing, income framing, guaranteed-return framing, custody framing, or delegated trading framing.

## Allowed Claim Types

| Claim type | Requirement |
| --- | --- |
| Page-displayed fact | Include source URL, snapshot date, observed value, and `Needs verification` status unless independently verified. |
| On-chain fact | Include explorer/indexer source, date checked, exact observed value, and reviewer. |
| Market data | Treat as dated snapshot only. Never present as a stable fact. |
| Media asset | Include origin, capture date, license or rights status, and description. |
| Derived value | State the formula or dependency and keep the derived value verification-gated. |

## Disallowed Claim Types

Do not add claims that suggest:

| Claim category | Repository handling |
| --- | --- |
| Guaranteed outcomes | Do not include. |
| Investment performance | Do not include. |
| Income expectations | Do not include outside the QA note below. |
| Managed strategy or delegated trading | Do not include. |
| User deposits or custody | Do not include. |
| Wallet connection as a verification step | Do not include. |
| Coinbase, exchange, bridge, or listing support | Do not include unless there is direct source evidence from the named venue. |

## Removed / Avoided Claims QA Note

The testedprofit public pages include passive-income and earning-oriented wording. This repository intentionally does not use those phrases as token positioning, utility language, investment framing, or reader-facing benefit claims.

## Verification Labels

Use these labels consistently:

| Label | Meaning |
| --- | --- |
| Needs verification | The value is recorded but not independently confirmed. |
| Needs on-chain verification | The value should be checked against an explorer, indexer, transaction, account, or asset record. |
| Snapshot only | The value was observed on a date and may change. |
| Verified | Only use when the source, date, method, observed value, and reviewer are recorded. |

## Editing Checklist

Before merging public claims:

| Check | Required result |
| --- | --- |
| Source link present | Yes |
| Snapshot date present | Yes |
| Verification label present | Yes |
| No investment framing | Yes |
| No transaction instructions | Yes |
| No secrets or credentials | Yes |
