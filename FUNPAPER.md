# ProfitNet / PNET Funpaper

Status: Professional not-an-investment-asset companion paper with a sense of humor  
Publication date: 2026-07-11  
Canonical technical document: [WHITEPAPER.md](WHITEPAPER.md)  
Repository: https://github.com/testedprofit/pnet-asset-dossier

## 1. Purpose of This Document

This document explains ProfitNet (`PNET`) in plain language. It is intentionally more readable than the canonical whitepaper, but it still uses real project facts and conservative public claims.

The short version:

```text
PNET is an AI-first Web3 experiment.
PNET is rooted on Algorand.
PNET is testing a Base ERC-20 expansion.
PNET is not being presented as an investment asset.
PNET does not promise profit, yield, hashrate rewards, or future value.
```

That last part matters. PNET is an on-chain token/asset in the technical blockchain sense. Algorand literally calls the original object an Algorand Standard Asset, and wallets/explorers will often use the word "asset" because they enjoy making lawyers drink water.

This document uses "not an asset" only in the public-offering sense:

```text
PNET is not being marketed as an investment asset.
PNET is not being marketed as a security.
PNET is not being marketed as a claim on revenue, hashrate, compute, treasury assets, or future value.
```

PNET is a project token used to test documentation, metadata, community tooling, AI-assisted operations, and multichain workflows.

If the project ever starts sounding like a magic money machine, something has gone wrong and the paperwork should be asked to sit quietly and think about what it did.

## 2. Current Verified Facts

### 2.1 Algorand Root

PNET began on Algorand and remains rooted there.

| Field | Value |
| --- | --- |
| Network | Algorand MainNet |
| Asset type | Algorand Standard Asset |
| ASA ID | `3169177585` |
| Name | ProfitNet |
| Unit | PNET |
| Total supply | `100,000,000` PNET |
| Decimals | `6` |
| Creator address | `7FRTVAZ5KCEF2CDCJACZHLLHH5QF3DTC7R4IV4KJO4K3P7TMD75ADU3Y5E` |
| Creation tx | `WZJQENKDUTA36XE3SKYZD37D45NFP4WXWHP5LGRPVSNKNGGZJMJA` |
| Current ASA controls | Manager, reserve, freeze, and clawback verified as zero address in the dated public-indexer proof |
| Public market reference | https://vestige.fi/asset/3169177585 |

The public dossier records the Algorand identity, public source links, verification status, and unresolved claims. The project should continue treating Algorand as the root context unless a formal migration or multichain architecture is documented.

### 2.2 Base ERC-20 Expansion

PNET also has a Base ERC-20 deployment used for EVM compatibility and multichain testing.

| Field | Value |
| --- | --- |
| Network | Base mainnet |
| Chain ID | `8453` |
| Contract | `0xe1F7F585f458cB6AFFCEE2286b8482523B19ee5a` |
| Name | ProfitNet |
| Symbol | PNET |
| Total supply | `100,000,000` PNET |
| Decimals | `18` |
| Initial recipient | `0xd58cc829622c4c988af43028aaa37eda84104649` |
| Deployment tx | `0x7d6300cb7f84d18fdaeafe3c34195e946ec86e6ce8c91d87d577177873b39fd1` |

The Base contract is intentionally simple:

- fixed supply,
- no owner,
- no admin mint,
- no pause,
- no blacklist,
- no transfer tax,
- no upgrade proxy.

In technical terms, it is boring. In token-contract terms, boring is a feature.

### 2.3 Verification and Metadata

Current Base verification status:

| Item | Status |
| --- | --- |
| BaseScan source verification | Complete |
| BaseScan address ownership verification | Complete |
| Blockscout source verification | Complete |
| Sourcify source verification | Complete |
| BaseScan token profile/logo | Pending external BaseScan review after submission |
| Public SVG logo | Available |

Current logo submission URL:

```text
https://raw.githubusercontent.com/testedprofit/pnet-asset-dossier/376be2dada8af8f8371bfc45516ca16be594060f/media/pnet-logo-32.svg
```

