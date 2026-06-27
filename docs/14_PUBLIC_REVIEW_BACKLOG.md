# Public Review Backlog

Status date: 2026-06-27

This backlog records safe, non-promotional improvements identified during public dossier review. It is not a roadmap promise, investment document, listing document, or product launch commitment.

Items in this file should be treated as review tasks until completed with public evidence.

## Highest-Priority Verification Tasks

| Priority | Task | Why it matters | Status |
| --- | --- | --- | --- |
| P0 | Publish exact burn wallets and burn transaction set | Burned-supply claims differ across public sources | Needs verification |
| P0 | Publish founder allocation address and lock mechanism | The 25M PNET lock claim needs source evidence | Needs on-chain verification |
| P0 | Publish strategic reserve address and lock mechanism | The 15M PNET reserve claim needs source evidence | Needs on-chain verification |
| P0 | Explain Sept 2026 unlock mechanics | Unlock timing should not rely on page text alone | Needs on-chain verification |
| P0 | Reconcile website, Vestige, and explorer supply/burn/circulation fields | Public diligence requires one documented methodology | Needs methodology review |
| P0 | Confirm LP/vault labels with pool IDs, balances, and account evidence | Pool labels are not proof of lock or burn state | Needs on-chain verification |
| P0 | Verify ASA creation date and creation round from explorer/indexer sources | A review PDF cited `August 12, 2025` and round `52678300`; these should not be treated as facts until independently confirmed | Needs verification |
| P0 | Verify Pera asset verification status and meaning | Explorer badges can change and may not mean broad project endorsement | Needs verification |
| P0 | Verify claimed lost-creator burn path | A later snapshot claims opted-out tokens sent to the original creator account are permanently irrecoverable; this needs on-chain, wallet-control, and disclosure review before publication | Needs on-chain and disclosure review |
| P0 | Review operational wallet label disclosure | The operational wallet address is now published in `ROADMAP.md` as user-provided; balance, role, and project-control status still require independent verification | Needs security review |

## Documentation and Transparency Tasks

| Priority | Task | Public-safe implementation |
| --- | --- | --- |
| P1 | Add a recurring update cadence | Monthly dated review notes or changelog entries |
| P1 | Add a public maintainer/transparency page | Role-based maintainers or project handles; no private identity records |
| P1 | Add official channel list | Public website, GitHub, explorer, market pages, and social links with `Needs verification` status where needed |
| P1 | Add correction/dispute process | GitHub issue template or public review process |
| P1 | Add reviewer-signed verification records | Human review notes for control fields, locks, burns, liquidity, and market snapshots |
| P1 | Add tokenomics methodology definitions | Define total supply, circulating supply, burned supply, locked supply, vault balance, liquidity balance, and excluded balances |
| P1 | Add public utility roadmap status labels | Use `Live`, `TestNet`, `Planned`, `Deprecated`, or `Needs verification`; do not imply release commitments |
| P1 | Add revenue attribution transparency template | Track public revenue categories and treasury support only; do not describe holder payouts without legal, governance, and security review |
| P1 | Add wallet-movement monitoring methodology | If any project-controlled address is publicly labeled, publish dated balance deltas, source links, and correction notes without exposing private operational notes |
| P1 | Define intelligence receipt schema | Include source links, capture dates, review status, content hash, and correction history |
| P1 | Define canonical hash method for receipts | Make off-chain snapshots reproducible before on-chain anchoring |
| P1 | Define treasury accounting template | Include source category, amount, asset, date, route, transaction reference, policy version, reviewer, and correction path |
| P1 | Add revenue feedback policy review | Treat allocation splits as research until legal, governance, security, and public-claims review are complete |
| P1 | Review website utility roadmap copy | Ensure Phase 1-3 statuses remain `Spec ready`, `Pending`, or `Not approved` until evidence exists |
| P1 | Review website operational-wallet copy | Confirm address disclosure, role label, balance source, movement notes, and correction process |
| P1 | Create TestNet testing matrix | Cover voluntary locks, tool payments, treasury attribution, receipt hashes, governance, and wallet monitoring |
| P1 | Create KPI dashboard source map | Define source, capture date, stale-data policy, and approval status for each KPI |

## Product and Ecosystem Tasks

Future tools such as AlgoFlow, AlgoPulse, ProfitLock, launchpad tools, MultiSend, wallet inspection, or registry services should not be described as live until public source evidence exists.

