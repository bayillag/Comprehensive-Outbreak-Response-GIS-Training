# **Day 97 – Integrating Colab with Google Drive & GitHub**
  
Bloom Level: Apply & Create | Duration: 4 hrs  

---

## Objectives  

- Mount and manage Google Drive within Colab for persistent storage.  

- Clone, pull, and push GitHub repositories directly from a Colab notebook.  

- Implement version control workflows (branching, committing, merging) in the Colab environment.  

- Automate synchronization between Drive and GitHub using Python scripts.  

- Handle merge conflicts and collaborate on notebooks via GitHub pull requests.  

---

## Agenda  

1. Lecture: Colab, Drive, and Git Architecture (30 min)  
   - Colab file system overview and Drive mounting  
   - Authentication methods: OAuth vs. SSH keys  
   - Git operations available in Colab  

2. Demo: Mounting & Cloning (30 min)  
   - Mount Google Drive and navigate to a working folder  
   - Clone a remote GitHub repo into Colab’s runtime  
   - Inspect notebook and data files  

3. Lab Part 1 – Drive-Backed Notebook Versioning (60 min)  
   - Save and checkpoint notebooks to Drive  
   - Initialize a Git repo in Drive, stage changes, and commit  
   - Push commits to GitHub using a personal access token  

4. Lab Part 2 – Automated Sync Script & Conflict Resolution (45 min)  
   - Write a Python script to pull updates and push new commits  
   - Simulate a merge conflict by editing the same notebook in two places  
   - Resolve the conflict via Colab’s terminal or notebook interface  

5. Discussion & Q&A (15 min)  
   - Best practices for collaborative notebook development  
   - Security considerations for storing tokens and keys  
   - Strategies for continuous integration of notebooks  

---

## Exercise Details  

**Data Provided:**  

| Item                          | Description                                               |
|-------------------------------|-----------------------------------------------------------|
| `colab_template.ipynb`        | Starter notebook with placeholders for each integration step  |
| `github_repo_url.txt`         | Text file containing the URL of the sample GitHub repo    |
| `sample_data.csv`             | Example dataset to use and commit in the notebook         |

**Key Tasks:**  

- Authenticate and mount Google Drive at `/content/drive`.  

- Clone the sample GitHub repository into a Drive folder.  

- Modify the notebook and stage changes using Git commands in notebook cells or terminal.  

- Push updates back to the remote repository using a stored personal access token.  

- Create a Python script (`sync.py`) that automates `git pull` and `git push` on demand.  

- Introduce and resolve a merge conflict by editing the notebook from two browser sessions.  

---

## Assignment  

Submit to `assignments/day97/` by Day 98 morning:  

1. Integration Notebook  
   - `day97_colab_github_integration.ipynb` with annotated cells for mounting, cloning, Git operations, and conflict resolution.  

2. Sync Script  
   - `day97_integration_script.py` implementing automated pull/push logic with logging.  

3. Usage Documentation  
   - `day97_usage.md` detailing setup steps, authentication methods, and commands for Colab-Git integration.  

4. Git Commit Log  
   - `day97_git_log.txt` showing the sequence of commits, merges, and conflict resolutions.  

5. Reflection  
   - `day97_reflection.md` (200 words) on the challenges of notebook versioning, security considerations, and tips for collaborative workflows.  

---

By completing this session, you’ll establish a robust workflow for version-controlling Colab notebooks via Google Drive and GitHub—enabling seamless collaboration and reproducible research.
