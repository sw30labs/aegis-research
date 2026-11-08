# ADR-0015: Follow the SW30 research engine and treat sibling repos as connections, not integrations

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

SW30 Labs already has projects that touch agentic security, OSCAL guardrails, drift measurement, and TSLIT. A new proposal could be read as wrapping those projects into one certified stack.

## Decision

Place AEGIS primarily under Agentic Security & Trust, with a cross-link to AI & Computing Systems. Use the SW30 Research Engine methodology: hypothesis → experiment → evidence → finding → kill / modify / reproduce / promote. Optimize for the rate at which ideas become evidence; failure is a result.

Related independent projects named in the README — agentic-ai-pentesting, OSCAL Skills Guardrails, DriftLab, and TSLIT-DSPy DGX — are research connections, not completed AEGIS integrations or certifications. TSLIT may later contribute scoped experiments; it cannot issue a universal "clean model" guarantee, and model origin or nationality is not a substitute for testing.

The conceptual README diagram is not a product render or a claim that hardware exists (`assets/README.md`).

## Consequences

- Positive: AEGIS can cite siblings without inheriting their results or implying a product integration.
- Negative: Readers must visit those other repos for their actual status; this edition does not compose them.

## Alternatives considered

- Present AEGIS as an integration or certification of the named projects (explicitly rejected).
- Rely on model provenance instead of behavioral tests (rejected by `docs/THREAT-MODEL.md`).

## Evidence

- `README.md` (Research connections; "Build a chapel, not a cathedral")
- `docs/THREAT-MODEL.md` (measured evidence; TSLIT limit)
- `assets/README.md`
- `c5a0cec70f5b9ed098c61fc333135bfeaa875fe4`
