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

Current Gate Status: SECTION 1 READY FOR REVIEW; TESTNET IMPLEMENTATION PENDING OUTSIDE THIS REPOSITORY.
