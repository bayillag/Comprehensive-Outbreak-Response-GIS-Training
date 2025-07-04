# Day **8 – Ensuring Data Quality and Completeness**
  
Bloom Level: Analyze | Duration: 4 hrs  

## Objectives  

- Evaluate data completeness, consistency, and accuracy in animal disease line lists.  
- Apply validation rules and automated checks to detect errors, outliers, and anomalies.  
- Implement strategies for handling missing or implausible values (imputation, follow-up, flagging).  
- Design dashboards or reports to monitor data quality over time.  

## Agenda  

1. Lecture: Dimensions of Data Quality (45 min)  
   - Completeness, validity, consistency, timeliness, and uniqueness  
   - Common sources of error in field and lab data  

2. Case Study: Incomplete Foot-and-Mouth Disease Records (30 min)  
   - Assess the impact of missing dates and mis-entered coordinates  
   - Discuss corrective actions taken in a real outbreak  

3. Group Exercise: Designing Audit Checks (45 min)  
   - Teams define a suite of validation rules (e.g., date bounds, species codes, geo-bounds)  
   - Create a data-quality checklist for routine field reporting  

4. Interactive Demo: Automated QA in R/Python (60 min)  
   - Use pandas profiling or an R data-validation package to generate a quality report  
   - Apply SQL constraints in PostgreSQL/PostGIS to enforce referential integrity  

5. Discussion & Q&A (30 min)  
   - Balancing rapid data collection with rigorous quality checks  
   - Building feedback loops to train field teams on data entry best practices  

---

## Exercise Details  

**Data Provided:**  
- `day08_raw_linelist.csv` with deliberate missing fields, typos, and outlier coordinates  
- Validation rule template (`qa_checks.xlsx`)  

**Key Tasks:**  
1. Run automated profiling to identify completeness gaps and invalid entries.  
2. Implement a script to apply your validation rules and produce a summary report.  
3. Propose imputation or follow-up protocols for unresolved missing data.  

---

## Assignment  

Submit to `assignments/day08/` by Day 9 morning:

1. **Cleaned Line List** (`day08_cleaned.csv`)  
   - Original dataset corrected, imputed where appropriate, and flagged otherwise.  

2. **Data Quality Report** (`day08_qa_report.md`)  
   - Summary of checks performed, anomalies detected, and resolution methods.  

3. **QA Script** (`day08_qa_script.py` or `day08_qa_script.R`)  
   - Reproducible code implementing validation rules and generating the report.  

4. **Reflection** (`day08_reflection.md`)  
   - 200 words on the trade-offs between speed and data integrity in outbreak settings and lessons learned.