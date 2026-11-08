# ADR-0009: Treat the number of agents as an experimental variable and keep a serial baseline

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

Multi-agent designs are a common default for "AI-assisted assessment," but they add coordination delay and failure surface.

## Decision

Use a minimal planner, broker, isolated runtime, and evidence store. The number of agents is an experimental variable rather than a fixed requirement. Preserve a serial or non-agentic baseline so AI-assisted runs have something to beat.

E001 compares a deterministic/serial reference, where applicable, with one local AI-assisted workflow.

## Consequences

- Positive: More agents cannot be declared better without measurement; H1's end-to-end comparison stays possible.
- Negative: The first harness has to implement at least two execution styles.

## Alternatives considered

- Fix a multi-agent topology in the architecture (rejected: agent count is an experimental variable).
- Skip a non-agentic baseline (rejected by `docs/ARCHITECTURE.md` and E001).

## Evidence

- `docs/ARCHITECTURE.md` (Software)
- `experiments/AEGIS-E001.md` (Conditions)
- `c5a0cec70f5b9ed098c61fc333135bfeaa875fe4`
