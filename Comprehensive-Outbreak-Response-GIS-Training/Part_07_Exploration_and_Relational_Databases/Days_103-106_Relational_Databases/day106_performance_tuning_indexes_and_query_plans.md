# **Day 106 – Performance Tuning: Indexes & Query Plans**
  
Bloom Level: Analyze & Optimize | Duration: 4 hrs  

## Objectives  

- Explain the role of indexes and query plans in database performance.  
- Use EXPLAIN and EXPLAIN ANALYZE to inspect execution strategies and cost estimates.  
- Create and benchmark B-tree, GiST, and GIN indexes for both attribute and spatial queries.  
- Apply table partitioning and up-to-date statistics to speed up large-scale data scans.  
- Monitor performance metrics and refine database configuration for optimal throughput.  

---  

## Agenda  

1. Lecture: Index Types & Use Cases (45 min)  
   - B-tree for equality/range filters, GiST/GiN for spatial and full-text  
   - Index maintenance costs and trade-offs  

2. Demo: Exploring Query Plans (30 min)  
   - EXPLAIN vs. EXPLAIN ANALYZE outputs  
   - Identifying seq scans, index scans, joins, and sorts  

3. Lab Part 1 – Index Creation & Benchmarking (60 min)  
   - Run baseline queries and record execution times  
   - Create B-tree index on `cases(report_date)` and GiST on `regions(geom)`  
   - Rerun queries with ANALYZE and compare performance  

4. Lab Part 2 – Partitioning & Statistics (45 min)  
   - Implement range partitioning of `cases` by year  
   - Schedule ANALYZE to refresh planner statistics  
   - Measure query speed on partitioned vs. non-partitioned tables  

5. Discussion & Q&A (30 min)  
   - Balancing index overhead with query gains  
   - When to reindex or adjust autovacuum settings  

---  

## Exercise Details  

**Data Provided:**  

| File                            | Description                                                                          |
|---------------------------------|--------------------------------------------------------------------------------------|
| day106_db.sql                   | PostgreSQL dump with tables: `cases`, `patients`, `locations`, and spatial `regions` |
| day106_queries.sql              | Starter SQL file with sample queries for tuning                                      |
| day106_partition_template.sql   | Template script for range partitioning of the `cases` table                          |
| day106_schema_diagram.png       | Updated ER diagram including spatial and temporal attributes                         |

**Key Tasks:**  

- Restore `day106_db.sql` into a local PostgreSQL instance and inspect schemas with `\d`.  
- Execute provided queries to establish baseline execution times using `EXPLAIN ANALYZE`.  
- Create a B-tree index on `cases(report_date)` and a GiST index on `regions(geom)`.  
- Rerun tuned queries, document reductions in execution time and planning cost.  
- Apply table partitioning on `cases` by year using the template, then test queries against partitions.  
- Run `ANALYZE` and view updated planner statistics; compare performance before and after.  
- Export query plans and timing results for reporting.  

---  

## Assignment  

Submit to `assignments/day106/` by Day 107 morning:  

1. **Tuning Script**  
   - `day106_tuning.sql` with indexed creation, partition definitions, and ANALYZE commands.  

2. **psql Command Log**  
   - `day106_psql_commands.txt` listing all psql meta-commands and tuning steps.  

3. **Query Plan Reports**  
   - `day106_query_plans.md` showing before/after EXPLAIN ANALYZE outputs with commentary.  

4. **Performance Metrics**  
   - `day106_performance.csv` recording query names, execution times, and cost estimates.  

5. **Partition Definition**  
   - `day106_partitioning.sql` implementing range partitions and triggers for `cases`.  

6. **Analytical Report**  
   - `day106_report.md` (300 words) summarizing tuning methodology, index impacts, and partition benefits.  

7. **Reflection**  
   - `day106_reflection.md` (200 words) on challenges in indexing, planner behavior surprises, and next steps for sustained performance.  

---  

Fine-tuning indexes and understanding query plans will empower you to handle massive epidemiological datasets with speed and reliability.
