# Algorand Asset Launch and Verification Protocol

Status date: 2026-06-27

This is a public-safe operating checklist for Algorand Standard Asset launch and verification review. It was derived from a maintainer-provided SOP document after privacy and repository-scope review.

This file is not a live wallet guide, transaction guide, exchange guide, custody guide, legal opinion, listing application, or investment document. It should be used as a review framework for public evidence, not as instructions to transfer funds, sign transactions, or disclose private material.

For PNET specifically, this document does not instruct anyone to recreate the asset. PNET already has ASA ID `3169177585`; all PNET-specific facts should be verified against the existing asset record and the current dossier.

## Public-Safety Rules

Do not commit or publish:

- seed phrases, recovery phrases, private keys, passwords, wallet backup files, or signing material,
- screenshots showing wallet balances, wallet seed flows, identity documents, verification selfies, admin panels, cookies, or session data,
- personal email addresses, personal phone numbers, home addresses, government IDs, or private identity-verification records,
- API keys, bearer tokens, `.env` files, DNS account credentials, registrar credentials, or hosting credentials,
- live transaction instructions, deposit instructions, exchange funding steps, or private operational runbooks.

Use project-owned role accounts and project-owned domains for public verification workflows. Avoid personal inboxes in public documentation.

## Gate 1: Asset Purpose and Public Scope

Before any launch or verification workflow, record the asset's public purpose.

| Check | Required output |
| --- | --- |
| Asset purpose | Neutral description of what the asset represents |
| Non-purpose | Explicitly exclude return promises, passive-income framing, managed strategies, copy trading, user deposits, and guaranteed listings |
| Public source of truth | Official site, repository, or public dossier |
| Review owner | Human reviewer or maintainer role, not a private identity record |
| Status | `Draft`, `Needs verification`, `Verified`, or `Rejected` |

## Gate 2: Domain and Brand Readiness

Verification workflows usually require a project-controlled web presence. Record only public, non-sensitive evidence.

| Item | Public-safe evidence |
| --- | --- |
| Project website | Public URL |
| Domain ownership check | Public DNS record result or verification status, not registrar credentials |
| Project role email | Role-account description such as `admin [at] project-domain.example` |
| Brand assets | Public logo file, brand name, and asset icon |
| Public repository | GitHub or equivalent public documentation repository |

Do not publish personal inboxes, registrar screenshots, billing records, or DNS account screenshots.

## Gate 3: Custody and Authority Review

An asset launch or verification workflow should define authority before any irreversible action.

| Question | Why it matters | Public status field |
| --- | --- | --- |
| Who controls the creator account? | Creator authority can affect trust analysis | Role label only |
| Are manager, reserve, freeze, and clawback fields set? | These fields define administrative risk | Public address or zero address |
| Can any address freeze or claw back user balances? | Freeze/clawback authority changes risk posture | `Present`, `Cleared`, or `Needs verification` |
| Is the control policy documented? | Reviewers need intent plus evidence | Link to public policy |
| Is there a recovery plan? | Operational continuity matters | Summary only; no recovery material |

Public docs may describe a custody policy. They must not include recovery phrases, private keys, passphrases, device screenshots, password-manager exports, or emergency access instructions.

## Gate 4: Asset Parameter Worksheet

Asset parameters should be recorded before creation and verified after creation.

| Field | Review requirement |
| --- | --- |
| Asset name | Must match public brand or documented asset identity |
| Unit name | Short ticker or unit label |
| Total supply | Confirm intended display supply |
| Decimals | Confirm precision and raw-unit derivation |
| Asset URL | Must point to a project-controlled public URL |
| Metadata hash | Record if present |
| Creator | Public address after creation |
| Manager | Public address or zero address |
| Reserve | Public address or zero address |
| Freeze | Public address or zero address |
| Clawback | Public address or zero address |
| Default frozen | Public chain value |

For PNET, the current dossier records the existing ASA ID as `3169177585` and should be used instead of a new-asset workflow.

## Gate 5: Control-Field Policy

Control fields must be handled as a public risk surface.

| Control field | Public-review question | Public-safe recommendation |
| --- | --- | --- |
| Manager | Can asset configuration be changed later? | If cleared, record source evidence. If present, explain why. |
| Reserve | Is supply representation affected? | Record address and methodology if used. |
| Freeze | Can accounts be frozen? | Avoid unless legally or operationally required; disclose if present. |
| Clawback | Can balances be forcibly transferred? | Avoid unless legally or operationally required; disclose if present. |
| Default frozen | Are new holders frozen by default? | Record exact chain value. |

Do not describe any private process for controlling, rotating, or recovering these authorities in this public repository.

## Gate 6: Verification Package

Prepare public verification evidence without exposing private operational data.

| Evidence | Public-safe form |
| --- | --- |
| ASA ID | Numeric ASA identifier |
| Asset metadata | Explorer or indexer link |
| Official website | Public URL |
| Logo/icon | Public image file or media folder reference |
| DNS verification | Result, timestamp, and source only |
| Role email check | Role-account status only, not inbox screenshots |
| Identity checks | State that provider review may be required; do not publish documents or screenshots |
| Review date | UTC or local date plus timezone |
| Reviewer | Role or maintainer handle, not private identity data |

## Gate 7: Post-Launch Evidence Record

After launch or verification, record only public evidence.

| Evidence | Required details |
| --- | --- |
| Asset record | Source URL, capture date, observed values |
| Control fields | Manager, reserve, freeze, clawback, default frozen |
| Supply | Raw total, decimals, display total |
| Liquidity references | Pool IDs, venue, counter-asset, capture date |
| Tokenomics claims | Source page, claim text summarized neutrally, status label |
| Wallet labels | Label source and `Needs verification` status unless independently confirmed |
| Market data | Treat as stale snapshot immediately after capture |

## Gate 8: Public Claims Review

Before publishing a launch or verification page, remove or downgrade unsafe claims.

| Claim type | Public-safe handling |
| --- | --- |
| Guaranteed profit or guaranteed return | Do not include |
| Passive-income framing | Do not include |
| Managed strategy or copy-trading framing | Do not include |
| User-deposit framing | Do not include |
| Exchange/listing confirmation | Include only with direct source evidence from the named venue |
| Bridge support | Mark as future research unless verified from direct bridge documentation |
| Burns, locks, vaults, reserves | Mark `Needs on-chain verification` until source evidence is recorded |

## Human Review Checklist

- Confirm the asset URL is project-controlled.
- Confirm ASA metadata through at least one public explorer or indexer.
- Confirm manager, reserve, freeze, clawback, and default-frozen fields.
- Confirm raw total, decimals, and display supply.
- Confirm no private wallet, recovery, identity, registrar, hosting, or inbox material is committed.
- Confirm no screenshots contain sensitive browser tabs, balances, admin panels, or wallet details.
- Confirm public claims use `Verified`, `Snapshot only`, `Needs verification`, or `Needs on-chain verification`.
- Confirm market data includes source and capture date.
- Confirm no exchange, bridge, yield, return, or listing support is implied without direct evidence.

## Repository Placement

Public SOP content should be committed as Markdown where possible. Raw DOCX files should not be committed unless they have been privacy-scrubbed, rendered for QA, and reviewed for hidden comments, tracked changes, metadata, embedded objects, and personal data.
