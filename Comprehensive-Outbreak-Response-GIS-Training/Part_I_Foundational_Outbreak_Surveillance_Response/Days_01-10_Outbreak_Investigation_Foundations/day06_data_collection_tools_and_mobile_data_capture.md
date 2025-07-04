# **Day 6 – Data Collection Tools and Mobile Data Capture**

Bloom Level: Apply | Duration: 4 hrs  

## Objectives  

- Compare leading mobile data‐capture platforms (ODK, KoboToolbox, Survey123, EpiCollect5, QField) and their fit for animal health surveys.  
- Design and configure a mobile form with geolocation, photos, and multimedia support.  
- Implement data validation, skip logic, and constraint checks to ensure data quality.  
- Set up offline data collection, synchronization workflows, and basic security measures (SSL, encryption).  

---

## Agenda  

1. Lecture: Mobile Data Capture Ecosystem (45 min)  
   - Platform overviews: strengths, limitations, hosting options  
   - Key features: geotagging, multimedia, validation, offline support  

2. Demo: Building a KoboToolbox Form (30 min)  
   - Creating questions, grouping, skip logic, and constraints  
   - Enabling GPS capture and image uploads  

3. Lab Part 1 – Form Development (60 min)  
   - Import the provided form skeleton into Kobo/ODK  
   - Add fields for species, flock size, clinical signs, and sample type  
   - Configure required fields, value constraints, and skip patterns  

4. Lab Part 2 – Deployment & Sync (45 min)  
   - Publish form to server, configure user accounts  
   - Collect test submissions in the field app and sync to server  
   - Export submissions to CSV/JSON  

5. Discussion & Q&A (30 min)  
   - Best practices for training field teams on digital tools  
   - Strategies for ensuring data security and offline reliability  

---

## Exercise Details  

- **Data Provided:**  
  - `region_shapefile.zip` (administrative boundaries)  
  - `form_skeleton.xlsx` (survey template with column definitions)  
  - Sample image files and GPS coordinates for testing  

- **Key Tasks:**  
  1. Customize the provided skeleton to include animal species, herd demographics, and clinical observations.  
  2. Embed GPS point capture and image‐upload questions with proper constraints.  
  3. Deploy to a hosted server (Kobo/ODK instance) and perform at least three test submissions.  

---

## Assignment  

Submit to `assignments/day06/` by Day 7 morning:

1. **Mobile Form File** (`day06_form.xlsx` or `day06_form.xml`)  
   - Completed form template with validation and skip logic, ready for upload.  

2. **Deployment Guide** (`day06_deployment.md`)  
   - Step‐by‐step instructions on publishing the form, setting user roles, and syncing submissions.  

3. **Test Submission Dataset** (`day06_submissions.csv`)  
   - Exported CSV of your test submissions, demonstrating geotags and multimedia references.  

4. **Reflection** (`day06_reflection.md`)  
   - 200 words on challenges configuring offline workflows and ensuring data quality in mobile surveys.
