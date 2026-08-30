# Generative AI — Specific Risks

*[Home](../INDEX.md) › [06 · Generative AI](../06-generative-ai/content-provenance.md)*

Generative AI (LLMs, image/audio/video generation) inherits the risks in [01-foundations/risk-taxonomy.md](../01-foundations/risk-taxonomy.md) but adds several distinct failure modes.

## Hallucination
Generating plausible but false, fabricated, or unverifiable content (fake citations, invented facts, non-existent case law/APIs) — often stated with confident tone that gives no signal of uncertainty. Highest-stakes in legal, medical, financial, and safety-critical uses. Mitigate with RAG grounding, citation requirements, confidence calibration, and human review for high-stakes outputs.

## Prompt injection and jailbreaking
- **Prompt injection**: malicious instructions hidden in input or retrieved content (a webpage, document, email) hijack model behavior — especially dangerous when the model's output triggers downstream actions (agentic context).
- **Jailbreaking**: adversarial prompting techniques designed to bypass safety training and elicit disallowed content.

## Content authenticity and deepfakes
Generated images, audio, and video can convincingly impersonate real people or fabricate events, enabling fraud, disinformation, harassment, and non-consensual content. See [content-provenance.md](content-provenance.md).

## IP and copyright exposure
Training data provenance, output similarity to copyrighted works, and ambiguity around ownership of AI-generated output create legal exposure. See [copyright-and-ip.md](copyright-and-ip.md).

## Data leakage and memorization
Models can memorize and regurgitate training data verbatim, including PII or proprietary content; RAG systems can leak content across access boundaries if retrieval isn't permission-aware.

## Toxic/harmful content generation
Even with safety training, models can be prompted (directly or via jailbreak) to produce hate speech, harassment, instructions for harm, or age-inappropriate content.

## Overreliance and automation bias
Users trusting generated content without appropriate scrutiny, especially as fluency of output creates a false impression of reliability — a human factors risk, not just a model risk.

## Sycophancy
Models telling users what they want to hear rather than what's accurate, particularly under conversational pressure — undermines factual reliability in subtle ways that are hard to catch in single-turn evaluation.

## Model/output homogenization
Widespread reliance on a small number of foundation models can homogenize content, style, and even ideas across an industry or information ecosystem — a systemic rather than per-deployment risk.

## Mitigation summary

| Risk | Primary mitigations |
|---|---|
| Hallucination | RAG grounding, citations, confidence signaling, human review |
| Prompt injection | Input/output sanitization, privilege separation, treat retrieved content as untrusted |
| Deepfakes | Provenance/watermarking, detection tools, use-case restrictions |
| IP exposure | Licensed training data, output similarity checks, indemnification terms with vendors |
| Data leakage | Access-aware retrieval, PII redaction, output filtering |
| Toxic content | Layered content filters, red-teaming, refusal training |

See [prompt-and-output-safety.md](prompt-and-output-safety.md) for concrete controls.
