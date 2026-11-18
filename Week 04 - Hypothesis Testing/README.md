# Is the New AI Model Really Better? Hypothesis Testing of Model Accuracy

AIT 530 assignment — statistical inference for AI model performance: hypothesis tests, p-values, confidence intervals, and Type I/II errors.

Uses the course-provided AIT-530 Topic 4 dataset (15,000 evaluation runs of four AI models) to test whether a candidate model (C) beats the baseline (A) on accuracy. A two-sample Welch t-test gives t = 1.74, p = 0.081, and a 95% CI for the difference of −0.07 to +1.21 percentage points, so H₀ is not rejected. A one-sample test against a 75% target, an ANOVA with Tukey's HSD (only C vs. D differs), and permutation, bootstrap, and Mann–Whitney checks support the result. A simulation shows the false-positive rate rising from 5% for one planned test to about 20% when picking the best of six comparisons. A power analysis gives 42% power for the observed gain and 86.5% for a 1-point gain. A TOST equivalence test finds Models B and D practically equivalent to the baseline and Model C inconclusive.

- [`Hypothesis_Testing_Model_Accuracy.ipynb`](./Hypothesis_Testing_Model_Accuracy.ipynb) — the full notebook, built on the 15-section Jupyter Notebook Template: research question and hypotheses, assumption checks, t-tests, ANOVA and Tukey, robustness checks, Type I/II error analysis, equivalence test, and references.
- `model_data/` — the AIT-530 Topic 4 dataset (`AIT-530-T4-Dataset.csv`, unzipped from the course's `AIT-530-T4-Dataset.zip`). Course material, so it is not tracked in git.
- `Assignment.docx` — original assignment instructions (not tracked in git).
- `script.md` — narration script for the video presentation (not tracked in git).
