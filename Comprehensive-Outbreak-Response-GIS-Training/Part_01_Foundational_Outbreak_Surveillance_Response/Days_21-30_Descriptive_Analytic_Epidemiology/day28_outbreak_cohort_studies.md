# **Day 28 – Outbreak Cohort Studies**
  
Bloom Level: Apply | Duration: 4 hrs  

## Objectives  

- Describe design and implementation of outbreak cohort studies.  
- Define exposed and unexposed groups based on case‐definition criteria.  
- Calculate attack rates, risk ratios, and risk differences from 2×2 tables.  
- Control confounding via stratification and multivariable models.  
- Interpret cohort findings to guide outbreak control measures.  

## Agenda  

1. Lecture: Outbreak Cohort Study Design (45 min)  
   - Prospective vs. retrospective cohort approaches  
   - Inclusion/exclusion criteria and exposure classification  
   - 2×2 contingency table for cohort analysis  
   - Measures: attack rate, risk ratio (RR), risk difference (RD)  
   - Strengths, biases, limitations  

   2×2 Contingency Table Structure:

   |                | Exposed (Yes) | Exposed (No) |
   |----------------|--------------|---------------|
   | Cases          | a             | b            |
   | Non-cases      | c             | d            |

2. Case Study: Salmonellosis in Poultry Flocks (30 min)  
   - Retrospective cohort using feed source exposure  
   - Compute group-specific attack rates and RR  

3. Group Exercise: Cohort Table Construction (45 min)  
   - Teams classify animals into exposed/unexposed  
   - Populate 2×2 tables, calculate a–d counts  
   - Compute AR, RR, and RD  

4. Interactive Demo: Analysis in R/Python (60 min)  
   - R: `epiR::epi.2by2()` for cohort measures  
   - Python: `pandas` + `statsmodels` for RR and RD  
   - Stratified analysis and basic logistic regression for adjustment  

5. Discussion & Q&A (30 min)  
   - Inferring causality and addressing loss to follow-up  
   - Dealing with missing exposure or outcome data  

---

## Exercise Details  

**Data Provided:**  
- `day28_cohort_data.csv`: animal IDs, exposure status, outcome status, covariates  
- `day28_population.csv`: flock sizes by exposure group  
- `cohort_template.xlsx`: spreadsheet template for 2×2 tables  

**Key Tasks:**  
1. Define inclusion criteria and classify each animal as exposed or unexposed.  
2. Calculate attack rates for both groups; compute RR and RD.  
3. Stratify analysis by a confounder (e.g., age group) and compare stratified RRs.  
4. Fit a logistic regression model to estimate adjusted odds ratios (OR) as an approximation of RR.  

---

## Assignment  

Submit to `assignments/day28/` by Day 29 morning:

1. Cohort Analysis Script (`day28_cohort_analysis.R` or `day28_cohort_analysis.py`)  
   - Annotated code calculating attack rates, RR, RD, and adjusted ORs.  

2. Results Tables (`day28_attack_rates.csv`, `day28_rr_rd_results.csv`)  
   - Tables with group counts, ARs, RRs, and RDs (plus 95% CIs).  

3. Figure (`day28_forest_plot.png`)  
   - Forest plot of RRs by subgroup or stratification factor.  

4. Epidemiological Summary (`day28_summary.md`)  
   - 400–500 words interpreting cohort findings and implications for control.  

5. Reflection (`day28_reflection.md`)  
   - 200 words on practical challenges in outbreak cohort studies and lessons learned.
