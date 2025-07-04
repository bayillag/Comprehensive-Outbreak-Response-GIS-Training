# **Day 23 – Constructing Epidemic Curves and Histograms**
  
Bloom Level: Analyze & Apply | Duration: 4 hrs  

## Objectives  

- Understand the role and interpretation of epidemic curves in outbreak analysis.  
- Create epidemic curves by onset date using R (`ggplot2`) and Python (`matplotlib`/`seaborn`).  
- Build histograms of case attributes (e.g., age, incubation period) and assess distribution shapes.  
- Stratify curves and histograms by species, zone, or other key variables to reveal patterns.  

## Agenda  

1. Lecture: Principles of Epidemic Curves & Histograms (45 min)  
   - Curve anatomy: time axis, case counts, peak interpretation  
   - Histogram basics: bin width, skewness, modality  

2. Demo: R vs. Python Visualization (30 min)  
   - R: `geom_bar()`, `geom_histogram()` in `ggplot2`  
   - Python: `plt.hist()`, `sns.countplot()` with styling  

3. Lab Part 1 – Epidemic Curve Construction (60 min)  
   - Load `day23_linelist.csv`; aggregate cases by onset date  
   - Plot overall curve, then stratify by species and zone  

4. Lab Part 2 – Histogram Generation (45 min)  
   - Select variables (age, incubation_days)  
   - Generate histograms, test different bin widths, overlay density curves  

5. Discussion & Q&A (30 min)  
   - Inferring transmission dynamics from curve shapes  
   - Addressing data quality issues: missing dates, rounding  

---

## Exercise Details  

**Data Provided:**  
- `day23_linelist.csv`: fields include `case_id`, `species`, `onset_date`, `age`, `incubation_days`, `zone`  
- `day23_population.csv`: optional denominators for rate-adjusted curves  

**Key Tasks:**  
1. Produce a daily epidemic curve of all cases.  
2. Create stratified epidemic curves by species and by zone.  
3. Build histograms for `age` and `incubation_days`, experimenting with bin widths.  

---

## Assignment  

Submit to `assignments/day23/` by Day 24 morning:  

1. Epidemic Curve Script (`day23_epi_curve.R` or `day23_epi_curve.py`)  
2. Histogram Script (`day23_histograms.R` or `day23_histograms.py`)  
3. Plot Outputs (`day23_epi_curve.png`, `day23_histograms.png`)  
4. Visualization Report (`day23_report.md`)  
   - 300–400 words interpreting curve features, distribution patterns, and analytic implications.  
5. Reflection (`day23_reflection.md`)  
   - 200 words on insights gained from visualizing data and best practices for communicative graphs.