# PNET Verification Handbook

Status date: 2026-06-27

This handbook explains how anyone can audit PNET from public sources.

The goal is reproducibility. A reviewer should be able to start from the ASA ID, inspect public sources, and decide which claims are verified, stale, unresolved, or unsupported.

## Verification Standard

Each material claim should include:

| Field | Requirement |
| --- | --- |
| Claim | Plain-language statement |
| Source | Public link or repository file |
| Capture date | Date observed |
| Method | How the value was obtained |
| Observed value | Raw value when possible |
| Derived value | Formula if transformed |
| Status | Verified, snapshot only, Needs verification, or Needs methodology review |
| Limitation | What the check does not prove |

## Asset Identity Check

Check:

- ASA ID,
- asset name,
- unit name,
- decimals,
- total supply,
- URL,
- creator,
- manager,
- reserve,
- freeze,
- clawback,
- default frozen,
- metadata hash if present.

Suggested public sources:

- Algonode Indexer asset endpoint,
- Nodely Indexer asset endpoint,
- Lora asset page,
- Pera Explorer asset page,
- Allo asset page.

Record both raw supply and display supply:

```text
display_supply = raw_total / 10^decimals
```

## Control Field Check

For manager, reserve, freeze, and clawback:

1. read the asset record from at least two public sources,
2. confirm whether each field is empty, zeroed, or set,
3. record source date,
4. inspect transaction history if claiming controls were renounced,
5. mark the claim `Needs verification` until transaction-history review is complete.

What this proves:

- whether current public sources show active ASA control addresses.

What this does not prove:

- fair distribution,
- safe liquidity,
- wallet ownership,
- project integrity,
- absence of off-chain risk.

## Supply and Tokenomics Check

Separate supply categories:

| Category | Verification method |
| --- | --- |
| Total supply | ASA raw total and decimals |
| Direct burned supply | Burn address or transaction set with methodology |
| Inaccessible-account supply | Methodology and reviewer sign-off; do not call direct burn without evidence |
| Locked supply | Lock contract/app/account evidence and unlock conditions |
| Circulating supply | Published formula and excluded accounts |
| Liquidity supply | Pool account balances and pool labels |

The following remain `Needs verification` unless independently confirmed:

- burned supply shown on website,
- founder allocation lock,
- strategic reserve lock,
- September 2026 unlock details,
- LP/vault labels,
- partner allocation labels,
- operational wallet role and balance.

## Holder Review

Suggested method:

1. query asset balances from an indexer,
2. exclude zero balances only if documented,
3. sort balances descending,
4. compute top-holder concentration,
5. label wallets only when public evidence supports the label,
6. mark unknown labels as `Needs human confirmation`.

Do not publish private wallet screenshots or personal notes.

## Market and Liquidity Review

Market metrics are stale immediately after capture.

For each market snapshot, record:

- source,
- capture date,
- pool or route ID if available,
- counter-asset,
- liquidity or TVL metric,
- volume metric if shown,
- methodology limitations,
- status as `Snapshot only`.

Public market references may include Vestige, Tinyman, Pact, ASAstats, Allo, and explorer account views.

## Contribution Protocol Review

Before trusting a contribution protocol deployment, verify:

| Check | Evidence |
| --- | --- |
| Network | TestNet or MainNet |
| App ID | Explorer/indexer link |
| Deployment transaction | Public tx link |
| Creator | Public address |
| Source | Public repository and commit |
| ABI | Machine-readable ABI and method table |
| Artifact hashes | Approval and clear program hashes |
| Admin policy | Admin, partner, pause, update, delete rules |
| Non-custodial behavior | No user PNET deposit or transfer path |
| Receipt policy | Meaning and storage of receipt hashes |
| Audit status | Unaudited, reviewed, audited, deprecated, or blocked |

If any item is missing, mark the deployment `Needs verification` or `Not ready`.

## Public Claims Review

Reject or rewrite any claim that implies:

- guaranteed profit,
- risk-free participation,
- passive income,
- deposit and earn,
- copy trading,
- managed strategy,
- Coinbase listing confirmed,
- guaranteed listing,
- guaranteed value,
- yield or APY.

Safe replacement pattern:

```text
PNET documentation records dated public evidence and unresolved claims. Contribution credits, if deployed, are app-local access/reputation records only and do not represent deposits, yield, passive income, guaranteed value, or investment return.
```

## Verification Report Template

```markdown
## Verification Report

Status date:
Reviewer:
Scope:

### Claim

### Source Links

### Method

### Observed Values

### Status

### Limitations

### Follow-up
```

Current Gate Status: VERIFICATION HANDBOOK READY FOR REVIEW; OPEN CLAIMS REMAIN MARKED.
