# Uniswap CCA Verified Listing Plan

Status date: 2026-07-11

Scope: the pink check shown beside some projects in Uniswap's Continuous Clearing Auction interface.

## What The Pink Check Means

The pink check is a **Verified CCA auction/launch** designation. It is not a general verification of the PNET token contract, not an endorsement, and not a safety ruling.

Uniswap's published requirements are:

1. At least 1% of total token supply **or** 25% of the auctioned tokens must be added to a Uniswap liquidity pool.
2. The project must meet at least three of these four criteria:
   - identified and visible founders on public social channels;
   - approximately 20,000 or more followers on X;
   - project coverage from CoinList, Blockworks, Fortune, Decrypt, The Block, or The Defiant;
   - documented funding from one of the major U.S. funds enumerated by Uniswap.
3. The project must submit Uniswap's official evaluation form and pass Uniswap's review.

Official criteria: https://support.uniswap.org/hc/en-us/articles/43107250032781-What-are-CCA-Verified-Listings

Official form: https://share.hsforms.com/1AN-LREhwT3uK03oGKvOGvgs8pgg

## PNET Current Scorecard

| Requirement | Current evidence | Status |
| --- | --- | --- |
| LP allocation gate | Auction UI reports 75% committed to LP. Approximately 3,559,314 PNET is configured for post-auction liquidity, about 3.559% of the 100,000,000 supply and 75% of the approximately 4,745,752 PNET auction amount. | Configuration appears sufficient; final proof requires successful migration and LP-addition transaction evidence. |
| Publicly visible founder | The public dossier and current website do not identify a founder and link matching LinkedIn/social identity evidence. | Not currently evidenced. User input required. |
| 20,000+ X followers | The website's `@TestedProfit` link is stale. A project-associated `@ProfitnetPNET` profile has been observed, but project control must be confirmed and the 20,000-follower threshold is not evidenced. | Not currently evidenced. |
| Qualifying major press | No qualifying outlet coverage is recorded in this dossier. | Not currently evidenced. |
| Qualifying U.S. fund backing | No qualifying investment evidence is recorded in this dossier. | Not currently evidenced. Do not imply backing that does not exist. |

Conclusion: PNET is not currently documented as meeting the required three-of-four identity/traction test. There is no truthful instant or paid shortcut to the CCA badge.

## PNET CCA Evidence

| Item | Reference | Status |
| --- | --- | --- |
| Base token | `0xe1F7F585f458cB6AFFCEE2286b8482523B19ee5a` | Source verified; fixed supply |
| Auction contract | `0x777900C0FF11845c8e0D6C134b58C695023Aab4e` | Active CCA reference at status date |
| Auction page | https://app.uniswap.org/explore/auctions/base/0x777900C0FF11845c8e0D6C134b58C695023Aab4e | Public Uniswap interface |
| Launcher transaction | `0xcaca93427d8d2a3c29704373e2906ca8e8ce5c84fe5198ce48e9b5726951cb54` | Public Base transaction |
| LBP strategy | `0x34385dD739FE5464892BF0bA4CC42492804dA000` | Public chain reference |
| Lock / fee-recipient contract | `0xe684c6a25fcced415a5b503bf9738abf7873d023` | Public chain reference |
| Auction window | 2026-07-11 02:59:59 UTC through 2026-07-18 02:59:59 UTC | Configured schedule |
| LP timelock end | 2026-08-17 02:59:59 UTC | Configured 30-day post-auction timelock; final migrated LP must be recorded |
| Final migrated pool and position | Pending | Do not claim migration or final pool identity until confirmed on-chain |

## Execution Plan

### Phase 1: Fix Public Identity

1. Confirm the project-controlled X handle. Update the website, dossier, BaseScan follow-up, and metadata to one working handle.
2. Establish a domain-controlled project email.
3. Publish a founder/team disclosure page with the founder's chosen public name, role, current LinkedIn profile, project X profile, and a concise conflict/holdings disclosure.
4. Update the official PNET page so the Base contract, BaseScan source, CCA auction, public dossier, and legacy Algorand ASA are clearly separated.
5. Remove dead Discord or social links until valid replacements exist.

Founder page template: [templates/FOUNDER_DISCLOSURE_TEMPLATE.md](templates/FOUNDER_DISCLOSURE_TEMPLATE.md)

### Phase 2: Finish The On-Chain Gate

After the auction ends:

1. Confirm graduation and migration on-chain.
2. Record the final canonical pool ID and position.
3. Record the exact PNET and USDC liquidity amounts.
4. Record the LP owner/recipient and timelock end block/time.
5. Publish transaction links and update this scorecard.
6. Keep the earlier seed pool labeled `legacy seed pool`; do not create another pool for badge optics.

### Phase 3: Earn Three Of Four

The most plausible truthful route, absent real qualifying fund backing, is:

1. Public founder identity.
2. Organic growth of the confirmed project X account to the published threshold.
3. Independent editorial coverage from one of Uniswap's named outlets.

Use [marketing/CCA_PRESS_KIT.md](marketing/CCA_PRESS_KIT.md) as a factual source pack. Paid placement, follower purchases, fabricated coverage, or invented funding must not be used.

### Phase 4: Submit

Submit only when the public evidence supports the required criteria. The current form requests:

- project email;
- project X profile;
- founder identity evidence;
- qualifying major press evidence;
- qualifying fund evidence;
- optional logo upload.

Prepared worksheet: [templates/UNISWAP_CCA_APPLICATION_WORKSHEET.md](templates/UNISWAP_CCA_APPLICATION_WORKSHEET.md)

If the project qualifies using founder identity, X following, and press but has no qualifying fund, state that honestly rather than implying investment. Ask Uniswap support how it prefers a non-relied-upon required field to be completed.

## Separate Blockaid Workstream

The CCA check and the Blockaid warning are different systems. Earning the CCA badge does not itself remove the warning. Continue the false-positive process in [24_WALLET_WARNING_BLOCKAID_REMEDIATION.md](24_WALLET_WARNING_BLOCKAID_REMEDIATION.md).

The verified Base contract does not contain honeypot mechanics. The displayed warning remains active pending third-party review and surface updates.

## Anti-Fraud Guardrails

- Do not pay a person claiming they can sell a Uniswap verification badge.
- Do not sign wallet messages or transactions for off-platform badge verification.
- Do not buy followers, press mentions, bids, holders, or trading volume.
- Do not fabricate founder identity, funding, or outlet coverage.
- Use only the form linked from Uniswap's official support article.
- Describe any future designation as `Verified CCA auction/launch`, not `Uniswap-verified token`.
