# ADR-0011: Make AEGIS-E001 a synthetic, known-answer bottleneck baseline

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

The hardware thesis depends on inference being a material part of workflow time. That cannot be checked on undefined live targets without mixing scope, legality, and measurement problems.

## Decision

Define AEGIS-E001 as a planned protocol (draft 1), not a runnable benchmark:

- Use synthetic local artifacts and known-answer tasks: summarize a configuration, identify planted policy inconsistencies, and draft a finding that cites supplied evidence.
- Do not scan live third-party infrastructure.
- Freeze the artifact set, expected outcomes, and scoring rubric before execution.
- Separate inference, tool, queue, and human-review time from total time.
- Record correctness, unsupported findings, abstentions, failures, review corrections, and energy when measurable.
- Before a confirmatory run, choose the minimum useful time improvement and maximum acceptable quality regression.
- If inference is not the bottleneck, modify the hardware hypothesis rather than replacing the metric with tokens per second.

## Consequences

- Positive: The first test is lawful, repeatable, and aimed at the actual hardware claim.
- Negative: Synthetic tasks may not represent later authorized assessments; energy may remain unknown.

## Alternatives considered

- Start with live third-party scans (explicitly forbidden in E001 and the threat-model scope).
- Optimize for tokens per second (explicitly rejected as a substitute metric).

## Evidence

- `experiments/AEGIS-E001.md`
- `experiments/REGISTER.md` (AEGIS-E001 row)
- `RESEARCH.md` (Next experiment)
- `c5a0cec70f5b9ed098c61fc333135bfeaa875fe4`
