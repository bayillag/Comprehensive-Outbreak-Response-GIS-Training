# **Day 52 – Resource Mobilization and Logistics Planning**
  
Bloom Level: Evaluate & Create | Duration: 4 hrs  

## Objectives  

- Identify and quantify key resources (personnel, vaccines, PPE, transport) for outbreak response.  

- Develop a logistics plan covering procurement, storage, distribution, and cold‐chain management.  

- Estimate costs and optimize resource allocation under budget and time constraints.  

- Coordinate with stakeholders and map supply chains to anticipate bottlenecks.  

- Establish monitoring indicators to track resource utilization and delivery performance.  

## Agenda  

1. Lecture: Logistics Frameworks (45 min)  
   - Supply chain stages: sourcing, warehousing, transportation, last‐mile delivery  
   - Cold‐chain requirements for vaccines and temperature‐sensitive supplies  
   - Key performance indicators: lead time, fill rate, stock‐out risk  

2. Case Study: FMD Vaccination Campaign Logistics (30 min)  
   - Overview of resource mobilization in past ring‐vaccination effort  
   - Discussion of challenges: terrain, storage capacity, delivery timelines  

3. Group Exercise: Resource Mapping (45 min)  
   - Teams receive a list of supplies, personnel rosters, and regional demand figures  
   - Create a resource matrix and prioritize allocations by risk zone  

4. Interactive Demo: Route Optimization & Scheduling (60 min)  
   - Python: using `PuLP` or `ortools` to optimize vehicle routing  
   - R: `lpSolve` for allocation under capacity and time windows  
   - Generate Gantt chart of supply delivery schedule  

5. Discussion & Q&A (30 min)  
   - Anticipating disruptions: weather, road closures, supply shortages  
   - Stakeholder coordination: roles of government, NGOs, and local partners  
   - Real‐time monitoring: dashboards and mobile reporting  

---

## Exercise Details  

**Data Provided:**  
- `day52_resources.csv`: itemized list of supplies with unit size, cost, storage requirements  
- `day52_demand.csv`: demand estimates by district and risk zone  
- `day52_transport.csv`: vehicle fleet details (capacity, speed, cost per km)  
- `day52_roads.shp`: road network for routing  

**Key Tasks:**  
1. Merge resource and demand tables to compute total quantities per district.  
2. Build a procurement and storage plan, accounting for cold‐chain capacity limits.  
3. Formulate and solve a vehicle routing problem to deliver supplies within time windows.  
4. Develop a delivery schedule (Gantt chart) showing sequence and timing for each route.  
5. Define monitoring indicators (e.g., on‐time delivery rate, stock‐out days) and targets.  

---

## Assignment  

Submit to `assignments/day52/` by Day 53 morning:

1. Logistics Plan Document (`day52_logistics_plan.md`)  
   - 500–600 words describing procurement, warehousing, distribution, and monitoring strategies.  

2. Optimization Script (`day52_routing.py` or `day52_routing.R`)  
   - Annotated code solving vehicle routing and resource allocation problems.  

3. Delivery Schedule (`day52_schedule.png`)  
   - Gantt chart of delivery tasks by vehicle and district.  

4. Cost Summary Table (`day52_costs.csv`)  
   - Total and per‐unit costs for procurement, storage, and transport.  

5. Supply Chain Map (`day52_supply_map.png`)  
   - Map showing routes from central warehouse to district distribution points.  

6. Reflection (`day52_reflection.md`)  
   - 200 words on challenges in logistics planning, data limitations, and stakeholder coordination.
