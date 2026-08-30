# Documentation Artifacts

*[Home](../INDEX.md) › [04 · AI Assurance](../04-ai-assurance/assurance-overview.md)*

Standard artifacts that make AI systems auditable, transferable, and reviewable. Templates for several of these live in [13-implementation-playbooks](../13-implementation-playbooks/agentic-deployment-checklist.md) and [templates](../templates/README.md).

## Model Card
Summarizes a model's intended use, performance across subgroups, training data, known limitations, and ethical considerations. Originated from Google's "Model Cards for Model Reporting" research; now a near-universal practice. See [13-implementation-playbooks/model-card-template.md](../13-implementation-playbooks/model-card-template.md).

## Datasheet for Datasets
Documents a dataset's motivation, composition, collection process, preprocessing, and recommended/discouraged uses — analogous to a "nutrition label" for data.

## System Card (Gen AI / compound systems)
Broader than a model card: documents the full system, including retrieval components, guardrails, tool integrations, and orchestration logic — appropriate for RAG applications and agentic systems where behavior emerges from multiple components, not one model.

## Data Protection Impact Assessment (DPIA)
Required under GDPR-style regimes (and increasingly under India's DPDP Act practice) when processing is likely to result in high risk to individuals. Assesses necessity, proportionality, and risk mitigation for personal data processing.

## Algorithmic Impact Assessment (AIA)
Broader than a DPIA — assesses impact on rights, fairness, and societal effects, not just data protection. Often required for public-sector or high-risk private-sector AI.

## Agent Action Log / Audit Trail
For agentic systems: a structured, tamper-evident log of what the agent perceived, decided, and did — including tool calls and their inputs/outputs — sufficient to reconstruct "why did the agent do that" after the fact. See [07-agentic-ai/agentic-evaluation.md](../07-agentic-ai/agentic-evaluation.md).

## Red-team / Evaluation Report
Summary of adversarial testing performed, vulnerabilities found, and remediation status — should be refreshed on material model/prompt changes, not just at initial launch.

## Where these fit
| Artifact | Required for |
|---|---|
| Model card | All Tier 1–2 systems |
| Datasheet | Any custom-collected or fine-tuning dataset |
| System card | Gen AI / RAG / agentic systems |
| DPIA | Any system processing personal data at Tier 1, and Tier 2 where sensitive data is involved |
| AIA | Public sector or Tier 1 systems affecting rights |
| Agent action log | All agentic systems with real-world action capability |
| Red-team report | Tier 1 systems, and any Gen AI system exposed externally |
