# **Day 48 – Introduction to Network Analysis for Movement Risk**
  
Bloom Level: Understand & Apply | Duration: 4 hrs  

## Objectives  

- Describe key network concepts: nodes, edges, directed vs. undirected, and edge weights.  
- Construct an animal‐movement network from transaction data.  
- Compute centrality metrics (degree, in/out‐degree, betweenness, eigenvector) to identify high‐risk nodes.  
- Detect communities or clusters of highly connected locations.  
- Visualize movement networks both as abstract graphs and overlaid on maps.  

---  

## Agenda  

1. **Lecture: Network Theory for Epidemiology** (45 min)  
   - Nodes and edges in animal movement context  
   - Directed vs. undirected edges; edge weighting by number of animals  
   - Centrality measures and their epidemiological interpretation  
   - Community detection (e.g., modularity, Louvain)  

2. **Demo: Tools & Workflows** (30 min)  
   - Python: `networkx` for graph construction and metrics  
   - R: `igraph` for centrality and community detection  
   - Overlaying network edges on basemap using GeoPandas or QGIS  

3. **Lab Part 1 – Building the Movement Graph** (60 min)  
   - Load `day48_nodes.csv` (node IDs, coordinates) and `day48_edges.csv` (source, target, count)  
   - Create a directed, weighted graph object  
   - Compute node‐level metrics: degree, in‐degree, out‐degree, betweenness, eigenvector  

4. **Lab Part 2 – Community Detection & Mapping** (45 min)  
   - Apply Louvain or fast‐greedy algorithm to partition the network  
   - Assign community labels to each node  
   - Export node metrics and community membership  
   - Visualize network overlay: lines colored by community, nodes sized by centrality  

5. **Discussion & Q&A** (30 min)  
   - Identifying “super‐spreader” premises based on centrality  
   - Implications of tightly‐connected clusters for targeted interventions  
   - Data quality considerations in movement records  

---  

## Exercise Details  

**Data Provided:**  
- `day48_nodes.csv`: `node_id`, `latitude`, `longitude`  
- `day48_edges.csv`: `from_node`, `to_node`, `animal_count`  
- Optional basemap shapefile: `day48_districts.shp`  

**Key Tasks:**  
1. Merge node coordinates and build a directed graph weighted by `animal_count`.  
2. Calculate centrality metrics for each node and detect communities.  
3. Export a node‐level table with metrics and community labels.  
4. Generate two visual outputs:  
   - Abstract network plot (nodes sized by betweenness, colored by community)  
   - Spatial network map overlaid on administrative boundaries  

---  

## Assignment  

Submit to `assignments/day48/` by Day 49 morning:  

1. Network Script (`day48_network.py` or `day48_network.R`)  
   - Annotated code for graph creation, metric computation, and community detection.  

2. Node Metrics Table (`day48_node_metrics.csv`)  
   - Columns: `node_id`, `degree`, `in_degree`, `out_degree`, `betweenness`, `eigenvector`, `community`.  

3. Visualizations  
   - `day48_network_plot.png` (abstract graph)  
   - `day48_spatial_network.png` (map overlay)  

4. Analytical Report (`day48_report.md`) (300 words)  
   - Interpret key metrics, highlight high‐risk nodes, and discuss community structure implications.  

5. Reflection (`day48_reflection.md`) (200 words)  
   - Challenges in data preparation, metric interpretation, and using network insights for risk management.