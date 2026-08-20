# Monitoring and Observability Techniques

Implementation detail supporting [02-ai-lifecycle/monitoring-and-observability.md](../../02-ai-lifecycle/monitoring-and-observability.md) and [07-agentic-ai/agent-observability.md](../../07-agentic-ai/agent-observability.md).

## Drift detection techniques

- **Data drift**: statistical tests (e.g., population stability index, KL divergence) comparing production input distribution to training/validation distribution
- **Concept drift**: monitoring the relationship between inputs and correct outputs changing over time (harder to detect directly without ground truth; often inferred from proxy signals like user correction/override rates)
- **Output drift**: monitoring shifts in the model's output distribution itself, which can signal upstream data or behavior changes even without labeled ground truth

## Gen AI-specific monitoring

- Guardrail trigger rate over time (a rising rate can indicate either increasing adversarial probing or upstream data/prompt issues)
- Groundedness/citation-rate sampling in production, not just at evaluation time
- User feedback signals (thumbs up/down, explicit corrections) aggregated as a quality proxy

## Agentic-specific monitoring

See [07-agentic-ai/agent-observability.md](../../07-agentic-ai/agent-observability.md) for the full treatment — action-level telemetry, permission-boundary events, escalation tracking.

## Alerting design

- Threshold-based alerts tied to pre-defined acceptability bounds (set during [02-ai-lifecycle/deployment-and-release.md](../../02-ai-lifecycle/deployment-and-release.md)), not arbitrary statistical anomaly thresholds alone
- Route alerts to a named, accountable on-call owner — an alert no one is responsible for acting on isn't a control
- Tiered severity so low-signal noise doesn't drown out genuinely urgent alerts

## Sampling-based human review

Automated metrics miss qualitative failure modes (subtly wrong-but-plausible outputs, culturally inappropriate content, edge-case reasoning errors). Pair automated monitoring with a regular cadence of human review on a representative production sample — this is often where the most valuable "we didn't know this was happening" findings come from.

## Tooling

See [09-tools-and-frameworks/observability-tools.md](../../09-tools-and-frameworks/observability-tools.md).
