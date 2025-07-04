
# **Day 85 – Raster Data & Environmental Covariates with Google Earth Engine**
  
Bloom Level: Understand & Apply | Duration: 4 hrs  

## Objectives  

- Harness Google Earth Engine (GEE) to access and manage global raster datasets.  
- Extract key environmental covariates: precipitation, temperature, NDVI, land cover, elevation.  
- Apply preprocessing steps in GEE: reprojection, mosaicking, cloud masking, temporal aggregation.  
- Integrate GEE Python/R APIs into local analytic workflows.  
- Export processed rasters for downstream risk modeling and mapping.  

---  

## Agenda  

1. Lecture: Google Earth Engine Fundamentals (45 min)  
   - Data catalog overview (satellite, climate, topography)  
   - JavaScript Code Editor vs. Python/R API usage  
   - Quotas, asset management, and export options  

2. Demo: Preprocessing and Covariate Extraction (30 min)  
   - Cloud masking for MODIS/Sentinel imagery  
   - Temporal aggregation (monthly, seasonal composites)  
   - Calculating zonal statistics on custom geometries  

3. Lab Part 1 – Import & Preprocess Rasters (60 min)  
   - Load CHIRPS precipitation and compute annual mean  
   - Access MODIS NDVI; apply QA band mask and derive seasonal NDVI  
   - Import SRTM elevation and compute slope/aspect  

4. Lab Part 2 – Covariate Extraction & Export (45 min)  
   - Define study-area geometry via asset or shapefile upload  
   - Extract zonal statistics for each covariate by administrative unit  
   - Export rasters and tables to Google Drive or Cloud Storage  

5. Discussion & Q&A (30 min)  
   - Balancing spatial resolution, temporal span, and processing time  
   - Data licensing and sharing considerations  
   - Integrating GEE exports into local risk‐model pipelines  

---  

## Exercise Details  

**Data Sources & Assets:**  

| Covariate        | GEE Collection/Asset                             | Notes                                     |
|------------------|--------------------------------------------------|-------------------------------------------|
| Precipitation    | `UCSB-CHG/CHIRPS/DAILY`                          | Daily, 0.05° resolution                   |
| NDVI             | `MODIS/006/MOD13Q1`                              | 16-day composites, quality‐masked         |
| Land Cover       | `ESA/WorldCover/v200`                            | 10 m resolution, 2020 map                 |
| Elevation        | `USGS/SRTMGL1_003`                               | 30 m resolution; derive slope/aspect      |
| Temperature      | `ECMWF/ERA5_LAND/HOURLY`                         | Hourly, 0.1° resolution                   |

**Key Tasks:**  
1. Authenticate with GEE and initialize the Python or R API.  
2. Load each collection; apply filters for date range and study extent.  
3. Preprocess imagery:  
   - Reproject to a common CRS (e.g., EPSG:3857) and resolution (e.g., 1 km).  
   - Cloud mask MODIS using QA flags.  
   - Aggregate to monthly or seasonal composites.  
4. Define study‐area geometry by importing a shapefile or drawing a polygon.  
5. Compute zonal statistics (mean, median, max) for each covariate at admin‐unit level.  
6. Export:  
   - Composite rasters as GeoTIFFs.  
   - Zonal‐stats tables as CSV.  

---  

## Assignment  

Submit to `assignments/day85/` by Day 86 morning:  

1. GEE Script  
   - `day85_gee_script.js` (JavaScript Code Editor) **or** `day85_gee_api.py` / `day85_gee_api.R`  
   - Includes authentication, preprocessing, covariate extraction, and export commands.  

2. Exported Rasters  
   - `day85_precip_mean.tif`  
   - `day85_ndvi_seasonal.tif`  
   - `day85_elevation_slope.tif`  

3. Zonal Statistics Table  
   - `day85_covariates_by_admin.csv` with columns: `admin_unit`, `precip_mean`, `ndvi_mean`, `elevation_mean`, `landcover_mode`.  

4. Integration Notebook  
   - `day85_integration_notebook.ipynb` or `.Rmd` showing how to import exported rasters and merge CSV for modeling.  

5. Analytical Report (`day85_report.md`, 300 words)  
   - Document data sources, preprocessing methods, export workflow, and preliminary insights on covariate distributions.  

6. Reflection (`day85_reflection.md`, 200 words)  
   - Reflect on challenges in GEE asset management, processing quotas, and integrating cloud‐based workflows into local analyses.  

---  

Leveraging Google Earth Engine accelerates access to vast environmental datasets and streamlines covariate preparation for spatial epidemiological modeling.