# **Day 14 – Database Design for Case and Laboratory Data**

Bloom Level: Apply | Duration: 4 hrs  

## Objectives  

- Understand relational database fundamentals and normalization principles for outbreak data.  

- Model entities and relationships for animal cases, premises, and laboratory results.  

- Incorporate spatial data types (geometry) and indexing strategies for efficient geospatial queries.  

- Implement a PostgreSQL/PostGIS schema with appropriate primary keys, foreign keys, and constraints.  

## Agenda  

1. Lecture: Principles of Relational Modeling (45 min)  
   - Entities, attributes, relationships, and normalization (1NF, 2NF, 3NF)  
   - Spatial extensions: PostGIS geometry columns and GiST indexes  

2. Case Study: Integrated Case–Lab Database (30 min)  
   - Review a published schema from an avian influenza response  
   - Discuss design decisions: one-to-many cases to samples, handling updates  

3. Group Exercise: Entity–Relationship Diagram (45 min)  
   - Teams draft an ERD with tables: `premises`, `cases`, `lab_results`, `species`, `sample_types`  
   - Define cardinalities, key fields, and spatial columns for premises  

4. Interactive Demo: Schema Implementation (60 min)  
   - Create a new database, enable PostGIS extension  
   - Write and execute `CREATE TABLE` statements, add `FOREIGN KEY` and `CHECK` constraints  
   - Load sample CSVs into tables and build spatial index on `geom` column  

5. Discussion & Q&A (30 min)  
   - Performance tuning: indexes, partitioning by date or geography  
   - Strategies for schema evolution and version control (Liquibase, Flyway)  

## Exercise Details  

**Data Provided:**  
- `day14_premises.csv` (farm IDs, names, lat/lon)  
- `day14_cases.csv` (case IDs, farm IDs, species code, onset date)  
- `day14_lab.csv` (sample IDs, case IDs, test type, result, test date)  
- `species_lookup.csv`, `sample_types.csv` for reference tables  

**Key Tasks:**  
1. Draft an ERD diagram reflecting all tables, keys, and relationships.  
2. Write SQL DDL to create each table with appropriate data types (including `geometry(Point,4326)`).  
3. Implement spatial and regular indexes to optimize common queries (e.g., cases by location).  
4. Load the CSV data into the schema and validate referential integrity.  

## Assignment  

Submit to `assignments/day14/` by Day 15 morning:  

1. **ER Diagram** (`day14_erd.png`)  
   - Visual representation of tables, keys, and relationships.  

2. **SQL Schema Script** (`day14_schema.sql`)  
   - `CREATE TABLE` statements with constraints and index definitions.  

3. **Data Load Script** (`day14_load.sql` or `day14_load.py`)  
   - Commands or code to import provided CSVs into the database.  

4. **Reflection** (`day14_reflection.md`)  
   - 200 words on challenges in balancing normalization, performance, and geospatial needs.