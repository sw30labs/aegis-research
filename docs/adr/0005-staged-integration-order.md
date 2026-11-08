# ADR-0005: Integrate in a fixed measurement order

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

Hardware-specific work could start immediately, but several software and evaluation preconditions are still unproven.

## Decision

Use this integration order:

1. Synthetic workflow on existing hardware.
2. Per-action policy gate and evidence manifest.
3. Adversarial boundary tests and controlled shutdown.
4. Backend comparison with matched quality and workload.
5. Hardware-specific integration only after the prior measurements justify it.

## Consequences

- Positive: Later steps have explicit gates; E001–E006 map onto this sequence.
- Negative: Specialized hardware work is deferred, possibly for a long time if inference is not the bottleneck.

## Alternatives considered

- Parallel hardware prototyping from day one (not described; step 5 is explicit about waiting).
- Skip adversarial and shutdown tests (contradicted by step 3 and E002/E005/E006).

## Evidence

- `docs/ARCHITECTURE.md` (Integration order)
- `experiments/REGISTER.md`
- `c5a0cec70f5b9ed098c61fc333135bfeaa875fe4`
