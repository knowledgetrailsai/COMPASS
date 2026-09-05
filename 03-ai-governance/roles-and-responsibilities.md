# Roles and Responsibilities

*[Home](../INDEX.md) › [03 · AI Governance](../03-ai-governance/AI-assurance.md)*

Builds on [01-foundations/stakeholder-roles.md](../01-foundations/stakeholder-roles.md) with the specific governance-layer roles needed to operate the framework in [ai-governance-framework.md](ai-governance-framework.md).

## Core governance roles

### AI Governance Lead / Head of Responsible AI
Owns the overall governance framework, chairs or co-chairs the governance board, tracks the AI inventory, and reports risk posture to leadership.

### AI Governance Board / Council members
Cross-functional representatives (product, engineering, legal, security, privacy, ethics/DEI where applicable) who review and approve Tier 1 use cases and set policy. See [ai-governance-board.md](ai-governance-board.md).

### System Owner (per AI system)
The named, accountable individual for a specific AI system's behavior — responsible for ensuring lifecycle checkpoints are met, documentation is current, and monitoring is active. Every Tier 1–2 system must have one.

### Model/Technical Reviewer
Provides independent technical review of evaluation results for Tier 1 systems; should not be the same person who built the system, to avoid confirmation bias.

### Privacy/Data Protection Officer
Reviews DPIAs, data handling practices, and privacy-by-design compliance for AI systems processing personal data.

### Security Reviewer
Assesses AI-specific attack surface (prompt injection, tool abuse, model extraction) as part of Tier 1 review and incident response.

### Business/Product Owner
Defines intended use, balances business goals against risk tolerance, and is accountable for user-facing decisions like disclosure and consent design.

## See also RACI

For activity-level responsibility assignment across these roles, see [RACI.md](RACI.md).

## Sizing this to your organization

Small organizations can combine several of these roles in one or two people; the key is that each function above is *explicitly assigned to someone*, even informally, rather than assumed to be "everyone's job" (which in practice becomes no one's job).
