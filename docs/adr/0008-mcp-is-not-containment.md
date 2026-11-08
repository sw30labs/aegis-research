# ADR-0008: Treat MCP as a tool interface, not a sandbox or authorization guarantee

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

MCP is a convenient way to expose tools to an agent. The cited MCP security guidance itself says implementations must address authorization and protocol-specific risks.

## Decision

MCP may provide a tool interface. It is not itself a sandbox or authorization guarantee. A container likewise supplies one potential isolation layer, not a proof against host compromise. Compare isolation choices against the threat model rather than labeling every containerized or MCP-based design secure.

## Consequences

- Positive: Adopting MCP later would not be mistaken for completing H2 or the runtime-isolation tests.
- Negative: If MCP is used, a separate broker, scope check, and isolation boundary are still required.

## Alternatives considered

- Use MCP as the security architecture (rejected by `docs/ARCHITECTURE.md` and the MCP row in `docs/SOURCES.md`).
- Forbid MCP entirely (not stated; it is allowed as an interface).

## Evidence

- `docs/ARCHITECTURE.md` (Software)
- `docs/SOURCES.md` (MCP security best practices row)
- `c5a0cec70f5b9ed098c61fc333135bfeaa875fe4`
