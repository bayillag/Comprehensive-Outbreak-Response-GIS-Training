# **Day 4 – Descriptive Epidemiology—Animal, Place, Time**
  
Bloom Level: Apply | Duration: 4 hrs  

## Objectives  

- Calculate species-specific case counts and incidence rates over time.  
- Map case distributions by location and animal species.  
- Construct epidemic curves stratified by species and temporal units (day, week).  
- Interpret spatial patterns and temporal trends to inform hypotheses.  

## Agenda  

1. Lecture: Principles of Descriptive Epidemiology (45 min)  
   - Components: animal (species, age), place (farm, zone), time (date of onset)  
   - Choosing appropriate denominators for rate calculations  

2. Demo: Epi-Curves & Stratified Analyses (30 min)  
   - Using R (`ggplot2`) or Python (`matplotlib/seaborn`) to plot curves by species  
   - Generating summary tables of incidence rates  

3. Lab Part 1 – Temporal Analysis (60 min)  
   - Load line list into R/Python; aggregate cases by species and time period  
   - Create species-specific epidemic curves and calculate peak incidence  

4. Lab Part 2 – Spatial Mapping (45 min)  
   - Import case data and administrative boundaries into QGIS or `geopandas`  
   - Produce choropleth maps of incidence rates by zone and species  

5. Discussion & Q&A (30 min)  
   - Insights from combining animal, place, and time dimensions  
   - Limitations of descriptive analyses in outbreak settings  

## Exercise Details  

- **Data Provided:** `day04_linelist.csv` with fields: `case_id`, `species`, `farm_id`, `latitude`, `longitude`, `onset_date`, `population_at_risk`  
- **Key Tasks:**  
  - Compute daily and weekly case counts per species.  
  - Calculate incidence rates (cases per 1,000 animals) for each zone.  
  - Generate epidemic curves and maps highlighting hotspots.  

## Assignment  

Submit to `assignments/day04/` by Day 5 morning:

1. **Epidemic Curves & Rate Tables** (`day04_epi_curves.png`, `day04_rates.csv`)  
   - Plots stratified by species; CSV with time-period counts and incidence rates.  

2. **Incidence Maps** (`day04_incidence_maps.png`)  
   - Choropleth showing species-specific incidence rates per zone.  

3. **Descriptive Report** (`day04_report.md`)  
   - 300–400 words interpreting temporal peaks, species differences, and spatial patterns.  

4. **Reflection** (`day04_reflection.md`)  
   - 200 words on challenges in descriptive mapping and lessons for hypothesis generation.