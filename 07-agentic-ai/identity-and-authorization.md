# Identity and Authorization for Agents

## Why this is becoming fundamental

An agent isn't just producing an answer — it can act on behalf of a user or organization. That means an agent needs an identity the rest of your systems can recognize, and an authorization model that determines what it's allowed to do under that identity — the same category of problem as human identity and access management, but with new failure modes because the "user" can be manipulated by its inputs.

## Agent identity models

| Model | Description | Risk profile |
|---|---|---|
| **Acts as itself** | Agent has its own service identity/credentials, distinct from any human | Clear attribution, but requires careful permission scoping since there's no natural human accountability tied to each action |
| **Acts on behalf of a user** | Agent inherits/exercises a specific human's permissions (delegated authority) | Actions are attributable to the user, but the agent could take actions the user didn't specifically intend within their permission scope |
| **Acts on behalf of the organization** | Agent has organization-level credentials not tied to a specific human | Hardest to attribute individual actions; needs the strongest independent logging and oversight |

Most production agentic systems should default to the delegated-user model with tightly scoped, time-boxed permissions, reserving organization-level identity for narrowly scoped, well-monitored automation.

## Authorization principles

- **Least privilege**: the agent's effective permissions should be the minimum needed for its task — see [tool-use-and-permissions.md](tool-use-and-permissions.md)
- **Explicit delegation, not implicit inheritance**: don't let an agent silently inherit a user's full permission set because it's acting "on their behalf" — define exactly which of the user's permissions are delegated to the agent for a given task
- **Time-boxed grants**: authorization should expire with the task/session rather than persisting indefinitely
- **Re-authentication for step-up actions**: high-stakes actions (large financial transactions, permission changes, irreversible operations) should require fresh, explicit authorization even mid-session, not rely on authorization granted at session start
- **Non-repudiation**: every agent action should be logged with enough identity and context information to establish, after the fact, who/what authorized it and why

## Multi-agent identity

In systems where agents delegate to other agents, authorization should not silently propagate at full scope — each delegation should be its own explicit, scoped grant, auditable independently. See [multi-agent-governance.md](multi-agent-governance.md).

## Standards and patterns to watch

Emerging protocols and patterns for agent identity/authorization (OAuth-style delegated authorization adapted for agents, agent-specific identity providers) are an active area of development — treat this as a fast-evolving space and revisit vendor/architecture choices periodically rather than assuming today's pattern is final.

## Related

- [tool-use-and-permissions.md](tool-use-and-permissions.md)
- [autonomy-and-control.md](autonomy-and-control.md)
- [05-responsible-ai-principles/accountability-and-human-oversight.md](../05-responsible-ai-principles/accountability-and-human-oversight.md)
