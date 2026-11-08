# ADR-0003: Keep policy, tool brokerage, and stop control outside the model

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

An AI planner that proposes assessment actions can be steered by untrusted target content. A fast model, a container, a signature, or a physical switch alone does not establish an enforcement boundary.

## Decision

Separate planes:

- The operator defines target scope, allowed task classes, duration, resource limits, and approval rules.
- A policy and approval controller validates a versioned scope artifact independently of the AI planner.
- The planner proposes structured actions; a tool broker validates each action against current scope and identity immediately before execution.
- Unknown scope or expired authorization blocks execution.
- An independent stop control acts on the broker.
- Retrieved pages, tool output, and target responses are untrusted input and cannot alter authorization.
- Evidence export is a distinct reviewed action.

Hypothesis H2 is that a policy controller outside the model can reject out-of-scope actions, including those proposed after untrusted content is read.

## Consequences

- Positive: Authorization is not delegated to model behavior; rejected requests can be logged and tested (E002).
- Negative: The design needs an independent broker and stop path, so a "just run the agent" prototype would not satisfy the proposal.

## Alternatives considered

- Rely on the model to stay in scope (rejected by the threat model row "Untrusted content to planner" and H2).
- Treat a container or a signature as sufficient containment (explicitly rejected in the README architecture note and `docs/ARCHITECTURE.md`).

## Evidence

- `README.md` (mermaid diagram; "Every execution path needs an enforcement boundary.")
- `docs/ARCHITECTURE.md` (Separate planes)
- `docs/THREAT-MODEL.md` (operator/controller, content-to-planner, planner-to-broker, stop-control rows)
- `RESEARCH.md` (H2)
- `c5a0cec70f5b9ed098c61fc333135bfeaa875fe4`
