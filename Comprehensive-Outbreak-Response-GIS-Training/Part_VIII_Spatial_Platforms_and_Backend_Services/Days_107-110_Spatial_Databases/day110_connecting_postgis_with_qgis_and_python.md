# **Day 110 – Connecting PostGIS with QGIS & Python**  
Bloom Level: Apply & Integrate | Duration: 4 hrs  

## Objectives  

- Establish and manage a PostGIS database connection within QGIS.  
- Load and style PostGIS layers dynamically in QGIS projects.  
- Use Python (psycopg2, SQLAlchemy, GeoPandas) to query, analyze, and update PostGIS data.  
- Automate spatial workflows: read, process, and write back to PostGIS via QGIS’s Python console and standalone scripts.  
- Securely handle database credentials and optimize connection settings for performance.  

---

## Agenda  

1. Lecture: QGIS & PostGIS Integration (45 min)  
   - Data Source Manager and connection parameters  
   - Layer styling and symbology for PostGIS tables  
   - Managing connection profiles and SSL settings  

2. Demo: Python–PostGIS Workflows (30 min)  
   - Using GeoPandas to load spatial tables via SQLAlchemy  
   - Executing SQL commands with psycopg2 for spatial queries  
   - Writing processed GeoDataFrames back to PostGIS  

3. Lab Part 1 – QGIS Project Setup (60 min)  
   - Create a new QGIS project and add a PostGIS connection  
   - Load `cases`, `districts`, and `roads` layers from the database  
   - Apply categorized and graduated symbology based on attributes  
   - Save the project with relative paths and connection reuse  

4. Lab Part 2 – Python Automation (45 min)  
   - Write a standalone Python script:  
     * Connect to PostGIS via SQLAlchemy  
     * Read `cases` table into GeoPandas, compute nearest road distance, add new column  
     * Update the PostGIS `cases` table with computed distances  
   - Use QGIS’s Python console to run a processing algorithm that buffers high-risk areas and saves results to PostGIS  

5. Discussion & Q&A (30 min)  
   - Best practices for long-running queries and batch uploads  
   - Handling geometry SRID mismatches and coordinate transforms  
   - Managing credentials securely (environment variables, `.pgpass`)  

---

## Exercise Details  

| Item                     | Description                                                 |
|--------------------------|-------------------------------------------------------------|
| PostGIS Database         | Contains tables: `cases`, `districts`, `roads`              |
| QGIS Project Template    | `day110_template.qgz` with empty PostGIS connections        |
| Python Script Template   | `day110_postgis_template.py` with connection placeholders   |
| Sample Data              | CSV of new case records to import into PostGIS              |

**Key Tasks:**  

- Configure a PostGIS connection in QGIS’s Data Source Manager.  
- Load, style, and save three spatial layers from PostGIS in a QGIS project.  
- In Python, authenticate to PostGIS, read and modify spatial data, and write updates back.  
- Buffer polygon output from QGIS Processing toolbox and store the result in PostGIS.  

---

## Assignment  

Submit to `assignments/day110/` by Day 111 morning:  

1. QGIS Project  
   - `day110_project.qgz` with established PostGIS connections and styled layers.  

2. Python Automation Script  
   - `day110_postgis_workflow.py` with sections for connection, query, processing, and upload.  

3. Jupyter Notebook  
   - `day110_postgis_notebook.ipynb` demonstrating GeoPandas and psycopg2 operations interactively.  

4. Updated Database Tables  
   - Confirmation (SQL) that `cases` table includes `nearest_road_dist` column and buffered `high_risk_zones`.  

5. Analytical Report (`day110_report.md`, 300 words)  
   - Document connection setup, data retrieval and update processes, styling decisions, and performance tips.  

6. Reflection (`day110_reflection.md`, 200 words)  
   - Discuss challenges in integrating QGIS and Python workflows with PostGIS, credential management, and next steps for automation.  

---

By mastering PostGIS connections in both QGIS and Python, you’ll streamline spatial data management—bridging desktop GIS and code-driven analyses for robust, reproducible epidemiological workflows.
