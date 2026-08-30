# Stage 7: Monitoring & Observability

*[Home](../INDEX.md) › [02 · AI Lifecycle](../02-ai-lifecycle/lifecycle-overview.md)*

## Purpose

Verify the system continues to behave as validated once it's operating on real, evolving, real-world data and users — evaluation is a point-in-time check; monitoring is continuous.

## What to monitor

- **Performance drift**: accuracy/quality metrics degrading over time as real-world data diverges from training/validation data
- **Fairness drift**: subgroup outcome metrics re-checked on a regular cadence, not just at launch — representation and behavior of the user population can shift
- **Gen AI**: hallucination rate, groundedness, guardrail trigger rate, user feedback/complaint signals
- **Agentic AI**: task success rate, permission-boundary violations (even attempted ones), escalation rate and appropriateness, action volume/value against expected baselines — see [07-agentic-ai/agent-observability.md](../07-agentic-ai/agent-observability.md)
- **Security signals**: anomalous input patterns consistent with prompt injection or jailbreak attempts, unusual tool-call patterns
- **Operational health**: latency, uptime, error rates — standard reliability monitoring, but tied to RAI thresholds (e.g., a fallback triggering more than expected may indicate an upstream data/model issue)

## Monitoring infrastructure

- Dashboards visible to the accountable owner and, for Tier 1 systems, to the governance board
- Automated alerting tied to pre-defined thresholds (from [deployment-and-release.md](deployment-and-release.md) rollback criteria) rather than relying on manual review to catch drift
- Sampling-based human review of real outputs/actions on a regular cadence, even for high-volume automated systems — automated metrics alone miss qualitative failure modes

## Feedback loops

User reports and complaint channels should route back to the accountable owner and inform both immediate triage ([incident-and-remediation.md](incident-and-remediation.md)) and periodic re-evaluation.

## Periodic re-validation

Even without a triggering incident, Tier 1 systems should undergo full re-evaluation against original fairness/safety benchmarks on a defined cadence (e.g., annually, or after significant usage-pattern shifts) — monitoring catches acute problems; periodic re-validation catches slow drift that stays under alert thresholds.

## Related

- [08-controls-and-techniques/monitoring-and-observability](../08-controls-and-techniques/monitoring-and-observability/README.md)
- [04-ai-assurance/audit.md](../04-ai-assurance/audit.md)
