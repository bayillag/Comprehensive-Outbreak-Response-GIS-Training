# **Day 65 – Early Detection Strategies for Emerging Threats**
  
Bloom Level: Understand & Apply | Duration: 4 hrs  

## Objectives  

- Explain the role of early detection in preventing outbreaks and limiting spread.  
- Compare surveillance modalities: sentinel networks, event-based, syndromic, market, and genomic.  
- Design a risk-based sentinel site network using spatial optimization and population data.  
- Develop a prototype anomaly-detection pipeline for real-time syndromic or market data.  
- Integrate GIS and dashboard outputs to trigger timely field investigations.  

---  

## Agenda  

1. Lecture: Early Detection Frameworks (45 min)  
   - Importance of lead time and threshold definitions  
   - Surveillance modalities and data streams  
   - Trade-offs: sensitivity vs. specificity vs. timeliness  

2. Demo: Event-Based and Genomic Surveillance Tools (30 min)  
   - Python pipeline for syndromic anomaly detection (e.g., Farrington algorithm)  
   - Integrating viral sequence metadata into GIS dashboards  

3. Lab Part 1 – Sentinel Site Network Design (60 min)  
   - Load risk strata map (`day62_risk_map.png`) and livestock density raster  
   - Apply spatial optimization (e.g., p-median) to select N sentinel sites  
   - Validate site coverage against travel-time isochrones  

4. Lab Part 2 – Anomaly Detection Pipeline (45 min)  
   - Ingest `day65_syndromic_reports.csv` and `day65_market_surveillance.csv`  
   - Implement a rolling-window outbreak detection algorithm in Python  
   - Map alerts dynamically and flag threshold breaches  

5. Discussion & Q&A (30 min)  
   - Evaluating false-alarm rates and resource implications  
   - Integrating community reporting and participatory approaches  

---  

## Exercise Details  

**Data Provided:**  
- `day65_risk_map.png`: composite risk strata for the region  
- `day65_livestock_density.tif`: raster of herd density  
- `day65_syndromic_reports.csv`: daily symptom counts by site  
- `day65_market_surveillance.csv`: weekly animal movement and sales records  
- `day65_specimen_sequences.fasta`: pathogen genetic sequences (metadata in `day65_sequences.csv`)  

**Key Tasks:**  
1. Optimize the placement of 15 sentinel sites to maximize high-risk coverage and minimize travel times.  
2. Write a Python script that:  
   - Reads syndromic and market data.  
   - Applies an anomaly detection method to flag unusual increases.  
   - Exports a map of alert locations when thresholds are exceeded.  
3. Build a simple HTML or Jupyter-based dashboard displaying:  
   - Live sentinel site statuses.  
   - Time series of detected alerts.  
   - Links to sequence metadata for genomic signals.  

---  

## Assignment  

Submit to `assignments/day65/` by Day 66 morning:

1. Sentinel Network Plan  
   - `day65_sentinel_plan.md` detailing site selection methodology, coverage analysis, and travel-time isochrones.  

2. Event Detection Pipeline Script  
   - `day65_event_detection.py` with annotations, threshold definitions, and map export routines.  

3. Dashboard Prototype  
   - `day65_dashboard.html` (or Jupyter notebook) integrating live plots, maps, and sequence links.  

4. Alert Map  
   - `day65_alert_map.png` showing flagged sites and dates of alerts.  

5. Analytical Report  
   - `day65_report.md` (400 words) summarizing sentinel design, detection algorithm performance, and integration strategy.  

6. Reflection  
   - `day65_reflection.md` (200 words) on challenges in balancing timeliness vs. false alarms, data interoperability, and next steps for field validation.  

---  

This module equips you to build and operationalize early-warning systems that leverage spatial risk, real-time data, and genomic signals for proactive outbreak prevention.
