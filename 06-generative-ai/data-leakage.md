# Data Leakage (Generative AI)

*[Home](../INDEX.md) › [06 · Generative AI](../06-generative-ai/)*

## Forms of leakage specific to Gen AI

### Training data memorization
Large models can memorize and verbatim-reproduce portions of training data, including PII, proprietary text, or licensed content, when prompted in ways that trigger recall rather than generation.

### RAG/retrieval context leakage
The most common enterprise leakage vector: a retrieval system surfaces content from documents the querying user isn't authorized to see, because access control was enforced at the source system but not re-enforced at retrieval/query time. See [RAG-governance.md](RAG-governance.md).

### Prompt/conversation leakage
User prompts and conversation history — which can contain sensitive personal or business data — get logged, retained, and potentially exposed via debugging tools, analytics pipelines, or (if used for model improvement) future model behavior.

### System prompt leakage
Adversarial prompting extracts the system prompt/instructions, which can reveal proprietary business logic, guardrail configuration (helping an attacker evade it), or confidential context.

### Cross-session/cross-tenant leakage
In multi-tenant systems, improper session or memory isolation can leak one user's/organization's data into another's context — see [07-agentic-ai/memory-and-state-risk.md](../07-agentic-ai/memory-and-state-risk.md) for the agentic-memory-specific version.

## Mitigations

- **Access-aware retrieval**: enforce document/row-level permissions as a hard filter at query time, never as a model instruction alone
- **PII detection and redaction** on both ingestion (before indexing/training) and output (before returning to the user)
- **Data minimization in prompts**: don't pass more context to the model than the specific request requires
- **Retention limits** on logs, conversation history, and cached context, with clear ownership of the retention policy
- **Tenant isolation testing**: explicitly test for cross-tenant leakage in multi-tenant architectures, not just assume application-layer logic prevents it
- **System prompt hygiene**: avoid putting genuinely sensitive information (credentials, unredacted business logic) in system prompts, since extraction should be assumed possible

## Related

- [05-responsible-ai-principles/privacy-and-data-protection.md](../05-responsible-ai-principles/privacy-and-data-protection.md)
- [08-controls-and-techniques/privacy-techniques](../08-controls-and-techniques/privacy-techniques/)
