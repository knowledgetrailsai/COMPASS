# Privacy Techniques

Implements [05-responsible-ai-principles/privacy-and-data-protection.md](../../05-responsible-ai-principles/privacy-and-data-protection.md) as concrete methods.

## Data minimization and de-identification

- **Anonymization**: irreversibly removing identifying information — the gold standard where feasible, since properly anonymized data generally falls outside data protection regulation scope, though true anonymization (resistant to re-identification) is harder to achieve than it sounds
- **Pseudonymization**: replacing identifiers with reversible tokens — reduces risk but remains regulated personal data since re-identification is possible with the key
- **Data masking/redaction**: removing or obscuring specific sensitive fields (PII detection and redaction) before data is used for training, logging, or display

## Privacy-preserving computation

- **Differential privacy**: adding calibrated statistical noise to data or model outputs so individual records can't be reliably distinguished, with a formal, quantifiable privacy guarantee (epsilon parameter) — used in both training (DP-SGD) and query/aggregate release contexts
- **Federated learning**: training a model across decentralized data sources without centralizing the raw data — reduces data concentration risk, though the transmitted model updates can still leak information without additional protection
- **Synthetic data generation**: generating artificial data that preserves statistical properties without containing real individual records — useful for testing/development, requires validation that it doesn't leak identifiable patterns from source data

## PII detection and handling

- Automated PII detection (named entity recognition tuned for identifiers, regex/pattern matching for structured IDs) applied at ingestion, logging, and output stages
- Consistent redaction/tokenization policy applied uniformly, not ad hoc per pipeline

## Access-aware retrieval (Gen AI/RAG)

Enforcing document/row-level permissions as a retrieval-time filter — see [06-generative-ai/RAG-governance.md](../../06-generative-ai/RAG-governance.md) — is a privacy technique specific to enterprise Gen AI, distinct from classic anonymization.

## Choosing techniques

Match technique to risk: differential privacy for aggregate statistical release with formal guarantees, federated learning when data can't be centralized at all, straightforward redaction/masking for most enterprise logging and RAG use cases. Avoid over-engineering (e.g., full differential privacy) where simpler data minimization and access control suffice.

## Tooling

See [09-tools-and-frameworks/open-source-tools.md](../../09-tools-and-frameworks/open-source-tools.md) (Presidio for PII detection, various DP libraries).
