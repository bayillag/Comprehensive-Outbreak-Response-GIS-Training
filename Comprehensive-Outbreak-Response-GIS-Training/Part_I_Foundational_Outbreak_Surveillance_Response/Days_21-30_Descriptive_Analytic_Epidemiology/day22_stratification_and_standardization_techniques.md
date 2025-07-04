# **Day 22 – Stratification and Standardization Techniques**

Bloom Level: Analyze & Apply | Duration: 4 hrs  

## Objectives  

- Define stratification and standardization in epidemiological analysis.  
- Describe direct and indirect standardization methods for rate comparisons.  
- Perform stratified incidence and attack-rate calculations by species, age group, and zone.  
- Compute directly standardized rates using a reference population.  

## Agenda  

1. Lecture: Stratification vs Standardization (45 min)  
   - Purpose of stratification: control for confounding by subgroup analysis  
   - Standardization goals: adjust rates for population structure differences  
   - Comparison table  

   | Concept           | Definition                                                   | Use Case                                |
   |-------------------|--------------------------------------------------------------|-----------------------------------------|
   | Stratification    | Separating data into subgroups (e.g., species, age, zone)    | Identify subgroup-specific risks        |
   | Direct Standardization   | Applying age/stratum-specific rates to a standard population | Compare overall rates across populations |
   | Indirect Standardization | Applying standard rates to study population structure      | Compute standardized morbidity ratios   |

2. Demo: Implementing Direct Standardization (30 min)  
   - R: `epitools::ageadjust.direct()` example  
   - Python: custom function using `pandas`  

3. Lab Part 1 – Stratified Analysis (60 min)  
   - Load `day22_cases.csv` and `day22_population.csv`  
   - Calculate incidence rates by species–age group and by zone  
   - Tabulate subgroup counts and rates  

4. Lab Part 2 – Standardization Methods (45 min)  
   - Apply direct standardization using `day22_standard_pop.csv`  
   - Compute standardized incidence ratios (SIR) via indirect method  
   - Compare crude vs standardized rates  

5. Discussion & Q&A (30 min)  
   - Interpreting differences between crude and adjusted rates  
   - Choosing the appropriate standard population  
   - Limitations and assumptions of each method  

---

## Exercise Details  

**Data Provided:**  
- `day22_cases.csv`: case counts with `species`, `age_group`, `zone`, `onset_date`  
- `day22_population.csv`: at-risk population by `species`, `age_group`, and `zone`  
- `day22_standard_pop.csv`: reference population distribution by `age_group`  

**Key Tasks:**  
1. Stratify the dataset and calculate subgroup-specific incidence rates (per 1,000 animals).  
2. Perform direct standardization: apply subgroup rates to the standard population and compute overall rate.  
3. Perform indirect standardization: calculate expected cases and compute SIR for each zone.  
4. Create a table comparing crude, directly standardized, and indirectly standardized rates.  

---

## Assignment  

Submit to `assignments/day22/` by Day 23 morning:

1. Stratified Analysis Script (`day22_stratified_analysis.R` or `day22_stratified_analysis.py`)  
2. Standardization Script (`day22_standardization.R` or `day22_standardization.py`)  
3. Results Tables (`day22_subgroup_rates.csv`, `day22_standardized_rates.csv`)  
4. Plots (`day22_rate_comparison.png`)  
5. Analytical Report (`day22_report.md`)  
   • 400–500 words describing methods, results, and interpretation of adjusted rates.  
6. Reflection (`day22_reflection.md`)  
   • 200 words on challenges in standardization and the impact of standard population choice.
