# Source and Evidence Policy

*[Home](../INDEX.md) › [00 · Navigation & Methodology](../00-navigation-and-methodology/framework-map.md)*

## Why this matters

A Responsible AI knowledge base that can't distinguish "this is a legal requirement," "this is a widely-adopted standard," "this is our internal policy choice," and "this is a good practice recommendation" will eventually mislead someone into treating guidance as law or vice versa. This policy sets the bar for how claims in this repository should be sourced.

## Sourcing tiers

| Tier | Description | Example |
|---|---|---|
| **Tier 1 — Primary legal/regulatory text** | The actual law, regulation, or official regulator guidance | EU AI Act text, DPDP Act text, official regulator FAQ |
| **Tier 2 — Formal standard** | Published standard from a recognized standards body | ISO/IEC 42001, NIST AI RMF |
| **Tier 3 — Established industry guidance** | Widely adopted, community/industry-vetted guidance | OWASP LLM Top 10, MITRE ATLAS |
| **Tier 4 — Documented case/incident** | A reported, verifiable real-world event | Regulatory enforcement action, published post-mortem |
| **Tier 5 — Internal policy/judgment call** | This organization's own decision, not externally mandated | "We require human approval above $10k transactions" |

## Rules for content in this repository

1. Every claim about a legal obligation (section 10) should be traceable to Tier 1 source text or official guidance, not a secondary summary alone. Note the source and, where feasible, a retrieval/review date.
2. Every claim about a named framework/standard (section 09) should cite the specific document/version.
3. Case studies (section 12) should distinguish confirmed facts (Tier 4, with a citation) from inference or interpretation — keep them separate in the write-up.
4. Internal policy recommendations (playbooks, governance templates) should be clearly labeled as organizational choices, not external requirements, unless directly citing one.
5. Content should carry a `_Last reviewed: YYYY-MM-DD_` marker where currency matters (regulations, tool capabilities, vendor terms), see [CONTRIBUTING.md](../CONTRIBUTING.md).

## What this repository is not

This is a working reference, not a substitute for legal advice or an official compliance audit. High-stakes decisions relying on section 10 content should be verified against current primary sources and reviewed by qualified legal/compliance counsel before being acted on.

## Handling uncertainty or evolving law

Where a legal question is genuinely unsettled (e.g., active litigation, a regulation not yet in force), say so explicitly rather than presenting one interpretation as settled; see [06-generative-ai/copyright-and-ip.md](../06-generative-ai/copyright-and-ip.md) for an example of this treatment.
