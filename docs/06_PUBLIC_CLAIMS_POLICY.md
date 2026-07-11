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
| Contribution evidence | State category, review date, reviewer, receipt hash, and privacy status. Do not publish user-specific payouts, balances, private wallet screenshots, or personal referral identifiers. |

## Disallowed Claim Types

Do not add claims that suggest:

| Claim category | Repository handling |
| --- | --- |
| Guaranteed outcomes | Do not include. |
| Investment performance | Do not include. |
| Income expectations | Do not include outside the QA note below. |
| Managed strategy or delegated trading | Do not include. |
| Undisclosed repurchase or market support | Do not present issuer-, founder-, treasury-, affiliate-, or related-party-funded repurchase, liquidity-support, or market-support activity as organic demand, a price floor, guaranteed liquidity, appreciation, returns, or buyer protection. |
| User deposits or custody | Do not include. |
| Wallet connection as a verification step | Do not include. |
| Coinbase, exchange, bridge, or listing support | Do not include unless there is direct source evidence from the named venue. |
| User-specific third-party earnings | Do not publish. Contribution evidence may be reviewed only as redacted activity evidence for app-local credits. |
| Market-cap comparisons to user earnings | Do not include. They can imply investment upside or token-value linkage. |
| Cost-free or renewable-energy claims | Do not include unless independently evidenced and scoped. Renewable energy may be listed as future research or roadmap only. |

## Removed / Avoided Claims QA Note

The testedprofit public pages include passive-income and earning-oriented wording. This repository intentionally does not use those phrases as token positioning, utility language, investment framing, or reader-facing benefit claims.

## Token Sale and Market-Support Disclosure

Before any token sale is announced or opened, any planned issuer-, founder-, treasury-, affiliate-, or related-party-funded PNET repurchase, liquidity-support, or market-support program must receive written review from qualified securities, commodities, and market-manipulation counsel. Counsel-approved public sale materials must disclose all material terms and a truthful non-sensitive funding-source category.

Full funding-source details belong in private counsel/compliance records. Sensitive operational details may be redacted from the public record only if the public category and material economic terms remain truthful and non-misleading and counsel approves the redaction. No program may be framed as a price floor, appreciation mechanism, guaranteed liquidity, return promise, or substitute for organic demand, and no activity may be used to manufacture auction participation, volume, price, holder count, or listing evidence. This is a generic disclosure rule, not authorization for a PNET repurchase, market-support program, or sale term. If a program is planned, the dossier and sale materials must be updated before any sale is announced or opened.

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
| No personal dashboards, private wallet screenshots, or user-specific payout values | Yes |
| No market-cap comparison to user-specific external activity | Yes |
| No unevidenced cost-free, energy-source, or environmental-impact claim | Yes |
| Any planned issuer/founder/affiliate-funded repurchase or market-support program disclosed and counsel-reviewed before a token sale | Yes or not applicable |
