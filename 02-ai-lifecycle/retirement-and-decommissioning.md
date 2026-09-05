# Stage 9: Retirement & Decommissioning

*[Home](../INDEX.md) › [02 · AI Lifecycle](../02-ai-lifecycle/lifecycle-overview.md)*

## Purpose

Responsibly wind down an AI system, an often-skipped stage that leaves orphaned data, stale access grants, and unclear accountability if not handled deliberately.

## Activities

- **Decommissioning plan**: define the shutdown timeline, migration path for any affected users/processes, and communication plan
- **Data handling**: delete or archive training data, logs, and (for agentic systems) accumulated memory per retention policy; don't let decommissioned-system data linger indefinitely by default
- **Access revocation**: remove any standing credentials, tool access, or API keys associated with the system, especially for agentic systems with tool permissions
- **User communication**: notify affected users where the system's removal impacts them materially, particularly if it was involved in decisions with ongoing effect (e.g., an active recommendation or eligibility system)
- **AI inventory update**: mark the system as retired, with retirement date and reason, in the central registry ([03-ai-governance/ai-governance-framework.md](../03-ai-governance/ai-governance-framework.md)) — the inventory should reflect what's actually running, not accumulate stale entries
- **Knowledge preservation**: retain the model/system card, evaluation history, and incident record for the organization's institutional memory (useful if a similar system is built later, or if questions arise post-retirement) even after the live system is gone

## Common failure modes

- Decommissioning the user-facing feature but leaving the underlying model/agent with live credentials and tool access running unmonitored
- Losing institutional knowledge of why a system was retired, leading a future team to repeat the same design mistake
- Retention of training/log data past its lawful basis once the original purpose (operating the system) no longer applies

## Related

- [04-ai-lifecycle/incident-and-remediation.md](incident-and-remediation.md) if retirement is incident-driven
- [05-responsible-ai-principles/privacy-and-data-protection.md](../05-responsible-ai-principles/privacy-and-data-protection.md)
