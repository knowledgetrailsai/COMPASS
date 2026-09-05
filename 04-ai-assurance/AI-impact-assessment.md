# AI Impact Assessment

*[Home](../INDEX.md) › [04 · AI Assurance](../04-ai-assurance/assurance-overview.md)*

## Purpose

A structured, documented assessment of an AI system's potential impact on individuals, groups, and society — broader than a privacy-focused DPIA, covering fairness, rights, safety, and societal effects. Sometimes called an Algorithmic Impact Assessment (AIA).

## When required

Tier 1 systems (per [03-ai-governance/risk-management.md](../03-ai-governance/risk-management.md)), public-sector AI, and any system materially affecting access to opportunity, rights, or safety.

## Assessment structure

1. **System description**: purpose, intended use, out-of-scope use, technology type (traditional ML/Gen AI/Agentic AI)
2. **Affected parties**: direct users, indirect/non-user affected individuals, particularly vulnerable groups
3. **Potential impacts**: for each affected party, assess against the risk taxonomy ([01-foundations/risk-taxonomy.md](../01-foundations/risk-taxonomy.md)): fairness, privacy, safety, autonomy/rights
4. **Severity and likelihood scoring**: consistent with [03-ai-governance/risk-management.md](../03-ai-governance/risk-management.md) tiering criteria
5. **Mitigations**: controls applied to reduce each identified impact, and residual risk after mitigation
6. **Human rights considerations**: for Tier 1 systems, explicit review against [01-foundations/human-rights-and-ai.md](../01-foundations/human-rights-and-ai.md)
7. **Stakeholder input**: where feasible, input from representatives of affected groups, not solely internal assessment
8. **Sign-off**: accountable owner and, for Tier 1, governance board approval

## Relationship to DPIA

A DPIA (Data Protection Impact Assessment) is a legally-defined subset focused specifically on personal data risk under privacy law (GDPR-style regimes, India's DPDP Act). An AI Impact Assessment is broader. Where both are required, conduct the DPIA as a component of the fuller AI Impact Assessment rather than as a wholly separate exercise, to avoid duplicated effort and inconsistent conclusions.

## Output

A signed-off impact assessment document, retained as an assurance artifact ([evidence-and-traceability.md](evidence-and-traceability.md)), referenced in any later audit or incident investigation.

## Related

- [AI-risk-assessment.md](AI-risk-assessment.md), the risk-scoring methodology this assessment draws on
- [13-implementation-playbooks/conducting-an-ai-risk-assessment.md](../13-implementation-playbooks/conducting-an-ai-risk-assessment.md) — step-by-step working version
