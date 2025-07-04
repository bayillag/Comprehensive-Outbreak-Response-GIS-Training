# **Day 100 – Navigating Kaggle Datasets & APIs**
  
Bloom Level: Understand & Apply | Duration: 4 hrs  

## Objectives  

- Configure and authenticate the Kaggle API for seamless data access.  

- Search, discover, and filter epidemiology‐relevant datasets programmatically.  

- Download and manage large files via the Kaggle CLI and Python/R clients.  

- Integrate downloaded data into Pandas/GeoPandas workflows for spatial analysis.  

- Automate dataset updates and maintain a manifest of fetched resources.  

---  

## Agenda  

1. Lecture: Kaggle Platform & API Basics (45 min)  
   - Overview of Kaggle’s data catalog, competitions, and kernels  
   - Authentication flow: `kaggle.json`, environment variables, and security  

2. Demo: Using the Kaggle CLI & Python Client (30 min)  
   - Installing `kaggle` via `pip` and configuring credentials  
   - Listing datasets, files, and dataset metadata via CLI and `kaggle.api`  

3. Lab Part 1 – Dataset Discovery & Download (60 min)  
   - Search for keywords like “cholera”, “livestock disease”, “environmental covariates”  
   - Programmatically list files in a chosen dataset  
   - Download specific files (CSV, GeoJSON, TIFF) into a workspace folder  

4. Lab Part 2 – Data Integration & Manifesting (45 min)  
   - Load CSV and raster data into Pandas/GeoPandas and validate schemas  
   - Build a `dataset_manifest.csv` capturing dataset slug, file name, file size, and date  
   - Write a script to check for updates and re‐download changed files  

5. Discussion & Q&A (30 min)  
   - Strategies for versioning and caching large datasets  
   - Handling rate limits and storage constraints  
   - Best practices for reproducible data pipelines  

---  

## Exercise Details  

| Resource                      | Description                                              |
|-------------------------------|----------------------------------------------------------|
| `kaggle.json`                 | Kaggle API token for authenticating the CLI              |
| `day100_kaggle_template.ipynb`| Starter notebook with API‐key placeholders and examples  |
| `day100_datasets.csv`         | CSV listing target dataset slugs and search keywords     |

**Key Tasks:**  

- Install and configure the Kaggle CLI; test authentication with `kaggle datasets list`.  
- Search and filter datasets using keywords and metadata filters (e.g., size, tags).  
- Programmatically list and download specific files from a selected dataset.  
- Load downloaded files into Pandas/GeoPandas, inspect schemas, and perform a simple plot.  
- Create and update `day100_dataset_manifest.csv` tracking slug, file names, download dates, and checksums.  

---  

## Assignment  

Submit to `assignments/day100/` by Day 101 morning:  

1. **Kaggle API Script**  
   - `day100_kaggle_api.py` or `day100_kaggle_api.R` implementing functions to search, list, and download files.  

2. **Exploration Notebook**  
   - `day100_kaggle_workflow.ipynb` showing interactive dataset discovery, download, and basic analysis.  

3. **Dataset Manifest**  
   - `day100_dataset_manifest.csv` with columns: `dataset_slug`, `file_name`, `size_bytes`, `download_date`, `checksum`.  

4. **Integration Report** (`day100_report.md`, 300 words)  
   - Outline your dataset selection process, API commands used, data loading steps, and initial insights.  

5. **Reflection** (`day100_reflection.md`, 200 words)  
   - Discuss the advantages and pitfalls of using Kaggle for epidemiological data, and strategies for reliable version control.  

---  

By mastering the Kaggle API and CLI, you’ll expedite access to high‐quality datasets and embed automated data retrieval into your spatial epidemiology pipelines—enhancing reproducibility and scale.
