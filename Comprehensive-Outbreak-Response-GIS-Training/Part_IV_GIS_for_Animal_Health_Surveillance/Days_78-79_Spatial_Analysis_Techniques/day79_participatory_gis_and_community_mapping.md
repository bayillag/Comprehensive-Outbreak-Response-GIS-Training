# **Day 79 – Participatory GIS & Community Mapping**
  
Bloom Level: Create & Evaluate | Duration: 4 hrs  

## Objectives  

- Explain principles and ethics of participatory GIS and community mapping.  
- Facilitate community-driven mapping exercises to elicit local knowledge of risks and resources.  
- Georeference and digitize community‐drawn sketch maps into GIS layers.  
- Validate participatory data against official datasets and integrate insights into spatial analyses.  
- Use community maps to inform targeted interventions and resource allocation.  

---  

## Agenda  

1. Lecture: Participatory GIS Fundamentals (45 min)  
   - Concepts: volunteered geographic information, power dynamics, data ownership  
   - Ethical considerations: informed consent, anonymity, benefit sharing  

2. Demo: Georeferencing & Digitizing Scanned Maps (30 min)  
   - Importing scanned sketch maps in QGIS  
   - Using control points to align community sketches with basemap  
   - Digitizing features and assigning attributes  

3. Lab Part 1 – Community Map Processing (60 min)  
   - Load `day79_basemap.tif` and `day79_scanned_maps.zip` (village sketches)  
   - Georeference each sketch using ground control points  
   - Digitize key features (water sources, grazing areas, meeting points) into separate layers  

4. Lab Part 2 – Validation & Integration (45 min)  
   - Import `day79_official_features.shp` (roads, administrative boundaries)  
   - Spatially compare and reconcile community‐digitized layers with official data  
   - Attribute participatory layers with metadata: mapper, date, confidence level  

5. Discussion & Q&A (40 min)  
   - Triangulating community insights and technical data  
   - Ensuring community ownership and feedback loops  
   - Leveraging participatory maps for intervention planning  

---  

## Exercise Details  

**Data Provided:**  
- day79_basemap.tif: blank georeferenced village map  
- day79_scanned_maps.zip: scanned PDF sketches from focus groups  
- day79_official_features.shp: roads, administrative boundaries, waterpoints  
- day79_participant_log.csv: mapper IDs, village names, session notes  

**Key Tasks:**  
1. Georeference each scanned sketch by matching 5+ identifiable ground control points on the basemap.  
2. Create vector layers for community‐identified features (e.g., water sources, grazing zones, high‐risk areas).  
3. Attach attributes to each feature: `feature_type`, `source` (participant ID), and `confidence_rating`.  
4. Perform spatial overlay with official features to identify concordance and discrepancies.  
5. Prepare a composite participatory‐community map highlighting unique community insights.  

---  

## Assignment  

Submit to `assignments/day79/` by Day 80 morning:  

1. Participatory GIS Plan (`day79_participatory_plan.md`)  
   - Description of facilitation methods, ethical protocols, and data‐flow steps.  

2. Georeferenced Sketch Layers  
   - `day79_community_water.shp`, `day79_grazing_zones.shp`, `day79_risk_areas.shp` with attribute tables.  

3. Composite Participatory Map (`day79_composite_map.png`)  
   - Basemap showing overlaid community features and official layers, with legend.  

4. Analytical Report (`day79_report.md`, 400 words)  
   - Methods, key participatory findings, validation results, and implications for interventions.  

5. Reflection (`day79_reflection.md`, 200 words)  
   - Discuss challenges in community engagement, georeferencing accuracy, and integrating local knowledge with formal datasets.  

---  

By embedding community voices into GIS, this module ensures spatial analyses reflect lived realities and empowers stakeholders in decision‐making.
