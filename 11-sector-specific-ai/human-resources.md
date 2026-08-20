# Human Resources

*[Home](../INDEX.md) › [11 · Sector-Specific AI](../11-sector-specific-ai/)*

## Common AI use cases
Resume screening, candidate ranking/scoring, interview analysis, performance evaluation support, workforce analytics, AI-driven scheduling/task allocation, agentic recruiting assistants.

## Sector-specific risk emphasis
- **Fairness in hiring/promotion**: among the most heavily scrutinized AI fairness applications, given direct impact on economic opportunity and well-established anti-discrimination law
- **Explainability for candidates and employees**: rejected candidates and employees affected by AI-driven decisions increasingly have a right to know AI was involved and, in some jurisdictions, to an explanation
- **Proxy discrimination**: resume-screening models can learn to proxy for protected attributes through seemingly neutral signals (school names, gaps in employment, certain phrasing patterns) — see [05-responsible-ai-principles/fairness-and-bias.md](../05-responsible-ai-principles/fairness-and-bias.md)
- **Worker surveillance/autonomy concerns**: AI-driven performance monitoring and workforce analytics raise distinct dignity and autonomy concerns beyond pure fairness — see [01-foundations/human-rights-and-ai.md](../01-foundations/human-rights-and-ai.md) (right to work / economic rights)
- **Interview analysis tools** (facial/voice/emotion analysis in hiring): a category facing specific regulatory restriction or prohibition in multiple jurisdictions given weak scientific validity and elevated bias risk — treat as high scrutiny by default

## Applicable regulation (illustrative)
Employment discrimination law generally applies to AI-assisted decisions the same as human ones (e.g., EEOC guidance on AI in employment in the US); several jurisdictions have hiring-AI-specific disclosure/audit laws (e.g., New York City's automated employment decision tool law as a widely-referenced example of this category); EU AI Act classifies most employment-related AI as high-risk by default.

## Control emphasis
- Mandatory bias audits before deployment and on a recurring cadence, often with a specific legal requirement in some jurisdictions for independent audit
- Human review of AI-driven rejection decisions, not full automation, particularly at the final-decision stage
- Clear candidate/employee disclosure that AI is used in the process
- Avoid facial/emotion analysis-based candidate scoring given weak validity and elevated regulatory scrutiny — favor structured, validated assessment methods instead

## Assurance emphasis
Where jurisdiction-mandated independent bias audits apply (increasingly common for hiring AI specifically), treat this as a hard compliance gate — see [04-ai-assurance/independent-assessment.md](../04-ai-assurance/independent-assessment.md) — not a discretionary best practice.
