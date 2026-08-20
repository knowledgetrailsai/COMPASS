# Responsible AI Guide

A comprehensive Responsible AI knowledge base — covering traditional ML, Generative AI, and Agentic AI — organized as a **control plane**, not an encyclopedia. Content flows through a consistent chain so any risk can be traced from principle to proof:

```
PRINCIPLES → RISKS → REQUIREMENTS → CONTROLS → TEST/EVALUATE → EVIDENCE → ASSURANCE
```

applied across the AI lifecycle, across AI types (Gen AI, Agentic AI), and across stakeholders, jurisdictions, and sectors. See [00-navigation-and-methodology/knowledge-map.md](00-navigation-and-methodology/knowledge-map.md) for the full model, including a worked example tracing one risk end-to-end through every section below.

## Start here

New to this repository? Read [00-navigation-and-methodology/how-to-use-this-repository.md](00-navigation-and-methodology/how-to-use-this-repository.md) — it routes you to the right section based on your role and task.

## Section map

| # | Section | Answers |
|---|---|---|
| 00 | [Navigation and methodology](00-navigation-and-methodology/) | How to use this repo; terminology; source policy |
| 01 | [Foundations](01-foundations/) | What is RAI; ethics vs. RAI vs. governance vs. assurance; principles; risk taxonomy; roles |
| 02 | [AI lifecycle](02-ai-lifecycle/) | When RAI checkpoints apply, use-case scoping through retirement |
| 03 | [AI governance](03-ai-governance/) | How practices are institutionalized organizationally |
| 04 | [AI assurance](04-ai-assurance/) | How you prove a system is actually responsible |
| 05 | [Responsible AI principles](05-responsible-ai-principles/) | Deep dives: fairness, transparency, privacy, safety, accountability, robustness, sustainability |
| 06 | [Generative AI](06-generative-ai/) | Hallucination, prompt injection, jailbreaks, IP, RAG, fine-tuning, evaluation |
| 07 | [Agentic AI](07-agentic-ai/) | Autonomy, tool use, identity, multi-agent, memory, observability, incident response |
| 08 | [Controls and techniques](08-controls-and-techniques/) | Risk → control → technique → test, implemented concretely |
| 09 | [Tools and frameworks](09-tools-and-frameworks/) | Open-source tools, platforms, and named standards (NIST, ISO, OWASP, MITRE) |
| 10 | [Regulations and standards](10-regulations-and-standards/) | Binding law by jurisdiction: EU, US, India, UK, China, Singapore, Canada |
| 11 | [Sector-specific AI](11-sector-specific-ai/) | How everything combines per industry |
| 12 | [Case studies](12-case-studies/) | Real, sourced incidents and good practices, structured for reuse |
| 13 | [Implementation playbooks](13-implementation-playbooks/) | Step-by-step checklists tying the whole chain together |
| [glossary](glossary/) | Alphabetical term reference | |
| [templates](templates/) | Index of reusable templates | |
| [assets](assets/) | Diagrams and images | |

## Key distinctions this repository maintains

- **Ethics ≠ Responsible AI ≠ Governance ≠ Assurance** — four different layers, not synonyms. See [01-foundations/responsible-ai-vs-ai-ethics.md](01-foundations/responsible-ai-vs-ai-ethics.md).
- **Law ≠ Standard ≠ Framework ≠ Guidance** — different legal weight, kept in separate sections (10 vs. 09). See [00-navigation-and-methodology/terminology-and-glossary.md](00-navigation-and-methodology/terminology-and-glossary.md).
- **Lifecycle ≠ Governance** — lifecycle is *when*; governance is *who decides*. Kept as separate sections (02 vs. 03).

## How to use this repository

Start with **01-foundations** for shared vocabulary and principles. Building with Gen AI or Agentic AI? Read the relevant technology section (06 or 07) alongside **02-ai-lifecycle** for checkpoints and **13-implementation-playbooks** as your working checklist. Reviewing or approving a use case? Go to **03-ai-governance** for process and **04-ai-assurance** for what evidence to demand. In legal/compliance? **10-regulations-and-standards** is binding law; **09-tools-and-frameworks** is voluntary — don't conflate them.

This is a living document — see [CONTRIBUTING.md](CONTRIBUTING.md) for how to propose updates as regulations, tools, and practices evolve, and [00-navigation-and-methodology/source-and-evidence-policy.md](00-navigation-and-methodology/source-and-evidence-policy.md) for how claims should be sourced.

## Disclaimer

This repository provides general guidance and educational content. It is not legal advice. Regulatory sections (10) summarize publicly available law as of their last review date and are in an area that changes quickly — always confirm current requirements with legal/compliance counsel before relying on them for a specific decision.
