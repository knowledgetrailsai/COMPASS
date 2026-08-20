# Governance Models

*[Home](../INDEX.md) › [03 · AI Governance](../03-ai-governance/)*

## Centralized vs. federated vs. hybrid

| Model | Description | Fits |
|---|---|---|
| **Centralized** | One central AI governance function reviews and approves all material AI use cases | Smaller orgs, early-maturity AI adoption, or highly regulated industries needing consistent control |
| **Federated** | Business units/product teams own governance within a central policy framework, with central function handling only Tier 1 review | Larger orgs with mature, distributed AI development |
| **Hybrid** | Central function sets policy, risk tiering, and reviews Tier 1; business units self-certify Tier 2–3 against the shared framework | Most common in practice — balances consistency with velocity |

Most organizations should start centralized while AI governance muscle is being built, and federate as maturity and tooling (automated guardrail checks, self-service risk tiering) make distributed self-certification reliable.

## Governance maturity model

| Level | Characteristics |
|---|---|
| **Ad hoc** | No formal process; individual teams decide independently; no AI inventory |
| **Defined** | Policies exist but inconsistently applied; inventory incomplete |
| **Managed** | Risk-tiered review process in place; central inventory maintained; documentation required |
| **Optimized** | Automated guardrails/evaluation gates in CI/CD; metrics tracked and reported to leadership; governance keeps pace with development velocity |

## Choosing a model

Consider: number of AI use cases in flight, regulatory exposure, organizational risk appetite, and available governance staffing. A federated model without adequate tooling to make self-certification reliable often silently degrades to "ad hoc with paperwork" — invest in the tooling (automated fairness/guardrail checks, standardized templates) before federating.

## Related

- [ai-governance-framework.md](ai-governance-framework.md)
- [roles-and-responsibilities.md](roles-and-responsibilities.md)
