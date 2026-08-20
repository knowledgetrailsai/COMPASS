# Privacy and Data Protection

## Core obligations

- **Data minimization**: collect/use only data necessary for the stated purpose
- **Purpose limitation**: don't repurpose data (e.g., support chat logs) for training without proper basis/consent
- **Consent and lawful basis**: ensure a valid legal basis for processing, especially for training data and any sensitive data category
- **Retention limits**: don't keep data (including chat/agent logs) longer than necessary
- **Rights fulfillment**: support access, correction, deletion requests — including from AI training data and memory stores where feasible

## AI-specific privacy risks

- **Memorization**: large models can memorize and regurgitate training data verbatim, including PII, if not properly mitigated
- **Re-identification**: seemingly anonymized data can be re-identified when combined with model outputs or other datasets
- **Inference risk**: models can infer sensitive attributes (health, sexual orientation, etc.) from seemingly unrelated data
- **RAG context leakage**: retrieval-augmented systems can surface sensitive documents to users who shouldn't see them if access controls aren't enforced at retrieval time, not just at the UI layer
- **Prompt/query logging**: user prompts themselves can contain sensitive personal data that gets logged and retained
- **Agentic memory**: persistent agent memory can accumulate sensitive personal data over time without a clear retention/deletion policy

## Mitigation techniques

See [08-controls-and-techniques/privacy-techniques](../08-controls-and-techniques/privacy-techniques/) for depth: differential privacy, federated learning, PII detection/redaction, anonymization/pseudonymization, and synthetic data.

## Practical controls

- PII detection and redaction on both inputs (before logging/training) and outputs (before returning to user)
- Enforce document/row-level access control at retrieval time in RAG systems — never rely solely on "the model won't share it"
- Separate training/fine-tuning data pipelines from production logs with explicit opt-in, not default inclusion
- Define and enforce retention windows for prompts, outputs, and agent memory
- Data Processing Agreements (DPAs) with any third-party model/API provider, with clear terms on whether your data is used for their model training (default should be no, for enterprise use)

## Regulatory anchors

GDPR (EU), India's DPDP Act 2023, and sector-specific rules (HIPAA for health data, financial data protection rules) all apply to AI systems processing personal data — there is no "AI exception." See [10-regulations-and-standards](../10-regulations-and-standards/).

## DPIA trigger

Conduct a Data Protection Impact Assessment when: processing sensitive/special-category data at scale, using profiling with legal/significant effect, or deploying novel AI technology with unclear privacy risk — see [13-implementation-playbooks/conducting-an-ai-risk-assessment.md](../13-implementation-playbooks/conducting-an-ai-risk-assessment.md).
