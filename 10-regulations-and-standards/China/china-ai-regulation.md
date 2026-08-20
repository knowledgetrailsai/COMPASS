# China — AI Regulation

*[Home](../../INDEX.md) › [10 · Regulations & Standards](../../10-regulations-and-standards/) › [China](../../10-regulations-and-standards/China/)*

_Last reviewed: 2026-08-19. China's AI regulatory regime is binding and among the most developed globally in specific areas (algorithms, generative AI, deep synthesis) — confirm current specific requirements directly given the pace of new implementing rules._

## Approach: binding, technology-specific rules issued progressively

Rather than one comprehensive AI statute, China has issued a series of binding, technology/use-case-specific regulations, generally administered by the Cyberspace Administration of China (CAC) alongside other ministries — covering recommendation algorithms, deep synthesis (deepfakes), and generative AI services specifically.

## Key regulatory instruments (by category)

- **Algorithmic recommendation regulation**: governs recommendation-system transparency, user control (ability to turn off personalized recommendation), and prohibits certain manipulative uses
- **Deep synthesis regulation**: governs AI-generated/manipulated content (deepfakes), requiring labeling/disclosure and restricting non-consensual or deceptive use
- **Generative AI service measures**: requirements for generative AI service providers, including content moderation obligations (alignment with core socialist values and content restrictions), security assessment before public release for services with public-opinion or social-mobilization properties, and algorithm registration with the CAC
- **Algorithm registration system**: providers of certain algorithmic services must register with regulators, providing algorithm details for the government's algorithm filing system

## Practical implications for AI systems operating in/serving China

- Content moderation and disclosure obligations are generally more prescriptive and binding than in most other jurisdictions covered in this section — build compliance in from the start rather than retrofitting
- Algorithm registration requirements mean transparency to the regulator (not just the public) is often a binding obligation, distinct from the EU/US approach of primarily user-facing transparency
- Security assessment requirements for generative AI services with public-facing/opinion-forming characteristics should be factored into [02-ai-lifecycle/deployment-and-release.md](../../02-ai-lifecycle/deployment-and-release.md) planning timelines for China-facing launches

## Data considerations

China's data protection framework (Personal Information Protection Law, PIPL, and related cybersecurity/data-security laws) imposes strict data localization and cross-border transfer restrictions relevant to any AI system processing Chinese user data — treat as at least as stringent as GDPR/DPDP-style regimes for planning purposes, and verify current cross-border transfer mechanisms directly given this is an actively regulated area.

## Related

- [global-overview.md](../global-overview.md)
- [06-generative-ai/content-provenance.md](../../06-generative-ai/content-provenance.md)
