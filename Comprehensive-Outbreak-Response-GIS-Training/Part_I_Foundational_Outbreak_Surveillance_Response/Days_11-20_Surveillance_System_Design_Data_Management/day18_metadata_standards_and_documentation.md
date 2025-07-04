# **Day 18 – Metadata Standards and Documentation**
  
Bloom Level: Understand & Apply | Duration: 4 hrs  

## Objectives  

- Explain the role of metadata in ensuring data discoverability, reuse, and interoperability.  
- Compare key metadata standards (e.g., Dublin Core, ISO 19115, DataCite) for epidemiological and spatial datasets.  
- Draft a machine-readable data dictionary and README to accompany outbreak data.  
- Implement metadata annotations in CSV, JSON, and spatial files using common conventions.  

---

## Agenda  

1. Lecture: Metadata Principles & Standards (45 min)  
   - Definitions: provenance, versioning, attribution, licensing  
   - Overview of Dublin Core, ISO 19115 (spatial), and DataCite schema  

2. Case Study: Documenting a Rift Valley Fever Dataset (30 min)  
   - Review an open-access animal health dataset with full metadata  
   - Discuss how metadata supports reproducibility and integration  

3. Group Exercise: Metadata Schema Design (45 min)  
   - Teams receive a raw line list and shapefile without metadata  
   - Define mandatory and recommended metadata fields (title, abstract, creator, date, spatial extent, variable definitions)  

4. Interactive Demo: Creating a Data Dictionary & README (60 min)  
   - Build a markdown-based data dictionary for tabular fields  
   - Annotate a GeoJSON file with ISO 19115 tags  
   - Prepare a README.md outlining file descriptions, usage instructions, and licensing  

5. Discussion & Q&A (30 min)  
   - Balancing thoroughness with usability in metadata  
   - Strategies for automated metadata extraction and validation  

---

## Exercise Details  

**Data Provided:**  
- `day18_raw_linelist.csv` (no header descriptions)  
- `day18_cases.geojson` (lacks properties documentation)  
- Metadata template (`metadata_template.xlsx`)  

**Key Tasks:**  
1. Draft a metadata schema listing core terms and their definitions.  
2. Populate the provided template with per-field descriptions, data types, units, and valid ranges.  
3. Add metadata blocks to the GeoJSON’s `properties` section using ISO 19115 conventions.  
4. Write a README.md that explains file contents, update history, and contact information.  

---

## Assignment  

Submit to `assignments/day18/` by Day 19 morning:

1. **Metadata Schema** (`day18_metadata_schema.md`)  
   - Markdown table with metadata fields, descriptions, and standard mappings.  

2. **Completed Metadata Template** (`day18_metadata_template.xlsx`)  
   - Spreadsheet populated with field-level metadata for the CSV and GeoJSON.  

3. **Annotated GeoJSON** (`day18_cases_annotated.geojson`)  
   - Original file extended with ISO 19115-style metadata in the `properties` header.  

4. **README Document** (`day18_README.md`)  
   - Overview of dataset, file descriptions, instructions for use, licensing, and version history.  

5. **Reflection** (`day18_reflection.md`)  
   - 200 words on the challenges of metadata creation in outbreak settings and the benefits for downstream users.