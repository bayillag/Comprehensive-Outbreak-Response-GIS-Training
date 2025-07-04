# **Day 108 – Spatial Queries: Buffer, Intersect & Distance**
  
Bloom Level: Apply & Create | Duration: 4 hrs  

## Objectives  

- Understand the use cases and parameters of ST_Buffer, ST_Intersects, and ST_Distance.  

- Generate buffer zones around points and lines to define areas of interest.  

- Extract overlapping features using intersection queries.  

- Calculate and rank distances between geometries for proximity analyses.  

- Combine spatial predicates to answer epidemiological questions (e.g., service coverage).  

---  

## Agenda  

1. Lecture: Core Spatial Functions (45 min)  
   - Semantics of ST_Buffer, ST_Intersects, ST_Distance  
   - Units, precision, and performance considerations  

2. Demo: Spatial Queries in PostGIS (30 min)  
   - Executing buffer, intersection, and distance queries in psql  
   - Visualizing query outputs in QGIS  

3. Lab Part 1 – Buffer & Intersection Operations (60 min)  
   - Create 500 m, 1 km, and 5 km buffers around villages and roads  
   - Extract water sources and roads within village buffers using ST_Intersects  

4. Lab Part 2 – Distance-Based Filtering (45 min)  
   - Compute nearest health facility for each case point with ST_Distance and ORDER BY  
   - Identify cases beyond specified service thresholds  

5. Discussion & Q&A (30 min)  
   - Performance tips: leveraging spatial indexes, avoiding full-table scans  
   - Handling invalid geometries and edge-case buffers  

---  

## Exercise Details  

**Data Provided:**  

| File                    | Description                                        |
|-------------------------|----------------------------------------------------|
| day108_villages.shp     | Village locations (points)                         |
| day108_roads.shp        | Major roads (lines)                                |
| day108_water.shp        | Water sources (wells, springs)                     |
| day108_cases.shp        | Geocoded disease case points                       |
| day108_facilities.shp   | Health facilities with capacity attributes         |

**Key Tasks:**  

- Reproject all layers to a common CRS (e.g., EPSG:3857) and load into PostGIS.  

- Use ST_Buffer to build 500 m, 1 km, and 5 km buffer zones around village points and roads.  

- Run ST_Intersects to list roads and water sources that fall within each village buffer.  

- Calculate ST_Distance between each case point and the nearest facility; insert results into a table.  

- Query villages with no facilities within 10 km and export their IDs.  

---  

## Assignment  

Submit to `assignments/day108/` by Day 109 morning:  

1. **Spatial Query Script**  
   - `day108_spatial_queries.sql` containing annotated ST_Buffer, ST_Intersects, and ST_Distance queries.  

2. **psql Command Log**  
   - `day108_psql_commands.txt` listing meta-commands and SQL statements executed.  

3. **Result Tables**  
   - `day108_buffers.geojson`: buffer polygons around villages and roads.  
   - `day108_intersections.csv`: records of intersecting features per buffer.  
   - `day108_case_distances.csv`: case IDs, nearest facility IDs, and distances.  

4. **Analytical Report** (`day108_report.md`, 300 words)  
   - Document methods, query optimizations, and spatial insights relevant to outbreak coverage.  

5. **Reflection** (`day108_reflection.md`, 200 words)  
   - Reflect on challenges in spatial querying, performance considerations, and lessons for outbreak analysis.  

---  

By mastering buffer, intersect, and distance operations in PostGIS, you’ll unlock powerful spatial querying capabilities to define service areas, assess overlaps, and measure proximity—key tasks in targeted epidemiological analyses.
