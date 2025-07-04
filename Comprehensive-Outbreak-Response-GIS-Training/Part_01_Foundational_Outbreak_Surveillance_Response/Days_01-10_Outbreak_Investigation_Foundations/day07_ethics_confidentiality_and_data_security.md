# **Day 7 – Ethics, Confidentiality, and Data Security**

Bloom Level: Apply | Duration: 4 hrs  

## Objectives  

- Understand ethical principles in animal disease investigations, including animal welfare, community consent, and data stewardship.  

- Explain confidentiality protocols such as de-identification, role-based access, and data-sharing agreements.  

- Demonstrate data security practices: encryption at rest/in transit, secure authentication, and backup strategies.  

- Apply international and national guidelines (WOAH standards, national veterinary acts) to outbreak data management workflows.  

---  

## Agenda  

1. Lecture: Ethics and Data Governance (45 min)  
   - Core bioethical tenets: beneficence, justice, respect for farmers and animals  
   - Regulatory frameworks: WOAH guidelines, regional/national policies  

2. Case Study: Data Breach in a Zoonotic Outbreak (30 min)  
   - Analyze an incident where farm identities were exposed  
   - Discuss consequences for trust, reporting, and control efforts  

3. Group Exercise: Drafting a Data Governance Framework (45 min)  
   - Define user roles, permissions, data lifecycle, and retention policies  
   - Develop consent forms and information sheets for field teams  

4. Interactive Demo: Implementing Security Controls (60 min)  
   - Encrypt a sample line list and set file‐level passwords  
   - Configure role-based access in PostgreSQL/PostGIS  

5. Discussion & Q&A (30 min)  
   - Balancing transparency, data sharing, and confidentiality  
   - Building community trust through ethical practices  

---  

## Exercise Details  

Data Provided:  
- `day07_linelist.csv`: Sample case list with farm coordinates and contact details  
- `data_sharing_agreement.docx`: Template for stakeholder data-use agreements  

Key Tasks:  
1. Anonymize or pseudonymize the sample dataset to protect identities.  
2. Draft a one-page data governance plan specifying access levels and retention rules.  
3. Encrypt the anonymized file and demonstrate a secure transfer workflow.  

---  

## Assignment  

Submit to `assignments/day07/` by Day 8 morning:  

1. Data Governance Plan (`day07_datagov.md`)  
   400–500 words covering ethical guidelines, consent procedures, and role-based controls.  

2. Anonymized Dataset (`day07_anonymized.csv`)  
   Masked or pseudonymized version of the provided line list.  

3. Security Implementation Guide (`day07_security.md`)  
   Step-by-step on file encryption, password policy, and database permission setup.  

4. Reflection (`day07_reflection.md`)  
   200 words on ethical challenges and the importance of confidentiality in animal health surveillance.