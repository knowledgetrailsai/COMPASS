# Risk Tiering

## Why tier

Not every AI use case warrants the same scrutiny. Risk tiering lets governance effort scale with actual risk — informed heavily by the EU AI Act's risk-based approach (unacceptable / high / limited / minimal risk).

## Suggested tiers

### Tier 0 — Prohibited
Use cases banned outright: social scoring of individuals, real-time biometric categorization in public spaces for law enforcement (with narrow exceptions), manipulative AI exploiting vulnerabilities, subliminal manipulation. Mirrors EU AI Act Article 5 prohibited practices.

### Tier 1 — High risk
Materially affects rights, safety, or access to opportunity: hiring/promotion decisions, credit/lending, insurance underwriting, medical diagnosis support, law enforcement/judicial support, critical infrastructure control, autonomous agents with authority to take consequential actions (financial transactions, irreversible operations) without human confirmation.
**Requires**: governance board approval, full documentation, bias testing, human oversight mechanism, ongoing monitoring, DPIA if personal data involved.

### Tier 2 — Medium risk
Meaningful but bounded impact: internal productivity tools with human review of outputs, customer-facing chatbots for non-critical support, content generation with human-in-the-loop publishing, recommendation systems.
**Requires**: lightweight review, documented testing, disclosure to users, monitoring for drift/misuse.

### Tier 3 — Low / minimal risk
Limited blast radius: internal drafting assistance, code completion, summarization of non-sensitive internal documents.
**Requires**: self-certification checklist, standard terms of use, awareness of acceptable-use policy.

## Tiering questions (use to classify a new use case)

1. Does the system make or materially influence a decision about a person (employment, credit, benefits, legal status, safety)?
2. Can the system take autonomous action with real-world or financial consequences (agentic)?
3. Does it process sensitive personal data, biometric data, or data about vulnerable populations?
4. What is the blast radius if it fails or is misused — one user, many users, or systemic?
5. Is a human required to review/approve outputs before they take effect?
6. Is this a "high-risk" category under applicable regulation (check [10-regulations-and-standards](../10-regulations-and-standards/))?

## Agentic AI note

Tiering agentic systems should weight **autonomy level** and **tool/action scope** heavily — an agent that can only read data is lower risk than one that can send emails, move money, or modify production systems, even performing "the same task." See [07-agentic-ai/autonomy-and-control.md](../07-agentic-ai/autonomy-and-control.md).

## Re-tiering

Risk tier isn't static — re-assess when scope expands (new data sources, new tool access, new user population) or after a near-miss/incident.
