# Memory and State Risk

*[Home](../INDEX.md) › [07 · Agentic AI](../07-agentic-ai/agent-incident-response.md)*

## Why persistent memory adds risk

Agents with memory (conversation history, learned facts about users, task state across sessions) accumulate data and behavior patterns over time, in ways that create risks distinct from stateless single-turn Gen AI.

## Specific risks

### Sensitive data accumulation
Memory can silently accumulate personal or sensitive information disclosed across many interactions, without an explicit collection event that would normally trigger privacy review. Creating a de facto profile the organization may not have properly assessed under privacy obligations. See [05-responsible-ai-principles/privacy-and-data-protection.md](../05-responsible-ai-principles/privacy-and-data-protection.md).

### Stale or incorrect belief persistence
Once an agent "learns" something (a fact, a preference, a corrected instruction) into memory, it may continue acting on it even after it's no longer true or was itself an error, without a clear mechanism for the information to be re-verified or expire.

### Memory poisoning
Deliberately feeding an agent false information designed to be stored in memory and influence future behavior — a persistence-based variant of prompt injection with a longer-lived effect than a single-session attack.

### Cross-user/cross-context leakage
Shared memory stores that aren't properly partitioned can leak one user's data into another user's session, especially in systems where memory architecture wasn't designed with multi-tenancy in mind from the start.

### Right to deletion/correction
Individuals' rights to access, correct, or delete their data (under GDPR/DPDP-style regimes) extend to what's stored in agent memory. This needs to be technically feasible, not just a policy statement, which requires memory architecture that supports targeted deletion.

## Governance practices

- **Retention policy for agent memory**: define how long memory persists, what triggers expiration, and who owns the policy; don't let memory accumulate indefinitely by default
- **Explicit vs. implicit memory writes**: prefer memory that's written based on clear signals (an explicit user statement or confirmation) over inferred/implicit memory that's harder to audit or correct
- **User visibility and control**: where feasible, let users see and edit/delete what an agent has "remembered" about them
- **Memory partitioning**: strict isolation between users/tenants/contexts, tested explicitly, not assumed from application-layer logic alone
- **Verification before acting on stored memory** for high-stakes decisions: treat memory as a prior, not ground truth, and re-verify critical facts rather than blindly trusting stale stored state
- **Audit trail**: log what was written to memory, when, and from what interaction, to support incident investigation and deletion requests

## Related

- [multi-agent-governance.md](multi-agent-governance.md)
- [13-implementation-playbooks/agentic-deployment-checklist.md](../13-implementation-playbooks/agentic-deployment-checklist.md)
