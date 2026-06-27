# PNET Community Contribution Protocol Final Package

Status date: 2026-06-27

Scope: public-safe synthesis for the planned PNET Community Contribution Protocol and its separate TestNet prototype.

Current Gate Status: TESTNET PROTOTYPE REVIEW ONLY; NOT MAINNET; NOT AUDITED; NOT LIVE.

## Executive Summary

The PNET Community Contribution Protocol is a planned non-custodial Algorand application for app-local contribution credits that may support access and reputation features for approved ecosystem participation. The current prototype separates contribution accounting from token custody: it does not require user deposits, does not transfer user PNET, does not create yield, and does not make claims about value. The next stage is to prove the design through public TestNet deployment records, reproducible source and ABI publication, receipt-hash verification, measured usage reports, and independent security review before any MainNet decision.

## Implementation Status

### Completed In Separate TestNet Prototype Workspace

The implementation prototype is separate from this docs-only dossier. This dossier may summarize status, but source code and deployment tooling must remain in a separate implementation repository until publication review is complete.

| Area | Status | Notes |
| --- | --- | --- |
| PyTeal contract source | Complete for local prototype | App-local contribution-credit accounting only |
| ABI generation | Complete for local prototype | ABI includes assignment, gifting, consumption, read methods, and receipt hash reads |
| Generated TEAL artifacts | Complete for local prototype | Generated from reviewed local source; not published in this dossier |
| Unit tests | Passing locally | `7 passed` in latest local test run |
| Multi-wallet simulation | Complete locally | Deterministic test addresses only; no recovery words or private keys generated |
| Receipt hashes | Implemented in prototype | Assignment and consumption calls require 32-byte receipt hashes |
| Transaction logs | Implemented in prototype | State-changing methods emit `PNET_CC:` logs |
| Safer terminology | Implemented in prototype | `earned` was replaced by `granted`; public copy uses `assigned credits` where possible |
| Self-gift prevention | Implemented in prototype | Self-gifting blocked |
| Partner self-assignment prevention | Implemented in prototype | Partner self-grants blocked |
| Explicit TestNet asset ID | Implemented in prototype deployment helper | Avoids defaulting TestNet records to MainNet PNET ASA |
| Public framing guide | Complete in prototype docs | Defines approved wording and prohibited claims |
| Measurement framework | Complete in prototype docs | Defines KPIs, dashboard method, reporting cadence, and iteration plan |

### Not Complete

| Area | Status | Required before public MainNet claim |
| --- | --- | --- |
| Public implementation repository | Pending | Publish source, ABI, tests, generated artifacts, and exact reviewed commit |
| TestNet deployment record | Pending | Record app ID, deployment tx, creator, app address, source commit, ABI, and review status |
| Action-code registry | Pending | Publish public meanings for assignment and consumption codes |
| Receipt evidence policy | Pending | Define what evidence is hashed, where it is retained, and how corrections work |
| Read-only dashboard | Pending | Build from public indexer data; no wallet connection required |
| Independent security review | Pending | Required before MainNet |
| Admin / upgrade policy | Pending | Decide immutable, multisig, timelock, or admin-upgrade model |
| Legal / public-claims review | Pending | Required before website launch or MainNet announcement |
| MainNet deployment | Not approved | Must remain blocked until review gates pass |

## Public Dossier Sections Ready To Commit

The following sections are safe for the public dossier because they do not include code, signer logic, private keys, wallet setup, or deployment instructions.

### Repository Scope Addition

```markdown
- Contribution protocol public disclosure plan: [docs/20_CONTRIBUTION_PROTOCOL_PUBLIC_DISCLOSURE_PLAN.md](docs/20_CONTRIBUTION_PROTOCOL_PUBLIC_DISCLOSURE_PLAN.md)
- Contribution protocol final package: [docs/21_CONTRIBUTION_PROTOCOL_FINAL_PACKAGE.md](docs/21_CONTRIBUTION_PROTOCOL_FINAL_PACKAGE.md)
```

### Current Gate Status Addition

```markdown
| Contribution protocol disclosure plan | READY FOR REVIEW | Public-safe website copy, security/verification wording, and contract-publication checklist are documented; no code is included. |
| Contribution protocol final package | READY FOR REVIEW | Executive summary, implementation status, risk register, next actions, and announcement draft are documented; no live contract is claimed. |
```

### Website Tokenomics Section

```markdown
## PNET Community Contribution Protocol

Status: Planned / TestNet prototype. Not MainNet. Not audited. Not live.

The PNET Community Contribution Protocol is designed as a non-custodial Algorand application for app-local contribution credits.

Users may be assigned or receive contribution credits for approved ecosystem participation. These credits are intended for access and reputation features inside PNET-related tools and community workflows.

Contribution credits are not PNET tokens. They are not deposits, not yield, not passive income, not profit share, not a promise of value, and not an investment return.

The protocol is designed to avoid custody of user PNET. It does not require users to deposit PNET into the application. It does not mint PNET, change PNET supply, or create a guaranteed claim on treasury assets.

Before any public MainNet deployment is described as live, the project should publish the source repository, reviewed source commit, generated ABI, deployment transaction, application ID, creator address, admin policy, security review status, known limitations, action-code registry, and receipt policy.
```

### Contract Publication Checklist

