# PNET Contribution Protocol Public Disclosure Plan

Status date: 2026-06-27

This document defines public-safe disclosure rules for the planned PNET Community Contribution Protocol.

The protocol should be described only as:

> PNET Community Contribution Protocol: users may be assigned or receive app-local PNET contribution credits for approved, non-custodial ecosystem participation. Credits may support access and reputation features. Credits are not PNET tokens, not deposits, not yield, not passive income, not guaranteed value, and not an investment return.

Current Gate Status: TESTNET PROTOTYPE REVIEW ONLY; NOT MAINNET; NOT AUDITED; NOT LIVE.

## Public Documentation Plan

The public dossier remains documentation and media only. Contract source, deployment scripts, signer tooling, frontend interaction code, and CLI tools belong in a separate implementation repository or private TestNet workspace until reviewed for publication.

| Item | Public dossier | Separate implementation repository | Internal only |
| --- | --- | --- | --- |
| Protocol overview | Yes | Yes | No |
| Public claims policy | Yes | Yes | No |
| Contract source code | No | Yes, after review | Drafts may exist privately |
| ABI / method documentation | Summary only; link to public ABI | Yes | Drafts may exist privately |
| Generated TEAL / build artifacts | No, unless published as reviewed release evidence | Yes | Drafts may exist privately |
| TestNet deployment record | Summary only after privacy/security review | Yes | Raw local logs before review |
| MainNet deployment record | Yes, only after deployment and review | Yes | No |
| Admin / partner policy | Yes | Yes | Internal drafts before approval |
| Action-code / receipt registry | Yes | Yes | Internal drafts before approval |
| Security review notes | Public-safe summary | Full technical notes where appropriate | Private exploit reproductions until fixed |
| Audit report | Yes, if publishable | Yes | Private preliminary audit correspondence |
| Wallet recovery material | Never | Never | Never commit or share |
| Private signer files | Never | Never | Local secure environment only |
| `.env` files or API keys | Never | Never | Local secure environment only |
| Personal identity notes | Never | Never | Minimize and protect if legally required |
| Wallet screenshots | Never | Never | Avoid collecting |

## Protocol Scope

### In Scope

| Feature | Public-safe description | Status |
| --- | --- | --- |
| User opt-in | A user explicitly opts into the application before local state is initialized | Planned / prototype |
| Admin-assigned credits | Approved administrator assigns app-local contribution credits | Planned / prototype |
| Partner-assigned credits | Approved partner accounts may assign credits within configured limits | Planned / prototype |
| User-to-user credit gifting | Opted-in users may transfer app-local credits to other opted-in users | Planned / prototype |
| Credit consumption | Users may consume app-local credits for access or reputation purposes | Planned / prototype |
| Pause control | Administrator may pause state-changing contribution actions | Planned / prototype |
| Read-only visibility | Public indexers can inspect application state, method calls, and deployment metadata | Required |

### Out of Scope

The contribution protocol must not include or imply:

- staking yield,
- APY or APR,
- passive income,
- guaranteed returns,
- investment return,
- user deposits,
- project custody of user PNET,
- managed strategy,
- copy trading,
- trading, routing, swapping, bridging, or exchange support,
- token minting,
- supply expansion,
- automated burns,
- wallet recovery,
- private signer management.

## Safe Public Wording

Use these phrases:

| Prefer | Avoid |
| --- | --- |
| app-local contribution credits | rewards |
| assigned contribution credits | earned credits |
| receive credits | earn yield |
| consume credits for access | redeem for value |
| access and reputation purposes | income opportunity |
| approved ecosystem participation | staking return |
| non-custodial application | deposit program |
| TestNet prototype | live income product |

## Website Tokenomics Page Text

The following copy is public-safe and ready to paste into the testedprofit tokenomics page after maintainer review.

