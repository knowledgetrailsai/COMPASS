# Prompt and Output Safety

*[Home](../INDEX.md) › [06 · Generative AI](../06-generative-ai/content-provenance.md)*

## Defense-in-depth model

No single control reliably prevents unsafe Gen AI behavior. Layer controls across the request lifecycle:

### 1. Input layer
- **Input validation/sanitization**: strip or flag suspicious patterns (instruction-like text embedded in data fields)
- **Treat all retrieved/external content as untrusted**: web pages, documents, tool outputs, emails fed into the model can contain injected instructions: never grant them the same trust as the system prompt
- **Rate limiting and abuse detection**: throttle and flag patterns consistent with automated jailbreak attempts

### 2. Instruction layer
- **System prompt hardening**: clear task scoping, explicit refusal instructions for out-of-scope requests — but never rely on system prompt instructions alone as a security boundary, since they can be leaked or overridden
- **Privilege separation**: keep untrusted user/retrieved content clearly delineated from trusted system instructions (structurally, not just descriptively) where the model framework supports it

### 3. Model/inference layer
- **Safety-tuned models**: use models with safety training appropriate to the deployment context
- **Guardrail models/classifiers**: a separate, smaller model or ruleset that screens input and output for policy violations independent of the primary generation model

### 4. Output layer
- **Output filtering**: scan generated content for policy violations (toxicity, PII, disallowed categories) before returning to the user
- **Groundedness checking (RAG)**: verify output claims are supported by retrieved source material; flag or block ungrounded claims in high-stakes contexts
- **Structured output validation**: when output feeds a downstream system (code execution, API call, agentic action), validate against a schema/allowlist rather than executing free-text output directly

### 5. Human layer
- **Human review for high-stakes outputs** before they reach end users or trigger actions
- **User feedback and reporting mechanisms** to catch what automated layers miss, feeding back into red-teaming and filter tuning

## Red-teaming

Systematic adversarial testing before launch and on a recurring cadence: jailbreak attempts, prompt injection via realistic retrieved-content scenarios, edge-case and adversarial inputs targeting known risk categories. See [08-controls-and-techniques/robustness-testing](../08-controls-and-techniques/robustness-testing/README.md).

## Guardrail tooling

See [09-tools-and-frameworks/open-source-tools.md](../09-tools-and-frameworks/open-source-tools.md) for specific frameworks (e.g., NeMo Guardrails, Guardrails AI, Llama Guard–style classifiers) and [08-controls-and-techniques/guardrails-and-controls.md](../08-controls-and-techniques/guardrails-and-controls.md) for implementation patterns.

## Key principle

Treat prompt injection and jailbreaking as an assumed, ongoing threat rather than a solved problem: design systems to limit the blast radius of a successful attack (least-privilege tool access, output validation before action, human approval for consequential steps) rather than relying purely on preventing the attack from succeeding.
