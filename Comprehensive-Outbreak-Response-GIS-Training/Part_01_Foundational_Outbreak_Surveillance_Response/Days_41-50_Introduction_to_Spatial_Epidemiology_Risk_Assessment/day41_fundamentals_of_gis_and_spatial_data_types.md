# **Day 41 – Fundamentals of GIS & Spatial Data Types**

Bloom Level: Understand | Duration: 4 hrs  

## Objectives  

- Define raster and vector spatial data types and their key characteristics.  

- Understand coordinate reference systems (CRS) and map projections.  

- Identify common GIS file formats and their typical use cases.  

- Explore spatial data structure, topology, and attribute table integration.  

- Prepare vector and raster datasets for basic mapping tasks.  

## Agenda  

1. Lecture: Spatial Data Models (45 min)  
   - Overview of vector (points, lines, polygons) and raster (pixels) structures  
   - Coordinate Reference Systems, projections, and datum transformations  
   - Topology, attribute tables, and metadata  
   - Comparison table:

   | Data Type | Structure               | Use Cases                         | File Formats             |
   |-----------|-------------------------|-----------------------------------|--------------------------|
   | Vector    | Points, lines, polygons | Sampling sites, boundaries, roads | Shapefile, GeoJSON, GPKG |
   | Raster    | Grid cells, pixels      | Elevation, imagery, climate data  | GeoTIFF, ASCII grid      |

2. Demo: GIS Software Overview (30 min)  
   - QGIS interface: layers panel, map canvas, toolbars  
   - Loading, styling, and symbolizing vector and raster layers  
   - Inspecting attribute tables and layer metadata  

3. Lab Part 1 – Loading and Inspecting Spatial Data (60 min)  
   - Load `day41_points.shp`, `day41_polygons.shp`, and `day41_raster.tif` into QGIS  
   - Examine geometries, attribute fields, and layer properties  
   - Reproject all layers to a common CRS (e.g., EPSG:4326)  

4. Lab Part 2 – Creating a Point Layer from CSV (45 min)  
   - Import `day41_coords.csv` with latitude/longitude columns  
   - Define CRS and convert the table to a spatial point layer  
   - Edit attribute fields and export as GeoJSON  

5. Discussion & Q&A (30 min)  
   - Troubleshooting CRS mismatches and topology errors  
   - Best practices for organizing GIS projects and naming conventions  

---

## Exercise Details  

**Data Provided**  
- `day41_points.shp`, `day41_points.dbf`, `day41_points.shx`  
- `day41_polygons.shp`, `day41_polygons.dbf`, `day41_polygons.shx`  
- `day41_raster.tif`  
- `day41_coords.csv`  

**Key Tasks**  
1. Open and explore the provided vector and raster datasets in QGIS.  
2. Identify geometry types and list attribute fields for each layer.  
3. Reproject all layers to EPSG:4326 and verify coordinate transformations.  
4. Create a new point layer from `day41_coords.csv`; confirm correct CRS assignment.  
5. Export the new point layer to GeoJSON and Geopackage (GPKG) formats.  

---

## Assignment  

Submit to `assignments/day41/` by Day 42 morning:  

1. GIS Project File (`day41_qgis_project.qgz`) containing loaded layers and styling.  
2. New Point Layer (`day41_points_created.geojson`) with correctly assigned CRS.  
3. Attribute Summary (`day41_attributes.md`) detailing field names, data types, and sample values.  
4. Workflow Report (`day41_report.md`, 300 words) describing spatial data types, the importance of CRS, and file format choices.  
5. Reflection (`day41_reflection.md`, 200 words) on challenges encountered working with spatial data and proposed next learning steps.
