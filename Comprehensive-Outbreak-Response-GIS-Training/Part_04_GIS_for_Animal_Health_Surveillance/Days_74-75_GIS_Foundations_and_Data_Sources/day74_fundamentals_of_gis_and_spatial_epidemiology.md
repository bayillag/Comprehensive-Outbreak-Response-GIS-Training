# **Day 74 – Fundamentals of GIS & Spatial Epidemiology**
  
Bloom Level: Understand & Apply | Duration: 4 hrs  

---  

## Objectives  

- Explain core GIS concepts and their applications in spatial epidemiology.  

- Identify spatial data types (vector, raster) and manage coordinate reference systems.  

- Perform basic spatial operations: buffering, spatial joins, and overlay analyses.  

- Create choropleth maps to visualize disease incidence and population density.  

- Conduct kernel density estimation and Local Moran’s I for hotspot detection.  

---  

## Agenda  

1. Lecture: GIS Principles & Spatial Epidemiology (45 min)  
   - GIS fundamentals: data models, CRS, map projections  
   - Spatial epidemiology concepts: clustering, autocorrelation, risk surfaces  

2. Demo: Preparing Spatial Data (30 min)  
   - Loading shapefiles and rasters in QGIS and GeoPandas  
   - Inspecting and reprojecting CRS  
   - Overview of spatial join and overlay tools  

3. Lab Part 1 – Data Import & Mapping (60 min)  
   - Load `day74_admin.shp`, `day74_case_points.shp`, and `day74_population_raster.tif`  
   - Verify and set CRS (e.g., WGS84 → UTM)  
   - Perform a spatial join to assign cases to administrative units  
   - Calculate case rates per 1,000 animals and produce a choropleth map  

4. Lab Part 2 – Hotspot Analysis (60 min)  
   - Generate a kernel density surface of case points  
   - Compute Local Moran’s I or Getis-Ord Gi* for cluster detection  
   - Classify and map hotspots, coldspots, and non-significant areas  

5. Discussion & Q&A (45 min)  
   - Interpreting spatial analysis outputs in epidemiological context  
   - Common pitfalls: edge effects, scale choices, multiple testing  
   - Applications for targeting interventions and surveillance  

---  

## Exercise Details  

**Data Provided:**  
- `day74_admin.shp`: administrative boundaries with population attributes  
- `day74_case_points.shp`: geocoded case locations  
- `day74_population_raster.tif`: raster of livestock density  
- `day74_coordinates.csv`: sample CSV with latitude/longitude points  

**Key Tasks:**  
1. Import and reproject all layers to a common CRS suitable for area calculations.  
2. Use spatial join to aggregate case counts by admin unit and compute incidence rates.  
3. Create a choropleth map of incidence rates, applying an appropriate classification scheme (e.g., quantiles).  
4. Run kernel density estimation on case-point data to generate a smooth risk surface.  
5. Calculate Local Moran’s I or Getis-Ord Gi* in Python or QGIS; map significant clusters.  

---  

## Assignment  

Submit to `assignments/day74/` by Day 75 morning:  

1. Spatial Analysis Report (`day74_gis_report.md`, 300 words)  
   - Document data preparation steps, CRS decisions, methods, and key findings.  

2. QGIS Project or Python Notebook (`day74_gis_project.qgz` or `day74_spatial_analysis.ipynb`)  

3. Maps:  
   - `day74_choropleth.png` (incidence rate map)  
   - `day74_kde_surface.png` (kernel density heatmap)  
   - `day74_lisa_clusters.png` (Local Moran’s I cluster map)  

4. Analysis Script (`day74_spatial_analysis.py` or `day74_spatial_analysis.R`)  
   - Fully annotated code for import, processing, and spatial analyses.  

5. Reflection (`day74_reflection.md`, 200 words)  
   - Reflect on challenges in handling CRS, classification choices, and translating spatial outputs into actionable insights.  

---  

By mastering these GIS fundamentals, you will be able to map disease patterns, detect hotspots, and inform targeted public‐health interventions.
