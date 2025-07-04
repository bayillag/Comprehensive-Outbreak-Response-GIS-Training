# **Day 11 – Types of Surveillance—Passive, Active, Syndromic**  
Bloom Level: Analyze | Duration: 4 hrs  

## Objectives  

- Define and distinguish passive, active, and syndromic surveillance in animal health contexts.  
- Compare resource requirements, data quality, and timeliness of each surveillance modality.  
- Select the most appropriate surveillance approach based on outbreak scenario and objectives.  
- Design a hybrid surveillance framework integrating multiple methods.  

## Agenda  

1. Lecture: Surveillance Modalities Overview (45 min)  
   - Passive: routine farm‐ and lab‐based reporting  
   - Active: scheduled field visits and targeted sampling  
   - Syndromic: monitoring clinical syndromes via automated or mobile platforms  
   - Comparison table  

   | Surveillance Type | Data Source                       | Frequency      | Strengths                        | Limitations                             |
   |-------------------|-----------------------------------|----------------|----------------------------------|-----------------------------------------|
   | Passive           | Farmer/lab reports                | Ad hoc         | Low cost, scalable               | Under-reporting; delayed detection      |
   | Active            | Field inspections, sampling teams | Scheduled      | Higher sensitivity; targeted     | Resource-intensive; logistical burden   |
   | Syndromic         | Clinical signs, mobile alerts     | Near real-time | Early warning; broad coverage    | Low specificity; requires validation    |

2. Case Study: Rift Valley Fever Surveillance (30 min)  
   - Contrasting passive lab notifications with community-based active case finding  
   - Syndromic signals captured via mobile reporting  

3. Group Exercise: Scenario-Based Strategy (45 min)  
   - Three contexts: remote pastoral, peri-urban farms, zoonotic spillover  
   - Teams select and justify a surveillance mix, map data flows, define alert triggers  

4. Interactive Demo: Building a Syndromic Filter (60 min)  
   - Configure syndrome definitions (e.g., hemorrhagic signs, neurological symptoms) in Kobo/ODK or R Shiny  
   - Simulate alerts; review sensitivity vs specificity  

5. Discussion & Q&A (30 min)  
   - Balancing speed, cost, and data validity  
   - Adapting surveillance as outbreaks evolve  

---

## Exercise Details  

**Data Provided:**  
- `day11_case_signs.csv`: simulated clinical report dataset with timestamps  
- `scenario_briefs.pdf`: detailed descriptions of three surveillance contexts  

**Key Tasks:**  
1. Complete the surveillance comparison table, noting resource needs and data quality trade‐offs.  
2. Draft brief surveillance plans for each scenario, specifying methods, frequency, data flows, and trigger thresholds.  
3. Build and test a syndromic alert in your chosen tool; capture sample notification outputs.  

---

## Assignment  

Submit to `assignments/day11/` by Day 12 morning:

1. Surveillance Comparison Table (`day11_matrix.md`)  
2. Scenario Surveillance Plans (`day11_plans.md`)  
3. Syndromic Filter Configuration (`day11_filter.json` or `day11_filter.md`)  
4. Reflection (`day11_reflection.md`)  
   - 200 words on practical trade‐offs among surveillance types and their real‐world application.