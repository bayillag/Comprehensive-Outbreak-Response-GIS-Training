# **Day 107 – PostGIS Geometry Types & Spatial Indexes**
  
Bloom Level: Understand & Apply | Duration: 4 hrs  

## Objectives  

- Explore PostGIS geometry types: Point, LineString, Polygon, Multi* variants.  
- Inspect and transform geometries using ST_GeometryType, ST_Multi, ST_Force2D, and casting.  
- Understand spatial reference systems and coordinate transformations with ST_Transform.  
- Create GiST and SP-GiST spatial indexes and comprehend their performance trade-offs.  
- Write spatial queries (bounding-box, distance, intersection) that leverage spatial indexes for speed.  

---  

## Agenda  

1. Lecture: Geometry Types & SRIDs (45 min)  
   - PostGIS geometry classes, SRID metadata, dimensionality (2D/3D)  
   - Use cases for single vs. multi-geometries  

2. Demo: Geometry Inspection & Casting (30 min)  
   - Querying ST_GeometryType and ST_SRID  
   - Converting between geometry types and forcing 2D/3D  

3. Lab Part 1 – Geometry Operations (60 min)  
   - Load sample tables (`roads`, `admin`, `water_sources`) into PostGIS  
   - Identify mixed geometry types and enforce consistency with ST_Multi  
   - Reproject geometries to a common SRID and extract centroids  

4. Lab Part 2 – Spatial Indexing & Benchmarking (45 min)  
   - Create GiST and SP-GiST indexes on geometry columns  
   - Run EXPLAIN ANALYZE on spatial queries before and after indexing  
   - Compare query plans and execution times for each index type  

5. Discussion & Q&A (40 min)  
   - When to choose GiST vs. SP-GiST vs. BRIN for spatial data  
   - Index maintenance costs, clustering, and VACUUM considerations  

---  

## Exercise Details  

**Data Provided:**  

| Item                                   | Description                                                    |
|----------------------------------------|----------------------------------------------------------------|
| `day107_data.sql`                      | PostgreSQL dump (with PostGIS) containing `roads`, `admin`, `water_sources` tables |
| `day107_geometry_template.sql`         | Starter SQL script with placeholders for geometry and index tasks |
| `day107_schema_diagram.png`            | ER diagram showing geometry columns and SRIDs                  |

**Key Tasks:**  

1. Restore `day107_data.sql` into a PostGIS-enabled database; verify PostGIS extension.  
2. Use `SELECT ST_GeometryType(geom), ST_SRID(geom)` to catalogue geometry types and CRSs.  
3. Normalize mixed types: apply `ST_Multi` and `ST_Force2D` where needed, then validate with your queries.  
4. Reproject all tables to SRID 3857 using `ST_Transform` and confirm with `ST_SRID`.  
5. Build a GiST index on `roads(geom)` and SP-GiST on `admin(geom)`; record creation times.  
6. Craft spatial filters:  
   - Bounding-box: `WHERE geom && ST_MakeEnvelope(...)`  
   - Distance: `WHERE ST_DWithin(geom, ST_SetSRID(...), distance)`  
   - Intersection: `WHERE ST_Intersects(geom, other_geom)`  
7. Execute each query before and after indexing; capture EXPLAIN ANALYZE outputs and timings.  

---  

## Assignment  

Submit to `assignments/day107/` by Day 108 morning:  

1. **Geometry & Index Script**  
   - `day107_geometry_indexes.sql` with annotated `CREATE INDEX`, geometry casts, and reprojection steps.  

2. **psql Command Log**  
   - `day107_psql_commands.txt` listing all psql commands and meta-commands used.  

3. **Query Performance Table**  
   - `day107_performance.csv` with columns: `query_type`, `index_type`, `exec_time_ms`, `plan_summary`.  

4. **EXPLAIN Reports**  
   - `day107_explain_before.txt` and `day107_explain_after.txt` containing full plan outputs.  

5. **Analytical Report** (`day107_report.md`, 300 words)  
   - Summarize geometry normalization steps, index selection rationale, and performance improvements.  

6. **Reflection** (`day107_reflection.md`, 200 words)  
   - Reflect on challenges in handling heterogeneous geometries, index trade-offs, and lessons for large spatial datasets.  

---  

Mastering PostGIS geometry types and spatial indexing will enable you to write high-performance spatial queries—essential for scalable, real-time epidemiological analyses.
