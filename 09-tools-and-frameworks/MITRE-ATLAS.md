# MITRE ATLAS

*[Home](../INDEX.md) › [09 · Tools & Frameworks](../09-tools-and-frameworks/commercial-platforms.md)*

_Type: Threat knowledge base / security guidance. Issuer: MITRE. Last reviewed: 2026-08-19._

## What it is

Adversarial Threat Landscape for Artificial-Intelligence Systems — a knowledge base of adversarial tactics and techniques against AI/ML systems, modeled on the structure of MITRE ATT&CK (the widely-used cybersecurity threat framework). Documents real-world and demonstrated attack techniques against ML systems, including case studies.

## Structure

Organized by tactic (the adversary's goal, e.g., "Reconnaissance," "ML Model Access," "Exfiltration," "Impact") and technique (specific methods achieving that tactic) — providing a common vocabulary for describing and defending against AI-specific attacks, analogous to how ATT&CK standardized traditional cybersecurity threat description.

## Relevant tactic categories

- **Reconnaissance and resource development**: adversary gathering information about a target ML system
- **ML model access**: techniques for gaining access to query, extract, or manipulate a model
- **ML attack staging**: crafting adversarial inputs, poisoned data, or backdoors
- **Exfiltration**: extracting model information, training data, or proprietary details
- **Impact**: degrading model performance, causing harmful outputs, or achieving denial of service

## How to use it

- **Red-teaming reference**: structure adversarial test scenarios ([04-ai-assurance/red-teaming.md](../04-ai-assurance/red-teaming.md)) around ATLAS tactics/techniques relevant to your system type, rather than starting from scratch
- **Threat modeling input**: during [02-ai-lifecycle/requirements-and-design.md](../02-ai-lifecycle/requirements-and-design.md), use ATLAS to systematically check which attack categories apply to your architecture
- **Incident classification**: when an AI security incident occurs, ATLAS technique IDs provide a standard way to classify and communicate what happened

## Relationship to OWASP LLM Top 10

ATLAS covers the broader ML/AI attack surface (including traditional ML); OWASP LLM Top 10 ([OWASP-llm-top10.md](OWASP-llm-top10.md)) is narrower and specifically focused on LLM application-layer risks. Use both together for a Gen AI system — ATLAS for the underlying model attack surface, OWASP for the application layer built around it.

## Related

- [08-controls-and-techniques/robustness-testing](../08-controls-and-techniques/robustness-testing/README.md)
- [05-responsible-ai-principles/safety-and-security.md](../05-responsible-ai-principles/safety-and-security.md)
- [14-ai-security/ai-threat-model.md](../14-ai-security/ai-threat-model.md) — this repository's own threat model, structured on the same lifecycle-stage pattern
