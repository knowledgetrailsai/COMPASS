# Framework Comparison

*[Home](../INDEX.md) › [09 · Tools & Frameworks](../09-tools-and-frameworks/commercial-platforms.md)*

| Framework | Type | Binding? | Scope | Certifiable? |
|---|---|---|---|---|
| EU AI Act | Law | Yes (in applicable jurisdiction) | Risk-tiered obligations for AI providers/deployers | N/A (conformity assessment, not certification) |
| NIST AI RMF | Framework | No (voluntary; some US federal contexts reference it) | General AI risk management lifecycle | No |
| ISO/IEC 42001 | Management-system standard | No (voluntary; contractual/procurement mandates possible) | Organizational AI management system | Yes |
| ISO/IEC 23894 | Standard | No | AI risk management methodology | No (supports 42001 certification) |
| OECD AI Principles | Framework (intergovernmental) | No | High-level trustworthy AI principles | No |
| UNESCO Recommendation on AI Ethics | Framework (intergovernmental) | No | Ethics-first, broad societal/rights framing | No |
| OWASP LLM Top 10 | Security guidance | No | LLM application security risks | No |
| MITRE ATLAS | Threat knowledge base | No | Adversarial ML/AI attack techniques | No |

## How to choose

- **Need to prove legal compliance** → identify applicable law first ([10-regulations-and-standards](../10-regulations-and-standards/global-overview.md)), not a framework
- **Need a certifiable claim for customers/procurement** → ISO/IEC 42001
- **Need an internal risk process, no certification needed** → NIST AI RMF, informed by ISO/IEC 23894 methodology
- **Need a public ethics/values statement** → OECD Principles or UNESCO Recommendation
- **Securing an LLM/agentic application** → OWASP LLM Top 10 + MITRE ATLAS together

## The core mistake to avoid

Treating any framework in this table as legally binding, or treating the EU AI Act as "just another framework" alongside voluntary guidance. See [00-navigation-and-methodology/terminology-and-glossary.md](../00-navigation-and-methodology/terminology-and-glossary.md) — law, standard, framework, and guidance are different categories with different consequences for non-compliance.

## Layering frameworks in practice

Most mature organizations use several of these together: a legal baseline from applicable regulation (10), a risk-management backbone from NIST AI RMF or ISO/IEC 23894, security guidance from OWASP/MITRE for Gen AI and agentic systems, and — if pursuing certification — ISO/IEC 42001 as the overarching management system tying it together. They're complementary, not competing, choices.
