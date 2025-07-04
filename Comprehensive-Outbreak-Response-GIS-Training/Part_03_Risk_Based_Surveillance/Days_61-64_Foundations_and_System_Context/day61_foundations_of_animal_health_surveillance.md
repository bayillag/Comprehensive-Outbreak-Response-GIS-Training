# **Day 61 – Foundations of Animal Health Surveillance**
  
Bloom Level: Understand & Apply | Duration: 4 hrs  

## Objectives  

- Define surveillance objectives: early detection, trend monitoring, and response evaluation.  

- Distinguish passive, active, sentinel, and syndromic surveillance systems and their trade-offs.  

- Identify key data sources, reporting pathways, and stakeholder roles in animal health surveillance.  

- Develop standard case definitions and sampling strategies to ensure representative data.  

- Assess data quality metrics: completeness, timeliness, validity, and acceptability.  

---  

## Agenda  

1. Lecture: Surveillance Concepts (45 min)  
   - Surveillance rationale and objectives  
   - Passive vs. active vs. sentinel vs. syndromic approaches  
   - Data flows, feedback loops, and stakeholder engagement  

2. Demo: System Overview & Tools (30 min)  
   - Walkthrough of a sample surveillance database  
   - Dashboard prototype for report monitoring  

3. Lab Part 1 – Mapping Data Sources (60 min)  
   - Load `day61_sentinel_sites.csv` and `day61_reporting_logs.csv`  
   - Map sentinel sites, veterinary posts, and municipal reporting centers  
   - Diagram data flow from field to central database  

4. Lab Part 2 – Case Definitions & Sampling (45 min)  
   - Draft clear case definitions for two priority diseases (e.g., FMD, Brucellosis)  
   - Design an active surveillance sampling plan (site selection, sample size, frequency)  

5. Discussion & Q&A (30 min)  
   - Address underreporting, resource limitations, and data confidentiality  
   - Strategies to improve community and stakeholder participation  

---  

## Exercise Details  

**Data Provided:**  
- day61_sentinel_sites.csv: Site IDs, locations, service capacity  
- day61_reporting_logs.csv: Historical passive report timestamps and outcomes  
- day61_population_data.xlsx: Livestock counts by district  

**Key Tasks:**  
1. Create a spatial map of sentinel and passive reporting sites in QGIS or Python.  
2. Analyze reporting logs to calculate average delays and reporting completeness by site.  
3. Write standardized case definitions for two diseases, including clinical and lab criteria.  
4. Propose a multi‐stage sampling strategy for active surveillance in high-risk zones, justifying sample sizes.  

---  

## Assignment  

Submit to `assignments/day61/` by Day 62 morning:  

1. Surveillance System Map  
   - `day61_surveillance_map.png` or `.pdf` showing all reporting and sentinel sites with data-flow arrows.  

2. Case Definitions Document  
   - `day61_case_definitions.md` with structured definitions for each disease.  

3. Sampling Plan Report  
   - `day61_sampling_plan.md` detailing objectives, design (cluster/sentinel), sample sizes, and rationale.  

4. Data Quality Assessment  
   - `day61_quality_assessment.md` summarizing completeness, timeliness metrics, and identified gaps.  

5. Reflection  
   - `day61_reflection.md` (200 words) on challenges in system design, data trade-offs, and potential improvements.  

---
