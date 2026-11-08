# ADR-0001: Publish AEGIS as a research proposal, not an implementation

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

The repository presents a hardware-plus-software-plus-AI idea for governed security assessment. A reader could mistake a public GitHub tree with architecture diagrams for a product, appliance, or benchmark suite.

## Decision

Ship this edition as a research proposal only: architecture, testable hypotheses, and experiment protocols. Include no appliance implementation, custom chip design, trained model, installation command, or measured AEGIS performance results. Keep `results/` as an empty placeholder until a real run exists.

## Consequences

- Positive: The public record matches what is actually available and avoids implying a working product.
- Negative: There is nothing to install or reproduce yet; evaluation of the thesis has to wait for a later harness.

## Alternatives considered

- Publish a prototype or harness in the same commit (no evidence this was attempted; README says there is no implementation to install).
- Omit a results directory until data exists (rejected in favor of a placeholder that states no results are available).

## Evidence

- `README.md` (Status: research proposal; "No installation command is provided because there is no implementation to install.")
- `results/README.md`
- `experiments/AEGIS-E001.md` ("No harness or measured run yet.")
- `c5a0cec70f5b9ed098c61fc333135bfeaa875fe4`
