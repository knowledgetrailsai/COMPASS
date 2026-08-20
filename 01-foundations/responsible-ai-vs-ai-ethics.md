# Responsible AI vs. AI Ethics vs. AI Governance vs. AI Assurance

These four terms are often used interchangeably, which causes real confusion about what a given team or document is actually responsible for. This repository treats them as distinct, connected layers.

## The four layers

### AI Ethics — what *ought* to be done
The normative, philosophical layer: what values should an AI system embody, whose interests should it serve, and should a given system be built at all. Draws on moral philosophy, human rights frameworks, and societal values. See [ai-ethics.md](ai-ethics.md).

### Responsible AI — how those expectations become practice
The translation layer: converting ethical commitments and stakeholder expectations into concrete engineering and organizational practices — fairness testing, transparency mechanisms, safety guardrails, documentation. This is the operational discipline most of this repository covers.

### AI Governance — how practice is institutionalized
The organizational layer: structures, roles, policies, and decision rights that make Responsible AI practices consistent, enforceable, and auditable across an organization rather than dependent on individual goodwill. See [03-ai-governance](../03-ai-governance/).

### AI Assurance — how you prove it actually works
The verification layer: independent or systematic evidence that governance and RAI practices are functioning as intended — audits, red-teaming, conformity assessment, documented evidence trails. See [04-ai-assurance](../04-ai-assurance/).

## Why the distinction matters

- A system can be **ethically well-intentioned** but **operationally irresponsible** (no bias testing, no monitoring).
- A system can have **good RAI practices** applied inconsistently because there's **no governance** enforcing them org-wide.
- An organization can have **governance on paper** with **no assurance** that it's actually followed — policies that exist but aren't tested or audited.

Each layer is necessary; none is sufficient alone.

## A worked example

*Should we build an AI system that scores job candidates?* — an ethics question (fairness to applicants, dignity of work, power asymmetry between employer and candidate).

*Given we're building it, how do we make it fair and transparent?* — a Responsible AI question (bias testing methodology, explainability approach).

*How do we make sure every hiring AI project at this company follows that methodology?* — a governance question (policy, review board, risk tiering).

*How do we prove to a regulator or auditor that we actually did?* — an assurance question (documented evidence, independent audit, conformity assessment).

## Relationship to this repository's structure

| Layer | Primary section |
|---|---|
| Ethics | 01-foundations (this section) |
| Responsible AI practice | 05, 06, 07, 08 |
| Governance | 02, 03 |
| Assurance | 04 |
