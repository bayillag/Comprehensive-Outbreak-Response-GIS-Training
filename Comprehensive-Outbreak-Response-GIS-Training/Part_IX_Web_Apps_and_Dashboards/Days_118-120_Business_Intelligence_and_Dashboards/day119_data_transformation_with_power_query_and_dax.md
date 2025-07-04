# **Day 119 – Data Transformation with Power Query & DAX**  

Bloom Level: Understand & Apply | Duration: 4 hrs  

---  

## Objectives  

- Use Power Query Editor to perform complex data shaping tasks (merge, append, pivot, unpivot).  

- Write and optimize custom M functions for reusable transformations and parameterized queries.  

- Implement error handling and data validation steps in M (e.g., `try … otherwise`, `Table.Schema`).  

- Create calculated tables and columns using DAX to support dynamic segmentation and what-if scenarios.  

- Develop advanced DAX measures leveraging time-intelligence, filter context, and statistical functions.  

- Integrate transformed datasets into the Tabular model and prepare for reporting.  

---  

## Agenda  

1. Lecture: Advanced Power Query Techniques (45 min)  
   - Query dependencies and performance implications  
   - Custom columns vs. M functions, invoking parameter queries  

2. Demo: M Language Patterns (30 min)  
   - Writing `let`/`in` blocks, `Table.Group`, `Table.Pivot`, and record transformations  
   - Handling errors and nulls programmatically  

3. Lab Part 1 – Power Query Transformations (60 min)  
   - Merge case and location tables, extract year/month, unpivot category fields  
   - Create a parameterized query to filter by date range and region  
   - Author a reusable M function for currency conversion or unit standardization  

4. Lab Part 2 – DAX Calculations & Tables (45 min)  
   - Build a calculated table for rolling 12-month summaries  
   - Write DAX calculated columns for severity bands and risk categories  
   - Develop measures for cumulative totals, moving averages, and YOY comparisons  

5. Discussion & Q&A (30 min)  
   - Balancing transformations in Power Query vs. DAX for performance  
   - Query folding opportunities and limitations  
   - Version control and documentation of M scripts and DAX formulas  

---  

## Exercise Details  

| Resource                         | Description                                                            |
|----------------------------------|------------------------------------------------------------------------|
| `day119_powerquery_template.pbix`| Power BI file with raw tables and blank Query Editor steps             |
| `epidemic_data.xlsx`             | Excel workbook containing raw case, demographics, and geography sheets |
| `day119_parameters.xlsx`         | Parameter table for date ranges and region codes                        |
| `day119_dax_template.pbix`       | PBIX with data model and placeholder for DAX calculated tables/measures |

**Key Tasks:**  

- In Power Query:  
  - Merge the case and demographics sheets on a common ID.  
  - Unpivot symptom and outcome columns into attribute–value pairs.  
  - Group by region and month to calculate aggregated counts.  
  - Create a parameterized query using the `day119_parameters.xlsx` table.  
  - Write a custom M function for unit conversion (e.g., from per-100k to raw counts).  

- In the data model:  
  - Build a calculated table `RollingStats` that computes a 12-month moving window of case counts per region.  
  - Add calculated columns for severity banding (`Low`, `Medium`, `High`) based on thresholds.  
  - Develop DAX measures:  
    * `TotalCases = SUM(Cases[CaseCount])`  
    * `RollingAverage = AVERAGEX(VALUES(RollingStats[Month]), RollingStats[CaseCount])`  
    * `YOYChange = DIVIDE([TotalCases] – CALCULATE([TotalCases], SAMEPERIODLASTYEAR(Dates[Date])), CALCULATE([TotalCases], SAMEPERIODLASTYEAR(Dates[Date])))`  

---  

## Assignment  

Submit to `assignments/day119/` by Day 120 morning:  

1. Power BI File  
   - `day119_transformed.pbix` containing all Query Editor steps, M functions, and DAX elements.  

2. M Script Export  
   - `day119_m_queries.txt` with the full M code for each query and function.  

3. DAX Formulas Document  
   - `day119_dax_measures.md` listing calculated tables, columns, and measures with descriptions.  

4. Transformation Steps  
   - `day119_query_steps.md` enumerating each applied step in the Query Editor with rationale.  

5. Model Diagram  
   - `day119_model_diagram.png` showing table relationships and calculated table integration.  

6. Analytical Report (`day119_report.md`, 300 words)  
   - Describe your transformation strategy, performance optimizations, and how DAX complements Power Query.  

7. Reflection (`day119_reflection.md`, 200 words)  
   - Reflect on the division of transformation logic between M and DAX, challenges faced, and best practices for maintainable Power BI solutions.  

---  

By mastering Power Query’s M language alongside advanced DAX, you’ll architect robust, high-performance data models—enabling deeper insights and flexible analyses in your epidemiology dashboards.
