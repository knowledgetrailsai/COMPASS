# Case Study Template

Every case study in this section should follow this structure so cases are comparable and machine-readable as knowledge, not just narrative stories. Per [00-navigation-and-methodology/source-and-evidence-policy.md](../00-navigation-and-methodology/source-and-evidence-policy.md), factual claims should be sourced (Tier 4: documented, verifiable events) and clearly separated from interpretation.

```markdown
# [Case Name]

**Context**: Organization/sector, what the AI system was for, when this occurred.

**AI system**: Type (traditional ML / Gen AI / Agentic AI), what it did.

**What happened**: Factual account of the incident, sourced.

**Root cause**: What technical/process/governance failure led to this — distinguish confirmed cause from analysis/inference.

**Risk category**: Map to [01-foundations/risk-taxonomy.md](../01-foundations/risk-taxonomy.md).

**Lifecycle stage where it could have been caught**: Map to [02-ai-lifecycle](../02-ai-lifecycle/) stages.

**Control failure**: Which control (per [08-controls-and-techniques](../08-controls-and-techniques/)) was missing, inadequate, or not followed.

**Impact**: Who/what was affected, scale, reversibility.

**Regulatory implications**: Any enforcement action, fine, or regulatory response — sourced.

**Lessons learned**: What this means for practice.

**Preventive controls**: Specific controls that would have prevented or mitigated this, cross-referenced to [08-controls-and-techniques](../08-controls-and-techniques/) and [13-implementation-playbooks](../13-implementation-playbooks/).

**Sources**: Full citations.
```

## Categories in this section

| Folder | Focus |
|---|---|
| [failures/](failures/) | General AI system failures not fitting a more specific category |
| [regulatory-actions/](regulatory-actions/) | Cases resulting in regulatory enforcement |
| [security-incidents/](security-incidents/) | Security-specific AI incidents |
| [bias-and-discrimination/](bias-and-discrimination/) | Fairness failures |
| [privacy-incidents/](privacy-incidents/) | Privacy/data leakage failures |
| [hallucination-and-reliability/](hallucination-and-reliability/) | Gen AI factual/reliability failures |
| [agentic-failures/](agentic-failures/) | Agentic AI-specific incidents |
| [good-practices/](good-practices/) | Positive examples worth emulating |

## Using case studies

Reference these during [02-ai-lifecycle/requirements-and-design.md](../02-ai-lifecycle/requirements-and-design.md) (to inform risk identification) and [04-ai-assurance/red-teaming.md](../04-ai-assurance/red-teaming.md) (to inform test scenarios) — real precedent is often more persuasive to stakeholders than an abstract risk description.
