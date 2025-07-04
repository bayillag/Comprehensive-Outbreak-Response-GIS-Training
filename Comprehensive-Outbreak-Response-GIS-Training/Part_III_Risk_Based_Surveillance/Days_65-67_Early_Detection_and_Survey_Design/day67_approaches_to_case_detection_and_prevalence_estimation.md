# **Day 67 – Approaches to Case Detection and Prevalence Estimation**
  
Bloom Level: Apply & Analyze | Duration: 4 hrs  

## Objectives  

- Differentiate case detection methods (passive, active, sentinel, participatory) and their biases.  
- Define and apply standard case definitions for prevalence estimation.  
- Design surveys to estimate animal‐level and herd‐level prevalence, accounting for clustering.  
- Calculate point estimates, confidence intervals, and design effects.  
- Interpret prevalence metrics for surveillance planning and resource allocation.  

---  

## Agenda  

1. Lecture: Case Detection Modalities (45 min)  
   - Passive vs. active vs. sentinel vs. participatory detection  
   - Implications for sensitivity, timeliness, and representativeness  

2. Lecture: Prevalence Concepts (30 min)  
   - Animal‐level vs. herd‐level prevalence definitions  
   - Point estimates, exact and approximate confidence intervals  
   - Impact of cluster sampling and design effect  

3. Demo: Computing Prevalence & CIs (30 min)  
   - R: `epiR::epi.prev()` and `survey` package for clustered data  
   - Python: `statsmodels` for binomial CIs and design effect adjustments  

4. Lab Part 1 – Data Preparation & Case Counts (45 min)  
   - Load `day67_cases.csv` (herd_id, tested, positives) and `day67_cluster_info.csv` (cluster_id)  
   - Merge cluster metadata and calculate crude prevalence per herd and cluster  

5. Lab Part 2 – Estimation & Mapping (45 min)  
   - Compute animal‐level prevalence and 95% CIs using Wilson’s method  
   - Estimate herd‐level prevalence with cluster‐adjusted standard errors  
   - Map district‐level prevalence choropleth in QGIS or Python  

6. Discussion & Q&A (25 min)  
   - Comparing methods: exact vs. approximate CIs  
   - Addressing sparse data and zero‐positive clusters  
   - Using prevalence results to guide surveillance intensification  

---  

## Exercise Details  

**Data Provided:**  
- `day67_cases.csv`: columns `herd_id`, `cluster_id`, `animals_tested`, `positive_cases`  
- `day67_cluster_info.csv`: `cluster_id`, `district`, `cluster_size`  
- `day67_population.xlsx`: livestock counts by district for weighting  

**Key Tasks:**  
1. Merge case and cluster files; calculate crude prevalence = positive_cases / animals_tested.  
2. Compute 95% confidence intervals for each herd using Wilson’s score method.  
3. Aggregate to cluster and district levels; calculate design effect and adjusted CIs.  
4. Produce a prevalence table with columns: `level`, `units`, `estimate`, `lower_CI`, `upper_CI`, `design_effect`.  
5. Create a choropleth map of district‐level prevalence with CI shading.  

---  

## Assignment  

Submit to `assignments/day67/` by Day 68 morning:  

1. Prevalence Analysis Script  
   - `day67_prevalence.R` or `day67_prevalence.py` with annotated code for data merging, prevalence and CI calculations, and design effect computation.  

2. Prevalence Results Table  
   - `day67_prevalence_results.csv` containing herd‐, cluster‐, and district‐level estimates with confidence bounds.  

3. Prevalence Map  
   - `day67_prevalence_map.png` (choropleth of district‐level prevalence and CI categories).  

4. Survey Design Evaluation  
   - `day67_survey_evaluation.md` (300 words) assessing how detection methods and sampling design influenced prevalence estimates and recommending improvements.  

5. Reflection  
   - `day67_reflection.md` (200 words) on challenges in handling clustered data, interpreting design effects, and applying results to surveillance strategy.  

---  

This session will equip you to rigorously estimate disease prevalence across multiple levels, understand the impact of detection and sampling biases, and translate findings into actionable surveillance plans.
