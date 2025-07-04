# **Day 27 – Introduction to Time‐to‐Event Analysis**

Bloom Level: Understand & Apply | Duration: 4 hrs  

## Objectives  

- Define key concepts: time origin, event, censoring, survival and hazard functions.  
- Estimate and plot Kaplan–Meier survival curves in R and Python.  
- Compare survival between groups using the log-rank test.  
- Fit a Cox proportional hazards model and interpret hazard ratios.  

## Agenda  

1. Lecture: Fundamentals of Time-to-Event Analysis (45 min)  
   - Event definitions, right‐censoring, survival function S(t), hazard function h(t)  
   - When to use survival methods in animal health (e.g., time to recovery, time to death)  

2. Demo: Kaplan–Meier Estimation (30 min)  
   - R: `survival::survfit()`, `survminer::ggsurvplot()`  
   - Python: `lifelines.KaplanMeierFitter` and plotting  

3. Lab Part 1 – Generating Survival Curves (60 min)  
   - Load `day27_followup.csv`, define `time` and `event` indicators  
   - Fit overall Kaplan–Meier curve; extract median survival and confidence bands  
   - Stratify by key covariate (e.g., species or treatment group)  

4. Lab Part 2 – Log‐Rank Test & Cox Model (45 min)  
   - Perform log-rank comparisons across strata (`survdiff()` in R, `logrank_test` in Python)  
   - Fit a multivariable Cox PH model (`coxph()` or `CoxPHFitter`); test proportional hazards  

5. Discussion & Q&A (30 min)  
   - Interpreting survival probabilities and hazard ratios  
   - Addressing censoring patterns and model assumptions in outbreak data  

---

## Exercise Details  

**Data Provided:**  
- `day27_followup.csv`: records with `animal_id`, `start_date`, `event_date`, `event_flag` (1=event, 0=censored)  
- `day27_covariates.csv`: covariate table (`animal_id`, `species`, `age_group`, `treatment`)  

**Key Tasks:**  
1. Merge follow-up and covariate files; compute `time = event_date – start_date`.  
2. Fit and plot Kaplan–Meier curves overall and by group; report median survival and 95% CI.  
3. Conduct a log-rank test to compare strata.  
4. Build a Cox proportional hazards model; interpret coefficients and check PH assumption.  

---

## Assignment  

Submit to `assignments/day27/` by Day 28 morning:

1. Kaplan–Meier Script (`day27_km.R` or `day27_km.py`)  
2. Cox PH Script (`day27_cox.R` or `day27_cox.py`)  
3. Survival Plots (`day27_survival_curves.png`)  
4. Analytical Report (`day27_report.md`)  
   - 400–500 words describing methods, key results, and epidemiological interpretation.  
5. Reflection (`day27_reflection.md`)  
   - 200 words on handling censoring, assumptions challenges, and insights from time-to-event analysis.
