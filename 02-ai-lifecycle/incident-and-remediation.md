# AI Incident Response

## What counts as an AI incident

Any event where an AI system caused, or nearly caused, harm: biased/discriminatory decisions, hallucinated content presented as fact, data leakage, agent taking an unauthorized or harmful action, security exploit (prompt injection leading to data exfiltration), or significant public/regulatory complaint.

## Response phases

### 1. Detect
Sources: automated monitoring alerts (drift, guardrail triggers, anomalous agent actions), user reports, internal QA, security monitoring, media/social monitoring for public-facing systems.

### 2. Triage & classify
- Severity (harm caused/potential, number of people affected, reversibility)
- Scope (single user vs. systemic — check if the same model/prompt/config is used elsewhere)
- Whether the system should be paused immediately (kill switch — see [07-agentic-ai/autonomy-and-control.md](../07-agentic-ai/autonomy-and-control.md) for agentic systems)

### 3. Contain
- Disable or roll back the specific feature/model/agent capability
- For agentic systems: revoke tool permissions or pause autonomous execution pending investigation
- Preserve logs/evidence before any rollback destroys them

### 4. Investigate
- Reconstruct root cause using action logs, model card, and evaluation history
- Determine whether this was a known/accepted limitation, a novel failure mode, or a governance process gap

### 5. Remediate
- Fix (retrain, adjust prompts/guardrails, tighten tool permissions, add a missing eval)
- Re-run relevant evaluation suite before re-enabling
- Update documentation (model/system card, known limitations)

### 6. Communicate
- Internal: governance board, affected teams
- External: affected users/customers per legal/regulatory obligation (breach notification timelines vary by jurisdiction — see [10-regulations-and-standards](../10-regulations-and-standards/))
- Regulators, where required (e.g., serious incident reporting for high-risk systems under the EU AI Act)

### 7. Post-incident review
Blameless review: what failed (technical control, process, or judgment call), what would have caught it earlier, what changes to governance/tooling are needed. Feed findings back into [13-implementation-playbooks](../13-implementation-playbooks/) checklists.

## Severity matrix (illustrative)

| Severity | Definition | Response time |
|---|---|---|
| SEV1 | Widespread harm, safety/legal exposure, agent took irreversible unauthorized action | Immediate — pause system, executive notification |
| SEV2 | Contained harm, single user or small group, reversible | Same business day |
| SEV3 | Near-miss, no realized harm, or minor quality issue | Standard bug-fix cycle, logged for trend analysis |

## Readiness checklist

- Kill switch/rollback mechanism exists and is tested for every Tier 1 system
- On-call ownership defined for AI incidents (who gets paged)
- Escalation path to legal/compliance defined in advance, not improvised during an incident
