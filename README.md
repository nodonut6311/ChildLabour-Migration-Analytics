# Child Labour and Migration Analysis

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

## Table of Contents

- [About](#about)  
- [Motivation](#motivation)  
- [Data & Usage Restrictions](#data--usage-restrictions)  
- [Notebooks & Workflow](#notebooks--workflow)  
- [Key Findings](#key-findings)  
- [Technology & Tools](#technology--tools)  
- [How to Run / Reproduce](#how-to-run--reproduce)  
- [Project Structure](#project-structure)  
- [Contributing](#contributing)  
- [License](#license)  

---

## About

This repository explores the relationship between **child labour** and **migration**, using household and child-level data collected through surveys.  
The goal is to clean, unify, and analyze the data to uncover patterns that may inform research, advocacy, or policy design related to children’s rights and welfare.

---

## Motivation

- Understand how household migration impacts the incidence of child labour.  
- Combine and unify quarterly datasets to build consistent long-term records.  
- Provide a reproducible workflow for cleaning, merging, and validating child and household-level data.  

---

## Data & Usage Restrictions

⚠️ **Important Notice**  
The datasets used in this project are the property of **Child Rights and You (CRY)** and its partner organizations.  

- The **raw and processed forms** (child and household) are **copyrighted** and cannot be redistributed.  
- This repository therefore only contains **code, workflows, and documentation**.  
- If you wish to use the data, you must obtain explicit permission from CRY and its partners.  

---

## Notebooks & Workflow

The analysis pipeline is modular, with each notebook performing a specific role:

| Notebook | Purpose |
| --- | --- |
| `pre_processing.ipynb` | Performs initial cleaning of quarterly data, including handling missing values, normalizing variables, and preparing the base datasets for unification. |
| `child_data_unified.ipynb` | Merges the cleaned quarterly data with **child forms**, using the *child beneficiary ID* as the key. This step expands the dataset by adding additional child-specific columns, producing a unified child-level dataset. |
| `household_data_unified.ipynb` | Merges the cleaned quarterly data with **household forms**, using the *household ID* as the key. This process resolves discrepancies, integrates non-repeating columns, and produces a consistent household-level dataset. |
| `test_cleaning.ipynb` | Runs duplicate removal and consistency checks on one quarter of the source data to validate the cleaning approach before scaling it across all quarters. |

This workflow ensures **scalability, reproducibility, and modularity**.

---

## Key Findings

*(To be filled in after your analysis results are finalized — examples might include):*

- Trends in child labour incidence across migrant vs non-migrant households.  
- Socio-economic factors most strongly correlated with child labour.  
- How discrepancies across quarterly data were resolved in the unified datasets.  

---

## Technology & Tools

- **Language & runtime**: Python (Jupyter Notebooks)  
- **Data manipulation**: pandas, numpy  
- **Visualization**: matplotlib, seaborn (if applicable)  
- **Other tools**: scikit-learn, statsmodels (if used)  

---

## How to Run / Reproduce

1. **Prerequisites**  
   - Python ≥ 3.x  
   - Install dependencies (from `requirements.txt` if available, or manually: `pandas`, `numpy`, `matplotlib`, `seaborn`, etc.)

2. **Clone the repository**

   ```bash
   git clone https://github.com/nodonut6311/Child-Labour-and-Migration-Analysis.git
   cd Child-Labour-and-Migration-Analysis

