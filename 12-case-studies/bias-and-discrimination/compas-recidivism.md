# COMPAS Recidivism Risk Scoring

*[Home](../../INDEX.md) › [12 · Case Studies](../../12-case-studies/) › [bias-and-discrimination](../../12-case-studies/bias-and-discrimination/)*

**Context**: US criminal justice system, COMPAS risk-assessment tool (developed by Northpointe/Equivant) used by courts in several US states to inform bail, sentencing, and parole decisions. Most prominently analyzed by ProPublica in 2016.

**AI system**: Traditional ML — a proprietary risk-scoring model predicting likelihood of recidivism.

**What happened**: ProPublica's 2016 analysis found that COMPAS was substantially more likely to falsely flag Black defendants as high risk for future crime (higher false positive rate) and substantially more likely to falsely flag white defendants as low risk (higher false negative rate) than the reverse, even though the tool's overall accuracy was similar across groups and the tool did not use race as an explicit input. Northpointe disputed the analysis, noting the tool was well-calibrated (predicted risk levels corresponded to similar actual recidivism rates across groups) — a foundational, widely cited illustration of the fairness-definition tension described in [05-responsible-ai-principles/fairness-and-bias.md](../../05-responsible-ai-principles/fairness-and-bias.md#fairness-definitions-there-is-no-single-fair).

**Root cause**: A structural, definitional issue rather than a single coding bug — the tool satisfied one legitimate fairness definition (calibration) while failing another (equalized error rates) — demonstrating that different fairness metrics can be mathematically incompatible with each other given underlying base-rate differences across groups.

**Risk category**: Bias and fairness risk; also a due-process/human-rights consideration given the tool's use in decisions affecting liberty.

**Lifecycle stage where it could have been caught**: [02-ai-lifecycle/requirements-and-design.md](../../02-ai-lifecycle/requirements-and-design.md) — the specific fairness definition and acceptable trade-off should have been an explicit, deliberated, and disclosed design decision rather than left implicit.

**Control failure**: No public, deliberate choice-and-disclosure of which fairness definition the tool was optimized for, and no independent, public evaluation before wide judicial adoption — a transparency and independent-assessment gap ([04-ai-assurance/independent-assessment.md](../../04-ai-assurance/independent-assessment.md)).

**Impact**: Affected liberty-related decisions (bail, sentencing) for large numbers of defendants across adopting jurisdictions over years of use.

**Regulatory implications**: The case fueled a wave of academic, legal, and policy scrutiny of algorithmic risk assessment in criminal justice, and is frequently cited in subsequent regulatory frameworks' treatment of high-risk/rights-affecting AI (including the reasoning behind risk-tiering approaches like the EU AI Act's).

**Lessons learned**: "Fair" is not a single measurable property — the specific fairness definition matters, should be a deliberate and disclosed choice appropriate to the decision's stakes (see [05-responsible-ai-principles/fairness-and-bias.md](../../05-responsible-ai-principles/fairness-and-bias.md)), and proprietary/opaque tools used in high-stakes public decisions warrant independent, public scrutiny.

**Preventive controls**: Explicit fairness-definition selection with documented rationale during [02-ai-lifecycle/requirements-and-design.md](../../02-ai-lifecycle/requirements-and-design.md); independent, published evaluation before adoption in rights-affecting public-sector use ([11-sector-specific-ai/public-sector.md](../../11-sector-specific-ai/public-sector.md)); transparency sufficient for external audit despite proprietary model status.

**Sources**: ProPublica, "Machine Bias" (2016); Northpointe/Equivant's public response; extensive subsequent academic literature on the mathematical incompatibility of fairness definitions (e.g., Kleinberg et al., Chouldechova, 2016-2017).
