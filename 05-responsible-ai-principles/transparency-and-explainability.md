# Transparency and Explainability

## Distinguishing the two

- **Transparency**: disclosure that AI is involved, what it's used for, and its general limitations — a governance/communication practice.
- **Explainability**: the technical ability to understand why a specific model produced a specific output — an engineering practice.

Both are needed; transparency without explainability leaves users unable to challenge a decision, explainability without transparency leaves users unaware a decision was automated at all.

## Levels of explainability

1. **Global explainability**: understanding overall model behavior/logic (e.g., which features matter most in general)
2. **Local explainability**: understanding a single prediction/output (e.g., why this loan application was denied)
3. **Counterfactual explanation**: what would need to change for a different outcome ("if income were $X higher, this would be approved")

## Techniques

See [08-controls-and-techniques/explainability](../08-controls-and-techniques/explainability/) for tool-level detail: SHAP, LIME, feature attribution, attention visualization, counterfactual generation, and the inherent-interpretability-vs-post-hoc-explanation tradeoff.

## Transparency obligations (practical)

- Disclose when users are interacting with an AI system, not a human (chatbots, voice agents)
- Disclose when content is AI-generated (especially images/video/audio — see [06-generative-ai/content-provenance.md](../06-generative-ai/content-provenance.md))
- Provide accessible explanation of automated decisions with legal/significant effect (required under GDPR Art. 22-style regimes)
- Publish model cards / system cards for material AI systems

## Gen AI-specific: explainability limits

Large generative models are often not meaningfully explainable at the mechanism level (why did the model choose these exact words). Compensate with:
- Source attribution/citations for RAG systems (show what the answer was grounded in)
- Confidence signaling and appropriate hedging in outputs
- Clear documentation of training data sources and known limitations at the system level, even without token-level explainability

## Agentic AI-specific: decision rationale

Because agents plan and take multi-step actions, explainability needs to cover **why the agent chose this plan/action**, not just why it produced particular text. Techniques: structured reasoning traces, action logs with justification, and human-readable summaries of agent decision points before high-stakes actions execute.

## Tension with other goals

Full transparency can conflict with IP protection (revealing proprietary model details) or security (revealing exploitable system internals). Resolve by tiering disclosure: full technical detail to regulators/auditors under NDA, meaningful-but-general explanation to end users.
