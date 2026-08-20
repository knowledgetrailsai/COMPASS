# Knowledge Map

This repository is organized as a **Responsible AI control plane**, not a flat encyclopedia. Content flows through a consistent chain:

```
PRINCIPLES  →  RISKS  →  REQUIREMENTS  →  CONTROLS  →  TEST/EVALUATE  →  EVIDENCE  →  ASSURANCE
(05)           (01)      (Law/Standards/   (08)          (08, 06, 07     (04)          (04)
                          Policy — 10, 03)                 evaluation
                                                            files)
```

Applied across two cross-cutting dimensions:
- **AI Lifecycle** (02) — where in the build/run process a control applies
- **AI Type** (06 Generative AI, 07 Agentic AI) — technology-specific risk extensions of the core model

And grounded in:
- **Who/Where** — stakeholders (01), jurisdictions and sectors (10, 11)

## The four questions this repository answers

| Question | Sections |
|---|---|
| **What** — principles, risks, technology, regulation | 01, 05, 06, 07, 09, 10 |
| **When** — AI lifecycle / SDLC | 02 |
| **How** — controls, techniques, assessments, playbooks | 03, 04, 08, 13 |
| **Who / Where** — stakeholders, jurisdictions, industries | 01 (roles), 10 (jurisdictions), 11 (sectors) |

## Section map

| # | Section | Answers |
|---|---|---|
| 00 | Navigation and methodology | How to use this repo |
| 01 | Foundations | What is RAI, ethics vs. RAI vs. governance vs. assurance, principles, risk taxonomy, roles |
| 02 | AI lifecycle | When RAI checkpoints apply, from use-case scoping to retirement |
| 03 | AI governance | How practices are institutionalized organizationally |
| 04 | AI assurance | How you prove a system is actually responsible — evidence, audit, red-teaming |
| 05 | Responsible AI principles | Deep dives on fairness, transparency, privacy, safety, accountability, robustness, sustainability |
| 06 | Generative AI | Technology-specific risks/controls for LLMs, RAG, content generation |
| 07 | Agentic AI | Technology-specific risks/controls for autonomous, tool-using agents |
| 08 | Controls and techniques | Concrete methods that implement principles/requirements as working controls |
| 09 | Tools and frameworks | Open-source tools, platforms, and named standards/frameworks (NIST, ISO, OWASP, etc.) |
| 10 | Regulations and standards | Law and regulation by jurisdiction |
| 11 | Sector-specific AI | How everything above combines in a given industry |
| 12 | Case studies | Real-world evidence, structured for reuse |
| 13 | Implementation playbooks | Step-by-step checklists that tie the whole chain together for a real project |

## Example: tracing one risk through the full chain

**Risk: Prompt injection (Generative/Agentic AI)**

1. Principle at stake: Safety and security ([05-responsible-ai-principles/safety-and-security.md](../05-responsible-ai-principles/safety-and-security.md))
2. Risk detail: [06-generative-ai/prompt-injection.md](../06-generative-ai/prompt-injection.md), [07-agentic-ai/tool-use-and-permissions.md](../07-agentic-ai/tool-use-and-permissions.md)
3. Requirement: OWASP LLM Top 10 (LLM01), internal security policy ([09-tools-and-frameworks](../09-tools-and-frameworks/))
4. Controls: input isolation, trusted/untrusted content separation, least-privilege tool access ([08-controls-and-techniques/guardrails-and-controls.md](../08-controls-and-techniques/guardrails-and-controls.md))
5. Test: adversarial red-team scenarios ([04-ai-assurance/red-teaming.md](../04-ai-assurance/red-teaming.md))
6. Evidence: red-team report, action logs ([04-ai-assurance/evidence-and-traceability.md](../04-ai-assurance/evidence-and-traceability.md))
7. Assurance: signed off by governance board as part of deployment approval ([03-ai-governance/ai-governance-board.md](../03-ai-governance/ai-governance-board.md))

This is the pattern to apply when researching any risk in this repository.
