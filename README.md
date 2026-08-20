# Responsible AI Guide

A comprehensive Responsible AI knowledge base — covering traditional ML, Generative AI, and Agentic AI — organized as a **control plane**, not an encyclopedia. Content flows through a consistent chain so any risk can be traced from principle to proof:

```
PRINCIPLES → RISKS → REQUIREMENTS → CONTROLS → TEST/EVALUATE → EVIDENCE → ASSURANCE
```

applied across the AI lifecycle, across AI types (Gen AI, Agentic AI), and across stakeholders, jurisdictions, and sectors. See [00-navigation-and-methodology/knowledge-map.md](00-navigation-and-methodology/knowledge-map.md) for the full model, including a worked example tracing one risk end-to-end through every section below.

## Start here

New to this repository? Read [00-navigation-and-methodology/how-to-use-this-repository.md](00-navigation-and-methodology/how-to-use-this-repository.md) — it routes you to the right section based on your role and task.

Three ways to navigate, depending on what you already know:

| You know... | Use |
|---|---|
| The section (e.g. "I need 06-generative-ai") | The repository structure below, or browse the folders directly |
| The topic, not the section (e.g. "privacy," "security") | [00-navigation-and-methodology/topic-index.md](00-navigation-and-methodology/topic-index.md) — groups files across sections by theme |
| Nothing yet, want to scan everything | [INDEX.md](INDEX.md) — every file in the repository, one flat list |

Every file also carries a breadcrumb (`Home › Section › ...`) at the top so you always know where you are and can jump back out.

## Repository structure

Every file in the repository, grouped by section — the same listing as [INDEX.md](INDEX.md), kept here so the structure is visible without leaving the README. If this list and INDEX.md ever drift, INDEX.md is the source of truth.

### 00 · Navigation and Methodology

- [Framework Map](00-navigation-and-methodology/framework-map.md)
- [How to Use This Repository](00-navigation-and-methodology/how-to-use-this-repository.md)
- [Knowledge Map](00-navigation-and-methodology/knowledge-map.md)
- [Source and Evidence Policy](00-navigation-and-methodology/source-and-evidence-policy.md)
- [Terminology — Key Distinctions](00-navigation-and-methodology/terminology-and-glossary.md)
- [Topic Index](00-navigation-and-methodology/topic-index.md)

### 01 · Foundations

- [AI Ethics](01-foundations/ai-ethics.md)
- [Human Rights and AI](01-foundations/human-rights-and-ai.md)
- [Core Principles](01-foundations/principles.md)
- [Responsible AI vs. AI Ethics vs. AI Governance vs. AI Assurance](01-foundations/responsible-ai-vs-ai-ethics.md)
- [Risk Taxonomy](01-foundations/risk-taxonomy.md)
- [Stakeholder Roles](01-foundations/stakeholder-roles.md)
- [What is Responsible AI](01-foundations/what-is-responsible-ai.md)

### 02 · AI Lifecycle

- [Stage 3: Data & Data Governance](02-ai-lifecycle/data-and-data-governance.md)
- [Stage 6: Deployment & Release](02-ai-lifecycle/deployment-and-release.md)
- [Stage 5: Evaluation & Validation](02-ai-lifecycle/evaluation-and-validation.md)
- [AI Incident Response](02-ai-lifecycle/incident-and-remediation.md)
- [AI Lifecycle Overview](02-ai-lifecycle/lifecycle-overview.md)
- [Stage 4: Model Development](02-ai-lifecycle/model-development.md)
- [Stage 7: Monitoring & Observability](02-ai-lifecycle/monitoring-and-observability.md)
- [Stage 1: Opportunity & Use Case](02-ai-lifecycle/opportunity-and-use-case.md)
- [Stage 2: Requirements & Design](02-ai-lifecycle/requirements-and-design.md)
- [Stage 9: Retirement & Decommissioning](02-ai-lifecycle/retirement-and-decommissioning.md)

### 03 · AI Governance

- [AI Assurance (Governance Pointer)](03-ai-governance/AI-assurance.md)
- [RACI — AI Governance Activities](03-ai-governance/RACI.md)
- [AI Governance Board](03-ai-governance/ai-governance-board.md)
- [AI Governance Framework](03-ai-governance/ai-governance-framework.md)
- [Governance Models](03-ai-governance/governance-models.md)
- [Policy Management](03-ai-governance/policy-management.md)
- [Risk Tiering](03-ai-governance/risk-management.md)
- [Roles and Responsibilities](03-ai-governance/roles-and-responsibilities.md)
- [Third-Party AI Governance](03-ai-governance/third-party-ai-governance.md)

