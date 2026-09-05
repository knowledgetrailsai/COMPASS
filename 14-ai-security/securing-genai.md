# Securing Generative AI

*[Home](../INDEX.md) › [14 · AI Security](../14-ai-security/README.md)*

A consolidated security view over content already detailed in [06-generative-ai](../06-generative-ai/content-provenance.md) — start here for the threat-and-control summary, follow the links for full depth.

## Threat catalog

| Threat | Detail | Primary controls |
|---|---|---|
| Prompt injection (direct and indirect) | [06-generative-ai/prompt-injection.md](../06-generative-ai/prompt-injection.md) | Trusted/untrusted content separation, least-privilege downstream actions, output validation |
| Jailbreaking | [06-generative-ai/jailbreaks.md](../06-generative-ai/jailbreaks.md) | Safety-tuned models, independent guardrail classifiers, continuous red-teaming |
| Sensitive information disclosure / data leakage | [06-generative-ai/data-leakage.md](../06-generative-ai/data-leakage.md) | Access-aware retrieval, PII redaction, retention limits |
| Insecure output handling | Free-text model output executed or rendered without validation (e.g., as code, SQL, or HTML) | Schema/allowlist validation before any output triggers an action; treat output as untrusted, same as user input |
| Training/fine-tuning data poisoning | [06-generative-ai/fine-tuning-governance.md](../06-generative-ai/fine-tuning-governance.md) | Data provenance, safety re-evaluation post-fine-tuning |
| Model/system prompt extraction | [06-generative-ai/prompt-injection.md](../06-generative-ai/prompt-injection.md) | Avoid embedding secrets in system prompts; assume extractable |
| Denial of service via resource exhaustion | Adversarial inputs designed to maximize compute cost (long generations, expensive tool loops) | Rate limiting, cost/token caps, timeout enforcement |
| Overreliance-enabled fraud | Users trusting fabricated output for consequential decisions | Grounding, disclosure, human review gates — see [06-generative-ai/hallucination-and-grounding.md](../06-generative-ai/hallucination-and-grounding.md) |

## The OWASP LLM Top 10 mapping

See [09-tools-and-frameworks/OWASP-llm-top10.md](../09-tools-and-frameworks/OWASP-llm-top10.md) for the full mapping of this threat catalog to the standard OWASP categories; use that file as the canonical checklist during security review.

## Defense-in-depth summary

Full layered control detail lives in [06-generative-ai/prompt-and-output-safety.md](../06-generative-ai/prompt-and-output-safety.md) and [08-controls-and-techniques/guardrails-and-controls.md](../08-controls-and-techniques/guardrails-and-controls.md): input layer, instruction layer, model/inference layer, output layer, human layer. No single layer is sufficient. A successful attack at one layer should be contained by the next.

## RAG-specific security

Access control enforced at retrieval time, not just at the source system, is the single highest-impact RAG security control — see [06-generative-ai/RAG-governance.md](../06-generative-ai/RAG-governance.md).

## Testing

[security-testing-program.md](security-testing-program.md); tools: Garak, promptfoo (red-team mode), see [09-tools-and-frameworks/security-tools.md](../09-tools-and-frameworks/security-tools.md).
