# **Day 105 – Functions, Triggers & Stored Procedures**
  
Bloom Level: Analyze & Create | Duration: 4 hrs  

## Objectives  

- Differentiate between SQL functions, triggers, and stored procedures and their use cases.  

- Write PL/pgSQL functions to encapsulate reusable logic (e.g., computing incidence rates or risk scores).  

- Create row‐level and statement‐level triggers to enforce database integrity and automate field population.  

- Develop stored procedures for batch processing tasks such as summary table updates.  

- Test, debug, and document database routines using the psql interface.  

---  

## Agenda  

1. Lecture: Database Routines & Automation (45 min)  
   - Overview of functions vs. stored procedures in PostgreSQL 11+  
   - Trigger types: BEFORE/AFTER INSERT, UPDATE, DELETE  
   - When to push logic into the database for performance and integrity  

2. Demo: Building a PL/pgSQL Function (30 min)  
   - Defining a `calculate_incidence()` function that returns numeric rates  
   - Error handling with `RAISE EXCEPTION` and using `STRICT` parameters  

3. Lab Part 1 – Writing SQL Functions (60 min)  
   - Create a `compute_risk_score(age INT, severity INT) RETURNS NUMERIC` function  
   - Implement a spatial helper function using PostGIS (e.g., `ST_BufferArea(geom, dist)`)  
   - Test functions in psql and verify edge‐case behavior  

4. Lab Part 2 – Triggers & Stored Procedures (45 min)  
   - Define a `cases_before_insert` trigger to auto‐populate the `risk_score` column  
   - Build a stored procedure `update_weekly_summary()` that truncates and repopulates a summary table  
   - Manually invoke the procedure and inspect performance  

5. Discussion & Q&A (30 min)  
   - Debugging functions and trigger recursion pitfalls  
   - Best practices for versioning and documenting database routines  
   - Balancing business logic between application and database layers  

---  

## Exercise Details  

**Data Provided:**  

| File                      | Description                                                        |
|---------------------------|--------------------------------------------------------------------|
| `day105_db.sql`           | PostgreSQL dump with tables: `cases`, `patients`, `locations`, `risk_factors` |
| `day105_routines_template.sql` | Starter PL/pgSQL function, trigger, and procedure definitions     |
| `day105_schema_diagram.png`   | ER diagram including `cases` and `summary_weekly` tables           |

**Key Tasks:**  

1. Restore `day105_db.sql` in your local PostgreSQL instance and explore schemas via `\d`.  

2. In `day105_routines_template.sql`, implement:  
   - A `compute_risk_score(age INT, severity INT)` function with conditional logic.  
   - A PostGIS helper function to calculate polygon buffer areas (`BUFFER_AREA(geom, meters)`).  

3. Create a trigger `set_case_risk` on table `cases` that calls `compute_risk_score` before insert.  

4. Define a stored procedure `update_weekly_summary()` that:  
   - Truncates `summary_weekly`.  
   - Aggregates new case counts, average risk scores per district, and inserts into `summary_weekly`.  

5. Test each routine in psql:  
   - Insert sample rows to fire the trigger.  
   - Call `update_weekly_summary()` and measure execution time.  

---  

## Assignment  

Submit to `assignments/day105/` by Day 106 morning:  

1. SQL Routine Script  
   - `day105_functions_triggers.sql` containing annotated `CREATE FUNCTION`, `CREATE TRIGGER`, and `CREATE PROCEDURE` statements.  

2. psql Command Log  
   - `day105_psql_commands.txt` listing all psql commands used to create, test, and invoke routines.  

3. Routine Summary Document  
   - `day105_routines_summary.md` describing each function, trigger, and procedure, its parameters, return types, and purpose.  

4. Test Output CSVs  
   - `day105_trigger_test.csv` showing inserted case records with computed risk scores.  
   - `day105_weekly_summary.csv` exporting the contents of `summary_weekly` after procedure execution.  

5. Analytical Report (`day105_report.md`, 300 words)  
   - Discuss how moving logic into database routines improves data integrity, performance considerations, and maintenance.  

6. Reflection (`day105_reflection.md`, 200 words)  
   - Reflect on challenges in PL/pgSQL syntax, debugging triggers, and strategies for documenting database code.  

---  

By mastering functions, triggers, and stored procedures, you’ll embed critical logic within your database—ensuring consistent, performant, and maintainable spatial epidemiology workflows.
