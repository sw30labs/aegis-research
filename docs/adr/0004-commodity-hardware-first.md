# ADR-0004: Start on commodity local hardware; specialized silicon must earn its place

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

The proposal mentions specialized inference silicon (and cites vendor material about model-specific chips) but has no device, supply agreement, or measured bottleneck yet.

## Decision

Begin with a software reference on existing local hardware. A later specialized ASIC, GPU, or other accelerator may implement the inference interface, not the policy authority. Specialized silicon is a candidate backend only if measurements justify integration and update costs. Changing model revision, quantization, context limit, decoding configuration, or backend creates a new evaluation condition.

Hypothesis H4: a replaceable inference backend keeps the system maintainable; specialized silicon must earn reduced flexibility through measurement.

## Consequences

- Positive: Hardware spend and lock-in wait for evidence that inference is the bottleneck (E001, E004).
- Negative: Early work will not demonstrate the full appliance thesis.

## Alternatives considered

- Lead with a custom chip or vendor partnership (no chip interface or vendor agreement is specified; NOTICE.md disclaims partnership).
- Treat vendor throughput claims as AEGIS validation (rejected by `docs/SOURCES.md` and `results/README.md`).

## Evidence

- `README.md` (Start small)
- `docs/ARCHITECTURE.md` (Hardware and inference; Integration order steps 1 and 5)
- `RESEARCH.md` (H1, H4; Next experiment)
- `docs/SOURCES.md` (Taalas row: vendor-reported, no AEGIS benchmark or partnership)
- `c5a0cec70f5b9ed098c61fc333135bfeaa875fe4`
