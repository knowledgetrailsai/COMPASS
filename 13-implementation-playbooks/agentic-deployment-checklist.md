# Playbook: Agentic AI Deployment Checklist

*[Home](../INDEX.md) › [13 · Implementation Playbooks](../13-implementation-playbooks/agentic-deployment-checklist.md)*

## Scoping and design
- [ ] Autonomy level explicitly chosen and justified for this task ([07-agentic-ai/autonomy-and-control.md](../07-agentic-ai/autonomy-and-control.md))
- [ ] Tool/action allowlist defined, default deny ([07-agentic-ai/tool-use-and-permissions.md](../07-agentic-ai/tool-use-and-permissions.md))
- [ ] Agent identity/authorization model defined (acts as itself / on behalf of user / on behalf of org) ([07-agentic-ai/identity-and-authorization.md](../07-agentic-ai/identity-and-authorization.md))
- [ ] Least-privilege, time-boxed credentials issued, distinct from any human operator's

## Safety controls
- [ ] Action validation (schema/allowlist check) implemented before every tool call executes
- [ ] Human approval gates defined for high-stakes action categories
- [ ] Escalation-on-uncertainty behavior implemented and tested, not left to default model behavior ([07-agentic-ai/planning-and-reasoning-risk.md](../07-agentic-ai/planning-and-reasoning-risk.md))
- [ ] Kill switch implemented and tested in the actual production environment ([07-agentic-ai/autonomy-and-control.md](../07-agentic-ai/autonomy-and-control.md))
- [ ] Rate/value/scope limits set per action type

## Multi-agent (if applicable)
- [ ] Roles and boundaries defined per agent ([07-agentic-ai/multi-agent-governance.md](../07-agentic-ai/multi-agent-governance.md))
- [ ] System-level circuit breaker exists, not just per-agent
- [ ] Attributable logging for inter-agent delegation

## Memory (if applicable)
- [ ] Retention policy defined for agent memory ([07-agentic-ai/memory-and-state-risk.md](../07-agentic-ai/memory-and-state-risk.md))
- [ ] Deletion/correction mechanism technically feasible, not just policy
- [ ] Memory partitioning tested for multi-tenant isolation

## Evaluation
- [ ] Scripted task suite covering realistic complexity, not just simple demos ([07-agentic-ai/agentic-evaluation.md](../07-agentic-ai/agentic-evaluation.md))
- [ ] Adversarial testing: prompt injection via tool outputs, permission-boundary probing ([04-ai-assurance/red-teaming.md](../04-ai-assurance/red-teaming.md))
- [ ] Recovery/error-handling behavior tested under injected tool failures

## Observability
- [ ] Action-level telemetry implemented ([07-agentic-ai/agent-observability.md](../07-agentic-ai/agent-observability.md))
- [ ] Alerting on anomalous action volume/scope and blocked-action spikes
- [ ] Sampling-based human review of action logs scheduled

## Human-agent interaction
- [ ] Agent status/capability clearly visible to operators ([07-agentic-ai/human-agent-interaction.md](../07-agentic-ai/human-agent-interaction.md))
- [ ] Approval requests carry sufficient context for genuine review
- [ ] Interruptibility verified

## Governance and incident readiness
- [ ] Risk tier assigned with autonomy/action-scope weighted appropriately ([03-ai-governance/risk-management.md](../03-ai-governance/risk-management.md))
- [ ] Agent-specific incident response plan in place ([07-agentic-ai/agent-incident-response.md](../07-agentic-ai/agent-incident-response.md))
- [ ] Tier 1: governance board sign-off obtained
