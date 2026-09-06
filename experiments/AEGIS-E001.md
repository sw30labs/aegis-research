# AEGIS-E001 — Workflow bottleneck baseline

Status: planned. Protocol draft 1. No harness or measured run yet.

## Hypothesis
Inference time may be a material portion of a small AI-assisted assessment workflow. A faster backend is valuable only if overall completion time improves at acceptable correctness and review effort.

## Minimal workload
Use synthetic local artifacts and known-answer tasks: summarize a configuration, identify deliberately planted policy inconsistencies, and draft a finding that cites the supplied evidence. Do not scan live third-party infrastructure. Freeze the artifact set, expected outcomes and scoring rubric before execution.

## Conditions
Compare a deterministic/serial reference where applicable with one local AI-assisted workflow. Record hardware, model hash/version, prompt, context size, quantization, decoding, tool versions and warm/cold state. Repeat tasks with recorded seeds where supported; document nondeterminism.

## Measurements
Collect total time and separate inference, tool, queue and human-review time. Record task correctness, unsupported findings, abstentions, failures, review corrections and energy when measurable. Missing energy measurements remain unknown.

## Gate
Before the confirmatory run, choose the minimum useful time improvement and maximum acceptable quality regression. Report raw per-task values and uncertainty. If inference is not the bottleneck, modify the hardware hypothesis rather than replacing the metric with tokens per second.

## Output
Write a run manifest, raw timing/score records, analysis and a kill / modify / reproduce / promote decision under results/AEGIS-E001/<run-id>/. No result files are currently supplied.
