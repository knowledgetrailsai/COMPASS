# Synthetic Content

*[Home](../INDEX.md) › [06 · Generative AI](../06-generative-ai/content-provenance.md)*

## Scope

AI-generated text, image, audio, and video content. Covers both legitimate use (marketing content, synthetic training data, accessibility applications like text-to-speech) and the misuse risks that come with the same capability (deepfakes, disinformation, fraud).

## Legitimate use considerations

- **Synthetic training/test data**: generating artificial data to augment scarce or sensitive datasets (e.g., for privacy-preserving model development) — validate that synthetic data doesn't silently encode or amplify the same biases as its source, and doesn't inadvertently leak identifiable patterns from real data it was derived from
- **Content generation at scale**: marketing copy, product descriptions, design assets. Apply [copyright-and-ip.md](copyright-and-ip.md) and quality/brand review before publishing
- **Accessibility applications**: synthetic voice/text for accessibility tools: generally lower risk but still warrants disclosure where the output could be mistaken for a real recorded voice

## Misuse risks

- **Deepfakes**: synthetic image/video/audio convincingly depicting real people saying or doing things they didn't — enables fraud (voice cloning for financial scams), non-consensual content, and disinformation
- **Synthetic disinformation at scale**: generating large volumes of fabricated news-like content or fake reviews/testimonials
- **Identity fraud**: synthetic identity documents or biometric spoofing material

## Controls

- **Provenance and watermarking**: apply content credentials (C2PA) and/or watermarking to organizationally-generated synthetic content: see [content-provenance.md](content-provenance.md)
- **Consent capture for likeness/voice**: technical and process controls requiring explicit, verifiable consent before generating content using a real person's likeness or voice
- **Use-case restrictions**: explicit policy prohibiting generation of content depicting real, identifiable people without consent, especially in sensitive contexts (political figures, intimate content)
- **Detection tooling**: deploy AI-content detection as a monitoring signal for platforms accepting user-generated content, while recognizing current detection accuracy limitations
- **Rate limiting and abuse monitoring**: for any public-facing generation tool, monitor for patterns consistent with abuse (mass generation of a specific real person's likeness, disinformation-pattern content)

## Regulatory context

Increasingly regulated explicitly, deepfake-specific laws in various jurisdictions, EU AI Act transparency obligations for synthetic content, and platform-level policies. See [10-regulations-and-standards](../10-regulations-and-standards/global-overview.md).

## Related

- [content-provenance.md](content-provenance.md)
- [12-case-studies](../12-case-studies/case-study-template.md) for documented synthetic-content misuse incidents
