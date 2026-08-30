# Insurance

*[Home](../INDEX.md) › [11 · Sector-Specific AI](../11-sector-specific-ai/README.md)*

## Common AI use cases
Underwriting and risk pricing, claims processing and fraud detection, customer service automation, agentic claims-handling assistants.

## Sector-specific risk emphasis
- **Fairness in pricing/underwriting**: proxy discrimination is a central concern — seemingly neutral variables (location, device type, browsing behavior) can correlate strongly with protected attributes and drive unfair pricing outcomes even without explicit protected-attribute use
- **Explainability for adverse decisions**: claim denials and unfavorable pricing decisions often carry regulatory or contractual expectations of explanation, similar to credit decisioning in [financial-services.md](financial-services.md)
- **Data sensitivity**: underwriting often uses health, financial, and behavioral data requiring the strictest privacy handling
- **Agentic claims automation**: autonomous claim approval/denial carries direct financial and customer-trust consequences — apply conservative autonomy levels ([07-agentic-ai/autonomy-and-control.md](../07-agentic-ai/autonomy-and-control.md)) especially for denials

## Applicable regulation (illustrative)
State/national insurance regulators (e.g., IRDAI in India, state insurance commissioners in the US, FCA in the UK) increasingly issuing AI-specific or AI-relevant guidance on underwriting fairness and algorithmic accountability, layered on top of general anti-discrimination and consumer protection law and horizontal AI regulation (e.g., EU AI Act often treats insurance risk-assessment/pricing AI as high-risk).

## Control emphasis
- Proxy variable auditing: explicit testing for indirect discrimination via correlated features, not just direct protected-attribute exclusion ([08-controls-and-techniques/fairness-testing](../08-controls-and-techniques/fairness-testing/README.md))
- Clear, actionable explanation for denied claims and adverse pricing decisions
- Human review pathway for denied claims, particularly for anything agentic-automated
- Documented actuarial/statistical justification for pricing factors, consistent with existing insurance regulatory expectations extended to AI-driven pricing

## Assurance emphasis
Insurance regulators often expect the same rigor applied to traditional actuarial models — extend existing actuarial review/audit processes to cover AI-driven pricing and underwriting rather than treating AI models as exempt from established actuarial governance.
