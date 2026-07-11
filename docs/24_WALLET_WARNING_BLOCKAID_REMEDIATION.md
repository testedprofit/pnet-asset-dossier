# Base Wallet Warning and Blockaid Remediation

Status: active public remediation record

Date: 2026-07-11

## Current Public Status

PNET is a legitimate project. The verified Base contract does not contain honeypot mechanics. The warning appears to be a third-party heuristic false positive, likely from new-token/tiny-liquidity/not-listed/holder-concentration signals.

That conclusion is based on review of the verified deployed source described below. It does not mean the third-party warning has already been removed. At the date of this record, the warning remains displayed in Uniswap or wallet surfaces that consume the Blockaid result, pending review and an update by the relevant provider.

The likely signals listed above are an evidence-based remediation hypothesis, not a statement from Blockaid about the exact rule that fired. In particular, a message that PNET is not listed on leading U.S. exchanges describes market/listing status; it is not evidence of contract-level sell blocking.

## Canonical Asset References

| Field | Public reference | Status |
| --- | --- | --- |
| Project / token | ProfitNet / `PNET` | Maintainer identity |
| Base chain | Base mainnet, chain ID `8453` | Public chain reference |
| Base contract | `0xe1F7F585f458cB6AFFCEE2286b8482523B19ee5a` | Source verified on BaseScan |
| Base supply | `100,000,000` PNET | Fixed constructor mint in verified source |
| Deployment transaction | [BaseScan transaction](https://basescan.org/tx/0x7d6300cb7f84d18fdaeafe3c34195e946ec86e6ce8c91d87d577177873b39fd1) | Public chain reference |
| Verified source | [BaseScan contract source](https://basescan.org/address/0xe1F7F585f458cB6AFFCEE2286b8482523B19ee5a#code) | Verified source |
| PNET/USDC market | [Uniswap v4 pool](https://app.uniswap.org/explore/pools/base/0xff481004f38fc7db43f3e3b47f6ad3e155482a00866d709d89700d303b0b4f3a) | Very small seed-liquidity reference |
| Liquidity position | [Uniswap v4 position 2731162](https://app.uniswap.org/positions/v4/base/2731162) | Public UI reference; not proof of a lock or burn |
| Base holder snapshot | [Block `48,477,164` proof](../data/on-chain-proofs/base-holder-distribution-2026-07-11.md) | Maintainer-reported project/founder control of the top two addresses is at least `89.747111457500%`; no on-chain vesting, lock, or custody access for the 15,000,000-PNET founder allocation is evidenced |
| Legacy asset | Algorand ASA `3169177585` | Legacy ProfitNet asset reference |
| Public dossier | [testedprofit/pnet-asset-dossier](https://github.com/testedprofit/pnet-asset-dossier) | Maintainer-controlled documentation |

## Verified Contract Review

The deployed Base source is a minimal OpenZeppelin ERC-20. The code-level review found:

| Reviewed capability | Finding |
| --- | --- |
| Initial supply | Fixed supply minted once in the constructor |
| Transfer behavior | Standard ERC-20 behavior; no transfer override |
| Ownership / administration | No `Ownable`, owner, or administrator control |
| Additional minting | No post-deployment mint function |
| Pause controls | None |
| Blacklist / whitelist | None |
| Transfer tax / fee | None |
| Upgrade path | No proxy |
| Common privilege probes | `owner()` and `minter()` are not exposed |

No contract-level logic was found that selectively blocks sells, restricts recipients, changes transfer amounts through a tax, pauses transfers, or lets an administrator turn those behaviors on later. On that evidence, no contract-level honeypot mechanics were found.

This is a focused verified-source review, not a formal third-party audit and not a guarantee of price, liquidity, market depth, holder behavior, frontend safety, or future market access. Those are separate risks and evidence categories.

## How the Displayed Warning Is Sourced

[Uniswap's token-warning explanation](https://support.uniswap.org/hc/en-us/articles/8723118437133-What-are-token-warnings) states that its token warnings are supplied by Blockaid, which evaluates tokens using dynamic and static heuristics and AI/ML methods. Uniswap also states that it does not independently verify or guarantee the accuracy of those warnings and directs token-warning disputes to Blockaid.

The official [Blockaid report portal](https://report.blockaid.io/) includes a path to report a mistake or false-positive result. These sources explain the remediation route; they do not show that PNET's warning has already been reviewed or cleared.

## Evidence and Remediation Status

| Evidence item | Status | Required follow-up |
| --- | --- | --- |
| BaseScan source verification | Complete | Keep the verified-source URL in every packet |
| BaseScan address ownership verification | Complete | Retain the ownership-verification record for submissions |
| BaseScan token profile/logo | Submitted; external approval pending | Finish the approval workflow and record the approval date |
| Successful PNET buy transaction | Not yet recorded in this dossier | Add a dated Base transaction link and observed outcome |
| Successful PNET sell transaction | Not yet recorded in this dossier | Add a dated Base transaction link and observed outcome |
| Uniswap v4 pool | Public; very small seed liquidity | Record dated liquidity, price-impact, and availability snapshots |
| Uniswap v4 position | Public UI link recorded | Document position ownership and management without calling it locked |
| Auction evidence | PNET CCA, launcher transaction, strategy, dates, and configured LP allocation recorded | Record graduation/migration transaction and final canonical pool after auction completion |
| LP lock or burn evidence | Lock/fee-recipient contract and configured 30-day timelock recorded | Record final migrated position, exact amounts, timelock block/time, and any executed dead-address transfers separately |
| Holder distribution | Block-pinned snapshot and maintainer-supplied founder-control label published; concentration risk remains open | Publish custody/vesting status, refresh after CCA settlement, and improve distribution through genuine participation |
| Blockaid false-positive report | Submission not evidenced in this dossier | Submit the verified-source packet through Blockaid's official report portal and record date/ticket status |
| Warning removal | Pending external provider update | Recheck affected surfaces and record the first confirmed clear result |

## Remediation Plan

1. Finish the pending BaseScan profile/logo approval and preserve the submission and approval references.
2. Record one successful ordinary buy transaction and one successful ordinary sell transaction from the existing PNET/USDC v4 pool. Publish transaction hashes, timestamps, amounts, and observed outcomes as factual test evidence, not as a trading recommendation.
3. Publish liquidity provenance. Identify the existing pool and position, every relevant liquidity transaction, and any auction mechanism actually used. A position page alone does not prove that liquidity is locked or burned.
4. If liquidity is locked or burned, publish the exact on-chain mechanism, transaction, amount, duration or permanence, unlock authority, and beneficiary. If it is not locked or burned, say so plainly.
5. Maintain dated holder-distribution snapshots, publish the controlled-address registry and founder-allocation custody/vesting status, and improve concentration honestly through genuine users, contributors, liquidity participants, or disclosed allocations. Keep the project/founder control label identified as maintainer-supplied. Do not manufacture holder count by splitting balances across controlled wallets.
6. Submit a false-positive packet to Blockaid using the official report portal. Include the verified source, deployment transaction, address-ownership evidence, BaseScan metadata status, pool and position links, recorded buy/sell transactions, liquidity evidence, holder snapshot, official website, and this dossier.
7. Reference Uniswap's official token-warning article when asking Uniswap support to route or track the provider-level correction. Record the submission date and ticket/reference number without publishing private support correspondence.
8. Recheck Uniswap and affected wallet surfaces after Blockaid responds. Do not mark the issue resolved until the warning is actually absent or the provider confirms correction.

## Shortcuts That Must Not Be Used

- Do not create a duplicate Uniswap v2 pool merely to burn its LP token. That would fragment the real market, create a misleading secondary liquidity artifact, and would not correct the evidence for the existing v4 pool.
- Do not wash trade, self-trade for appearance, buy fake volume, or coordinate artificial swaps. Listing and warning evidence must reflect organic activity.
- Do not create fake holders or undisclosed controlled-wallet distributions.
- Do not label the v4 position as locked, burned, renounced, or auction-distributed without the corresponding public evidence.
- Do not tell users that the warning has been removed while it remains visible.
- Do not ask users to disable wallet protections, ignore transaction previews, or connect to an unverified site to help with remediation.

## Public Response Wording

Use this wording while the warning remains visible:

> PNET is a legitimate project. The verified Base contract does not contain honeypot mechanics. The warning appears to be a third-party heuristic false positive, likely from new-token/tiny-liquidity/not-listed/holder-concentration signals. The warning is still displayed pending Blockaid or wallet-provider review. The verified contract, deployment transaction, market links, and remediation status are published in the PNET asset dossier.

Do not shorten this to “warning resolved” or “Blockaid approved PNET” unless a dated provider response or visible product update supports that statement.

## Maintainer Update Record

When evidence changes, append a dated entry containing:

- affected surface;
- previous and current warning text;
- public transaction or source links;
- Blockaid ticket status and any optional Uniswap support follow-up;
- reviewer;
- and whether the warning is still displayed.

Until such an entry is added, the public status remains: verified contract review supports a heuristic false-positive conclusion; provider correction is pending.
