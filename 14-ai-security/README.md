# AI Security

*[Home](../INDEX.md) › [14 · AI Security](../14-ai-security/)*

## Why this section exists

AI-specific security content was previously scattered across the safety principle (05), controls (08), and named frameworks (09) — findable if you knew where to look, not if you were starting from "how do we secure our AI systems." This section pulls it together into one threat-model-to-response view, while the underlying detail stays in place and is cross-linked rather than duplicated.

## How this differs from 05-responsible-ai-principles/safety-and-security.md

[05-responsible-ai-principles/safety-and-security.md](../05-responsible-ai-principles/safety-and-security.md) states the *principle* (why safety and security matter, the high-level threat categories). This section is the *practitioner's operating view*: threat model, control catalog, testing program, and incident response specific to AI systems — the security-team analog to how section 02 operationalizes the lifecycle and section 04 operationalizes assurance.

## Contents

| File | Covers |
|---|---|
| [ai-threat-model.md](ai-threat-model.md) | The full AI-specific attack surface, organized by system type and attack lifecycle stage |
| [securing-traditional-ml.md](securing-traditional-ml.md) | Adversarial examples, data poisoning, model extraction, membership inference |
| [securing-genai.md](securing-genai.md) | Prompt injection, jailbreaks, data leakage — consolidated view with pointers into 06 |
| [securing-agentic-ai.md](securing-agentic-ai.md) | Tool-use abuse, identity/authorization, excessive agency — consolidated view with pointers into 07 |
| [supply-chain-security.md](supply-chain-security.md) | Model, data, and dependency provenance; third-party/vendor AI risk |
| [security-testing-program.md](security-testing-program.md) | How red-teaming, penetration testing, and continuous scanning fit together for AI |
| [security-incident-response.md](security-incident-response.md) | AI-specific triage and containment, consolidating 02's general incident process and 07's agent-specific process |
| [security-metrics-and-reporting.md](security-metrics-and-reporting.md) | What to measure and report to demonstrate security posture |

## Relationship to the rest of the repository

This section doesn't replace the security content already embedded in [05-responsible-ai-principles/safety-and-security.md](../05-responsible-ai-principles/safety-and-security.md), [06-generative-ai](../06-generative-ai/) (prompt-injection.md, jailbreaks.md, data-leakage.md), [07-agentic-ai](../07-agentic-ai/) (tool-use-and-permissions.md, identity-and-authorization.md, agent-incident-response.md), [08-controls-and-techniques/guardrails-and-controls.md](../08-controls-and-techniques/guardrails-and-controls.md) and [08-controls-and-techniques/robustness-testing](../08-controls-and-techniques/robustness-testing/), or [09-tools-and-frameworks](../09-tools-and-frameworks/) (OWASP LLM Top 10, MITRE ATLAS, security-tools.md). It's the front door into all of that — start here if you're approaching the repository from a security angle, then follow the links out to the technology-specific depth.

## Governance tie-in

Security review is a required input to [03-ai-governance/ai-governance-board.md](../03-ai-governance/ai-governance-board.md) approval for Tier 1 systems, and security assurance evidence (red-team reports, penetration test results) feeds [04-ai-assurance/evidence-and-traceability.md](../04-ai-assurance/evidence-and-traceability.md).
