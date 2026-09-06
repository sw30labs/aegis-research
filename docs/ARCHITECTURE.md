# Proposed architecture

## Separate planes

The operator defines target scope, allowed task classes, duration, resource limits and approval rules. A policy controller validates a versioned scope artifact independently of the AI planner. The planner proposes structured actions; the tool broker validates each action against current scope and identity immediately before execution. Unknown scope or expired authorization blocks execution.

The execution runtime reaches only authorized lab targets. Evidence and results return through a controlled interface. Retrieved pages, tool output and target responses are untrusted input; they cannot alter authorization. Evidence export is a distinct reviewed action.

## Hardware and inference

Start with a commodity local backend. A later specialized ASIC, GPU or other accelerator implements the inference interface, not the policy authority. Record exact model revision, quantization, context limit, decoding configuration and backend. Changing any of these creates a new evaluation condition.

Physical stop controls, watchdogs, secure boot and device identities are candidate design elements. Each needs a defined enforcement path, failure mode and test. A stop control should revoke new execution and address in-flight work; a hardware switch that only updates software state may not supply independent containment.

A modular inference board may ease replacement, but electrical, thermal, firmware and driver compatibility must be demonstrated. Low-rank adapter support is backend-specific; adapters cannot be assumed portable across unrelated base-model architectures. No chip interface or vendor supply agreement is specified here.

## Software

Use a minimal planner, broker, isolated runtime and evidence store. The number of agents is an experimental variable rather than a fixed requirement. More agents can increase coordination delay and failure surface. Preserve a serial or non-agentic baseline.

MCP can provide a tool interface; it is not itself a sandbox or authorization guarantee. A container supplies one potential isolation layer, not a proof against host compromise. Compare isolation choices against the threat model rather than labeling every containerized design secure.

## Network modes

An offline analysis mode can process approved local artifacts without network access. An assessment mode may require a restricted connection to an authorized target network. The latter is network-isolated or constrained, not literally air-gapped from all other systems. Describe each interface and export route explicitly.

## Provenance

Record hashes and versions for models, adapters, data, prompts, tools, policy, runtime image and configuration. Sign a run manifest and preserve raw evidence plus the interpretation that used it. Define signer identity, key custody, clock assumptions and retention. A signed false statement remains false; a hash proves content identity, not benign behavior.

Begin with a signed append-only record and verify its actual tamper properties. Introduce a distributed ledger only if a multi-party trust requirement justifies it. Hashing training inputs does not guarantee deterministic training or prove that fabricated hardware implements specified weights; those require separate validation.

## Integration order

1. Synthetic workflow on existing hardware.
2. Per-action policy gate and evidence manifest.
3. Adversarial boundary tests and controlled shutdown.
4. Backend comparison with matched quality and workload.
5. Hardware-specific integration only after the prior measurements justify it.