### 2.4 Known Unknowns

The dossier intentionally keeps some claims in the "Needs verification" box:

- original creator wallet access status,
- lost-creator or inaccessible-account supply effects,
- direct burn accounting,
- founder allocation lock status,
- strategic reserve lock status,
- LP/vault labels,
- and any future bridge state.

That is not a weakness. That is the point of the dossier. A fact graduates when the evidence shows up, not when the vibes become compelling.

## 3. What ProfitNet Is

ProfitNet is an AI-first Web3 project focused on learning, documentation, tooling, and interoperability.

The project is currently exploring:

- how AI agents can help manage Web3 project operations,
- how token metadata can be kept consistent across explorers and wallets,
- how Algorand and EVM environments can coexist under one project identity,
- how public claims can be documented without exaggeration,
- how community tooling can be built without presenting the token as a financial product,
- and how future multichain workflows can be tested carefully.

This is not the loudest possible version of a crypto project. That is intentional. The loudest possible version usually arrives with a countdown timer and leaves behind broken links.

## 4. What ProfitNet Is Not

ProfitNet is not presented as:

- a security,
- an investment contract,
- a dividend or revenue-share product,
- a cloud-mining product,
- a hashrate-backed instrument,
- a passive-income system,
- a managed trading strategy,
- a deposit program,
- a guaranteed-return product,
- an exchange-listing promise,
- a bridge-support guarantee,
- or a claim on any machine, wallet, treasury, liquidity pool, or future business revenue.

There may be internal or undisclosed compute / hashrate connected to broader project operations. That context is not a PNET holder entitlement. It is not a yield source. It is not a mining contract. It is not an implied claim on revenue.

The clean framing is:

```text
Hashrate may exist as private operational context.
Hashrate is not a PNET feature, right, promise, or payout source.
```

Simple. Slightly less exciting. Much safer.

## 5. Why AI-First?

Web3 projects create a lot of operational exhaust:

- contract addresses,
- token IDs,
- liquidity links,
- explorer pages,
- verification forms,
- bridge notes,
- logo files,
- wallet warnings,
- half-finished docs,
- and screenshots that somehow become project management.

ProfitNet uses AI as a coordination layer for that complexity. The goal is not to replace judgment. The goal is to help keep the project legible.

AI can help:

- summarize project state,
- generate repeatable runbooks,
- compare claims against public evidence,
- maintain documentation,
- prepare verification checklists,
- spot missing links,
- and help future reviewers understand what happened without needing to excavate an entire chat history.

The AI is not the CEO. It is closer to an over-caffeinated documentation assistant with excellent recall and no wallet.

## 6. Why Algorand Still Matters

Algorand remains important to PNET because the original public asset identity lives there.

The Algorand side provides:

- the legacy PNET ASA ID,
- fast and inexpensive transaction infrastructure,
- public indexer access,
- clear asset parameters,
- and a long-running reference point for the project.

The Base expansion does not erase the Algorand root. It adds an EVM surface for experimentation.

The project should be described as:

```text
Algorand-rooted.
Base-expanded.
Attempting multichain interoperability.
Still experimental.
```

That is more accurate than pretending every chain is already perfectly synchronized and wearing matching uniforms.

## 7. Why Base?

Base gives PNET access to the EVM ecosystem:

- Solidity,
- OpenZeppelin,
- Hardhat,
- Basescan,
- Uniswap,
- wallet support,
- and future Wormhole NTT practice paths.

Base is not replacing Algorand. Base is the current EVM experiment.

The Base ERC-20 contract gives the project a simple, verifiable token surface for testing wallets, metadata, liquidity discovery, and future bridge mechanics.

## 8. Liquidity Status

PNET has a very small Uniswap v4 USDC/PNET pool on Base.

Public references:

```text
Uniswap pool:
https://app.uniswap.org/explore/pools/base/0xff481004f38fc7db43f3e3b47f6ad3e155482a00866d709d89700d303b0b4f3a

Uniswap position:
https://app.uniswap.org/positions/v4/base/2731162
```

