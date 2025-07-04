# **Day 113 – Deployment, Security & Best Practices**
  
Bloom Level: Apply & Evaluate | Duration: 4 hrs  

## Objectives  

- Understand deployment environments (development, staging, production) and associated workflows.  

- Containerize applications using Docker and orchestrate deployments with Docker Compose or Kubernetes/Helm.  

- Implement secure practices: TLS/SSL certificates, environment variable secrets, and secret‐management services.  

- Configure logging, monitoring, and health‐check endpoints to ensure operational visibility.  

- Adopt best practices for CI/CD gating, infrastructure as code, documentation, backups, and disaster recovery.  

---  

## Agenda  

1. Lecture: Deployment Architectures & Security Fundamentals (45 min)  
   - Multi‐environment promotion: dev → staging → prod  
   - Security pillars: confidentiality, integrity, availability  
   - Secrets management patterns: env vars, Vault, Kubernetes Secrets  

2. Demo: Docker Compose & Kubernetes Deployment (30 min)  
   - Building and tagging Docker images  
   - Defining services in `docker-compose.yml`  
   - Deploying a Helm chart to a Kubernetes cluster  

3. Lab Part 1 – Containerization & Infrastructure as Code (60 min)  
   - Write a `Dockerfile` for your Day 112 API and dashboard  
   - Create a `docker-compose.yml` for app, database, and proxy with HTTPS  
   - (Optional) Scaffold a simple Helm chart with templated values  

4. Lab Part 2 – Security, Monitoring & Health Checks (45 min)  
   - Generate a self‐signed or Let’s Encrypt TLS certificate and configure an NGINX reverse proxy  
   - Store API keys and DB credentials securely in `.env` or Kubernetes Secret manifests  
   - Add `/health` and `/metrics` endpoints; integrate Prometheus scraping and Grafana dashboard  

5. Discussion & Q&A (30 min)  
   - CI/CD gating: tests, linting, security scans before deployment  
   - Backup & restore strategies for databases and file storage  
   - Documentation and runbooks for on‐call and incident response  

---  

## Exercise Details  

**Data & Templates Provided:**  

| Item                                  | Description                                                  |
|---------------------------------------|--------------------------------------------------------------|
| `day113_docker_template/`             | Example `Dockerfile` and `docker-compose.yml`                |
| `day113_helm_chart/`                  | Starter Helm chart scaffold with templated `values.yaml`     |
| `nginx_tls_example/`                  | NGINX config for TLS termination and reverse proxy           |
| `prometheus_grafana_templates/`       | Basic Prometheus scrape config and Grafana dashboard JSON    |

**Key Tasks:**  
- Build and tag Docker images for your API and QGIS‐exported dashboards.  
- Define a `docker-compose.yml` that spins up the app, PostGIS, Prometheus, and Grafana.  
- (Optional) Package your application as a Helm chart; install to a local or cloud k8s cluster.  
- Generate or import TLS certificates; configure NGINX (in Docker or k8s Ingress) for HTTPS.  
- Create environment variable files and Kubernetes Secret manifests for DB credentials and API keys.  
- Implement health (`/health`) and metrics (`/metrics`) endpoints in your service.  
- Configure Prometheus to scrape metrics and Grafana to visualize request rates, error counts, and resource usage.  

---  

## Assignment  

Submit to `assignments/day113/` by Day 114 morning:  

1. Container Configurations  
   - `Dockerfile` and `docker-compose.yml` in `day113_containers/` with inline comments.  

2. (Optional) Helm Chart  
   - `day113_helm_chart/` directory containing `Chart.yaml`, `templates/`, and `values.yaml`.  

3. Security Setup  
   - `nginx.conf` for TLS proxy or k8s Ingress manifest with certificate references.  
   - Secret manifests or `.env.example` showing variable names (no real secrets).  

4. Monitoring & Health Checks  
   - Service code snippet adding `/health` and `/metrics` endpoints.  
   - `prometheus.yml` and `grafana_dashboard.json` with scrape/job definitions.  

5. CI/CD Pipeline Snippet  
   - YAML excerpt showing build→test→scan→deploy stages and secret handling.  

6. Analytical Report (`day113_report.md`, 400 words)  
   - Describe your deployment architecture, security controls, monitoring setup, and how they support reliability and compliance.  

7. Reflection (`day113_reflection.md`, 200 words)  
   - Reflect on challenges encountered in container orchestration, certificate management, and monitoring integration, and outline next steps for production readiness.  

---  

By completing this session, you’ll deploy robust, secure, and observable epidemiology applications—ensuring smooth operation, rapid iteration, and resilience in production environments.
