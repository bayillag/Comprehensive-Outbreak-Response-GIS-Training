# **Day 77 – Visualization & Map Symbology**
  
Bloom Level: Understand & Apply | Duration: 4 hrs  

## Objectives  

- Apply cartographic principles to choose effective color schemes and classification methods.  
- Design clear, accessible symbology for choropleth, proportional symbol, and dot-density maps.  
- Customize map elements: legends, scale bars, north arrows, labels, and insets.  
- Ensure visualizations adhere to accessibility standards (colorblind‐friendly palettes, contrast).  
- Produce polished map layouts ready for reports and presentations.  

---  

## Agenda  

1. Lecture: Cartographic Design Principles (45 min)  
   - Visual variables: color hue, saturation, value, shape, size  
   - Classification methods: equal interval, quantiles, natural breaks, standard deviation  
   - Accessibility considerations: colorblind palettes, legibility, context  

2. Demo: Symbology in QGIS & Python (30 min)  
   - QGIS styling panel: categorized vs. graduated symbology  
   - Python/GeoPandas with Matplotlib: custom color maps and legend creation  
   - Exporting high-resolution maps with embedded elements  

3. Lab Part 1 – Choropleth Mapping (60 min)  
   - Load administrative boundaries and disease incidence data  
   - Experiment with three classification schemes and two color ramps  
   - Add a clear legend, dynamic labels, and descriptive title  

4. Lab Part 2 – Proportional Symbols & Dot Density (45 min)  
   - Overlay proportional symbols for case counts on the choropleth  
   - Design a dot-density layer for population distribution  
   - Position north arrow, scale bar, and inset map  

5. Discussion & Q&A (30 min)  
   - Balancing information density and clarity  
   - Common pitfalls: misclassification, visual bias, over-symbolization  
   - Strategies for consistency across multiple map outputs  

---  

## Exercise Details  

**Data Provided:**  

| File                         | Description                                            |
|------------------------------|--------------------------------------------------------|
| day77_admin.shp              | Administrative boundaries with attributes              |
| day77_incidence.csv          | District-level incidence rates per 1,000 animals       |
| day77_case_points.shp        | Geocoded case locations                                |
| day77_population_raster.tif  | Livestock density raster                               |
| day77_baseline_risk.tif      | Kernel density risk surface                            |

**Key Tasks:**  

1. Import and reproject all layers to a common CRS suitable for map production.  
2. Create three choropleth maps using different classification methods; compare visual outcomes.  
3. Select and apply a colorblind-friendly palette; justify your choice.  
4. Overlay proportional symbols for case counts; size symbols based on a clear scaling function.  
5. Assemble a final map layout including legend, north arrow, scale bar, neatline, and inset.  

---  

## Assignment  

Submit to `assignments/day77/` by Day 78 morning:  

1. Choropleth Comparison (`day77_choropleth_comparison.png`)  
   - Three side-by-side maps with different classification schemes and identical color ramps.  

2. Final Map Layout (`day77_final_map.png`)  
   - Polished map combining choropleth, proportional symbols, labels, and cartographic elements.  

3. Project File or Notebook  
   - `day77_qgis_project.qgz` or `day77_symbology_notebook.ipynb` with styling steps and code.  

4. Symbology Report (`day77_symbology_report.md`)  
   - 300 words on classification choices, color palettes, symbol scaling, and accessibility features.  

5. Reflection (`day77_reflection.md`, 200 words)  
   - Discuss challenges in map design, lessons on visual clarity, and strategies for consistent symbology across projects.  

---  

This session refines your cartographic skills, ensuring your spatial outputs communicate epidemiological patterns with clarity, accuracy, and visual appeal.
