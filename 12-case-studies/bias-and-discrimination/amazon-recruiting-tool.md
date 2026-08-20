# Amazon's Experimental AI Recruiting Tool

**Context**: Amazon, internal recruiting, developed ~2014, scrapped ~2017 after internal discovery of the bias described below (widely reported in 2018).

**AI system**: Traditional ML — a resume-screening/candidate-scoring model trained to rate applicants.

**What happened**: The model was trained on 10 years of resumes submitted to Amazon, most from men, reflecting male dominance in the tech industry at the time. The model learned to penalize resumes containing the word "women's" (e.g., "women's chess club captain") and downgraded graduates of two all-women's colleges. Amazon engineers attempted to fix the specific identified issues, but reportedly could not be confident the model wasn't finding other, less obvious ways to produce gender-biased outcomes, and the project was scrapped before wide deployment.

**Root cause**: Historical bias in training data (a male-dominated resume history) learned and amplified by the model — a textbook historical-bias failure mode (see [05-responsible-ai-principles/fairness-and-bias.md](../../05-responsible-ai-principles/fairness-and-bias.md)).

**Risk category**: Bias and fairness risk.

**Lifecycle stage where it could have been caught**: [02-ai-lifecycle/data-and-data-governance.md](../../02-ai-lifecycle/data-and-data-governance.md) (representativeness assessment) and [02-ai-lifecycle/evaluation-and-validation.md](../../02-ai-lifecycle/evaluation-and-validation.md) (subgroup fairness testing) before any production use.

**Control failure**: No apparent subgroup fairness testing against gender before the model was trusted for candidate scoring; training data representativeness wasn't assessed against fairness requirements before development.

**Impact**: Contained — Amazon reportedly did not rely on the tool as the sole basis for hiring decisions and discontinued the project before wide production use. Reputational impact from public reporting was still significant.

**Regulatory implications**: No confirmed enforcement action reported; the case became a widely cited reference point in subsequent AI hiring regulation discussions (see [11-sector-specific-ai/human-resources.md](../../11-sector-specific-ai/human-resources.md)).

**Lessons learned**: Historical hiring data reflects historical hiring bias by default — treating past decisions as ground truth for training a scoring model reproduces past discrimination unless deliberately corrected for. Internal discovery (rather than external exposure) is the better outcome, but only if it happens before deployment, not after.

**Preventive controls**: Mandatory subgroup fairness testing before deployment ([08-controls-and-techniques/fairness-testing](../../08-controls-and-techniques/fairness-testing/)); explicit review of whether historical decision data is an appropriate training target for a "fair going forward" model.

**Sources**: Widely reported contemporaneously by Reuters ("Amazon scraps secret AI recruiting tool that showed bias against women," 2018) and extensively cited in subsequent AI fairness literature and regulatory discussion.
