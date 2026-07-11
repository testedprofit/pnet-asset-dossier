# PNET Website Copy Templates

Status date: 2026-06-27

These templates are public-safe copy for the testedprofit website. They should be reviewed before publication and updated when evidence changes.

## Tokenomics Page Section

```markdown
## PNET Tokenomics and Verification Status

PNET is the unit for the ProfitNet Algorand Standard Asset, ASA ID 3169177585.

Current public records in the PNET dossier track total supply, decimals, asset controls, public source links, tokenomics-page claims, holder concentration, market snapshots, and verification gaps.

Supply and allocation claims are handled as dated records. A claim is not treated as verified unless it has public evidence, capture date, methodology, and review status.

Known verification categories:

- Total supply and decimals: recorded from public indexer review; recheck before external use.
- Burned supply: Needs on-chain verification.
- Lost creator wallet / inaccessible-account supply: Needs on-chain and methodology verification.
- Founder allocation: Needs lock verification.
- Strategic reserve: Needs lock verification.
- LP, vault, and pool labels: Need on-chain verification.
- Operational wallet role and balance: Needs verification.

PNET documentation does not claim guaranteed returns, passive income, investment return, exchange listing, or bridge support.

Verification dossier:
https://github.com/testedprofit/pnet-asset-dossier
```

## Multichain Status Section

```markdown
## PNET Network Status

ProfitNet / PNET is becoming a multichain project: rooted on Algorand, expanded to Base, and preparing a supply-backed Robinhood Chain path through Chainlink CCIP/CCT.

| Network | Status |
| --- | --- |
| Algorand | Legacy/root PNET ASA `3169177585`; holder migration support is planned but not live |
| Base | Verified ERC-20 PNET at `0xe1F7F585f458cB6AFFCEE2286b8482523B19ee5a` |
| Robinhood Chain | Planned supply-backed representation through Chainlink CCIP/CCT; not deployed |

Base PNET is source verified and fixed supply. The verified Base contract has no owner/admin mint, pause, blacklist, transfer tax, transfer override, or proxy.

Robinhood Chain support is not live yet and does not imply a Robinhood app or brokerage listing.
```

## Algorand to Base Migration Section

```markdown
## Algorand <> Base Migration Status

ProfitNet is evaluating a capped migration reserve so existing Algorand PNET holders can swap into Base PNET and Base holders can swap back into Algorand PNET. The first proposed cap is 5,000,000 PNET.

This migration path is not live yet. The project will publish reserve addresses, terms, limits, proof links, and support instructions before accepting any migration transfers.

Do not send PNET to any migration address until an official migration page and proof record are published.
```

## Utility Page Section

```markdown
## PNET Utility Roadmap

PNET is being documented as a public market-intelligence coordination asset for Algorand.

The roadmap focuses on verification-first utility:

1. Public asset dossier
   Dated records for asset facts, tokenomics claims, market snapshots, public links, and review gaps.

2. Market-intelligence receipts
   Planned source-linked snapshots with content hashes and public verification steps.

3. Community contribution credits
   Planned non-custodial app-local credits for access and reputation workflows.

4. Developer and ecosystem review tools
   Planned read-only guides, APIs, and dashboards for source-linked asset review.

Contribution credits are not PNET tokens, not deposits, not yield, not passive income, not profit share, not guaranteed value, and not investment returns.

Current protocol status: TestNet starter only. Not MainNet. Not audited. Not live.
```

## Contribution Protocol Section

```markdown
## PNET Community Contribution Protocol

Status: TestNet starter only. Not MainNet. Not audited. Not live.

The PNET Community Contribution Protocol is designed as a non-custodial Algorand application for app-local contribution credits.

Users may be assigned or receive contribution credits for approved ecosystem participation. These credits are intended for access and reputation features inside PNET-related tools and community workflows.

Contribution credits are not PNET tokens. They are not deposits, not yield, not passive income, not profit share, not dividends, not a promise of value, and not an investment return.

The protocol is designed to avoid custody of user PNET. It does not require users to deposit PNET into the application. It does not mint PNET, change PNET supply, or create a guaranteed claim on treasury assets.

Before any MainNet deployment is described as live, the project should publish:

- source repository,
- reviewed source commit,
- generated ABI,
- deployment transaction,
- application ID,
- creator address,
- admin and partner policy,
- update/delete policy,
- security review status,
- known limitations,
- action-code registry,
- receipt policy.
```

## Contribution Credit System Tokenomics Addition

```markdown
## Real-World Participation and Access Credits

ProfitNet is developing a TestNet-first Contribution Credit System for verified non-custodial participation.

Initial draft categories include:

- Kryptex-style compute participation
- Honeygain / JumpTask-style bandwidth-sharing evidence

How it works:

1. Users opt into the Community Contribution Protocol.
2. Users submit redacted activity evidence for review.
3. Evidence files and account references are hashed for privacy.
4. After verification, app-local access/reputation credits may be recorded for the user.
5. Credits may support ecosystem access and reputation workflows and may be gifted between opted-in users.

Important:

Contribution credits represent access and reputation only. They do not constitute an investment, staking position, deposit, yield product, passive-income product, or promise of financial return. External participation can involve real costs, including electricity, hardware, and internet usage, and is entirely voluntary.

Full documentation:
https://github.com/testedprofit/pnet-asset-dossier/tree/main/docs/pnet-contribution-protocol
```

## Operational Wallet Section

```markdown
## Current Operational Wallet Disclosure

The following address has been disclosed by the project as a current operational wallet:

CIVTUU6KLTYO26SPVEBDFBKP3UMZM2DPEO5RINODUVCI5NVIFC6HVNWS7E

Public status: Needs verification.

Before this wallet is used in tokenomics, treasury, lock, contract-admin, or listing-readiness claims, the project should publish a dated public review of role, balance, movement history, control model, and relationship to any deployed application.

No recovery words, private custody notes, personal device details, or wallet screenshots should be published.
```

## Lost Creator Account Section

```markdown
## Lost Creator Account / Burn-Accounting Review

The project has disclosed that access to the original creator account may be unavailable.

This may affect supply methodology if tokens are demonstrably inaccessible. The dossier separates direct burned supply, inaccessible-account supply, locked supply, and circulating supply.

Until public on-chain evidence and methodology are recorded, the lost creator account should be treated as Needs verification and should not be described as verified burned supply.
```

Current Gate Status: WEBSITE COPY READY FOR REVIEW; PUBLICATION REQUIRES MAINTAINER AND CLAIMS REVIEW.
