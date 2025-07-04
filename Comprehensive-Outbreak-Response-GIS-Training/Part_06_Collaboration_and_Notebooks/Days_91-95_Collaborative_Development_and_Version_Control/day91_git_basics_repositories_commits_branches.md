# **Day 91 – Git Basics: Repositories, Commits & Branches**
  
Bloom Level: Understand & Apply | Duration: 4 hrs  

## Objectives  

- Explain version control concepts and the role of Git in collaborative projects.  

- Initialize and clone Git repositories locally and remotely.  

- Stage changes and create meaningful commits with messages.  

- Create, switch, and manage branches for parallel development.  

- Merge branches, resolve simple conflicts, and review commit history.  

---  

## Agenda  

1. Lecture: Git Fundamentals (45 min)  
   - Version control terminology: repository, commit, branch, remote, merge  
   - Git architecture: working directory, staging area, local vs. remote repo  

2. Demo: Core Git Workflows (30 min)  
   - Initializing (`git init`) and cloning (`git clone`) a repo  
   - Staging (`git add`), committing (`git commit`), and checking status (`git status`)  
   - Creating (`git branch`), listing, and switching (`git checkout`) branches  
   - Merging branches (`git merge`) and handling conflicts  

3. Lab Part 1 – Repository Setup & Commits (60 min)  
   - Initialize a local repo in `day91_project/`  
   - Create sample scripts and documentation; stage and commit incrementally  
   - Connect to a remote GitHub/GitLab repository; push initial commit  

4. Lab Part 2 – Branching & Merging (45 min)  
   - Create feature branches (`feature/update-readme`, `feature/add-script`)  
   - Implement changes on separate branches; commit updates  
   - Merge feature branches into `main`, deliberately introduce and resolve a simple conflict  

5. Discussion & Q&A (30 min)  
   - Best practices: commit messaging, branch naming conventions, pull request workflows  
   - Strategies for conflict avoidance and resolution  
   - Integrating Git into data-analysis and reporting pipelines  

---  

## Exercise Details  

**Data Provided:**  
- A remote template repository at `https://git.example.com/day91_template.git`  
- Local folder `day91_project/` containing placeholder files: `README.md`, `analysis.py`, `data/`  

**Key Tasks:**  
1. Clone the remote template repo into your workspace.  
2. Create and switch to a new branch `feature/first-commit`; modify `README.md`, stage, and commit with a clear message.  
3. Push the branch to the remote and open a pull request.  
4. Back on `main`, create two branches (`feature/update-script`, `feature/add-notebook`); add sample code or markdown, commit, and push each branch.  
5. Merge both branches sequentially into `main`; when a merge conflict arises in `README.md`, resolve it, stage the resolution, and commit the merge.  
6. Use `git log --graph --oneline --all` to visualize commit history; export the log to `day91_git_log.txt`.  

---  

## Assignment  

Submit to `assignments/day91/` by Day 92 morning:  

1. Git Command Log (`day91_git_commands.md`)  
   - List of Git commands executed, organized by task, with brief explanations.  

2. Branching Diagram (`day91_branch_diagram.png`)  
   - A simple flowchart showing branch creation, commits, merges, and conflict resolution.  

3. Commit History Export (`day91_git_log.txt`)  
   - Output of `git log --graph --oneline --all`.  

4. Pull Request Screenshots (`day91_prs.zip`)  
   - Zipped PNGs showing your pull requests and merge confirmation on the remote platform.  

5. Reflection (`day91_reflection.md`, 200 words)  
   - Challenges encountered with branching and conflict resolution, lessons learned, and how you’ll apply Git best practices in future projects.  

---  

By mastering these Git basics, you’ll maintain clean, reproducible code histories and collaborate effectively on epidemiological analyses and spatial workflows.
