# **Day 49 – Temporal Mapping and Time-Series Animations**
  
Bloom Level: Create & Apply | Duration: 4 hrs  

## Objectives  

- Integrate spatial and temporal data to produce dynamic visualizations of case progression.  
- Configure time-enabled layers in QGIS using the Time Manager plugin.  
- Generate time-series animations in Python with Matplotlib, Plotly, or Folium.  
- Customize animation parameters (frame rate, color ramps, basemaps) for clarity.  
- Export and embed animations in reports and dashboards.  

---

## Agenda  

1. Lecture: Principles of Temporal Mapping (45 min)  
   - Why animate? Conveying outbreak dynamics  
   - Data requirements: time stamps, consistent CRS, temporal resolution  
   - Animation parameters: duration, speed, interpolation  

2. Demo: QGIS Time Manager Workflow (30 min)  
   - Installing and configuring the Time Manager plugin  
   - Preparing vector/point layers with date fields  
   - Styling temporal transitions and exporting GIF/MP4  

3. Lab Part 1 – QGIS Temporal Map (60 min)  
   - Load `day49_cases.geojson` with `date` and `admin_code`  
   - Define time settings: time format, frame length, aggregation  
   - Style point symbology and add basemap  
   - Export a 30-second MP4 time-series animation  

4. Lab Part 2 – Python Animation (45 min)  
   - Load spatial data with GeoPandas and time series of case counts  
   - Use Matplotlib’s `FuncAnimation` to plot maps per time slice  
   - Optionally create a Plotly animated choropleth or Folium time slider  
   - Save output as `day49_animation.gif` or `day49_animation.html`  

5. Discussion & Q&A (30 min)  
   - Comparing tools: interactivity vs. ease of export  
   - Handling large datasets and performance tuning  
   - Best practices for embedding animations in presentations  

---

## Exercise Details  

**Data Provided:**  
- `day49_cases.geojson`: case locations with attributes `admin_code`, `date`, and `case_count`.  
- `day49_admin.shp`: administrative boundaries with lookup field `admin_code`.  
- `day49_timeseries.csv`: aggregated daily counts per admin unit.  

**Key Tasks:**  
1. Ensure all spatial layers share a common CRS (e.g., EPSG:3857) and temporal field is parsed correctly.  
2. In QGIS: configure Time Manager, set up a step of one day, and style cases by count.  
3. Export the animation at 12 frames per second, 30 seconds total duration.  
4. In Python: load data, iterate over sorted unique dates, update the map per frame, and generate an animation.  
5. Evaluate both outputs for smoothness, readability, and temporal accuracy.  

---

## Assignment  

Submit to `assignments/day49/` by Day 50 morning:

1. QGIS Project File  
   - `day49_project.qgz` with Time Manager settings saved.  

2. Python Animation Script  
   - `day49_animation.py` (or Jupyter notebook) with annotated steps using Matplotlib or Plotly.  

3. Animation Files  
   - `day49_time_series.mp4` (from QGIS)  
   - `day49_animation.gif` or `day49_animation.html` (from Python)  

4. Analytical Report (`day49_report.md`) (300 words)  
   - Compare both workflows, discuss tool strengths/limitations, and recommend contexts for each.  

5. Reflection (`day49_reflection.md`) (200 words)  
   - Reflect on data preparation challenges, animation customization, and effective communication of temporal patterns.  

---
