# Day 89 – Spatial Modeling with Regression Techniques**
  
Bloom Level: Analyze & Create | Duration: 4 hrs  

## Objectives  

- Understand spatial dependence and its effects on standard regression analyses.  

- Implement ordinary least squares (OLS) and diagnose spatial autocorrelation in residuals.  

- Fit spatial lag and spatial error models using PySAL or R’s spdep.  

- Apply geographically weighted regression (GWR) to capture spatially varying relationships.  

- Compare model performance, interpret spatial patterns of coefficients, and map residuals.  

---  

## Agenda  

1. Lecture: Spatial Regression Fundamentals (45 min)  
   - Concept of spatial dependence and spillover effects  
   - Distinction between spatial lag and spatial error processes  
   - Introduction to GWR and its use cases  

2. Demo: Fitting Spatial Models (30 min)  
   - OLS with diagnostics (Moran’s I on residuals)  
   - Spatial lag/error model workflows in Python (PySAL) or R (spdep)  
   - GWR implementation and bandwidth selection  

3. Lab Part 1 – OLS & Diagnostic Testing (60 min)  
   - Load and merge `day89_admin.shp`, `day89_outcome.csv`, `day89_covariates.csv`  
   - Fit OLS: outcome ~ covariates; examine coefficients and R²  
   - Compute Moran’s I on residuals and map residual clusters  

4. Lab Part 2 – Spatial Regression & GWR (45 min)  
   - Build spatial weights from `day89_weights.gal`  
   - Fit spatial lag and spatial error models; compare AIC and parameter changes  
   - Run GWR; map local coefficient surfaces for key predictors  

5. Discussion & Q&A (40 min)  
   - Interpreting differences across models  
   - When to prefer global vs. local models  
   - Communicating spatial regression findings to stakeholders  

---  

## Exercise Details  

**Data Provided:**  

- `day89_admin.shp`: polygons with `admin_id`  
- `day89_outcome.csv`: `admin_id`, disease incidence rate  
- `day89_covariates.csv`: `admin_id`, socio‐economic and environmental predictors  
- `day89_weights.gal`: spatial weights for contiguity or k‐NN  

**Key Tasks:**  

1. Merge shapefile and CSVs into a spatial data frame.  

2. Fit an OLS regression; extract coefficients, p‐values, R², and check residual Moran’s I.  

3. Build a spatial weights object; fit spatial lag and spatial error models; record AIC, log‐likelihood, and coefficient shifts.  

4. Implement GWR with an adaptive bandwidth; produce local coefficient maps for at least two predictors.  

5. Map residuals from each model to assess spatial patterns of unexplained variation.  

---  

## Assignment  

Submit to `assignments/day89/` by Day 90 morning:  

1. Spatial Regression Script  
   - `day89_spatial_regression.py` or `day89_spatial_regression.R` with OLS, lag, error, and GWR models.  

2. OLS Diagnostics Report  
   - `day89_ols_diagnostics.md` summarizing OLS results, residual Moran’s I statistic, and a small residual map.

3. Model Comparison Table  
   - `day89_model_summary.csv` listing model type, AIC, log‐likelihood, R² (or pseudo‐R²), and key coefficients.  

4. GWR Coefficient Maps  
   - `day89_gwr_coef_1.png` and `day89_gwr_coef_2.png` for two chosen predictors.  

5. Residuals Map  
   - `day89_residuals_map.png` showing residuals from the best‐performing model.  

6. Analytical Report  
   - `day89_report.md` (400 words) comparing global and local models, interpreting spatial coefficient patterns, and recommending modeling approaches.  

7. Reflection  
   - `day89_reflection.md` (200 words) on challenges in weight selection, model diagnostics, and balancing complexity vs. interpretability.  

---  

By mastering spatial regression and GWR, you’ll be able to quantify and visualize how relationships vary across space, leading to more nuanced risk modeling and targeted interventions.
