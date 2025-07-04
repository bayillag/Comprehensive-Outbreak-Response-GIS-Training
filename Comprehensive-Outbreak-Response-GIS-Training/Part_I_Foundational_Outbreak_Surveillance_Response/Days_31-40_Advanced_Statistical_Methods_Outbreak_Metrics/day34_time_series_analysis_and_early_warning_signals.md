# **Day 34 – Time-Series Analysis and Early Warning Signals**
  
Bloom Level: Analyze & Apply | Duration: 4 hrs  

## Objectives  

- Describe components of surveillance time series: trend, seasonality, and residual noise.  
- Apply decomposition (classical, STL) and smoothing techniques (moving average, exponential smoothing).  
- Detect early warning signals (EWS) using control charts (EWMA, CUSUM) and change-point methods.  
- Design a prototype early warning system that flags unusual increases in case counts.  

## Agenda  

1. Lecture: Time-Series Fundamentals (45 min)  
   - Definitions: trend, seasonal cycle, irregular component  
   - Stationarity and autocorrelation concepts  
   - Overview of EWS indicators (variance, autocorrelation, skewness)  

2. Demo: Decomposition & Smoothing (30 min)  
   - R: `stats::decompose()`, `forecast::stl()`  
   - Python: `statsmodels.tsa.seasonal_decompose`, `exponential_smoothing`  
   - Moving average vs. exponential smoothing examples  

3. Group Exercise: Time-Series Analysis Workflow (45 min)  
   - Load `day34_daily_cases.csv`; convert to time-series object  
   - Perform classical and STL decomposition; extract components  
   - Apply moving average and Holt–Winters smoothing; compare residuals  

4. Interactive Demo: Early Warning Signals (60 min)  
   - Implement EWMA and CUSUM in R (`qcc` package) or Python (`numpy`, `pandas`)  
   - Detect change points using `changepoint` (R) or `ruptures` (Python)  
   - Overlay signals on time-series plots; evaluate sensitivity  

5. Discussion & Q&A (30 min)  
   - Trade-offs: false alarms vs. detection speed  
   - Integrating environmental covariates (e.g., rainfall) into warning algorithms  
   - Operationalizing EWS in low-resource settings  

---

## Exercise Details  

**Data Provided:**  
- `day34_daily_cases.csv`: daily animal case counts with `date`, `cases`.  
- `day34_rainfall.csv`: daily rainfall amounts (`date`, `rain_mm`) for the same period.  
- `scenario_brief_ts.pdf`: context on past seasonal outbreaks in the region.  

**Key Tasks:**  
1. Convert `cases` into a time-series object; produce plots of raw data.  
2. Perform classical and STL decompositions; present trend and seasonal components.  
3. Apply moving average (7-day) and exponential smoothing; compare residual distributions.  
4. Compute EWMA and CUSUM thresholds; flag points exceeding control limits.  
5. Detect change points in `cases` series; document method and parameter choices.  

---

## Assignment  

Submit to `assignments/day34/` by Day 35 morning:

1. Time-Series Analysis Script (`day34_ts_analysis.R` or `day34_ts_analysis.py`)  
2. Decomposition & Smoothing Plots (`day34_decomposition.png`, `day34_smoothing.png`)  
3. Early Warning Signals Script (`day34_ews.R` or `day34_ews.py`)  
4. EWS Dashboard Screenshot (`day34_ews_dashboard.png` or link)  
5. Analytical Report (`day34_report.md`)  
   • 400–500 words describing methods, findings, and operational recommendations.  
6. Reflection (`day34_reflection.md`)  
   • 200 words on challenges detecting early signals and balancing alarm thresholds.
