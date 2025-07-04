# **Day 40 – Integrating Statistical Outputs into Reports**

Bloom Level: Create & Evaluate | Duration: 4 hrs  

## Objectives  

- Demonstrate how to embed tables, figures, and narrative from analyses into dynamic reports.  
- Automate generation of HTML, PDF, and Word outputs with parameterized scripts.  
- Apply styling and layout best practices for clarity and impact.  
- Implement version control and reproducible workflows for report artifacts.  

---  

## Agenda  

1. Lecture: Reporting Principles (45 min)  
   - Roles of narrative, tables, and visualizations in conveying findings  
   - Report formats: static vs dynamic, pros and cons  
   - Essentials of reproducibility, versioning, and traceability  

2. Demo: Dynamic Report Workflows (30 min)  
   - RMarkdown: code chunks, parameters, templates  
   - Jupyter Book or nbconvert: cell tagging, metadata, PDF conversion  

3. Lab Part 1 – Embedding Outputs (60 min)  
   - Use `day40_analysis.R`/`.py` to produce key tables and plots  
   - Integrate outputs into `report_template.Rmd` or `report_template.ipynb`  
   - Customize styling: titles, captions, CSS or YAML options  

4. Lab Part 2 – Parameterization & Automation (45 min)  
   - Introduce parameters for date ranges, regions, and species filters  
   - Write a wrapper script (`generate_report.R`/`.py`) to render multi-format outputs  
   - Set up Git hooks or Makefile for automatic rendering on commit  

5. Discussion & Q&A (30 min)  
   - Handling large outputs and caching strategies  
   - Collaborating on reports: branching, pull requests, and review workflows  

---  

## Exercise Details  

**Data Provided:**  
- `day40_analysis.R` or `day40_analysis.py`: scripts generating `tables.csv` and `plots.png`  
- `report_template.Rmd` or `report_template.ipynb`: skeleton with placeholders  
- CSS file (`report_style.css`) and YAML config (`params.yaml`)  

**Key Tasks:**  
1. Run analysis scripts to produce summary tables and figures.  
2. Insert table outputs as formatted Markdown/HTML tables and embed plots with captions.  
3. Parameterize the template to accept `start_date`, `end_date`, and `zone` filters.  
4. Automate report rendering to HTML, PDF, and Word using your wrapper script.  

---  

## Assignment  

Submit to `assignments/day40/` by Day 41 morning:  

1. Completed Report Template (`day40_report.Rmd` or `day40_report.ipynb`)  
2. Analysis Scripts (`day40_analysis.R` or `day40_analysis.py`; `day40_generate.R` or `day40_generate.py`)  
3. Sample Outputs (`day40_report.html`, `day40_report.pdf`, `day40_report.docx`)  
4. Workflow Configuration (`day40_workflow.md`)  
   - Description of commands or hooks used for automation  
5. Reflection (`day40_reflection.md`)  
   - 200 words on challenges in integrating analysis into reports and strategies for maintainable workflows  
---