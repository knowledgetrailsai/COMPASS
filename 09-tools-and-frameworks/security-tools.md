# Security Tools

*[Home](../INDEX.md) › [09 · Tools & Frameworks](../09-tools-and-frameworks/)*

## AI/LLM-specific security testing

| Tool/category | Purpose |
|---|---|
| Garak | Automated LLM vulnerability scanning (jailbreaks, prompt injection, data leakage probes) |
| promptfoo (red-team mode) | Automated adversarial prompt testing integrated into CI |
| Custom fuzzing harnesses | Automated generation of adversarial/edge-case inputs targeting known failure categories |

## Adversarial ML / traditional model security

| Tool | Purpose |
|---|---|
| Adversarial Robustness Toolbox (ART) | Adversarial attack simulation and defense evaluation |
| Foolbox | Adversarial example generation for robustness testing |

## Guardrail and classification tools

See [08-controls-and-techniques/guardrails-and-controls.md](../08-controls-and-techniques/guardrails-and-controls.md) and [open-source-tools.md](open-source-tools.md) — NeMo Guardrails, Guardrails AI, safety classifier models — function as both a control and a security tool.

## Agentic security

- Sandboxing/isolation tooling (containerization, restricted execution environments) for any agent with code execution or file system access
- Secrets/credential management systems supporting scoped, time-boxed credential issuance for agent tool access — see [07-agentic-ai/identity-and-authorization.md](../07-agentic-ai/identity-and-authorization.md)
- API gateway / policy enforcement tooling for validating and rate-limiting agent tool calls independent of the agent's own logic

## Threat intelligence references (not tools, but essential inputs)

- **OWASP Top 10 for LLM Applications**: the standard reference threat list for LLM/Gen AI application security
- **MITRE ATLAS**: adversarial ML tactics/techniques knowledge base, useful for structuring red-team scenarios

See [09-tools-and-frameworks/OWASP-llm-top10.md](OWASP-llm-top10.md) and [09-tools-and-frameworks/MITRE-ATLAS.md](MITRE-ATLAS.md).

## Integration with existing security tooling

AI-specific security tools should feed into existing SIEM/security monitoring infrastructure rather than operate as an isolated silo — anomalous agent action patterns or repeated jailbreak attempts are security events that belong in the same triage flow as any other security alert.

## Related

- [14-ai-security](../14-ai-security/) — the practitioner-level threat model, control catalog, and testing program these tools implement
