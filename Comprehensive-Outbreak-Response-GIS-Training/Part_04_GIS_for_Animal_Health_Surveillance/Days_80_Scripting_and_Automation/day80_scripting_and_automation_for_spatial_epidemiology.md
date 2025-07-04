# **Day 80 – Scripting & Automation for Spatial Epidemiology**
  
Bloom Level: Apply & Create | Duration: 4 hrs  

## Objectives  

- Automate end-to-end spatial epidemiology workflows using scripts and processing models.  
- Ensure reproducibility by version controlling code and documenting dependencies.  
- Integrate geoprocessing, risk scoring, mapping, and reporting into a unified pipeline.  
- Leverage command-line scheduling (cron, Task Scheduler) or CI tools (GitHub Actions) for routine execution.  
- Build self-documenting scripts with clear modular structure and logging.  

---  

## Agenda  

1. Lecture: Automation Fundamentals (45 min)  
   - Benefits of scripted workflows vs. GUI processing  
   - Design patterns: modular functions, parameterization, logging  
   - Workflow orchestration: cron jobs, GitHub Actions, Docker  

2. Demo: Python & R Geoprocessing Scripts (30 min)  
   - GeoPandas/Fiona for vector tasks, rasterio for raster workflows  
   - R’s `sf`, `raster`, and `targets` package for pipeline management  
   - QGIS Processing Model integration  

3. Lab Part 1 – Developing Core Scripts (60 min)  
   - Load and reproject spatial layers (`day80_admin.shp`, `day80_cases.shp`)  
   - Perform spatial join and risk scoring in code  
   - Export processed outputs and maps automatically  

4. Lab Part 2 – Pipeline Orchestration & Scheduling (45 min)  
   - Wrap scripts into a master pipeline (`day80_pipeline.py` or `day80_pipeline.R`)  
   - Add command-line arguments and logging (timestamps, errors)  
   - Configure a scheduler or CI workflow to run the pipeline nightly  

5. Discussion & Q&A (30 min)  
   - Handling failures, notifications, and rollback strategies  
   - Best practices for dependency management (virtualenv, renv, conda)  
   - Documenting and sharing pipelines with stakeholders  

---  

## Exercise Details  

**Data Provided:**  

- `day80_admin.shp`: administrative boundaries  
- `day80_cases.shp`: geocoded case locations  
- `day80_population.tif`: raster of livestock density  
- `day80_risk_weights.csv`: weights for risk factors  
- `day80_report_template.Rmd` / `day80_report_template.ipynb`: report skeleton  

**Key Tasks:**  

1. Develop a script to:  
   - Reproject input layers to a common CRS.  
   - Calculate a composite risk score for each admin unit by weighting factors.  
   - Generate choropleth and KDE maps and save as PNG.  

2. Automate report generation:  
   - Integrate map outputs and summary tables into the RMarkdown or notebook.  
   - Render a PDF or HTML report via script.  

3. Build a pipeline wrapper that:  
   - Accepts configuration (paths, date range) via a YAML or JSON file.  
   - Executes processing steps in sequence, logs progress, catches errors.  

4. Schedule the pipeline:  
   - Configure a cron entry (Linux/macOS) or Task Scheduler (Windows) to run daily.  
   - Or implement a simple GitHub Actions workflow to trigger on push.  

5. Version control and documentation:  
   - Initialize a Git repository, commit code, and write a README with usage instructions.  

---  

## Assignment  

Submit to `assignments/day80/` by Day 81 morning:  

1. Automation Plan (`day80_plan.md`)  
   - Description of pipeline architecture, modules, scheduling, and logging approach.  

2. Pipeline Script(s)  
   - `day80_pipeline.py` or `day80_pipeline.R` with inline comments, modular functions, and CLI support.  

3. QGIS Model or Workflow File  
   - `day80_qgis_model.model3` (if using Processing model) or equivalent.  

4. Generated Outputs  
   - `day80_risk_map.png` (choropleth)  
   - `day80_kde_map.png` (kernel density)  
   - `day80_summary_report.pdf` or `day80_summary_report.html`  

5. Scheduler Configuration  
   - Cron entry snippet or GitHub Actions YAML file (`.github/workflows/day80_pipeline.yml`).  

6. Reflection (`day80_reflection.md`, 200 words)  
   - Discuss challenges in modularizing code, dependency management, and ensuring pipeline robustness.  

---  

By scripting and automating spatial epidemiology tasks, you’ll achieve reproducible, scalable analyses that can run unattended—empowering timely, data-driven decision making.
