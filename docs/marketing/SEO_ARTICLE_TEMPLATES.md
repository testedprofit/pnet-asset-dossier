# SEO Article Templates

Status date: 2026-06-27

These templates are ready for blog or website use. Replace bracketed fields before publishing. Keep claims source-linked, dated, and non-promotional.

## Template 1: How to Verify Any Algorand ASA Tokenomics

SEO title: How to Verify Any Algorand ASA Tokenomics
Meta description: Learn a repeatable method for checking Algorand ASA supply, decimals, control fields, burns, locks, liquidity, and public tokenomics claims.
Slug: `how-to-verify-algorand-asa-tokenomics`
Primary keyword: Algorand ASA tokenomics
Secondary keywords: ASA supply, Algorand token verification, ASA control fields, tokenomics checklist

### Ready-to-use article

```markdown
# How to Verify Any Algorand ASA Tokenomics

Tokenomics review should start with public records, not project summaries.

An Algorand Standard Asset has public fields that help reviewers separate facts from claims: ASA ID, asset name, unit name, decimals, total supply, URL, creator, manager, reserve, freeze, clawback, and default frozen status.

This guide shows a repeatable review method.

## 1. Start With The ASA ID

The ASA ID is the anchor. Search the asset on at least two public sources, such as an indexer and an explorer.

Record:

- ASA ID,
- asset name,
- unit name,
- decimals,
- total raw supply,
- display supply,
- URL,
- creator.

## 2. Convert Raw Supply Correctly

Use:

`display supply = raw supply / 10^decimals`

If the raw total is `100000000000000` and decimals are `6`, the display supply is `100,000,000`.

## 3. Review Control Fields

Check manager, reserve, freeze, and clawback.

If a project says controls are renounced, do not stop at the claim. Confirm the current fields and review transaction history where possible.

## 4. Separate Supply Categories

Do not merge these without methodology:

| Category | Meaning |
| --- | --- |
| Total supply | Asset supply from the ASA record |
| Direct burned supply | Tokens proven unrecoverable by public transaction evidence |
| Inaccessible-account supply | Tokens believed inaccessible because an account is unavailable |
| Locked supply | Tokens held in a reviewed lock or escrow |
| Liquidity supply | Tokens in pool or LP accounts |
| Circulating supply | Methodology-defined supply available under a stated formula |

## 5. Treat Market Data As A Snapshot

Liquidity, volume, price, and route data change. Record the source and date, then mark the observation as a snapshot.

## 6. Mark Unknowns

`Needs verification` is a useful label. It tells readers that a claim exists but should not be repeated as fact.

## Checklist

- [ ] ASA ID checked
- [ ] Name and unit checked
- [ ] Decimals checked
- [ ] Raw and display supply checked
- [ ] Control fields checked
- [ ] Burn claims separated from inaccessible-account claims
- [ ] Locks verified by on-chain evidence
- [ ] Market data dated
- [ ] Unknowns marked

Educational content only. No investment advice, no deposit request, no passive-income claim, no guaranteed value, and no exchange-listing claim.
```

## Template 2: How to Read ASA Control Fields

SEO title: How to Read Algorand ASA Control Fields
Meta description: Understand manager, reserve, freeze, and clawback fields for Algorand assets and why they matter for public asset review.
Slug: `algorand-asa-control-fields-explained`
Primary keyword: ASA control fields

### Ready-to-use article

```markdown
# How to Read Algorand ASA Control Fields

Algorand ASAs expose control fields that are important for asset review.

The four fields to check are manager, reserve, freeze, and clawback.

## Manager

The manager field controls whether certain asset configuration changes can be made. If the manager is cleared, that capability may be permanently removed. Confirm current state from public sources and review transaction history before relying on the claim.

## Reserve

The reserve field can identify an account associated with undistributed supply. A reserve field alone does not prove treasury policy, lock status, or circulating supply.

## Freeze

The freeze field can allow asset freezing if configured. A cleared freeze field may reduce control risk, but it does not prove liquidity quality or distribution fairness.

## Clawback

The clawback field can allow asset transfer from accounts if configured. A cleared clawback field may reduce control risk, but it does not remove all project or market risks.

## Review Method

1. Search the ASA ID in two public sources.
2. Record the four fields.
3. Capture the date.
4. Check transaction history for claimed renunciation.
5. Mark unresolved items as `Needs verification`.

## Safe Interpretation

Cleared controls can be a trust point. They are not a guarantee of value, liquidity, listing support, or project success.
```

## Template 3: Market Snapshot vs Live Metric

SEO title: Market Snapshot vs Live Metric in Crypto Asset Research
Meta description: Learn why liquidity, TVL, volume, and route data should be treated as dated snapshots unless refreshed from public sources.
Slug: `market-snapshot-vs-live-metric`
Primary keyword: crypto market snapshot

### Ready-to-use article

```markdown
# Market Snapshot vs Live Metric

Market data changes quickly.

A liquidity number, volume figure, TVL value, or route quote may be useful at capture time and misleading later.

## Snapshot

A snapshot is a dated observation. It should include source, date, value, method, and limitation.

Example:

| Field | Example |
| --- | --- |
| Source | Vestige asset page |
| Date | 2026-06-27 |
| Observed value | [insert value] |
| Method | Manual page review |
| Status | Snapshot only |

## Live Metric

A live metric is current only when requested. If a page or API changes, a prior value should not be repeated as current.

## Best Practice

Write:

`Liquidity observed on [date] from [source]. Snapshot only. Recheck before relying on it.`

Do not write:

`This asset has [value] liquidity.`

## Why This Matters

Dated market records protect readers from stale claims and help reviewers understand what was known at the time.
```

## Template 4: What App-Local Contribution Credits Are

SEO title: What App-Local Contribution Credits Are
Meta description: A public-safe explanation of non-custodial contribution credits for access and reputation workflows.
Slug: `app-local-contribution-credits-explained`
Primary keyword: contribution credits

### Ready-to-use article

```markdown
# What App-Local Contribution Credits Are

App-local contribution credits are records inside an application.

They may support access and reputation workflows for approved ecosystem participation. They are not tokens, deposits, yield, passive income, guaranteed value, or claims on treasury assets.

## Why They Exist

Communities need ways to recognize useful participation without turning every action into a financial promise.

Contribution credits can record participation context while keeping custody and investment framing out of scope.

## What They Can Support

- access to community features,
- reputation signals,
- participation history,
- reviewer contribution tracking,
- transparent action logs.

## What They Must Not Claim

- passive income,
- APY or APR,
- guaranteed value,
- PNET payout,
- treasury claim,
- exchange listing,
- deposit program.

## Verification Requirements

Before any live deployment is described publicly, publish:

- app ID,
- deployment transaction,
- source commit,
- ABI,
- admin policy,
- action-code registry,
- receipt policy,
- audit status.

Educational content only. Verify public sources before relying on any protocol claim.
```

## Reusable SEO Blocks

### FAQ Block

```markdown
## FAQ

### Is this investment advice?

No. This article is educational and focused on public verification methods.

### Does verification remove risk?

No. Verification can reduce confusion, but it does not guarantee value, liquidity, safety, or future support.

### What should I do with an unsupported claim?

Mark it `Needs verification` until public evidence, date, method, and reviewer context are available.
```

### Author Bio

```markdown
ProfitNet publishes verification-first guides for Algorand asset review, public market-intelligence records, and safe community contribution workflows.
```

Current Gate Status: SEO ARTICLE TEMPLATES READY FOR REVIEW.
