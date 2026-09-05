# AI Ethics

*[Home](../INDEX.md) › [01 · Foundations](../01-foundations/ai-ethics.md)*

## Scope

AI Ethics addresses the normative question underlying every other section of this repository: what *ought* an AI system do, whose values should it encode, and where should lines be drawn regardless of what's technically possible or even legally permitted.

## Major ethical frameworks applied to AI

- **Consequentialist framing**: judge AI systems by outcomes — net benefit vs. harm across all affected parties, including those not using the system directly
- **Deontological/rights-based framing**: certain actions or uses are impermissible regardless of net benefit (e.g., using AI to violate fundamental rights, even if "efficient")
- **Virtue/care ethics framing**: what does building and deploying this system say about the values and character of the organization doing so, and does it embody care for those affected
- **Justice and fairness framing**: how are benefits and burdens of AI distributed; does it concentrate power/benefit while distributing risk/harm unevenly

Most organizational AI ethics statements implicitly blend these rather than committing to one. Worth making explicit when a genuine dilemma arises rather than defaulting to whichever framing is convenient.

## Recurring ethical questions in AI

- **Should this be built at all?** Some capabilities (mass surveillance, manipulation, autonomous weapons) raise the question independent of how well they're built.
- **Whose values?** Whose definition of "fair," "harmful," or "appropriate" is encoded — and was that decision made with input from those affected, or unilaterally by the builder?
- **Consent and autonomy**: are people meaningfully informed and able to opt out of AI-mediated decisions affecting them?
- **Power and accountability**: does the system shift power/information asymmetrically toward its operator and away from the people it affects?
- **Dual use**: can a beneficial capability be repurposed for harm, and what responsibility does the builder bear for foreseeable misuse?

## Ethics review in practice

Ethics questions are often the hardest to operationalize into a checklist, they benefit from structured deliberation (an ethics review as part of the governance board, diverse stakeholder input, "red team the ethics" exercises) rather than a single reviewer's judgment. See [03-ai-governance/ai-governance-board.md](../03-ai-governance/ai-governance-board.md).

## Ethics is necessary but not sufficient

An ethically sound intention doesn't guarantee a responsibly built system; see [responsible-ai-vs-ai-ethics.md](responsible-ai-vs-ai-ethics.md) for why this repository treats ethics as the starting layer, translated into practice, governance, and assurance in the sections that follow.

## Related

- [human-rights-and-ai.md](human-rights-and-ai.md)
- [principles.md](principles.md)
