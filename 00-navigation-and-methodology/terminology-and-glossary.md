# Terminology — Key Distinctions

A short guide to terms this repository uses precisely and consistently. For the full alphabetical glossary, see [glossary/ai-glossary.md](../glossary/ai-glossary.md).

## Ethics, Responsible AI, Governance, Assurance — the four layers

| Term | Answers | Example |
|---|---|---|
| **AI Ethics** | What *ought* to be done — the normative/moral questions | Should this system be built at all? Whose values does it encode? |
| **Responsible AI** | How those expectations become organizational and technical practice | Bias testing, guardrails, documentation |
| **AI Governance** | How those practices are institutionalized organizationally | Governance boards, policy, risk tiering, RACI |
| **AI Assurance** | How you demonstrate the practices actually work | Audits, red-teaming, conformity assessment, evidence |

See [01-foundations/responsible-ai-vs-ai-ethics.md](../01-foundations/responsible-ai-vs-ai-ethics.md) for the full discussion.

## Law, Standard, Framework, Guidance — don't conflate these

| Term | Nature | Example |
|---|---|---|
| **Law / Regulation** | Legally binding, enforceable by a government body | EU AI Act, India's DPDP Act |
| **Standard** | Formal, often certifiable specification from a standards body | ISO/IEC 42001, ISO/IEC 23894 |
| **Framework** | Structured but voluntary guidance for organizing practice | NIST AI RMF |
| **Guidance / Industry practice** | Non-binding recommendations, often from a community or vendor | OWASP LLM Top 10, MITRE ATLAS |

Treating a voluntary framework as a legal requirement (or vice versa) is a common and costly mistake — [10-regulations-and-standards](../10-regulations-and-standards/) is reserved for binding law; frameworks/standards live in [09-tools-and-frameworks](../09-tools-and-frameworks/).

## Risk, Control, Technique, Test — the implementation chain

| Term | Definition |
|---|---|
| **Risk** | A specific way the system could cause harm (e.g., prompt injection) |
| **Control** | A policy or architectural measure that reduces the risk (e.g., input isolation, human approval) |
| **Technique** | A concrete method implementing a control (e.g., prompt sanitization, sandboxing) |
| **Test** | How you verify the control/technique actually works (e.g., adversarial red-team scenario) |

## Tool vs. Framework vs. Standard (commonly conflated)

Fairlearn is a **tool**. NIST AI RMF is a **framework**. ISO/IEC 42001 is a **management-system standard**. OWASP LLM Top 10 is **security guidance**. They don't sit at the same level, and this repository keeps them in [09-tools-and-frameworks](../09-tools-and-frameworks/) with that distinction explicit.

## Traditional ML vs. Generative AI vs. Agentic AI

See [01-foundations/what-is-responsible-ai.md](../01-foundations/what-is-responsible-ai.md#scope-of-this-guide) for the scope table.
