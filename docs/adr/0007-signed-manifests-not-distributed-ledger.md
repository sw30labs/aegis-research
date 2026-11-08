# ADR-0007: Prove runs with signed manifests; add a distributed ledger only if needed

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

Reconstructing what ran, and what evidence supported a finding, is part of the thesis (H3, E003). A public blockchain or similar ledger is a tempting default for "tamper evidence."

## Decision

Record hashes and versions for models, adapters, data, prompts, tools, policy, runtime image, and configuration. Sign a run manifest and preserve raw evidence plus the interpretation that used it. Define signer identity, key custody, clock assumptions, and retention.

Begin with a signed append-only record and verify its actual tamper properties. Introduce a distributed ledger only if a multi-party trust requirement justifies it.

A signed false statement remains false; a hash proves content identity, not benign behavior. Hashing training inputs does not guarantee deterministic training or prove that fabricated hardware implements specified weights.

## Consequences

- Positive: Provenance can start without a multi-party ledger; H3 is scoped (artifacts improve reconstruction, they do not prove model safety or finding correctness).
- Negative: Key custody, clocks, and retention become part of the design; a full disk or lost signer must fail closed for actions that require an audit record.

## Alternatives considered

- Start with a distributed ledger (rejected unless a multi-party trust requirement appears).
- Treat hashes or signatures as proof of correctness or model safety (explicitly rejected).

## Evidence

- `docs/ARCHITECTURE.md` (Provenance)
- `RESEARCH.md` (H3)
- `docs/THREAT-MODEL.md` (Evidence to report; Audit path)
- `experiments/REGISTER.md` (AEGIS-E003)
- `c5a0cec70f5b9ed098c61fc333135bfeaa875fe4`
