# Deployments and Public References

This repository does not contain deployment code, smart contract code, wallet code, signer logic, or transaction logic.

## Asset Reference

| Network / Venue | Reference | Status |
| --- | --- | --- |
| Base ERC-20 | `0xe1F7F585f458cB6AFFCEE2286b8482523B19ee5a` | Source verified on BaseScan/Blockscout/Sourcify; token profile submitted and review pending |
| Base Uniswap CCA | https://app.uniswap.org/explore/auctions/base/0x777900C0FF11845c8e0D6C134b58C695023Aab4e | Active auction; migration pending at status date |
| Base Uniswap v4 seed pool | https://app.uniswap.org/explore/pools/base/0xff481004f38fc7db43f3e3b47f6ad3e155482a00866d709d89700d303b0b4f3a | Small legacy seed-liquidity reference; not the final auction-migrated pool |
| Base Uniswap v4 price chart | https://app.uniswap.org/explore/pools/base/0xff481004f38fc7db43f3e3b47f6ad3e155482a00866d709d89700d303b0b4f3a?chart=price | Third-party chart reference |
| Algorand ASA | `3169177585` | Verified by public indexers in [data/on-chain-proofs/asset-identity-proof-2026-06-27.md](data/on-chain-proofs/asset-identity-proof-2026-06-27.md) |
| Vestige | https://vestige.fi/asset/3169177585 | Needs verification |
| Official website | https://testedprofit.com | Needs verification |
| Tokenomics page | https://testedprofit.com/pages/tokenomics/ | Needs verification |
| PNET page | https://testedprofit.com/pages/PNET/ | Needs verification |

## Deployment Notes

- The Base ERC-20 ProfitNet token is identified by contract `0xe1F7F585f458cB6AFFCEE2286b8482523B19ee5a`.
- BaseScan source verification, address ownership verification, and token profile update submission were completed on 2026-07-11 UTC. Token profile/logo approval is still an external BaseScan review process.
- A public 32 x 32 SVG icon for BaseScan and wallet submissions is available at `media/pnet-logo-32.svg`.
- A very small Base Uniswap v4 USDC/PNET seed pool exists for discovery and experimentation. This dossier does not claim deep liquidity or market stability.
- A Uniswap Continuous Clearing Auction was launched through transaction `0xcaca93427d8d2a3c29704373e2906ca8e8ce5c84fe5198ce48e9b5726951cb54`. Its auction contract is `0x777900C0FF11845c8e0D6C134b58C695023Aab4e`, LBP strategy is `0x34385dD739FE5464892BF0bA4CC42492804dA000`, and lock/fee-recipient contract is `0xe684c6a25fcced415a5b503bf9738abf7873d023`.
- The auction reports 75% committed to LP and a configured 30-day post-auction LP timelock ending 2026-08-17 02:59:59 UTC. Final migration, pool, position, liquidity amounts, and lock evidence remain pending until confirmed on-chain.
- The asset is identified by ASA ID `3169177585`. Verified by public indexers at capture round `62554271`.
- Creator address from indexers: `7FRTVAZ5KCEF2CDCJACZHLLHH5QF3DTC7R4IV4KJO4K3P7TMD75ADU3Y5E`.
- Current manager, reserve, freeze, and clawback fields are the Algorand zero address in the dated asset identity proof.
- No deep liquidity, marketplace endorsement, or exchange relationship is verified in this repository. Needs verification.
- The CCA configuration and timelock recipient are recorded, but no final migrated LP position or executed Base dead-address transfer is yet claimed. Legacy Algorand LP, vault, burn, partner, and lock labels remain separate evidence questions.
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
