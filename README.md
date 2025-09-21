# ChildLabour-Migration-Analytics

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

*A data-driven exploration of the links between migration, education, and child labour, using household and child-level survey dat.*

---

## Table of Contents

- [About](#about)  
- [Motivation](#motivation)  
- [Data & Usage Restrictions](#data--usage-restrictions)  
- [Notebooks & Workflow](#notebooks--workflow)  
- [Key Findings](#key-findings)  
- [Technology & Tools](#technology--tools)  
- [How to Run / Reproduce](#how-to-run--reproduce)  
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

Insights are drawn from children involved in **economic activities (labour):**

---

### Age-wise Schooling & Dropout Patterns

| Age Group | Enrolled | Dropped Out | Never Enrolled | Key Risks |
|-----------|----------|-------------|----------------|-----------|
| 6–10 yrs  | 67% (1,812) | 13% (361) | 19% (518) | Early exclusions → high risk of entering child labour young |
| 11–14 yrs | 71% (4,150) | 24% (1,413) | 5% (275) | Vulnerable due to family responsibilities & economic hardship |
| 15–18 yrs | 46% (3,761) | 50% (4,047) | 2% (156) | Highest dropout; many already in hazardous/exploitative labour |

🔹 **Recommendations:**  
- 6–10 yrs → Flexible school timings, midday meals, family livelihood support.  
- 11–14 yrs → Counseling, retention programs, additional livelihood support.  
- 15–18 yrs → Bridge education, vocational training, stipend-based models.  

---

### Birth Registration & Identity

| Status              | Share of Children | Implications |
|---------------------|-------------------|--------------|
| Registered Birth    | 68% (45,000+)     | Positive base for access to entitlements |
| Not Registered      | 32% (21,099)      | Legally invisible, vulnerable to exclusion |

🔹 **Recommendations:**  
- Leverage registered children for **Aadhaar, schooling, health, protections**.  
- Prioritize **registration drives** in rural/migrant-heavy areas.  

---

### Parental Education & Child Labour

| Father’s Education  | Share of Working Children | Key Insight |
|---------------------|---------------------------|-------------|
| Illiterate          | 27.1% (21,163)           | Strongest link to child labour; unstable livelihoods & low awareness |
| Class 1–5           | 35.6% (27,382)           | Early-grade schooling gives little protection without economic stability |
| Graduate & Above    | 3.5% (2,807)             | Strong inverse correlation with child labour |

---

### Overall Education Status

| Status         | Share of Children | Notes |
|----------------|-------------------|-------|
| Enrolled       | ~87% (192,034)    | Majority successfully engaged in school |
| Dropped Out    | ~7% (15,439)      | Significant group needing re-enrollment |
| Never Enrolled | ~2% (4,012)       | Critical group at risk of long-term exclusion |

🔹 **Recommendations:**  
- Dropout tracing, counseling, flexible education (open schooling, vocational).  
- Enrollment drives in **remote, migrant, marginalized** areas.  

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
