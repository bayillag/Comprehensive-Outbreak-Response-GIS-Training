# **Day 33 – Estimating Reproductive Number (R₀)**

Bloom Level: Analyze & Apply | Duration: 4 hrs  

---

## Conceptual Overview

Basic Reproductive Number (R₀)
R₀ (“R nought”) is the average number of secondary cases produced by one infectious individual in a fully susceptible population. It depends on:  
- Contact rate (interactions per time unit)  
- Transmission probability per contact  
- Duration of infectiousness  
- Proportion of contacts who remain susceptible  

If R₀ < 1, an introduced pathogen will die out. If R₀ > 1, it can spark an epidemic. As susceptible hosts decline, Rₑ (the effective reproductive number) falls below 1 and transmission peters out.  

Estimated Dissemination Ratio (EDR)
EDR approximates R₀ in real time. Over an n-day window ending on day i:  

`plaintext
EDRₙ(i) = 
  [Cases from day i−(n−1) to day i] 
  ÷ [Cases from day i−2n to day i−n]
`  

An EDR consistently below 1 indicates that control measures are working; values above 1 signal ongoing spread.  

---

## Objectives

- Define R₀ and differentiate it from Rₑ  
- Detail the components driving R₀ (contact rate, transmission probability, infectious period, susceptibility)  
- Compare three estimation methods: exponential growth, maximum likelihood, and attack-rate  
- Calculate R₀ from incidence data using growth‐rate and likelihood approaches  
- Analyze how serial-interval assumptions affect R₀ via sensitivity testing  
- Compute and interpret EDR as a real-time proxy for transmission potential  

---

## Agenda

1. Lecture (45 min):  
   - R₀ vs. Rₑ, threshold for epidemic growth  
   - Drivers of R₀ and implications for control  

2. Demo (30 min):  
   - Exponential-growth fitting (log-linear model)  
   - Maximum-likelihood frameworks (Wallinga–Teunis, Poisson regression)  
   - Final-size attack-rate equation  

3. Lab Part 1 (60 min):  
   - Load day33_incidence.csv  
   - Fit log-linear model to estimate growth rate (r)  
   - Compute R₀ via the SI moment-generating function:  
     $$R₀ = \frac{1}{M(-r)}$$  

4. Lab Part 2 (45 min):  
   - Use R0::estimate.R() or Python MLE to fit Poisson model  
   - Apply attack-rate formula to closed-population data  
   - Calculate daily EDR₇ and plot as a time series  

5. Discussion & Q&A (30 min):  
   - Impact of SI mean/SD shifts on R₀ estimates  
   - Choosing methods by outbreak stage and data quality  
   - Leveraging R₀ and EDR for strategic interventions  

---

## Lab Exercises

- Exponential-Growth Method:  
  1. Aggregate daily cases from day33_incidence.csv.  
  2. Fit a linear regression on log(cases) to estimate r.  
  3. Load SI parameters from generation_time.json and compute $M(-r)$.  
  4. Derive R₀.  

- Likelihood & Attack-Rate:  
  1. Run R0::estimate.R() (or custom Python MLE) to estimate R₀.  
  2. Apply the final-size equation for a closed herd.  
  3. Compute 7-day EDR and visualize the series.  

- Sensitivity Analysis:  
  Vary SI mean ±2 days and SD ±1 day; re-estimate R₀ and plot results.  

---

## Assignment (Due Day 34 Morning)

Submit to assignments/day33/:  

1. Estimation Script (.R or .py) with comments  
2. Results Table (day33R0results.csv):  
   - Growth rate (r), R₀ by method, SI parameters  
3. EDR Time-Series Plot (day33EDRplot.png)  
4. Sensitivity Plot (day33_sensitivity.png): R₀ vs. SI variations  
5. Analytical Report (day33_report.md, 400–500 words):  
   - Compare methods, interpret differences, and discuss control implications  
6. Reflection Note (day33_reflection.md, 200 words):  
   - Limitations of R₀ & EDR estimation and strategic insights  

---

Mastering these metrics will sharpen your ability to quantify transmission potential and guide data-driven response strategies in real-world outbreaks.