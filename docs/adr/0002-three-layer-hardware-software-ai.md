# ADR-0002: Frame the research question as three cooperating layers

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

Local inference hardware, policy software, and AI assistance could each be studied alone. The proposal is about whether they improve an authorized assessment workflow when integrated.

## Decision

State the research question as the convergence of three layers, each with a role and a demonstration burden:

- Hardware: local inference, isolation boundaries, operator controls, and device identity.
- Software: scope enforcement, tool mediation, evidence capture, and reproducible workflows.
- AI: propose actions, interpret evidence, and assist reporting, under a fixed evaluation with calibrated uncertainty and human review.

The useful outcome is a reproducible assessment with clear authorization, evidence, and operator control. Token throughput is an intermediate metric, not the goal.

## Consequences

- Positive: Evaluation cannot declare success from a faster model alone.
- Negative: The thesis is harder to test than a single-layer experiment; many open questions remain (workload, model/license, isolation boundary, update path).

## Alternatives considered

- Treat AEGIS as primarily an inference-hardware project (rejected by H1 and the "why it matters" section: end-to-end improvement may be small when tools or review dominate).
- Treat AEGIS as primarily an agent framework (rejected by the hardware and enforcement layers).

## Evidence

- `README.md` (three-layer table; research question)
- `RESEARCH.md` (Question; Hypotheses H1–H4; Why it matters)
- `c5a0cec70f5b9ed098c61fc333135bfeaa875fe4`
