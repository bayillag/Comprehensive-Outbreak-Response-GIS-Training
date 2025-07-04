# **Day 101 – Building & Sharing Kaggle Notebooks**
  
Bloom Level: Apply & Create | Duration: 4 hrs  

## Objectives  

- Configure and launch a new Kaggle Notebook with the appropriate kernel environment.  
- Import and mount datasets (Kaggle‐hosted and external) for analysis.  
- Structure notebooks with clear sections: narrative, code, outputs, and parameters.  
- Leverage Kaggle features: dataset versioning, notebook metadata, and GPU/TPU accelerators.  
- Publish, share, and collaborate on Notebooks using Kaggle’s discussion and version control tools.  

---

## Agenda  

1. Lecture: Kaggle Notebooks Fundamentals (45 min)  
   - Notebook environment versus local Jupyter/Colab  
   - Kaggle’s dataset attachments, versioning, and commit history  
   - Enabling accelerators and managing internet access  

2. Demo: Notebook Authoring Best Practices (30 min)  
   - Organizing content with Markdown, headings, and badges  
   - Parameterizing notebooks with `kaggle-script` metadata  
   - Using the Data Explorer and Output files panel  

3. Lab Part 1 – Creating Your First Notebook (60 min)  
   - Select or attach a target dataset via the Kaggle UI or API  
   - Write code to load data, perform a simple spatial plot, and record results  
   - Add narrative: objective, methods, and interpretation blocks  

4. Lab Part 2 – Publishing & Collaboration (45 min)  
   - Commit notebook versions and add descriptive changelog entries  
   - Share with the community: set visibility, add tags, and link to datasets  
   - Use the “Fork” feature to collaboratively improve a peer’s Notebook  

5. Discussion & Q&A (30 min)  
   - Strategies for reproducible parameter sweeps with Kaggle metadata  
   - Collaborating via comments, votes, and code reviews on Kaggle  
   - Integrating Kaggle Notebooks into larger CI/CD or pipeline workflows  

---

## Exercise Details  

| Item                       | Description                                                                 |
|----------------------------|-----------------------------------------------------------------------------|
| `day101_dataset_slug.txt`  | Text file containing the slug of the dataset to attach in your Notebook     |
| `day101_notebook_template.ipynb` | Starter notebook with placeholders for sections and metadata              |
| `day101_example_output/`   | Folder with example plots and tables to replicate or extend                 |

**Key Tasks:**  
- Attach the specified dataset using the Kaggle UI or `kaggle datasets attach` command.  
- Rename the Notebook with a descriptive title (`“Spatial Exploration – YourName”`).  
- Populate the template: load data, conduct a simple map or table, and explain findings.  
- Configure Notebook metadata: select accelerator, internet access, and add tags.  
- Commit and publish your Notebook; obtain the shareable URL.  

---

## Assignment  

Submit to `assignments/day101/` by Day 102 morning:  

1. Kaggle Notebook URL  
   - Link to your published notebook with public visibility.  

2. Notebook File  
   - `day101_spatial_notebook.ipynb` exported from Kaggle, containing code, outputs, and metadata.  

3. Collaboration Log (`day101_collab.md`)  
   - Record any forks, peer comments received, and how you addressed feedback.  

4. Example Outputs  
   - `day101_plot.png` and `day101_table.csv` generated within the Notebook.  

5. Usage Guide (`day101_usage.md`)  
   - Instructions on how to re‐run your Notebook: environment settings, parameters, and expected runtime.  

6. Reflection (`day101_reflection.md`, 200 words)  
   - Discuss challenges in adapting to the Kaggle interface, lessons on sharing, and how Notebook versioning inspired reproducibility.  

---

By the end of this session, you’ll be proficient at authoring, versioning, and sharing spatial analysis Notebooks on Kaggle—empowering collaborative, reproducible data science workflows.