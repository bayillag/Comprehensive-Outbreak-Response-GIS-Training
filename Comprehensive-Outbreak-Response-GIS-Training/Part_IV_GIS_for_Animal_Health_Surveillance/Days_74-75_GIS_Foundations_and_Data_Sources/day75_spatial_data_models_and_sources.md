# **Day 75 – Spatial Data Models & Sources**  

Bloom Level: Understand & Apply | Duration: 4 hrs  

## Objectives  

- Explain core spatial data models: vector (points, lines, polygons) versus raster (grids).  

- Identify and evaluate common spatial data sources: administrative boundaries, open‐street‐maps, satellite imagery, and crowd‐sourced data.  

- Assess data quality dimensions: spatial resolution, positional accuracy, temporal currency, and licensing constraints.  

- Manage and integrate multiple spatial formats (Shapefile, GeoJSON, GeoPackage, GeoTIFF).  

- Document metadata and data lineage for reproducibility and compliance.  

---  

## Agenda  

1. Lecture: Spatial Data Models & Formats (45 min)  
   - Vector vs. raster data structures and use cases  
   - Attribute tables, topology, and raster bands  
   - Common file formats and interoperability  

2. Demo: Spatial Data Repositories (30 min)  
   - OpenStreetMap and Geofabrik extracts  
   - Global Administrative Areas (GADM) and Natural Earth  
   - Landsat/Sentinel archives and Web Map Services (WMS)  

3. Lab Part 1 – Vector & Raster Handling (60 min)  
   - Load `day75_admin.shp` and inspect attribute schema  
   - Reproject to UTM and export as GeoPackage  
   - Load `day75_landsat.tif`, examine bands, and derive NDVI  

4. Lab Part 2 – Data Source Integration (45 min)  
   - Import `day75_osm.geojson` (roads, waterways) and merge with administrative polygons  
   - Clip raster to study area and convert key features to vector  
   - Build a unified spatial database  

5. Discussion & Q&A (30 min)  
   - Evaluating data resolution vs. analytical needs  
   - Handling licensing and attribution requirements  
   - Best practices for metadata, version control, and provenance  

---  

## Exercise Details  

**Data Provided:**  

| File                          | Description                                               |
|-------------------------------|-----------------------------------------------------------|
| day75_admin.shp               | Administrative boundaries with population attributes      |
| day75_osm.geojson             | Roads and waterways from OpenStreetMap                    |
| day75_landsat.tif             | Multi‐band satellite imagery (bands 4,5 for NDVI)         |
| day75_elevation.tif           | Digital elevation model                                   |
| day75_metadata_template.xlsx  | Metadata schema (fields: title, source, date, license)    |

**Key Tasks:**  

1. Import and inspect the vector shapefile; verify CRS and attribute integrity.  

2. Reproject and export vector data as a GeoPackage, preserving attribute tables.  

3. Load raster imagery; calculate NDVI and crop to administrative extents.  

4. Merge OSM vector layers with administrative boundaries; perform spatial joins.  

5. Compile metadata for each dataset using the provided template, noting source, date, resolution, and license.  

---  

## Assignment  

Submit to `assignments/day75/` by Day 76 morning:  

1. Data Inventory Table  
   - `day75_data_inventory.csv`: listing each dataset, format, CRS, resolution, and license.  

2. Metadata Records  
   - `day75_metadata.xlsx`: completed metadata for all provided and derived layers.  

3. Integration Script  
   - `day75_data_integration.py` or `day75_data_integration.R`: annotated code for import, reprojection, raster processing, and merges.  

4. Combined Map  
   - `day75_combined_map.png`: overlay of administrative boundaries, roads, NDVI raster hillshade.  

5. Spatial Data Source Report  
   - `day75_report.md` (300 words): evaluate data model choices, quality trade‐offs, and integration challenges.  

6. Reflection  
   - `day75_reflection.md` (200 words): discuss lessons on data interoperability, metadata importance, and future data sourcing strategies.  

---  

Mastering spatial data models and source integration lays the foundation for robust geospatial analyses in epidemiology and decision support.
