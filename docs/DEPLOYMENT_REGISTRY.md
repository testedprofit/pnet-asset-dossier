# PNET Deployment Registry

Status date: 2026-07-11

This registry records what is deployed, what is a local prototype, and what remains planned.

## Rules

- Do not list a component as live without app ID or URL, source reference, deployment transaction, test status, and audit status.
- TestNet deployments must be clearly labeled TestNet.
- MainNet deployments require audit/legal/security gates.
- Local prototype packages must not be presented as public deployments.

## Registry

| Component | Network | Status | App ID / URL | Source reference | Deployment tx | Tests | Audit status | Public claim |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| PNET ERC-20 | Base Mainnet | Deployed token | `0xe1F7F585f458cB6AFFCEE2286b8482523B19ee5a` | [Base token metadata](../data/asset-metadata/pnet-base-token.json) | `0x7d6300cb7f84d18fdaeafe3c34195e946ec86e6ce8c91d87d577177873b39fd1` | Verified interface/source review | No formal audit; minimal OpenZeppelin ERC-20 review recorded | Fixed-supply Base token; profile review pending |
| PNET Uniswap CCA | Base Mainnet | Active auction; migration pending | `0x777900C0FF11845c8e0D6C134b58C695023Aab4e` | [CCA verified-listing plan](25_UNISWAP_CCA_VERIFIED_LISTING_PLAN.md) | `0xcaca93427d8d2a3c29704373e2906ca8e8ce5c84fe5198ce48e9b5726951cb54` | Public UI/on-chain configuration read | Protocol configuration only; project not CCA-verified | Active CCA; no pink badge claimed; final LP proof pending |
| PNET ASA | MainNet | Deployed asset | ASA `3169177585` | [asset identity proof](../data/on-chain-proofs/asset-identity-proof-2026-06-27.md) | `WZJQENKDUTA36XE3SKYZD37D45NFP4WXWHP5LGRPVSNKNGGZJMJA` | N/A | N/A | Asset identity only |
| Community Contribution Protocol | Local/TestNet candidate | MVP ready for TestNet deployment | Pending TestNet app ID | [pnet-contribution-protocol/MVP.md](pnet-contribution-protocol/MVP.md); artifact hashes recorded | Pending | Static checks pass; live TestNet tests pending | Not audited | TestNet MVP only |
| Market-intelligence dashboard | Local prototype | Prototype | Pending | Separate dashboard package; public repo/commit needed | N/A | Build/tests required | Not audited | Planned/public alpha only |
| Governance prototype | Local prototype | Prototype | Pending | Separate governance package; public repo/commit needed | Pending | Local tests required | Not audited | Advisory research only |
| Treasury ledger prototype | Local prototype | Prototype | Pending | Separate governance package; public repo/commit needed | Pending | Local tests required | Not audited | Accounting research only |
| Ecosystem growth registry | Local/TestNet candidate | Prototype | Pending | Separate growth package; public repo/commit needed | Pending | Local tests required | Not audited | Receipt scaffold only |

## Deployment Record Template

| Field | Value |
| --- | --- |
| Component |  |
| Network |  |
| Status |  |
| App ID / URL |  |
| Deployment transaction |  |
| Creator |  |
| Admin |  |
| Source repository |  |
| Source commit/hash |  |
| ABI hash |  |
| Approval hash |  |
| Clear hash |  |
| Test report |  |
| Audit status |  |
| Known limitations |  |
| Reviewer |  |
| Date |  |

Current Gate Status: DEPLOYMENT REGISTRY STARTED; NO PNET PROTOCOL CONTRACT IS CLAIMED LIVE OR MAINNET-READY.
