# **Day 88 – Time-Series Mapping & Animation**
  
Bloom Level: Apply & Create | Duration: 4 hrs  

## Objectives  

- Load and manage spatial datasets with temporal attributes in QGIS, Python, or R.  

- Design and produce sequences of static maps to depict changes over time.  

- Create animated visualizations (GIFs, MP4s) illustrating spatio‐temporal trends.  

- Develop interactive time‐enabled web maps using Leaflet, Kepler.gl, or QGIS Temporal Controller.  

- Integrate animations into reports and dashboards for compelling storytelling.  

---  

## Agenda  

1. Lecture: Temporal Cartography Fundamentals (45 min)  
   - Principles of time‐series mapping: visual variables, classification consistency, basemap stability  
   - Use cases: epidemic progression, environmental change, intervention tracking  

2. Demo: Animation Tools & Workflows (30 min)  
   - QGIS Temporal Controller and Time Manager plugin  
   - Python Matplotlib/Plotly animation pipelines  
   - R’s `gganimate` and `leaflet.extras2` for interactive timelines  

3. Lab Part 1 – Static Map Series (60 min)  
   - Load `day88_admin.shp` and `day88_case_timeseries.csv`  
   - Join cases by date to boundary layer; verify CRS  
   - Generate a templated map for each time slice with consistent symbology  

4. Lab Part 2 – Animated & Interactive Maps (45 min)  
   - Build a GIF/MP4 showing case distribution evolution over time  
   - Configure a Leaflet or QGIS time‐slider web map for user interaction  

5. Discussion & Q&A (30 min)  
   - Balancing detail and readability in temporal animations  
   - Performance considerations for web‐based maps  
   - Ethical framing of time‐series data (scale, speed, context)  

---  

## Exercise Details  

**Data Provided:**  
- `day88_admin.shp`: administrative boundaries  
- `day88_case_timeseries.csv`: date, district, case_count  
- `day88_raster_series/`: folder of daily risk rasters (`YYYYMMDD.tif`)  
- `day88_basemap.geojson`: roads and waterways for context  

**Key Tasks:**  
1. Import and reproject all layers to a unified CRS.  
2. Join `case_timeseries.csv` to `admin.shp` by date to create a time‐enabled vector layer.  
3. Produce a series of static maps (PNG) for each week in the dataset with uniform classification.  
4. Use a scripting approach (Python or R) to stitch these PNGs into an animated GIF or MP4.  
5. Configure an interactive web map with a time‐slider control to pan through dates.  

---  

## Assignment  

Submit to `assignments/day88/` by Day 89 morning:  

1. Static Map Series  
   - `day88_maps_weekly/` containing `week1.png` through `weekN.png`.  

2. Animation File  
   - `day88_animation.gif` (or `day88_animation.mp4`) showing temporal progression.  

3. Interactive Web Map  
   - `day88_timemap.html` (Leaflet or QGIS export) with time‐slider functionality.  

4. Mapping Script or Project  
   - `day88_mapping.py` or `day88_mapping.R` with annotated code for map generation and animation.  

5. Analytical Report (`day88_report.md`, 300 words)  
   - Describe data preparation, symbology choices, animation workflow, and insights revealed.  

6. Reflection (`day88_reflection.md`, 200 words)  
   - Reflect on challenges in synchronizing symbology, handling performance, and ensuring temporal accuracy.  

---  

By mastering time‐series mapping and animation, you’ll bring spatial data to life—enabling dynamic storytelling of epidemic trends and informing timely decisions.
