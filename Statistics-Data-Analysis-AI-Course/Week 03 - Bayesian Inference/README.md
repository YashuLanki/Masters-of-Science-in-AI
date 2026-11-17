# Bayesian Inference for Online Shopper Conversion: Updating Beliefs as New Data Arrives

AIT 530 assignment — Bayesian statistics: prior, likelihood, and posterior for an online store's purchase conversion rate, updated as new data arrives and compared with frequentist maximum likelihood.

Uses the [UCI Online Shoppers Purchasing Intention dataset](https://doi.org/10.24432/C5F88Q) (12,330 sessions) to estimate the conversion rate θ with a Beta(2, 18) prior and a Bernoulli likelihood. The exact conjugate posterior (mean 15.47%, 95% credible interval 14.83–16.11%) is confirmed by a PyMC MCMC model (r-hat = 1.001). The posterior is updated month by month and in a simulated stream from three priors, showing the interval narrowing and the priors converging. A chi-square test and one-month-ahead predictions show the rate changes by season (only 1 of 9 months inside the 90% predictive range), and a forgetting factor cuts the prediction error from 6.2 to 4.4 points. Compared with MLE, the Bayesian estimate has half the error at n = 10 and never reports a 0% rate, while the two agree with large samples, including for a logistic regression on PageValues. The report also estimates P(new visitors convert better than returning) ≈ 100% and discusses Bayesian methods in adaptive learning.

- [`Bayesian_Shopper_Conversion.ipynb`](./Bayesian_Shopper_Conversion.ipynb) — the full notebook, built on the 15-section Jupyter Notebook Template: Kaggle review, data preprocessing, prior/likelihood/posterior, PyMC model, sequential updating, validation, Bayesian vs. MLE comparison, error estimation, improvements, and references.
- [`shopper_data/`](./shopper_data) — the UCI Online Shoppers Purchasing Intention dataset (`online_shoppers_intention.csv`).
- `Assignment.docx` — original assignment instructions (not tracked in git).
- `script.md` — narration script for the video presentation (not tracked in git).
