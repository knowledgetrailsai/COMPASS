# Multi-Agent Governance

*[Home](../INDEX.md) › [07 · Agentic AI](../07-agentic-ai/agent-incident-response.md)*

## Why multi-agent systems need distinct governance

When multiple agents interact — delegating subtasks, negotiating, competing for shared resources, or supervising one another — behavior can emerge that isn't predictable from any single agent's design. Governance needs to address the system, not just each component.

## Specific risks

### Emergent behavior
Interaction effects (agents reinforcing each other's errors, unexpected coordination or competition dynamics) that weren't explicitly designed and may not appear in single-agent testing.

### Miscommunication and error propagation
One agent's incorrect output becomes another agent's trusted input, propagating and potentially amplifying errors across the system without an opportunity for correction — similar to cascading failure in [agentic-risk-landscape.md](agentic-risk-landscape.md) but across agent boundaries rather than within one agent's steps.

### Responsibility diffusion
When an outcome results from several agents' combined actions, accountability (see [05-responsible-ai-principles/accountability-and-human-oversight.md](../05-responsible-ai-principles/accountability-and-human-oversight.md)) can become unclear — design systems so each agent's actions are individually attributable and logged, even within a larger orchestrated workflow.

### Resource contention and conflicting goals
Agents pursuing individually reasonable sub-goals can conflict at the system level (e.g., two agents both trying to "optimize" a shared resource in incompatible ways).

### Collusion or unintended cooperation
In systems where agents interact with agents from other organizations (e.g., negotiation, marketplace agents), unintended cooperative or adversarial dynamics can arise that no single party fully controls or anticipated.

## Governance practices

- **Define clear roles and boundaries** for each agent in a multi-agent system — what it owns, what it can request from other agents, what it cannot do unilaterally
- **Central orchestration with oversight**, rather than fully decentralized peer-to-peer agent negotiation, for higher-risk workflows — an orchestrator/supervisor pattern makes monitoring and control tractable
- **System-level evaluation**, not just per-agent evaluation — test the full multi-agent workflow end-to-end, including adversarial and edge-case scenarios, before trusting individual agent-level test results
- **Circuit breakers at the system level**: the ability to halt the entire multi-agent workflow, not just one agent, when anomalous behavior is detected
- **Attributable logging**: every inter-agent message and action logged with clear attribution, enabling reconstruction of how an outcome emerged
- **Bounded interaction**: limit the number of interaction rounds/delegation depth to prevent runaway loops or unbounded resource consumption

## When to prefer a single-agent design

If a task can be reliably accomplished by a single, well-scoped agent, the added complexity, cost, and governance burden of a multi-agent architecture may not be justified. Reserve multi-agent designs for genuinely decomposable tasks where specialization provides clear value.

## Related

- [tool-use-and-permissions.md](tool-use-and-permissions.md)
- [agentic-evaluation.md](agentic-evaluation.md)