| Priority | Task | Safety condition |
| --- | --- | --- |
| P1 | Separate live product claims from future-product targets | Every feature should be marked `Live`, `TestNet`, `Planned`, or `Needs verification` |
| P1 | Publish public API/schema docs only after implementation | Docs should remain read-only and should not include signing, wallet, or transaction logic |
| P1 | Add product status table | Include product name, network, status, source link, and security-review status |
| P1 | Create AlgoFlow tool status matrix | Review Crowdfund, Token Launchpad, PNET Genesis, MultiSend, Wallet Inspector, AlgoSocial, ProfitLock, and AlgoPool with source-backed status labels |
| P1 | Evaluate contribution/access-tier design | Any lock or access mechanism should be utility-based, non-yield-framed, and reviewed for security/listing risk before publication |
| P1 | Create separate Phase 1 implementation repository | Contract code, ABI, deployment scripts, frontend stubs, and CLI tools must stay outside this docs-only dossier |
| P1 | Write Phase 1 threat model | Cover escrow custody, admin powers, reward accounting, treasury depletion, migration, and stale dashboard data |
| P1 | Create separate Phase 2 implementation repository scope | Snapshot scripts, hash-anchor prototypes, query endpoints, and governance prototypes must stay outside this docs-only dossier |
| P1 | Write lightweight governance proposal template | Include advisory/binding status, snapshot round, voting rule, execution note, and concentration context |
| P1 | Write operational-wallet hardening guide | Verify role/balance, segment functions, review time-lock strategy, and avoid private custody details |
| P1 | Write Phase 3 threat model | Cover treasury accounting errors, admin control, legal/listing risk, buyback/burn assumptions, and operational-wallet compromise |
| P1 | Add website contract deployment table | Prevent live-contract claims unless app IDs, source commits, audit status, and deployment dates are recorded |
| P1 | Write MainNet migration checklist | Require TestNet history, audit status, governance approval, treasury policy, and claims review before MainNet |
| P1 | Track professional audit needs | Identify contracts, treasury routing, governance, receipt hashing, and operational-wallet controls needing external review |
| P2 | Add neutral integration notes | Do not imply partner endorsement from public links alone |
| P2 | Add market-intelligence receipt examples | Use static examples and source citations, not executable transaction code |

## Website and Claims Tasks

| Priority | Task | Public-safe implementation |
| --- | --- | --- |
| P1 | Separate PNET protocol pages from earning-oriented/referral content | Keep PNET positioning focused on market intelligence and verification |
| P1 | Replace promotional language with factual language | Describe what is live, what is planned, and what is unverified |
| P1 | Add a neutral asset verification page | Include ASA ID, links, source dates, and risk disclosures |
| P1 | Add source-linked public data/content index | Use dated entries, source URLs, review status, and correction notes; avoid income or return framing |
| P2 | Add FAQ for asset verification | Avoid purchase instructions, return framing, and exchange/listing implications |
| P2 | Add content-source methodology | Explain how public claims, market data, and tokenomics snapshots are reviewed |

## Liquidity and Market-Data Tasks

| Priority | Task | Public-safe implementation |
| --- | --- | --- |
| P1 | Publish canonical liquidity references | Venue, pool ID, pair assets, capture date, and source |
| P1 | Publish slippage and counter-asset quality methodology | Treat all market metrics as stale snapshots |
| P1 | Track LP concentration and withdrawal sensitivity | Do not present token liquidity as protocol TVL |
| P1 | Evaluate protocol-liquidity policy only after treasury policy exists | Liquidity work should be documented as risk management, not as a TVL target or market-making promise |
| P1 | Reconcile direct burn figures with claimed irrecoverable-wallet mechanics | Document which explorers count direct burn-address balances and which require separate methodology for inaccessible accounts |
| P2 | Add liquidity fragmentation notes | Explain micro-pool and long-tail pair risk |
| P2 | Add dashboard/source comparison notes | Compare Vestige, Pera, Allo, Lora, Tinyman, Pact, and indexer data when available |

## Security and Risk Tasks

| Priority | Task | Public-safe implementation |
| --- | --- | --- |
| P1 | Add future-contract security scope | Separate future code repos from this docs-only dossier |
| P1 | Add responsible disclosure process for future software | Keep sensitive reports out of public issues |
| P1 | Monitor impersonation risk | Publish official channels and caution against lookalike assets |
| P2 | Add audit status field for future tools | Mark `Not applicable` until code exists |
| P2 | Add incident/correction log | Record public corrections without deleting prior context |

## Items Not Imported From Review Material

The source review material contained suggestions or descriptions that should not be added to this dossier as claims without evidence.

| Item type | Handling |
| --- | --- |
| Staking or revenue-share language | Not imported as PNET utility; requires formal design and legal/security review |
| Buyback or burn-from-revenue ideas | Not imported as a commitment; would require governance and treasury policy |
| Holder-benefit or token-value phrasing | Not imported; public docs should define utility and risks without implying expected returns |
| Internal strategic analysis PDFs | Raw PDFs not imported when labeled internal/confidential; only sanitized findings may be added |
| User-provided operational wallet address | Included only in `ROADMAP.md` after explicit user instruction; not treated as verified without on-chain and human review |
| Code-generation prompt requesting contracts or deployment scripts | Not implemented in this docs-only repository; future code belongs in a separate implementation repository |
| Purchase or exchange onboarding instructions | Not included in this dossier |
| Web2 earning/referral positioning | Not imported as PNET protocol positioning |
| MainNet tool availability claims | Mark `Needs verification` unless live source evidence is recorded |
| Partner or integration claims | Mark `Needs verification` unless direct evidence from the named party exists |

Current Gate Status: OPEN BACKLOG; no new claims verified by this file.
