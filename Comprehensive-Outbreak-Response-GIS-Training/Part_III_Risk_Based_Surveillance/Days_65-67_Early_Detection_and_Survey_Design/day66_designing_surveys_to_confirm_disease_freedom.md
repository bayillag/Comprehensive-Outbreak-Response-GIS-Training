# **Day 66 – Designing Surveys to Confirm Disease Freedom**
  
Bloom Level: Apply & Create | Duration: 4 hrs  

## Objectives  

- Define “disease freedom” and its regulatory and surveillance implications.  

- Distinguish survey types for freedom assessment: simple random, stratified, risk-based, and cluster sampling.  

- Calculate sample sizes for herd‐ and within‐herd stages, incorporating design prevalence, test sensitivity, specificity, and confidence levels.  

- Develop a two‐stage sampling protocol: selecting herds and animals per herd.  

- Integrate spatial distribution and logistic constraints into a practical field sampling frame.  

---  

## Agenda  

1. Lecture: Principles of Freedom Surveys (45 min)  
   - Regulatory definitions and OIE guidelines  
   - Design prevalence vs. true prevalence  
   - Impact of test characteristics on survey sensitivity  

2. Demo: Sample Size Calculation Tools (30 min)  
   - R’s `epiR::epi.ssdetect()` and EpiTools workflows  
   - Python implementations for herd‐level and within‐herd calculations  
   - Building a spatial sampling frame in QGIS  

3. Lab Part 1 – Sample Size & Protocol Draft (60 min)  
   - Define target population and risk strata from `day66_herd_list.csv`  
   - Calculate number of herds needed to detect at least one positive (alpha = 0.05, P* = 1%)  
   - Compute within‐herd sample size based on herd‐level sensitivity requirements and test Se/Sp  

4. Lab Part 2 – Spatial Sampling Frame (45 min)  
   - Load `day66_herd_locations.shp` in QGIS; assign strata and select random herds per strata  
   - Generate within‐herd animal selection plan; export `day66_sampling_frame.shp`  
   - Map travel routes and cluster points for field teams  

5. Discussion & Q&A (30 min)  
   - Balancing statistical rigor and field feasibility  
   - Addressing imperfect tests and non‐response  
   - Documenting protocols for regulatory acceptance  

---  

## Exercise Details  

**Data Provided:**  
- `day66_herd_list.csv`: herd IDs, strata, population at risk  
- `day66_herd_locations.shp`: spatial points of herds  
- `day66_test_params.csv`: test sensitivity and specificity  

**Key Tasks:**  
1. Calculate herd‐level sample size formula:  
   $$ n = \frac{\ln(1 - \text{Confidence})}{\ln(1 - (\text{Design Prevalence} \times \text{Se}))} $$

Where:
*   `n` = The required sample size (the number of animals to test).
*   `ln` = The natural logarithm.
*   `Confidence` = The desired level of confidence (e.g., 95% or 0.95).
*   `Design Prevalence` (or $P^*$) = The assumed minimum prevalence of the disease you want to be able to detect.
*   `Se` = The sensitivity of the diagnostic test being used.


2. Compute within‐herd sample size using hypergeometric or binomial approximations.  

3. Stratify herds by risk or geography and allocate sample numbers proportionally.  

4. Implement random selection in QGIS or code; verify spatial coverage.  

5. Draft a field protocol with sampling steps, test methods, and data recording templates.  

---


## Assignment  

Submit to `assignments/day66/` by Day 67 morning:  

1. Survey Design Report (`day66_survey_design.md`)  
   - Rationale, target population, design prevalence, confidence level, and sampling scheme.  

2. Sample Size Script (`day66_sample_size.R` or `day66_sample_size.py`)  
   - Annotated code performing herd‐ and within‐herd calculations.  

3. Sampling Frame Shapefile (`day66_sampling_frame.shp`)  
   - Selected herds and within‐herd sampling points with strata attributes.  

4. Map of Selected Herds (`day66_selected_herds.png`)  
   - Choropleth or symbol map showing sampled herds by stratum.  

5. Survey Protocol Template (`day66_protocol.md` or `.docx`)  
   - Step-by-step SOP for field teams: herd selection, animal sampling, test procedures, data capture.  

6. Reflection (`day66_reflection.md`, 200 words)  
   - Challenges in sample size trade-offs, spatial representativeness, and implementing two‐stage designs in the field.  

---  

This session equips you to design statistically robust, logistically feasible surveys that demonstrate disease freedom with high confidence.
