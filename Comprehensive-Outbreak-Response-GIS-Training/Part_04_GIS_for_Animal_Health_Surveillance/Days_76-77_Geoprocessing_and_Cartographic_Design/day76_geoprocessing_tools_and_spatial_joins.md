# **Day 76 – Geoprocessing Tools & Spatial Joins**
  
Bloom Level: Understand & Apply | Duration: 4 hrs  

---

## Objectives  

- Master core geoprocessing operations: clipping, buffering, dissolving, merging, and intersection.  

- Perform spatial joins to link attribute data across layers (points→polygons, lines→polygons).  

- Use distance and proximity analyses to derive new spatial attributes.  

- Automate workflows using scripts in QGIS, Python (GeoPandas), or R (sf).  

- Prepare clean geospatial datasets for downstream epidemiological analyses.  

---

## Agenda  

1. Lecture: Geoprocessing Fundamentals (45 min)  
   - Definitions and use cases for clip, buffer, intersect, union, and dissolve  
   - Concepts behind spatial join and attribute transfer  
   - Common pitfalls: topology errors, CRS mismatches, sliver polygons  

2. Demo: Step-by-Step Geoprocessing (30 min)  
   - QGIS Processing Toolbox walkthrough  
   - Python GeoPandas examples for buffer and spatial join  
   - R sf workflows for intersection and distance calculations  

3. Lab Part 1 – Vector Operations (60 min)  
   - Clip administrative boundaries to a study area  
   - Buffer roads and waterways to create risk corridors  
   - Dissolve hazard zones to eliminate overlaps  

4. Lab Part 2 – Spatial Joins & Proximity (45 min)  
   - Join case points to polygons to count cases per district  
   - Attach nearest hospital attributes to each case by distance  
   - Compute distance from each village centroid to nearest water source  

5. Discussion & Q&A (30 min)  
   - Validating results and troubleshooting attribute mismatches  
   - Strategies for batching geoprocessing tasks  
   - Ensuring reproducibility and documenting workflows  

---

## Exercise Details  

**Data Provided:**  

| File                          | Description                                          |
|-------------------------------|------------------------------------------------------|
| day76_admin.shp               | Administrative boundaries (polygons)                 |
| day76_case_points.shp         | Geocoded disease case locations (points)             |
| day76_roads.shp               | Road network (lines)                                 |
| day76_waterways.shp           | Rivers and streams (lines)                           |
| day76_hospitals.csv           | Hospital locations with coordinates and capacity     |
| day76_study_area.shp          | Study-area polygon for clipping                      |
| day76_hazard_zones.shp        | Overlapping risk zones for dissolution practice      |

**Key Tasks:**  
1. Reproject all layers to a common CRS (e.g., UTM) and verify extents.  
2. Clip `day76_admin.shp` using `day76_study_area.shp` to produce `admin_clipped.shp`.  
3. Buffer `day76_roads.shp` by 500 m and waterways by 200 m; merge buffers into a single “risk_corridor” layer.  
4. Dissolve `day76_hazard_zones.shp` by risk category to remove overlaps.  
5. Perform a spatial join:  
   - Count case points per clipped admin unit (`cases_by_district`).  
   - Join nearest hospital attributes (name, capacity) to each case point (`case_hospitals`).  
6. Calculate Euclidean distance from each district centroid to the closest waterway; append as a new field.  
7. Export final processed layers and a summary CSV of district-level case counts and distances.  

---

## Assignment  

Submit to `assignments/day76/` by Day 77 morning:  

1. Geoprocessing Script  
   - `day76_geoprocessing.py` or `day76_geoprocessing.R` with annotated code for all operations.  

2. Processed Layers  
   - `admin_clipped.shp` (clipped boundaries)  
   - `risk_corridor.shp` (merged buffers)  
   - `hazard_dissolved.shp` (dissolved zones)  
   - `cases_by_district.csv` (district, case_count, distance_to_water)  
   - `case_hospitals.csv` (case_id, nearest_hospital, distance_km)  

3. Maps  
   - `day76_buffer_map.png` showing roads & waterways buffers over admin units  
   - `day76_case_join_map.png` choropleth of cases per district with hospital points  

4. Geoprocessing Report  
   - `day76_report.md` (300 words) documenting workflow steps, CRS decisions, parameter choices, and key outcomes.  

5. Reflection  
   - `day76_reflection.md` (200 words) on challenges encountered (e.g., sliver polygons, join mismatches), solutions applied, and lessons for reproducible GIS workflows.  

---

This session ensures you can leverage geoprocessing and spatial joins to prepare robust, analysis-ready geospatial data, laying the groundwork for advanced spatial epidemiology.
