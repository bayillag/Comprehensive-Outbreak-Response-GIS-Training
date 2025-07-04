# **Day 39 – Decision Analysis and Cost‐Effectiveness**

Bloom Level: Evaluate & Apply | Duration: 4 hrs  

## Objectives  

- Explain decision analysis frameworks (decision trees, cost–benefit matrices) in animal health contexts.  

- Identify and categorize costs (direct, indirect, programmatic) and health outcomes (cases averted, DALYs).  

- Calculate cost‐effectiveness metrics such as incremental cost‐effectiveness ratio (ICER).  

- Perform sensitivity analyses (one‐way, probabilistic) to assess uncertainty in economic evaluations.  

## Agenda  

1. Lecture: Decision Analysis & Economic Evaluation (45 min)  
   - Decision tree structure and value of information  
   - Cost identification: vaccine, personnel, surveillance, indirect losses  
   - Outcome metrics: cases averted, disability‐adjusted life years (DALYs) in zoonoses  
   - Cost‐effectiveness: average vs incremental ratios  
   - Uncertainty analysis: one‐way sensitivity, Monte Carlo simulations  

2. Case Study: Foot‐and‐Mouth Disease Vaccination Strategies (30 min)  
   - Compare mass‐vaccination vs ring‐vaccination for herd protection  
   - Review published ICER and budget‐impact findings  

3. Group Exercise: Building a Decision Tree (45 min)  
   - Define decision nodes, chance nodes, and terminal outcomes  
   - Assign probabilities and costs for two intervention arms  
   - Compute expected costs and health outcomes  

4. Interactive Demo: Economic Modeling in R/Python (60 min)  
   - R: `dectree` or `heemod` package workflows  
   - Python: custom `tree` functions or `SimPy` for Monte Carlo  
   - Calculate ICER and generate cost‐effectiveness acceptability curves (CEAC)  

5. Discussion & Q&A (30 min)  
   - Interpreting ICER relative to willingness‐to‐pay thresholds  
   - Balancing cost, feasibility, and impact in resource‐limited settings  
   - Communicating economic findings to decision‐makers  

---

## Exercise Details  

**Data Provided:**  
- `day39_costs.csv`: intervention cost components by category  
- `day39_effects.csv`: cases averted, DALYs prevented per scenario  
- Templates: `day39_decision_template.R` and `day39_decision_template.py`  

**Key Tasks:**  
1. Construct a decision‐tree schematic for two control strategies.  
2. Populate the tree with probabilities and cost/outcome values.  
3. Compute expected cost, expected effect, and ICER for each branch.  
4. Conduct one‐way sensitivity analyses on key parameters (vaccine cost, efficacy).  
5. Run probabilistic sensitivity analysis (Monte Carlo) to generate CEAC.  

---

## Assignment  

Submit to `assignments/day39/` by Day 40 morning:

1. Decision Tree Model (`day39_decision_tree.R` or `day39_decision_tree.py`)  
2. Cost‐Effectiveness Results (`day39_ce_results.csv`)  
3. Sensitivity Analysis Script (`day39_sensitivity.R` or `day39_sensitivity.py`)  
4. Visual Outputs:  
   - Tornado Diagram (`day39_tornado.png`)  
   - Cost‐Effectiveness Acceptability Curve (`day39_ceac.png`)  

5. Analytical Report (`day39_report.md`)  
   400–500 words summarizing methods, ICER findings, and policy implications.  

6. Reflection (`day39_reflection.md`)  
   200 words on challenges balancing cost constraints with outbreak control benefits.
