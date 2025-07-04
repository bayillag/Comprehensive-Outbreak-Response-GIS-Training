# **Day 20 – Evaluating System Performance Metrics**  
Bloom Level: Analyze | Duration: 4 hrs  

## Objectives  

- Define key surveillance performance metrics: sensitivity, specificity, positive predictive value, timeliness, completeness, and representativeness.  
- Calculate these metrics using sample outbreak and reporting datasets.  
- Interpret metric results to identify system strengths, weaknesses, and bias.  
- Recommend targeted improvements to surveillance design and field operations based on metric findings.  

## Agenda  

1. Lecture: Surveillance Performance Framework (45 min)  
   - Metric definitions and formulas (e.g., sensitivity = true positives ÷ [true positives + false negatives]).  
   - System attributes: timeliness (lag from onset to report), completeness (proportion of expected reports received), representativeness (coverage across strata).  

2. Case Study: Foot-and-Mouth Disease Surveillance Audit (30 min)  
   - Review a published evaluation of FMD reporting in mixed‐herd settings.  
   - Discuss how metric findings drove changes in sampling cadence and training.  

3. Group Exercise: Metric Calculation (45 min)  
   - Teams receive a simulated dataset with true case status, reported cases, dates, and locations.  
   - Compute sensitivity, specificity, PPV, timeliness, and completeness by zone.  

4. Interactive Demo: Automated Metric Dashboards (60 min)  
   - Use R (`epiR`) or Python (`epi_metrics` or custom code) to calculate metrics.  
   - Build a simple dashboard (Shiny or Plotly) showing metric trends over time and by region.  

5. Discussion & Q&A (30 min)  
   - Interpreting trade-offs between sensitivity and specificity in resource-limited contexts.  
   - Strategies for improving lag times and completeness without overburdening field teams.  

## Exercise Details  

**Data Provided:**  
- `day20_truth.csv`: “Gold standard” case list with true positive/negative labels.  
- `day20_reports.csv`: Reported cases with timestamps and location codes.  
- `zones_lookup.csv`: Reference table of administrative zones and population at risk.  

**Key Tasks:**  
1. Merge truth and reporting data; flag true positives, false negatives/positives, and true negatives.  
2. Calculate sensitivity, specificity, PPV, timeliness (median reporting delay), and completeness (reports received ÷ expected).  
3. Create summary tables and time-series plots of each metric by zone.  

## Assignment  

Submit to `assignments/day20/` by Day 21 morning:

1. **Performance Report** (`day20_report.md`)  
   - 400–500 words summarizing metric definitions, results by zone, interpretations, and recommendations.  

2. **Metric Calculations Script** (`day20_metrics.R` or `day20_metrics.py`)  
   - Script with comments showing data merging, metric computations, and summary table exports.  

3. **Dashboard Screenshots** (`day20_dashboard.png`)  
   - Two images: a time-series of sensitivity/completeness and a zonal comparison chart.  

4. **Reflection** (`day20_reflection.md`)  
   - 200 words on challenges in metric interpretation and how findings would inform redesign of surveillance workflows.