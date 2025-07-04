# **Day 63 – Essentials of Surveillance Evaluation**
  
Bloom Level: Evaluate & Analyze | Duration: 4 hrs  

## Objectives  

- Explain the purpose and framework of surveillance system evaluation.  
- Calculate core performance metrics: sensitivity, predictive value positive, timeliness, and completeness.  
- Assess qualitative attributes: simplicity, flexibility, acceptability, stability.  
- Synthesize quantitative and qualitative findings into actionable recommendations.  
- Design an evaluation report and dashboard to guide system improvements.  

---

## Agenda  

1. Lecture: Evaluation Principles (45 min)  
   - Why evaluate? Uses and stakeholders  
   - CDC attributes: sensitivity, PVP, timeliness, completeness, simplicity, flexibility, acceptability, stability  
   - Interpreting metrics in context  

2. Demo: Metrics in Action (30 min)  
   - Python/R: computing sensitivity and PVP from case data  
   - Visualizing timeliness and completeness distributions  
   - Charting qualitative scores with radar/spider plots  

3. Lab Part 1 – Quantitative Analysis (60 min)  
   - Load `day63_surveillance_data.csv` (true cases vs. detected) and `day63_reporting_delays.csv`  
   - Compute sensitivity = detected/true, PVP = true positives/(reported positives)  
   - Calculate median reporting delay and percentage of reports within target window  
   - Summarize completeness by site and week  

4. Lab Part 2 – Qualitative Assessment (45 min)  
   - Load `day63_system_survey.csv` with stakeholder ratings on simplicity, flexibility, etc.  
   - Normalize scores and plot a radar chart of system attributes  
   - Identify strengths and weaknesses  

5. Discussion & Q&A (30 min)  
   - Balancing quantitative and qualitative insights  
   - Prioritizing recommendations under resource constraints  
   - Planning follow‐up evaluation cycles  

---

## Exercise Details  

**Data Provided:**  
- `day63_surveillance_data.csv`: weekly counts of true cases and reported cases by district.  
- `day63_reporting_delays.csv`: individual records with date of onset and date of report.  
- `day63_system_survey.csv`: Likert‐scale survey of 50 field staff on system attributes.  

**Key Tasks:**  
1. Compute system sensitivity and predictive value positive per district.  
2. Calculate timeliness metrics: mean, median, and proportion within 48-hour target.  
3. Assess completeness: percent of expected weekly reports received.  
4. Aggregate survey responses and normalize attribute scores (0–1 scale).  
5. Visualize metrics in tables, line plots (delays), and a radar chart.  

---

## Assignment  

Submit to `assignments/day63/` by Day 64 morning:  

1. Evaluation Script (`day63_evaluation.py` or `day63_evaluation.R`)  
   - Annotated code for metric calculations and plots.  

2. Performance Metrics Table (`day63_metrics.csv`)  
   - Columns: `district`, `sensitivity`, `PVP`, `median_delay`, `completeness`.  

3. Radar Chart (`day63_radar.png`)  
   - Visual of normalized scores for simplicity, flexibility, acceptability, stability.  

4. Evaluation Report (`day63_report.md`, 400 words)  
   - Introduction, methods, results, attribute assessment, and prioritized recommendations.  

5. Improvement Plan (`day63_improvement_plan.md`)  
   - 200-word action plan with timelines and responsible parties to address performance gaps.  

6. Reflection (`day63_reflection.md`, 200 words)  
   - Discuss challenges in metric interpretation, survey collection, and translating findings into practice.  

---
