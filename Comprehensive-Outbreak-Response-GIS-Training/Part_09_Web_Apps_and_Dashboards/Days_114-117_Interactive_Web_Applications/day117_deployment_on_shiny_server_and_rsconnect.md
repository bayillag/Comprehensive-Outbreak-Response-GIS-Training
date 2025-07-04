# **Day 117 – Deployment on Shiny Server & rsconnect**  

Bloom Level: Apply & Evaluate | Duration: 4 hrs  

## Objectives  

- Deploy Shiny applications to a self-hosted Shiny Server (open source or Pro edition).  

- Configure and use the `rsconnect` R package to publish apps on shinyapps.io.  

- Manage application dependencies and system requirements on remote hosts.  

- Set up SSL termination, reverse proxy, and basic authentication for Shiny Server.  

- Automate deployment workflows with scripts and integrate into CI pipelines.  

---  

## Agenda  

1. Lecture: Shiny Hosting Landscape (45 min)  
   - Differences between Shiny Server open source, Pro, and shinyapps.io  
   - Infrastructure components: NGINX/Apache reverse proxy, SSL, load balancing  

2. Demo: Publishing via rsconnect (30 min)  
   - Installing and configuring `rsconnect`  
   - Deploying a sample app to shinyapps.io and managing versions  

3. Lab Part 1 – Shiny Server Setup (60 min)  
   - Provision a Linux server or VM and install Shiny Server  
   - Configure `/etc/shiny-server/shiny-server.conf` for multiple apps  
   - Deploy `day117_shiny_app/` into the server’s apps directory  
   - Enable HTTPS via self-signed or Let’s Encrypt certificates  

4. Lab Part 2 – Automating with rsconnect & CI (45 min)  
   - Write `deploy_app.R` invoking `rsconnect::deployApp()` with parameters  
   - Store tokens securely and automate deployments in GitHub Actions or GitLab CI  
   - Roll back to a previous version on shinyapps.io  

5. Discussion & Q&A (30 min)  
   - Best practices for scaling: Docker, Kubernetes, Shiny Server Pro features  
   - Monitoring app health, logs, and user authentication strategies  

---  

## Exercise Details  

| Resource                           | Description                                                           |
|------------------------------------|-----------------------------------------------------------------------|
| `day117_shiny_app/`                | Sample Shiny app folder (including `app.R`, `www/`, and `data/`)      |
| `shiny-server.conf.template`       | Starter configuration file with reverse proxy and SSL placeholders    |
| `rsconnect_script.R`               | Template R script for automated deployments via `rsconnect`           |
| `github-actions-deploy.yml`        | CI workflow snippet for deploying to shinyapps.io                     |

**Key Tasks:**  
- Install Shiny Server and verify the service status on your Linux host.  
- Adapt `shiny-server.conf.template` and reload the server to serve your app over HTTPS.  
- Use `rsconnect` to authenticate with shinyapps.io and publish the same app as a cloud backup.  
- Securely store and reference deployment tokens in a CI pipeline for one-click publishing.  
- Test version rollback on shinyapps.io by deploying an earlier commit.  

---  

## Assignment  

Submit to `assignments/day117/` by Day 118 morning:  

1. Shiny Server Configuration  
   - `shiny-server.conf` with comments explaining each directive and SSL setup.  

2. Deployed App URL  
   - Public URL of your app on Shiny Server and on shinyapps.io.  

3. Deployment Script  
   - `deploy_app.R` using `rsconnect::deployApp()` with parameterized arguments.  

4. CI Workflow Snippet  
   - `github-actions-deploy.yml` (or equivalent) demonstrating automated deploy stages.  

5. Analytical Report (`day117_report.md`, 300 words)  
   - Document your hosting choices, security configuration, and automation strategy.  

6. Reflection (`day117_reflection.md`, 200 words)  
   - Reflect on challenges in server configuration, SSL management, and CI integration.  

---  

By completing this session, you’ll master both self-hosted and managed Shiny deployments—ensuring your epidemiology dashboards are secure, scalable, and easy to update.
