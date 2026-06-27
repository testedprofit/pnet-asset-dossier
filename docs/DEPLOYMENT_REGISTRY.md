# PNET Deployment Registry

Status date: 2026-06-27

This registry records what is deployed, what is a local prototype, and what remains planned.

## Rules

- Do not list a component as live without app ID or URL, source reference, deployment transaction, test status, and audit status.
- TestNet deployments must be clearly labeled TestNet.
- MainNet deployments require audit/legal/security gates.
- Local prototype packages must not be presented as public deployments.

## Registry

| Component | Network | Status | App ID / URL | Source reference | Deployment tx | Tests | Audit status | Public claim |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
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
