# Stage 6: Deployment & Release

*[Home](../INDEX.md) › [02 · AI Lifecycle](../02-ai-lifecycle/)*

## Purpose

Move from validated system to live production exposure in a way that limits blast radius if something was missed in evaluation, and ensures user-facing obligations (disclosure, consent) are live before anyone is exposed.

## Activities

- **Staged rollout**: shadow mode (system runs but doesn't affect real decisions/actions) → limited beta (small, monitored user group) → general availability. Each stage should have defined success criteria before progressing.
- **Guardrails live before traffic**: content/action filters, rate limits, and (for agents) permission enforcement must be active and tested in the production environment before any real user or action exposure — not enabled "after we see how it goes."
- **User-facing disclosure**: AI-interaction disclosure, AI-generated content labeling, and any required consent flows implemented and tested, not just documented as a requirement.
- **Kill switch verified in production**: confirm the rollback/pause mechanism actually works in the real deployment environment, not just in theory — see [07-agentic-ai/autonomy-and-control.md](../07-agentic-ai/autonomy-and-control.md).
- **Runbook and on-call readiness**: incident response plan ([incident-and-remediation.md](incident-and-remediation.md)) has a named on-call owner before launch, not assigned reactively during the first incident.
- **AI inventory update**: mark the system as live in the central registry with current risk tier, owner, and evaluation status.

## Deployment approval

Tier 1 systems require explicit governance sign-off to proceed past shadow/limited-beta stages. Tier 2–3 can typically proceed on standard release process with RAI checklist confirmation.

## Rollback criteria

Define, before launch, the specific conditions that trigger a rollback at each rollout stage (e.g., fairness metric deviation beyond X%, error rate above Y%, any Tier-1-severity incident) — deciding this during an actual incident, under pressure, produces worse decisions than deciding it in advance.

## Related

- [08-controls-and-techniques/guardrails-and-controls.md](../08-controls-and-techniques/guardrails-and-controls.md)
- [13-implementation-playbooks/genai-app-launch-checklist.md](../13-implementation-playbooks/genai-app-launch-checklist.md)
- [13-implementation-playbooks/agentic-deployment-checklist.md](../13-implementation-playbooks/agentic-deployment-checklist.md)
