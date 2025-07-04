# **Day 9 – Managing Line Lists in Excel, R, and Python**

Bloom Level: Apply | Duration: 4 hrs  

## Objectives  

- Describe workflows for importing and structuring line list data in Excel, R, and Python  
- Utilize Excel features (filters, pivot tables, data validation) to explore and summarize case records  
- Apply R packages (`readr`, `dplyr`, `tidyr`) and Python’s `pandas` for cleaning, transforming, and aggregating line lists  
- Automate routine tasks and ensure reproducibility through scripts and templates  

## Agenda  

1. Lecture: Comparative Toolchains for Data Management (45 min)  
   - Strengths and limitations of Excel vs. scripted approaches  
   - When to pivot from manual to automated workflows  

2. Demo: Excel Techniques for Line Lists (30 min)  
   - Importing CSVs, applying filters, sorting, and custom views  
   - Building pivot tables to summarize cases by species, location, and status  

3. Lab Part 1 – R Scripting with the Tidyverse (60 min)  
   - Read and inspect the line list with `readr::read_csv()`  
   - Use `dplyr` verbs to filter, mutate new fields, and group summaries  
   - Reshape data with `tidyr` and export cleaned outputs  

4. Lab Part 2 – Python Pandas Workflow (45 min)  
   - Load the dataset with `pandas.read_csv()`  
   - Clean and transform columns (`dropna`, `astype`, `apply`)  
   - Aggregate counts by key variables and save results to Excel/CSV  

5. Discussion & Q&A (30 min)  
   - Best practices for versioning Excel workbooks  
   - Ensuring script portability and documenting code  

## Exercise Details  

**Data Provided:**  
- `day09_raw_linelist.csv` containing duplicate entries, missing values, and inconsistent codes  
- Starter Excel workbook (`day09_template.xlsx`) with basic headers and validation lists  

**Key Tasks:**  
1. In Excel, clean and validate the raw data: remove duplicates, fix codes, and create a pivot summary.  
2. Write an R script (`day09_clean.R`) that replicates your Excel cleaning steps and exports a tidy CSV.  
3. Develop a Python script (`day09_clean.py`) using `pandas` to perform the same cleaning and produce an Excel summary sheet.  

## Assignment  

Submit to `assignments/day09/` by Day 10 morning:

1. Cleaned Excel Workbook (`day09_cleaned.xlsx`)  
2. R Script (`day09_clean.R`) with comments explaining each step  
3. Python Script (`day09_clean.py`) with clear function definitions  
4. Reflection (`day09_reflection.md`) (200 words on your choice of tool for different tasks and lessons learned)