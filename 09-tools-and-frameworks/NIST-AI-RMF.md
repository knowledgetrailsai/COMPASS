# NIST AI Risk Management Framework (AI RMF)

*[Home](../INDEX.md) › [09 · Tools & Frameworks](../09-tools-and-frameworks/commercial-platforms.md)*

_Type: Framework (voluntary). Issuer: U.S. National Institute of Standards and Technology. Last reviewed: 2026-08-19 — verify current version and any Generative AI Profile updates directly with NIST._

## What it is

A voluntary framework helping organizations manage AI risk across the system lifecycle, structured around four core functions. Widely referenced internationally even outside the US as a structured, credible risk-management vocabulary.

## Core functions

| Function | Purpose |
|---|---|
| **Govern** | Cultivate a risk-management culture; establish policies, roles, and accountability | 
| **Map** | Identify context, categorize the AI system, and identify risks specific to it |
| **Measure** | Assess, analyze, and track identified risks using appropriate metrics |
| **Manage** | Prioritize and act on risks; allocate resources to risk response |

## How it maps to this repository

| NIST function | This repository |
|---|---|
| Govern | [03-ai-governance](../03-ai-governance/AI-assurance.md) |
| Map | [01-foundations/risk-taxonomy.md](../01-foundations/risk-taxonomy.md), [04-ai-assurance/AI-risk-assessment.md](../04-ai-assurance/AI-risk-assessment.md) |
| Measure | [08-controls-and-techniques/evaluation-and-benchmarking](../08-controls-and-techniques/evaluation-and-benchmarking/README.md), [04-ai-assurance](../04-ai-assurance/assurance-overview.md) |
| Manage | [08-controls-and-techniques](../08-controls-and-techniques/README.md), [02-ai-lifecycle/incident-and-remediation.md](../02-ai-lifecycle/incident-and-remediation.md) |

## Generative AI Profile

NIST has published a Generative AI-specific profile supplementing the core RMF with risks particular to generative systems (content provenance, confabulation/hallucination, and others); cross-reference against [06-generative-ai](../06-generative-ai/content-provenance.md) when applying it.

## When to use this framework

Good fit for organizations wanting a structured internal risk process without pursuing formal certification (contrast with [ISO-42001.md](ISO-42001.md), which is certifiable). Frequently used as the underlying risk vocabulary even when the ultimate goal is a different jurisdiction's regulatory compliance, since its structure maps cleanly onto most regulatory risk-based approaches (including the EU AI Act's).

## Not binding law

The AI RMF is voluntary guidance, not a legal requirement. See [00-navigation-and-methodology/terminology-and-glossary.md](../00-navigation-and-methodology/terminology-and-glossary.md) for why this distinction matters. Some US federal agency contexts do reference or require RMF alignment; check current applicable requirements for your specific context.
