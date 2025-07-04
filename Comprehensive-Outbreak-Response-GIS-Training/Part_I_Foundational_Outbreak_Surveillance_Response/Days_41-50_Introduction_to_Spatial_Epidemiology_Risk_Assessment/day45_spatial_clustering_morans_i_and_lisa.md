# **Day 45 – Spatial Clustering—Moran’s I and LISA**
  
Bloom Level: Analyze & Apply | Duration: 4 hrs  

## Objectives  

- Define global spatial autocorrelation and local indicators of spatial association (LISA).  

- Explain Moran’s I statistic and its interpretation for detecting clustering in disease rates.  

- Compute global Moran’s I with permutation testing to assess significance of spatial patterns.  

- Calculate local Moran’s I to identify high‐high, low‐low, and spatial outlier clusters.  

- Visualize spatial clustering results in QGIS and Python (PySAL) or R (`spdep`).  

## Agenda  

1. Lecture: Spatial Autocorrelation Concepts (45 min)  
   - Distinction between global and local measures  
   - Moran’s I formula, expected value, and variance  
   - Interpretation of positive, negative, and zero autocorrelation  
   - LISA cluster types and multiple testing concerns  

2. Demo: Implementing Moran’s I and LISA (30 min)  
   - QGIS: “Spatial Autocorrelation (Moran’s I)” and “LISA Cluster Maps” tools  
   - Python: PySAL (`esda.Moran`, `esda.Moran_Local`) workflow  
   - R: `spdep::moran.test()`, `spdep::localmoran()` examples  

3. Lab Part 1 – Global Moran’s I Calculation (60 min)  
   - Load `day45_admin.shp` with `case_rate` attribute  
   - Build spatial weights matrix (Queen contiguity, row‐standardized)  
   - Compute Moran’s I and perform 999‐permutation test; record I, z‐score, p‐value  

4. Lab Part 2 – Local Moran’s I and LISA Mapping (45 min)  
   - Calculate local Moran’s I values and raw p‐values  
   - Adjust p‐values (e.g., Benjamini–Hochberg) and classify cluster types  
   - Style and export LISA cluster map highlighting significant clusters  

5. Discussion & Q&A (30 min)  
   - Interpreting global vs. local results in disease control  
   - Handling multiple testing and weight‐matrix sensitivity  
   - Targeting interventions using cluster insights  

---

## Exercise Details  

**Data Provided:**  
- `day45_admin.shp`: administrative boundaries with `admin_code`, `case_count`, and `population` fields  
- `day45_population.csv`: population at risk by `admin_code` (if rate needs recalculation)  

**Key Tasks:**  
1. Merge population data to compute `case_rate` per administrative unit.  
2. Generate Queen contiguity spatial weights and inspect neighbor counts.  
3. Calculate global Moran’s I with permutation inference; record statistic, z‐score, and p‐value.  
4. Compute local Moran’s I, adjust p‐values for multiple comparisons, and assign each unit to cluster categories (HH, LL, HL, LH, NS).  
5. Produce a Moran scatterplot and a LISA cluster map with clear legends and classification.  

---

## Assignment  

Submit to `assignments/day45/` by Day 46 morning:  

1. Spatial Clustering Script (`day45_spatial_clust.R` or `day45_spatial_clust.py`)  

2. Weights and Results Files  
   - `day45_weights_matrix.csv` (neighbor list or standardized weights)  
   - `day45_global_results.csv` (Moran’s I, z‐score, p‐value)  
   - `day45_local_results.csv` (local I, adjusted p‐value, cluster classification)  

3. Visual Outputs  
   - `day45_moran_scatter.png` (global Moran’s I scatterplot)  
   - `day45_lisa_map.png` (LISA cluster map)  

4. Analytical Report (`day45_report.md`)  
   - 400–500 words interpreting global and local clustering findings and their implications for outbreak response.  

5. Reflection (`day45_reflection.md`)  
   - 200 words on challenges in choosing spatial weights, correcting for multiple tests, and applying clustering results in field settings.
