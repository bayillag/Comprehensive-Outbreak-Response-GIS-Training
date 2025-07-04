# **Day 68 – Economic Evaluation Methods for Surveillance**
  
Bloom Level: Evaluate & Create | Duration: 4 hrs  

## Objectives  

- Describe economic evaluation frameworks: cost‐of‐illness, cost‐effectiveness (CEA), cost‐benefit (CBA), and cost‐utility (CUA).  

- Identify and categorize surveillance costs: fixed vs. variable, direct vs. indirect, programmatic vs. societal.  

- Calculate total and incremental costs for alternative surveillance strategies.  

- Compute key metrics: average cost‐effectiveness ratios, incremental cost‐effectiveness ratios (ICERs), net monetary benefit, and benefit-cost ratios.  

- Perform sensitivity analyses to assess robustness of economic conclusions.  

---

## Agenda  

1. Lecture: Economic Evaluation Concepts (45 min)  
   - Overview of CEA, CBA, CUA frameworks  
   - Perspective selection (health system vs. societal)  
   - Time horizon, discounting, and analytic assumptions  

2. Demo: Cost Data Processing & Analysis (30 min)  
   - R: using `dampack`, `hesim`, or base workflows for cost summaries and ICER  
   - Python: pandas for cost tabulation and custom CEA functions  

3. Lab Part 1 – Cost Classification & Aggregation (60 min)  
   - Load `day68_costs.csv` (itemized program costs) and `day68_resource_use.csv` (activity volumes)  
   - Categorize costs into fixed/variable and direct/indirect  
   - Aggregate total and per‐unit costs for two surveillance scenarios  

4. Lab Part 2 – Cost‐Effectiveness Analysis (45 min)  
   - Import `day68_outcomes.csv` (cases detected, outbreaks prevented)  
   - Compute average cost‐effectiveness ratios and ICER between Strategy A (passive) and B (risk‐based)  
   - Plot cost‐effectiveness plane and cost‐effectiveness acceptability curve (CEAC)  

5. Discussion & Q&A (30 min)  
   - Interpreting ICERs and willingness‐to‐pay thresholds  
   - Conducting one‐way and probabilistic sensitivity analyses  
   - Communicating economic findings to stakeholders  

---

## Exercise Details  

**Data Provided:**  
- `day68_costs.csv`: line-item costs by category and strategy  
- `day68_resource_use.csv`: number of visits, tests, travel days per zone  
- `day68_outcomes.csv`: surveillance yield (cases detected), response metrics (outbreak days averted)  
- `day68_parameter_ranges.csv`: lower/upper bounds for sensitivity analysis  

**Key Tasks:**  
1. Merge cost and resource‐use tables; calculate total costs per strategy and cost per activity.  
2. Link outcomes to cost data; derive cost per case detected and cost per outbreak day averted.  
3. Compute ICER = (Cost_B – Cost_A) / (Effect_B – Effect_A).  
4. Generate:  
   - Cost‐effectiveness plane scatterplot  
   - CEAC showing probability of cost‐effectiveness across willingness‐to‐pay values  
   - Tornado diagram for one‐way sensitivity analysis on key parameters  

---

## Assignment  

Submit to `assignments/day68/` by Day 69 morning:  

1. Economic Evaluation Script  
   - `day68_economic_evaluation.R` or `day68_economic_evaluation.py` with annotated cost calculations, ICER, and sensitivity analyses.  

2. Cost Summary Table  
   - `day68_costs_summary.csv` detailing fixed, variable, direct, and indirect costs per strategy.  

3. CEA Results  
   - `day68_cea_results.csv` with average CERs, ICER, net monetary benefit at selected thresholds.  

4. Figures  
   - `day68_ce_plane.png` (cost‐effectiveness scatter)  
   - `day68_ceac.png` (acceptability curve)  
   - `day68_sensitivity_tornado.png` (tornado plot)  

5. Analytical Report (`day68_report.md`, 400 words)  
   - Describe methods, key findings, threshold interpretations, and recommendations for surveillance investment.  

6. Reflection (`day68_reflection.md`, 200 words)  
   - Reflect on challenges in data collection, model assumptions, and translating economic results into policy guidance.  

---  

This module empowers you to weigh costs against surveillance benefits, guiding efficient allocation of limited resources in disease prevention efforts.
