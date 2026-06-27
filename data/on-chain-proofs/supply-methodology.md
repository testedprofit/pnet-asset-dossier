# PNET Supply Methodology

Status date: 2026-06-27
Status: Methodology draft. Burned, locked, vault, and circulating values remain `Needs verification` until proof packets exist.

## Purpose

This document defines how the dossier should calculate and label PNET supply categories.

## Verified Baseline

From [asset-identity-proof-2026-06-27.md](asset-identity-proof-2026-06-27.md):

| Field | Value | Status |
| --- | --- | --- |
| Raw total supply | `100000000000000` | Verified |
| Decimals | `6` | Verified |
| Display total supply | `100,000,000` PNET | Verified |

Formula:

```text
display_supply = raw_supply / 10^decimals
100,000,000 = 100000000000000 / 10^6
```

## Supply Categories

| Category | Definition | Evidence required | Current status |
| --- | --- | --- | --- |
| Total supply | Raw ASA total adjusted by decimals | ASA params from public indexer | Verified |
| Direct burned supply | PNET held by addresses or mechanisms proven unrecoverable by public evidence | transaction set, recipient address, methodology, reviewer | Needs on-chain verification |
| Inaccessible-account supply | PNET believed inaccessible because account access is claimed lost | account balance, public statement, methodology, reviewer; must be separated from direct burn | Needs methodology review |
| Locked supply | PNET held by reviewed lock, escrow, vault, or time-bound app | app ID, escrow address, source, terms, admin policy, unlock path | Needs on-chain verification |
| Circulating supply | Methodology-defined available supply after exclusions | formula, excluded accounts, proof files, capture date | Needs methodology review |
| Operational holdings | PNET held by disclosed operational wallet(s) | wallet proof, role, control model, movement policy | Needs role verification |
| LP/pool supply | PNET in liquidity pools | pool app IDs, pool addresses, LP token references, source | Needs on-chain verification |

## Direct Burn Calculation

Use this only when burn proof packets exist:

```text
direct_burned_supply = sum(PNET balances in verified burn addresses)
                     + sum(PNET amounts in verified unrecoverable burn transactions)
```

Required proof fields:

- burn address or transaction ID,
- reason it is considered unrecoverable,
- raw PNET amount,
- display PNET amount,
- source URL,
- capture date,
- reviewer.

## Locked Supply Calculation

Use this only when lock/vault proof packets exist:

```text
locked_supply = sum(PNET balances in verified lock/vault/escrow addresses)
```

Each excluded account must include:

- app ID or escrow address,
- lock source code or public lock mechanism,
- admin/update/delete status,
- unlock terms or time,
- current balance source,
- capture date,
- reviewer.

## Circulating Supply Calculation

No circulating supply value is currently verified by this dossier.

Future formula template:

```text
circulating_supply = total_supply
                   - direct_burned_supply
                   - verified_locked_supply
                   - excluded_operational_or_reserve_supply
```

Any exclusion must be justified with a proof packet. If a claim cannot be reproduced from public data, keep it `Needs verification`.

## Lost Creator Wallet Treatment

The user-provided claim that the original creator wallet is unavailable remains `Needs verification`.

Important distinction:

- Direct burned supply requires public on-chain evidence that tokens are unrecoverable.
- Inaccessible-account supply may be disclosed separately if there is a public methodology and reviewer sign-off.
- Do not combine inaccessible-account supply with direct burned supply unless counsel, reviewers, and methodology explicitly approve the category.

Current Gate Status: TOTAL SUPPLY VERIFIED; BURNED, LOCKED, CIRCULATING, AND INACCESSIBLE-ACCOUNT SUPPLY REMAIN NEEDS VERIFICATION.
