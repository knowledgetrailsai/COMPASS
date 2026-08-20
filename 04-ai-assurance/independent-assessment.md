# Independent Assessment

*[Home](../INDEX.md) › [04 · AI Assurance](../04-ai-assurance/)*

## Why independence matters

Teams that build a system are prone to confirmation bias when evaluating it — they know what it's supposed to do, and unconsciously test in ways that confirm success rather than actively hunting for failure. Independent assessment counteracts this by involving reviewers without a stake in the system passing.

## Levels of independence

| Level | Description | Appropriate for |
|---|---|---|
| Self-assessment | Build team evaluates its own system | Tier 3 |
| Internal independent | A separate internal team (central RAI function, QA, security) evaluates | Tier 2, baseline for Tier 1 |
| External independent | A third-party firm or expert with no organizational stake assesses | Tier 1, high public-trust systems, regulatory-mandated conformity assessment |
| Regulatory/notified body | An accredited body performs assessment as a legal requirement | Where mandated (e.g., specific EU AI Act high-risk categories) |

## What makes an assessment genuinely independent

- The assessor's incentives aren't tied to the system launching on schedule or the build team's performance review
- The assessor has genuine access — to the system, its documentation, and relevant staff — not a curated subset designed to pass review
- Findings go to the governance board directly, not filtered/summarized solely by the build team first
- The assessor has explicit authority to block or condition a launch, not just advise

## Building internal independence at scale

Not every organization can afford external assessment for every Tier 1 system. A dedicated internal RAI/red-team function, organizationally separate from product engineering (different reporting line, different incentives), can provide meaningful independence at lower cost — the key structural requirement is that the assessor isn't evaluated on the same success metrics as the build team.

## Relationship to other assurance activities

Independent assessors typically execute or verify [model-validation.md](model-validation.md) and [red-teaming.md](red-teaming.md), and their findings become part of [evidence-and-traceability.md](evidence-and-traceability.md) for governance board review.

## Practical guidance

Reserve external independent assessment for the highest-stakes systems (Tier 1 with significant rights/safety impact, or where regulation mandates it) given cost and lead time — use strong internal independence as the default for the rest of Tier 1 and Tier 2.