This pool should be described carefully:

- it is real,
- it is public,
- it is useful for discovery and testing,
- it is not deep liquidity,
- it is not proof of market demand,
- it is not a valuation guarantee,
- and it should not be used to imply stability.

In plain English: the pool exists. It is not yet a swimming pool. It is closer to a carefully labeled puddle with a contract address.

## 9. Multichain Direction

ProfitNet is attempting to become multichain in a controlled way.

Current direction:

- keep Algorand as a root project context,
- keep Base as the verified EVM ERC-20 surface,
- test Wormhole NTT on testnets before mainnet bridge work,
- document every manager role and token mode,
- avoid duplicate-supply confusion,
- and avoid claiming bridge support before bridge evidence exists.

The correct bridge posture is:

```text
Testnet first.
Tiny amounts.
No production role grants without review.
No public bridge claims until a round trip is proven.
```

This may sound cautious, but bridges are one of the few places in crypto where "we clicked it and hoped" is not considered a robust security model.

## 10. Public Claims Policy

ProfitNet should make claims that are:

- dated,
- sourced,
- reproducible,
- conservative,
- and easy to correct.

ProfitNet should avoid claims that are:

- promotional without evidence,
- based only on screenshots,
- promising future value,
- implying investment returns,
- implying mining revenue,
- implying exchange support,
- implying guaranteed bridge support,
- or pretending experimental work is production infrastructure.

The project can be ambitious without sounding like a brochure found under a casino seat.

## 11. Roadmap

### Phase 1: Public Identity and Metadata

Goals:

- verify contracts,
- submit token profiles,
- maintain logo assets,
- keep public links updated,
- and make the project understandable to humans and AI agents.

Status: active.

### Phase 2: AI-Assisted Operations

Goals:

- maintain runbooks,
- document deployments,
- track verification gates,
- support public-safe copy,
- and reduce the odds that an important token address lives only in someone's browser history.

Status: active.

### Phase 3: Multichain Testing

Goals:

- practice Wormhole NTT on testnets,
- document Base and peer-chain roles,
- test tiny transfers,
- and avoid making mainnet changes while excited.

Status: planned / lab.

### Phase 4: Community Tooling

Goals:

- explore non-custodial contribution tooling,
- keep credits separate from PNET tokens,
- avoid yield or reward promises,
- and publish evidence before claiming utility.

Status: specification work.

## 12. Risk Summary

PNET has real risks:

- low current Base liquidity,
- experimental multichain setup,
- fragmented Algorand and Base identity,
- token profile approval still pending,
- bridge tooling not yet production-ready,
- possible public confusion around hashrate,
- possible public confusion around "asset" language,
- AI-generated workflows requiring human review,
- and no guarantee of adoption.

The project's answer is documentation, not denial.

If a fact is verified, record it.  
If a fact is pending, label it.  
If a claim sounds too exciting, slow down and add a source.

## 13. Conclusion

ProfitNet is an AI-first, Algorand-rooted, multichain Web3 experiment with a verified Base ERC-20 expansion.

Its current value is not a promise of price, yield, hashrate, or investment return. Its current value is operational: testing how AI, public documentation, token metadata, and cautious multichain workflows can work together without turning every update into a marketing fireworks show.

The professional version:

```text
PNET is a public token identity and coordination experiment.
It is not marketed as an investment asset.
It is not a hashrate claim.
It is not a yield product.
It is a testbed for AI-assisted Web3 operations and multichain learning.
```

The slightly funnier version:

```text
PNET is the project writing down what it is doing before the internet guesses for it.
```

That is a reasonable place to start.

## 14. Final Disclaimer

This document is informational and comedic in tone, but the boundaries are serious. It is not financial, legal, tax, investment, mining, or trading advice. It does not create rights to profit, revenue, hashrate, compute, liquidity, listings, bridge support, governance outcomes, or future value.

Anyone evaluating PNET should rely on public records, independent research, and qualified professional advice where appropriate.
