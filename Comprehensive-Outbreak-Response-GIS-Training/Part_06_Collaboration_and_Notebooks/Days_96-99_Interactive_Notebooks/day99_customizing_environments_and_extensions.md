# **Day 99 – Customizing Development Environments & Extensions**
  
Bloom Level: Apply & Create | Duration: 4 hrs  

## Objectives  

- Configure reproducible Python and R environments using Conda, `renv`, or virtual environments.  
- Customize code editors and notebooks (VS Code, Jupyter) with extensions and debug tooling.  
- Install, enable, and configure QGIS plugins to extend geoprocessing capabilities.  
- Develop and load a simple QGIS Python plugin skeleton for spatial tasks.  
- Share and version environment definitions and editor settings for team consistency.  

---  

## Agenda  

1. Lecture: Environment & Editor Customization (45 min)  
   - Reproducible environments: Conda `environment.yml`, `requirements.txt`, R’s `renv.lock`  
   - IDE features: linting, formatting, debugging, integrated terminals  
   - GIS plugin architecture: QGIS plugin repository and Python hooks  

2. Demo: VS Code & Jupyter Customization (30 min)  
   - Installing and configuring extensions: Python, R, Pylance, `black`, `isort`, Jupyter Nbextensions  
   - Setting up debugging configurations (`launch.json`) and workspace settings (`settings.json`)  
   - Enabling Jupyter widgets (e.g., `ipywidgets`) and interactive map extensions (`ipyleaflet`)  

3. Lab Part 1 – Reproducible Python/R Environments (60 min)  
   - Use provided `environment.yml` or `renv.lock` to recreate the analysis environment  
   - Add a new dependency (e.g., `folium` for Python or `leaflet` for R), update lock files, and push changes  
   - Configure VS Code workspace settings to auto‐format on save and enforce linting rules  

4. Lab Part 2 – QGIS Plugin Skeleton & Notebook Extensions (45 min)  
   - Generate a QGIS plugin skeleton with the Plugin Builder template  
   - Implement a minimal function (e.g., buffer analyst) and load it in QGIS for testing  
   - Install and enable Jupyter Nbextensions: Table of Contents, Codefolding, and Variable Inspector  

5. Discussion & Q&A (30 min)  
   - Managing conflicting dependencies and environment drift  
   - Distributing plugins and extension settings to collaborators  
   - Balancing customization with maintainability  

---  

## Exercise Details  

**Templates Provided:**  

| File                                 | Description                                             |
|--------------------------------------|---------------------------------------------------------|
| `environment.yml`                    | Conda definition with core GIS, analysis, and plotting packages |
| `renv.lock`                          | R package lockfile for risk‐assessment project          |
| `.vscode/settings.json`              | Recommended VS Code workspace settings                  |
| `plugin_skeleton/`                   | QGIS Plugin Builder–generated template skeleton         |
| `notebook_extensions_list.txt`       | List of Jupyter Nbextension commands and configurations |

**Key Tasks:**  

1. Recreate the Python environment via `conda env create -f environment.yml` or R environment with `renv::restore()`.  
2. Install an additional package (e.g., `geemap` or `rmapshaper`), update lock files, and commit environment changes.  
3. Apply the provided `.vscode/settings.json` to your workspace and verify auto‐formatting, linting, and debug launch configurations.  
4. Scaffold a QGIS plugin from `plugin_skeleton/`, implement a “buffer zones” tool, and install into QGIS’s plugin directory for testing.  
5. Enable Jupyter Nbextensions listed in `notebook_extensions_list.txt` and demonstrate:  
   - A table‐of‐contents pane  
   - Code folding  
   - A variable inspector panel  

---  

## Assignment  

Submit to `assignments/day99/` by Day 100 morning:  

1. Environment Definition  
   - Updated `environment.yml` and/or `renv.lock` reflecting added dependencies.  

2. IDE Configuration  
   - `.vscode/settings.json` and `launch.json` showing formatting, linting, and debug setup.  

3. QGIS Plugin  
   - Final plugin folder (`day99_buffer_plugin/`) zipped, including source code and metadata.  
   - Screenshot `day99_plugin_ui.png` of the plugin loaded in QGIS.  

4. Notebook with Extensions  
   - `day99_nbextensions_demo.ipynb` illustrating enabled Nbextensions (TOC, folding, inspector).  

5. Analytical Report (`day99_report.md`, 300 words)  
   - Document your environment setup process, editor customizations, plugin development steps, and benefits to reproducibility.  

6. Reflection (`day99_reflection.md`, 200 words)  
   - Discuss challenges in environment management, extension compatibility, and how these customizations will streamline your spatial epidemiology workflows.  

---  

By mastering environment definitions and extending your editors and GIS platform, you’ll create a consistent, efficient workspace that enhances collaboration and reproducibility across your spatial analysis projects.
