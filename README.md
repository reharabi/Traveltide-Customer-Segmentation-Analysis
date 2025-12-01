# TravelTide Rewards Program: Customer Segmentation for Personalized Marketing

## Project Description
This project was completed as a **Mastery Project for MasterSchool**.

It addresses a realistic marketing challenge: supporting the launch of a new customer rewards program for a simulated e-commerce client, **TravelTide**.  
The primary objective was to define distinct customer segments based on booking behavior, demographics, and spend profile, in order to create a **highly personalized rewards program**.  
The goal is to maximize customer sign-up by emphasizing the specific reward perk most relevant to each customer segment.

---

## Project Summary
- **Users Segmented:** 5,998 active users  
- **Segmentation Method:** Manual Hierarchical Segmentation (chosen over K-Means/PCA for better business interpretability)  
- **Number of Segments:** Six mutually exclusive groups  

### Key Insights
- **Data Filtration:** Dataset filtered to 5,998 active users (≥ 8 sessions, activity after Jan 4, 2023).  
- **User Engagement:** Bookers had a median of **22 page clicks**, vs. **8 clicks** for non-bookers → engagement strongly predicts conversion.  
- **Family Market:** 32.6% of users travel with children; they show high transaction values → premium segment.  
- **Model Failure:** K-Means clustering (even with PCA) failed to produce clear segments → business-logic-driven hierarchical model adopted.  
- **Strategic Recommendation:** Tailored incentives across all six segments are essential to maximize rewards program impact.  

---

## Deliverables
- [Executive Summary](https://github.com/reharabi/Traveltide-Customer-Segmentation-Analysis/blob/main/Traveltide%20Executive%20Summary%20(1).pdf/executive_summary.md)
- [Detailed Report](https://github.com/your-username/your-repo/blob/main/reports/detailed_segmentation_report.md)

### Notebooks
- [Data Prep & EDA](https://github.com/your-username/your-repo/blob/main/notebooks/traveltide-segmentation-analysis%20(3).ipynb)
- [ML Approach (Discarded)](https://github.com/your-username/your-repo/blob/main/notebooks/ML%20Approach.ipynb)
- [Final Segmentation Logic](https://github.com/your-username/your-repo/blob/main/notebooks/Customer%20Segmentation%20Final%20(1).ipynb)

---

## Installation and Dependencies
This project was executed in a standard Python data science environment (e.g., Jupyter, VS Code).

### Dependencies
| Library       | Purpose                                                                 |
|---------------|-------------------------------------------------------------------------|
| **Pandas**    | Data manipulation, feature aggregation, segment assignment/summary      |
| **NumPy**     | Numerical operations and array manipulation                            |
| **Scikit-learn** | K-Means clustering, PCA, StandardScaler for ML prototyping           |
| **Matplotlib / Seaborn** | Exploratory Data Analysis (EDA) visualizations              |

---

## Usage Instructions
1. **Environment Setup:** Ensure Python environment with required libraries installed.  
2. **Data Loading:** Load raw datasets (`sessions`, `users`, `flights`, `hotels`) into Pandas DataFrames.  
3. **Run EDA Notebook:** Execute `traveltide-segmentation-analysis (3).ipynb` sequentially → generates aggregated user-level features (`filtered_users_pd`).  
4. **Run Final Segmentation Notebook:** Apply `assign_final_segment_v4` on aggregated user data → produces final segments and summary table.  

---

## Directory Structure
```bash
.
├── notebooks/
│   ├── traveltide-segmentation-analysis (3).ipynb   # Data Prep & EDA
│   ├── ML Approach.ipynb                            # K-Means/PCA Attempt
│   └── Customer Segmentation Final (1).ipynb        # Final Hierarchical Logic
├── reports/
│   ├── executive_summary.md
│   └── detailed_segmentation_report.md
└── README.md
