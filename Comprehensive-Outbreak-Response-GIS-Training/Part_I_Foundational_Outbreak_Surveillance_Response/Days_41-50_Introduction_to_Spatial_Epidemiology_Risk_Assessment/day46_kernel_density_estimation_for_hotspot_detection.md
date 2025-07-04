# **Day 46 – Kernel Density Estimation for Hotspot Detection**
  
Bloom Level: Analyze & Apply | Duration: 4 hrs  

## Objectives  

- Understand the principles of kernel density estimation (KDE) and its role in identifying spatial hotspots.  
- Select appropriate kernel functions and bandwidth parameters for animal case data.  
- Generate continuous density surfaces in QGIS and Python.  
- Define and extract hotspot polygons based on density thresholds.  
- Integrate density outputs with administrative boundaries for targeted interventions.  

---  

## Agenda  

1. **Lecture: KDE Fundamentals** (45 min)  
   - Theory of KDE: kernel shapes, bandwidth trade‐offs, edge effects  
   - Bandwidth selection methods: rule‐of‐thumb, cross‐validation  
   - Applications in outbreak investigations  

2. **Demo: QGIS vs. Python Workflows** (30 min)  
   - QGIS Heatmap tool: parameters, weight by case counts  
   - Python: `scikit-learn`’s `KernelDensity`, gridded evaluation, raster exporting  

3. **Lab Part 1 – KDE in QGIS** (60 min)  
   - Load `day46_cases.geojson` and `day46_study_area.shp`  
   - Reproject to an equal‐area CRS (e.g., EPSG:6933)  
   - Configure Heatmap: choose radius (bandwidth), output extent, weight by `case_count`  
   - Clip density raster to study area and style with a sequential color ramp  

4. **Lab Part 2 – KDE in Python** (45 min)  
   - Read case points with GeoPandas, transform CRS  
   - Fit `KernelDensity(bandwidth=500, kernel='gaussian')` on point coordinates  
   - Evaluate density on a regular grid, convert to raster with Rasterio  
   - Apply density thresholds (e.g., top 10%) to delineate hotspots  

5. **Discussion & Q&A** (30 min)  
   - Comparing QGIS and Python outputs: consistency and performance  
   - Setting thresholds: statistical vs. policy‐driven approaches  
   - Communicating hotspots to stakeholders  

---  

## Exercise Details  

**Data Provided:**  
- `day46_cases.geojson`: spatial points with `case_count` attribute  
- `day46_study_area.shp`: polygon defining the analysis extent  

**Key Tasks:**  
1. Project data to an appropriate equal‐area CRS for KDE.  
2. Generate KDE raster in QGIS, clip to study area, and export as `day46_kde_qgis.tif`.  
3. Implement Python KDE:  
   - Extract point coordinates, fit `KernelDensity`, evaluate on grid.  
   - Rasterize and save as `day46_kde_py.tif`.  
4. Determine a density threshold (e.g., 90th percentile) and extract hotspot polygons (`day46_hotspots.shp`).  
5. Compare and validate hotspot boundaries from both workflows.  

---  

## Assignment  

Submit to `assignments/day46/` by Day 47 morning:

1. **KDE Scripts**  
   - `day46_kde_qgis_project.qgz` (QGIS project with Heatmap settings)  
   - `day46_kde.py` (Python script using GeoPandas and scikit-learn)  

2. **Outputs**  
   - `day46_kde_qgis.tif` (clipped KDE raster)  
   - `day46_kde_py.tif` (Python‐generated KDE raster)  
   - `day46_hotspots.shp` (hotspot polygons)  

3. **Analytical Report** (`day46_report.md`, 300 words)  
   - Describe KDE parameter choices, thresholding approach, and interpretation of hotspot patterns.  

4. **Reflection** (`day46_reflection.md`, 200 words)  
   - Reflect on challenges in bandwidth selection, rasterization, and integrating KDE with decision‐making.  

---
