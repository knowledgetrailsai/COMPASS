# Retail

*[Home](../INDEX.md) › [11 · Sector-Specific AI](../11-sector-specific-ai/README.md)*

## Common AI use cases
Product recommendation, dynamic/personalized pricing, demand forecasting, customer service chatbots, fraud detection, agentic shopping/inventory assistants.

## Sector-specific risk emphasis
- **Personalization vs. manipulation**: recommendation and personalized-pricing systems sit close to the line between legitimate personalization and manipulative practice (e.g., price discrimination that exploits individual willingness-to-pay signals, or engagement-optimized recommendation that exploits attention/compulsive behavior) — see [01-foundations/ai-ethics.md](../01-foundations/ai-ethics.md)
- **Dynamic pricing fairness**: personalized pricing can create de facto discriminatory outcomes across demographic or geographic lines even without explicit protected-attribute use. Apply proxy-discrimination scrutiny similar to [insurance.md](insurance.md) and [financial-services.md](financial-services.md)
- **Dark pattern risk in Gen AI/agentic shopping assistants**: conversational commerce agents can blur into manipulative sales tactics if not deliberately designed against it: a consumer-protection-adjacent risk beyond the standard RAI categories
- **Data volume and profiling**: retail AI often involves extensive behavioral data collection and profiling, warranting close attention to [05-responsible-ai-principles/privacy-and-data-protection.md](../05-responsible-ai-principles/privacy-and-data-protection.md)

## Applicable regulation (illustrative)
General consumer protection law (unfair/deceptive practices authority) applies directly to manipulative AI-driven sales/pricing practices; data protection law governs the underlying behavioral profiling; some jurisdictions have specific rules or proposed rules on algorithmic/personalized pricing transparency.

## Control emphasis
- Clear boundaries on personalization vs. manipulation, defined in policy ([03-ai-governance/policy-management.md](../03-ai-governance/policy-management.md)) rather than left to individual product teams' judgment
- Disclosure when pricing is personalized/dynamic, where required or as a trust-building practice even where not strictly mandated
- Guardrails on agentic shopping assistants to prevent manipulative upsell patterns — treat this as a safety/ethics guardrail category, not just a business tuning parameter

## Assurance emphasis
Periodic fairness testing of pricing/recommendation outcomes across demographic and geographic segments, even absent a specific "high-risk" regulatory classification, given the reputational and consumer-trust stakes of a perceived-discriminatory pricing incident.
