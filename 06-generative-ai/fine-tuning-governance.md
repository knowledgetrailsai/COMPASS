# Fine-Tuning Governance

*[Home](../INDEX.md) › [06 · Generative AI](../06-generative-ai/content-provenance.md)*

## Why fine-tuning needs distinct governance

Fine-tuning customizes a base model's behavior using organization-specific data — it offers more control than prompting alone, but introduces its own data governance, IP, and safety-drift risks that a pure prompting or RAG approach doesn't.

## Key risks specific to fine-tuning

- **Training data governance**: fine-tuning data needs the same rigor as any training data — lawful basis, representativeness, PII handling — see [02-ai-lifecycle/data-and-data-governance.md](../02-ai-lifecycle/data-and-data-governance.md). Fine-tuning sets are often smaller and less rigorously audited than base model pretraining data, which can make them a weaker link.
- **Safety regression**: fine-tuning can inadvertently weaken a base model's safety training (a well-documented phenomenon where narrow fine-tuning erodes broader safety behaviors) — re-run safety/red-team evaluation after fine-tuning, don't assume base model safety properties carry over unchanged.
- **Memorization risk**: fine-tuning on a smaller, more specific dataset increases the risk of the model memorizing and later regurgitating that data verbatim, including any PII or confidential content it contains.
- **Bias amplification**: a narrow fine-tuning dataset can amplify biases present in that data more sharply than a broad pretraining corpus would, since the model's behavior shifts more directly toward the fine-tuning distribution.
- **IP and licensing**: confirm rights to use the fine-tuning data for this purpose, and check the base model provider's terms on whether fine-tuning is permitted and what rights you retain over the resulting model.

## Governance checklist for a fine-tuning project

- Datasheet for the fine-tuning dataset ([04-ai-assurance/evidence-and-traceability.md](../04-ai-assurance/evidence-and-traceability.md))
- Documented lawful basis / licensing for the data
- Pre/post fine-tuning safety evaluation comparison, not just post-tuning evaluation in isolation
- Bias/fairness testing on the fine-tuned model specifically, not inherited from base model evaluation
- Re-run relevant red-teaming ([04-ai-assurance/red-teaming.md](../04-ai-assurance/red-teaming.md))
- Version control and documentation of exactly which base model + fine-tuning data + hyperparameters produced this version, for reproducibility and incident investigation

## When to prefer RAG or prompting over fine-tuning

Fine-tuning is the highest-governance-overhead customization approach. Prefer RAG (for grounding in specific knowledge) or prompt engineering (for behavior/style adjustment) where they achieve the needed outcome with less governance burden and easier update/rollback — reserve fine-tuning for cases genuinely requiring it (deep behavioral/domain adaptation RAG/prompting can't achieve).