```markdown
No PNET utility, contribution, access, treasury, receipt, governance, lock, payment, or burn contract should be described as live until all required public evidence exists.

| Check | Required evidence | Status |
| --- | --- | --- |
| Source published | Public repository URL and exact reviewed commit | Pending |
| ABI documented | Machine-readable ABI and human-readable method table | Pending |
| Deployment tx recorded | Transaction ID and explorer/indexer link | Pending |
| App ID recorded | Network-specific application ID | Pending |
| Creator recorded | Creator address and role | Pending |
| Admin policy documented | Admin, multisig, timelock, pause, and update/delete policy | Pending |
| Action-code registry published | Public meaning of each assignment and consumption code | Pending |
| Receipt policy published | Evidence hash format, retention policy, and correction process | Pending |
| Tests published | Unit, simulation, and negative test summary | Pending |
| Security status published | Unaudited, reviewed, audited, deprecated, or blocked | Pending |
| Public claims reviewed | No deposit, yield, income, listing, or guaranteed-value claim | Pending |
```

## Risk Register

| Severity | Risk | Status | Mitigation |
| --- | --- | --- | --- |
| High | Unaudited smart contract | Open | Keep TestNet-only; audit before MainNet |
| High | Admin update/delete authority | Open | Decide immutable vs multisig/timelock before MainNet |
| High | Public misunderstanding as yield, income, or investment product | Mitigated, ongoing | Use approved framing guide; review every announcement |
| High | MainNet claims before public deployment evidence exists | Open | Do not announce live status until source, ABI, tx, app ID, and review records are published |
| Medium | Admin or partner discretion could inflate contribution credits | Partially mitigated | Publish partner policy, limits, action-code registry, and receipt hashes |
| Medium | Receipt hashes without durable evidence could be hard to verify | Open | Publish receipt evidence policy and correction process |
| Medium | Partner self-assignment could distort reputation metrics | Mitigated in prototype | Partner self-grants blocked; publish policy |
| Medium | Self-gifting could inflate activity metrics | Mitigated in prototype | Self-gifting blocked; report unique active contributors separately |
| Medium | Lost creator wallet / burn-accounting confusion | Open | Keep burn accounting separate; mark inaccessible-account claims `Needs verification` |
| Medium | Operational wallet role and balance uncertainty | Open | Verify role, balance, movement history, and control model from public sources |
| Medium | Dashboard or reports could become promotional | Open | Exclude price, TVL, market cap, yield, income, and listing metrics from protocol KPIs |
| Low | Local prototype source not yet published as a formal repo | Open | Publish implementation repository after review |
| Low | TestNet asset ID confusion | Mitigated in prototype | Deployment helper requires explicit TestNet asset ID |
| Low | Private data leakage in reports | Open | Use public links only; prohibit wallet screenshots, private notes, and recovery material |

## Recommended Next Actions

### Immediate

1. Create or designate a separate implementation repository for the TestNet prototype.
2. Publish the exact source, ABI, tests, and generated TEAL artifacts from a reviewed commit.
3. Add a public `ACTION_CODE_REGISTRY.md`.
4. Add a public `RECEIPT_POLICY.md`.
5. Prepare a TestNet deployment record template before deployment.
6. Keep this dossier docs-only; do not add contract code or signer scripts here.

### Before TestNet Announcement

1. Deploy only to TestNet with an explicit TestNet asset ID.
2. Record app ID, deployment tx, creator address, app address, source commit, ABI, and audit status.
3. Run the multi-wallet scenario: admin, partner, at least three users, assignment, gift, consumption, pause, and negative tests.
4. Publish the first weekly measurement report.
5. Confirm the announcement copy matches the approved framing guide.

### Audit Timing

| Timing | Audit action |
| --- | --- |
| Before public MainNet candidate | Internal source review, public claims review, and TestNet evidence package |
| Before MainNet deployment | Independent Algorand smart contract audit |
| Before any token-transfer, payment, burn, treasury, or lock feature | Separate security scope and legal/public-claims review |
| Before exchange/listing diligence use | Publish audit status, deployment record, source commit, and risk register |

### MainNet Gate

MainNet remains blocked until:

- source and ABI are public,
- TestNet deployment is source-linked,
- receipt and action-code policies are published,
- admin / update / pause policy is documented,
- measurement reports exist,
- public claims review is complete,
- independent security review is complete,
- no unresolved high-severity risk remains.

## Public Announcement Draft

```markdown
PNET Community Contribution Protocol update

We are preparing a TestNet prototype for app-local contribution credits.

The protocol is designed to support access and reputation features for approved ecosystem participation while keeping user PNET non-custodial.

Contribution credits are not PNET tokens, not deposits, not yield, not passive income, not profit share, not guaranteed value, and not an investment return.

Before anything is described as live, we will publish the source, ABI, deployment transaction, application ID, action-code registry, receipt policy, and review status.

Current status: TestNet prototype review. Not MainNet. Not audited. Not live.
```

## Verification-First Culture

The contribution protocol should be judged by whether it makes participation easier to verify, not by whether it creates promotional metrics. Every public statement should answer:

- What is the source?
- What is the date?
- What is the network?
- What is the app ID?
- What is verified?
- What still needs review?
- What claim is explicitly not being made?

Current Gate Status: FINAL PACKAGE READY FOR REVIEW; TESTNET PROTOTYPE NOT LIVE; MAINNET NOT APPROVED.
