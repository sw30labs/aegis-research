# ADR-0010: Pre-register planned experiments instead of filling results after the fact

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

A public research repo can accumulate optimistic narrative without tests. The SW30 research engine asks for hypothesis → experiment → evidence → finding → kill / modify / reproduce / promote.

## Decision

Keep an experiment register whose IDs identify proposals, not completed work. All six entries (AEGIS-E001 through AEGIS-E006) are planned. Predeclare numeric acceptance thresholds once a concrete workload and baseline exist. Do not invent favorable results to populate the register. Invalid runs are recorded separately from negative findings. Do not call a faster but less reliable run an improvement.

## Consequences

- Positive: Success, failure, and "not yet run" are distinguishable; later results have a place to land (`results/AEGIS-E001/<run-id>/`).
- Negative: The public register currently shows intent only.

## Alternatives considered

- Write ADRs or marketing claims as if experiments had run (contradicted by `RESEARCH.md` Evidence and `results/README.md`).
- Leave experiments implicit in prose (rejected in favor of `experiments/REGISTER.md`).

## Evidence

- `experiments/REGISTER.md`
- `RESEARCH.md` (Success and failure criteria; Evidence; Current conclusion)
- `README.md` (SW30 Research Engine methodology)
- `results/README.md`
- `c5a0cec70f5b9ed098c61fc333135bfeaa875fe4`
