# **Day 37 – Sensitivity, Specificity, and Predictive Values**

Bloom Level: Analyze & Apply | Duration: 4 hrs  

## Objectives  

- Define sensitivity, specificity, positive predictive value (PPV), and negative predictive value (NPV).  
- Calculate these metrics from diagnostic test results in animal health contexts.  
- Explore how disease prevalence affects PPV and NPV.  
- Interpret test performance for surveillance and clinical decision-making.  

## Agenda  

1. Lecture: Test Performance Metrics (45 min)  
   - Definitions and formulae:  
     | Metric            | Formula                                          | Interpretation                                 |
     |-------------------|--------------------------------------------------|-----------------------------------------------|
     | Sensitivity (Se)  | Se = a / (a + c)                                 | True positive rate                            |
     | Specificity (Sp)  | Sp = d / (b + d)                                 | True negative rate                            |
     | Positive Predictive Value (PPV) | PPV = a / (a + b)                   | Probability disease when test positive        |
     | Negative Predictive Value (NPV) | NPV = d / (c + d)                   | Probability no disease when test negative     |

2. Case Study: Avian Influenza Rapid Test Evaluation (30 min)  
   - Review field data: test results vs. gold standard PCR  
   - Discuss trade-offs in surveillance (speed vs. accuracy)  

3. Group Exercise: Hand Calculations (45 min)  
   - Teams receive a 2×2 table of test vs. status  
   - Compute Se, Sp, PPV, NPV by hand  
   - Recalculate PPV/NPV under three hypothetical prevalence scenarios  

4. Interactive Demo: Implementing Metrics in R/Python (60 min)  
   - R: `caret::confusionMatrix()` and custom functions  
   - Python: `sklearn.metrics` for sensitivity, specificity, PPV, NPV  
   - Simulate prevalence changes and plot PPV/NPV curves  

5. Discussion & Q&A (30 min)  
   - Choosing tests for screening vs. confirmation  
   - Impacts of low prevalence on PPV and false alarms  
   - Reporting and communicating test limitations  

---

## Exercise Details  

**Data Provided:**  
- `day37_test_results.csv`: sample IDs with `true_status` (1=diseased, 0=healthy) and `test_result` (1=positive, 0=negative)  
- Prevalence scenarios: `day37_prevalence.yaml` with population sizes and case counts  

**Key Tasks:**  
1. Generate a confusion matrix for the provided data.  
2. Calculate sensitivity, specificity, PPV, and NPV.  
3. Adjust prevalence in simulations (e.g., 1%, 5%, 20%) and recompute PPV/NPV.  
4. Plot PPV and NPV as functions of prevalence.  

---

## Assignment  

Submit to `assignments/day37/` by Day 38 morning:

1. Confusion Matrix Table (`day37_confusion_matrix.md`)  
   - 2×2 table with labeled cells a, b, c, d.  

2. Calculation Script (`day37_metrics.R` or `day37_metrics.py`)  
   - Annotated code computing Se, Sp, PPV, NPV, and prevalence simulations.  

3. Results Table (`day37_metrics_results.csv`)  
   - Computed metrics for observed data and each prevalence scenario.  

4. Plot Outputs (`day37_ppv_npv_curve.png`)  
   - Graphs showing PPV and NPV vs. prevalence.  

5. Analytical Report (`day37_report.md`) (400–500 words)  
   - Interpret test performance, prevalence effects, and recommendations for use.  

6. Reflection (`day37_reflection.md`) (200 words)  
   - Discuss challenges in evaluating diagnostic tests and considerations for field deployment.