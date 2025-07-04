# **Day 90 – GIS for Outbreak Decision Support**
  
Bloom Level: Apply & Create | Duration: 4 hrs  

---

## Objectives  

- Describe the role of GIS in real‐time outbreak decision making and situational awareness.  

- Design interactive maps and dashboards to monitor case trends, resource deployment, and intervention impact.  

- Implement geospatial scenario modeling for targeted control measures (e.g., ring vaccination, movement restrictions).  

- Integrate logistics, health‐facility capacity, and travel‐time analyses to optimize response planning.  

- Establish geo‐notification workflows to alert field teams of emerging hotspots and task assignments.  

---

## Agenda  

1. Lecture: GIS in Operational Response (45 min)  
   - Key decision‐support needs: detection, prioritization, resource allocation  
   - Components of a GIS‐enabled command center: data streams, dashboards, mobile apps  

2. Demo: Building Interactive Dashboards (30 min)  
   - QGIS with DataPlotly plugin or Python Dash/Streamlit examples  
   - Embedding real‐time data: case feeds, facility reports, risk layers  

3. Lab Part 1 – Dashboard Prototype Development (60 min)  
   - Load outbreak cases (`day90_cases.shp`), facilities (`day90_facilities.shp`), and admin boundaries  
   - Create an interactive map with filter controls for date, case severity, and facility status  
   - Add panels for summary statistics, time series charts, and capacity gauges  

4. Lab Part 2 – Scenario Mapping & Logistics (45 min)  
   - Import travel‐time raster (`day90_travel_time.tif`) and road network  
   - Model a ring‐vaccination buffer around recent cases and map target zones  
   - Calculate optimal supply‐route from central depot to health facilities using network analysis  

5. Discussion & Q&A (30 min)  
   - Ensuring dashboard usability for non‐GIS stakeholders  
   - Automating data updates and alert workflows  
   - Integrating mobile data collection and offline use  

---

## Exercise Details  

**Data Provided:**  
- `day90_cases.shp`: geocoded case locations with dates and status  
- `day90_facilities.shp`: health posts and hospitals with bed capacity  
- `day90_admin_boundaries.shp`: district and sub‐district polygons  
- `day90_travel_time.tif`: raster of travel time to nearest road  
- `day90_depot.shp`: central logistics depot point  
- `day90_roads.shp`: road network for routing  

**Key Tasks:**  
1. Prepare and reproject all layers into a common CRS.  
2. Develop an interactive dashboard:  
   - Map view with dynamic symbology by case status and date slider  
   - Sidebar charts: daily case counts, facility occupancy rates  
   - Search and pan controls for field teams  
3. Scenario modeling:  
   - Generate ring buffers (e.g., 5 km, 10 km) around new cases to define vaccination zones  
   - Perform least‐cost path analysis from depot to each facility, overlaying on travel‐time raster  
4. Geo‐notification setup (conceptual):  
   - Define triggers (e.g., new hotspot detection) and target teams  
   - Sketch a workflow for dispatching mobile notifications with location links  

---

## Assignment  

Submit to `assignments/day90/` by Day 91 morning:  

1. Decision Support Plan (`day90_plan.md`)  
   - Outline GIS dashboard features, scenario‐modeling approach, and alert workflows.  

2. Dashboard Prototype  
   - `day90_dashboard.html` (or Streamlit app) with map, filters, and charts.  

3. Scenario Maps  
   - `day90_ring_vaccination_zones.png` showing buffer zones.  
   - `day90_supply_routes.png` displaying least‐cost paths.  

4. Resource Allocation Map  
   - `day90_facility_capacity_map.png` mapping bed availability and travel times.  

5. Analytical Report (`day90_report.md`, 400 words)  
   - Summarize methods, dashboard insights, scenario outcomes, and decision‐support recommendations.  

6. Reflection (`day90_reflection.md`, 200 words)  
   - Discuss challenges in real‐time data integration, dashboard usability, and next steps for operationalizing GIS support.  

---  

By the end of this session, you’ll be equipped to build GIS‐based decision tools that empower rapid, data‐driven outbreak response and resource optimization.
