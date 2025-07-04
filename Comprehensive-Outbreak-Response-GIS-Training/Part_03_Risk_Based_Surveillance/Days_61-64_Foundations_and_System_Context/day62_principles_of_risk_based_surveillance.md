# **Day 62 – Principles of Risk-Based Surveillance**

Bloom Level: Apply & Analyze | Duration: 4 hrs  

## Objectives  

- Define risk-based surveillance and contrast it with passive and active systems.  
- Identify and quantify key risk factors for prioritizing surveillance efforts.  
- Develop a risk scoring framework to stratify regions or populations.  
- Design a targeted sampling protocol based on risk strata.  
- Integrate GIS outputs for optimal allocation of surveillance resources.  

---  

## Agenda  

1. Lecture: Risk-Based Surveillance Concepts (45 min)  
   - Rationale and advantages over uniform sampling  
   - Key steps: risk factor identification, scoring, stratification, protocol design  

2. Demo: Risk Mapping & Prioritization Tools (30 min)  
   - QGIS: weighted overlay of risk layers  
   - Python/R: pandas and GeoPandas for risk scoring and map exports  

3. Lab Part 1 – Risk Factor Analysis (60 min)  
   - Load `day62_risk_factors.csv` and spatial layers (`day62_admin.shp`, `day62_population.tif`)  
   - Normalize and weight each factor (e.g., animal density, proximity to markets, historical cases)  
   - Compute composite risk score per administrative unit  

4. Lab Part 2 – Designing a Risk-Based Sampling Plan (45 min)  
   - Stratify units into high/medium/low risk based on score quantiles  
   - Define sample sizes and visit frequencies for each stratum  
   - Map sampling sites and routes in QGIS  

5. Discussion & Q&A (30 min)  
   - Balancing resource constraints and surveillance sensitivity  
   - Updating risk models as new data arrives  

---  

## Exercise Details  

**Data Provided:**  
- `day62_risk_factors.csv`: columns `admin_code`, `animal_density`, `market_proximity_km`, `past_case_rate`  
- Spatial files: `day62_admin.shp` (boundaries), `day62_population.tif`  
- Historical case points: `day62_cases.geojson`  

**Key Tasks:**  
1. Normalize each risk factor (min–max) and assign expert weights (e.g., 0.4 animal density; 0.3 proximity; 0.3 case history).  
2. Calculate a composite risk score:  
   
| Risk Factor | Weight | Normalization Method |
| :--- | :--- | :--- |
| Animal density | 0.4 | Min–Max |
| Market proximity | 0.3 | Inverse Min–Max |
| Historical case rate| 0.3 | Min–Max |

3. Classify administrative units into high, medium, and low risk (top 25%, middle 50%, bottom 25%).  
4. Develop a sampling protocol:  
   - High-risk: 10% of herds sampled monthly  
   - Medium-risk: 5% quarterly  
   - Low-risk: sentinel site sampling biannually  
5. Produce a risk map with zones and proposed sample sites.  

---  

## Assignment  

Submit to `assignments/day62/` by Day 63 morning:  

1. Risk Scoring Script (`day62_risk_analysis.py` or `day62_risk_analysis.R`)  
   - Annotated code for normalization, weighting, scoring, and classification.  

2. Risk Map (`day62_risk_map.png`)  
   - Choropleth of risk strata with sample-site markers.  

3. Sampling Plan Document (`day62_sampling_plan.md`)  
   - Protocol detailing strata definitions, sample sizes, frequency, and site selection criteria.  

4. Surveillance Protocol Template (`day62_protocol.docx`)  
   - SOP for field teams: data collection forms, chain-of-custody, and data submission procedures.  

5. Reflection (`day62_reflection.md`, 200 words)  
   - Discuss challenges in factor selection, weighting trade-offs, and operationalizing a risk-based approach.  

---  

This session equips you to concentrate surveillance where it matters most, ensuring efficient use of resources and timely detection in high-risk areas.
