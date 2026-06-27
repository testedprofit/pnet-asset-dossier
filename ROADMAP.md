# PNET Roadmap Preparation

Status date: 2026-06-27

Scope: This is a docs-only preparation document for future PNET implementation work. It is not code, not a deployment guide, not a wallet setup guide, and not an investment document.

## Section 1: Roadmap Overview and Preparation

### Objective

Align the ProfitNet / PNET review process before any coding begins. The first phase is to document current state, identify facts that need verification, define security boundaries, and prepare a separate TestNet implementation path that does not place wallet material or executable code in this dossier.

## Source Review Set

| Source | Review purpose | Status |
| --- | --- | --- |
| GitHub dossier | Existing whitepaper, security notes, verification records, public claims policy, and backlog | Reviewed locally |
| `WHITEPAPER.md` | Market-intelligence protocol vision and trust model | Reviewed locally |
| `https://testedprofit.com` | Current public website positioning and AlgoFlow/TestNet references | Recheck before implementation |
| `https://testedprofit.com/pages/tokenomics/` | Public tokenomics-page claims, vault labels, and risk wording | Recheck before implementation |
| `https://testedprofit.com/pages/PNET/` | Public PNET page and Web2/Web3 positioning | Recheck before implementation |
| 2026-06-27 standalone data snapshot PDF | User-provided wallet and supply-context notes | Privacy-reviewed; raw PDF not committed |

## Current State Context

| Item | Current handling |
| --- | --- |
| Asset | ProfitNet / PNET, Algorand ASA `3169177585` |
| Supply | `100,000,000` PNET with `6` decimals; source claims remain subject to independent verification |
| Control addresses | Prior dossier records indicate manager, reserve, freeze, and clawback controls are zeroed; continue verifying from indexers before relying on this in public diligence |
| Original creator account status | User-provided claim: creator account access is unavailable. Any claim that opted-out tokens sent there are permanently irrecoverable must be independently reviewed before being treated as a burn-method fact |
| Operational wallet | User-provided disclosure: `CIVTUU6KLTYO26SPVEBDFBKP3UMZM2DPEO5RINODUVCI5NVIFC6HVNWS7E`. Role, current balance, movement history, and project-control status require on-chain and human verification |
| Product state | Public website references AlgoFlow tools and TestNet activity. Each tool must be labeled `Live`, `TestNet`, `Planned`, `Deprecated`, or `Needs verification` before being used in roadmap claims |
| Public claims risk | Website pages include earning-oriented language. Dossier and roadmap language should remain neutral, dated, source-linked, and non-promissory |

## Preparation Tasks

| Priority | Task | Gate |
| --- | --- | --- |
| P0 | Reconfirm current repo scope before implementation | `pnet-asset-dossier` remains documentation and media only |
| P0 | Verify operational wallet role and balance | Needs on-chain review and explicit maintainer sign-off |
| P0 | Verify lost-creator burn-path claim | Needs chain analysis and disclosure review |
| P0 | Define separate implementation location | Future code should use a separate TestNet repo or implementation branch outside this docs-only dossier |
| P0 | Prepare TestNet-only wallet procedure | No recovery words, private keys, `.env` files, or signer configs may be committed |
| P1 | Create product status matrix | Track AlgoFlow, ProfitLock, Token Launchpad, MultiSend, Wallet Inspector, AlgoSocial, Crowdfund, AlgoPool, and PNET Genesis |
| P1 | Write implementation-readiness checklist | Separate planning, contracts, tests, audits, deploy records, and public docs |
| P1 | Define review cadence | Every implementation milestone should produce a dated, source-linked verification note |

## Dedicated Work Area

This repository should use `ROADMAP.md` as the public planning index. It should not receive smart contracts, deployment scripts, wallet setup files, transaction submission logic, or environment files.

Future implementation work should happen in one of the following:

| Option | Use when | Requirement |
| --- | --- | --- |
| Separate implementation repository | Building contracts, apps, dashboards, indexers, or APIs | Must include its own security policy, tests, and secret-handling rules |
| Dedicated implementation branch outside this docs-only scope | Preparing reviewed code before a separate release | Must not merge executable code into this dossier |
| Private TestNet workspace | Creating or funding wallets, running deploys, or testing signers | Must never be committed or mirrored into this public dossier |

## TestNet Setup Confirmation

