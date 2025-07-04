# **Day 83 – Spatial Risk Assessment using QGIS**
  
Bloom Level: Apply & Create | Duration: 4 hrs  

## Objectives  

- Define spatial risk assessment and its role in targeting interventions.  

- Identify and prepare hazard, exposure, and vulnerability layers for analysis.  

- Apply weighted overlay and raster calculator tools in QGIS to generate composite risk surfaces.  

- Validate risk maps against case‐point data and expert‐elicited thresholds.  

- Produce a prioritized risk map to guide surveillance and resource allocation.  

---  

## Agenda  

1. Lecture: Spatial Risk Assessment Concepts (45 min)  
   - Framework: hazard × exposure × vulnerability  
   - Data normalization and weighting principles  
   - Uses in epidemiology and One Health contexts  

2. Demo: QGIS Weighted Overlay & Raster Calculator (30 min)  
   - Loading and styling rasters  
   - Building and running a raster calculator expression  
   - Automating overlays with the Processing Modeler  

3. Lab Part 1 – Input Layer Preparation (60 min)  
   - Import and reproject hazard, exposure, and vulnerability layers  
   - Normalize each raster to a 0–1 scale using the ‘Raster calculator’  
   - Define and document weight schema in a CSV  

4. Lab Part 2 – Composite Risk Surface Generation (45 min)  
   - Execute a weighted overlay in QGIS Processing Toolbox  
   - Classify the output into low, medium, and high‐risk zones  
   - Style each class with a clear, colorblind‐friendly palette  

5. Discussion & Q&A (30 min)  
   - Interpreting and communicating risk map outputs  
   - Validation approaches with case data and expert review  
   - Limitations and ethical considerations in risk mapping  

---  

## Exercise Details  

**Data Provided:**  

| File                           | Description                                             |
|--------------------------------|---------------------------------------------------------|
| day83_hazard.tif               | Raster of environmental hazard intensity                |
| day83_exposure.tif             | Raster of livestock density                             |
| day83_vulnerability.tif        | Raster of socioeconomic vulnerability indices           |
| day83_case_points.shp          | Geocoded disease case locations                         |
| day83_weights.csv              | Weight values for each raster layer (hazard, exposure, vulnerability) |
| day83_admin_boundaries.shp     | Administrative units for final map layout               |

**Key Tasks:**  

1. Reproject all rasters and vector layers to a common CRS (e.g., UTM).  

2. Use the QGIS Raster Calculator to normalize each input raster (min–max scaling).  

3. Import `day83_weights.csv` and apply the weights in a weighted‐sum overlay (Processing → Raster → Weighted sum).  

4. Classify the composite risk surface into three strata (quantile or Jenks) and apply symbology.  

5. Overlay `day83_case_points.shp` to assess concordance between high‐risk zones and actual cases.  

6. Export intermediate normalized rasters and the final composite risk layer.  

---  

## Assignment  

Submit to `assignments/day83/` by Day 84 morning:  

1. Risk Assessment Report  
   - `day83_risk_report.md` (300 words) documenting data preparation, weight rationale, methods, and key findings.  

2. QGIS Project  
   - `day83_risk_assessment.qgz` containing all layers, symbology, and processing history.  

3. Composite Risk Map  
   - `day83_composite_risk_map.png` showing low/medium/high risk strata with legend and scale bar.  

4. Validation Map  
   - `day83_validation_map.png` overlaying case points on the risk strata to illustrate predictive performance.  

5. Data Workflow Documentation  
   - `day83_workflow.md` or flowchart describing each processing step, inputs, and outputs.  

6. Reflection  
   - `day83_reflection.md` (200 words) on challenges in weighting decisions, validation trade‐offs, and next steps for operational use.  

---  

By completing this session, you will be able to transform multiple spatial datasets into an actionable risk surface, ready to inform targeted surveillance and intervention strategies.
