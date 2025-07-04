# **Day 81 – Exploratory Spatial Data Analysis (ESDA)**
  
Bloom Level: Analyze & Evaluate | Duration: 4 hrs  

## Objectives  

- Define the role of ESDA in uncovering spatial patterns and anomalies.  
- Apply visual and statistical techniques to explore spatial distributions.  
- Compute global and local spatial statistics (e.g., Moran’s I, semivariogram).  
- Use interactive mapping and scatterplots to detect outliers and clusters.  
- Translate ESDA findings into hypotheses for further analysis.  

---  

## Agenda  

1. Lecture: ESDA Principles (45 min)  
   - Rationale and workflow of ESDA  
   - Visual vs. statistical exploration  

2. Demo: ESDA Tools & Workflows (30 min)  
   - QGIS interactive symbology and atlas  
   - Python: GeoPandas, PySAL, and Seaborn for ESDA  

3. Lab Part 1 – Visual Exploration (60 min)  
   - Load point and polygon layers  
   - Create choropleth, proportional symbol, and heat maps  
   - Generate spatial scatterplots and correlograms  

4. Lab Part 2 – Statistical Measures (45 min)  
   - Compute global Moran’s I and interpret significance  
   - Calculate semivariogram and fit variogram model  
   - Identify local clusters with Local Moran’s I  

5. Discussion & Q&A (40 min)  
   - Interpreting ESDA outputs in an epidemiological context  
   - When to move from exploration to formal modeling  

---  

## Exercise Details  

**Data Provided:**  

| File                         | Description                                      |
|------------------------------|--------------------------------------------------|
| day81_case_points.shp        | Geocoded case locations with attributes          |
| day81_admin_units.shp        | Administrative boundaries with population counts |
| day81_attributes.csv         | Case attributes: date, severity, species         |
| day81_spatial_weights.gal    | Contiguity-based spatial weights matrix          |

**Key Tasks:**  

1. Import and reproject all layers to a common CRS.  
2. Produce at least three map types: choropleth of incidence rate, proportional symbols of case counts, and kernel density heatmap.  
3. Create spatial scatterplots (e.g., attribute vs. join count) and correlograms to visualize spatial autocorrelation.  
4. Calculate global Moran’s I for incidence rates; test for statistical significance.  
5. Generate a semivariogram from case attributes and fit a theoretical variogram model.  
6. Run Local Moran’s I to identify local clusters and map significant hot/cold spots.  

---  

## Assignment  

Submit to `assignments/day81/` by Day 82 morning:  

1. ESDA Script  
   - `day81_esda.py` or `day81_esda.R` with annotated code for data import, visualization, and statistical calculations.  

2. Maps & Plots  
   - `day81_choropleth.png`  
   - `day81_proportional_symbols.png`  
   - `day81_kde_heatmap.png`  
   - `day81_correlogram.png`  
   - `day81_hotspot_map.png`  

3. Statistical Summary Table  
   - `day81_stats_summary.csv` containing global Moran’s I, semivariogram parameters, and Local Moran’s I results for each unit.  

4. ESDA Report (`day81_report.md`, 300 words)  
   - Document methods, key ESDA findings, and potential hypotheses for further spatial modeling.  

5. Reflection (`day81_reflection.md`, 200 words)  
   - Discuss challenges in choosing weights, interpreting variograms, and insights gained from exploratory analyses.  

---  

By mastering ESDA techniques you will be equipped to uncover hidden spatial structures in epidemiological data, guiding more targeted and effective follow-up analyses.