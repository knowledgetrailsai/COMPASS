# AI Audit

## Purpose

Periodic, systematic review of AI systems and governance processes already in production — verifies that approved controls are still in place and effective, not just that they were correctly designed at launch.

## Types of audit

### System audit
Reviews a specific AI system's current behavior, documentation currency, and control effectiveness against what was approved at launch. Checks for drift between documented and actual behavior.

### Governance process audit
Reviews whether the governance framework itself ([03-ai-governance](../03-ai-governance/)) is being followed consistently — are risk tiers being assigned correctly, is the AI inventory complete and current, are approvals being properly documented?

### Compliance audit
Reviews specific regulatory obligations ([10-regulations-and-standards](../10-regulations-and-standards/)) for evidence of ongoing compliance, often ahead of or in response to a regulatory inquiry.

## Audit scope and cadence

| System tier | Audit frequency |
|---|---|
| Tier 1 | Annually at minimum, plus triggered by material change or incident |
| Tier 2 | Every 1–2 years, or sampled |
| Tier 3 | Sampled periodically as part of governance process audit, not individually |

## Audit process

1. **Scope definition**: which systems/processes, against which requirements
2. **Evidence gathering**: pull documentation, logs, monitoring data, prior evaluation/red-team reports — see [evidence-and-traceability.md](evidence-and-traceability.md)
3. **Testing**: verify claims against actual evidence (e.g., re-run a sample of fairness tests rather than trusting the original report alone)
4. **Findings**: documented gaps between required and actual state, with severity ratings
5. **Remediation tracking**: findings assigned owners and deadlines, tracked to closure — an audit finding that's never remediated is a governance failure in itself
6. **Reporting**: findings summarized for governance board and, where relevant, leadership — see [assurance-reporting.md](assurance-reporting.md)

## Internal vs. external audit

Internal audit (by a function independent of the system owners) is the workhorse for regular cadence; external audit adds credibility for regulatory response, customer trust requirements, or after a significant incident. See [independent-assessment.md](independent-assessment.md) for the independence principles that apply equally here.

## Relationship to certification

Audits supporting a management-system certification (e.g., ISO/IEC 42001) follow the certifying body's specific audit methodology — see [09-tools-and-frameworks](../09-tools-and-frameworks/) — in addition to, not instead of, an organization's own internal audit practice.
