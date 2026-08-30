# Playbook: Model / System Card Template

*[Home](../INDEX.md) › [13 · Implementation Playbooks](../13-implementation-playbooks/agentic-deployment-checklist.md)*

Working template implementing [04-ai-assurance/evidence-and-traceability.md](../04-ai-assurance/evidence-and-traceability.md).

```markdown
# Model/System Card: [Name]

## Overview
- Purpose and intended use
- Out-of-scope / not-recommended uses
- Technology type: traditional ML / Gen AI / Agentic AI
- Owner (accountable system owner)
- Risk tier

## Model/System Details
- Architecture / base model (and version)
- Training data summary (link to datasheet)
- Fine-tuning details, if applicable (link to fine-tuning governance record)
- For Gen AI: RAG corpus description, if applicable
- For Agentic AI: tools/permissions granted, autonomy level

## Evaluation Results
- Performance metrics (aggregate and by relevant subgroup)
- Fairness testing results and methodology used
- Robustness/adversarial testing summary
- Gen AI: hallucination rate, groundedness score
- Agentic AI: task success rate, permission-compliance rate under adversarial testing
- Red-team summary (findings, remediation status)

## Known Limitations
- Documented failure modes
- Populations/scenarios where performance is weaker
- Conditions under which the system should not be relied upon

## Human Oversight
- Oversight model (human-in-the-loop / on-the-loop / in-command)
- Escalation/approval gate design, if applicable

## Monitoring
- Metrics tracked in production
- Review cadence

## Governance
- Approval date and approving body
- Applicable regulations reviewed
- Next scheduled re-evaluation date

## Version History
- Version, date, summary of change, re-evaluation status
```

## Usage notes

- Complete this progressively during [02-ai-lifecycle/model-development.md](../02-ai-lifecycle/model-development.md) rather than retroactively at launch
- Update on every material change, not just at initial creation
- For Gen AI/agentic systems with frequent prompt/tool changes, keep a lightweight changelog section rather than requiring a full card rewrite each time
