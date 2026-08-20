# Tool Selection Matrix

*[Home](../INDEX.md) › [09 · Tools & Frameworks](../09-tools-and-frameworks/)*

A quick-reference guide for which category of tool addresses which need, cross-referenced to risk tier and lifecycle stage.

| Need | Tool category | Section | Minimum for |
|---|---|---|---|
| Bias/fairness testing | Fairness testing libraries | [open-source-tools.md](open-source-tools.md) | Tier 1–2 |
| Explaining a specific decision | Explainability libraries | [open-source-tools.md](open-source-tools.md) | Tier 1 (required), Tier 2 (recommended) |
| Protecting PII in data/logs | PII detection/redaction | [open-source-tools.md](open-source-tools.md) | All tiers processing personal data |
| Preventing prompt injection / jailbreaks | Guardrail frameworks + security scanners | [08-controls-and-techniques/guardrails-and-controls.md](../08-controls-and-techniques/guardrails-and-controls.md), [security-tools.md](security-tools.md) | All externally-exposed Gen AI/agentic systems |
| RAG quality assurance | RAG evaluation frameworks | [evaluation-frameworks.md](evaluation-frameworks.md) | All RAG systems |
| Agent action safety | Sandboxing, permission/policy enforcement | [security-tools.md](security-tools.md), [07-agentic-ai/tool-use-and-permissions.md](../07-agentic-ai/tool-use-and-permissions.md) | All agentic systems |
| Production drift detection | ML monitoring platforms | [observability-tools.md](observability-tools.md) | Tier 1–2 |
| AI inventory / governance workflow | Governance platform | [governance-platforms.md](governance-platforms.md) | Organization-wide, once use-case volume exceeds manual tracking |
| Certifiable management system | ISO/IEC 42001-aligned processes/tooling | [ISO-42001.md](ISO-42001.md) | Organizations pursuing certification |

## Decision guide

1. Start from the risk this tool needs to address (section 01, 06, or 07)
2. Identify the control category it implements (section 08)
3. Use this matrix to shortlist tool categories
4. Compare specific tools within the category on: maintenance/activity, fit with your existing stack, data handling implications ([03-ai-governance/third-party-ai-governance.md](../03-ai-governance/third-party-ai-governance.md))
5. For anything supporting Tier 1 assurance evidence, prefer tools with a track record and active maintenance — evidence produced by an abandoned tool weakens an audit or governance case

## Avoid over-tooling

Not every system needs every tool category — match tooling investment to risk tier. A Tier 3 internal productivity tool doesn't need a dedicated drift-monitoring platform; a Tier 1 credit-decisioning model does.
