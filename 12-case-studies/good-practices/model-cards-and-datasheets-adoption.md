# Widespread Adoption of Model Cards and Datasheets

*[Home](../../INDEX.md) › [12 · Case Studies](../../12-case-studies/) › [good-practices](../../12-case-studies/good-practices/)*

**Context**: Industry-wide practice originating from research publications — "Model Cards for Model Reporting" (Mitchell et al., Google, 2019) and "Datasheets for Datasets" (Gebru et al., 2018/2021) — subsequently adopted as standard practice across much of the AI industry, including major model providers publishing model/system cards for significant model releases.

**AI system**: Practice applies horizontally across traditional ML and Gen AI model releases industry-wide.

**What happened**: Following the publication of structured documentation proposals for models and datasets, model cards and datasheets became a widely adopted norm — major AI labs and many enterprises now routinely publish structured documentation covering intended use, limitations, training data characteristics, and evaluation results alongside model releases, and equivalent internal documentation practices are increasingly standard for enterprise AI governance programs.

**What worked**: A simple, low-friction, standardized documentation format lowered the barrier to actually producing and consuming AI documentation, compared to bespoke, inconsistent write-ups. Standardization also made it easier for downstream users, auditors, and regulators to know what to expect and where to look, and for procurement/governance teams to compare systems consistently.

**Risk category addressed**: Transparency and explainability risk; supports assurance and evidence practices broadly ([04-ai-assurance/evidence-and-traceability.md](../../04-ai-assurance/evidence-and-traceability.md)).

**Lifecycle stage**: Embedded across [02-ai-lifecycle/model-development.md](../../02-ai-lifecycle/model-development.md) (documented as you build) through [02-ai-lifecycle/evaluation-and-validation.md](../../02-ai-lifecycle/evaluation-and-validation.md) (finalized with real results).

**Why this is a good-practice example, not just a neutral tool adoption**: The practice succeeded broadly because it was lightweight enough for routine use rather than a heavyweight compliance exercise reserved for the highest-risk systems only — a lesson directly applicable to how organizations should design their own internal RAI documentation requirements ([02-ai-lifecycle/documentation-artifacts.md via 04-ai-assurance/evidence-and-traceability.md](../../04-ai-assurance/evidence-and-traceability.md)): favor a practical, consistently-used lightweight standard over an ideal-but-rarely-completed heavyweight one.

**Preventive/enabling factors for replication**: Keep documentation templates short and structured rather than open-ended; integrate documentation into the standard development workflow rather than treating it as a separate compliance task; make the practice the default for all Tier 1–2 systems, not an optional extra reserved for audits.

**Sources**: Mitchell, M., et al., "Model Cards for Model Reporting," FAT* 2019 (Google); Gebru, T., et al., "Datasheets for Datasets," Communications of the ACM, 2021; widespread subsequent industry adoption documented in model/system cards published by major AI labs for significant model releases.
