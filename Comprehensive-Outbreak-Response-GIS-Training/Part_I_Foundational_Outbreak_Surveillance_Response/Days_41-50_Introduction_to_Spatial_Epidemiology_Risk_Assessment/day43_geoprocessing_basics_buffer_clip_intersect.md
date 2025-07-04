# **Day 43 – Geoprocessing Basics—Buffer, Clip, Intersect**
  
Bloom Level: Apply | Duration: 4 hrs  

## Objectives  

- Understand buffer, clip, and intersect geoprocessing operations and their use cases.  

- Create buffer zones around vector features to define influence areas.  

- Clip spatial layers to a study‐area extent to limit dataset boundaries.  

- Perform intersection of multiple vector layers to derive common spatial features.  

- Execute these operations in both QGIS and Python (GeoPandas).  

---  

## Agenda  

1. Lecture: Geoprocessing Fundamentals (45 min)  
   - Definitions of buffer, clip, and intersect  
   - When and why to use each operation in outbreak investigations  

2. Demo: QGIS Toolbox & Python Geoprocessing (30 min)  
   - QGIS Buffer, Clip, and Intersection tools  
   - Python: GeoPandas methods (`buffer()`, `clip()`, `overlay()`)  

3. Lab Part 1 – Buffer Zones (60 min)  
   - Generate fixed‐distance buffers around roads or water sources  
   - Explore variable buffers (e.g., 1 km, 5 km, 10 km)  

4. Lab Part 2 – Clip and Intersect Operations (45 min)  
   - Clip buffer output to a study‐area polygon  
   - Intersect clipped buffer with point layer to select features within the zone  

5. Discussion & Q&A (30 min)  
   - Handling coordinate units and projection considerations  
   - Troubleshooting topology and attribute join issues  

---  

## Exercise Details  

**Data Provided:**  
- `day43_roads.shp`: line layer of roads  
- `day43_study_area.shp`: polygon of the study boundary  
- `day43_points.shp`: point features (e.g., case locations)  

**Key Tasks:**  
1. Create a 500 m buffer around `day43_roads.shp`.  
2. Clip that buffer output to `day43_study_area.shp`.  
3. Intersect the clipped buffer with `day43_points.shp` to extract points within the buffer.  
4. Validate geometric and attribute integrity of each output.  
5. Record geoprocessing parameters and any projection transformations.  

---  

## Assignment  

Submit to `assignments/day43/` by Day 44 morning:  

1. Geoprocessing Script  
   - `day43_geoprocess.py` or `day43_geoprocess.R` with annotated steps  

2. QGIS Project File  
   - `day43_project.qgz` containing loaded layers and styling  

3. Output Layers  
   - `day43_buffer.shp` (buffer zone)  
   - `day43_clipped_buffer.shp` (clipped buffer)  
   - `day43_intersect_points.shp` (points within buffer)  

4. Workflow Report (`day43_report.md`, 300 words)  
   - Describe each geoprocessing step, parameter choices, and key results  

5. Reflection (`day43_reflection.md`, 200 words)  
   - Reflect on challenges with coordinate units, topology errors, and performance considerations  

---
