# **Day 72 – Implementing the Risk-Based Surveillance Framework**
  
Bloom Level: Apply & Create | Duration: 4 hrs  

## Objectives  

- Operationalize the end-to-end risk-based surveillance pipeline from stratification to field deployment.  

- Integrate risk scoring outputs with sampling plan generation and data-collection workflows.  

- Develop real-time monitoring dashboards and maps to track surveillance activity and coverage.  

- Establish adaptive feedback loops to update risk strata and reprioritize sampling dynamically.  

- Coordinate stakeholders and field teams on data flows, reporting protocols, and performance targets.  

---  

## Agenda  

1. Lecture: From Theory to Practice (45 min)  
   - Review risk-based surveillance stages: scoring, stratification, sampling, feedback  
   - Data architecture and workflow orchestration  

2. Demo: Automated Pipeline Walkthrough (30 min)  
   - Ingest risk scores → generate sampling frame → export field schedules  
   - Real-time ingestion of field reports and risk re-calculation  

3. Lab Part 1 – Pipeline Development (60 min)  
   - Load `day72_risk_scores.csv` and classify admin units into high/medium/low strata  
   - Write code to auto-generate site visit schedules and data-collection forms  

4. Lab Part 2 – Dashboard & Map Integration (45 min)  
   - Use the template (`day72_dashboard_template.Rmd` or `.py`) to build live plots of strata and activity logs  
   - Create a map of planned vs. completed visits, with coverage heatmap  

5. Discussion & Q&A (30 min)  
   - Handling field-data delays, missing reports, and recalibration triggers  
   - Stakeholder coordination: roles, communication channels, and SOPs  

---  

## Exercise Details  

**Data Provided:**  
- `day72_risk_scores.csv`: admin codes, composite risk scores, previous sampling dates  
- `day72_sample_plan_template.docx`: placeholder for visit schedules and site lists  
- `day72_data_schema.json`: field data JSON schema for animal sampling records  
- `day72_field_data.csv`: simulated incoming field reports (timestamps, results)  
- `day72_dashboard_template.Rmd` / `day72_dashboard_template.py`: starter code for monitoring dashboard  

**Key Tasks:**  
1. Normalize and classify risk scores into strata; document thresholds used.  
2. Auto-populate the sample-plan template with site IDs, dates, and sampling targets per strata.  
3. Build a script to ingest `day72_field_data.csv`, validate against `day72_data_schema.json`, and update coverage metrics.  
4. Design a dashboard showing:  
   - Current risk map and strata  
   - Number of sites planned vs. completed by strata  
   - Alerts for low coverage or overdue visits  
5. Generate a map of planned visits (dashed markers) vs. completed visits (solid markers) colored by strata.  

---  

## Assignment  

Submit to `assignments/day72/` by Day 73 morning:  

1. **Implementation Plan** (`day72_implementation_plan.md`)  
   - Describe data flows, pipeline components, scheduling logic, and feedback loops.  

2. **Surveillance Pipeline Script** (`day72_pipeline.py` or `day72_pipeline.R`)  
   - Annotated code for risk classification, plan generation, data ingestion, and updates.  

3. **Dashboard Prototype** (`day72_dashboard.html` or Jupyter Notebook)  
   - Interactive dashboard showing strata map, activity metrics, and alert logic.  

4. **Surveillance Activity Map** (`day72_activity_map.png`)  
   - Map overlay of planned vs. completed site visits by risk stratum.  

5. **Performance Monitoring Table** (`day72_monitoring.csv`)  
   - Weekly summary of sites planned, visits completed, coverage %, and outstanding flags.  

6. **Reflection** (`day72_reflection.md`, 200 words)  
   - Discuss challenges in automating workflows, ensuring data quality, and maintaining dynamic risk updates.  

---  

This session cements your ability to transform risk-based surveillance theory into a scalable, data-driven operational framework.