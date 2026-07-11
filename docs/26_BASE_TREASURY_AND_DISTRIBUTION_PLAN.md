# Base Treasury and Distribution Plan

Status date: 2026-07-11

Decision: **NO-GO on scheduling another standard Uniswap CCA now.** Finish and document the active CCA first, establish transparent treasury custody and beneficial-owner labels, build organic demand in one canonical market, and require every future distribution gate below to pass.

This is a project operations and disclosure plan, not project-specific legal, tax, securities, or investment advice. Another public token sale or auction requires qualified counsel in the relevant jurisdictions before launch.

Base treasury-category amounts and allocation percentages remain pending the project owner's documented decision and legal review. This plan does not assign tokens to treasury, team, grants, liquidity, or any sale.

## Why Another Auction Is Not The Immediate Fix

The [dated holder snapshot](../data/on-chain-proofs/base-holder-distribution-2026-07-11.md) records:

- `74.747111457500%` in the largest address;
- an unlabelled `15,000,000`-PNET address, making potential same-control concentration `89.747111457500%` if it shares the largest address's beneficial controller;
- `4.745752137568%` in the active CCA contract;
- `3.559314103176%` in its LBP strategy; and
- `1.947813470058%` at the Uniswap v4 PoolManager.

CCA, LBP-strategy, and PoolManager balances are contract inventory, not independent people. More contracts or more addresses do not by themselves decentralize beneficial ownership.

A repeated stock CCA can also fragment the market. A Uniswap v4 pool is identified by its currencies, fee, tick spacing, and hooks. The stock launcher reserves a target PoolId; an overlapping launch using that PoolId is rejected, while a launch that selects different fee/tick/hook parameters creates a different PoolKey. If an intended hookless pool already exists, the stock LBP strategy can fall back to a strategy-hooked PoolKey, also a different pool. It initializes the selected pool; it is not the normal path for increasing an existing position.

Primary technical references:

