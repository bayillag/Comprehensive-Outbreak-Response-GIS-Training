# **Day 92 – Collaboration: Pull Requests & Code Reviews**
  
Bloom Level: Apply & Evaluate | Duration: 4 hrs  

## Objectives  

- Understand branching‐and‐pull‐request workflows to manage shared code.  
- Create, update, and merge pull requests (PRs) on a remote Git platform.  
- Conduct systematic code reviews: commenting, suggesting changes, approving.  
- Integrate continuous integration (CI) checks and enforce PR templates.  
- Adopt best practices for review checklists, linking issues, and documenting feedback.  

---  

## Agenda  

1. Lecture: Collaborative Development Workflows (45 min)  
   - Fork vs. shared repo models  
   - Pull request lifecycle: open, review, revise, merge  
   - Roles: author, reviewer, maintainer  

2. Demo: Pull Requests & Reviews in Practice (30 min)  
   - Navigating GitHub/GitLab UI for PR creation  
   - Adding reviewers, labels, linking issues  
   - Inline comments, suggestions vs. blocking comments  
   - Enabling CI status checks and review protection rules  

3. Lab Part 1 – Opening & Updating a Pull Request (60 min)  
   - Fork and clone `day92_collab_template.git`  
   - Create branch `feature/refactor-prevalence` and implement a refactoring in analysis script  
   - Commit changes, push branch, open a PR against upstream `main` with a descriptive title and body  
   - Update PR based on CI feedback: fix linting errors, add tests, push follow‐up commits  

4. Lab Part 2 – Performing a Code Review (45 min)  
   - Reviewer role: fetch author’s branch locally and inspect code  
   - Submit inline review comments: request renaming variables, adjust documentation, optimize loops  
   - Approve or request changes using the platform’s review UI  
   - Author responds to comments: resolve threads and push fixes  

5. Discussion & Q&A (30 min)  
   - Balancing thorough reviews with timeliness  
   - Using PR templates and checklists to standardize feedback  
   - Handling merge conflicts that arise during review  

---  

## Exercise Details  

**Data Provided:**  
- Remote repository URL: `https://git.example.com/day92_collab_template.git`  
- Starter files in `analysis/`: `prevalence.py`, `report_template.md`  
- CI configuration file `.github/workflows/lint-test.yml`  

**Key Tasks:**  
1. Fork and clone the template repo to your account.  
2. Create `feature/refactor-prevalence` branch; refactor prevalence calculation into a function and add unit tests.  
3. Push branch and open a pull request against the original `main`. Include:  
   - A clear title (`Refactor prevalence calculation into function`)  
   - A descriptive body linking to issue #15 and summarizing changes.  
4. Run CI checks; fix any lint or test failures by pushing updates to the same branch.  
5. Switch roles: review a peer’s PR in the shared workspace:  
   - Check code style and use of docstrings  
   - Suggest improvements or ask clarifying questions  
   - Approve when all concerns are addressed  

---  

## Assignment  

Submit to `assignments/day92/` by Day 93 morning:  

1. Pull Request URL  
   - Link to your PR in `day92_collab_template.git`.  

2. Review Log (`day92_review_log.md`)  
   - Summary of your review comments on a peer’s PR, grouped by file and line, and the outcome (resolved/unresolved).  

3. PR Template (`day92_pr_template.md`)  
   - Your proposed PR template with sections for description, linked issues, test plan, and reviewer checklist.  

4. CI Badge Snapshot (`day92_ci_badge.png`)  
   - Screenshot of the passing CI badge in your merged PR.  

5. Reflection (`day92_reflection.md`, 200 words)  
   - Reflect on challenges encountered in authoring and reviewing PRs, how CI influenced your workflow, and strategies for more effective collaboration.  

---  

By mastering pull request workflows and structured code reviews, you’ll foster high‐quality, collaborative code development—essential for scalable spatial epidemiology pipelines.