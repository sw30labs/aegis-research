# ADR-0006: Distinguish offline analysis from restricted assessment networking

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

An assessment appliance might be described as "air-gapped," which overstates isolation if it must reach an authorized target network or export evidence.

## Decision

Define two modes:

- Offline analysis: process approved local artifacts without network access.
- Assessment mode: may require a restricted connection to an authorized target network. That mode is network-isolated or constrained, not literally air-gapped from all other systems.

Describe each interface and export route explicitly. The execution runtime reaches only authorized lab targets; evidence returns through a controlled interface.

## Consequences

- Positive: Claims about isolation have to name interfaces instead of using "air-gapped" as a slogan.
- Negative: Assessment mode still has an egress/export surface that must be threat-modeled.

## Alternatives considered

- Claim a universal air gap (explicitly rejected in `docs/ARCHITECTURE.md`).
- Allow general internet access during assessment (not described; runtime is limited to authorized lab targets).

## Evidence

- `docs/ARCHITECTURE.md` (Network modes; Separate planes)
- `docs/THREAT-MODEL.md` (Runtime to host/network)
- `c5a0cec70f5b9ed098c61fc333135bfeaa875fe4`
