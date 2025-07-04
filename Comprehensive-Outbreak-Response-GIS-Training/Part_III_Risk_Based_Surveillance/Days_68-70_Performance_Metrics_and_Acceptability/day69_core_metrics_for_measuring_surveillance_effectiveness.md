# **Day 69 – Core Metrics for Measuring Surveillance Effectiveness**
  
Bloom Level: Evaluate & Analyze | Duration: 4 hrs  

## Objectives  

- Define and calculate core surveillance metrics: sensitivity, predictive value positive (PPV), timeliness, completeness, and representativeness.  
- Assess system-level and unit-level performance using quantitative and spatial analyses.  
- Visualize metric distributions over time and space to identify weak links.  
- Interpret findings to recommend targeted improvements for the surveillance system.  

---  

## Agenda  

1. **Lecture: Key Surveillance Metrics** (45 min)  
   - Definitions and formulas for sensitivity, PPV, timeliness, completeness, representativeness  
   - Uses and limitations of each metric in outbreak monitoring  

2. **Demo: Computing Metrics in Code** (30 min)  
   - Python: pandas and NumPy workflows for metric calculation  
   - R: dplyr and epiR approaches  

3. **Lab Part 1 – Quantitative Metric Calculation** (60 min)  
   - Load `day69_reporting_data.csv` and `day69_population.csv`  
   - Compute:  
     - Sensitivity = detected true cases / total true cases  
     - PVP = true positives / reported positives  
     - Timeliness = proportion of reports within target window  
     - Completeness = proportion of expected reports received  
     - Representativeness = sample distribution vs. animal population distribution  

4. **Lab Part 2 – Spatial & Temporal Visualization** (45 min)  
   - Map district-level sensitivity and completeness using `day69_districts.shp`  
   - Plot timeliness trends over weeks and highlight breach events  
   - Identify spatial clusters of low performance  

5. **Discussion & Q&A** (40 min)  
   - Interpreting conflicting metric signals (e.g., high sensitivity but low PVP)  
   - Prioritizing interventions based on metric patterns  
   - Planning follow-up evaluations  

---  

## Exercise Details  

**Data Provided:**  
- `day69_reporting_data.csv`: records with `district`, `date_reported`, `cases_reported`, `cases_confirmed`  
- `day69_population.csv`: district-level livestock counts  
- `day69_expected_reports.csv`: scheduled reporting frequency per site  
- `day69_districts.shp`: administrative boundaries  
- `day69_response_times.csv`: individual report timestamps (onset to report)  

**Key Tasks:**  
1. Merge reporting and population tables; calculate each core metric by district and week.  
2. Create a summary table of metrics with definitions and formula references.  
3. Produce:  
   - Choropleth maps for sensitivity and completeness  
   - Line chart of weekly timeliness proportions  
   - Scatterplot of PVP vs. sensitivity per district  
4. Identify three top-performing and three under-performing districts.  
5. Draft metric-driven recommendations to strengthen data quality and timeliness.  

---  

## Assignment  

Submit to `assignments/day69/` by Day 70 morning:  

1. **Metric Calculation Script**  
   - `day69_metrics.R` or `day69_metrics.py` with annotated code for all metric computations.  

2. **Metrics Summary Table**  
   - `day69_metrics_summary.csv` containing `district`, `metric_name`, `value`, `lower_CI`, `upper_CI`, and `interpretation`.  

3. **Spatial & Temporal Visualizations**  
   - `day69_sensitivity_map.png` (choropleth)  
   - `day69_completeness_map.png` (choropleth)  
   - `day69_timeliness_trend.png` (line chart)  
   - `day69_pvp_vs_sensitivity.png` (scatterplot)  

4. **Analytical Report** (`day69_report.md`, 400 words)  
   - Describe methods, key findings, metric discrepancies, and targeted improvement proposals.  

5. **Reflection** (`day69_reflection.md`, 200 words)  
   - Reflect on challenges in balancing multiple metrics, data limitations, and using findings to drive system change.  

---  

This session empowers you to rigorously measure surveillance effectiveness, map performance gaps, and translate insights into actionable system enhancements.
