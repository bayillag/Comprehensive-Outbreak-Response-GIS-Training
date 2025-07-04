# **Day 25 – Measures of Association—Risk Ratios and Odds Ratios**  
Bloom Level: Analyze & Apply | Duration: 4 hrs  

## Objectives  

- Understand the role of measures of association in animal disease investigations.  
- Calculate risk ratios (RR) and odds ratios (OR) from 2×2 tables.  
- Interpret point estimates and 95% confidence intervals for RR and OR.  
- Choose the appropriate measure based on study design and data structure.  

---

## Agenda  

1. Lecture: Measures of Association (45 min)  
   - Definitions and interpretations of RR and OR  
   - Constructing a 2×2 contingency table for cohort and case–control data  
   - Formulae for RR and OR and their confidence intervals  

2. Case Study: Brucellosis in Goats (30 min)  
   - Cohort analysis: calculating RR for exposure to communal watering points  
   - Case–control analysis: computing OR for seropositivity and contact history  

3. Group Exercise: Hand Calculations (45 min)  
   - Teams receive a summarized dataset  
   - Compute a, b, c, d counts, then calculate RR and OR by hand  

4. Interactive Demo: Scripted Computation (60 min)  
   - R: `epiR::epi.2by2()` example  
   - Python: custom function using `pandas` and `statsmodels`  
   - Generate estimates and CIs, compare outputs  

5. Discussion & Q&A (30 min)  
   - When OR approximates RR  
   - Interpretation pitfalls in low‐prevalence settings  
   - Reporting and communication of measures to stakeholders  

---

## Key Comparison  

| Measure         | Formula                                  | Study Design     | Interpretation                         |
|-----------------|------------------------------------------|------------------|----------------------------------------|
| Risk Ratio (RR) | (a / (a+c)) / (b / (b+d))               | Cohort           | Relative risk in exposed vs unexposed |
| Odds Ratio (OR) | (a × d) / (b × c)                        | Case–Control, Logistic models | Odds in exposed vs unexposed         |

2×2 Contingency Table Structure:

|                | Exposed (Yes) | Exposed (No) |
|----------------|---------------|--------------|
| Diseased       | a             | b            |
| Not Diseased   | c             | d            |

---

## Exercise Details  

**Data Provided:**  
- `day25_cohort.csv`: cohort dataset with exposure and outcome flags  
- `day25_casecontrol.csv`: case–control sample with case status and exposure history  
- Calculation template (`day25_2x2_template.xlsx`)  

**Key Tasks:**  
1. Populate the 2×2 tables for both datasets and compute RR and OR by hand.  
2. Script RR and OR calculations in R and Python, including 95% CIs.  
3. Compare hand‐computed and script outputs, investigate any discrepancies.  

---

## Assignment  

Submit to `assignments/day25/` by Day 26 morning:

1. 2×2 Table Calculations (`day25_hand_calculations.md`)  
   - Completed tables with hand‐computed RR, OR, and interpretations.  

2. R/Python Script (`day25_measures.R` or `day25_measures.py`)  
   - Annotated code that reads data, calculates RR and OR, and outputs results with CIs.  

3. Results Table (`day25_results.csv`)  
   - Summary of measures, confidence intervals, and data counts.  

4. Interpretation Report (`day25_report.md`) (400–500 words)  
   - Discuss findings, differences between RR and OR, and implications for outbreak control.  

5. Reflection (`day25_reflection.md`) (200 words)  
   - Challenges in choosing and interpreting measures of association and lessons learned.
