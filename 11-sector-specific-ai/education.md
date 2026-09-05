# Education

*[Home](../INDEX.md) › [11 · Sector-Specific AI](../11-sector-specific-ai/README.md)*

## Common AI use cases
Adaptive learning platforms, automated grading/assessment, plagiarism/AI-content detection, admissions support, student support chatbots, agentic tutoring assistants.

## Sector-specific risk emphasis
- **Children's rights and heightened protection**: a large share of education AI serves minors, triggering the strictest consent, data protection, and content-safety considerations across virtually every regulatory regime: see [01-foundations/human-rights-and-ai.md](../01-foundations/human-rights-and-ai.md)
- **Fairness in assessment/admissions**: AI-assisted grading or admissions scoring carries the same disparate-impact concerns as hiring, with added sensitivity given the long-term life impact of educational access decisions
- **Detection tool reliability**: AI-content/plagiarism detectors have documented false-positive risk, disproportionately affecting non-native English speakers in some studies. Treat detector output as a signal requiring human judgment, never as automated grounds for an accusation of misconduct
- **Overreliance and skill development concerns**: unlike most sectors, education has a distinct pedagogical risk dimension — AI tools that do the learning task for the student rather than supporting learning can undermine the educational purpose itself, a consideration beyond standard RAI risk categories
- **Data sensitivity**: student data (including performance and behavioral data on minors) warrants strict minimization and retention limits

## Applicable regulation (illustrative)
Children's privacy law (e.g., COPPA-style regimes, DPDP Act's specific provisions for children's data in India) applies directly; education-specific privacy law in some jurisdictions (e.g., FERPA in the US); general AI regulation frequently treats education access/assessment AI as high-risk (e.g., EU AI Act).

## Control emphasis
- Parental/guardian consent mechanisms where required by age and jurisdiction
- Human review of any AI-assisted decision with material educational consequence (grading disputes, admissions, misconduct accusations)
- Conservative default settings for any AI tool accessible to minors (content filtering, data minimization) rather than opt-out defaults
- Pedagogical review, not just technical evaluation, for tools that could affect learning outcomes, a discipline-specific addition beyond the standard evaluation chain

## Assurance emphasis
Given the children's-data sensitivity, apply DPIA-equivalent assessment ([04-ai-assurance/AI-impact-assessment.md](../04-ai-assurance/AI-impact-assessment.md)) as a default requirement rather than reserving it for the highest risk tier only.
