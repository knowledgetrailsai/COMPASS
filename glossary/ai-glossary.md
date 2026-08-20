# AI Glossary

Alphabetical reference. For the conceptual distinctions between related terms (ethics/RAI/governance/assurance; law/standard/framework/guidance), see [00-navigation-and-methodology/terminology-and-glossary.md](../00-navigation-and-methodology/terminology-and-glossary.md) instead — this file is for quick individual-term lookup.

**Agentic AI** — AI systems that plan, use tools, and take multi-step autonomous actions toward a goal, as opposed to producing a single response to a single prompt.

**AI Assurance** — Systematic, evidence-based verification that RAI principles, governance, and controls are functioning as intended. See [04-ai-assurance](../04-ai-assurance/).

**AI Governance** — Organizational structures, roles, and processes that institutionalize Responsible AI practice. See [03-ai-governance](../03-ai-governance/).

**Bias (algorithmic)** — Systematic, unfair skew in a model's outputs or decisions, typically traced to training data, feature choice, or objective design. See [05-responsible-ai-principles/fairness-and-bias.md](../05-responsible-ai-principles/fairness-and-bias.md).

**Conformity Assessment** — Formal process demonstrating an AI system meets a regulatory standard's requirements before market placement. See [04-ai-assurance/conformity-assessment.md](../04-ai-assurance/conformity-assessment.md).

**Differential Privacy** — A mathematical framework adding calibrated noise to data/outputs to provide a formal, quantifiable privacy guarantee against re-identification.

**Explainability** — The technical ability to understand why a model produced a specific output. See [05-responsible-ai-principles/transparency-and-explainability.md](../05-responsible-ai-principles/transparency-and-explainability.md).

**Fine-tuning** — Further training a pre-trained (base) model on a smaller, task/organization-specific dataset to adapt its behavior. See [06-generative-ai/fine-tuning-governance.md](../06-generative-ai/fine-tuning-governance.md).

**Grounding** — Constraining generative model output to verifiable source material rather than relying solely on trained-in (parametric) knowledge. See [06-generative-ai/hallucination-and-grounding.md](../06-generative-ai/hallucination-and-grounding.md).

**Guardrails** — Runtime mechanisms constraining a system's inputs, outputs, or actions independent of the underlying model's own behavior. See [08-controls-and-techniques/guardrails-and-controls.md](../08-controls-and-techniques/guardrails-and-controls.md).

**Hallucination** — Generative output that is plausible-sounding but false, fabricated, or unsupported by any source. See [06-generative-ai/hallucination-and-grounding.md](../06-generative-ai/hallucination-and-grounding.md).

**High-Risk AI System** — A regulatory classification (e.g., under the EU AI Act) for AI systems with significant potential impact on health, safety, or fundamental rights, triggering extensive compliance obligations.

**Human-in-the-loop / on-the-loop / in-command** — Models of human oversight ranging from pre-approval of every action to system-level override authority. See [07-agentic-ai/autonomy-and-control.md](../07-agentic-ai/autonomy-and-control.md).

**Jailbreaking** — Adversarial prompting techniques designed to bypass a model's safety training. See [06-generative-ai/jailbreaks.md](../06-generative-ai/jailbreaks.md).

**Model Card** — Standardized documentation of a model's intended use, performance, limitations, and ethical considerations. See [13-implementation-playbooks/model-card-template.md](../13-implementation-playbooks/model-card-template.md).

**Prompt Injection** — An attack embedding malicious instructions in content a model processes, causing it to follow injected instructions instead of its intended task. See [06-generative-ai/prompt-injection.md](../06-generative-ai/prompt-injection.md).

**RAG (Retrieval-Augmented Generation)** — A Gen AI architecture pattern that grounds model output in retrieved documents. See [06-generative-ai/RAG-governance.md](../06-generative-ai/RAG-governance.md).

**Red-Teaming** — Adversarial testing that deliberately tries to make a system fail, misbehave, or be misused. See [04-ai-assurance/red-teaming.md](../04-ai-assurance/red-teaming.md).

**Responsible AI (RAI)** — The practice of designing, building, deploying, and operating AI systems fairly, transparently, safely, and accountably. See [01-foundations/what-is-responsible-ai.md](../01-foundations/what-is-responsible-ai.md).

**Risk Tiering** — Classifying an AI use case by risk level to scale governance rigor proportionately. See [03-ai-governance/risk-management.md](../03-ai-governance/risk-management.md).

**Specification Gaming** — An agent finding a literal path that technically satisfies a stated goal while violating its intent. See [07-agentic-ai/planning-and-reasoning-risk.md](../07-agentic-ai/planning-and-reasoning-risk.md).

**System Card** — Documentation covering a full compound AI system (model + retrieval + guardrails + orchestration), broader than a model card. See [04-ai-assurance/evidence-and-traceability.md](../04-ai-assurance/evidence-and-traceability.md).
