# Autonomy and Control

*[Home](../INDEX.md) › [07 · Agentic AI](../07-agentic-ai/)*

## Autonomy levels (a practical scale)

| Level | Description | Example |
|---|---|---|
| L0 — Suggest | Agent proposes an action; human performs it manually | Drafts an email for a human to send |
| L1 — Approve | Agent prepares an action; human must explicitly approve before execution | Agent stages a code change; human clicks merge |
| L2 — Monitor | Agent executes autonomously within pre-approved bounds; human monitors and can intervene | Agent auto-responds to routine support tickets, human reviews a sample |
| L3 — Autonomous with exceptions | Agent executes autonomously; escalates to human only for defined edge cases/thresholds | Agent processes refunds under $50 automatically, escalates above that |
| L4 — Fully autonomous | Agent operates without routine human checkpoints | Reserved for very low-risk, well-validated, reversible tasks only |

**Guidance**: match autonomy level to the risk tier ([03-ai-governance/risk-management.md](../03-ai-governance/risk-management.md)) and to action reversibility. Irreversible or high-value actions (financial transactions, external communications, production system changes, anything affecting a person's rights/access) should default to L0–L1 until the agent has a substantial track record and the organization has robust monitoring in place — and even then, high-stakes categories often stay at L1 permanently as a policy choice, not just a maturity stage.

## Key control mechanisms

### Approval gates
Explicit human sign-off required before specific action types execute — should be based on action category/impact, not a blanket "review everything" (which degrades into rubber-stamping) or "review nothing."

### Scoped permissions (least privilege)
The agent's credentials/tool access should be the minimum needed for its task, time-boxed where possible, and distinct from a human operator's full permission set. See [tool-use-and-permissions.md](tool-use-and-permissions.md).

### Circuit breakers / kill switches
A tested, reliable mechanism to immediately pause or stop an agent's autonomous operation — at the individual agent level and, ideally, at a system-wide level for a given agent type/deployment. Test this like you'd test a production rollback, not just document it.

### Rate and scope limits
Bound how much an agent can do in a given time window (number of actions, monetary value, number of affected records) so a malfunctioning or manipulated agent has a capped blast radius even before a human notices.

### Escalation on uncertainty
Default behavior when the agent is uncertain, encounters an unexpected state, or receives conflicting/ambiguous instructions should be to pause and ask a human — not to guess and proceed. This should be an explicit design requirement, tested in evaluation.

## Anti-patterns to avoid

- Granting broad, standing tool access "to be safe/flexible" rather than scoping to the task
- Treating a system prompt instruction ("only do X") as a security control instead of a suggestion the model might not reliably follow
- Approval fatigue: routing so many low-stakes approvals to humans that reviewers stop reading them carefully, defeating the purpose
- No tested rollback: discovering during an actual incident that the kill switch doesn't fully stop in-flight actions

## Related

- [tool-use-and-permissions.md](tool-use-and-permissions.md)
- [13-implementation-playbooks/agentic-deployment-checklist.md](../13-implementation-playbooks/agentic-deployment-checklist.md)
