# **Day 58 – Present Control & Containment Strategy**
  
Bloom Level: Evaluate & Create | Duration: 4 hrs  

## Objectives  

- Define risk-based control zones (red, orange, green) using case density and movement corridors.  
- Allocate teams, vaccines, and logistics resources per zone in a structured matrix.  
- Integrate GIS risk maps and network analyses to select optimal intervention points.  
- Develop and deliver a map-driven briefing tailored to technical and lay audiences.  
- Establish real-time feedback channels for logistics, communications, and command‐and‐control adjustments.  

---  

## Agenda  

1. Lecture: Control & Containment Frameworks (45 min)  
   - Zoning principles: buffer vs. inner ring vs. surveillance perimeter  
   - Resource allocation strategies and surge capacity planning  
   - GIS outputs (risk surfaces, movement corridors) for targeting interventions  

2. Demo: Map-Driven Briefing Tools (30 min)  
   - Crafting layered maps in QGIS: technical vs. community versions  
   - Slide deck integration: high-impact visuals and call-outs  
   - Live dashboards and feedback forms  

3. Workshop Part 1 – Zoning & Resource Matrix (60 min)  
   - Define red/orange/green boundaries on provided risk map  
   - Populate resource allocation table with teams, vaccines, cold‐chain, vehicles  
   - Peer critique for feasibility  

4. Workshop Part 2 – Briefing Development & Rehearsal (45 min)  
   - Build a 12-slide deck: context, zones, resources, timelines, Q&A prep  
   - Draft speaker notes and lay-person slide annotations  
   - Practice deliverable with peer feedback  

5. Discussion: Feedback Mechanisms & Adaptation (30 min)  
   - Real‐time data flows: field reports, hotline, dashboard alerts  
   - Decision gates and command‐structure updates  
   - Continuous improvement via daily after‐action snapshots  

---  

## Exercise Details  

**Data Provided:**  
- `day58_risk_map.tif`: kernel density surface and case hotspots  
- `day58_corridors.shp`: major movement routes and market nodes  
- `day58_resources.xlsx`: list of teams, vaccine stocks, cold‐chain assets, vehicles  
- `day58_slide_template.pptx`: branded slide master with map placeholders  

**Key Tasks:**  
1. Import risk and corridor layers into QGIS; delineate red, orange, and green zones.  
2. Create a resource allocation matrix by zone, detailing personnel, doses, cold-chain, and transport.  
3. Design two map outputs:  
   - Technical map with zonation, corridor overlays, and sampling points.  
   - Community map with colored zones, icons for vaccination sites, and helpline number.  
4. Develop a 12-slide briefing deck: embed maps, tables, and timelines; add speaker notes.  
5. Simulate delivery of the briefing (5–7 min) and record peer feedback on clarity, pacing, and actionable content.  

---  

## Assignment  

Submit to `assignments/day58/` by Day 59 morning:  

1. Zoning & Resource Plan (`day58_zoning_resources.md`)  
   - Table of zones with definitions and core actions  
   - Resource allocation matrix by zone  

2. GIS Maps  
   - `day58_map_technical.png` (detailed control zones + corridors)  
   - `day58_map_community.png` (simplified public-facing version)  

3. Briefing Materials  
   - Slide deck (`day58_control_strategy.pptx`) with embedded visuals and speaker notes  
   - Q&A anticipation sheet (`day58_QA_anticipation.md`) listing top 5 questions and bullet answers  

4. Feedback Log (`day58_feedback_log.csv`)  
   - Columns: `timestamp`, `source`, `feedback_type`, `action_item`, `owner`  

5. Reflection (`day58_reflection.md`, 200 words)  
   - Discuss challenges in zoning accuracy, resource trade-offs, briefing design, and incorporating real‐time feedback.  

---  

## Reflection  

Reflect on the efficacy of your zoning logic, the realism of resource allocations, and how GIS integrations informed your decisions. Consider how stakeholder feedback can reshape command structures in fast-moving outbreaks.