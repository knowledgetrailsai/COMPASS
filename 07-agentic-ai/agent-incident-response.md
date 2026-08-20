# Agent Incident Response

*[Home](../INDEX.md) › [07 · Agentic AI](../07-agentic-ai/)*

## How this differs from general AI incident response

[02-ai-lifecycle/incident-and-remediation.md](../02-ai-lifecycle/incident-and-remediation.md) covers the general AI incident process. Agentic incidents add urgency and specific containment steps because the system may still be actively taking actions while the incident is being triaged.

## Immediate containment priorities

1. **Stop further action, not just alert**: the first response to a suspected agentic incident should be pausing/halting the specific agent (or agent type/deployment) via the kill switch ([07-agentic-ai/autonomy-and-control.md](autonomy-and-control.md)) — an agent that's actively misbehaving continues causing harm every additional minute it runs.
2. **Preserve action logs before any rollback**: agent action logs are the primary evidence for root-causing what happened — ensure they're captured/exported before any cleanup or rollback activity that might affect logging systems.
3. **Assess in-flight and completed actions**: determine what the agent already did (not just what it was about to do) — irreversible actions taken before containment need separate remediation from the underlying cause.
4. **Revoke/rotate credentials if compromise is suspected**: if the incident involves suspected prompt injection or credential misuse, treat it as a security incident requiring credential rotation, not just a behavior bug.

## Triage questions specific to agentic incidents

- Was this a single malfunctioning agent instance, or a systemic issue affecting all agents using this model/prompt/tool configuration?
- Was the trigger internal (model error, planning failure) or external (prompt injection, manipulated tool output, compromised credential)?
- What is the full scope of actions taken during the incident window, across all affected agent instances?
- Did the agent's guardrails/permission checks function as designed but prove insufficient, or did they fail outright?

## Remediation specific to agentic systems

- Tighten permission scope or add missing action validation before resuming
- Add the failure scenario to the adversarial red-team suite ([04-ai-assurance/red-teaming.md](../04-ai-assurance/red-teaming.md)) to prevent regression
- Review whether the autonomy level was appropriate for the task ([autonomy-and-control.md](autonomy-and-control.md)) — many agentic incidents are, at root, an autonomy-level-vs-risk mismatch rather than a pure technical bug
- Notify affected parties if the agent took actions with real-world consequences on their behalf (a financial transaction, a communication sent, data modified)

## Post-incident

Feed findings into [agentic-evaluation.md](agentic-evaluation.md) test suites and update the agent's action-log review sampling rate temporarily post-incident to build confidence before returning to standard monitoring cadence.

## Related

- [02-ai-lifecycle/incident-and-remediation.md](../02-ai-lifecycle/incident-and-remediation.md)
- [agent-observability.md](agent-observability.md)
