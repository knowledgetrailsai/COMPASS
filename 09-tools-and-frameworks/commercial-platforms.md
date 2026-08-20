# Commercial / Vendor Platforms

*[Home](../INDEX.md) › [09 · Tools & Frameworks](../09-tools-and-frameworks/)*

_Last reviewed: 2026-08-19 — vendor capabilities and naming change frequently; verify current feature sets directly with vendors before relying on specifics here._

## Cloud provider Responsible AI suites

| Platform | Provider | Notable capabilities |
|---|---|---|
| Responsible AI dashboard / Azure AI Content Safety | Microsoft Azure | Fairness assessment, interpretability, content safety filtering, error analysis |
| SageMaker Clarify | AWS | Bias detection (pre/post-training), explainability |
| Vertex AI (Model Monitoring, Explainable AI) | Google Cloud | Drift/skew detection, feature attribution, model evaluation |
| watsonx.governance | IBM | AI governance, model lifecycle tracking, risk/compliance reporting |

## AI governance / GRC platforms

Dedicated platforms for AI inventory management, risk tiering, policy enforcement, and audit trail across an organization's full AI portfolio — evaluate against the governance functions in [03-ai-governance](../03-ai-governance/) and assurance functions in [04-ai-assurance](../04-ai-assurance/) to check actual coverage rather than marketing claims.

## Gen AI evaluation / observability platforms

Commercial platforms offering LLM tracing, evaluation pipelines, guardrail management, and prompt/RAG monitoring at production scale — typically layer on top of the open-source tools in [open-source-tools.md](open-source-tools.md) with added enterprise features (SSO, audit logging, SLAs).

## Selection considerations

- **Data handling**: does using the platform mean sending sensitive data to a third party, and under what terms? See [03-ai-governance/third-party-ai-governance.md](../03-ai-governance/third-party-ai-governance.md).
- **Coverage vs. your actual stack**: cloud-provider RAI tooling is generally strongest for models/systems built on that same cloud — factor this into build platform decisions if RAI tooling coverage matters.
- **Depth vs. breadth**: broad GRC platforms are strong on governance workflow but often shallower on technical evaluation depth than specialized tools; combining a GRC platform with specialized open-source technical tools is a common pattern.
- **Avoid vendor lock-in for evidence**: ensure assurance evidence (evaluation results, audit logs) can be exported/retained independent of the platform, since this evidence needs to outlive any single vendor relationship for audit and incident-investigation purposes.

## Related

- [governance-platforms.md](governance-platforms.md)
- [tool-selection-matrix.md](tool-selection-matrix.md)
