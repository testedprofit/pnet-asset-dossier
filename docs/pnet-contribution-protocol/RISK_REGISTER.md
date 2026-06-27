# PNET Community Contribution Protocol Risk Register

Version: 1.0
Date: 2026-06-27
Status: MVP / TestNet candidate. Not MainNet. Not audited.

This register tracks identified risks for the PNET Community Contribution Protocol, their likelihood, impact, mitigation status, and owner.

## Risk Table

| ID | Risk Category | Description | Likelihood | Impact | Risk Level | Mitigation / Status | Owner |
| --- | --- | --- | --- | --- | --- | --- | --- |
| R01 | Regulatory / Legal | Claims around the protocol could be misinterpreted as investment products, yield-bearing instruments, payout systems, or token-value promises. | Medium | High | High | Strict public claims policy drafted. No yield/staking/passive-income framing allowed. Professional legal/public-claims review required before public launch. | Project Lead |
| R02 | Smart Contract | Bugs in credit assignment, gifting, external-activity recording, rejection logging, or local-state accounting. | Medium | High | High | Unit tests, static checks, and artifact hashes completed for MVP. Live TestNet tests and professional audit remain pending. App update/delete disabled for MVP. | Dev Team |
| R03 | Verification Process | Manual review process could be subjective, inconsistent, or hard to reproduce. | Medium | Medium | Medium | Verification process documented. Reviewer criteria, reason codes, and receipt hashes required. Community/multisig review is future work. | Project Lead |
| R04 | Privacy | User activity data from compute participation or bandwidth-sharing evidence could be sensitive. | Low | Medium | Low | Only hashes and non-sensitive metadata should be recorded on-chain. Raw proofs, screenshots, payout values, private dashboards, and private account data must not be published in the dossier. | Dev Team |
| R05 | Operational | Early credit concentration or reviewer discretion could create perceived unfairness. | Medium | Medium | Medium | Credits are app-local access/reputation records only. Publish reviewer policy, limits, action codes, receipt hashes, and periodic review summaries. | Project Lead |
| R06 | User Experience | Users may misunderstand credits as having guaranteed financial value or token-equivalent value. | Medium | Medium | Medium | Disclaimers added to docs and frontend copy. Education-focused content and safe wording required before public release. | Project Lead |
| R07 | Technical Dependency | External services such as Kryptex-style or Honeygain / JumpTask-style tools may change interfaces, policies, or evidence formats. | Low | Low | Low | Protocol only records reviewed evidence hashes. It does not depend on these services for core contract logic. Service terms and evidence formats remain `Needs verification`. | Dev Team |
| R08 | Adoption | Low user participation could limit usefulness of contribution credits. | Medium | Low | Low | Support multiple external participation categories while keeping claims neutral. Measure opt-ins, reviewed submissions, accepted/rejected records, and credit usage. | Project Lead |
| R09 | Security | Unauthorized or abusive credit assignment by admin/partner accounts. | Low | High | Medium | Contract uses admin/partner access control and pause control. Partner list, limits, review policy, and on-chain actions must be public. Professional audit pending. | Dev Team |
| R10 | Documentation | Dossier, website, or deployment records could become stale or inconsistent. | Medium | Medium | Medium | Living documentation model with `CHANGELOG.md`, proof index, deployment registry, and regular review cadence. | Project Lead |
| R11 | MainNet Readiness | TestNet MVP could be mistaken for MainNet-ready infrastructure. | Medium | High | High | All docs must state TestNet candidate / not audited / MainNet blocked until deployment evidence, audit, legal review, and maintainer approval. | Project Lead |
| R12 | Evidence Integrity | Hashes may be recorded without enough public context to reproduce what was reviewed. | Medium | Medium | Medium | Public receipt metadata must include category, period code, reviewer, decision, evidence hash, account-reference hash, review hash, tx ID, and privacy status. | Dev Team |

## Risk Management Process

- Review this register before every major release, TestNet deployment, or public announcement.
- High and Critical risks must have mitigation plans before MainNet.
- Update risk status after TestNet deployment, external review, audit findings, policy changes, or major frontend changes.
- Do not downgrade a risk because a mitigation is planned. Downgrade only after evidence exists.
- Record material risk changes in `CHANGELOG.md`.

## MainNet Gate

MainNet remains blocked until:

- live TestNet deployment evidence is recorded,
- live TestNet tests pass,
- legal/public-claims review is complete,
- security review or professional audit is complete,
- admin/partner policy is published,
- emergency response process is documented,
- maintainer go/no-go decision is recorded.

Current Gate Status: RISK REGISTER DRAFTED; HIGH RISKS REMAIN OPEN UNTIL TESTNET EVIDENCE, AUDIT, AND LEGAL REVIEW ARE COMPLETE.
