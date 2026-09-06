# Research record

## Question
Does integrating inference hardware, policy-enforced software and AI assistance improve a defined authorized assessment workflow relative to a conventional local baseline?

## Hypotheses

- H1: Local inference can reduce inference delay while preserving task quality. End-to-end improvement may be small when tool execution or human review dominates.
- H2: A policy controller outside the model can reject out-of-scope actions in the tested threat model, including actions proposed after untrusted content is read.
- H3: Versioned artifacts and signed manifests can improve reconstruction of what ran and what evidence supported a finding. They do not establish model safety or finding correctness.
- H4: A replaceable inference backend can keep the system maintainable as models and hardware change. Specialized silicon must earn its cost and reduced flexibility through measurement.

## Why it matters
The useful outcome is a reproducible assessment with clear authorization, evidence and operator control. Token throughput is an intermediate metric.

## Experiment
Start with AEGIS-E001 on existing hardware and synthetic tasks. Subsequent protocols are in the experiment register. Fix criteria and the evaluation set before confirmatory runs.

## Success and failure criteria
Compare end-to-end time, correct completed tasks, false findings, unsupported statements, blocked actions, review burden, energy and total operational cost. Do not call a faster but less reliable run an improvement. Record invalid runs separately from negative findings.

## Evidence
No AEGIS experimental results yet. External vendor announcements and other projects’ results are background, not AEGIS validation.

## Current conclusion
The integration is plausible enough to formulate tests. Its benefit and enforceability remain unproven.

## Open questions
Which workload? Which model and license? Which isolation boundary? Which update path? What part of runtime is actually inference-bound? How are lost authorization, logging failure and operator absence handled?

## Next experiment
Implement the smallest E001 reference harness. Stop or modify the hardware thesis if the measured bottleneck is elsewhere.
