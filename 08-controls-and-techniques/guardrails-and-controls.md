# Guardrails and Runtime Controls

*[Home](../INDEX.md) › [08 · Controls & Techniques](../08-controls-and-techniques/README.md)*

## Definition

Runtime mechanisms that constrain a system's inputs, outputs, or actions in real time — the last line of defense that operates independently of the underlying model's own training/behavior, and the most direct implementation of the "Controls" layer in the risk → control → technique → test chain.

## Guardrail types

### Input guardrails
- Input validation/sanitization for structural anomalies
- Classifier-based screening for known attack patterns (jailbreak attempts, injection patterns)
- Rate limiting and abuse-pattern detection

### Output guardrails
- Content classifiers screening for disallowed categories (toxicity, harmful content, PII) before returning output
- Groundedness/faithfulness checks for RAG outputs before display
- Format/schema validation for structured outputs feeding downstream systems

### Action guardrails (Agentic AI)
- Allowlist/schema validation before a tool call executes
- Permission boundary enforcement independent of the model's own "judgment" — see [07-agentic-ai/tool-use-and-permissions.md](../07-agentic-ai/tool-use-and-permissions.md)
- Rate/value/scope limits per action type
- Human approval gate injection for defined high-stakes action categories

## Design principles

- **Independent of the primary model**: guardrails implemented as a separate classifier/ruleset are more robust than relying on the primary model to police itself, since a successful jailbreak/injection targeting the primary model doesn't automatically defeat an independent check
- **Fail closed for high-stakes actions**: when a guardrail check itself errors or times out, default to blocking/escalating rather than allowing the action through
- **Defense in depth**: layer multiple guardrails (input + output + action) rather than relying on any single check, consistent with [06-generative-ai/prompt-and-output-safety.md](../06-generative-ai/prompt-and-output-safety.md)
- **Explainable rejections**: when a guardrail blocks something, log why — both for debugging false positives and for security monitoring

## Common pitfalls

- Guardrails so aggressive they block a large share of legitimate requests, creating pressure to weaken them without addressing the underlying false-positive rate
- Guardrails implemented once at launch and never updated as new attack patterns emerge
- Treating guardrails as sufficient on their own, without the surrounding permission scoping and human oversight controls in [07-agentic-ai](../07-agentic-ai/agent-incident-response.md)

## Tooling

See [09-tools-and-frameworks/open-source-tools.md](../09-tools-and-frameworks/open-source-tools.md) — NeMo Guardrails, Guardrails AI, Llama Guard–style classifiers.

## Testing

Guardrail effectiveness should be verified through [04-ai-assurance/red-teaming.md](../04-ai-assurance/red-teaming.md), not assumed from configuration alone.

## Related

- [14-ai-security](../14-ai-security/README.md) — full threat model and control catalog these guardrails implement