### 04 · AI Assurance

- [AI Impact Assessment](04-ai-assurance/AI-impact-assessment.md)
- [AI Risk Assessment](04-ai-assurance/AI-risk-assessment.md)
- [AI Assurance — Overview](04-ai-assurance/assurance-overview.md)
- [Assurance Reporting](04-ai-assurance/assurance-reporting.md)
- [AI Audit](04-ai-assurance/audit.md)
- [Conformity Assessment](04-ai-assurance/conformity-assessment.md)
- [Documentation Artifacts](04-ai-assurance/evidence-and-traceability.md)
- [Independent Assessment](04-ai-assurance/independent-assessment.md)
- [Model Validation](04-ai-assurance/model-validation.md)
- [Red-Teaming](04-ai-assurance/red-teaming.md)

### 05 · Responsible AI Principles

- [Accountability and Human Oversight](05-responsible-ai-principles/accountability-and-human-oversight.md)
- [Fairness and Bias](05-responsible-ai-principles/fairness-and-bias.md)
- [Privacy and Data Protection](05-responsible-ai-principles/privacy-and-data-protection.md)
- [Robustness and Reliability](05-responsible-ai-principles/robustness-and-reliability.md)
- [Safety and Security](05-responsible-ai-principles/safety-and-security.md)
- [Sustainability](05-responsible-ai-principles/sustainability.md)
- [Transparency and Explainability](05-responsible-ai-principles/transparency-and-explainability.md)

### 06 · Generative AI

- [RAG-Specific Considerations](06-generative-ai/RAG-governance.md)
- [Content Provenance and Authenticity](06-generative-ai/content-provenance.md)
- [Copyright and IP Considerations](06-generative-ai/copyright-and-ip.md)
- [Data Leakage (Generative AI)](06-generative-ai/data-leakage.md)
- [Fine-Tuning Governance](06-generative-ai/fine-tuning-governance.md)
- [Generative AI Evaluation](06-generative-ai/genai-evaluation.md)
- [Generative AI — Specific Risks](06-generative-ai/genai-risk-landscape.md)
- [Hallucination and Grounding](06-generative-ai/hallucination-and-grounding.md)
- [Jailbreaking](06-generative-ai/jailbreaks.md)
- [Prompt and Output Safety](06-generative-ai/prompt-and-output-safety.md)
- [Prompt Injection](06-generative-ai/prompt-injection.md)
- [Synthetic Content](06-generative-ai/synthetic-content.md)

### 07 · Agentic AI

- [Agent Incident Response](07-agentic-ai/agent-incident-response.md)
- [Agent Observability](07-agentic-ai/agent-observability.md)
- [Agentic Evaluation](07-agentic-ai/agentic-evaluation.md)
- [Agentic AI — Risk Landscape](07-agentic-ai/agentic-risk-landscape.md)
- [Autonomy and Control](07-agentic-ai/autonomy-and-control.md)
- [Human-Agent Interaction](07-agentic-ai/human-agent-interaction.md)
- [Identity and Authorization for Agents](07-agentic-ai/identity-and-authorization.md)
- [Memory and State Risk](07-agentic-ai/memory-and-state-risk.md)
- [Multi-Agent Governance](07-agentic-ai/multi-agent-governance.md)
- [Planning and Reasoning Risk](07-agentic-ai/planning-and-reasoning-risk.md)
- [Tool Use and Permissions](07-agentic-ai/tool-use-and-permissions.md)

### 08 · Controls and Techniques

