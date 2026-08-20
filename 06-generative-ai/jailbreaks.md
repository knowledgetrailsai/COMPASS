# Jailbreaking

## Definition

Adversarial prompting techniques specifically designed to bypass a model's safety training and elicit outputs the model was trained/instructed to refuse — hate speech, dangerous instructions, disallowed content categories, or leaking system prompts/confidential configuration.

## Common technique families (illustrative, not exhaustive — techniques evolve continuously)

- **Role-play/persona framing**: instructing the model to act as a fictional character or entity "without restrictions"
- **Hypothetical/academic framing**: requesting disallowed content framed as fiction, research, or a thought experiment
- **Instruction override attempts**: directly instructing the model to ignore prior instructions or safety training
- **Encoding/obfuscation**: encoding disallowed requests (alternate languages, ciphers, unusual formatting) to evade pattern-matching filters
- **Multi-turn erosion**: gradually shifting a conversation toward disallowed territory across many turns, exploiting looser scrutiny of later-turn context
- **Many-shot / context stuffing**: providing many examples of the desired (disallowed) behavior pattern to shift the model's in-context behavior

## Why this differs from prompt injection

Jailbreaking is generally direct (the user themselves is the adversary, trying to make the model itself misbehave), while prompt injection ([prompt-injection.md](prompt-injection.md)) often targets a system on behalf of an unaware end user via third-party content. The mitigations overlap significantly but the threat model — and who's doing the attacking — differs.

## Mitigations

- Safety-tuned base models appropriate to the deployment context, refreshed as providers release improved safety training
- Independent guardrail/classifier layer that screens for jailbreak patterns, separate from the primary generation model — a second opinion that doesn't share the same blind spots
- Continuous red-teaming specifically targeting known and novel jailbreak techniques, not a one-time pre-launch check — see [04-ai-assurance/red-teaming.md](../04-ai-assurance/red-teaming.md)
- Rate limiting and behavioral anomaly detection to catch systematic jailbreak-probing patterns
- Monitoring and rapid patching cadence, since jailbreak techniques evolve quickly and a defense effective today may not be tomorrow

## Realistic expectation-setting

No current mitigation makes a model fully jailbreak-proof. Design the surrounding system (permissions, output validation, human review for consequential actions) so a successful jailbreak has bounded impact, consistent with the defense-in-depth approach in [prompt-and-output-safety.md](prompt-and-output-safety.md).
