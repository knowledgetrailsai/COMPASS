# Public Sector

*[Home](../INDEX.md) › [11 · Sector-Specific AI](../11-sector-specific-ai/README.md)*

## Common AI use cases
Benefits eligibility determination, fraud detection in public programs, law enforcement/predictive policing tools, permitting/licensing automation, public service chatbots, agentic case-management assistants.

## Sector-specific risk emphasis
- **Highest human rights stakes**: public sector AI directly mediates access to rights and essential services (benefits, licenses, due process) — apply [01-foundations/human-rights-and-ai.md](../01-foundations/human-rights-and-ai.md) rigorously, and treat most consequential public-sector AI as Tier 1 by default
- **Due process and contestability**: affected individuals typically have a stronger legal expectation of explanation and appeal for government decisions than for private-sector ones — see [05-responsible-ai-principles/accountability-and-human-oversight.md](../05-responsible-ai-principles/accountability-and-human-oversight.md)
- **Power asymmetry**: citizens generally cannot opt out of interacting with government systems the way they can choose a different private vendor, raising the bar for fairness and transparency
- **Predictive policing/surveillance-adjacent use cases**: carry acute fairness and civil liberties risk given documented historical bias in underlying crime data, and are subject to outright prohibition or severe restriction in some regulatory regimes (e.g., specific EU AI Act prohibitions touch this category)
- **Vulnerable population impact**: benefits/eligibility AI disproportionately affects lower-income and otherwise vulnerable populations — apply the fairness and human-rights review with particular attention to this population

## Applicable regulation (illustrative)
Often the most stringent regulatory tier in any given framework — the EU AI Act, for instance, treats many public-sector AI uses (law enforcement, migration, benefits eligibility, essential public services) as high-risk by default; administrative law and due process requirements apply independent of AI-specific regulation; several jurisdictions have public-sector-specific algorithmic accountability laws or procurement requirements (e.g., requiring an algorithmic impact assessment before public-sector AI deployment).

## Control emphasis
- Meaningful human review and appeal pathway for any AI-influenced decision affecting access to a public service or right
- Public transparency about AI use in government systems, often exceeding private-sector disclosure norms
- Independent, often externally-mandated review before deployment — see [04-ai-assurance/independent-assessment.md](../04-ai-assurance/independent-assessment.md)
- Explicit prohibition review against [03-ai-governance/risk-management.md](../03-ai-governance/risk-management.md) Tier 0 categories before any surveillance-adjacent use case proceeds

## Assurance emphasis
Public-sector AI often faces the highest public scrutiny and legal challenge risk of any category in this repository — invest in full [04-ai-assurance](../04-ai-assurance/assurance-overview.md) rigor (impact assessment, independent assessment, audit, red-teaming) as a default rather than a risk-tier-dependent choice.
