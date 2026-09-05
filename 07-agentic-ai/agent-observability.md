# Agent Observability

*[Home](../INDEX.md) › [07 · Agentic AI](../07-agentic-ai/agent-incident-response.md)*

## Why standard application monitoring isn't enough

Agents make decisions and take variable, sometimes unpredictable sequences of actions; observability needs to cover not just "is the system up," but "is the agent doing what it's supposed to, within its intended scope, reliably."

## What to instrument

### Action-level telemetry
Every tool call/action: what was called, with what parameters, what was returned, whether it succeeded, and what triggered it (which step in the agent's plan). This is the foundation for both debugging and audit, see [04-ai-assurance/evidence-and-traceability.md](../04-ai-assurance/evidence-and-traceability.md).

### Decision/reasoning traces
Where feasible, capture the agent's stated rationale for key decisions — useful for debugging and explainability, while remembering (per [planning-and-reasoning-risk.md](planning-and-reasoning-risk.md)) that stated reasoning isn't guaranteed to fully reflect actual decision drivers.

### Permission boundary events
Log both successful actions and *attempted* actions that were blocked by a permission/guardrail check. Attempted-but-blocked events are an early signal of either a misbehaving agent, a prompt injection attempt, or an overly narrow permission scope causing legitimate task friction.

### Escalation and approval events
Track when and why an agent escalated to a human, whether the human approved/denied/modified, and how long escalations sat before resolution: informs both safety and UX tuning.

### Outcome tracking
Task success/failure, not just individual action success — an agent can complete every individual tool call successfully while still failing the overall task.

## Alerting

- Anomalous action volume, value, or scope for a given agent/task type relative to baseline
- Spike in blocked/attempted-boundary-violation events
- Spike in escalations (could indicate a changed environment or an emerging edge case the agent wasn't designed for) or a drop to near-zero escalations after previously escalating regularly (could indicate a guardrail silently failing open)
- Task success rate degradation

## Dashboards and review

- Real-time operational dashboard for on-call/system owners
- Periodic (e.g., weekly) human review of a representative sample of full action logs, not just aggregate metrics; qualitative review catches failure modes that don't trip any predefined alert
- Governance-board-level rollup for Tier 1 agentic systems, feeding into [04-ai-assurance/assurance-reporting.md](../04-ai-assurance/assurance-reporting.md)

## Related

- [02-ai-lifecycle/monitoring-and-observability.md](../02-ai-lifecycle/monitoring-and-observability.md)
- [08-controls-and-techniques/monitoring-and-observability](../08-controls-and-techniques/monitoring-and-observability/README.md)
