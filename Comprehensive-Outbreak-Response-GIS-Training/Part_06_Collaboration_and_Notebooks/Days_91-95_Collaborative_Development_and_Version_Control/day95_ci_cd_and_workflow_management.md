# **Day 95 – CI/CD & Workflow Management**
  
Bloom Level: Apply & Evaluate | Duration: 4 hrs  

## Objectives  

- Explain continuous integration, delivery, and deployment principles in data‐driven projects.  
- Design automated pipelines that run linting, testing, building, and deployment for spatial epidemiology workflows.  
- Manage workflow orchestration tools (GitHub Actions, GitLab CI/CD, Jenkins) and versioned artifacts.  
- Monitor pipeline health, configure notifications, and implement rollback strategies on failure.  
- Deploy containerized analyses, dashboards, or APIs to staging and production environments.  

---  

## Agenda  

1. Lecture: CI/CD Patterns & Best Practices (45 min)  
   - Pipeline‐as‐code, branching strategies, artifact management  
   - Security: secrets handling, least‐privilege builds  

2. Demo: Advanced CI/CD Pipelines (30 min)  
   - GitHub Actions with matrix builds, caching, artifact uploads  
   - Docker image builds and registry pushes  

3. Lab Part 1 – Pipeline Implementation (60 min)  
   - Scaffold `day95_ci_cd.yml` to:  
     1. Checkout code and install dependencies  
     2. Run unit tests and geoprocessing scripts  
     3. Build and push Docker containers  

4. Lab Part 2 – Deployment & Monitoring (45 min)  
   - Deploy container to a local or cloud cluster via Kubernetes/Helm  
   - Configure health checks, Slack/email notifications, and rollback triggers  

5. Discussion & Q&A (30 min)  
   - Balancing pipeline complexity vs. maintainability  
   - Strategies for secrets management and audit logging  

---  

## Exercise Details  

**Data Provided:**  

| Item                        | Description                                                 |
|-----------------------------|-------------------------------------------------------------|
| day95_repo_template.git     | Starter repository with scripts, tests, and Dockerfile      |
| ci-cd-template.yml          | Boilerplate GitHub Actions workflow                         |
| Dockerfile                  | Base container spec for Python/R spatial environments       |
| deployment-config/          | Example Kubernetes manifests and Helm charts                |

**Key Tasks:**  

- Clone and explore the template repo and existing CI skeleton.  
- Customize `day95_ci_cd.yml` to implement multi‐stage jobs: test, build, deploy.  
- Build and push a Docker image to a container registry.  
- Deploy the image using provided Kubernetes/Helm manifests.  
- Implement rollback logic when health checks fail, and configure notifications.  

---  

## Assignment  

Submit to `assignments/day95/` by Day 96 morning:  

1. **CI/CD Workflow File**  
   - `day95_ci_cd.yml` with inline comments describing each job, step, and trigger.  

2. **Docker & Deployment Config**  
   - Final `Dockerfile` and any modified Kubernetes/Helm manifests.  

3. **Deployment Report** (`day95_deployment_report.md`, 300 words)  
   - Document pipeline design, artifact versioning, deployment strategy, and rollback policy.  

4. **Workflow Diagram**  
   - `day95_pipeline_diagram.png` illustrating stages, triggers, artifact flow, and notification points.  

5. **Reflection** (`day95_reflection.md`, 200 words)  
   - Discuss challenges in orchestrating CI/CD, managing secrets, and lessons for sustainable automation.  

---  

Mastering CI/CD ensures reproducible, automated, and reliable delivery of spatial epidemiology analyses and decision‐support tools.
