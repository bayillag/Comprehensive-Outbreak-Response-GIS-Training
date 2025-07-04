# **Day 98 – Geospatial Analysis in Colab (geopandas & folium)**
  
Bloom Level: Apply & Create | Duration: 4 hrs  

---

## Objectives  

- Set up geospatial Python libraries (`geopandas`, `shapely`, `folium`) in a Google Colab environment.  
- Load and inspect vector and tabular geospatial data from Drive or GitHub.  
- Perform core spatial operations: coordinate reprojection, spatial joins, buffering, and clipping.  
- Build interactive web maps using Folium with custom popups, layers, and basemaps.  
- Export processed geodata and interactive maps for sharing and reporting.  

---

## Agenda  

1. Lecture: Geospatial Python in Colab (30 min)  
   - Overview of `geopandas`, `descartes`, `contextily`, and `folium`  
   - Differences between static plotting and interactive web maps  

2. Demo: Environment Setup & Data Loading (30 min)  
   - Installing libraries via `!pip install geopandas folium`  
   - Mounting Google Drive and cloning a GitHub repo  
   - Reading shapefiles and CSVs with `geopandas.read_file` and `pd.read_csv`  

3. Lab Part 1 – Spatial Operations with GeoPandas (60 min)  
   - Inspect CRS and reproject layers to metric coordinate system  
   - Perform a spatial join: assign case points to admin polygons  
   - Buffer water sources by a specified distance and clip to study area  
   - Compute summary statistics (case counts per district, buffer areas)  

4. Lab Part 2 – Interactive Mapping with Folium (45 min)  
   - Initialize a `folium.Map` with an appropriate basemap  
   - Add GeoJSON overlays for admin units colored by incidence rate  
   - Plot case points with circle markers and custom popups (e.g., date, severity)  
   - Toggle layers and add a legend control  

5. Discussion & Q&A (15 min)  
   - Best practices for performance in notebooks (tile caching, data sampling)  
   - Techniques for sharing maps (saving HTML, embedding in dashboards)  

---

## Exercise Details  

**Data Provided:**  

| File                     | Description                                 |
|--------------------------|---------------------------------------------|
| `day98_admin.shp`        | Administrative boundaries with population   |
| `day98_case_points.csv`  | Case locations: lat, lon, date, severity    |
| `day98_water_sources.shp`| Point locations of springs and wells        |
| `day98_study_area.geojson`| Polygon defining the study boundary        |

**Key Tasks:**  
1. Install and import all required libraries in your Colab notebook.  
2. Mount Google Drive or clone GitHub to access data files.  
3. Read spatial layers and verify their coordinate reference systems.  
4. Reproject all layers to a common metric CRS (e.g., EPSG:3857).  
5. Perform a spatial join to count cases per admin unit; save results to a new GeoDataFrame.  
6. Buffer water-source points by 500 m; clip the buffer to the study‐area polygon.  
7. Calculate total buffer area per district and join back to admin GeoDataFrame.  
8. Create an interactive Folium map:  
   - Choropleth of case incidence rate  
   - Layer of buffered water zones  
   - Circle markers for individual cases with pop-ups  

---

## Assignment  

Submit to `assignments/day98/` by Day 99 morning:  

1. **Colab Notebook**  
   - `day98_geospatial_colab.ipynb` with annotated code for setup, spatial operations, and mapping.  

2. **Spatial Processing Script**  
   - `day98_geoprocessing.py` extracting key GeoPandas operations for automation.  

3. **Interactive Map**  
   - `day98_map.html` (Folium export) and a screenshot `day98_map.png`.  

4. **Data Outputs**  
   - `day98_cases_by_district.geojson` with case counts and buffer areas.  
   - `day98_water_buffer.geojson` of clipped buffers.  

5. **Analytical Report**  
   - `day98_report.md` (300 words) documenting methods, key spatial findings, and map interpretation.  

6. **Reflection**  
   - `day98_reflection.md` (200 words) on challenges in Colab performance, interactive mapping trade-offs, and next steps for integrating results into dashboards.  

---

By completing this module, you’ll harness Colab’s cloud resources to perform geospatial analyses and build interactive maps—streamlining sharing and collaboration for spatial epidemiology projects.
