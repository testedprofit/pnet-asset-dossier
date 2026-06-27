# Documentation, Transparency, And Website Update Pack

Status date: 2026-06-27

Scope: This file provides public-safe Markdown copy and update guidance for the PNET dossier and testedprofit website pages. It does not contain code, deployment scripts, wallet logic, signer logic, private custody notes, credentials, or `.env` files.

## Objective

Maintain PNET's transparency posture while preparing website and dossier updates for future utility, market-intelligence receipts, governance, and tokenomics hardening.

## Source Review

| Source | Review use | Status |
| --- | --- | --- |
| `https://testedprofit.com/pages/tokenomics/` | Existing tokenomics page, supply display, vault labels, tool references, and claim-risk review | Reviewed 2026-06-27 |
| `https://testedprofit.com/pages/PNET/` | Existing PNET page, Web2/Web3 positioning, partner references, and claim-risk review | Reviewed 2026-06-27 |
| `ROADMAP.md` | Roadmap Sections 1-4 | Local source of truth |
| `docs/15_PHASE_1_CORE_TOKEN_UTILITY_SPEC.md` | Phase 1 utility requirements | Local source of truth |
| `docs/16_PHASE_2_MARKET_INTELLIGENCE_GOVERNANCE_SPEC.md` | Phase 2 intelligence and governance requirements | Local source of truth |
| `docs/17_PHASE_3_REVENUE_TOKENOMICS_HARDENING_SPEC.md` | Phase 3 treasury and tokenomics hardening requirements | Local source of truth |

## Dossier Updates

| Area | Update | Status |
| --- | --- | --- |
| Roadmap | Add Section 5 for documentation, transparency, and website updates | Ready for review |
| Tokenomics | Keep direct burn, inaccessible-account, locked-supply, and circulating-supply categories separate | Ready for review |
| Operational wallet | Publish address only with `User-provided / Needs verification` status | Ready for review |
| Contracts | Do not list contracts as live until app IDs, source commits, audits, and deployment records exist | Required |
| Snapshots | Preserve dated source-linked snapshots and stale-data warnings | Required |
| Website copy | Use neutral copy below; avoid earning, income, return, and listing language | Ready for review |

## Website Section: PNET Utility Roadmap

Suggested page: tokenomics page or dedicated PNET utility page.

```markdown
## PNET Utility Roadmap

PNET utility is being documented in phases. Each phase remains subject to TestNet validation, security review, public claims review, and source-linked deployment records before it is described as live.

| Phase | Focus | Current status |
| --- | --- | --- |
| Phase 1 | Voluntary lock/access-tier design, optional tool payments, and treasury attribution | Specification ready; implementation pending |
| Phase 2 | Market-intelligence receipts, source-linked snapshots, on-chain hash anchoring, and advisory governance | Specification ready; implementation pending |
| Phase 3 | Treasury accounting, revenue feedback policy research, operational-wallet hardening, and tokenomics methodology | Specification ready; distribution mechanisms not approved |

No phase should be described as deployed until contract IDs, source commits, deployment records, security notes, and public review notes are published.
```

## Website Section: Current Operational Wallet

Suggested page: tokenomics page, transparency page, or treasury page.

```markdown
## Current Operational Wallet

User-provided operational wallet:

`CIVTUU6KLTYO26SPVEBDFBKP3UMZM2DPEO5RINODUVCI5NVIFC6HVNWS7E`

Status: Needs verification.

This address is disclosed for transparency review. Its role, current balance, movement history, and project-control status should be verified from public indexers before being used in tokenomics, treasury, or listing-readiness claims.

Future updates should include:

- capture date,
- source links,
- observed balance,
- role label,
- movement notes for large transfers,
- reviewer handle or role,
- correction process.
```

## Website Section: Lost Creator Account And Burn Accounting

Use the pre-verification version until the burn documentation gate in [docs/17_PHASE_3_REVENUE_TOKENOMICS_HARDENING_SPEC.md](17_PHASE_3_REVENUE_TOKENOMICS_HARDENING_SPEC.md) is complete.

### Pre-Verification Copy

```markdown
## Burn Accounting Review

The project is reviewing a user-provided claim that the original creator account is no longer accessible and that some transfers or opt-out paths involving that account may affect effective circulating supply.

Status: Needs on-chain and disclosure review.

PNET tokenomics should distinguish:

- direct burned supply supported by explorer or indexer evidence,
- reviewed locked supply supported by lock or escrow evidence,
- inaccessible-account claims that require human and on-chain review,
- circulating supply calculated from a published methodology.

Do not send tokens to any address unless you understand the result. Burn and inaccessible-account accounting will be documented only from public evidence and dated reviewer notes.
```

### Post-Verification Copy

```markdown
## Burn Accounting Methodology

PNET supply accounting separates direct burned supply, reviewed locked supply, and verified inaccessible-account supply.

Direct burned supply is counted only when public explorer or indexer evidence supports the amount. Inaccessible-account supply is counted separately and only after a published methodology, public evidence, and reviewer sign-off are available.

Capture date:

Source links:

Reviewer:

Methodology version:
```

## Website Section: Contracts And Deployment Records

Use this section only after implementation work exists in a separate code repository.

```markdown
## Contracts And Deployment Records

No PNET utility, governance, receipt, or treasury-routing contract should be treated as live unless this table is complete.

| Component | Network | App / contract ID | Source commit | Audit / review status | Deployment date | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| Phase 1 utility | TestNet | Pending | Pending | Pending | Pending | Not live |
| Phase 2 receipts | TestNet | Pending | Pending | Pending | Pending | Not live |
| Phase 2 governance | TestNet | Pending | Pending | Pending | Pending | Advisory only until reviewed |
| Phase 3 treasury accounting | TestNet | Pending | Pending | Pending | Pending | Distribution mechanisms not approved |
```

## Code Publication Checklist

Future code should not be published through this dossier. It should use a separate implementation repository with:

| Requirement | Status |
| --- | --- |
| Clear README | Required |
| Source comments explaining security-sensitive paths | Required |
| Unit tests | Required |
| TestNet deployment records | Required |
| ABI files, if applicable | Required |
| No committed credentials or signer material | Required |
| Public security notes | Required |
| Audit or review status | Required |
| Dossier link back to deployment record | Required after review |

## Website Claim Guardrails

The current public pages include Web2 partner and earning-oriented language. That content should not be used as PNET token utility language. PNET pages should avoid:

| Avoid | Use instead |
| --- | --- |
| Outcome or income framing | Source-linked utility and verification status |
| Exchange or listing implication | Public links and `Not confirmed` status |
| Tool availability without evidence | `Live`, `TestNet`, `Planned`, or `Needs verification` |
| Burn claims without methodology | Direct burn, locked, inaccessible, and circulating categories |
| Contract claims without app IDs | Deployment-record table |

Current Gate Status: WEBSITE UPDATE PACK READY FOR REVIEW; WEBSITE NOT UPDATED BY THIS REPOSITORY.
