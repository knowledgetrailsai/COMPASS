# Stage 3: Data & Data Governance

## Purpose

Most downstream RAI failures (bias, privacy leakage, IP exposure) trace back to data decisions made here. Data governance for AI extends standard data governance with AI-specific concerns.

## Activities

- **Provenance and lawful basis**: document where data comes from, under what license/consent, and confirm a lawful basis for its use in this specific system — including fine-tuning or RAG corpus data, not just "primary" training data.
- **Representativeness assessment**: check subgroup coverage relevant to the use case's fairness requirements; identify and address gaps before they become model-level bias.
- **Data quality**: completeness, accuracy, consistency, freshness — especially important for RAG corpora, where stale or contradictory documents directly degrade output quality (see [06-generative-ai/RAG-governance.md](../06-generative-ai/RAG-governance.md)).
- **Sensitive data handling**: identify PII/special-category data, apply minimization, and apply privacy techniques ([08-controls-and-techniques/privacy-techniques](../08-controls-and-techniques/privacy-techniques/)) proportionate to sensitivity.
- **Access control design**: for RAG/retrieval systems, design permission-aware retrieval from the start — this is far harder to retrofit than to build in.
- **Datasheet creation**: document the dataset per [04-ai-assurance/evidence-and-traceability.md](../04-ai-assurance/evidence-and-traceability.md).
- **Third-party data assessment**: if using licensed or vendor-provided data/embeddings, verify the vendor's own data rights and downstream usage terms.

## Gen AI-specific

Fine-tuning data should be reviewed with the same rigor as any training data — including for bias, PII, and IP provenance — since fine-tuning can bake in narrower, less-audited data than a base model's broad pretraining corpus.

## Agentic AI-specific

Data an agent can *retrieve or write to* via tools is part of its effective data footprint — apply the same governance to tool-accessible data sources as to data used in training.

## Outputs

- Datasheet for each dataset/corpus used
- Documented lawful basis and consent status
- Access control design for any retrieval system

## Related

- [05-responsible-ai-principles/privacy-and-data-protection.md](../05-responsible-ai-principles/privacy-and-data-protection.md)
- [05-responsible-ai-principles/fairness-and-bias.md](../05-responsible-ai-principles/fairness-and-bias.md)
