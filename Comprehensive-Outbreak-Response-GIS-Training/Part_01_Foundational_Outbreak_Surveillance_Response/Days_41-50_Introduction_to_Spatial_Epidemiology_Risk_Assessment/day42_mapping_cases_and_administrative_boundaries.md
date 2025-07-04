# **Day 42 – Mapping Cases and Administrative Boundaries**

Bloom Level: Apply & Analyze | Duration: 4 hrs  

## Objectives  

- Display case locations and counts within administrative polygons.  
- Join attribute data (case counts, population) to boundary layers.  
- Create point and choropleth maps highlighting spatial patterns.  
- Apply appropriate symbology and classification schemes for risk communication.  
- Export high‐quality map outputs for reports and presentations.  

## Agenda  

1. Lecture: Principles of Thematic Mapping (45 min)  
   - Point mapping vs. choropleth mapping  
   - Data joins, proper alignment of case and boundary data  
   - Classification methods: equal interval, quantiles, natural breaks  

2. Demo: Mapping in QGIS and Python (30 min)  
   - QGIS: styling point and polygon layers, labeling, legend design  
   - Python: using GeoPandas and Matplotlib/Contextily for static maps  

3. Lab Part 1 – Case Point Mapping (60 min)  
   - Load `day42_cases.geojson` and `day42_admin.shp`  
   - Reproject layers to common CRS (e.g., EPSG:4326)
   - Style case layer with graduated symbols based on case counts  

4. Lab Part 2 – Choropleth of Case Rates (45 min)  
   - Load `day42_population.csv`, join to `day42_admin` by admin code  
   - Calculate case rates per 1,000 animals  
   - Classify rates and apply a sequential color ramp  

5. Discussion & Q&A (30 min)  
   - Choosing classification schemes and color palettes for accessibility  
   - Ensuring map readability when overlaying points on polygons  

---

## Exercise Details  

**Data Provided:**  
- `day42_cases.geojson`: case records with `admin_code` and `case_count`  
- `day42_admin.shp`: administrative boundaries with `admin_code` and `admin_name`  
- `day42_population.csv`: population at risk by `admin_code`  

**Key Tasks:**  
1. Reproject and load all spatial data into QGIS or GeoPandas.  
2. Map case points with graduated symbol sizes (e.g., small to large).  
3. Join population data to boundary layer; compute case rate = (cases ÷ population) × 1,000.  
4. Create a choropleth map of case rates using at least three classification methods and compare.  
5. Export two map images: one point map, one choropleth, with titles, north arrow, scale bar, and legend.  

---

## Assignment  

Submit to `assignments/day42/` by Day 43 morning:  

1. Mapping Script  
   - `day42_map.R` or `day42_map.py` with comments on data loading, reprojection, joins, and styling.  

2. Map Outputs  
   - `day42_case_points.png` (point map)  
   - `day42_case_rate_choropleth.png` (choropleth map)  

3. QGIS Project File  
   - `day42_project.qgz` with saved styling for case and admin layers.  

4. Map Comparison Table (`day42_map_comparison.md`)  
   | Classification Method | Breaks Example       | Advantages                  | Drawbacks                   |
   |-----------------------|----------------------|-----------------------------|-----------------------------|
   | Equal Interval        | 0–5, 5–10, 10–15     | Simple, uniform class width | May hide clustering        |
   | Quantiles             | 0–3, 4–7, 8–15       | Equal count per class       | Variable interval widths   |
   | Natural Breaks (Jenks)| 0–2, 3–8, 9–15       | Minimizes within‐class variance | Depends on distribution |

5. Report (`day42_report.md`, 300 words)  
   - Describe mapping workflow, classification choices, and interpretation of spatial patterns.  

6. Reflection (`day42_reflection.md`, 200 words)  
   - Discuss challenges in joining data, choosing symbology, and ensuring map clarity for stakeholders.
