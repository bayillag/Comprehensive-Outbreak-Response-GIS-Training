# **Day 84 – Spatial Risk Assessment using R**
  
Bloom Level: Apply & Create | Duration: 4 hrs  

## Objectives  

- Recap the hazard–exposure–vulnerability framework for risk assessment.  

- Load and preprocess raster and vector data in R using `terra` and `sf`.  

- Normalize raster layers to a common 0–1 scale programmatically.  

- Apply a weighted‐sum overlay in R to generate a composite risk surface.  

- Validate the risk map by extracting risk values at case‐point locations and assessing concordance.  

---

## Agenda  

1. **Lecture: R Workflows for Risk Mapping** (45 min)  
   - Overview of `terra`, `sf`, and `tidyverse` roles  
   - Strategies for raster normalization and weighted overlays in code  

2. **Demo: Scripted Risk Assessment** (30 min)  
   - Reading rasters and vector points  
   - Normalizing layers with `app()`  
   - Computing weighted sum and classification with `classInt`  

3. **Lab Part 1 – Data Preparation & Normalization** (60 min)  
   - Load `day84_hazard.tif`, `day84_exposure.tif`, `day84_vulnerability.tif`  
   - Read `day84_weights.csv` and `day84_admin_boundaries.shp`  
   - Reproject all to a common CRS and align extents/resolution  
   - Normalize each raster band (min–max scaling)  

4. **Lab Part 2 – Composite Risk Surface & Validation** (45 min)  
   - Compute composite risk = sum(layer * weight)  
   - Classify into low/medium/high using quantiles or Jenks breaks  
   - Load `day84_case_points.shp`, extract risk values at points  
   - Summarize risk‐at‐cases (mean, distribution) and map overlays  

5. **Discussion & Q&A** (30 min)  
   - Interpreting validation results and adjusting weights  
   - Automating the process in an RMarkdown/`targets` pipeline  
   - Communicating risk outputs to stakeholders  

---

## Exercise Details  

**Data Provided:**  
- `day84_hazard.tif`: environmental hazard raster  
- `day84_exposure.tif`: livestock density raster  
- `day84_vulnerability.tif`: socioeconomic vulnerability raster  
- `day84_case_points.shp`: geocoded case locations  
- `day84_weights.csv`: weights for hazard, exposure, vulnerability  
- `day84_admin_boundaries.shp`: polygons for final map context  

**Key Tasks:**  
1. Import rasters and vector layers; reproject to a unified CRS.  
2. Normalize each raster to 0–1 via min–max scaling in code.  
3. Read weights; apply a weighted overlay to generate a composite risk raster.  
4. Classify composite raster into three risk strata using quantile or Jenks breaks.  
5. Extract risk values at each case point; compute summary statistics and produce a validation map.  
6. Export normalized rasters, composite risk layer, and validation outputs.  

---

## Assignment  

Submit to `assignments/day84/` by Day 85 morning:

1. **Risk Assessment Script**  
   - `day84_risk_assessment.R` with annotated code for data import, normalization, overlay, and validation.  

2. **RMarkdown Report**  
   - `day84_risk_analysis.Rmd` rendering to HTML or PDF; include methods, maps, code snippets, and validation results.  

3. **Composite Risk Map**  
   - `day84_composite_risk_map.png` showing low, medium, and high risk zones with legend and scale bar.  

4. **Validation Summary**  
   - `day84_risk_at_cases.csv` listing case point IDs and their extracted risk values.  
   - `day84_validation_map.png` overlaying case points colored by risk stratum.  

5. **Analytical Report**  
   - `day84_risk_report.md` (300 words) detailing weight rationale, methods, key findings, and recommendations.  

6. **Reflection**  
   - `day84_reflection.md` (200 words) on challenges in scripting normalization, weight selection, and validating outputs.  

---  

Automating spatial risk assessment in R ensures reproducible, transparent workflows that integrate seamlessly into broader analytic pipelines.
