# **Day 82 – Investigation of Spatial Clustering in R**
  
Bloom Level: Analyze & Evaluate | Duration: 4 hrs  

## Objectives  

- Load and prepare spatial data in R using sf and spdep.  

- Construct spatial weights matrices (contiguity & distance-based).  

- Compute global Moran’s I and interpret its significance via permutation tests.  

- Calculate Local Moran’s I (LISA) and Getis-Ord Gi* statistics for cluster detection.  

- Visualize clustering results with tmap or ggplot2 and export analytic outputs.  

---  

## Agenda  

1. Lecture: R Packages & Clustering Concepts (45 min)  
   - Overview of sf, spdep, tmap, and mapview  
   - Global vs. local autocorrelation metrics  

2. Demo: Spatial Weights & Global Moran’s I in R (30 min)  
   - Creating queen and k-nearest neighbor weights  
   - Running moran.test() and interpreting permutations  

3. Lab Part 1 – Local Indicators of Spatial Association (LISA) (60 min)  
   - Computing localmoran() and identifying high–high, low–low clusters  
   - Adjusting p-values for multiple testing  

4. Lab Part 2 – Getis-Ord Gi* Analysis (45 min)  
   - Calculating local G* with spdep’s localG()  
   - Mapping significance and effect size  

5. Discussion & Q&A (40 min)  
   - Comparing LISA and Gi* outputs  
   - Addressing edge effects and weight selection  
   - Integrating findings into epidemiological decision-making  

---  

## Exercise Details  

**Data Provided:**  
- `day82_admin.shp`: polygon layer with incidence rates  
- `day82_case_points.shp`: geocoded case locations (for optional KDE)  
- `day82_incidence.csv`: district-level case counts and population  
- `day82_weights.gal`: precomputed gal file for weight verification  

**Key Tasks:**  
1. Import shapefile and incidence data; merge attributes into an sf object.  
2. Build spatial weights:  
   - Queen contiguity (poly2nb + nb2listw)  
   - k-nearest neighbors (k = 5)  
3. Compute global Moran’s I for both weight schemes; run 999 permutations and record p-values.  
4. Calculate Local Moran’s I (LISA); classify each polygon into high–high, low–low, high–low, low–high, or not significant.  
5. Compute Getis-Ord Gi*; map significant hotspots (z > 1.96) and coldspots (z < –1.96).  
6. (Optional) Overlay case KDE surface for visual comparison.  

---  

## Assignment  

Submit to `assignments/day82/` by Day 83 morning:  

1. Spatial Clustering Script  
   - `day82_spatial_clustering.R` with annotated code for data import, weights creation, Moran’s I, LISA, and Gi* calculations.  

2. Clustering Report (RMarkdown)  
   - `day82_clustering_report.Rmd` rendering to HTML or PDF; include methods, results tables, and maps.  

3. Results Table  
   - `day82_cluster_results.csv` with columns: `admin_unit`, `local_moran`, `p_value_LISA`, `Gi_star`, `p_value_Gi`, `cluster_category`.  

4. Maps  
   - `day82_global_moran_map.png` showing incidence choropleth annotated with global Moran’s I statistic.  
   - `day82_lisa_cluster_map.png` displaying LISA cluster categories.  
   - `day82_gistar_map.png` illustrating Gi* hot and cold spots.  

5. Reflection  
   - `day82_reflection.md` (200 words) reflecting on weight selection, interpreting local vs. global metrics, and potential applications of clustering in outbreak response.  

---  

By completing this module, you will harness R’s spatial statistics capabilities to detect and interpret disease clusters, strengthening your toolkit for targeted epidemiological interventions.