```markdown
## PNET Community Contribution Protocol

Status: Planned / TestNet prototype. Not MainNet. Not audited. Not live.

The PNET Community Contribution Protocol is designed as a non-custodial Algorand application for app-local contribution credits.

Users may be assigned or receive contribution credits for approved ecosystem participation. These credits are intended for access and reputation features inside PNET-related tools and community workflows.

Contribution credits are not PNET tokens. They are not deposits, not yield, not passive income, not a promise of value, and not an investment return.

The protocol is designed to avoid custody of user PNET. It does not require users to deposit PNET into the application. It does not mint PNET, change PNET supply, or create a guaranteed claim on treasury assets.

Before any public MainNet deployment is described as live, the project should publish:

- source repository link,
- reviewed source commit,
- generated ABI,
- deployment transaction ID,
- application ID,
- creator address,
- admin / upgrade policy,
- security review status,
- known limitations,
- public action-code or receipt policy.

Current status: under review. Treat all contribution-protocol functionality as experimental until a reviewed deployment record is published.
```

## Security & Verification

### On-Chain Visibility

Every public contract should be reviewable from public sources without asking users to connect a wallet.

| Record | Requirement | Status before MainNet |
| --- | --- | --- |
| Network | TestNet or MainNet must be explicit | Required |
| Application ID | Public app ID must be recorded | Required |
| Deployment transaction | Transaction ID and explorer/indexer link | Required |
| Creator address | Public address and role description | Required |
| Application address | Derived app address, if applicable | Required |
| Source commit | Exact reviewed commit or release tag | Required |
| ABI | Human-readable method table and machine-readable ABI link | Required |
| Approval / clear programs | Published build artifact or reproducible build instructions | Required in implementation repo |
| Admin address | Public address or multisig policy | Required |
| Partner list | Public partner addresses and status | Required if partners exist |
| Action-code registry | Public meaning of each grant or consumption code | Required |
| Receipt policy | Hash, URL, or evidence standard for public verification | Required |
| Update / delete policy | Immutable, multisig, timelock, or admin-upgrade model | Required |
| Audit status | Unaudited, reviewed, audited, or deprecated | Required |

### Non-Custodial Guarantee

The contribution protocol should preserve these invariants:

- no PNET custody by the protocol,
- no user deposit requirement,
- no inner asset-transfer path unless separately reviewed and documented,
- no route, swap, bridge, or exchange logic,
- no private wallet or signer logic in the dossier,
- no claim that credits have guaranteed monetary value.

If a future version introduces token transfer, escrow, payment, burn, or treasury routing, it must be treated as a separate security scope and pass a new review.

### Lost Creator Wallet / Burn Accounting

The contribution protocol does not depend on the original PNET creator account and does not implement a burn mechanism.

The dossier contains a user-provided claim that original creator account access may be unavailable and that some opt-out or transfer paths involving that account may affect effective circulating supply. This remains `Needs on-chain and disclosure review`.

Public wording must separate these categories:

| Category | Meaning | Public status |
| --- | --- | --- |
| Direct burned supply | Tokens held by recognized burn addresses or supported by burn transactions | Needs on-chain verification |
| Inaccessible-account supply | Tokens believed to be inaccessible because an account is claimed to be unavailable | Needs methodology and reviewer sign-off |
| Locked supply | Tokens held in a verified lock, escrow, or reviewed contract | Needs lock verification |
| Circulating supply | Methodology-defined supply available under the published supply policy | Needs methodology review |

Do not describe inaccessible-account supply as verified burned supply unless public evidence, methodology, and reviewer sign-off are recorded.

### Operational Wallet Handling

User-provided operational wallet:

`CIVTUU6KLTYO26SPVEBDFBKP3UMZM2DPEO5RINODUVCI5NVIFC6HVNWS7E`

Public status: `Needs verification`.

Before this wallet is used in any public contract disclosure, the dossier should record:

| Review item | Requirement |
| --- | --- |
| Role | Admin, treasury, partner, reserve, testing, or other role |
| Network | MainNet, TestNet, or both |
| Balance source | Dated public explorer or indexer link |
| Movement summary | Public balance delta notes without private custody details |
| Contract relationship | Whether the wallet is admin, creator, partner, treasury, or unrelated |
| Control model | Single signer, multisig, rekeyed account, or other public-safe description |
| Security status | Active, deprecated, compromised, migrated, or Needs verification |

