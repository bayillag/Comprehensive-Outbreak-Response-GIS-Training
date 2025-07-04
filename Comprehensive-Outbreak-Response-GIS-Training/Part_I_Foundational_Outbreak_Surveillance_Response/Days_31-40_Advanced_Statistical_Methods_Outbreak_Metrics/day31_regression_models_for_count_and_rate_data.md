# **Day 31 – Regression Models for Count and Rate Data**

Bloom Level: Apply & Evaluate | Duration: 4 hrs  

## Objectives  

- Differentiate count versus rate outcomes and select appropriate regression frameworks (Poisson, negative binomial, zero-inflated).  
- Incorporate offset terms to model rates (e.g., cases per animal-time at risk).  
- Diagnose overdispersion and assess model fit.  
- Interpret incidence rate ratios and compare model outputs to guide control decisions.  

## Agenda  

1. Lecture: Introduction to Count and Rate Regression (45 min)  
   - Poisson regression fundamentals and log‐link interpretation  
   - Overdispersion: when Poisson assumptions fail  
   - Negative binomial and zero-inflated alternatives  
   - Use of offsets for population/time denominators  

2. Case Study: Modeling Foot-and-Mouth Disease Counts (30 min)  
   - Dataset with weekly case counts by zone and herd size  
   - Interpret parameter estimates and rate ratios  

3. Group Exercise: Building and Comparing Models (45 min)  
   - Teams fit Poisson models with and without offsets  
   - Diagnose overdispersion (deviance/df, dispersion tests)  
   - Fit negative binomial or zero-inflated models and compare AIC  

4. Interactive Demo: Implementation in R and Python (60 min)  
   - R: `glm(..., family=poisson)`, `MASS::glm.nb()`, `pscl::zeroinfl()`  
   - Python: `statsmodels.api.Poisson`, `statsmodels.discrete.discrete_model.NegativeBinomial`, `ZeroInflatedPoisson`  
   - Generate diagnostic plots: residuals vs. fitted, Q-Q  

5. Discussion & Q&A (30 min)  
   - Choosing between Poisson and NB in field settings  
   - Communicating rate ratios and model assumptions to stakeholders  

---

## Exercise Details  

**Data Provided:**  
- `day31_case_counts.csv`: weekly case counts by `zone` and `week`  
- `day31_population.csv`: herd/flock counts per `zone` and `week`  
- `day31_covariates.csv`: zone‐level predictors (e.g., vaccination coverage, species mix)  

**Key Tasks:**  
1. Merge case and population files; compute offset = log(population).  
2. Fit a Poisson regression predicting `cases ~ covariates + offset(log_pop)`.  
3. Test for overdispersion; if present, fit a negative binomial model.  
4. Optionally fit a zero-inflated Poisson or NB if excess zeros exist.  
5. Extract incidence rate ratios, 95% CIs, and compare model goodness‐of‐fit (AIC, residual deviance).  

---

## Assignment  

Submit to `assignments/day31/` by Day 32 morning:

1. Regression Scripts (`day31_poisson.R` or `day31_poisson.py`, and `day31_nb.R` or `day31_nb.py`)  
2. Model Results Table (`day31_model_results.csv`)  
   - Estimates, standard errors, IRRs, 95% CIs, AIC/deviance for each model  
3. Diagnostic Plots (`day31_diagnostics.png`)  
   - Residuals vs. fitted, dispersion checks, zero-inflation diagnostics  
4. Analytical Report (`day31_report.md`)  
   - 400–500 words comparing models, interpreting IRRs, and recommending the best approach  
5. Reflection (`day31_reflection.md`)  
   - 200 words on practical challenges in modeling count data and lessons on overdispersion and offsets