# **Day 17 – Automating Routine Reports**  
Bloom Level: Apply | Duration: 4 hrs  

## Objectives  

- Develop scripts to automate extraction, analysis, and visualization of outbreak data.  
- Parameterize reports for date ranges, geographic areas, and species groups.  
- Generate dynamic documents (HTML, PDF, Word) using RMarkdown or Jupyter notebooks.  
- Implement scheduling and notifications via cron jobs or GitHub Actions.  

---  

## Agenda  

1. Lecture: Principles of Report Automation (45 min)  
   - Benefits of reproducibility, consistency, and timeliness  
   - Overview of tools: RMarkdown, Jupyter nbconvert, Papermill, nbformat  

2. Demo: Parameterized Reporting with RMarkdown (30 min)  
   - YAML front matter for inputs (dates, filters)  
   - Embedding code chunks, tables, and plots  

3. Lab Part 1 – Scripted Report Generation (60 min)  
   - Adapt `day17_linelist.csv` and `day17_lab_results.csv` to build a weekly summary  
   - Create an R or Python script that:  
     * Reads data based on input parameters  
     * Produces key metrics (case counts, positivity rates)  
     * Renders a complete report  

4. Lab Part 2 – Scheduling & Notifications (45 min)  
   - Configure a cron job or GitHub Actions workflow to run the report weekly  
   - Set up email notifications with attachment links  

5. Discussion & Q&A (30 min)  
   - Handling errors, logging, and alerting on failures  
   - Maintenance strategies and collaborative workflows  

---  

## Exercise Details  

**Data Provided:**  
- `day17_linelist.csv` and `day17_lab_results.csv`  
- Shapefile for administrative zones (`zones_shapefile.zip`)  
- Report template (`report_template.Rmd` or `report_template.ipynb`)  

**Key Tasks:**  
1. Parameterize the template to accept start/end dates and zone filters.  
2. Write a wrapper script (`generate_report.R` or `generate_report.py`) that:  
   - Reads inputs from a YAML or JSON config  
   - Calls the template renderer to output HTML and PDF  
3. Create a scheduler config:  
   - Cron entry example or GitHub Actions YAML file  
   - Email step using `mailx`, SendGrid, or GitHub Actions email action  

---  

## Assignment  

Submit to `assignments/day17/` by Day 18 morning:

1. **Automation Script** (`day17_generate_report.R` or `day17_generate_report.py`)  
   - Reads config, renders reports, and handles errors gracefully.  

2. **Report Template** (`day17_report_template.Rmd` or `day17_report_template.ipynb`)  
   - Document with placeholders for parameters and example output sections.  

3. **Scheduler Configuration** (`day17_scheduler.md`)  
   - Cron syntax or GitHub Actions YAML with steps for running and emailing reports.  

4. **Sample Output**  
   - PDF or HTML report for a specified week (`day17_sample_report.pdf`).  

5. **Reflection** (`day17_reflection.md`)  
   - 200 words on the value of automation in outbreak response, challenges faced, and next steps for scaling.