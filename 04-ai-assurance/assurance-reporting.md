# Assurance Reporting

## Purpose

How assurance findings (from validation, audit, red-teaming, and impact/risk assessments) get communicated to the people who need to act on them — governance board, executive leadership, and, where required, regulators.

## Audiences and content

| Audience | What they need | Cadence |
|---|---|---|
| System owner | Detailed findings and remediation actions for their system | Immediately on completion |
| Governance board | Summary findings, risk implications, approval/hold recommendation | At each Tier 1 gate, plus periodic portfolio review |
| Executive leadership | Aggregate risk posture across the AI portfolio, material findings, trend over time | Quarterly or per governance cadence |
| Regulators | Specific compliance evidence per applicable regulation (e.g., serious incident reports, conformity documentation) | As legally required |
| Customers/public (where applicable) | Transparency reports, high-level assurance statements | As committed to (e.g., annual transparency report) |

## Report structure (working template)

1. **Scope**: system(s)/process assessed, assessment type (validation/audit/red-team/impact assessment)
2. **Methodology**: what was tested and how, including independence level ([independent-assessment.md](independent-assessment.md))
3. **Findings**: by severity, with evidence references
4. **Risk implications**: how findings map to the risk register ([AI-risk-assessment.md](AI-risk-assessment.md))
5. **Remediation status**: what's fixed, what's in progress, what's accepted risk (with sign-off)
6. **Recommendation**: proceed / proceed with conditions / hold

## Portfolio-level reporting

Beyond individual system reports, aggregate reporting across the full AI inventory (open findings by severity, systems overdue for re-validation, incident trends) gives leadership and the governance board a view of overall risk posture — this is often more useful for resourcing and prioritization decisions than any single system's report.

## Escalation

Critical findings (active exploitable vulnerability, confirmed rights-impacting bias, regulatory non-compliance) should have a defined fast-path escalation to governance leadership and, where relevant, legal — not wait for the next scheduled reporting cycle.

## Related

- [03-ai-governance/ai-governance-board.md](../03-ai-governance/ai-governance-board.md)
- [02-ai-lifecycle/incident-and-remediation.md](../02-ai-lifecycle/incident-and-remediation.md)
