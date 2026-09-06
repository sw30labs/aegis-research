# Threat model and research boundaries

Scope: an operator-owned test environment with synthetic data and explicitly authorized targets. This repository provides no exploitation tooling. Deployment security has not been validated.

| Boundary | Failure to investigate | Proposed control and test |
|---|---|---|
| Operator to controller | Expired, altered or overly broad scope | Validate identity, scope revision and expiration; reject altered fixtures |
| Untrusted content to planner | Instructions embedded in target data redirect work | Treat content as data; test broker rejection independently of model behavior |
| Planner to tool broker | Model requests an unauthorized action | Per-action allowlist and independent approval check; record rejected requests |
| Runtime to host/network | Escape, unintended egress or access to unrelated files | Isolate runtime and restrict interfaces; assess the chosen boundary explicitly |
| Evidence to report | Fabricated, incomplete or misattributed evidence | Link claims to immutable run artifacts; human review and negative controls |
| Update to execution | Model, adapter or tool changes after approval | Bind approval to artifact identity and invalidate on change |
| Stop control to work queue | Queued or in-flight work continues after revocation | Test cancellation, queue drain and state preservation under failure |
| Audit path | Full disk, lost signer or unavailable log | Define fail-closed behavior for actions requiring an audit record |

Assess behavior using measured evidence. Model origin or nationality is not a substitute for testing, and no finite test suite proves absence of hidden behavior. TSLIT may contribute scoped experiments; it cannot issue a universal “clean model” guarantee.

No compliance certification, hardware containment guarantee, military endorsement or proof of zero data leakage is claimed. Legal and contractual applicability must be evaluated for a specific deployment; this research edition does not make blanket regulatory assertions.
