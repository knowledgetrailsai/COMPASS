# Framework Map

A quick cross-reference of where major external frameworks/standards map into this repository's own structure. Full detail on each lives in [09-tools-and-frameworks](../09-tools-and-frameworks/) (frameworks/standards) or [10-regulations-and-standards](../10-regulations-and-standards/) (binding law).

| External framework | Type | Primary focus | Maps to |
|---|---|---|---|
| NIST AI Risk Management Framework | Framework | Govern/Map/Measure/Manage risk lifecycle | 03-ai-governance, 04-ai-assurance |
| ISO/IEC 42001 | Management-system standard | AI management system (certifiable) | 03-ai-governance |
| ISO/IEC 23894 | Standard | AI risk management guidance | 03-ai-governance/risk-management.md, 04-ai-assurance |
| ISO/IEC 27001 (AI-relevant controls) | Standard | Information security management | 05-responsible-ai-principles/safety-and-security.md, 08-controls-and-techniques |
| OECD AI Principles | Framework (intergovernmental) | High-level principles | 01-foundations/principles.md |
| UNESCO Recommendation on the Ethics of AI | Framework (intergovernmental) | Ethics | 01-foundations/ai-ethics.md |
| EU AI Act | Law | Risk-tiered obligations | 10-regulations-and-standards/EU |
| OWASP Top 10 for LLM Applications | Security guidance | Gen AI/LLM application security | 06-generative-ai, 08-controls-and-techniques |
| MITRE ATLAS | Threat knowledge base | Adversarial ML/AI attack tactics | 04-ai-assurance/red-teaming.md, 08-controls-and-techniques/robustness-testing |
| NIST AI RMF Generative AI Profile | Framework supplement | Gen AI-specific risk profile | 06-generative-ai |

## How to use this map

When a project needs to demonstrate compliance or alignment with a specific external framework, use this table to jump directly to the repository sections implementing the equivalent controls, rather than treating the framework as a separate parallel exercise. Most frameworks map onto the same underlying principles → risks → controls → evidence chain described in [knowledge-map.md](knowledge-map.md) — the differences are mostly in structure, certification mechanics, and legal weight, not in substance.

## Framework selection guidance

- Building a certifiable AI management system → ISO/IEC 42001
- Need a structured internal risk process, not seeking certification → NIST AI RMF
- Need to know binding legal obligations → 10-regulations-and-standards, not this table
- Securing an LLM/Gen AI application → OWASP LLM Top 10 + MITRE ATLAS
- Communicating high-level commitments externally → OECD AI Principles / UNESCO
