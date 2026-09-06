# Experiment register

All experiments are **planned**. IDs identify proposals, not completed work.

| ID | Question | Controls and evidence | Decision |
|---|---|---|---|
| AEGIS-E001 | Where is time spent in a small authorized workflow? | Fixed synthetic tasks; serial baseline; component timings, reviewed correctness and configuration | Continue hardware exploration only if inference is a material bottleneck |
| AEGIS-E002 | Does independent policy enforcement block out-of-scope proposals? | Benign/denied fixtures, altered scope, stale approval and untrusted-input cases; rejection logs | Fix any tested boundary failure before expanding execution |
| AEGIS-E003 | Can a reviewer reconstruct every reported finding? | Signed manifests, intentionally missing/altered evidence and blind review | Modify provenance design when reconstruction fails |
| AEGIS-E004 | Do backend changes improve end-to-end performance at comparable quality? | Same tasks and scoring; exact model/backend revisions; latency, energy, cost and failures | Promote a backend only on whole-workflow evidence |
| AEGIS-E005 | Are updates and interruption recoverable? | Artifact mutation, power/process interruption, revoked scope, full audit store | Require bounded restart and invalidation of stale approvals |
| AEGIS-E006 | Does a physical control supply independent enforcement? | Simulated bypass attempts and controlled failure injection on a future test device | Record exact hardware guarantee and residual paths; no extrapolation from software-only tests |

Predeclare numeric acceptance thresholds once a concrete workload and baseline exist. Do not invent favorable results to populate this register.
