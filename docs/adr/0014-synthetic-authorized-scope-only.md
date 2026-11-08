# ADR-0014: Restrict scope to synthetic data and explicitly authorized targets

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

The subject is authorized security assessment. A public repo in that neighborhood can be mistaken for exploit tooling or a place to send customer data.

## Decision

Scope the work to an operator-owned test environment with synthetic data and explicitly authorized targets. This repository provides no exploitation tooling. Deployment security has not been validated.

Contributors must not submit customer data, credentials, private correspondence, proprietary vendor material, or unauthorized target information; they should use synthetic reproductions.

The first experiment forbids scanning live third-party infrastructure. Legal and contractual applicability must be evaluated for a specific deployment; this edition does not make blanket regulatory assertions.

Independence is stated explicitly: this is an SW30 Labs proposal; no employer, customer, chip vendor, or other organization is represented as a partner or sponsor.

## Consequences

- Positive: The public tree stays on the legal and ethical side of assessment research.
- Negative: Real-world assessment conditions are out of scope until a later, separately authorized edition.

## Alternatives considered

- Include offensive tooling or live-target recipes (contradicted by the threat-model scope and E001).
- Accept customer or proprietary material as feedback (forbidden by `CONTRIBUTING.md`).

## Evidence

- `docs/THREAT-MODEL.md` (opening scope; closing legal paragraph)
- `CONTRIBUTING.md`
- `experiments/AEGIS-E001.md` ("Do not scan live third-party infrastructure.")
- `README.md` (independence statement)
- `c5a0cec70f5b9ed098c61fc333135bfeaa875fe4`
