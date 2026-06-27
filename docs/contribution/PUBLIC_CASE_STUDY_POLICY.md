# Public Case Study Policy

Status date: 2026-06-27
Status: Draft policy. Applies to external activity examples, website copy, public announcements, and dossier examples.

## Purpose

External activity examples can help explain how contribution evidence is reviewed, but they can also create privacy, claims, and regulatory risk.

This policy defines what may be published when describing Kryptex-style compute-participation evidence, Honeygain / JumpTask-style bandwidth-sharing evidence, referral-campaign evidence, or similar real-world contribution categories.

## Public Decision

Do not publish user-specific earnings, payout values, daily averages, account balances, hardware profitability, market-cap comparisons, or private screenshots in the public dossier or website.

The public record should show:

- contribution category,
- review date,
- reviewer or reviewer address,
- decision,
- receipt hash,
- privacy-review status,
- app-local contribution credit amount if accepted,
- verification status.

## Why This Restriction Exists

| Risk | Reason |
| --- | --- |
| Privacy leakage | Earnings screenshots, account dashboards, device details, and wallet screens can expose personal or operational data. |
| Investment framing | Comparing a user's external activity to PNET market cap can imply financial upside or token value linkage. |
| Unstable data | Mining and bandwidth-sharing outcomes vary by hardware, electricity, network, service rules, prices, and availability. |
| Third-party service risk | Service terms and screenshot-sharing policies may restrict how evidence can be used. |
| Public-claims risk | Words such as profit, passive income, earning stream, and return can be misread as PNET benefit claims. |
| Energy-claim risk | Dual-use hardware and renewable-energy references can be misread as cost, impact, or sustainability claims unless evidence and limits are clear. |

## Allowed Public Example Format

Use a neutral contribution record.

```markdown
## External Activity Review Example

Status date: YYYY-MM-DD
Category: Compute-participation evidence
Service reference: Kryptex-style evidence
Decision: Accepted
Reviewer: [reviewer address or documented reviewer ID]
Evidence hash: [32-byte hash]
Review hash: [32-byte hash]
Privacy review: Passed
Public notes: Redacted evidence reviewed. No private screenshots, earnings values, account identifiers, device IDs, or wallet details are published.
Credits issued: [amount] app-local contribution credits
Verification status: Snapshot only
```

## Disallowed Public Example Format

Do not publish examples that include:

- monthly or daily earnings values,
- external payout values,
- net profit estimates,
- electricity-adjusted profit claims,
- hardware-specific profitability claims,
- claims that compute activity is cost-free, renewable, or environmentally neutral,
- user wallet screenshots,
- account dashboard screenshots,
- withdrawal addresses,
- private referral identifiers,
- comparisons to PNET market cap,
- statements that adoption could increase token value,
- claims that external activity creates PNET yield, passive income, or investment return.

## Safe Website Copy

Use:

> PNET may review redacted third-party activity evidence as part of the Community Contribution Protocol. Accepted submissions may receive app-local contribution credits for access and reputation workflows. Public records should contain only hashes, category codes, reviewer decisions, and non-sensitive metadata.

Do not use:

> Users can earn income through mining or bandwidth sharing and turn it into PNET value.

## Internal Review Notes

Maintainers may privately review screenshots or dashboard exports only if:

- the user intentionally submits them,
- private details are redacted where possible,
- the files are not committed to this repository,
- retention rules are documented,
- reviewer access is limited,
- the public receipt contains only hashes and non-sensitive metadata.

## Case Study Publication Checklist

| Check | Required result |
| --- | --- |
| No user-specific earnings or payout values | Yes |
| No market-cap comparison | Yes |
| No private wallet screenshot | Yes |
| No account dashboard screenshot committed | Yes |
| No income/yield/profit framing | Yes |
| No cost-free, renewable-energy, or environmental-neutrality claim | Yes |
| Service details marked `Needs verification` unless reviewed | Yes |
| Evidence hash and review hash present | Yes |
| Privacy-review status present | Yes |
| Credits described as app-local access/reputation credits only | Yes |

Current Gate Status: PUBLIC CASE STUDY POLICY DRAFTED; USER-SPECIFIC EXTERNAL EARNINGS EXAMPLES SHOULD NOT BE PUBLISHED.
