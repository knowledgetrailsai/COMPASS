# RACI — AI Governance Activities

*[Home](../INDEX.md) › [03 · AI Governance](../03-ai-governance/AI-assurance.md)*

R = Responsible (does the work), A = Accountable (answers for it), C = Consulted, I = Informed

| Activity | System Owner | Data Science/Eng | Product | Legal/Privacy | Governance Board | Security |
|---|---|---|---|---|---|---|
| Use case scoping & risk tiering | A | C | R | C | I | I |
| Requirements & acceptance criteria | A | R | R | C | I | I |
| Data governance / DPIA | C | R | I | A | I | I |
| Fairness/bias testing | C | R | I | C | I | I |
| Red-teaming / adversarial testing | C | C | I | I | I | R/A |
| Model card / system card | A | R | C | C | I | I |
| Tier 1 launch approval | R | C | C | C | A | C |
| Tool/permission scoping (agentic) | A | R | C | C | I | C |
| Production monitoring | A | R | I | I | I | I |
| Incident triage | R | R | C | C | I(SEV3)/A(SEV1) | R |
| Post-incident review | A | R | C | C | I | C |
| Third-party/vendor AI assessment | C | I | C | A | I | C |
| Retirement/decommissioning | A | R | I | C | I | I |

## Notes

- Governance Board accountability (A) generally applies at Tier 1 only; Tier 2–3 defaults to System Owner accountability with lighter Board involvement (I).
- Security's R/A on red-teaming reflects that adversarial testing should be led or independently verified by a function separate from the build team.
- Adapt column names/roles to your organization's actual structure — the point of a RACI is unambiguous single-point accountability per row, not a template followed verbatim.
