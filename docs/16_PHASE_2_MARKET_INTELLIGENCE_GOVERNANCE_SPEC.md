# Phase 2 Market Intelligence And Governance Specification

Status date: 2026-06-27

Scope: This is a documentation-only implementation specification. It does not contain snapshot scripts, contract code, deployment scripts, wallet logic, signer logic, frontend code, CLI code, API keys, credentials, or `.env` files.

## Objective

Define a safe Phase 2 path for the PNET whitepaper vision: public, dated, source-linked market intelligence objects and lightweight governance. Phase 2 should begin with off-chain snapshot files and on-chain content hashes before attempting fully on-chain storage or complex governance contracts.

## Phase 2 Principles

| Principle | Requirement |
| --- | --- |
| Verify before claiming | Every data point must have a capture date, source, and review status |
| Prefer simple receipts first | Start with off-chain JSON/Markdown snapshots plus on-chain hash anchoring |
| Preserve history | New snapshots should not overwrite older snapshots |
| Avoid oracle overreach | Receipt data should be treated as dated evidence, not a real-time oracle |
| Keep governance lightweight | Begin with transparent signaling before enforceable protocol actions |
| Separate implementation | Scripts, contracts, dashboards, and APIs belong in a separate implementation repository |

## Sub-Section 3.1: Intelligence Receipts / Snapshots

### Purpose

Create queryable records that describe what was known about an Algorand asset at a specific time. A receipt should be reproducible enough for a reviewer to understand the sources, but humble enough to mark stale or incomplete data clearly.

### Definition: Intelligence Receipt

An intelligence receipt is a dated, source-linked record of asset facts, market context, verification status, and reviewer notes. It may be stored off-chain and anchored on-chain by hash.

### Initial Storage Pattern

| Layer | Function | Phase 2 recommendation |
| --- | --- | --- |
| Off-chain snapshot file | Stores full JSON/Markdown receipt content | Start here |
| Repository commit | Preserves human-readable history and diff | Required for public review |
| Content hash | Identifies exact snapshot contents | Required |
| On-chain note or app state | Anchors content hash and minimal metadata | TestNet first |
| Public query endpoint | Serves latest and historical receipts | Future implementation repo |

### Receipt Fields

| Field | Description | Required |
| --- | --- | --- |
| `receipt_version` | Schema version | Yes |
| `asset_id` | Algorand ASA ID | Yes |
| `asset_name` | Asset name from source | Yes |
| `unit_name` | Asset unit from source | Yes |
| `network` | MainNet, TestNet, or other network | Yes |
| `capture_date` | Date and time of data capture | Yes |
| `source_links` | URLs or endpoint labels used | Yes |
| `source_status` | Available, inaccessible, partial, or stale | Yes |
| `asset_metadata` | Supply, decimals, URL, creator, control fields | Yes |
| `holder_metrics` | Holder count, concentration, top-bucket metrics | Optional but preferred |
| `liquidity_metrics` | Pools, liquidity, volume, routing notes | Optional |
| `verified_claims` | Claims independently confirmed | Optional |
| `needs_verification` | Claims not independently confirmed | Yes |
| `reviewer_notes` | Human notes, limits, caveats | Yes |
| `content_hash` | Hash of canonical receipt content | Yes |
| `on_chain_anchor` | Transaction ID, app ID, or note reference | Optional until TestNet implemented |

### PNET Example Receipt Scope

The first PNET receipt should include only facts that can be sourced or clearly marked.

| Category | Include | Status rule |
| --- | --- | --- |
| Asset identity | ASA ID, name, unit, decimals, supply | Use indexer/explorer source links |
| Control fields | Manager, reserve, freeze, clawback, default frozen | Verify from multiple indexers where possible |
| Website URL | On-chain URL and official website link | Mark source and capture date |
| Holder concentration | Top holder buckets and account counts | Treat as stale snapshot |
| Liquidity | Pool references, TVL, volume, routing context | Treat as stale snapshot |
| Tokenomics claims | Burned, locked, allocation, vault labels | Mark `Needs verification` unless independently confirmed |
| Operational wallet | Only if disclosure remains approved | Mark role and balance `Needs verification` unless verified |
| Lost-creator burn path | Include only after the burn documentation gate passes | Otherwise keep in `Needs verification` |

### Query Model

| Query | Expected result |
| --- | --- |
| Latest receipt by ASA ID | Most recent receipt metadata and source status |
| Receipt by hash | Exact historical receipt |
| Receipts by capture date | Historical timeline for an asset |
| Needs-verification claims | Open claims requiring review |
| Source health | Which sources were accessible, partial, or unavailable |

### Security And Integrity Requirements