| Check | Status | Notes |
| --- | --- | --- |
| Docs-only dossier remains clean | PASS | No code, deployment scripts, wallet files, or signer logic added |
| TestNet wallet material in repo | PASS | None added |
| `.env` or credential files in repo | PASS | None added |
| Basic TestNet implementation environment | PENDING | Should be created outside this repository |
| Basic testing wallet | PENDING | Create only in a wallet/tooling environment that keeps recovery material outside Git |
| Funding and deployment plan | PENDING | Must be documented without private keys or transaction-signing material |

## Section 2: Phase 1 - Core Token Utility

Detailed specification: [docs/15_PHASE_1_CORE_TOKEN_UTILITY_SPEC.md](docs/15_PHASE_1_CORE_TOKEN_UTILITY_SPEC.md)

### Objective

Give PNET a TestNet-first utility path through voluntary token locking, access tiers, optional tool payments, and transparent revenue attribution. This section is a specification only. It does not add code, signer logic, deployment scripts, frontend stubs, or CLI tooling to this docs-only repository.

### Phase 1 Components

| Component | Purpose | Current status |
| --- | --- | --- |
| Staking / proof-of-contribution | Test voluntary lock/accounting mechanics and tiered access flags | Spec ready; implementation pending outside this repo |
| PNET payments in AlgoFlow tools | Test optional tool fees routed to a documented treasury | Spec ready; implementation pending outside this repo |
| Revenue attribution view | Test dated, source-linked treasury and tool-fee reporting | Spec ready; implementation pending outside this repo |
| Burn mechanism documentation | Document lost-creator burn-path claims only after verification | Needs on-chain and disclosure review |

### Phase 1 Gate

Phase 1 cannot be described as live until a separate implementation repository or private TestNet workspace has reviewed code, tests, deployment records, security notes, and public claims review.

## Section 3: Phase 2 - Market Intelligence Layer And Governance

Detailed specification: [docs/16_PHASE_2_MARKET_INTELLIGENCE_GOVERNANCE_SPEC.md](docs/16_PHASE_2_MARKET_INTELLIGENCE_GOVERNANCE_SPEC.md)

### Objective

Start delivering the whitepaper vision through dated intelligence receipts, public queryability, and lightweight governance. This section is a specification only. It does not add snapshot scripts, storage contracts, voting contracts, deployment scripts, frontend stubs, or CLI tooling to this docs-only repository.

### Phase 2 Components

| Component | Purpose | Current status |
| --- | --- | --- |
| Intelligence receipts / snapshots | Record dated, source-linked asset facts, holder metrics, liquidity metrics, and claim status | Spec ready; implementation pending outside this repo |
| Off-chain snapshots plus on-chain hashes | Preserve full receipt content off-chain while anchoring exact content hashes on-chain | Recommended first pattern |
| Public query model | Support latest receipt, receipt by hash, historical timeline, and open verification claims | Spec ready; implementation pending outside this repo |
| Lightweight governance | Test advisory signaling for tool priorities, receipt schema, source policy, and treasury research | Spec ready; binding governance not approved |

### Phase 2 Gate

Phase 2 cannot be described as live until a separate implementation repository or private TestNet workspace has reviewed receipt schemas, hash anchoring, query examples, proposal records, voting-weight rules, security notes, and public claims review.

## Section 4: Phase 3 - Revenue Feedback And Tokenomics Hardening

Detailed specification: [docs/17_PHASE_3_REVENUE_TOKENOMICS_HARDENING_SPEC.md](docs/17_PHASE_3_REVENUE_TOKENOMICS_HARDENING_SPEC.md)

### Objective

Close the loop with auditable treasury accounting, reviewed allocation policy, operational-wallet hardening, and clearer tokenomics methodology. This section is a specification only. It does not add revenue-routing code, multisig setup, buyback logic, burn logic, deployment scripts, frontend stubs, or CLI tooling to this docs-only repository.

### Phase 3 Components

| Component | Purpose | Current status |
| --- | --- | --- |
| Treasury accounting | Record source-linked inflows, outflows, routes, and policy versions | Spec ready; implementation pending outside this repo |
| Revenue feedback policy | Define conservative allocation templates before any live mechanism | Spec ready; direct staker flow not approved |
| Operational wallet hardening | Verify role, balance, controls, movement history, and possible lock strategy | Needs on-chain, human, and security review |
| Lost-wallet burn accounting | Separate direct burn figures from inaccessible-account methodology | Needs methodology approval |

