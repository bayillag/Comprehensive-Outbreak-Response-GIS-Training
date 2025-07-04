# **Day 86 – Spatial Data Quality & Metadata**
  
Bloom Level: Understand & Evaluate | Duration: 4 hrs  

## Objectives  

- Define key spatial data quality dimensions: positional accuracy, attribute completeness, logical consistency, lineage, and resolution.  
- Identify and apply metadata standards (ISO 19115, FGDC) for documenting spatial datasets.  
- Perform geometry and topology validation to detect errors (gaps, overlaps, slivers, invalid geometries).  
- Assess attribute integrity: missing values, outliers, code compliance, and domain conformance.  
- Create comprehensive metadata records to ensure data discoverability and reproducibility.  

---  

## Agenda  

1. **Lecture: Data Quality & Metadata Standards** (45 min)  
   - Quality dimensions: accuracy, precision, completeness, consistency, currency, lineage  
   - Overview of ISO 19115 and FGDC metadata schemas  
   - Best practices for capturing data lineage and processing history  

2. **Demo: Quality Checks & Metadata Creation** (30 min)  
   - QGIS: Topology checker and geometry validator tools  
   - Python: using `geopandas`/`shapely` for geometry tests and `fiona` for metadata embedding  
   - Populating metadata templates in Excel  

3. **Lab Part 1 – Geometry & Attribute Validation** (60 min)  
   - Load `day86_admin.shp` and `day86_roads.shp` in QGIS or Python  
   - Check and report:  
     - Invalid geometries (self-intersection, holes)  
     - Unclosed polygon rings  
     - Topological errors (overlaps, gaps)  
   - Assess attribute tables for missing values, out-of-range codes, and inconsistent domains  

4. **Lab Part 2 – Metadata Documentation** (45 min)  
   - Complete the provided metadata template (`day86_metadata_template.xlsx`) for each dataset  
   - Include: title, abstract, keywords, CRS, data lineage, quality statements, contact information  
   - Embed spatial and attribute quality statements in an XML or JSON metadata file  

5. **Discussion & Q&A** (40 min)  
   - Strategies for automating quality validations in scripts and models  
   - Balancing strict quality checks with project timelines  
   - Sharing and maintaining metadata in team environments  

---  

## Exercise Details  

**Data Provided:**  

| File                          | Description                                      |
|-------------------------------|--------------------------------------------------|
| day86_admin.shp               | Administrative boundaries with attributes        |
| day86_roads.shp               | Road network layer                               |
| day86_population.csv          | Population counts by district                    |
| day86_metadata_template.xlsx  | Metadata schema with ISO 19115 fields            |

**Key Tasks:**  

- Reproject all layers to a common CRS and verify coordinate consistency.  
- Run geometry validations and export error reports (e.g., invalid_features.csv).  
- Perform attribute checks: identify nulls in required fields and flag out-of-range values.  
- Populate the metadata template with dataset descriptions, lineage, quality assessments, and usage constraints.  
- Export metadata as an XML or JSON file conforming to ISO 19115 schema.  

---  

## Assignment  

Submit to `assignments/day86/` by Day 87 morning:  

1. **Quality Assessment Report** (`day86_quality.md`)  
   - Summary of data quality findings: geometry errors, attribute issues, and CRS checks.  

2. **Data Validation Script**  
   - `day86_validation.py` or `day86_validation.R` with annotated code for geometry and attribute validations.  

3. **Error Logs**  
   - `day86_geometry_errors.csv` listing feature IDs and error types  
   - `day86_attribute_errors.csv` listing records with missing or invalid attribute values  

4. **Metadata Document**  
   - `day86_metadata.xml` (ISO 19115-compliant) or completed `day86_metadata_template.xlsx`  

5. **Data Inventory Table**  
   - `day86_data_inventory.csv` summarizing each file’s CRS, resolution, feature count, and license  

6. **Reflection** (`day86_reflection.md`, 200 words)  
   - Insights on challenges in ensuring spatial data quality, lessons learned in metadata creation, and next steps for sustainable data management.  

---  

By mastering spatial data quality checks and metadata documentation, you’ll ensure that your geospatial analyses are built on reliable, well-documented datasets—essential for transparent, reproducible epidemiological research.
