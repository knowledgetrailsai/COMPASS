# Sector-Specific AI

*[Home](../INDEX.md) › [11 · Sector-Specific AI](../11-sector-specific-ai/)*

## Why this section exists

Responsible AI requirements aren't uniform — they change significantly depending on where AI is deployed. This section shows how the rest of the repository's chain (regulation → risk → lifecycle → controls → testing → evidence) combines for a specific industry, so a team in that industry can go straight to what matters most for them rather than re-deriving it from first principles.

## Worked pattern (applies to every file in this section)

```
Sector-specific AI use case
        ↓
Sector-specific risks (fairness, privacy, safety, explainability — weighted differently per sector)
        ↓
Applicable regulation (horizontal + sector-specific)
        ↓
Required controls
        ↓
Testing/evaluation emphasis
        ↓
Evidence and assurance expectations
```

## Sectors covered

| Sector | File |
|---|---|
| Financial services | [financial-services.md](financial-services.md) |
| Healthcare | [healthcare.md](healthcare.md) |
| Insurance | [insurance.md](insurance.md) |
| Human resources | [human-resources.md](human-resources.md) |
| Education | [education.md](education.md) |
| Manufacturing | [manufacturing.md](manufacturing.md) |
| Retail | [retail.md](retail.md) |
| Public sector | [public-sector.md](public-sector.md) |
| Critical infrastructure | [critical-infrastructure.md](critical-infrastructure.md) |

Each file references the relevant horizontal principles (05), lifecycle (02), controls (08), and regulation (10) sections rather than duplicating that content — use this section to find the sector-specific *emphasis and additions*, not a standalone treatment.