### Phase 3 Gate

Phase 3 cannot be described as live until treasury accounting, legal review, governance review, security review, public-proof workflows, operational-wallet verification, and burn accounting methodology are complete.

## Section 5: Documentation, Transparency, And Website Updates

Detailed update pack: [docs/18_DOCUMENTATION_TRANSPARENCY_WEBSITE_UPDATES.md](docs/18_DOCUMENTATION_TRANSPARENCY_WEBSITE_UPDATES.md)

### Objective

Maintain and strengthen PNET's transparency posture through clear dossier updates, website copy, contract/deployment disclosure templates, utility-roadmap language, operational-wallet disclosure guidance, and burn-accounting methodology.

### Section 5 Components

| Component | Purpose | Current status |
| --- | --- | --- |
| Dossier update checklist | Track roadmap, tokenomics, wallet, contract, and snapshot documentation work | Ready for review |
| Website utility roadmap copy | Provide restrained language for Phase 1, Phase 2, and Phase 3 status | Ready for review |
| Operational wallet website copy | Disclose address only as user-provided and `Needs verification` | Ready for review |
| Lost creator account copy | Provide pre-verification and post-verification wording | Ready for review |
| Contract deployment table | Prevent claims of live contracts without app IDs, source commits, and review status | Ready for review |

### Section 5 Gate

Website updates should not describe utility, governance, revenue routing, burn accounting, or contracts as live until the related evidence, review status, and source-linked deployment records exist.

## Section 6: Testing, Security, Deployment, And Measurement

Detailed specification: [docs/19_TESTING_SECURITY_DEPLOYMENT_MEASUREMENT.md](docs/19_TESTING_SECURITY_DEPLOYMENT_MEASUREMENT.md)

### Objective

Ensure future implementation work is tested, reviewed, deployed, and measured before any public claim that utility, governance, receipt anchoring, or treasury-routing systems are live.

### Section 6 Components

| Component | Purpose | Current status |
| --- | --- | --- |
| TestNet testing plan | Define contract, payment, receipt, governance, and wallet-monitoring tests | Ready for review |
| Security checklist | Identify audit-sensitive custody, accounting, admin, treasury, and privacy areas | Ready for review |
| Deployment readiness plan | Separate TestNet gates from MainNet migration gates | Ready for review |
| KPI dashboard outline | Track utility, treasury attribution, governance, receipt cadence, and verification progress | Ready for review |

### Section 6 Gate

Deployment scripts, TestNet scripts, MainNet migration actions, and signer material must remain outside this docs-only repository. This dossier may record reviewed deployment summaries and KPI snapshots after sensitive material is excluded.

## Codex Planning Prompt

Use this prompt for planning only. Do not use it to add code to this dossier.

```text
You are an expert Algorand developer. Review the ProfitNet (PNET) ASA 3169177585 context: fixed 100M supply, 6 decimals, reported renounced controls, user-reported unavailable creator-account access that may affect burn accounting, and user-provided operational wallet CIVTUU6KLTYO26SPVEBDFBKP3UMZM2DPEO5RINODUVCI5NVIFC6HVNWS7E. Treat the operational-wallet role, balance, and project-control status as Needs verification. The whitepaper vision is a market-intelligence protocol. Create a high-level implementation plan for future roadmap sections. Prioritize security, transparency, Algorand-native patterns, TestNet-first validation, and clear separation between this docs-only dossier and any implementation repository.
```

## Exit Criteria For Section 1

Section 1 is complete when:

- the current dossier links to this roadmap,
- operational wallet context is disclosed only as user-provided and unverified,
- no wallet secrets or implementation code are present,
- TestNet setup is confirmed as external to this repository,
- future implementation work has a separate location and security policy,
- all claims remain dated, source-linked, and reviewable.

Current Gate Status: SECTION 1 READY FOR REVIEW; PHASE 1 SPEC READY FOR REVIEW; PHASE 2 SPEC READY FOR REVIEW; PHASE 3 SPEC READY FOR REVIEW; SECTION 5 WEBSITE UPDATE PACK READY FOR REVIEW; SECTION 6 TESTING/SECURITY SPEC READY FOR REVIEW; TESTNET IMPLEMENTATION PENDING OUTSIDE THIS REPOSITORY.
