# **Day 78 – Spatial Analysis for Risk & Clustering**
  
Bloom Level: Analyze & Evaluate | Duration: 4 hrs  

## Objectives  

- Differentiate between global and local measures of spatial autocorrelation.  

- Generate risk surfaces using kernel density estimation adjusted by population density.  

- Identify and map significant clusters with Local Moran’s I and Getis-Ord Gi*.  

- Apply spatial scan statistics for cluster detection using SaTScan or PySAL.  

- Interpret clustering results to prioritize targeted interventions.  

---  

## Agenda  

1. Lecture: Spatial Clustering Concepts (45 min)  
   - Global vs. local autocorrelation (Moran’s I, Geary’s C)  
   - Hotspot detection fundamentals: Gi* and spatial scan  

2. Demo: Kernel Density & Hotspot Mapping (30 min)  
   - QGIS Processing Toolbox and Python (GeoPandas/Seaborn) examples  
   - Generating risk surfaces and significance maps  

3. Lab Part 1 – Risk Surface & KDE (60 min)  
   - Load case and population layers  
   - Select optimal bandwidth and compute kernel density of cases  
   - Divide case density by population raster to produce risk surface  

4. Lab Part 2 – Local Clustering Analyses (45 min)  
   - Calculate global Moran’s I on administrative incidence rates  
   - Compute Local Moran’s I and Getis-Ord Gi* in Python or R  
   - Map significant high-high, low-low, and hotspot areas  

5. Discussion & Q&A (30 min)  
   - Comparing cluster detection methods  
   - Addressing multiple testing and edge effects  
   - Integrating cluster outputs into surveillance planning  

---  

## Exercise Details  

**Data Provided:**  

| Dataset                         | Description                                            |
|---------------------------------|--------------------------------------------------------|
| day78_admin.shp                 | Administrative boundaries with livestock counts        |
| day78_case_points.shp           | Geocoded case locations (points)                       |
| day78_population_density.tif    | Raster of animal population density                    |
| day78_incidence.csv             | Case counts and populations by admin unit              |

**Key Tasks:**  

- Normalize and reproject all layers to a common CRS.  

- Compute kernel density of case points with an empirically chosen bandwidth.  

- Produce a risk surface by dividing case density raster by population density raster.  

- Calculate global Moran’s I on computed incidence rates; test for significance.  

- Perform Local Moran’s I and Gi* analyses; identify significant clusters (p < 0.05).  

- Apply a spatial scan statistic (e.g., Kulldorff’s method) to detect primary and secondary clusters.  

---  

## Assignment  

Submit to `assignments/day78/` by Day 79 morning:  

1. Spatial Analysis Script  
   - `day78_spatial_analysis.py` or `day78_spatial_analysis.R` with annotated code for KDE, risk surface, and clustering analyses.  

2. Risk Surface Map  
   - `day78_risk_surface.png` showing normalized risk values across the study area.  

3. KDE Heatmap  
   - `day78_kde_heatmap.png` illustrating raw case-density kernel estimation.  

4. LISA Cluster Map  
   - `day78_lisa_clusters.png` highlighting high-high and low-low clusters from Local Moran’s I.  

5. Gi* Hotspot Map  
   - `day78_gistar_hotspots.png` depicting significant hotspot (Gi*) areas.  

6. Spatial Scan Cluster Map  
   - `day78_satscan_clusters.png` (or QGIS equivalent) showing detected clusters with likelihood ratio zones.  

7. Analytical Report  
   - `day78_report.md` (400 words) detailing methods, parameter choices, cluster interpretations, and intervention recommendations.  

8. Reflection  
   - `day78_reflection.md` (200 words) on challenges in bandwidth selection, multiple testing corrections, and translating cluster outputs into public-health actions.  

---  

This session equips you to uncover and interpret spatial patterns of risk and clustering, guiding data‐driven, geographically targeted interventions.
