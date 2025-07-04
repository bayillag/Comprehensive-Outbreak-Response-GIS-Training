# **Day 116 – Modularizing Apps & Custom Themes**
  
Bloom Level: Apply & Create | Duration: 4 hrs  

## Objectives  

- Understand the principles of Shiny modules and their benefits for app organization.  
- Refactor a monolithic Shiny app into reusable UI and server modules.  
- Manage namespaces to avoid ID collisions when nesting modules.  
- Develop a custom theme using **bslib** and/or CSS to enforce consistent branding.  
- Integrate modular code and themes into a cohesive Shiny application structure.  

---  

## Agenda  

1. Lecture: Shiny Module Concepts (45 min)  
   - Module anatomy: UI functions, server functions, and namespaces  
   - Advantages: testability, reuse, and collaboration  

2. Demo: Building & Calling Modules (30 min)  
   - Converting a UI block into `mod_filter_ui(id)` and its server counterpart  
   - Invoking multiple instances with distinct IDs  

3. Lab Part 1 – Refactoring to Modules (60 min)  
   - Identify logical components in `day116_monolith_app.R`  
   - Extract at least two modules (e.g., data loader, map renderer)  
   - Wire modules in a new `app.R` with `callModule()` or `moduleServer()`  

4. Lab Part 2 – Custom Theming (45 min)  
   - Use `bslib::bs_theme()` to define colors, fonts, and spacing  
   - Override or extend with custom CSS in `www/custom.css`  
   - Apply theme globally and test across UI modules  

5. Discussion & Q&A (30 min)  
   - Best practices for naming, file organization, and documentation  
   - Balancing flexibility and complexity in theme design  

---  

## Exercise Details  

| Resource                         | Description                                                          |
|----------------------------------|----------------------------------------------------------------------|
| `day116_monolith_app.R`          | Starter single‐file Shiny app                                        |
| `module_template/`               | Folder with `ui_module.R` and `server_module.R` templates           |
| `custom_theme.css`               | Example CSS to import and modify                                      |
| `day116_data.csv`                | Epidemiological dataset for filtering and mapping                    |

**Key Tasks:**  
- Review the monolithic app and outline module boundaries (data import, filters, plotting).  
- Create `mod_data_ui()`/`mod_data_server()`, `mod_map_ui()`/`mod_map_server()` in separate R files.  
- In `app.R`, source module files, instantiate modules with unique IDs, and pass reactive values between them.  
- Define a `bslib` theme in `app.R` (e.g., `bs_theme(bootswatch = "flatly", primary = "#2C3E50")`).  
- Add a `www/custom.css` to tweak headers, button styles, and sidebar width; ensure modules inherit styling.  

---  

## Assignment  

Submit to `assignments/day116/` by Day 117 morning:  

1. Modularized App Code  
   - `app.R` plus module scripts (`mod_data.R`, `mod_map.R`, etc.) organized in `R/` or `modules/`.  

2. Theme Files  
   - `custom_theme.R` (if using **bslib**) and `www/custom.css` with comments.  

3. UI Wireframe Update  
   - `day116_wireframe_updated.png` showing module layout and theme colors.  

4. Demo Recording  
   - `day116_demo.mp4` or `.gif` demonstrating module interaction and themed UI.  

5. Analytical Report (`day116_report.md`, 300 words)  
   - Describe the refactoring process, module design rationale, namespace management, and theming decisions.  

6. Reflection (`day116_reflection.md`, 200 words)  
   - Reflect on challenges modularizing the app, benefits observed, and next steps for a component library.  

---  

By modularizing your Shiny app and applying a custom theme, you’ll achieve cleaner code organization, easier maintenance, and a consistent user experience—key factors for scalable epidemiological dashboards.
