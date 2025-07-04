# **Day 103 – SQL Fundamentals & psql Interface**
  
Bloom Level: Understand & Apply | Duration: 4 hrs  

## Objectives  

- Explain relational database concepts: tables, rows, columns, primary and foreign keys.  

- Write basic SQL queries using SELECT, WHERE, ORDER BY, and LIMIT clauses.  

- Perform aggregations with GROUP BY, HAVING, and common aggregate functions (COUNT, SUM, AVG).  

- Join multiple tables (INNER, LEFT, RIGHT) to combine related data.  

- Use the psql command-line interface to connect, explore schemas, run scripts, and export results.  

- Create and modify tables, insert and update records, and build simple indexes for performance.  

---  

## Agenda  

1. Lecture: Core SQL Concepts (45 min)  
   - Relational model and normalization basics  
   - Key SQL statements: CREATE, SELECT, INSERT, UPDATE, DELETE  
   - Data types and constraints  

2. Demo: psql CLI Walkthrough (30 min)  
   - Connecting to PostgreSQL (`psql -h … -U …`)  
   - Meta-commands (`\dt`, `\d table`, `\l`) and script execution (`\i`)  
   - Exporting query results to CSV (`\copy`)  

3. Lab Part 1 – Querying & Aggregations (60 min)  
   - Load sample outbreak database (`cases`, `patients`, `locations`)  
   - Select subsets of data with filters (`WHERE`) and sort (`ORDER BY`)  
   - Compute case counts by district and average patient age with `GROUP BY`  

4. Lab Part 2 – Joins & Data Manipulation (45 min)  
   - Join `cases` to `patients` and `locations` via foreign keys  
   - Update patient status flags and insert a new follow-up record  
   - Create an index on `cases.report_date` and compare query plans  

5. Discussion & Q&A (30 min)  
   - Best practices for writing readable, efficient SQL  
   - When to use views, materialized views, and stored procedures  
   - Integrating psql scripts into broader automation workflows  

---  

## Exercise Details  

**Data Provided:**  

| File                         | Description                                                       |
|------------------------------|-------------------------------------------------------------------|
| day103_db.sql                | PostgreSQL dump containing tables: `cases`, `patients`, `locations` |
| day103_queries_template.sql  | Starter SQL file with placeholders for your queries               |
| day103_schema_diagram.png    | Entity-relationship diagram of the loaded database                |

**Key Tasks:**  

- Initialize a local PostgreSQL database by restoring `day103_db.sql`.  

- Connect via psql; list available databases, schemas, and tables using meta-commands.  

- Write and execute SELECT queries to:  
  - Retrieve all cases reported in the last 30 days.  
  - Count cases by district and calculate average severity score.  

- Implement JOINs to:  
  - Link each case to patient demographics and location names.  
  - Produce a combined view of case, patient age, and village.  

- Perform data updates:  
  - Flag all cases older than 60 years with a HIGH_RISK marker.  
  - Insert a new patient record and associate it with a follow-up case.  

- Create an index on `cases(report_date)`; compare execution time of a date-filtered query before and after indexing.  

- Export query results to CSV files using `\copy` for reporting.  

---  

## Assignment  

Submit to `assignments/day103/` by Day 104 morning:  

1. SQL Script (`day103_queries.sql`)  
   - Annotated SQL statements covering SELECT, JOIN, UPDATE, INSERT, and INDEX tasks.  

2. psql Command Log (`day103_psql_commands.txt`)  
   - Chronological list of psql meta-commands and shell commands used.  

3. Query Output CSVs  
   - `cases_last30days.csv`, `cases_by_district.csv`, and `high_risk_patients.csv`.  

4. Updated ER Diagram (`day103_schema_diagram_updated.png`)  
   - Reflect any schema modifications or new relations introduced.  

5. Analytical Report (`day103_report.md`, 300 words)  
   - Summarize methods, key query findings, performance impact of indexing, and insights for epidemiological monitoring.  

6. Reflection (`day103_reflection.md`, 200 words)  
   - Discuss challenges encountered with SQL syntax, psql tooling, and how mastering these skills will support your spatial epidemiology workflows.  

---  

By the end of this session, you’ll be proficient at querying, managing, and exporting relational epidemiological data using SQL and the psql interface—foundational skills for data-driven analyses.
