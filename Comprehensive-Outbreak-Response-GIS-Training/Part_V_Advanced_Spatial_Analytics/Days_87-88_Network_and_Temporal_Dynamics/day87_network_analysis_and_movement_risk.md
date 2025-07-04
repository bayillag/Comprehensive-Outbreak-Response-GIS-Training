# **Day 87 – Network Analysis & Movement Risk**
  
Bloom Level: Apply & Evaluate | Duration: 4 hrs  

## Objectives  

- Define transportation and movement networks in epidemiological contexts.  
- Construct and visualize network graphs from spatial road and movement data.  
- Compute network metrics (degree, betweenness, closeness, connectivity) to identify critical nodes and edges.  
- Develop origin–destination (OD) matrices and map movement flows.  
- Integrate network analysis with case locations to highlight high‐risk corridors and potential pathways of spread.  

---  

## Agenda  

1. Lecture: Network Theory & Movement Risk (45 min)  
   - Graph fundamentals: nodes, edges, weights  
   - Relevance to disease spread and surveillance  

2. Demo: Network Construction in QGIS & Python (30 min)  
   - QGIS Network Analysis plugin  
   - Python `networkx` workflows for spatial graphs  

3. Lab Part 1 – Building the Movement Network (60 min)  
   - Load road network (`day87_roads.shp`) and market/village points (`day87_market_points.shp`)  
   - Define nodes and edges; assign distances or travel times  
   - Create `networkx` graph and visualize topology  

4. Lab Part 2 – Metrics & Flow Analysis (45 min)  
   - Compute centrality measures (betweenness, closeness, degree)  
   - Load movement logs (`day87_movement_data.csv`) to build an OD matrix  
   - Map top 10% of flow corridors and identify high‐risk links  

5. Discussion & Q&A (40 min)  
   - Interpreting network metrics for surveillance targeting  
   - Incorporating dynamic movement data and seasonal variation  

---  

## Exercise Details  

**Data Provided:**  

| File                          | Description                                          |
|-------------------------------|------------------------------------------------------|
| day87_roads.shp               | Road centerlines with length and surface attributes  |
| day87_market_points.shp       | Market and village locations (nodes)                 |
| day87_movement_data.csv       | Records: `origin_id`, `dest_id`, `date`, `volume`    |
| day87_admin_units.shp         | Administrative boundaries for mapping context        |
| day87_case_locations.shp      | Geocoded case events for overlay analysis            |

**Key Tasks:**  

1. Reproject all layers to a common CRS and verify topology integrity.  
2. Use QGIS or Python to snap node points to the road network and generate edges.  
3. Build a weighted graph where edge weights reflect travel time or distance.  
4. Calculate centrality metrics for each node and rank the top 5 critical hubs.  
5. Aggregate movement logs into an OD matrix; calculate total flow volumes per edge.  
6. Identify and map the highest‐risk corridors (e.g., top quantile of flow × centrality).  
7. Overlay case locations to assess concordance with identified routes.  

---  

## Assignment  

Submit to `assignments/day87/` by Day 88 morning:  

1. Network Analysis Script  
   - `day87_network_analysis.py` or `day87_network_analysis.R` with code for data import, graph construction, metrics, and OD aggregation.  

2. Network Metrics Table  
   - `day87_network_metrics.csv` containing `node_id`, `degree`, `betweenness`, `closeness`, and `rank`.  

3. Movement Flow Map  
   - `day87_flow_corridors.png` showing top‐ranked corridors overlaid on administrative map.  

4. High‐Risk Network Map  
   - `day87_risk_network.png` highlighting critical nodes and edges by combined risk score.  

5. Analytical Report (`day87_report.md`, 400 words)  
   - Methods, key network findings, implications for surveillance and control, and limitations.  

6. Reflection (`day87_reflection.md`, 200 words)  
   - Discuss challenges in network creation, data quality issues, and how movement insights inform field strategies.  

---  

This session equips you with the tools to harness movement and network data for pinpointing critical transmission pathways and optimizing surveillance interventions.
