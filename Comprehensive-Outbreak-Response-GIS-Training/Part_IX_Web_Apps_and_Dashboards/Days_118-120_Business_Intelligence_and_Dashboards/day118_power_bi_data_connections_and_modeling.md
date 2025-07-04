# **Day 118 – Power BI: Data Connections & Modeling**  

Bloom Level: Understand & Apply | Duration: 4 hrs  

---  

## Objectives  

- Connect to diverse data sources (Excel, CSV, SQL databases, web APIs) within Power BI Desktop.  
- Clean and transform datasets using Power Query Editor and M functions.  
- Design a robust data model: define relationships, cardinality, and adopt star schema principles.  
- Create calculated columns and measures using DAX fundamentals (SUM, CALCULATE, FILTER).  
- Optimize performance through query folding techniques and configure incremental data refresh.  

---  

## Agenda  

1. Lecture: Power BI Architecture & Modeling Concepts (45 min)  
   - Overview of data ingestion pipeline, Query Editor, and the in-memory data model  
   - Star schema design, relationship types, and filter directions  

2. Demo: Establishing Data Connections & Transformations (30 min)  
   - Importing Excel workbooks, CSV files, and SQL Server tables  
   - Applying transformations: renaming columns, changing data types, merging and appending queries  

3. Lab Part 1 – Data Cleaning in Power Query (60 min)  
   - Remove errors and empty rows, split complex fields, and extract date components  
   - Build parameterized queries and custom M functions for reusable transformations  

4. Lab Part 2 – Building the Data Model & DAX Measures (45 min)  
   - Define one-to-many relationships with appropriate cardinality and cross-filtering  
   - Create calculated columns (e.g., region classification) and measures (e.g., cases per population)  

5. Discussion & Q&A (30 min)  
   - Best practices: enabling query folding, setting up incremental refresh policies  
   - Collaboration workflows: versioning PBIX files and publishing to Power BI Service  

---  

## Exercise Details  

**Data & Resources Provided:**  

| Resource                          | Description                                                   |
|-----------------------------------|---------------------------------------------------------------|
| day118_powerbi_template.pbix      | Starter Power BI file with sample tables and preliminary layout |
| epidemiology_data.xlsx            | Excel workbook containing raw case, location, and date tables |
| sqlconnection_info.txt            | Server name, database, and credential details for SQL import  |

**Key Tasks:**  

- Open the provided PBIX template and connect to `epidemiology_data.xlsx`.  
- In Query Editor, clean each table: remove nulls, split concatenated fields, and add index columns.  
- Establish a live connection to the sample SQL database; import lookup tables while preserving query folding.  
- In Model view, set up relationships among Cases, Regions, and Time tables with correct cross-filter directions.  
- Write DAX calculated columns for case severity categories and measures for total cases, incidence rate, and rolling averages.  
- Configure an incremental refresh policy on the Cases table to load historical data monthly.  

---  

## Assignment  

Submit to `assignments/day118/` by Day 119 morning:  

1. Power BI File  
   - `day118_modeling.pbix` containing all data connections, transformations, model definitions, and DAX measures.  

2. Query Transformation Steps  
   - `day118_query_steps.md` listing each applied step in Power Query with concise descriptions.  

3. Data Model Diagram  
   - `day118_model_diagram.png` illustrating tables, relationships, cardinality, and filter directions.  

4. DAX Expressions  
   - `day118_dax_measures.md` cataloging all DAX formulas along with a brief rationale for each.  

5. Analytical Report (`day118_report.md`, 300 words)  
   - Document your cleansing process, model design decisions, performance optimizations, and measure outcomes.  

6. Reflection (`day118_reflection.md`, 200 words)  
   - Reflect on challenges faced in data modeling and DAX authoring, and discuss how Power BI enhances your spatial epidemiology workflows.  

---  

Harnessing Power BI’s data connectivity and modeling capabilities will streamline your analytics pipeline—transforming raw epidemiological data into actionable, performant dashboards.
