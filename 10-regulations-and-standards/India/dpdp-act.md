# India — Digital Personal Data Protection (DPDP) Act & Rules

_Type: Law (Digital Personal Data Protection Act, 2023 + Digital Personal Data Protection Rules, 2025). Last reviewed: 2026-08-19 — confirm current compliance deadlines directly, as the rules include a phased implementation timeline._

## What it is

India's primary data protection law — not an AI-specific statute, but the main binding legal lever on AI systems processing personal data in India, in the absence (as of this review) of a dedicated Indian AI Act. The DPDP Act was passed in 2023; the implementing DPDP Rules, 2025 were notified in November 2025, giving the Act practical effect with a phased compliance timeline for different classes of obligations.

## Core obligations relevant to AI systems

- **Consent and lawful basis**: processing personal data (including data used for training, fine-tuning, or RAG corpora, and data collected through AI-powered products) generally requires clear, specific consent or falls under a "legitimate use" exception defined in the Act
- **Purpose limitation and data minimization**: data collected for one purpose (e.g., customer support) shouldn't be repurposed for AI training without a valid basis
- **Data Principal rights**: individuals have rights to access, correction, and erasure of their personal data — relevant to what's stored in training sets, RAG corpora, and agent memory (see [07-agentic-ai/memory-and-state-risk.md](../../07-agentic-ai/memory-and-state-risk.md))
- **Significant Data Fiduciary obligations**: entities processing data at scale or with higher-risk characteristics face additional obligations, potentially including impact assessments and audits — relevant to high-volume consumer-facing AI products
- **Children's data**: heightened consent and processing restrictions for data relating to minors, relevant to any AI product accessible to or targeting younger users
- **Cross-border data transfer**: the Act empowers the government to restrict transfers to certain jurisdictions — relevant to any AI architecture relying on foreign-hosted model APIs
- **Breach notification**: obligations to notify the Data Protection Board and affected individuals of personal data breaches — extends to AI-system-related data leakage incidents (see [06-generative-ai/data-leakage.md](../../06-generative-ai/data-leakage.md))

## Practical implications for AI systems

- Map every AI system's data flows against DPDP consent/purpose-limitation requirements as part of [02-ai-lifecycle/data-and-data-governance.md](../../02-ai-lifecycle/data-and-data-governance.md)
- Treat a DPIA-equivalent assessment as expected practice for higher-risk AI processing personal data, consistent with [04-ai-assurance/AI-impact-assessment.md](../../04-ai-assurance/AI-impact-assessment.md), even where the Act's specific impact-assessment triggers are still being clarified in practice
- RAG/retrieval systems and agent memory stores need an explicit deletion mechanism that can actually fulfill an erasure request, not just a policy statement

## Relationship to sector regulation

RBI (banking/NBFC), SEBI (securities), and IRDAI (insurance) each layer sector-specific data and AI-use guidance on top of the DPDP Act baseline — see [10-regulations-and-standards/India/sectoral-regulation.md](sectoral-regulation.md) and [11-sector-specific-ai](../../11-sector-specific-ai/).

## Status note

Given the Rules were only recently notified, implementation guidance and enforcement practice are still developing — this is an area to monitor closely rather than treat as settled.

Sources:
- [DPDP Rules, 2025 Notified — Press Information Bureau](https://static.pib.gov.in/WriteReadData/specificdocs/documents/2025/nov/doc20251117695301.pdf)
- [India's DPDP Rules 2025: A practical guide with implementation checklist](https://www.scrut.io/post/dpdp-rules)
- [Digital Personal Data Protection Rules, 2025 — Wikipedia](https://en.wikipedia.org/wiki/Digital_Personal_Data_Protection_Rules,_2025)
