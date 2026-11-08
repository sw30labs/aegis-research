# Architecture Decision Records

Retrospective ADRs for aegis-research, written 2026-11-08 from default branch `c5a0cec` after a full read of every tracked file (12 files, single commit). Format: PorterForcesAI ADR format. Open questions are in [../assumptions.md](../assumptions.md).

| ADR | Title |
|---|---|
| [0001](0001-research-proposal-not-implementation.md) | Publish AEGIS as a research proposal, not an implementation |
| [0002](0002-three-layer-hardware-software-ai.md) | Frame the research question as three cooperating layers |
| [0003](0003-enforcement-outside-the-model.md) | Keep policy, tool brokerage, and stop control outside the model |
| [0004](0004-commodity-hardware-first.md) | Start on commodity local hardware; specialized silicon must earn its place |
| [0005](0005-staged-integration-order.md) | Integrate in a fixed measurement order |
| [0006](0006-network-modes-not-airgap.md) | Distinguish offline analysis from restricted assessment networking |
| [0007](0007-signed-manifests-not-distributed-ledger.md) | Prove runs with signed manifests; add a distributed ledger only if needed |
| [0008](0008-mcp-is-not-containment.md) | Treat MCP as a tool interface, not a sandbox or authorization guarantee |
| [0009](0009-agent-count-is-experimental.md) | Treat the number of agents as an experimental variable and keep a serial baseline |
| [0010](0010-planned-experiment-register.md) | Pre-register planned experiments instead of filling results after the fact |
| [0011](0011-e001-synthetic-bottleneck-baseline.md) | Make AEGIS-E001 a synthetic, known-answer bottleneck baseline |
| [0012](0012-all-rights-reserved-working-name.md) | Keep this edition all-rights-reserved and treat AEGIS as a working name |
| [0013](0013-sourced-claim-boundaries.md) | Bound every external citation and refuse unsupported commercial claims |
| [0014](0014-synthetic-authorized-scope-only.md) | Restrict scope to synthetic data and explicitly authorized targets |
| [0015](0015-research-engine-and-related-projects.md) | Follow the SW30 research engine and treat sibling repos as connections, not integrations |
