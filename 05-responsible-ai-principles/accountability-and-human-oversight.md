# Accountability and Human Oversight

*[Home](../INDEX.md) › [05 · Responsible AI Principles](../05-responsible-ai-principles/accountability-and-human-oversight.md)*

## What accountability means for AI

Clear, traceable ownership for an AI system's behavior. Someone (a role, not just "the algorithm") who is answerable for its outcomes, can explain decisions, and has the authority and mechanism to intervene.

## Elements of accountability

- **Ownership**: every Tier 1/2 AI system has a named accountable owner (see [01-foundations/stakeholder-roles.md](../01-foundations/stakeholder-roles.md))
- **Traceability**: decisions/actions can be reconstructed after the fact (logs, versioning of models/prompts/data)
- **Contestability**: affected individuals can challenge/appeal an AI-driven decision, with a human review path
- **Redress**: a process exists to correct errors and remediate harm, not just acknowledge them

## Human oversight models

| Model | Description | Appropriate for |
|---|---|---|
| Human-in-the-loop | Human approves before an action/decision takes effect | High-risk decisions, high-autonomy agent actions |
| Human-on-the-loop | Human monitors and can intervene/override in real time, but doesn't pre-approve every action | Medium-risk, higher-volume systems |
| Human-in-command | Humans retain the ability to disable/override the system entirely, oversight is at the system-design level rather than per-decision | Lower-risk, well-validated systems |

Choice of model should match the risk tier from [03-ai-governance/risk-management.md](../03-ai-governance/risk-management.md) — higher risk and higher autonomy should push toward human-in-the-loop.

## Agentic AI: this principle is the crux

Agentic systems are exactly where "who is accountable when the system acts autonomously" gets tested. Practical mechanisms:
- Explicit approval gates before irreversible or high-stakes actions (financial transactions, external communications, production changes)
- Scoped permissions so the agent literally cannot take actions outside its accountable owner's sign-off (least privilege, [07-agentic-ai/tool-use-and-permissions.md](../07-agentic-ai/tool-use-and-permissions.md))
- Kill switches and the ability to pause/roll back an agent's autonomous operation
- Clear escalation: what happens when the agent is uncertain or encounters an out-of-scope situation; default should be "ask a human," not "guess and proceed"

## Avoiding "accountability laundering"

A common failure: an AI system's output is treated as if it removes human judgment from a decision ("the model said so"), diffusing accountability. Counter this by requiring human reviewers to genuinely evaluate AI-assisted outputs, not rubber-stamp them, and by measuring/monitoring override rates as a governance signal — near-zero overrides can indicate rubber-stamping rather than a great model.

## Documentation

Accountability is only real if it's traceable: tie this principle to [04-ai-assurance/evidence-and-traceability.md](../04-ai-assurance/evidence-and-traceability.md) (model cards, action logs) and to the incident response process ([incident-response.md](../02-ai-lifecycle/incident-and-remediation.md)).
