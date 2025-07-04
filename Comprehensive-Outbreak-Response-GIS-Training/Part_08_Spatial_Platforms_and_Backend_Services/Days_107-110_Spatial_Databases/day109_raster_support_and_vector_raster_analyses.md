# **Day 109 – Raster Support & Vector–Raster Analyses**
  
Bloom Level: Understand & Apply | Duration: 4 hrs  

## Objectives  

- Load and register raster datasets in PostGIS.  
- Inspect raster metadata and bands with ST_Metadata and ST_BandMetaData.  
- Perform raster-to-vector and vector-to-raster conversions.  
- Extract raster values at point locations and along line strings.  
- Compute zonal statistics by aggregating raster cells over polygon zones.  

---  

## Agenda  

1. **Lecture: PostGIS Raster Fundamentals** (45 min)  
   - Raster storage model in PostGIS (tiles, bands, overviews)  
   - Core functions: ST_AddRasterColumn, ST_RegisterRaster, ST_Metadata  

2. **Demo: Importing & Inspecting Rasters** (30 min)  
   - Loading GeoTIFFs via `raster2pgsql` or `ST_FromGDALRaster`  
   - Querying raster properties: extent, resolution, nodata values  

3. **Lab Part 1 – Raster Registration & Metadata Extraction** (60 min)  
   - Import `day109_elevation.tif` and `day109_landcover.tif` into PostGIS  
   - Use SQL to inspect SRID, block size, pixel type, and band statistics  
   - Build overviews (pyramids) with `ST_CreateOverview` for faster rendering  

4. **Lab Part 2 – Vector–Raster Operations** (45 min)  
   - Sample elevation at `day109_case_points.shp` using `ST_Value` and export results  
   - Calculate average elevation per district polygon with `ST_SummaryStatsAgg`  
   - Rasterize `day109_roads.shp` onto a new raster matching elevation grid  

5. **Discussion & Q&A** (30 min)  
   - Performance tips: tiling, overviews, indexing with `CREATE INDEX ... USING GIST`  
   - Choosing between on-the-fly queries and materialized views for large rasters  

---  

## Exercise Details  

**Data Provided:**  

| File                       | Description                                  |
|----------------------------|----------------------------------------------|
| day109_elevation.tif       | DEM GeoTIFF (30 m resolution)                |
| day109_landcover.tif       | Land cover raster (classification codes)     |
| day109_case_points.shp     | Disease case locations with coordinates      |
| day109_districts.shp       | Administrative zones for zonal statistics    |
| day109_roads.shp           | Road centerlines for rasterization           |

**Key Tasks:**  
1. Reproject and import both rasters into a PostGIS-enabled database.  
2. Query raster metadata: SRID, pixel width/height, band count, min/max values.  
3. Register overviews and create spatial indexes on raster tables.  
4. Extract pixel values at case points and save to `case_elevation_values.csv`.  
5. Aggregate mean and standard deviation of elevation within each district; export as `district_elevation_stats.csv`.  
6. Rasterize the road network to match elevation raster dimensions; store result as `roads_raster`.  

---  

## Assignment  

Submit to `assignments/day109/` by Day 110 morning:  

1. **Raster SQL Script**  
   - `day109_raster_operations.sql` with annotated commands for import, metadata queries, sampling, zonal stats, and rasterization.  

2. **psql Command Log**  
   - `day109_psql_commands.txt` listing meta-commands and SQL statements executed.  

3. **Output Files**  
   - `case_elevation_values.csv` (point-sampled elevation).  
   - `district_elevation_stats.csv` (zonal summary).  
   - `roads_raster.tif` (rasterized roads).  

4. **Analytical Report** (`day109_report.md`, 300 words)  
   - Document methods, SQL functions used, performance considerations, and key spatial findings.  

5. **Reflection** (`day109_reflection.md`, 200 words)  
   - Reflect on challenges in raster handling, indexing strategies, and how these techniques support epidemiological analyses.  

---  

Mastering PostGIS raster support and vector–raster analyses empowers you to integrate continuous environmental data with discrete surveillance layers—enabling richer, more nuanced spatial epidemiology workflows.
