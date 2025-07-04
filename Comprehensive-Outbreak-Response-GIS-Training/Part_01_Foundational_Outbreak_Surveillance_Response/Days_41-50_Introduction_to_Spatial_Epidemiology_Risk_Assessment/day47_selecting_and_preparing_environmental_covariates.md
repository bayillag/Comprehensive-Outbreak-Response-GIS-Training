# **Day 47 – Selecting and Preparing Environmental Covariates**
  
Bloom Level: Analyze & Apply | Duration: 4 hrs  

## Objectives  

- Identify relevant environmental variables (elevation, land cover, proximity to water) for spatial epidemiology.  
- Acquire and inspect vector and raster covariate layers.  
- Reproject, clip, and align environmental datasets to a common CRS and extent.  
- Extract raster values at case and control locations and join vector attributes.  
- Assess covariate distributions and multicollinearity before modeling.  

---

## Agenda  

1. Lecture: Role of Environmental Covariates (45 min)  
   - Importance in outbreak drivers and spatial risk modeling  
   - Types: continuous vs. categorical; static vs. dynamic layers  
   - Criteria for selecting layers: biological relevance, data quality, spatial resolution  

2. Demo: GIS & Code Workflows (30 min)  
   - QGIS: loading, styling, and projecting rasters and vectors  
   - Python: GeoPandas for vectors, rasterio/xarray for rasters; R: `sf` and `raster` packages  

3. Lab Part 1 – Preparing Spatial Layers (60 min)  
   - Load provided rasters (`day47_elevation.tif`, `day47_ndvi.tif`, `day47_distance_water.tif`) and vectors (`day47_landcover.shp`, `day47_study_area.shp`)  
   - Reproject all layers to EPSG:4326 and align pixel grids (resample rasters to common resolution)  
   - Clip to study boundary  

4. Lab Part 2 – Extracting and Merging Covariates (45 min)  
   - Load case/control points (`day47_points.geojson`)  
   - Extract raster values at each point and join landcover categories  
   - Output a single table with environmental attributes  

5. Discussion & Q&A (30 min)  
   - Checking for missing or out‐of‐range values  
   - Strategies for reducing multicollinearity (variable selection, PCA)  
   - Documenting metadata and provenance  

---

## Exercise Details  

**Data Provided:**  
- Raster layers:  
  - `day47_elevation.tif` (elevation in meters)  
  - `day47_ndvi.tif` (normalized difference vegetation index)  
  - `day47_distance_water.tif` (meters to nearest water source)  
- Vector layers:  
  - `day47_landcover.shp` (categorical land‐cover types)  
  - `day47_study_area.shp` (analysis boundary)  
  - `day47_points.geojson` (case/control locations)  

**Key Tasks:**  
1. Reproject all datasets to a common CRS and resolution; clip to the study area.  
2. Resample rasters so they align spatially; verify extents and cell sizes.  
3. Extract raster values and landcover categories for each point.  
4. Compile an attribute table (`point_id`, `elevation`, `ndvi`, `dist_water`, `landcover`).  
5. Produce summary statistics and pairwise correlation matrix to assess distributions and collinearity.  

---

## Assignment  

Submit to `assignments/day47/` by Day 48 morning:  

1. Preparation Script (`day47_prep_env.R` or `day47_prep_env.py`)  
   - Annotated code for reprojection, clipping, resampling, and covariate extraction.  

2. GIS Project File (`day47_project.qgz`)  
   - QGIS project showing loaded rasters, vectors, reprojection, and styling.  

3. Covariate Table (`day47_covariates.csv`)  
   - Point‐level table with extracted environmental attributes.  

4. Summary Outputs:  
   - Distribution plots (`day47_env_distributions.png`)  
   - Correlation matrix (`day47_corr_matrix.png`)  

5. Analytical Report (`day47_report.md`, 300 words)  
   - Describe data sources, processing steps, variable selection rationale, and collinearity findings.  

6. Reflection (`day47_reflection.md`, 200 words)  
   - Discuss challenges in aligning multi‐source layers and strategies for robust covariate preparation.
