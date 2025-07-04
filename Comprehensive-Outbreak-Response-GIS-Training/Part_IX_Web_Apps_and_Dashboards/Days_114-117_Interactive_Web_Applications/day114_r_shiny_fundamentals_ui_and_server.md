# **Day 114 – R Shiny Fundamentals: UI & Server**  

Bloom Level: Understand & Apply | Duration: 4 hrs  

---

## Objectives  

- Understand the two‐part Shiny app architecture: UI definitions and server logic.  

- Build responsive user interfaces using `fluidPage()`, layout functions, and common input controls.  

- Implement server‐side reactivity with `reactive()`, `render*()` functions, and observers.  

- Organize app code across `app.R` or split into `ui.R` and `server.R` for maintainability.  

- Debug and test Shiny components locally before deployment.  

---

## Agenda  

1. Lecture: Shiny App Architecture (45 min)  
   - UI vs. server responsibilities  
   - Reactive programming model and dependency graph  

2. Demo: Simple Shiny App Walkthrough (30 min)  
   - Creating `app.R` in RStudio  
   - Adding inputs (sliders, selects) and outputs (plots, tables)  

3. Lab Part 1 – Building the UI (60 min)  
   - Use `fluidPage()`, `sidebarLayout()`, `tabsetPanel()`  
   - Add `sliderInput()`, `selectInput()`, and `actionButton()` controls  
   - Style with themes and custom CSS  

4. Lab Part 2 – Implementing Server Logic (45 min)  
   - Define `reactive()` data transformations  
   - Use `renderPlot()`, `renderTable()`, `observeEvent()`  
   - Manage reactivity for efficient updates  

5. Discussion & Q&A (30 min)  
   - Best practices: modularizing UI/server, namespacing  
   - Testing strategies with `testServer()` and Shiny’s built‐in tools  

---

## Exercise Details  

**Data Provided:**  

| File                         | Description                                             |
|------------------------------|---------------------------------------------------------|
| `day114_shiny_template.R`    | Starter `app.R` with placeholder UI and server blocks   |
| `day114_data.csv`            | Sample epidemiological dataset (case counts by region)  |
| `day114_helpers.R`           | Utility functions for data wrangling and plotting       |

**Key Tasks:**  

- Load `day114_data.csv` in your Shiny app and preview with `tableOutput()`.  

- Construct a UI with:  
  - A sidebar containing range sliders and dropdowns for filtering data.  
  - A main panel with a dynamic plot (`plotOutput()`) and summary table.  

- In the server function:  
  - Wrap data filtering in a `reactive()` expression.  
  - Render a ggplot based on filtered data.  
  - Use `observeEvent()` to reset inputs or show notifications.  

- Apply a theme (e.g., `bslib::bs_theme()`) and include a custom CSS file for branding.  

---

## Assignment  

Submit to `assignments/day114/` by Day 115 morning:  

1. Shiny App Code  
   - `app.R` (or `ui.R`/`server.R`) containing fully functional UI and server logic.  

2. UI Sketch  
   - `day114_ui_wireframe.png` showing layout of inputs and outputs.  

3. Demo Video or GIF  
   - `day114_demo.mp4` or `.gif` illustrating interactive filtering and plot updates.  

4. Analytical Report  
   - `day114_report.md` (300 words) documenting app structure, reactive flows, and design choices.  

5. Reflection  
   - `day114_reflection.md` (200 words) on challenges in reactive programming, UI design trade‐offs, and next steps for scaling Shiny apps.  

---

Mastering Shiny’s UI and server fundamentals will enable you to build interactive dashboards that bring epidemiological data to life—facilitating real‐time exploration and decision making.
