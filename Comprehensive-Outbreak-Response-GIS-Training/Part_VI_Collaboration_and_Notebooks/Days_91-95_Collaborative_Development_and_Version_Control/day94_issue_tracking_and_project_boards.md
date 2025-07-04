# **Day 94 – Issue Tracking & Project Boards**
  
Bloom Level: Understand & Apply | Duration: 4 hrs  

---  

## Objectives  

- Explain the role of issue tracking in managing tasks, bugs, and features throughout a project lifecycle.  

- Create, triage, label, and prioritize issues using GitHub/GitLab platforms.  

- Design and apply issue templates to standardize bug reports and feature requests.  

- Set up and manage project boards (Kanban/Scrum) to visualize workflow stages.  

- Automate board updates by linking issues to pull requests and commits.  

---  

## Agenda  

1. Lecture: Issue Tracking Fundamentals (45 min)  
   - Issue lifecycle: open, triage, assign, resolve, close  
   - Metadata fields: titles, descriptions, labels, milestones, assignees  
   - Benefits of templates and checklists for consistent reporting  

2. Demo: GitHub/GitLab Issue Management (30 min)  
   - Creating and customizing issue templates in `.github/ISSUE_TEMPLATE/`  
   - Applying and filtering labels, assigning issues, setting milestones  

3. Lab Part 1 – Issue Creation & Triage (60 min)  
   - Clone `day94_repo_template.git` and push to your remote  
   - Draft two issue templates: `bug_report.md` and `feature_request.md`  
   - Create five issues: two bugs, two features, one chore  
   - Apply appropriate labels, assignees, and milestones  

4. Lab Part 2 – Project Board Setup & Automation (45 min)  
   - Create a project board with columns: To Do, In Progress, Review, Done  
   - Add issues to the board and move them through columns manually  
   - Configure automation: move to “In Progress” on PR open, to “Done” on merge  

5. Discussion & Q&A (30 min)  
   - Best practices for prioritization and issue hygiene  
   - Strategies for team collaboration and avoiding bottlenecks  
   - Integrating CI/CD statuses and notifications into board workflows  

---  

## Exercise Details  

**Data Provided:**  

| Item                                  | Description                                                  |
|---------------------------------------|--------------------------------------------------------------|
| day94_repo_template.git               | Barebones repository with code folder, `.github/ISSUE_TEMPLATE/`, and CI config |
| `.github/ISSUE_TEMPLATE/bug_report.md`| Starter Markdown template for bug reports                    |
| `.github/ISSUE_TEMPLATE/feature_request.md` | Starter Markdown template for feature requests           |
| `day94_tasks.xlsx`                    | Spreadsheet listing sample tasks, bugs, and feature ideas    |

**Key Tasks:**  

1. Fork or clone the template repo; push a personal copy to GitHub/GitLab.  
2. Complete and commit two issue templates (`bug_report.md`, `feature_request.md`) with required fields and checklists.  
3. Use templates to create five new issues: categorize as Bug, Feature, or Chore.  
4. Apply labels (e.g., bug, enhancement, chore), assign to team members, and set up a milestone “v1.0”.  
5. Create a Kanban‐style project board, add all open issues, and manually move two through workflow stages.  
6. Implement automation rules: issues auto‐move columns on PR open/merge.  

---  

## Assignment  

Submit to `assignments/day94/` by Day 95 morning:  

1. Issue Tracking Plan  
   - `day94_issue_plan.md` outlining naming conventions, label schema, milestone strategy, and triage workflow.  

2. Issue Templates  
   - `bug_report.md` and `feature_request.md` in `.github/ISSUE_TEMPLATE/` with sections for reproduction steps, acceptance criteria, and metadata.  

3. Exported Issues  
   - `day94_issues.json` or CSV export listing your five created issues with IDs, titles, labels, assignees, and statuses.  

4. Project Board Snapshot  
   - `day94_project_board.png` showing each column with issues in various states.  

5. Automation Workflow  
   - `day94_actions.yml` (or `.gitlab-ci.yml`) defining rules to auto‐move issues when PRs are opened or merged.  

6. Reflection  
   - `day94_reflection.md` (200 words) on lessons learned in issue hygiene, board management, and how this will improve your project collaboration.  

---  

Effective issue tracking and project boards keep teams aligned, tasks visible, and workflows transparent—crucial for large‐scale spatial epidemiology pipelines.
