# **Day 33 – Estimating Reproductive Number (R₀)**

Bloom Level: Analyze & Apply | Duration: 4 hrs  

## Objectives  

- Explain the concept of the basic reproductive number (R₀) and the effective reproductive number (Rₑ).  
- Identify assumptions underlying different estimation methods (exponential growth, maximum likelihood, attack‐rate).  
- Estimate R₀ from incidence data using exponential growth and likelihood approaches.  
- Apply the attack‐rate method for closed populations.  
- Conduct sensitivity analyses on serial‐interval (SI) parameter choices and interpret impacts on R₀ estimates.  

## Agenda  

1. Lecture: Reproductive Number Fundamentals (45 min)  
   - Definition of R₀, components (contact rate, transmission probability, infectious period)  
   - Distinction between R₀ and Rₑ, threshold conditions for epidemic growth or decline  

2. Demo: Overview of Estimation Methods (30 min)  
   - Exponential growth method: fitting log‐linear incidence to obtain growth rate (r)  
   - Maximum likelihood estimation (Wallinga–Teunis, Poisson regression)  
   - Attack‐rate formula for closed cohorts (final size equation)  

3. Lab Part 1 – Exponential Growth R₀ Estimation (60 min)  
   - Load `day33_incidence.csv` and aggregate daily cases  
   - Estimate growth rate (r) via linear regression on log‐incidence  
   - Compute R₀ using moment‐generating function of SI distribution  

4. Lab Part 2 – Likelihood & Attack‐Rate Methods (45 min)  
   - Use R’s `R0::estimate.R()` or Python custom MLE to fit Poisson model  
   - Apply final‐size attack‐rate equation to closed‐population data  
   - Compare R₀ estimates across methods  

5. Discussion & Q&A (30 min)  
   - Influence of SI mean and SD on R₀ estimates  
   - Choosing methods based on data quality and outbreak stage  
   - Implications of R₀ values for control strategies  

---

## Exercise Details  

**Data Provided:**  
- `day33_incidence.csv`: daily case counts (`date`, `cases`)  
- `day33_SI.csv`: observed serial‐interval pairs (`infector_date`, `infectee_date`)  
- `generation_time.json`: recommended SI distribution parameters (mean, sd)  

**Key Tasks:**  
1. Estimate the exponential growth rate (r) from the epidemic’s ascending phase.  
2. Calculate R₀ using the exponential‐growth formula:  
   \[R_0 = 1 / M(-r) \[  
   where \(M\) is the SI moment‐generating function.  
3. Fit a maximum likelihood model for R₀ in R or Python.  
4. Compute R₀ via the final‐size attack‐rate equation for a closed herd.  
5. Perform sensitivity analyses by varying SI mean (±2 days) and SD, and visualize R₀ changes.  

---

## Assignment  

Submit to `assignments/day33/` by Day 34 morning:

1. R₀ Estimation Script (`day33_R0_estimation.R` or `day33_R0_estimation.py`)  
2. Results Table (`day33_R0_results.csv`)  
   - Growth rate, R₀ estimates by method, SI parameters used  
3. Sensitivity Analysis Plot (`day33_sensitivity.png`)  
   - R₀ versus SI mean and SD variations  
4. Analytical Report (`day33_report.md`)  
   - 400–500 words on methods, results comparison, and epidemiological interpretation  
5. Reflection (`day33_reflection.md`)  
   - 200 words on the limitations of R₀ estimation and implications for outbreak control  

---