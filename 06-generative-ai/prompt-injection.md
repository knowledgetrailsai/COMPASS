# Prompt Injection

*[Home](../INDEX.md) › [06 · Generative AI](../06-generative-ai/)*

## Definition

An attack where malicious instructions are embedded in content the model processes — user input, or (more dangerously) content the model retrieves or is fed from an external source (a webpage, document, email, tool output) — causing the model to follow the injected instructions instead of, or in addition to, its intended task.

## Why it's structurally hard to fully prevent

Most current model architectures don't have a hard boundary between "trusted instructions" and "data to process" — both arrive as tokens in the same context. An attacker who can get text into anything the model reads has a potential path to influence its behavior. This is treated as a fundamentally different, harder problem than traditional input validation, not a bug that a simple filter fixes.

## Direct vs. indirect prompt injection

- **Direct**: the user themselves crafts an adversarial prompt to override system instructions (overlaps heavily with jailbreaking — see [jailbreaks.md](jailbreaks.md))
- **Indirect**: injected instructions arrive via third-party content the model processes without the end user's knowledge — a poisoned webpage, a malicious email in an inbox an agent is summarizing, a manipulated document in a RAG corpus. Indirect injection is the higher-severity risk for agentic and RAG systems, since neither the user nor sometimes even the operator is aware of the attack surface.

## Consequences

For a standalone chatbot: manipulated or leaked output. For a RAG or agentic system: potential data exfiltration, unauthorized tool use, or actions taken on the attacker's behalf using the legitimate user's or system's permissions — see [07-agentic-ai/tool-use-and-permissions.md](../07-agentic-ai/tool-use-and-permissions.md).

## Mitigations (defense in depth — no single fix is sufficient)

- Treat all external/retrieved content as untrusted, structurally separated from trusted system instructions where the framework/architecture supports it
- Least-privilege tool access so a successful injection has limited blast radius even if it succeeds
- Action validation before execution (schema/allowlist checks) rather than trusting model output directly as a command
- Output/action monitoring for anomalous patterns consistent with a successful injection
- Human approval gates for high-consequence actions regardless of what triggered the request

## Related

- [jailbreaks.md](jailbreaks.md)
- [05-responsible-ai-principles/safety-and-security.md](../05-responsible-ai-principles/safety-and-security.md)
- [08-controls-and-techniques/guardrails-and-controls.md](../08-controls-and-techniques/guardrails-and-controls.md)
- [09-tools-and-frameworks](../09-tools-and-frameworks/) — OWASP LLM Top 10 (LLM01: Prompt Injection)
