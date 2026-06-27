# PNET On-Chain Proof Package

Status date: 2026-06-27

Purpose: maintain source-linked, dated proof records for PNET on-chain claims.

This folder is the evidence layer for claims that appear in the whitepaper, tokenomics files, deployment registry, and public review materials.

## Rules

- Do not mark a claim `Verified` unless the proof file includes source URL, capture date, capture round when available, observed value, method, and reviewer.
- Use `Needs verification` when evidence is incomplete.
- Use `Needs methodology review` when a value exists but the calculation method is not established.
- Do not publish wallet screenshots, private wallet notes, recovery details, signer locations, private keys, mnemonics, API keys, cookies, or `.env` files.
- Do not infer lock, vault, burn, or operational-wallet role from labels alone.

## Current Proof Files

| File | Purpose | Status |
| --- | --- | --- |
| [asset-identity-proof-2026-06-27.md](asset-identity-proof-2026-06-27.md) | ASA identity, supply, decimals, control fields, creation transaction | Verified by Algonode and Nodely indexers at capture round |
| [operational-wallet-proof-2026-06-27.md](operational-wallet-proof-2026-06-27.md) | Dated public snapshot of user-provided operational wallet | Address and balance snapshot verified; role/control status needs human verification |
| [supply-methodology.md](supply-methodology.md) | Methodology for total, circulating, burned, locked, and inaccessible-account supply | Methodology draft; burn/lock/vault values need proof |
| [burn-lock-vault-worklist.md](burn-lock-vault-worklist.md) | Worklist for burn, lock, vault, LP, and allocation proof packets | Active worklist |
| [proof-index.json](proof-index.json) | Machine-readable proof index | Draft |
| [templates/transaction-proof-template.md](templates/transaction-proof-template.md) | Template for future transaction proof packets | Ready |

## Status Summary

| Claim area | Current status |
| --- | --- |
| ASA identity | Verified by public indexers |
| Total supply and decimals | Verified by public indexers |
| Current manager/reserve/freeze/clawback fields | Verified by public indexers as zero address |
| Asset creation transaction | Verified by public indexer |
| Operational wallet address validity | Verified as valid Algorand address |
| Operational wallet current PNET balance | Snapshot only |
| Operational wallet project role/control model | Needs human verification |
| Burned supply | Needs on-chain verification |
| Locked supply | Needs on-chain verification |
| Vault/LP labels | Needs on-chain verification |
| Lost creator wallet access status | Needs human and methodology verification |

Current Gate Status: ON-CHAIN PROOF PACKAGE STARTED; BURN/LOCK/VAULT CLAIMS REMAIN BLOCKED UNTIL TRANSACTION SETS AND METHODOLOGY ARE COMPLETE.