Never publish recovery words, device details, signer location, personal custody notes, or private screenshots.

## Contract Publication Checklist

No PNET utility, contribution, access, treasury, receipt, governance, lock, payment, or burn contract should be described as live until this checklist is complete.

| Check | Required evidence | Status |
| --- | --- | --- |
| Source published? | Public repository URL and exact commit hash | Pending |
| Source reviewed? | Reviewer name or audit status | Pending |
| Deployment tx recorded? | Transaction ID and explorer/indexer link | Pending |
| App ID recorded? | Network-specific app ID | Pending |
| Creator recorded? | Creator address and role | Pending |
| App address recorded? | Derived application address | Pending |
| ABI documented? | Method table and machine-readable ABI link | Pending |
| Method risks documented? | Access control, state changes, and failure modes | Pending |
| Admin policy documented? | Admin, multisig, timelock, or immutable decision | Pending |
| Update/delete policy documented? | Whether upgrades or deletion are possible | Pending |
| Pause policy documented? | Who can pause and what pause affects | Pending |
| Asset IDs documented? | Expected ASA IDs and network caveats | Pending |
| Non-custodial proof reviewed? | Confirmation that no deposit or custody path exists | Pending |
| Public claims reviewed? | No yield, income, ROI, deposit, or listing claims | Pending |
| Action-code registry published? | Public mapping of code values to meanings | Pending |
| Receipt policy published? | Evidence hash, URL, or source-link rules | Pending |
| Tests published? | Unit, integration, and negative tests | Pending |
| TEAL reproducibility checked? | Build process reproduces reviewed approval/clear programs | Pending |
| Audit gate passed? | Audit report or explicit unaudited status | Pending |
| Deployment record linked from dossier? | Dossier entry linking all public evidence | Pending |

## Pre-Publication Changes Required For Current Prototype

These items should be resolved before the contribution protocol is promoted from prototype to public MainNet candidate:

| Item | Reason |
| --- | --- |
| Rename `earned` / `get_earned` to `granted` / `get_granted` | Avoid income or yield interpretation |
| Add explicit admin-versus-partner authorization branch | Avoid unnecessary local-state reads and make access control easier to audit |
| Disallow self-gifting | Prevent artificial inflation of gift metrics |
| Restrict or disclose partner self-grants | Prevent partner-created reputation inflation |
| Add receipt hash or public evidence reference to grant/consume flows | Improve verifiability |
| Require an explicit TestNet ASA ID in deployment tooling | Avoid confusing MainNet ASA references in TestNet records |
| Decide immutable vs upgradeable MainNet policy | Reduce upgrade and admin-trust risk |

## Public Disclosure Template

Use this template for each future deployment record.

```markdown
## PNET Contribution Protocol Deployment Record

Status date:
Network:
Application ID:
Application address:
Deployment transaction:
Creator address:
Admin address:
Partner addresses:
PNET / test asset ID:
Source repository:
Reviewed source commit:
ABI:
Approval program hash:
Clear program hash:
Update/delete policy:
Pause policy:
Audit status:
Known limitations:
Public claims review:

Non-custodial statement:
This application does not custody user PNET, does not require user deposits, and does not provide guaranteed value, passive income, yield, or investment return.

Verification links:
- Explorer:
- Indexer:
- Source:
- ABI:
- Audit or review:
```

## Current Gate Status

| Gate | Status | Notes |
| --- | --- | --- |
| Public-safe framing | READY FOR REVIEW | Contribution credits are framed as app-local access/reputation records only |
| Dossier scope | PASS | No code, signer logic, or deployment script added by this file |
| Website copy | READY FOR REVIEW | Copy is safe to paste after maintainer review |
| Security and verification section | READY FOR REVIEW | Lost-wallet and operational-wallet items remain `Needs verification` |
| Contract checklist | READY FOR REVIEW | No contract should be marked live until checklist evidence exists |
| MainNet readiness | NOT READY | Requires code changes, TestNet evidence, public deployment record, and professional review |
