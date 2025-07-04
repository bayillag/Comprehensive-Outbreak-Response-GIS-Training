# **Day 36 – Bayesian Methods in Outbreak Analysis**

Bloom Level: Evaluate & Apply | Duration: 4 hrs  

## Objectives  

- Grasp Bayesian inference concepts: prior, likelihood, posterior.  
- Apply Bayesian estimation to outbreak parameters (e.g., prevalence, incidence rates).  
- Run MCMC sampling for posterior inference using R (`rstanarm`, `brms`) and Python (`PyMC3`/`PyMC4`).  
- Compare posterior credible intervals with frequentist confidence intervals.  
- Perform posterior predictive checks for model validation and sensitivity to priors.  

## Agenda  

1. Lecture: Bayesian Inference Basics (45 min)  
   - Bayes’ theorem, conjugate and non-informative priors  
   - Interpreting posteriors and credible intervals  
   - Prior sensitivity and model checking  

2. Demo: MCMC Sampling Workflows (30 min)  
   - R: `rstanarm::stan_glm()`, `brms::brm()` pipelines  
   - Python: `pymc3.Model()`, sampling with `pm.sample()`, diagnostics with `arviz`  

3. Lab Part 1 – Seroprevalence Estimation (60 min)  
   - Data: `day36_serosurvey.csv` (tested/positive by zone/species)  
   - Fit beta-binomial model for prevalence in each stratum  
   - Extract posterior medians and 95% credible intervals  

4. Lab Part 2 – Bayesian Poisson Regression (45 min)  
   - Data: `day36_incidence.csv` with `cases`, `animals` (offset) and covariates  
   - Specify Poisson model: `cases ~ offset(log(animals)) + predictors`  
   - Sample posterior, compute incidence rate ratios and credible bands  

5. Discussion & Q&A (30 min)  
   - Interpreting and communicating Bayesian results  
   - Convergence diagnostics: trace plots, R-hat, ESS  
   - Computational trade-offs and selecting priors in low-data settings  

---

## Exercise Details  

**Data Provided:**  
- `day36_serosurvey.csv`: `zone`, `species`, `tested`, `positive`  
- `day36_incidence.csv`: `zone`, `week`, `cases`, `animals`  
- `day36_covariates.csv`: zone-level predictors (e.g., vaccination coverage)  
- Templates: `day36_rstan_template.R`, `day36_pymc_template.py`  

**Key Tasks:**  
1. Select and justify priors in your script (e.g., Beta(1,1) vs Beta(2,2)).  
2. Run MCMC sampling; assess convergence via trace plots and R-hat.  
3. Summarize posterior distributions (median, 95% credible intervals) in a table.  
4. Perform a posterior predictive check: simulate data from posterior and compare to observed counts.  

---

## Assignment  

Submit to `assignments/day36/` by Day 37 morning:

1. Bayesian Analysis Script (`day36_bayesian.R` or `day36_bayesian.py`)  
2. Posterior Summary Table (`day36_posterior_summaries.csv`)  
3. MCMC Diagnostics (`day36_traceplots.png`, `day36_ppc.png`)  
4. Analytical Report (`day36_report.md`)  
   - 400–500 words on model choice, prior sensitivity, posterior interpretation, and check results.  

5. Reflection (`day36_reflection.md`)  
   - 200 words on the challenges of Bayesian modeling in outbreak contexts and lessons learned.
