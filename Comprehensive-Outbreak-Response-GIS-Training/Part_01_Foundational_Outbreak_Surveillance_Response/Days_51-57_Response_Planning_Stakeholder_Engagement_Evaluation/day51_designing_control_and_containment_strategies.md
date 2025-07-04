# **Day 51 – Designing Control and Containment Strategies**
  
Bloom Level: Evaluate & Create | Duration: 4 hrs  

## Objectives  

- Identify and compare a range of control measures (vaccination, movement restrictions, culling, biosecurity) for animal diseases.  

- Design strategic containment plans using spatial, temporal, and network analysis outputs.  

- Evaluate logistical, economic, and ethical considerations in implementing interventions.  

- Develop monitoring and evaluation metrics to assess the effectiveness of control strategies.  

---  

## Agenda  

1. Lecture: Control Measure Frameworks (45 min)  
   - Types of interventions: prophylactic vs. reactive  
   - Evidence-based decision criteria: R₀, hotspot clusters, network centrality  
   - Trade-offs: speed, coverage, cost, stakeholder acceptance  

2. Case Study: Ring Vaccination vs. Targeted Culling (30 min)  
   - Review published outbreak responses (e.g., FMD, avian influenza)  
   - Compare spatial extents, timing, and resource usage  

3. Group Exercise: Strategy Design Workshop (45 min)  
   - Teams receive a simulated outbreak scenario with maps, R₀ estimates, and network metrics  
   - Draft a multi-pronged control plan: define zones, choose interventions, and allocate resources  

4. Interactive Demo: Optimization & Simulation (60 min)  
   - Use Python or R to simulate intervention impacts on case trajectories (e.g., compartmental models with control parameters)  
   - Map buffer or ring zones around cases and high‐risk nodes  
   - Run simple cost‐effectiveness comparison between strategies  

5. Discussion & Q&A (30 min)  
   - Handling uncertainties and stakeholder trade-offs  
   - Communication plans and community engagement  
   - Monitoring indicators and adaptive management  

---  

## Exercise Details  

**Data Provided:**  
- `day51_cases.geojson`: spatial case locations and times  
- `day51_network_metrics.csv`: node centrality and community labels  
- `day51_costs.xlsx`: unit costs for vaccination, surveillance, movement permits  
- `day51_params.json`: outbreak parameters (R₀, incubation period)  

**Key Tasks:**  
1. Merge spatial and network data to identify priority zones (hotspots, high‐centrality nodes).  
2. Define control zones (e.g., inner buffer for culling, outer ring for vaccination).  
3. Simulate impact of each intervention scenario on case counts over 30 days.  
4. Calculate estimated costs, cases averted, and derive ICERs for each strategy.  

---  

## Assignment  

Submit to `assignments/day51/` by Day 52 morning:  

1. Strategy Design Plan (`day51_strategy.md`)  
   - 500–600 words detailing chosen control measures, zones, and rationale.  

2. Simulation Script (`day51_simulation.py` or `day51_simulation.R`)  
   - Annotated code implementing intervention scenarios and epidemic projections.  

3. Control Zone Map (`day51_control_zones.png`)  
   - Map showing delineated culling and vaccination rings or polygons.  

4. Cost‐Effectiveness Table (`day51_ce_results.csv`)  
   - Costs, cases averted, and incremental cost‐effectiveness ratios for each scenario.  

5. Monitoring & Evaluation Metrics (`day51_me.csv`)  
   - Proposed indicators, data sources, and thresholds for assessing strategy performance.  

6. Reflection (`day51_reflection.md`)  
   - 200 words on challenges in balancing efficacy, cost, and operational feasibility during control planning.  

---
