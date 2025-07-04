# **Day 112 – Building RESTful APIs & Realtime Subscriptions**
  
Bloom Level: Apply & Create | Duration: 4 hrs  

## Objectives  

- Understand REST principles and HTTP methods for CRUD operations.  

- Design and implement RESTful endpoints using a backend framework (Node.js/Express or Python/Flask).  

- Serialize and validate epidemiological data with JSON schemas and data transfer objects.  

- Enable realtime subscriptions for spatial event streams via WebSockets or Supabase Realtime.  

- Secure API endpoints with token-based authentication and rate limiting.  

---  

## Agenda  

1. Lecture: REST & Realtime Fundamentals (45 min)  
   - REST architecture: resources, URIs, status codes, verbs  
   - Realtime patterns: WebSockets, Server-Sent Events, Supabase Realtime  

2. Demo: CRUD API & Subscription Channel (30 min)  
   - Scaffold endpoints for cases and locations  
   - Implement a “new case” broadcast channel over WebSocket or Supabase  

3. Lab Part 1 – REST API Implementation (60 min)  
   - Initialize project skeleton and install dependencies  
   - Define routes for `GET`, `POST`, `PUT`, `DELETE` on `/cases` and `/locations`  
   - Validate JSON bodies against a schema and return proper status codes  

4. Lab Part 2 – Realtime Subscriptions (45 min)  
   - Configure WebSocket server or Supabase client to subscribe to case updates  
   - Broadcast new case events to all connected clients  
   - Build a simple HTML/JS client to display incoming events in real time  

5. Discussion & Q&A (30 min)  
   - Best practices for payload size and back-pressure  
   - Authentication flows for REST vs. realtime channels  
   - Monitoring and scaling API and subscription servers  

---  

## Exercise Details  

**Data Provided:**  

| Item                              | Description                                         |
|-----------------------------------|-----------------------------------------------------|
| `day112_api_template/`            | Starter project scaffold with basic file structure  |
| `cases_api_spec.yaml`             | OpenAPI stub for case and location endpoints        |
| `supabase_realtime_config.js`     | Example Supabase Realtime subscription setup        |
| `sample_data.json`                | Test payloads for POST and PUT requests             |

**Key Tasks:**  

1. Scaffold a new API project directory and install required packages.  
2. Implement CRUD endpoints for `/cases` and `/locations`, adhering to the OpenAPI spec.  
3. Connect endpoints to a PostGIS or Supabase database for data persistence.  
4. Validate incoming JSON against a predefined schema; return 4xx errors on validation failure.  
5. Set up a realtime channel (WebSocket or Supabase) that publishes new case records immediately.  
6. Secure REST and realtime endpoints with JWT authentication and configure rate limiting.  
7. Test all endpoints and subscription flows using Postman/curl and a simple frontend client.  

---  

## Assignment  

Submit to `assignments/day112/` by Day 113 morning:  

1. API Source Code  
   - `day112_api/` directory containing all server code, configurations, and package definitions.  

2. OpenAPI Specification  
   - `day112_api_spec.yaml` fully defined with paths, schemas, and security schemes.  

3. Postman Collection  
   - `day112_postman_collection.json` covering CRUD and auth workflows.  

4. Realtime Demo Client  
   - `day112_realtime_demo.html` (or JS script) demonstrating live updates of new cases.  

5. Analytical Report (`day112_report.md`, 300 words)  
   - Summarize your API design choices, subscription mechanism, security measures, and lessons learned.  

6. Reflection (`day112_reflection.md`, 200 words)  
   - Reflect on challenges in building realtime systems, authentication for streaming endpoints, and recommended best practices.  

---  

Connecting RESTful services with realtime subscriptions will empower your tools to deliver up-to-the-second epidemiological updates—crucial for rapid situational awareness and timely interventions.