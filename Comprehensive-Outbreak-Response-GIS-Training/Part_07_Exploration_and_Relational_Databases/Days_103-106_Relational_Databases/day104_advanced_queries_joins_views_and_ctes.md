# **Day 104 – Advanced Queries: Joins, Views & CTEs**  
Bloom Level: Analyze & Apply | Duration: 4 hrs  

## Objectives  

- Distinguish among INNER, LEFT, RIGHT, and FULL OUTER joins and their use cases.  

- Construct and optimize complex subqueries and nested joins for relational data.  

- Create standard and materialized views to encapsulate recurring query logic.  

- Write Common Table Expressions (CTEs), including recursive CTEs, to simplify multi-step queries.  

- Leverage advanced SQL features to streamline spatial data retrieval and reporting.  

---  

## Agenda  

1. Lecture: Advanced Join Types & Query Planning (45 min)  
   - Join algorithms, performance considerations, null handling  

2. Demo: Views & CTE Syntax in psql (30 min)  
   - Defining views and materialized views  
   - Crafting non-recursive and recursive CTEs  

3. Lab Part 1 – Complex Joins & Subqueries (60 min)  
   - Write queries to combine `cases`, `patients`, and `locations` using various join types  
   - Use subselects to compute derived fields (e.g., case-to-population ratios)  

4. Lab Part 2 – Views & CTEs (60 min)  
   - Define a view `vw_case_summary` that aggregates cases by district and age group  
   - Create a materialized view `mv_latest_cases` and refresh it  
   - Develop a recursive CTE to traverse administrative hierarchies from villages up to regions  

5. Discussion & Q&A (25 min)  
   - When to use views vs. CTEs vs. subqueries  
   - Best practices for query readability, maintainability, and indexing  

---  

## Exercise Details  

**Data Provided:**  

| File                              | Description                                                   |
|-----------------------------------|---------------------------------------------------------------|
| `day103_db.sql`                   | PostgreSQL dump with tables: `cases`, `patients`, `locations` |
| `day104_queries_template.sql`     | Starter SQL file with placeholders for advanced queries       |
| `day104_schema_diagram_updated.png` | Updated ER diagram including region hierarchy relationships   |

**Key Tasks:**  

1. Restore `day103_db.sql` into your local PostgreSQL instance.  

2. Use psql to explore table schemas and relationship constraints via meta-commands (`\d`).  

3. Implement and test:  
   - INNER JOIN to list all confirmed cases with patient demographics.  
   - LEFT OUTER JOIN to include locations even if no cases reported.  
   - FULL OUTER JOIN to reveal unmatched patients or locations.  

4. Create `vw_case_summary` as a standard view aggregating case counts and average ages per district.  

5. Build `mv_latest_cases` as a materialized view containing cases in the past 7 days; refresh and benchmark query speed.  

6. Write a recursive CTE to assemble a table of locations with their parent and grandparent administrative units.  

7. Save the results of each major query into separate CSV exports for reporting.  

---  

## Assignment  

Submit to `assignments/day104/` by Day 105 morning:  

1. Advanced SQL Script  
   - `day104_advanced_queries.sql` with annotated sections for each join type, view definition, and CTE.  

2. psql Command Log  
   - `day104_psql_commands.txt` capturing meta-commands, view and CTE creation steps, and export commands.  

3. Query Output CSVs  
   - `joined_cases.csv`, `cases_by_district_view.csv`, `latest_cases_materialized.csv`, `location_hierarchy_cte.csv`.  

4. Views Definition File  
   - `day104_views_definitions.sql` containing `CREATE VIEW` and `CREATE MATERIALIZED VIEW` statements.  

5. Analytical Report (`day104_report.md`, 300 words)  
   - Discuss how advanced joins, views, and CTEs improved query clarity and performance, with examples.  

6. Reflection (`day104_reflection.md`, 200 words)  
   - Reflect on challenges in choosing between views and CTEs, handling recursion, and optimizing complex queries.  

---  

By mastering advanced query techniques, you’ll write clearer, more maintainable SQL that powers efficient spatial and epidemiological analyses across large relational datasets.
