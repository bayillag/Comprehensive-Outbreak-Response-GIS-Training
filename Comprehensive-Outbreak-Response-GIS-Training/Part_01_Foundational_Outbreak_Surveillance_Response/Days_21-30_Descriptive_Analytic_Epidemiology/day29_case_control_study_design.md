# **Day 29 – Case–Control Study Design**

Bloom Level: Analyze & Apply | Duration: 4 hrs  

## Objectives  

- Define the principles and applications of case–control studies in animal health.  
- Establish rigorous case definitions and control selection criteria.  
- Construct and analyze 2×2 tables to calculate odds ratios (ORs).  
- Recognize and address key biases: selection, information, and confounding.  
- Design both unmatched and matched case–control frameworks.  

## Agenda  

1. Lecture: Case–Control Theory (45 min)  
   - Retrospective design and the odds ratio as the measure of association  
   - Crafting precise case definitions and sourcing cases  
   - Control selection strategies: population‐based, hospital‐based, and matching  
   - 2×2 Contingency Table Structure  

     |                | Exposed (Yes) | Exposed (No) |
     |----------------|---------------|--------------|
     | Cases          | a             | b            |
     | Controls       | c             | d            |

     Odds Ratio (OR) = (a × d) / (b × c)  

2. Case Study: Leptospirosis in Cattle (30 min)  
   - Review a published case–control investigation  
   - Discuss enrollment of cases, control sampling, and exposure assessment  

3. Group Exercise: Study Design Workshop (45 min)  
   - Teams draft a case definition and control inclusion/exclusion criteria  
   - Develop a sampling plan for unmatched vs. matched controls  
   - Identify potential confounders and matching variables  

4. Interactive Demo: Data Analysis in R/Python (60 min)  
   - R: `epiR::epi.2by2()`, `glm(family=binomial)`  
   - Python: `statsmodels.api.Logit`  
   - Compute crude OR with 95% CI; adjust for confounders via logistic regression  

5. Discussion & Q&A (30 min)  
   - Evaluating selection and information bias  
   - Interpreting matched vs. unmatched analyses  
   - Reporting standards (STROBE guidelines for case–control studies)  

---

## Exercise Details  

**Data Provided:**  
- `day29_cases.csv`: confirmed case records with exposure and covariate fields  
- `day29_controls.csv`: sampled control records with identical exposure and covariate schema  
- `exposure_codebook.xlsx`: definitions and coding dictionary for all exposure variables  

**Key Tasks:**  
1. Apply the case definition to select eligible cases.  
2. Sample controls according to your control‐selection plan (unmatched or matched).  
3. Build a 2×2 table of exposure versus disease status; hand‐compute the crude OR.  
4. Script the OR calculation and logistic regression to obtain adjusted ORs.  

---

## Assignment  

Submit to `assignments/day29/` by Day 30 morning:

1. Study Design Plan (`day29_design.md`)  
   - 400–500 words detailing case definition, control selection strategy, matching variables, and bias mitigation.  

2. 2×2 Table & Hand Calculations (`day29_2x2.md`)  
   - Completed contingency table with hand‐computed OR and interpretation.  

3. Analysis Script (`day29_analysis.R` or `day29_analysis.py`)  
   - Annotated code reading data, calculating crude and adjusted ORs, and outputting results with 95% CIs.  

4. Results Table (`day29_results.csv`)  
   - Exposure counts, crude OR, adjusted ORs, and confidence intervals.  

5. Epidemiological Report (`day29_report.md`)  
   - 400–500 words discussing key findings, validity considerations, and implications for control measures.  

6. Reflection (`day29_reflection.md`)  
   - 200 words on challenges in control selection, matching procedures, and interpreting ORs in an animal health context.
