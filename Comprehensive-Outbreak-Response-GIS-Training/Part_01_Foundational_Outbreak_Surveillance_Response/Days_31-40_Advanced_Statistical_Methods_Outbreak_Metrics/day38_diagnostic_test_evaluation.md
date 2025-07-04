# **Day 38 – Diagnostic Test Evaluation**

Bloom Level: Analyze & Apply | Duration: 4 hrs  

## Objectives  

- Define and calculate advanced diagnostic metrics: accuracy, likelihood ratios, and diagnostic odds ratio.  
- Generate and interpret ROC and precision–recall curves and compute AUC.  
- Determine assay limit of detection (LOD) and limit of quantification (LOQ).  
- Assess intra- and inter-assay reproducibility via coefficient of variation (CV).  

## Agenda  

1. Lecture: Advanced Diagnostic Metrics (45 min)  
   - Accuracy, positive/negative likelihood ratios, diagnostic odds ratio  
   - Interpreting ROC vs. precision–recall curves  
   - Concepts of LOD and LOQ in quantitative assays  
   - Reproducibility: within-run (intra-assay) and between-run (inter-assay) CV  

2. Demo: ROC and AUC Computation (30 min)  
   - R: `pROC::roc()`, `caret::confusionMatrix()` for optimal thresholds  
   - Python: `sklearn.metrics.roc_curve()`, `auc()`, `precision_recall_curve()`  

3. Lab Part 1 – Curve Analysis (60 min)  
   - Load `day38_testdata.csv` with continuous test scores and true status  
   - Plot ROC and precision–recall curves; compute AUC and optimal cut‐point by Youden’s index  
   - Tabulate threshold, sensitivity, specificity, and likelihood ratios  

4. Lab Part 2 – Assay Performance & Reproducibility (45 min)  
   - Load `day38_assay.csv` with repeated measurements at low, mid, high concentrations  
   - Estimate LOD/LOQ via standard deviation of blank and low‐conc replicates  
   - Calculate intra- and inter-assay CV for each concentration level  

5. Discussion & Q&A (30 min)  
   - Trade-offs in threshold selection: maximizing sensitivity vs. specificity  
   - Implications of assay precision on field deployment  
   - Reporting standards for diagnostic evaluations (e.g., STARD guidelines)  

## Exercise Details  

**Data Provided:**  
- `day38_testdata.csv`: continuous test values and binary true_status  
- `day38_assay.csv`: replicate measurements (`run_id`, `sample_concentration`, `measurement`)  
- Template: `day38_ROC_template.R` / `day38_ROC_template.py`  

**Key Tasks:**  
1. Compute ROC and precision–recall curves; extract AUC and best threshold.  
2. Generate a metrics table at chosen cut‐point (sensitivity, specificity, LR+, LR–).  
3. Determine LOD (mean_blank + 3×SD_blank) and LOQ (mean_blank + 10×SD_blank).  
4. Calculate intra-assay CV (within each run) and inter-assay CV (across runs).  

## Assignment  

Submit to `assignments/day38/` by Day 39 morning:

1. Analysis Scripts (`day38_ROC.R` or `day38_ROC.py`; `day38_assay_perf.R` or `day38_assay_perf.py`)  
2. ROC & PRC Plots (`day38_ROC_curve.png`, `day38_PR_curve.png`)  
3. Metrics Table (`day38_threshold_metrics.csv`)  
4. Assay Performance Table (`day38_LOD_LOQ_CV.csv`)  
5. Analytical Report (`day38_report.md`) (400–500 words on diagnostic performance, threshold choice, and reproducibility)  
6. Reflection (`day38_reflection.md`) (200 words on challenges in diagnostic evaluation and lessons for field testing)
