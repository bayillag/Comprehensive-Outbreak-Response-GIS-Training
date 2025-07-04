# **Day 2 – Developing and Using Case Definitions for Animal Disease Outbreaks**
  
Bloom Level: Apply | Duration: 4 hrs  

## Objectives  

- Define suspected, probable, and confirmed case categories in animal health contexts.  
- Draft pathogen- and species-specific case definitions using clinical, laboratory, and epidemiological criteria.  
- Translate definitions into operational filters for line lists and surveillance data.  
- Assess trade-offs between sensitivity and specificity when designing case definitions.  

## Agenda  

1. Lecture: Anatomy of a Case Definition (45 min)  
   - Components: clinical signs, laboratory thresholds, exposure history  
   - Classification levels: suspected, probable, confirmed  

2. Case Study: Avian Influenza in Poultry (30 min)  
   - Review official HPAI case definition document  
   - Debate rationale for clinical vs. lab-based criteria  

3. Group Exercise: Drafting Definitions (45 min)  
   - Scenario: HPAI outbreak in backyard flocks  
   - Teams draft suspected, probable, confirmed definitions with justification  

4. Interactive Demo: Applying Definitions (60 min)  
   - Load mock line list in R/Python/QGIS  
   - Filter and tag cases by category; map spatial patterns  

5. Discussion & Q&A (30 min)  
   - How definition choice affects case counts and resource allocation  
   - Adapting definitions as new evidence emerges  

## Exercise Details  

- Scenario packet includes outbreak background, mixed-case line list, lab results summary.  
- Teams build a table of definitions with explicit inclusion/exclusion criteria.  
- Participants use provided scripts to classify cases and produce category maps.  

## Assignment  

Submit to `assignments/day02_case_definitions/` by Day 3 morning:  

- Case Definitions Document (`day02_definitions.md`)  
  Table listing suspected, probable, and confirmed criteria with brief rationale.  

- Categorized Line List (`day02_categorized_cases.csv`)  
  Original line list augmented with a “case_category” column.  

- Reflection (`day02_reflection.md`)  
  200 words on balancing sensitivity versus specificity and the operational impact on field surveillance.