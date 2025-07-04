# **Day 12 – Sampling Strategies and Sentinel Sites**
  
Bloom Level: Analyze | Duration: 4 hrs  

## Objectives  

- Differentiate probability (simple random, stratified, cluster) versus non-probability sampling in livestock settings  
- Calculate sample sizes for prevalence estimation and confidence limits in animal populations  
- Establish criteria for selecting and maintaining sentinel surveillance sites (geographic, species, risk factors)  
- Integrate sampling design with operational constraints (logistics, budget, field capacity)  

## Agenda  

1. Lecture: Sampling Principles for Animal Health (45 min)  
   - Sampling frames, sampling units (herd, flock, individual)  
   - Trade-offs: precision, cost, feasibility  

2. Case Study: Sentinel Surveillance in Rift Valley Fever (30 min)  
   - Selection of sentinel herds based on risk maps and population density  
   - Review performance metrics: sensitivity, representativeness  

3. Group Exercise: Designing a Sampling Scheme (45 min)  
   - Scenario: suspected brucellosis in small ruminants across three districts  
   - Teams define sampling strategy (method, sample size, cluster selection)  

4. Interactive Demo: Sample Size Calculations (60 min)  
   - Use R (`epiR::epi.ss`) or Python to compute sample sizes for desired precision  
   - Adjust inputs for expected prevalence, design effect, non-response  

5. Discussion & Q&A (30 min)  
   - Sentinel site maintenance: rotation, data quality checks, community engagement  
   - Adapting sampling plans as outbreaks evolve  

## Exercise Details  

Data Provided:  
- `district_populations.csv` with flock/herd counts per district  
- `risk_score_shapefile.zip` with risk strata for spatial sampling  
- Sampling parameters template (`sampling_template.xlsx`)  

Key Tasks:  
1. Develop a stratified cluster sampling plan for three risk strata.  
2. Compute required sample sizes per stratum, accounting for design effect.  
3. Select and map sentinel sites (latitude/longitude) based on risk and accessibility.  

## Assignment  

Submit to `assignments/day12/` by Day 13 morning:

1. Sampling Plan Document (`day12_sampling_plan.md`)  
   - 400–500 words describing your design rationale, methods, and operational notes  

2. Sample Size Calculations (`day12_sample_size.csv`)  
   - Table with stratum, expected prevalence, sample size, design effect, confidence level  

3. Sentinel Site Map (`day12_sentinel_map.png`)  
   - Georeferenced map showing selected sentinel locations overlaid on risk strata  

4. Reflection (`day12_reflection.md`)  
   - 200 words on challenges in balancing statistical rigor with field constraints and lessons learned