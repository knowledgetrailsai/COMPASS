# Stakeholder Roles

Responsible AI fails when it's treated as one team's job. Below is a typical RACI-style breakdown; adapt titles to your org.

## Data scientists / ML engineers
Build and evaluate models; implement fairness/robustness testing; document model behavior and limitations; flag known risks to reviewers.

## Product managers
Define intended use cases and out-of-scope uses; own user-facing disclosure and consent flows; balance business goals against risk tolerance; escalate high-risk use cases for review.

## AI/ML platform or MLOps team
Build the guardrails, monitoring, and evaluation infrastructure that make RAI practices enforceable at scale rather than manual one-offs.

## Risk, compliance, and legal
Own regulatory mapping (section 08), review high-risk use cases, approve documentation (model cards, DPIAs), define escalation paths for incidents.

## AI governance board / council
Cross-functional body (product, legal, engineering, security, ethics) that reviews and approves high-risk AI use cases, sets organization-wide policy, and adjudicates edge cases. See [03-ai-governance/ai-governance-framework.md](../03-ai-governance/ai-governance-framework.md).

## Security team
Threat-models AI-specific attack surfaces (prompt injection, model extraction, tool-use abuse in agentic systems); integrates AI red-teaming into existing security practices.

## Executive sponsors
Set risk appetite, allocate resources for RAI tooling and review capacity, and are ultimately accountable for organizational AI incidents.

## End users and affected individuals
Not "owners" of the process, but the reason it exists — their right to disclosure, explanation, and recourse should shape every checkpoint above.

## RACI snapshot (illustrative)

| Activity | Data Science | Product | Legal/Compliance | Governance Board | Security |
|---|---|---|---|---|---|
| Risk tiering a new use case | C | R | C | A | I |
| Bias testing | R | I | C | I | I |
| Model card / documentation | R | C | A | I | I |
| High-risk use case approval | I | R | C | A | I |
| Red-teaming / adversarial testing | C | I | I | I | R |
| Incident response | R | C | A | I | R |

R = Responsible, A = Accountable, C = Consulted, I = Informed
