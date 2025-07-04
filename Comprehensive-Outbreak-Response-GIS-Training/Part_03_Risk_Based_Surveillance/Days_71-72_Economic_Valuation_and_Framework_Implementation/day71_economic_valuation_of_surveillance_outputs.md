# **Day 71 – Economic Valuation of Surveillance Outputs**
  
Bloom Level: Evaluate & Create | Duration: 4 hrs  

## Objectives  

- Define economic valuation concepts for public-health surveillance outputs.  

- Identify and quantify benefits: cases detected, outbreaks averted, and costs avoided.  

- Select and apply valuation methods (net present value, benefit–cost ratio, willingness-to-pay).  

- Integrate surveillance metrics with economic data to model value under alternative scenarios.  

- Perform sensitivity and scenario analyses to assess robustness of valuation outcomes.  

---

## Agenda  

1. Lecture: Economic Valuation Frameworks (45 min)  
   - Cost–benefit vs. cost–utility vs. willingness-to-pay  
   - Discounting, time horizon, and perspective selection  

2. Demo: Valuation Modeling Tools (30 min)  
   - R: `dampack` workflows for NPV and BCR  
   - Python: pandas for benefit aggregation and custom valuation functions  

3. Lab Part 1 – Benefit Identification & Quantification (60 min)  
   - Load `day71_surveillance_metrics.csv` and `day71_outbreak_costs.csv`  
   - Compute avoided costs per detected case and per outbreak averted  
   - Tabulate total benefits by surveillance strategy  

4. Lab Part 2 – Valuation Modeling & Sensitivity (45 min)  
   - Apply discount rates from `day71_discount_rates.csv` to future benefits  
   - Calculate NPV, benefit–cost ratio, and net monetary benefit  
   - Run one-way sensitivity analyses on discount rate and unit cost parameters  

5. Discussion & Q&A (30 min)  
   - Interpreting valuation metrics for policy  
   - Communicating uncertainty and scenario outcomes  

---

## Exercise Details  

**Data Provided:**  
- `day71_surveillance_metrics.csv`: cases detected, outbreaks averted by week and strategy  
- `day71_outbreak_costs.csv`: average treatment cost per case, economic loss per outbreak  
- `day71_discount_rates.csv`: annual discount factors (0%, 3%, 5%)  
- `day71_wtp_survey.csv`: willingness-to-pay estimates from stakeholders  

**Key Tasks:**  
1. Merge surveillance outputs with cost data to calculate total avoided costs for each strategy.  
2. Compute present value of benefits over a 5-year horizon using multiple discount rates.  
3. Calculate benefit–cost ratios and net monetary benefit for passive and risk-based approaches.  
4. Incorporate willingness-to-pay data to adjust benefit estimates.  
5. Generate sensitivity analyses and visualize impacts of varying discount rates and cost parameters.  

---

## Assignment  

Submit to `assignments/day71/` by Day 72 morning:  

1. Economic Valuation Script  
   - `day71_valuation.R` or `day71_valuation.py` with annotated steps for benefit calculation, discounting, and sensitivity analyses.  

2. Benefit–Cost Summary Table  
   - `day71_benefit_cost.csv` listing strategy, total benefits, total costs, NPV, BCR, and net monetary benefit.  

3. Valuation Figures  
   - `day71_npv_trends.png` (NPV over time under different discount rates)  
   - `day71_bcr_sensitivity.png` (tornado plot of BCR sensitivity)  

4. Analytical Report (`day71_report.md`, 400 words)  
   - Describe methods, key valuation results, scenario comparisons, and policy implications.  

5. Reflection (`day71_reflection.md`, 200 words)  
   - Reflect on challenges in assigning economic values, data limitations, and presenting uncertainty to stakeholders.  

---  

This session equips you to translate surveillance outputs into economic terms, guiding resource allocation and policy decisions with quantifiable value estimates.
