# **Day 26 – Chi-Square, Fisher’s Exact Test, and Confidence Intervals**

Bloom Level: Analyze & Apply | Duration: 4 hrs  

## Objectives  

- Understand when and how to apply chi-square tests and Fisher’s exact test to categorical data in animal disease investigations.  
- Compute chi-square statistics, p-values, and exact p-values for 2×2 and larger contingency tables.  
- Construct 95% confidence intervals for proportions and differences in proportions.  
- Interpret statistical test results and confidence intervals in the context of outbreak control decisions.  

## Agenda  

1. Lecture: Chi-Square vs Fisher’s Exact Test (45 min)  
   - Test assumptions: expected cell counts, sample size  
   - Choosing Fisher’s for small samples or sparse tables  
   - Overview of confidence-interval methods for proportions  

2. Case Study: Vaccine Efficacy in a Cattle Cohort (30 min)  
   - 2×2 table of vaccinated vs unvaccinated cases  
   - Calculate chi-square and Fisher’s p-values  

3. Group Exercise: Hand Calculations (45 min)  
   - Teams compute observed and expected counts  
   - Perform chi-square by formula; cross-check with Fisher’s exact for small-n subsets  

4. Interactive Demo: Scripted Analysis (60 min)  
   - R: `chisq.test()`, `fisher.test()`, `prop.test()`, `binom.test()`  
   - Python: `scipy.stats.chi2_contingency()`, `fisher_exact()`, custom CI functions  
   - Generate test results and confidence intervals for provided datasets  

5. Discussion & Q&A (30 min)  
   - Interpreting non-significant results in low-power settings  
   - Reporting both p-values and effect-size intervals  
   - Integrating statistical findings into surveillance recommendations  

---

## Exercise Details  

**Data Provided:**  
- `day26_contingency.csv`: categorical counts for two risk factors and outcomes  
- `day26_proportions.csv`: subgroup counts for CI calculations  
- Calculation template (`day26_tests_template.xlsx`)  

**Key Tasks:**  
1. Load the contingency dataset; run chi-square and Fisher’s exact tests on 2×2 and 3×2 tables.  
2. Calculate 95% confidence intervals for each proportion and for the difference between proportions.  
3. Compare test outcomes and interpret when to prefer exact methods.  

---

## Assignment  

Submit to `assignments/day26/` by Day 27 morning:

1. Statistical Test Scripts (`day26_tests.R` or `day26_tests.py`)  
2. Test Results Table (`day26_test_results.csv`)  
3. Confidence Interval Calculations (`day26_cis.csv`)  
4. Analytical Report (`day26_report.md`)  
   400–500 words interpreting test statistics, p-values, and confidence intervals.  
5. Reflection (`day26_reflection.md`)  
   200 words on challenges applying exact tests and CI methods in outbreak data.