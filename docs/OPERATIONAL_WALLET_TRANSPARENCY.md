# PNET Operational Wallet Transparency

Status date: 2026-06-27
Wallet: `CIVTUU6KLTYO26SPVEBDFBKP3UMZM2DPEO5RINODUVCI5NVIFC6HVNWS7E`
Status: Public balance snapshot recorded; role and control model remain `Needs verification`.

## Current Evidence

See [operational-wallet-proof-2026-06-27.md](../data/on-chain-proofs/operational-wallet-proof-2026-06-27.md).

At capture round `62554271`, Algonode Indexer showed:

| Field | Observed value |
| --- | --- |
| Valid Algorand address | `true` |
| PNET raw balance | `15583379085` |
| PNET display balance | `15,583.379085` PNET |
| Account status | `Offline` |
| Total created apps | `34` |
| Total created assets | `1` |

## What Is Verified

- The address is syntactically valid.
- The account exists on Algorand MainNet.
- The account held `15,583.379085` PNET at the capture round.

## What Is Not Verified

- Official project role.
- Wallet controller identity.
- Control model.
- Security setup.
- Whether created apps are official PNET/ProfitNet apps.
- Whether the wallet is treasury, operational, personal, or mixed-use.
- Whether any funds are locked, reserved, or committed.

## Required Maintainer Disclosure

Before this wallet is used in public diligence:

- confirm exact address,
- define role,
- define movement policy,
- define disclosure cadence,
- identify any related app IDs,
- identify whether control is single-sig or multisig,
- define security review status,
- record reviewer and date.

## Safe Public Wording

Use:

> The user-provided operational wallet is listed for transparency. A dated public indexer snapshot records its PNET balance at capture time. Its role, control model, and official status remain `Needs verification` until a maintainer disclosure and public review are complete.

Do not use:

- guaranteed treasury,
- locked treasury,
- strategic reserve,
- official multisig,
- audited wallet,
- burn wallet,
- vault wallet,
- exchange wallet,

unless separately verified.

Current Gate Status: OPERATIONAL WALLET SNAPSHOT RECORDED; ROLE AND CONTROL MODEL REMAIN NEEDS VERIFICATION.
