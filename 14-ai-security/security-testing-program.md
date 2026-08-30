# Security Testing Program

*[Home](../INDEX.md) › [14 · AI Security](../14-ai-security/README.md)*

## Bringing the testing methods together

This repository documents AI security testing in several places by necessity — this file is the program-level view tying them together into a coherent cadence.

## Testing methods and where they're detailed

| Method | Detail | Frequency |
|---|---|---|
| Red-teaming (structured adversarial testing) | [04-ai-assurance/red-teaming.md](../04-ai-assurance/red-teaming.md) | Pre-launch (Tier 1 mandatory), quarterly for externally-exposed Gen AI/agentic systems |
| Automated adversarial scanning | [09-tools-and-frameworks/security-tools.md](../09-tools-and-frameworks/security-tools.md) (Garak, promptfoo) | Continuous / every material change (CI-integrated) |
| Robustness/adversarial-example testing | [08-controls-and-techniques/robustness-testing](../08-controls-and-techniques/robustness-testing/README.md) | Pre-launch, on model/data change |
| Penetration testing (infrastructure/application layer around the AI system) | Standard security practice, extended to cover AI-specific endpoints and tool integrations | Per existing security program cadence, at minimum annually for Tier 1 |
| Independent model/system validation | [04-ai-assurance/independent-assessment.md](../04-ai-assurance/independent-assessment.md) | Pre-launch, periodic re-validation |
| Bug bounty (where applicable) | Not detailed elsewhere in this repository — consider for externally-exposed, high-traffic Gen AI/agentic products as a continuous, crowd-sourced complement to scheduled testing | Ongoing, once other testing layers are mature |

## Program design principles

- **Layer automated and manual testing**: automated scanning (Garak, promptfoo) catches known technique regressions cheaply and continuously; manual red-teaming catches novel, creative attacks automated tools miss — neither replaces the other
- **Test the actual enforced boundary, not the intended one**: per the lesson in [12-case-studies/agentic-failures/aisi-unsanctioned-agent-behavior.md](../12-case-studies/agentic-failures/aisi-unsanctioned-agent-behavior.md), verify containment technically, don't assume it from configuration
- **Scope testing using the threat model**: use [ai-threat-model.md](ai-threat-model.md) to ensure test scope covers the full applicable attack surface for the specific system type, rather than a generic checklist
- **Track findings to closure**: unresolved high-severity findings block launch/continued operation regardless of tier — see [04-ai-assurance/red-teaming.md](../04-ai-assurance/red-teaming.md#gate)

## Building an internal AI red team

For organizations with sufficient AI system volume, a dedicated internal AI red-team function (organizationally independent from build teams, per [04-ai-assurance/independent-assessment.md](../04-ai-assurance/independent-assessment.md)) is the most cost-effective way to sustain the testing cadence this program requires, reserving external specialist engagement for the highest-stakes systems.

## Related

- [security-metrics-and-reporting.md](security-metrics-and-reporting.md)
- [security-incident-response.md](security-incident-response.md)
