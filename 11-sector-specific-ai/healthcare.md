# Healthcare

## Common AI use cases
Diagnostic support, clinical decision support, medical imaging analysis, administrative automation (prior authorization, coding), patient-facing chatbots/triage, drug discovery, agentic clinical workflow assistants.

## Sector-specific risk emphasis
- **Safety is paramount**: errors can directly cause physical harm — the highest-stakes application of [05-responsible-ai-principles/safety-and-security.md](../05-responsible-ai-principles/safety-and-security.md) in this repository
- **Fairness in diagnosis/treatment**: documented disparities in AI diagnostic performance across demographic groups (e.g., certain imaging models historically underperforming on darker skin tones) — subgroup testing is not optional here
- **Human oversight is typically mandatory, not optional**: clinical AI is generally expected to support, not replace, clinician judgment — design for human-in-the-loop by default ([05-responsible-ai-principles/accountability-and-human-oversight.md](../05-responsible-ai-principles/accountability-and-human-oversight.md))
- **Hallucination risk in clinical Gen AI**: fabricated clinical information is a patient-safety issue, not just a quality issue — grounding and verification are safety-critical, not optional polish ([06-generative-ai/hallucination-and-grounding.md](../06-generative-ai/hallucination-and-grounding.md))
- **Data sensitivity**: health data is uniformly treated as highly sensitive across essentially every privacy regime — apply the strictest privacy techniques by default ([08-controls-and-techniques/privacy-techniques](../08-controls-and-techniques/privacy-techniques/))

## Applicable regulation (illustrative)
Medical device regulation applying to AI/ML-based diagnostic tools (e.g., FDA in the US, MHRA in the UK, equivalent bodies elsewhere) generally requiring a formal approval/clearance pathway distinct from general AI regulation; health-specific data protection law (HIPAA-style regimes, or health-data provisions within general data protection law like DPDP in India); EU AI Act treats many medical AI applications as high-risk by default.

## Control emphasis
- Formal clinical validation (often via a regulator-defined pathway, not just internal evaluation) before deployment for diagnostic/treatment-affecting AI
- Human oversight design that gives clinicians genuinely actionable, timely information rather than an unreviewable black-box output
- Continuous post-market monitoring, since patient population and clinical practice drift over time — see [02-ai-lifecycle/monitoring-and-observability.md](../02-ai-lifecycle/monitoring-and-observability.md)

## Assurance emphasis
Independent clinical validation, often by a body separate from the developer, is frequently a regulatory requirement rather than a best-practice recommendation — see [04-ai-assurance/independent-assessment.md](../04-ai-assurance/independent-assessment.md) and [04-ai-assurance/conformity-assessment.md](../04-ai-assurance/conformity-assessment.md).