- [Controls and Techniques](08-controls-and-techniques/README.md)
- [Guardrails and Runtime Controls](08-controls-and-techniques/guardrails-and-controls.md)
  - **evaluation-and-benchmarking/**
    - [Evaluation and Benchmarking](08-controls-and-techniques/evaluation-and-benchmarking/README.md)
  - **explainability/**
    - [Explainability Techniques](08-controls-and-techniques/explainability/README.md)
  - **fairness-testing/**
    - [Fairness Testing](08-controls-and-techniques/fairness-testing/README.md)
  - **monitoring-and-observability/**
    - [Monitoring and Observability Techniques](08-controls-and-techniques/monitoring-and-observability/README.md)
  - **privacy-techniques/**
    - [Privacy Techniques](08-controls-and-techniques/privacy-techniques/README.md)
  - **robustness-testing/**
    - [Robustness Testing](08-controls-and-techniques/robustness-testing/README.md)

### 09 · Tools and Frameworks

- [ISO/IEC 23894](09-tools-and-frameworks/ISO-23894.md)
- [ISO/IEC 42001](09-tools-and-frameworks/ISO-42001.md)
- [MITRE ATLAS](09-tools-and-frameworks/MITRE-ATLAS.md)
- [NIST AI Risk Management Framework (AI RMF)](09-tools-and-frameworks/NIST-AI-RMF.md)
- [OECD AI Principles](09-tools-and-frameworks/OECD-AI-principles.md)
- [OWASP Top 10 for LLM Applications](09-tools-and-frameworks/OWASP-llm-top10.md)
- [UNESCO Recommendation on the Ethics of AI](09-tools-and-frameworks/UNESCO-AI-ethics.md)
- [Commercial / Vendor Platforms](09-tools-and-frameworks/commercial-platforms.md)
- [Evaluation Frameworks](09-tools-and-frameworks/evaluation-frameworks.md)
- [Framework Comparison](09-tools-and-frameworks/framework-comparison.md)
- [Governance Platforms](09-tools-and-frameworks/governance-platforms.md)
- [Observability Tools](09-tools-and-frameworks/observability-tools.md)
- [Open-Source Tools](09-tools-and-frameworks/open-source-tools.md)
- [Security Tools](09-tools-and-frameworks/security-tools.md)
- [Tool Selection Matrix](09-tools-and-frameworks/tool-selection-matrix.md)

### 10 · Regulations and Standards

- [Global Regulatory Overview](10-regulations-and-standards/global-overview.md)
- [Regulatory Comparison](10-regulations-and-standards/regulatory-comparison.md)
  - **Canada/**
    - [Canada — AI Regulation](10-regulations-and-standards/Canada/canada-ai-regulation.md)
  - **China/**
    - [China — AI Regulation](10-regulations-and-standards/China/china-ai-regulation.md)
  - **EU/**
    - [EU AI Act](10-regulations-and-standards/EU/eu-ai-act.md)
  - **India/**
    - [India — Digital Personal Data Protection (DPDP) Act & Rules](10-regulations-and-standards/India/dpdp-act.md)
    - [India — Sectoral AI Guidance](10-regulations-and-standards/India/sectoral-regulation.md)
  - **Singapore/**
    - [Singapore — AI Regulation](10-regulations-and-standards/Singapore/singapore-ai-regulation.md)
  - **UK/**
    - [UK — AI Regulation](10-regulations-and-standards/UK/uk-ai-regulation.md)
  - **US/**
    - [US — Federal AI Policy](10-regulations-and-standards/US/federal.md)
    - [US — State AI Laws](10-regulations-and-standards/US/state-laws.md)

### 11 · Sector-Specific AI

- [Sector-Specific AI](11-sector-specific-ai/README.md)
- [Critical Infrastructure](11-sector-specific-ai/critical-infrastructure.md)
- [Education](11-sector-specific-ai/education.md)
- [Financial Services](11-sector-specific-ai/financial-services.md)
- [Healthcare](11-sector-specific-ai/healthcare.md)
- [Human Resources](11-sector-specific-ai/human-resources.md)
- [Insurance](11-sector-specific-ai/insurance.md)
- [Manufacturing](11-sector-specific-ai/manufacturing.md)
- [Public Sector](11-sector-specific-ai/public-sector.md)
- [Retail](11-sector-specific-ai/retail.md)

### 12 · Case Studies

- [Case Study Template](12-case-studies/case-study-template.md)
  - **agentic-failures/**
    - [AISI Incident: Unsanctioned Agent Behaviour During Cyber Testing](12-case-studies/agentic-failures/aisi-unsanctioned-agent-behavior.md)
  - **bias-and-discrimination/**
    - [Amazon's Experimental AI Recruiting Tool](12-case-studies/bias-and-discrimination/amazon-recruiting-tool.md)
    - [COMPAS Recidivism Risk Scoring](12-case-studies/bias-and-discrimination/compas-recidivism.md)
  - **failures/**
    - [Zillow Offers Home-Pricing Algorithm Failure](12-case-studies/failures/zillow-ibuying-algorithm.md)
  - **good-practices/**
    - [Widespread Adoption of Model Cards and Datasheets](12-case-studies/good-practices/model-cards-and-datasheets-adoption.md)
  - **hallucination-and-reliability/**
    - [Air Canada Chatbot Bereavement Fare Case](12-case-studies/hallucination-and-reliability/air-canada-chatbot.md)
  - **privacy-incidents/**
    - [Samsung Employees' Confidential Data Leak via ChatGPT](12-case-studies/privacy-incidents/samsung-chatgpt-leak.md)
  - **regulatory-actions/**
    - [Dutch Childcare Benefits Scandal (Toeslagenaffaire)](12-case-studies/regulatory-actions/dutch-childcare-benefits-scandal.md)
  - **security-incidents/**
    - [Microsoft Tay Chatbot](12-case-studies/security-incidents/microsoft-tay.md)

### 13 · Implementation Playbooks

- [Playbook: Agentic AI Deployment Checklist](13-implementation-playbooks/agentic-deployment-checklist.md)
- [Playbook: Conducting an AI Risk Assessment](13-implementation-playbooks/conducting-an-ai-risk-assessment.md)
- [Playbook: Gen AI App Launch Checklist](13-implementation-playbooks/genai-app-launch-checklist.md)
- [Playbook: Model / System Card Template](13-implementation-playbooks/model-card-template.md)
- [Playbook: Vendor / Third-Party AI Assessment](13-implementation-playbooks/vendor-third-party-ai-assessment.md)

### 14 · AI Security

- [AI Security](14-ai-security/README.md)
- [AI Threat Model](14-ai-security/ai-threat-model.md)
- [Securing Agentic AI](14-ai-security/securing-agentic-ai.md)
- [Securing Generative AI](14-ai-security/securing-genai.md)
- [Securing Traditional ML](14-ai-security/securing-traditional-ml.md)
- [AI Security Incident Response](14-ai-security/security-incident-response.md)
- [Security Metrics and Reporting](14-ai-security/security-metrics-and-reporting.md)
- [Security Testing Program](14-ai-security/security-testing-program.md)
- [AI Supply Chain Security](14-ai-security/supply-chain-security.md)

### Glossary

- [AI Glossary](glossary/ai-glossary.md)

### Templates

- [Templates](templates/README.md)

### Assets

- [Assets](assets/README.md)

### Root

- [Responsible AI Guide](README.md)
- [Contributing](CONTRIBUTING.md)

Not sure which section has what you need? [topic-index.md](00-navigation-and-methodology/topic-index.md) groups the same files by theme instead of by section.

## Key distinctions this repository maintains

- **Ethics ≠ Responsible AI ≠ Governance ≠ Assurance** — four different layers, not synonyms. See [01-foundations/responsible-ai-vs-ai-ethics.md](01-foundations/responsible-ai-vs-ai-ethics.md).
- **Law ≠ Standard ≠ Framework ≠ Guidance** — different legal weight, kept in separate sections (10 vs. 09). See [00-navigation-and-methodology/terminology-and-glossary.md](00-navigation-and-methodology/terminology-and-glossary.md).
- **Lifecycle ≠ Governance** — lifecycle is *when*; governance is *who decides*. Kept as separate sections (02 vs. 03).

## How to use this repository

Start with **01-foundations** for shared vocabulary and principles. Building with Gen AI or Agentic AI? Read the relevant technology section (06 or 07) alongside **02-ai-lifecycle** for checkpoints and **13-implementation-playbooks** as your working checklist. Reviewing or approving a use case? Go to **03-ai-governance** for process and **04-ai-assurance** for what evidence to demand. In legal/compliance? **10-regulations-and-standards** is binding law; **09-tools-and-frameworks** is voluntary — don't conflate them.

This is a living document — see [CONTRIBUTING.md](CONTRIBUTING.md) for how to propose updates as regulations, tools, and practices evolve, and [00-navigation-and-methodology/source-and-evidence-policy.md](00-navigation-and-methodology/source-and-evidence-policy.md) for how claims should be sourced.

## Disclaimer

This repository provides general guidance and educational content. It is not legal advice. Regulatory sections (10) summarize publicly available law as of their last review date and are in an area that changes quickly — always confirm current requirements with legal/compliance counsel before relying on them for a specific decision.
