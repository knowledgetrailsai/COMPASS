# OWASP Top 10 for LLM Applications

*[Home](../INDEX.md) › [09 · Tools & Frameworks](../09-tools-and-frameworks/commercial-platforms.md)*

_Type: Security guidance (community-developed, industry-adopted). Issuer: OWASP. Last reviewed: 2026-08-19 — check for the current version, as this list is periodically revised._

## What it is

A community-developed, widely-adopted list of the most critical security risks specific to LLM applications — the de facto standard reference vocabulary for LLM/Gen AI application security, analogous to the original OWASP Top 10 for web applications.

## Representative risk categories (illustrative — confirm current official list/numbering)

| Category | Maps to this repository |
|---|---|
| Prompt Injection | [06-generative-ai/prompt-injection.md](../06-generative-ai/prompt-injection.md) |
| Insecure Output Handling | [08-controls-and-techniques/guardrails-and-controls.md](../08-controls-and-techniques/guardrails-and-controls.md) |
| Training Data Poisoning | [02-ai-lifecycle/data-and-data-governance.md](../02-ai-lifecycle/data-and-data-governance.md) |
| Model Denial of Service | [05-responsible-ai-principles/robustness-and-reliability.md](../05-responsible-ai-principles/robustness-and-reliability.md) |
| Supply Chain Vulnerabilities | [03-ai-governance/third-party-ai-governance.md](../03-ai-governance/third-party-ai-governance.md) |
| Sensitive Information Disclosure | [06-generative-ai/data-leakage.md](../06-generative-ai/data-leakage.md) |
| Insecure Plugin/Tool Design | [07-agentic-ai/tool-use-and-permissions.md](../07-agentic-ai/tool-use-and-permissions.md) |
| Excessive Agency | [07-agentic-ai/autonomy-and-control.md](../07-agentic-ai/autonomy-and-control.md) |
| Overreliance | [06-generative-ai/genai-risk-landscape.md](../06-generative-ai/genai-risk-landscape.md) |
| Model Theft | [05-responsible-ai-principles/safety-and-security.md](../05-responsible-ai-principles/safety-and-security.md) |

## How to use it

- Baseline security checklist for any LLM/Gen AI application before launch — walk through each category and confirm a specific, documented control
- Reference vocabulary for security review and red-teaming scope ([04-ai-assurance/red-teaming.md](../04-ai-assurance/red-teaming.md))
- Common ground for communicating with security teams already familiar with the original OWASP Top 10 pattern

## Limitations

Application-layer focused — doesn't cover the full ML/AI attack surface (training-time attacks against underlying models are covered more thoroughly by [MITRE-ATLAS.md](MITRE-ATLAS.md)). Also doesn't cover fairness/bias or broader governance concerns — it's a security list, not a full RAI framework; use it alongside, not instead of, the rest of this repository.

## Related

- [MITRE-ATLAS.md](MITRE-ATLAS.md)
- [06-generative-ai](../06-generative-ai/content-provenance.md), [07-agentic-ai](../07-agentic-ai/agent-incident-response.md)
- [14-ai-security/securing-genai.md](../14-ai-security/securing-genai.md) — practitioner view using this checklist