| Risk | Required mitigation |
| --- | --- |
| Stale metrics | Display capture date on every query result |
| Source drift | Preserve source URLs and raw source status |
| Hash mismatch | Canonicalize receipt content before hashing and publish hash method |
| False verification | Separate `Verified`, `Needs verification`, `Rejected`, and `Stale` statuses |
| Reviewer bias | Preserve reviewer notes and correction history |
| On-chain cost creep | Anchor hashes, not large payloads, in early versions |
| Privacy leakage | Never include private wallet notes, screenshots, account credentials, or non-public identities |

### Required Deliverables In The Implementation Repo

| Deliverable | Status gate |
| --- | --- |
| Receipt schema | Reviewed and versioned |
| Snapshot creation script | TestNet/off-chain only at first; no committed credentials |
| Canonical hash method | Documented and tested |
| PNET example receipt | Generated from public sources and marked with review statuses |
| On-chain hash anchor prototype | TestNet first |
| Public query example | Read-only and source-linked |
| Correction workflow | Dated, reviewable, and non-destructive |

## Sub-Section 3.2: Lightweight Governance

### Purpose

Allow the community to signal preferences on tool priorities, snapshot parameters, verification policy, and treasury research without implying binding control before governance mechanics are mature.

### Definition: Lightweight Governance

Lightweight governance is a transparent signaling process where eligible participants can express preferences on proposals. Early governance should be non-binding unless a separate governance policy, security review, and maintainer approval process make it binding.

### Initial Governance Pattern

| Layer | Function | Phase 2 recommendation |
| --- | --- | --- |
| Proposal file | Human-readable topic, options, dates, and impact | Start here |
| Snapshot balance rule | Defines which balances count and at what round/date | Required before voting |
| Vote record | Records address, option, weight method, and source | TestNet/off-chain first |
| On-chain anchor | Hashes proposal and final result | TestNet first |
| Execution note | Explains whether action is advisory or implemented | Required |

### Example Proposal Types

| Proposal type | Example | Binding status |
| --- | --- | --- |
| Tool priority | Which AlgoFlow tool should receive TestNet implementation first | Advisory |
| Receipt schema | Add or remove a metric from intelligence receipts | Advisory |
| Source policy | Prefer one indexer fallback order over another | Advisory |
| Treasury research | Explore treasury route for TestNet tool payments | Advisory |
| Governance upgrade | Move from off-chain signaling to on-chain voting contract | Requires review |

### Voting Design Requirements

| Area | Requirement |
| --- | --- |
| Weight basis | Define whether weight uses PNET balance, locked PNET, contribution tier, or one-address signaling |
| Snapshot timing | Use a fixed round or timestamp to avoid moving-balance ambiguity |
| Delegation | Do not include delegation until a separate design review exists |
| Privacy | Do not require private identity disclosure |
| Sybil limits | Acknowledge address-based voting limits |
| Treasury authority | Do not make treasury actions binding in early governance |
| Proposal lifecycle | Draft, open, closed, reviewed, accepted, rejected, implemented |

### Governance Risks

| Risk | Mitigation |
| --- | --- |
| Whale dominance | Publish concentration context alongside vote results |
| Vote buying or borrowed balances | Use fixed snapshot rounds and disclose limits |
| Low participation | Publish quorum context without pretending low-turnout votes are mandate |
| Ambiguous execution | Mark every proposal advisory or binding before voting opens |
| Admin override | Document who can execute actions and why |
| Legal/listing risk | Avoid governance over distributions, investment framing, or exchange claims |

## Phase 2 Codex Prompt Snippets

Use these prompts only inside the future implementation repo or private TestNet workspace.

### Intelligence Receipts

```text
Design and implement a TestNet-first market-intelligence receipt system for Algorand assets. Start with off-chain JSON snapshots plus on-chain content-hash anchoring. Include a versioned receipt schema, canonical hash method, PNET example receipt, source-status fields, Needs verification handling, and read-only query examples. Do not include credentials, signer material, or transaction-submission examples in public docs.
```

### Lightweight Governance

```text
Design and implement a lightweight PNET governance prototype for advisory signaling. Include proposal files, fixed-round balance snapshots, vote records, result hashing, and a clear advisory-vs-binding status. Keep treasury decisions non-binding until a separate governance and security review is complete.
```

## Phase 2 Acceptance Gates

| Gate | Required result |
| --- | --- |
| Separate implementation repo or workspace exists | Pending |
| Receipt schema reviewed | Pending |
| PNET example receipt generated | Pending |
| Canonical hash method documented | Pending |
| On-chain hash anchoring tested | Pending |
| Public query example reviewed | Pending |
| Governance proposal template written | Pending |
| Voting weight rule documented | Pending |
| First advisory proposal completed | Pending |
| Binding governance approved | Not approved |

Current Gate Status: PHASE 2 SPEC READY FOR REVIEW; IMPLEMENTATION NOT STARTED IN THIS REPOSITORY.
