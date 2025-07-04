# **Day 111 – Supabase Setup: Authentication & Schema Design**
  
Bloom Level: Understand & Apply | Duration: 4 hrs  

## Objectives  

- Create a new Supabase project and understand key dashboard components.  
- Design a relational schema in Supabase’s Postgres database for epidemiological data.  
- Configure authentication methods (email/password, OAuth, SSO) and user roles.  
- Implement Row-Level Security (RLS) policies to enforce fine-grained access controls.  
- Test authentication flows and secure API endpoints with Supabase Client libraries.  

---  

## Agenda  

1. Lecture: Supabase Architecture & Auth Concepts (45 min)  
   - Supabase as a Backend-as-a-Service: database, auth, storage, functions  
   - Authentication flows: JWT tokens, refresh, OAuth providers  
   - Role management and security fundamentals  

2. Demo: Supabase Dashboard Walkthrough (30 min)  
   - Project creation and settings overview  
   - Database table editor and SQL editor  
   - Auth settings: providers, email templates, redirect URLs  

3. Lab Part 1 – Schema Design & Table Creation (60 min)  
   - Define tables: `users`, `roles`, `cases`, `locations`, `reports`  
   - Set primary keys, foreign keys, and constraints in the SQL editor  
   - Populate sample rows via the table editor or `INSERT` statements  

4. Lab Part 2 – Authentication & RLS Policy Implementation (45 min)  
   - Enable email/password and OAuth (e.g., Google) in Auth settings  
   - Create RLS policies:  
     - Allow users to read their own `reports`  
     - Grant admin role full access to all tables  
   - Test policies with Supabase’s “Run as user” feature  

5. Discussion & Q&A (30 min)  
   - Best practices for secret management and environment variables  
   - Balancing convenience and security in public APIs  
   - Integrating Supabase with frontend frameworks  

---  

## Exercise Details  

**Data Provided:**  

| Item                         | Description                                                        |
|------------------------------|--------------------------------------------------------------------|
| `day111_supabase_template.sql` | Starter SQL script for table definitions and sample data          |
| `supabase_env_example`       | Template for environment variables (`SUPABASE_URL`, `SUPABASE_KEY`) |
| `frontend_snippet.js`        | Example Supabase Client initialization code for JS/TS projects     |

**Key Tasks:**  

- Provision a new Supabase project and record the API URL and anon key.  
- Run the provided SQL script in the dashboard’s SQL editor to create tables and seed data.  
- Configure email/password and Google OAuth under Auth → Providers.  
- Define RLS policies in the SQL editor:  
  - Public can read `locations` but not `cases` or `reports`.  
  - Authenticated users can CRUD their own `reports`.  
  - Admin role (via `role` claim) can bypass all RLS.  
- Use the “Run as role” feature to verify each policy’s enforcement.  
- In a local Node.js script, initialize Supabase Client and demonstrate sign-up, sign-in, and a secured `select` query on `reports`.  

---  

## Assignment  

Submit to `assignments/day111/` by Day 112 morning:  

1. Supabase Project Summary (`day111_summary.md`)  
   - Supabase URL, anon key, and list of enabled auth providers.  

2. Schema Definition SQL (`day111_schema.sql`)  
   - `CREATE TABLE` and `ALTER TABLE` statements with comments.  

3. RLS Policies Script (`day111_rls_policies.sql`)  
   - Annotated `CREATE POLICY` and `ALTER TABLE ... ENABLE ROW LEVEL SECURITY` commands.  

4. Environment File Template (`day111_env.md`)  
   - Instructions and example variables for local and production setups.  

5. Client Demo Script (`day111_client_demo.js`)  
   - Code that authenticates a user, fetches their reports, and handles unauthorized access errors.  

6. Analytical Report (`day111_report.md`, 300 words)  
   - Reflect on schema design choices, RLS policy implications, and integration challenges.  

7. Reflection (`day111_reflection.md`, 200 words)  
   - Discuss lessons learned about auth security, policy testing, and next steps for full-stack integration.  

---  

By the end of this session, you’ll have a secure Supabase back end with a typed schema and fine-grained access controls—foundations for rapidly building authenticated, data-driven epidemiology applications.
