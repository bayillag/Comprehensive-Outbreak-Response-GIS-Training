# **Day 21 – Calculating Incidence, Prevalence, and Attack Rates**

Bloom Level: Apply | Duration: 4 hrs  

## Objectives  

- Define incidence rate, prevalence, and attack rate in animal health contexts.  
- Differentiate between period and point measures, appropriate denominators, and time at risk.  
- Compute incidence, prevalence, and attack rates using outbreak and population data.  
- Interpret and compare these measures to guide control strategies.  

## Agenda  

1. Lecture: Epidemiological Measures (45 min)  
   - Incidence rate vs. cumulative incidence  
   - Point prevalence vs. period prevalence  
   - Attack rate in outbreak investigations  
   - Choosing denominators and time windows  

2. Demo: Formula Implementation (30 min)  
   - R functions (`epiR`, `surveillance`) and Python (`pandas`, custom)  
   - Handling varying time at risk and population adjustments  

3. Lab Part 1 – Incidence & Prevalence (60 min)  
   - Load `day21_population.csv` and `day21_case_events.csv`  
   - Calculate weekly incidence rates per 1,000 animals  
   - Compute point prevalence at specified survey dates  

4. Lab Part 2 – Attack Rates (45 min)  
   - Define the outbreak period from `day21_outbreak_log.csv`  
   - Calculate species-specific and zone-specific attack rates  
   - Compare attack rates across risk strata  

5. Discussion & Q&A (30 min)  
   - Interpreting differences among measures  
   - Implications for resource allocation and targeted interventions  

---

## Exercise Details  

**Data Provided:**  
- `day21_population.csv`: herd/flock counts by zone and species  
- `day21_case_events.csv`: case onset dates, species, and zone codes  
- `day21_outbreak_log.csv`: start/end dates and total cases per zone  

**Key Tasks:**  
1. Compute weekly incidence rates per 1,000 animals for each species and zone.  
2. Determine point prevalence on two survey dates and compare trends.  
3. Calculate cumulative attack rates for the outbreak period, stratified by species and zone.  
4. Visualize results: time-series of incidence, bar chart of attack rates.  

---

## Assignment  

Submit to `assignments/day21/` by Day 22 morning:

1. Calculation Scripts (`day21_incidence_prevalence.R` or `day21_incidence_prevalence.py`)  
2. Results Tables (`day21_rates.csv`, `day21_attack_rates.csv`)  
3. Plots (`day21_incidence_plot.png`, `day21_attack_rate_chart.png`)  
4. Analytical Report (`day21_report.md`) (400–500 words interpreting measures and recommendations)  
5. Reflection (`day21_reflection.md`) (200 words on challenges in choosing denominators and time windows)