- [LiquidityLauncher supports one or more strategies](https://github.com/Uniswap/liquidity-launcher/blob/bb9952bfaf8a072340fcdd9519f228339ea9f7ad/src/LiquidityLauncher.sol#L13-L61)
- [LBP strategy PoolId reservation and conflict handling](https://github.com/Uniswap/liquidity-launcher/blob/bb9952bfaf8a072340fcdd9519f228339ea9f7ad/src/strategies/lbp/LBPStrategy.sol#L122-L143)
- [Existing intended-pool fallback selects a strategy-hooked PoolKey](https://github.com/Uniswap/liquidity-launcher/blob/bb9952bfaf8a072340fcdd9519f228339ea9f7ad/src/strategies/lbp/LBPStrategy.sol#L211-L263)
- [Selected-pool initialization behavior](https://github.com/Uniswap/liquidity-launcher/blob/bb9952bfaf8a072340fcdd9519f228339ea9f7ad/src/strategies/lbp/LBPStrategy.sol#L318-L329)
- [Uniswap guidance for adding liquidity to an existing pool](https://support.uniswap.org/hc/en-us/articles/32233918539533-How-to-add-a-new-liquidity-position-to-Uniswap-v4)
- [Uniswap guidance for increasing an existing position](https://support.uniswap.org/hc/en-us/articles/39530204759693-How-do-I-add-liquidity-to-an-existing-position)

If the goal is deeper liquidity, add or increase liquidity in the eventual canonical pool after the current CCA settles and the final PoolKey is known. If the goal is broader ownership, distribute to genuinely independent participants through a disclosed, reviewed program. Do not use another pool merely as a holder-count or badge artifact.

## Four Separate Objectives

| Objective | Honest measure | What does not count |
| --- | --- | --- |
| Custody resilience | Published multisig threshold, independent signers, hardware-wallet practices, recovery process, and tested execution | One person controlling several signer addresses |
| Economic distribution | Independently controlled beneficial owners, disclosed restrictions, concentration trend, and retention | Controlled-wallet splitting, dust transfers, auction contracts, or undisclosed related wallets |
| Liquidity depth | Canonical-pool TVL, two-sided execution, price impact, organic volume, and documented LP custody | Duplicate pools, self-trades, wash volume, or an ERC-20 holder count |
| Governance distribution | Independent decision-makers, documented scope, voting/approval policy, and conflict handling | Calling a treasury transfer “decentralization” without decision rights |

PNET should report these dimensions separately. A multisig improves custody but does not automatically broaden economic ownership. Grants can broaden ownership only when recipients are independent and retain genuine control. Liquidity contract balances do not prove LP ownership or lock status.

## Immediate Treasury Policy

1. **Label before moving.** Publish the purpose and beneficial-control category of the unlabelled 15,000,000-PNET address and every project-controlled Base address.
2. **Define Base tokenomics.** Publish Base treasury, team, liquidity, auction, grant, vesting, reserve, and circulating-supply treatments separately from the legacy Algorand ASA unless a verified bridge/accounting policy connects them.
3. **Improve custody deliberately.** Consider a `2-of-3` or `3-of-5` Safe with genuinely independent signers. Test creation, recovery, and a small transfer before moving material treasury inventory. Do not publish private signer details or recovery information.
4. **Use restrictions that are verifiable.** Where team or grant allocations are intended to vest, use reviewed vesting/timelock contracts and publish their addresses, schedules, beneficiaries by public role, and funding transactions.
5. **Do not move the whole balance for optics.** Approve a written allocation, risk review, and transaction packet first. Same-controller wallet transfers do not improve beneficial ownership.
6. **Publish a controlled-address registry.** Record address, public role, control category, custodian type, restrictions, funding source, and current balance. Mark unknown relationships as unknown.
7. **Separate LP evidence.** ERC-20 holder data cannot prove a v4 position NFT is locked. After migration, publish the final position token ID, owner, timelock contract, lock transaction, unlock time/block, withdrawal authority, fee recipient, and post-expiry plan. Until that exists, do not claim the current position is locked.

[Safe's official smart-account concepts](https://docs.safe.global/advanced/smart-account-concepts) describe owners and signature thresholds. A Safe configuration is only as independent as its real signers.

## Organic Distribution Channels

Use a portfolio of disclosed paths instead of repeated auctions:

1. Small milestone grants for shipped security work, documentation, integrations, product features, research, or verified community infrastructure.
2. Vested contributor allocations tied to written scopes and acceptance evidence.
3. Customer or user utility programs only after a working product exists, with clear eligibility and no promise of profit or price appreciation.
4. Liquidity provision in the canonical pool, with public custody and lock evidence.
5. At most one later public distribution round during this planning horizon, and only if every gate below passes.

Do not reward buying, holding, posting hype, recruiting buyers, generating trades, or maintaining a price. Do not select grants merely to increase the holder count. Publish conflicts and exclude project-controlled recipients from “independent holder” metrics.

## Future Distribution Go/No-Go Gates

These are PNET's proposed internal guardrails, not official Uniswap requirements.

| Gate | Required evidence before a GO decision |
| --- | --- |
| Current CCA resolved | Auction ended; success/failure, sold and unsold amounts, USDC raised/refunded, unique independently funded bidders, top-bidder concentration, and settlement transactions published |
| Migration complete | If the auction graduates, `migrate()` succeeded and the final PoolKey, pool ID, position, deposited amounts, and LP custody are published |
| Observation period | At least 30 days after successful migration with no overlapping public distribution round |
| Purpose and proceeds | Written non-price purpose, token source, maximum allocation, eligibility, use of proceeds, conflicts, refund/failure treatment, and public risk disclosure |
| One canonical market | The proposed mechanism is proven not to fragment liquidity; if the objective is liquidity, it adds to the existing canonical PoolKey instead of launching another stock CCA/pool |
| Organic participation | At least 25 non-affiliated organic traders over the trailing 30 days, including at least five sellers, excluding project/team/agent-controlled activity |
| Usable two-sided market | A modeled `US$100` buy and `US$100` sell each show no more than `2%` price impact at the review snapshot; methodology and timestamp published |
| Proportional scale | Canonical-pool TVL is at least the proposed gross raise and trailing-30-day organic volume is at least three times the proposed gross raise |
| Conservative size | Maximum tokens are the lesser of `1%` of fixed total supply or `50%` of the tokens actually sold in the first CCA |
| Concentration improvement | Forecast and post-round reports use beneficial-control groups, not address count, and show genuine improvement without related-wallet splitting |
| Integrity controls | No self/team bidding, self-trading, wallet splitting, rebates, bought holders, wash trading, artificial volume, trading contests, or undisclosed market support |
| External review | Current warning/remediation evidence updated, operational/security review passed, and qualified legal/tax counsel clears the proposed structure and disclosures |

A failed gate means **NO-GO**. The response is to fix demand, product, disclosure, liquidity, or control weaknesses—not to lower the measurement standard or create another pool.

## 30 / 60 / 90-Day Execution Plan

### Days 0–30: establish truth and finish the current launch

| Project owner / human actions | AI-assisted documentation and analysis |
| --- | --- |
| Confirm whether `0x7f97e32af1d2eb65d9d5f5b5ce15048768234a58` is related to the project and approve its public label. | Maintain the block-pinned holder snapshot and draft the beneficial-control registry with unknowns visibly marked. |
| Decide Base-specific allocation categories and approve a treasury policy; do not copy legacy Algorand figures without a documented relationship. | Draft allocation tables, circulating-supply methodology, treasury-policy text, and public transaction-proof templates. |
| Choose genuinely independent Safe signers, use hardware wallets, document conflicts, and test a small transaction before any material move. | Prepare an unsigned Safe setup/transaction checklist and review public configuration fields; never request or store keys, seed phrases, or recovery data. |
| Let the active CCA finish without project/team self-bids or undisclosed support. Execute settlement/migration only through the verified official flow. | Monitor public auction and chain state, then prepare a factual settlement report showing sold/unsold amounts, independently funded bidders, concentration, migration, final pool, and open gaps. |
| Finish BaseScan profile/logo follow-up and submit the verified-source false-positive evidence to Blockaid/Uniswap through official routes. | Assemble public evidence links and maintain remediation status without claiming the warning is removed before the affected surface updates. |

### Days 31–60: distribute through shipped work and harden custody

| Project owner / human actions | AI-assisted documentation and analysis |
| --- | --- |
| Approve only three to five small, milestone-based grants for real security, documentation, integration, or product deliverables; disclose conflicts and use vesting where appropriate. | Draft grant scopes, acceptance tests, disclosure forms, vesting schedules, and a public grant ledger. The owner—not AI—chooses recipients and signs transactions. |
| After review, execute approved treasury, vesting, or Safe transactions and publish their hashes. | Validate public fields, reconcile balances, and update holder/entity concentration at days 45 and 60. |
| Add liquidity only to the documented canonical pool when justified by the approved treasury policy; publish position custody and restrictions. | Model price impact and liquidity scenarios, check PoolKey consistency, and prepare an evidence packet. AI does not provide funds or execute swaps. |
| Ship and publicly demonstrate product utility, including the planned Command Center or equivalent working user flow. | Turn shipped artifacts into factual docs, integration guides, and measurement dashboards without price promises. |

### Days 61–90: audit outcomes and make one gated decision

| Project owner / human actions | AI-assisted documentation and analysis |
| --- | --- |
| Review the beneficial-owner report, custody controls, grant delivery, market quality, and legal advice. | Calculate top-holder and control-group shares, Gini, Nakamoto coefficient, holder retention, trader independence flags, volume exclusions, TVL, and buy/sell price impact. |
| Before any configured LP timelock expires, publish the verified current lock status and post-expiry no-withdrawal, relock, or custody policy. Do not call an NFT locked until on-chain proof exists. | Reconcile position ownership, timelock calls, unlock authority, fees, and post-expiry actions into a dated LP proof packet. |
| Approve a later distribution only if every gate passes; otherwise publish NO-GO and continue organic product/community work. | Produce a signed-off decision memo with each gate marked PASS, FAIL, or NOT EVIDENCED and update the public proof index. |

## Non-Negotiable Integrity Rules

- No self-bidding or team bidding in an auction presented as independent demand.
- No wash trading, circular trading, bought volume, fake market making, or coordinated price support.
- No dust airdrops, controlled-wallet splitting, or Sybil wallets used to inflate holder counts.
- No duplicate v2/v3/v4 pool created merely to burn or lock a different LP artifact.
- No claims of “decentralized,” “community owned,” “LP locked,” or “warning cleared” without the corresponding dated evidence.
- No guaranteed-return, price-target, “moonshot,” exchange-listing, or passive-income claims.
- No private keys, seed phrases, signer locations, personal data, private support correspondence, or wallet screenshots in this repository.

Uniswap's [CCA terms](https://support.uniswap.org/hc/en-us/articles/30935100859661-Uniswap-Labs-Terms-of-Service) apply independently. Integrity rules also protect the usefulness of the dossier's evidence and reduce the risk that remediation activity itself looks manipulative.

## Decision Record

Current decision: **NO-GO for another standard CCA.**

Reconsideration trigger: the current CCA is fully resolved, the final canonical pool and LP custody are proven, the 30-day observation period completes, beneficial-control labels are published, all quantitative gates pass, and qualified counsel approves the proposed distribution.

Related records:

- [Base holder-distribution snapshot](../data/on-chain-proofs/base-holder-distribution-2026-07-11.md)
- [Wallet warning and Blockaid remediation](24_WALLET_WARNING_BLOCKAID_REMEDIATION.md)
- [Uniswap CCA verified-listing plan](25_UNISWAP_CCA_VERIFIED_LISTING_PLAN.md)
- [Moonshot runway](22_MOONSHOT_RUNWAY.md)
- [Public claims policy](06_PUBLIC_CLAIMS_POLICY.md)
