# **Day 15 – Data Cleaning and Error‐Checking Methods**

Bloom Level: Apply | Duration: 4 hrs  

## Objectives  

- Evaluate common data quality issues in animal outbreak line lists and lab datasets.  

- Apply cleaning techniques to handle duplicates, missing values, inconsistent codes, and outliers.  

- Implement automated error–checking workflows in Excel, R, and Python for reproducible cleaning.  

- Document and standardize data‐cleaning protocols for team adoption and version control.  

## Agenda  

1. Lecture: Data Cleaning Best Practices (45 min)  
2. Demo: Excel-Based Error Checking and Validation (30 min)  
3. Lab Part 1 – R Scripting for Data Cleaning (60 min)  
4. Lab Part 2 – Python Pandas Workflows for Error Detection (45 min)  
5. Discussion & Q&A (30 min)  

## Common Data Issues & Approaches  

| Issue              | Detection Method                         | Correction Strategy              |
|--------------------|------------------------------------------|----------------------------------|
| Duplicate records  | Count by unique ID or entire row matching| Remove or merge with priority    |
| Missing values     | Null/NA checks on key fields             | Impute, follow up, or flag       |
| Inconsistent codes | Unique value enumeration                 | Map to standardized lookup table |
| Outlier values     | Statistical (IQR/Z-score) or visual scan | Verify source or correct entry   |

## Exercise Details  

**Data Provided:**  
- `day15_raw_linelist.csv` (with duplicate IDs, blank fields, mixed code sets)  
- `day15_lab_results.csv` (with date mismatches and value outliers)  
- Starter scripts: `clean_template.R`, `clean_template.py`  

**Key Tasks:**  
1. Profile both datasets to identify and quantify quality issues.  
2. In Excel, apply data validation rules and use filters/pivot tables to flag anomalies.  
3. Complete the R script to automate duplicate removal, missing‐value imputation, and code standardization.  
4. Develop the Python script to replicate R cleaning steps and generate a summary report of corrections.  

## Assignment  

Submit to `assignments/day15/` by Day 16 morning:  

- Cleaned Line List (`day15_cleaned_linelist.csv`)  
- Cleaned Lab Dataset (`day15_cleaned_lab.csv`)  
- R Cleaning Script (`day15_clean.R`) with comments explaining each step  
- Python Cleaning Script (`day15_clean.py`) organized into functions  
- Data Cleaning Protocol (`day15_protocol.md`) outlining your workflow, rules, and rationale  
- Reflection (`day15_reflection.md`) (200 words on trade-offs between automation and manual review, and lessons learned)