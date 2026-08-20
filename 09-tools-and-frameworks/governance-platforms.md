# Governance Platforms

## What this category covers

Software supporting the organizational processes in [03-ai-governance](../03-ai-governance/) and [04-ai-assurance](../04-ai-assurance/) at scale: AI inventory/registry, risk-tiering workflow, policy management, approval routing, and audit trail — distinct from the technical evaluation tools in [open-source-tools.md](open-source-tools.md) and [evaluation-frameworks.md](evaluation-frameworks.md).

## Core capabilities to evaluate

- **AI inventory/registry**: central, current record of every AI system with owner, risk tier, and review status (see [03-ai-governance/ai-governance-framework.md](../03-ai-governance/ai-governance-framework.md))
- **Workflow automation**: routing use cases through risk-tiering, review, and approval steps automatically rather than manually tracked in spreadsheets/email
- **Policy-as-code / automated checks**: where feasible, automated verification of policy compliance (e.g., flagging a system as non-compliant if required documentation is missing) rather than relying purely on manual review
- **Evidence repository**: centralized, tamper-evident storage for assurance artifacts ([04-ai-assurance/evidence-and-traceability.md](../04-ai-assurance/evidence-and-traceability.md))
- **Reporting**: dashboards and exportable reports for governance board and leadership reporting ([04-ai-assurance/assurance-reporting.md](../04-ai-assurance/assurance-reporting.md))
- **Regulatory mapping**: built-in mapping of requirements to specific regulations (EU AI Act, etc.) — useful as a starting point, but verify currency against [10-regulations-and-standards](../10-regulations-and-standards/) rather than trusting a vendor's regulatory content as legal authority

## Build vs. buy

Smaller organizations or those early in AI governance maturity often start with a well-structured shared document/spreadsheet-based inventory and lightweight workflow tooling (ticketing system, shared review templates) before investing in a dedicated platform — the discipline of consistent risk tiering and documentation matters more initially than the tooling sophistication. Consider a dedicated platform once volume of AI use cases makes manual tracking unreliable.

## Selection considerations

Same third-party assessment discipline applies as any vendor — see [03-ai-governance/third-party-ai-governance.md](../03-ai-governance/third-party-ai-governance.md), particularly around data handling given these platforms often hold sensitive information about your entire AI risk posture.

## Related

- [commercial-platforms.md](commercial-platforms.md)
- [03-ai-governance/ai-governance-framework.md](../03-ai-governance/ai-governance-framework.md)
