# **Day 44 – Visualizing Incidence Rates and Density Surfaces**
  
Bloom Level: Apply | Duration: 4 hrs  

## Objectives  

- Calculate and map incidence rates across administrative areas.  
- Generate kernel density surfaces from point case data to identify hotspots.  
- Integrate choropleth and raster density outputs for comprehensive spatial insight.  
- Customize symbology and classification for clear risk communication.  
- Use QGIS and Python (GeoPandas, rasterio, scikit-learn) for end-to-end workflows.  

## Agenda  

1. Lecture: Rate Mapping vs. Density Surfaces (45 min)  
   - Choropleth: incidence = cases ÷ population per unit  
   - Kernel density estimation (KDE): continuous hotspot surfaces  
   - Comparison table  

   | Visualization Type      | Input Data              | Tool/Method                      | Strengths                         | Limitations                    |
   |-------------------------|-------------------------|----------------------------------|-----------------------------------|--------------------------------|
   | Choropleth Map          | Polygon counts & pops   | QGIS styling, GeoPandas `plot()` | Clear rate comparison by unit     | Aggregation hides local detail |
   | Kernel Density Surface  | Point case locations    | QGIS Heatmap, Python `KernelDensity` | Reveals continuous hotspots       | Bandwidth choice affects output|

2. Demo: QGIS vs Python Workflows (30 min)  
   - QGIS: “Heatmap” tool, raster styling  
   - Python:  
     - GeoPandas for choropleth  
     - Scikit-learn or PySAL for KDE  
     - Rasterio/Folium for exporting maps  

3. Lab Part 1 – Incidence Choropleth (60 min)  
   - Load `day44_admin.shp` and `day44_population.csv`  
   - Load case points (`day44_cases.geojson`), aggregate by `admin_code`  
   - Compute incidence per 1,000 animals, join to admin layer  
   - Classify rates (quantiles, natural breaks) and apply color ramp  

4. Lab Part 2 – Density Surface Generation (45 min)  
   - In QGIS: run Heatmap -> set radius, output raster  
   - In Python:  
     - Extract 2D coordinates from GeoDataFrame  
     - Fit `KernelDensity` with chosen bandwidth  
     - Rasterize density surface and visualize with Matplotlib  

5. Discussion & Q&A (30 min)  
   - Choosing classification and bandwidth parameters  
   - Balancing interpretability and analytic accuracy  
   - Combining choropleth and density outputs in reports  

---

## Exercise Details  

**Data Provided:**  
- `day44_cases.geojson`: case points with `admin_code`.  
- `day44_admin.shp`: administrative boundaries.  
- `day44_population.csv`: population at risk by `admin_code`.  

**Key Tasks:**  
1. Aggregate point data into area counts; merge with population.  
2. Compute and map incidence rates with at least two classification methods.  
3. Produce a KDE surface in QGIS and replicate in Python; compare outputs.  
4. Export choropleth and density map images with legends and titles.  

---

## Assignment  

Submit to `assignments/day44/` by Day 45 morning:

1. Visualization Scripts  
   - `day44_choropleth.py` or `day44_choropleth.R`  
   - `day44_density.py` or `day44_density.R`  

2. Map Outputs  
   - `day44_incidence_choropleth.png`  
   - `day44_density_surface.png`  

3. QGIS Project File  
   - `day44_project.qgz` with layers and styling preserved  

4. Analytical Report (`day44_report.md`, 300 words)  
   - Describe methods, classification choices, bandwidth selection, and spatial insights.  

5. Reflection (`day44_reflection.md`, 200 words)  
   - Discuss challenges in mapping rates vs. densities and implications for stakeholder communication.