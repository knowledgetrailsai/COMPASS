# AI Governance Framework

*[Home](../INDEX.md) › [03 · AI Governance](../03-ai-governance/AI-assurance.md)*

## Purpose

An organizational structure and set of processes that ensures AI systems are reviewed, approved, and monitored proportionate to their risk — without becoming a bottleneck for low-risk use cases.

## Structural components

### 1. AI Governance Board / Council
Cross-functional (product, engineering, legal, security, data/privacy, ethics, business). Meets regularly to:
- Approve high-risk use cases before development or deployment
- Set organization-wide AI policy (acceptable use, model approval lists, data handling rules)
- Review incidents and near-misses
- Own the risk-tiering framework and keep it current with regulation

### 2. AI Inventory / Registry
A central, living record of every AI system in use (including Gen AI features and agentic workflows) with owner, purpose, risk tier, data used, and review status. Essential for regulatory response (e.g., EU AI Act requires this for high-risk systems) and for knowing your actual exposure.

### 3. Policy layer
- Acceptable use policy (what AI can/cannot be used for)
- Approved model/vendor list
- Data handling and retention rules for AI training/inference
- Human oversight requirements by risk tier
- Third-party/vendor AI assessment requirements

### 4. Review and approval workflow
Tied to [risk-management.md](risk-management.md): low-risk use cases self-certify via checklist; medium-risk get a lightweight review; high-risk require full governance board sign-off, documentation (model cards, DPIAs), and ongoing monitoring commitments.

### 5. Monitoring and audit
Post-deployment monitoring (see [08-controls-and-techniques/monitoring-and-observability](../08-controls-and-techniques/monitoring-and-observability/README.md)) feeding back into the governance board; periodic audits of high-risk systems; incident response tied into existing security/ops processes.

## Governance maturity levels

| Level | Characteristics |
|---|---|
| **Ad hoc** | No formal process; individual teams decide independently |
| **Defined** | Policies exist but inconsistently applied; no central inventory |
| **Managed** | Risk-tiered review process in place; central inventory maintained |
| **Optimized** | Automated guardrails and monitoring; governance integrated into CI/CD and MLOps tooling; metrics tracked and reported to leadership |

## Relationship to enterprise risk management

AI governance should plug into existing ERM, InfoSec, and privacy governance rather than exist as a silo, reuse existing risk committees, incident response processes, and audit functions where possible, adding AI-specific expertise rather than duplicating structure.

## Related

- [risk-management.md](risk-management.md)
- [../02-ai-lifecycle/lifecycle-overview.md](../02-ai-lifecycle/lifecycle-overview.md)
- [../04-ai-assurance/evidence-and-traceability.md](../04-ai-assurance/evidence-and-traceability.md)
