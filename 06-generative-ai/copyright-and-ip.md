# Copyright and IP Considerations

*[Home](../INDEX.md) › [06 · Generative AI](../06-generative-ai/)*

## Areas of legal uncertainty (evolving — verify current status with legal counsel)

### Training data
Whether training on copyrighted material without a license constitutes infringement or falls under fair use/text-and-data-mining exceptions is actively being litigated and legislated differently across jurisdictions (US fair use doctrine, EU TDM exceptions with opt-out mechanisms, evolving case law elsewhere). Organizations fine-tuning models on their own or licensed data face lower risk than those relying on unclear-provenance base model training data.

### Output similarity / infringement
Generated content that substantially reproduces or closely mimics copyrighted works (text, code, images, music, likeness/style) can create infringement exposure for the deploying organization, independent of how the underlying model was trained.

### Ownership of AI-generated output
Many jurisdictions (including the US Copyright Office's current position) hold that purely AI-generated content without sufficient human creative input is not copyrightable. Practical implication: content your organization wants to protect as IP may need meaningful human authorship/editing to qualify.

### Style/likeness mimicry
Generating content "in the style of" a named living artist, or voice/likeness cloning, raises right-of-publicity and, in some jurisdictions, emerging AI-specific likeness protection issues even where copyright doesn't directly apply.

## Practical risk-reduction steps

- Prefer models/vendors with clearly licensed or owned training data, and check vendor indemnification terms for IP claims arising from model output
- Implement output similarity screening for high-value or externally published generated content (code, marketing copy, media)
- Require meaningful human review/editing before publishing AI-generated content that needs IP protection
- Avoid prompts that explicitly request mimicry of a named living artist's style or a real person's voice/likeness without consent/license
- Maintain records of prompts and generation process for content your organization publishes, to support any future ownership or provenance questions
- Track vendor terms of service changes — whether your inputs/outputs can be used for the vendor's own model training is a frequently changing and commercially material term

## Vendor contract checklist

- IP indemnification scope and caps for output infringement claims
- Confirmation that your data isn't used for the vendor's general model training without explicit opt-in
- Data residency and deletion terms
- Audit rights for high-risk use cases

## Related

- [06-generative-ai/content-provenance.md](content-provenance.md)
- [13-implementation-playbooks/vendor-third-party-ai-assessment.md](../13-implementation-playbooks/vendor-third-party-ai-assessment.md)
