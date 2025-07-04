# **Day 32 – Survival Analysis for Animal Health Events**

Bloom Level: Apply & Evaluate | Duration: 4 hrs  

## Objectives  

- Reinforce Kaplan–Meier and Cox proportional hazards methods.  
- Introduce parametric survival models (exponential, Weibull) for event-time data.  
- Assess and address non–proportional hazards via time-dependent covariates and stratification.  
- Model competing risks (e.g., death vs. culling) and incorporate herd-level frailty effects.  
- Interpret parameter estimates and select the most appropriate survival framework.  

## Agenda  

1. Lecture: Advanced Survival Techniques (45 min)  
   - Parametric vs. semiparametric models  
   - Proportional hazards assumption checks  
   - Time-dependent covariates and strata  
   - Competing risks basics and frailty models  

2. Demo: Parametric Models & PH Diagnostics (30 min)  
   - R: `survival::survreg()` vs `coxph()`; `cox.zph()` for proportionality  
   - Python: `lifelines.WeibullFitter`, `CoxPHFitter`, and `check_assumptions()`  

3. Lab Part 1 – Fitting Parametric Survival Models (60 min)  
   - Load `day32_followup.csv` and `day32_covariates.csv`  
   - Fit exponential and Weibull models; compare AIC and log-likelihood  
   - Plot survival functions and overlay Kaplan–Meier estimates  

4. Lab Part 2 – Competing Risks & Frailty (45 min)  
   - Define competing events: death vs. culling (event codes in `day32_followup.csv`)  
   - Use Fine–Gray subdistribution hazards (`cmprsk` in R; `lifelines.CumulativeIncidenceFitter`)  
   - Fit a shared-frailty Cox model by herd ID (R: `coxph(..., frailty=~herd_id)`; Python: `CoxPHFitter(strata=['herd_id'])`)  

5. Discussion & Q&A (30 min)  
   - Choosing between model types under field constraints  
   - Communicating complex survival results to stakeholders  

---

## Exercise Details  

**Data Provided:**  
- `day32_followup.csv`: `animal_id`, `start_date`, `event_date`, `event_type` (0=censored, 1=death, 2=culling)  
- `day32_covariates.csv`: `animal_id`, `species`, `age_group`, `treatment`, `herd_id`  
- `day32_standard_pop.csv`: optional herd-level counts for offset analyses  

**Key Tasks:**  
1. Merge follow-up and covariates; compute `time = event_date – start_date`.  
2. Fit exponential and Weibull parametric models; compare fit statistics.  
3. Check PH assumption for Cox model; if violated, incorporate time-dependent covariates or stratify.  
4. Model competing risks: estimate cumulative incidence for each event type.  
5. Fit a frailty model by herd; interpret variance component and hazard ratios.  

---

## Assignment  

Submit to `assignments/day32/` by Day 33 morning:

1. Parametric & Cox Scripts (`day32_parametric.R` or `.py`, `day32_cox.R` or `.py`)  
2. Competing Risks & Frailty Script (`day32_competing_frailty.R` or `.py`)  
3. Survival Plots (`day32_parametric_survival.png`, `day32_cumulative_incidence.png`)  
4. Model Comparison Table (`day32_model_comparison.csv`)  
   - Distribution, parameter estimates, AIC/log-likelihood, PH test p-value  
5. Analytical Report (`day32_report.md`) (400–500 words describing model selection, diagnostics, and epidemiological interpretation)  
6. Reflection (`day32_reflection.md`) (200 words on the trade-offs of parametric vs. semiparametric and handling competing risks)
