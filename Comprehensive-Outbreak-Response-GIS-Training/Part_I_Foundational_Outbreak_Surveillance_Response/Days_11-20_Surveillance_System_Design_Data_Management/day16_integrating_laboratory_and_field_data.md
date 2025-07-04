# **Day 16 – Integrating Laboratory and Field Data**
  
Bloom Level: Apply | Duration: 4 hrs  

## Objectives  

- Understand how field case records and laboratory results relate via identifiers and spatial attributes.  

- Design a unified data schema that links cases, samples, and test outcomes.  

- Use scripting or database joins to merge datasets, resolve mismatches, and validate referential integrity.  

- Generate summary metrics (e.g., test positivity rates) and visualizations that draw on the integrated dataset.  

---  

## Agenda  

1. Lecture: Principles of Data Integration (45 min)  
   - One-to-many relationships (cases to samples)  
   - Key fields: case IDs, sample IDs, farm/premises identifiers, dates  

2. Demo: Merging in R and Python (30 min)  
   - R’s `dplyr::left_join()` and `merge()` strategies  
   - Python’s `pandas.merge()` with indicator flags for mismatches  

3. Group Exercise: Schema Mapping (45 min)  
   - Teams review field and lab CSV schemas  
   - Define join keys, identify potential mismatches, and propose handling rules  

4. Interactive Demo: Scripted Integration (60 min)  
   - Load `day16_field_cases.csv` and `day16_lab_results.csv`  
   - Perform joins, flag orphan records, and compute case-level positivity  
   - Export an integrated dataset and a discrepancy report  

5. Discussion & Q&A (30 min)  
   - Approaches to reconcile date and location inconsistencies  
   - Best practices for documenting integration logic and versioning datasets  

---  

## Exercise Details  

**Data Provided:**  
- `day16_field_cases.csv`: Case records with `case_id`, `farm_id`, `species`, `onset_date`  
- `day16_lab_results.csv`: Lab records with `sample_id`, `case_id`, `test_type`, `result`, `test_date`  
- `day16_farm_lookup.csv`: Farm metadata with `farm_id`, `latitude`, `longitude`  

**Key Tasks:**  
1. Profile each file to detect missing or inconsistent join keys.  
2. Merge records to create a case-sample master table, handling cases without lab results and vice versa.  
3. Validate that all lab records link to a valid case and flag orphans.  
4. Compute summary metrics: test positivity by species and by zone.  

---  

## Assignment  

Submit to `assignments/day16/` by Day 17 morning:  

1. Integrated Dataset (`day16_integrated_data.csv`)  
   - Master table combining field cases, lab results, and farm locations.  

2. Integration Script (`day16_integration.R` or `day16_integration.py`)  
   - Annotated code performing merges, validations, and metric calculations.  

3. Discrepancy Report (`day16_integration_report.md`)  
   - Summary of mismatches found, resolution strategies applied, and counts of orphans.  

4. Reflection (`day16_reflection.md`)  
   - 200 words on challenges in linking laboratory and field data and lessons for robust integration.