# **Day 120 – Designing, Publishing & Sharing Dashboards**  

Bloom Level: Evaluate & Create | Duration: 4 hrs  

---

## Objectives  

- Apply dashboard design principles for clarity, accessibility, and storytelling.  

- Choose appropriate visualizations and layouts that communicate epidemiological insights effectively.  

- Implement interactive features (filters, tooltips, drill-through) to enhance user exploration.  

- Apply consistent theming, branding, and accessibility standards across dashboard elements.  

- Publish and share dashboards via appropriate platforms (Power BI Service, Tableau Public, Shiny Server).  

- Establish version control, collaboration workflows, and user access management for dashboards.  

---

## Agenda  

1. Lecture: Dashboard Design & Best Practices (45 min)  
   - Visual hierarchy, Gestalt principles, and color accessibility  
   - Chart selection guidelines based on data type and message  

2. Demo: Building an Interactive Dashboard (30 min)  
   - Assembling visuals, slicers/filters, and dynamic titles  
   - Applying theme and layout consistency  

3. Lab Part 1 – Constructing the Dashboard (60 min)  
   - Connect to cleaned epidemiological data  
   - Create key visuals: maps, trend lines, KPI cards, and breakdown tables  
   - Configure interactions: cross-filtering, drill-through, and custom tooltips  

4. Lab Part 2 – Theming & Accessibility (45 min)  
   - Define a color palette that meets WCAG contrast ratios  
   - Add descriptive alt-text and keyboard navigation considerations  
   - Incorporate corporate or project branding elements  

5. Lab Part 3 – Publishing & Collaboration (30 min)  
   - Publish to Power BI Service or other platform  
   - Set up workspace permissions, sharing links, and row-level security  
   - Integrate version control or change-log processes  

6. Discussion & Q&A (30 min)  
   - Strategies for gathering user feedback and iterating  
   - Monitoring usage metrics and performance tuning  

---

## Exercise Details  

| Resource                         | Description                                                                   |
|----------------------------------|-------------------------------------------------------------------------------|
| `day120_dashboard_template.pbit` | Starter Power BI template with layout placeholders and sample visuals         |
| `epi_data_clean.csv`             | Cleaned, processed epidemiological dataset                                    |
| `style_guide.md`                 | Branding colors, fonts, and element spacing guidelines                        |
| `sharing_checklist.md`           | Steps and best practices for publishing, permissions, and documentation       |

**Key Tasks:**  

- Load `epi_data_clean.csv` into the template and verify data model relationships.  
- Build visuals: a choropleth map of incidence, a time-series trend line, KPI cards for total cases and R₀ estimates, and a drillable table of district metrics.  
- Add slicers for date range, region, and case severity; configure cross-filter settings.  
- Implement a custom theme using the provided `style_guide.md`, ensure all text and visuals meet accessibility contrast.  
- Publish the finished dashboard to Power BI Service (or alternative), configure workspace, sharing links, and row-level security for user groups.  
- Document a versioning process: changelog file, naming convention, and rollback plan.  

---

## Assignment  

Submit to `assignments/day120/` by Day 121 morning:  

1. **Dashboard File**  
   - `day120_dashboard.pbix` (Power BI) or equivalent (Tableau `.twbx`, Shiny app folder).  

2. **Published URL**  
   - Link to the live dashboard with viewer-level access.  

3. **Style & Accessibility Report** (`day120_style_report.md`, 300 words)  
   - Document theme choices, branding implementation, and accessibility compliance steps.  

4. **User Guide** (`day120_user_guide.md`, 300 words)  
   - Instructions for navigating, filtering, and interpreting dashboard elements.  

5. **Versioning & Collaboration Plan** (`day120_versioning.md`, 200 words)  
   - Describe your file naming, changelog, access controls, and rollback strategy.  

6. **Reflection** (`day120_reflection.md`, 200 words)  
   - Reflect on design trade-offs, publishing challenges, and how you’ll gather feedback for future improvements.  

---

By the end of Day 120, you’ll have built a polished, accessible epidemiology dashboard, shared it with stakeholders securely, and established practices for collaborative versioning and continuous improvement.
