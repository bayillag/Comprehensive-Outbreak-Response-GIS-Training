# **Day 50 – Building a Simple Risk Score and Composite Map**
  
Bloom Level: Create & Apply | Duration: 4 hrs  

## Objectives  

- Select and justify key risk factors for disease emergence or spread.  
- Normalize and weight covariates to construct a composite risk index.  
- Compute a unit‐level risk score and classify into meaningful categories.  
- Visualize the composite map alongside individual risk layers for validation.  
- Interpret and communicate a risk surface to guide targeted interventions.  

## Agenda  

1. Lecture: Principles of Risk Scoring (45 min)  
   - Rationale for composite indices in epidemiology  
   - Methods for variable selection, normalization (min–max, z‐score), and weighting  
   - Classification schemes for risk categories (equal interval, quantiles, expert breakpoints)  

2. Demo: Computing and Mapping a Risk Score (30 min)  
   - Python: pandas for index calculations; GeoPandas for spatial joins  
   - R: dplyr and sf workflows; tmap for composite mapping  

3. Lab Part 1 – Building the Composite Index (60 min)  
   - Load `day50_admin.shp` and `day50_covariates.csv`  
   - Normalize selected covariates and apply expert or statistical weights  
   - Sum weighted covariates to generate `risk_score` field  

4. Lab Part 2 – Mapping and Validation (45 min)  
   - Classify `risk_score` into three–five categories  
   - Create side‐by‐side maps: individual covariate layer vs composite map  
   - Validate by comparing high‐risk areas to historical case locations  

5. Discussion & Q&A (30 min)  
   - Sensitivity of composite indices to weighting choices  
   - Best practices for presenting risk maps to stakeholders  
   - Limitations and next steps (e.g., adding temporal or network data)  

## Exercise Details  

**Data Provided:**  
- `day50_admin.shp`: administrative units with `admin_code`  
- `day50_covariates.csv`: unit‐level covariates (elevation, proximity to water, market density, NDVI)  
- Historical case points (`day50_cases.geojson`) for validation  

**Key Tasks:**  
1. Join covariate table to admin polygons and inspect distributions.  
2. Normalize each covariate (min–max or z‐score) and assign weights (equal or expert‐driven).  
3. Calculate composite `risk_score` and examine summary statistics.  
4. Classify into risk bands and style maps with a sequential color ramp.  
5. Overlay historical case points to assess concordance with predicted high‐risk zones.  

## Assignment  

Submit to `assignments/day50/` by Day 51 morning:

1. Composite Index Script  
   - `day50_risk_score.R` or `day50_risk_score.py` with annotated normalization and weighting steps  

2. Composite Shapefile  
   - `day50_admin_risk.shp` including `risk_score` and `risk_category` fields  

3. Map Outputs  
   - `day50_covariate_maps.png` (grid of individual covariate choropleths)  
   - `day50_composite_map.png` (choropleth of risk categories overlaid with case points)  

4. Analytical Report (`day50_report.md`, 300 words)  
   - Describe variable selection, weighting rationale, classification method, and validation results  

5. Reflection (`day50_reflection.md`, 200 words)  
   - Reflect on challenges in weighting choices, sensitivity of the index, and communicating composite risk results to decision‐makers.
