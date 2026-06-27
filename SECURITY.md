# Security Policy

## Scope

This is a documentation and media repository. It should not contain executable code, wallet logic, signer logic, transaction logic, private keys, mnemonics, API keys, secrets, or `.env` files.

## Reporting Issues

Report documentation errors, suspicious links, incorrect metadata, or asset impersonation concerns through GitHub issues for this repository when public disclosure is appropriate.

For sensitive reports, use an official private contact channel controlled by the testedprofit / Profitnet brand. That contact channel is not verified in this repository. Needs verification.

## Sensitive Material Policy

Do not commit:

- Private keys
- Mnemonics or seed phrases
- API keys or bearer tokens
- `.env` files
- Wallet files
- Signer configuration
- Custody instructions
- Transaction-building logic

If sensitive material is accidentally committed, rotate or revoke the exposed secret immediately and remove it from repository history using a standard secret-removal process.

## Verification Safety

When verifying asset facts, use read-only public sources. This repository should not ask anyone to connect a wallet, sign a transaction, transfer assets, or grant account permissions.

