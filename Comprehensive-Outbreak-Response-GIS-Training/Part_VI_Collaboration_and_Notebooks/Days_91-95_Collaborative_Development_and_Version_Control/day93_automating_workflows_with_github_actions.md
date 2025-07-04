# **Day 93 – Automating Workflows with GitHub Actions**
  
Bloom Level: Apply & Create | Duration: 4 hrs  

---

## Objectives  

- Understand GitHub Actions fundamentals: workflows, jobs, steps, and runners.  

- Write YAML-based CI/CD pipelines to automate testing, linting, and reporting.  

- Integrate spatial analysis scripts into automated workflows.  

- Configure triggers (push, pull_request, scheduled) for end-to-end pipeline execution.  

- Monitor, debug, and maintain Actions workflows through logs and notifications.  

---

## Agenda  

1. Lecture: GitHub Actions Concepts (45 min)  
   - Workflow structure: `.github/workflows/*.yml`  
   - Runners, jobs, steps, actions marketplace  
   - Common triggers and concurrency controls  

2. Demo: Building a Simple Workflow (30 min)  
   - Creating a workflow to lint and test Python spatial scripts  
   - Using pre-built actions for setup (`actions/checkout`, `actions/setup-python`)  
   - Reading logs and fixing failing steps  

3. Lab Part 1 – Writing Custom Workflows (60 min)  
   - Scaffold `ci.yml` to:  
     - Checkout code  
     - Install dependencies via `requirements.txt` or `renv.lock`  
     - Run geoprocessing tests (`pytest`, `R CMD check`)  
     - Build maps or reports (`python day80_pipeline.py` or `Rscript day84_risk_assessment.R`)  

4. Lab Part 2 – Advanced Configurations (45 min)  
   - Add matrix builds (multiple Python/R versions)  
   - Implement scheduled runs (cron) for nightly reports  
   - Use secrets for API keys (e.g., Google Earth Engine authentication)  
   - Configure email or Slack notifications on failure  

5. Discussion & Q&A (30 min)  
   - Best practices for caching dependencies and artifacts  
   - Debugging common YAML syntax and environment errors  
   - Scaling workflows across large repositories  

---

## Exercise Details  

**Data Provided:**  

| Item                                | Description                                                |
|-------------------------------------|------------------------------------------------------------|
| `.github/workflows/template.yml`    | Starter workflow illustrating basic lint-and-test steps    |
| `requirements.txt` / `renv.lock`    | Dependency definitions for Python and R environments       |
| `scripts/` folder                   | Sample geoprocessing and risk‐assessment scripts           |
| `tests/` folder                     | Unit and integration tests for spatial analysis functions  |

---

**Key Tasks:**  

- Create a new workflow file `ci-spatial.yml` that runs on `push` and `pull_request` to `main`.  

- Define a job matrix across Python 3.8/3.9 and R 4.1/4.2 to install dependencies and run tests.  

- Add a nightly scheduled trigger (`cron: '0 2 * * *'`) to regenerate summary maps and CSV outputs.  

- Store sensitive credentials as GitHub Secrets (`GEE_API_KEY`, `SLACK_WEBHOOK`) and reference them in steps.  

- Save generated map artifacts (`.png`, `.html`) as workflow artifacts for download.  

---

## Assignment  

Submit to `assignments/day93/` by Day 94 morning:  

1. **Workflow File**  
   - `ci-spatial.yml` in `.github/workflows/` with inline comments explaining each section.  

2. **CI Badge**  
   - Markdown snippet for the workflow status badge and a screenshot (`day93_ci_badge.png`).  

3. **Artifacts Report**  
   - `day93_artifacts.md`: list of generated artifacts (maps, reports) and links to download from Actions.  

4. **Testing Logs**  
   - `day93_test_logs.txt`: excerpt of a successful run and a deliberately-induced failure run, highlighting debugging steps.  

5. **Configuration Diagram**  
   - `day93_workflow_diagram.png`: flowchart showing triggers, jobs, and notification paths.  

6. **Reflection** (`day93_reflection.md`, 200 words)  
   - Reflect on challenges in writing YAML, managing cross‐language matrices, and ensuring reproducible runs.  

---

By completing this module, you’ll automate your spatial epidemiology pipelines—guaranteeing consistent, hands-off testing and reporting, and accelerating team collaboration.
