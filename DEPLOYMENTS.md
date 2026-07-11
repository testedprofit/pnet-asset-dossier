# Deployments and Public References

This repository does not contain deployment code, smart contract code, wallet code, signer logic, or transaction logic.

## Asset Reference

| Network / Venue | Reference | Status |
| --- | --- | --- |
| Base ERC-20 | `0xe1F7F585f458cB6AFFCEE2286b8482523B19ee5a` | Source verified on BaseScan/Blockscout/Sourcify; token profile submitted and review pending |
| Base Uniswap v4 pool | https://app.uniswap.org/explore/pools/base/0xff481004f38fc7db43f3e3b47f6ad3e155482a00866d709d89700d303b0b4f3a | Small seed-liquidity reference only |
| Algorand ASA | `3169177585` | Verified by public indexers in [data/on-chain-proofs/asset-identity-proof-2026-06-27.md](data/on-chain-proofs/asset-identity-proof-2026-06-27.md) |
| Vestige | https://vestige.fi/asset/3169177585 | Needs verification |
| Official website | https://testedprofit.com | Needs verification |
| Tokenomics page | https://testedprofit.com/pages/tokenomics/ | Needs verification |
| PNET page | https://testedprofit.com/pages/PNET/ | Needs verification |

## Deployment Notes

- The Base ERC-20 ProfitNet token is identified by contract `0xe1F7F585f458cB6AFFCEE2286b8482523B19ee5a`.
- BaseScan source verification, address ownership verification, and token profile update submission were completed on 2026-07-11 UTC. Token profile/logo approval is still an external BaseScan review process.
- A public 32 x 32 SVG icon for BaseScan and wallet submissions is available at `media/pnet-logo-32.svg`.
- A very small Base Uniswap v4 USDC/PNET pool exists for discovery and experimentation. This dossier does not claim deep liquidity or market stability.
- The asset is identified by ASA ID `3169177585`. Verified by public indexers at capture round `62554271`.
- Creator address from indexers: `7FRTVAZ5KCEF2CDCJACZHLLHH5QF3DTC7R4IV4KJO4K3P7TMD75ADU3Y5E`.
- Current manager, reserve, freeze, and clawback fields are the Algorand zero address in the dated asset identity proof.
- No deep liquidity, marketplace endorsement, or exchange relationship is verified in this repository. Needs verification.
- No LP, vault, burn, partner, or lock label has been verified from an explorer or indexer in this repository. Needs verification.
- No professional audit, review, or formal attestation is included in this repository.

Detailed registry: [docs/DEPLOYMENT_REGISTRY.md](docs/DEPLOYMENT_REGISTRY.md).

## Publication Checklist

Before changing any reference from `Needs verification` to `Verified`, record:

| Required Record | Status |
| --- | --- |
| Verification date | Needs verification |
| Source URL or chain reference | Needs verification |
| Exact field checked | Needs verification |
| Observed value | Needs verification |
| Reviewer name or handle | Needs verification |
