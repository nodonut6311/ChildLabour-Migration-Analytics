# Child Labour and Migration Analysis

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

*A data-driven exploration of the links between migration, education, and child labour, using household and child-level survey data.*

---

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

Insights are drawn from children involved in **economic activities (labour)**:

### Age-wise Schooling & Dropout Patterns
- **6–10 years**  
  - 1,812 enrolled, but **361 dropped out** and **518 never enrolled**.  
  - Early exclusion puts children at **high risk of entering labour at a young age**.  
  - 🔹 *Recommendation:* Ensure flexible school timings, provide midday meals, and support family livelihoods to reduce push toward labour.

- **11–14 years**  
  - 4,150 enrolled, but **1,413 dropped out** and **275 never enrolled**.  
  - Highly vulnerable due to **family responsibilities** and **economic hardship**.  
  - 🔹 *Recommendation:* Expand livelihood support, counseling, and retention programs.

- **15–18 years**  
  - **4,047 dropped out**, surpassing **3,761 enrolled**, with **156 never enrolled**.  
  - Many already in **hazardous or exploitative labour**.  
  - 🔹 *Recommendation:* Introduce bridge education, vocational training, and stipend-based models to re-engage older adolescents.

---

### Birth Registration & Identity
- **68% (45,000+)** children have a registered birth → a **positive base** for access to entitlements.  
  - 🔹 *Recommendation:* Use this to link children with **Aadhaar, schooling, health benefits, and protection schemes**.  
- **32% (21,099)** lack registration → leaving them **legally invisible and vulnerable**.  
  - 🔹 *Recommendation:* Launch **birth registration drives** with government and local partners, especially in rural/migrant-heavy areas.

---

### Parental Education & Child Labour
- **27.1% (21,163)** of working children have **illiterate fathers** → strongest link to child labour.  
  - 🔹 *Insight:* Illiteracy often means unstable livelihoods and lack of awareness of rights/education benefits.  
- **35.6% (27,382)** have fathers educated only up to **Class 1–5** → early-grade education provides **little protection** against child labour without economic stability.  
- Only **3.5% (2,807)** of working children have fathers with **graduate or higher education** → confirming a **strong inverse correlation** between parental education and child labour.

---

### Overall Education Status
- **192,034** currently enrolled → strong engagement achieved.  
- **15,439** have dropped out → requiring **targeted re-enrollment**.  
  - 🔹 *Recommendation:* Implement dropout tracing, counseling, and flexible education pathways.  
- **4,012** never enrolled → at **highest risk of long-term exclusion**.  
  - 🔹 *Recommendation:* Partner with governments/communities for **enrolment drives** in remote, migrant, or marginalized areas.

---

## Technology & Tools

- **Language & runtime**: Python (Jupyter Notebooks)  
- **Data manipulation**: pandas, numpy  
- **Visualization**: matplotlib, seaborn 
- **Other tools**: scikit-learn, statsmodels 

---

## How to Run / Reproduce

1. **Prerequisites**  
   - Python ≥ 3.x  
   - Install dependencies (from `requirements.txt` if available, or manually: `pandas`, `numpy`, `matplotlib`, `seaborn`, etc.)

2. **Clone the repository**

   ```bash
   git clone https://github.com/nodonut6311/Child-Labour-and-Migration-Analysis.git
   cd Child-Labour-and-Migration-Analysis
