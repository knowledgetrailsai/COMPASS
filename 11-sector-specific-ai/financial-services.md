# Financial Services

## Common AI use cases
Credit/lending decisioning, fraud detection, algorithmic trading, robo-advisory, AML/KYC screening, customer service chatbots, insurance-adjacent underwriting support.

## Sector-specific risk emphasis
- **Fairness in credit/lending**: disparate impact in approval rates, pricing, and terms across protected groups — among the most heavily scrutinized fairness applications globally
- **Explainability**: adverse action notices (why a credit application was denied) are often a direct legal requirement, not just good practice — see [05-responsible-ai-principles/transparency-and-explainability.md](../05-responsible-ai-principles/transparency-and-explainability.md)
- **Model risk management**: financial regulators have long-standing model risk management expectations (originally developed for traditional quantitative models) that now extend to AI/ML models
- **Market conduct/manipulation**: algorithmic trading systems carry systemic and market-manipulation risk distinct from consumer-facing AI risk
- **Agentic AI in finance**: autonomous transaction execution, automated customer communications — apply [07-agentic-ai/autonomy-and-control.md](../07-agentic-ai/autonomy-and-control.md) with particular weight on approval gates for anything moving money

## Applicable regulation (illustrative — verify current requirements per jurisdiction)
Fair lending laws (e.g., ECOA/Regulation B and FCRA in the US), banking regulator model risk management guidance, RBI digital lending guidelines (India), MAS FEAT principles (Singapore), FCA guidance (UK) — see [10-regulations-and-standards](../10-regulations-and-standards/) and [11-sector-specific-ai](README.md) pattern.

## Control emphasis
- Rigorous, documented fairness testing with defined acceptability thresholds before any credit/pricing model launches ([08-controls-and-techniques/fairness-testing](../08-controls-and-techniques/fairness-testing/))
- Explainability sufficient to generate compliant adverse action notices, not just internal debugging explanations
- Independent model validation function, often already required by existing model risk management regulation — extend its scope to AI/ML models rather than building a parallel process
- Strong audit trail for every credit/trading decision ([04-ai-assurance/evidence-and-traceability.md](../04-ai-assurance/evidence-and-traceability.md))

## Assurance emphasis
Given existing regulatory examination practice in this sector, treat [04-ai-assurance/audit.md](../04-ai-assurance/audit.md) and [04-ai-assurance/independent-assessment.md](../04-ai-assurance/independent-assessment.md) as baseline expectations, not optional rigor — financial regulators are accustomed to demanding this level of evidence for traditional models and will expect no less for AI.
