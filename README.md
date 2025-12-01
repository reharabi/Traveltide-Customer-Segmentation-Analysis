#**TravelTide Rewards Program: Customer Segmentation for Personalized Marketing**

##Project Description

This project was completed as a Mastery Project for MasterSchool.

This project addresses a realistic marketing challenge: supporting the launch of a new customer rewards program for a simulated e-commerce client, TravelTide. It was executed based on a provided business scenario, with the primary objective being to define distinct customer segments based on their booking behavior, demographics, and spend profile, in order to create a highly personalized rewards program. The goal is to maximize customer sign-up by emphasizing the specific reward perk most relevant to each customer segment.

##Project Summary

The analysis successfully segmented 5,998 active users into six mutually exclusive groups using a Manual Hierarchical Segmentation approach, which provided greater business interpretability than an Unsupervised Machine Learning model (K-Means/PCA).

##Key Insights:

Data Filtration: The dataset was filtered to 5,998 active users by requiring a minimum of 8 sessions and activity after January 4th, 2023.

EDA Highlight (User Engagement): Users who successfully completed a booking had a median of 22.0 page clicks, significantly higher than non-bookers who had a median of just 8.0 clicks. High engagement is confirmed as a strong predictor of conversion.

The Family Market: Users traveling with children (32.6% of users) exhibit high transaction values, justifying their treatment as a premium, primary segment.

Model Failure: Traditional K-Means clustering (even after PCA dimension reduction) failed to generate clearly separable segments, leading to the adoption of a business-logic-driven Hierarchical Segmentation model.

Strategic Recommendation: The segmentation confirms the need for tailored incentives across all six customer groups to maximize the impact of the new rewards program.

##Deliverables

All documentation and notebooks are available in the repository folders linked below.

* Executive Summary: A concise, one-page summary of findings and recommendations. Read the Summary

* Detailed Report: An in-depth explanation of the methodology and segment profiles. Read the Full Report

* Notebooks:

Data Prep & EDA: traveltide-segmentation-analysis (3).ipynb
View Notebook (notebooks/traveltide-segmentation-analysis (3).ipynb)

ML Approach (Discarded): ML Approach.ipynb
View Notebook (notebooks/ML Approach.ipynb)

Final Segmentation Logic: Customer Segmentation Final (1).ipynb
View Notebook (notebooks/Customer Segmentation Final (1).ipynb)

Installation and Dependencies

This project was executed in a standard Python data science environment (e.g., Jupyter, Databricks).

Dependencies

Library

Purpose

Pandas

Data manipulation, feature aggregation, and final segment assignment/summary generation.

NumPy

Numerical operations and array manipulation.

Scikit-learn

K-Means clustering, PCA, and StandardScaler for ML prototyping.

Matplotlib / Seaborn

Exploratory Data Analysis (EDA) visualizations.

Usage Instructions

Environment Setup: Ensure a Python environment is configured with the necessary libraries installed (listed above).

Data Loading: Load the raw sessions, users, flights, and hotels datasets into Pandas DataFrames.

Run traveltide-segmentation-analysis (3).ipynb: Execute this notebook sequentially to perform data cleaning, filtering, and create the aggregated user-level features (filtered_users_pd). This generates the core feature set.

Run Customer Segmentation Final (1).ipynb: Apply the assign_final_segment_v4 function on the aggregated user data to generate the final segments and the segment summary table.

Directory Structure (Conceptual)

.
├── notebooks/
│   ├── (combined) traveltide-segmentation-analysis (3).ipynb   # Data Prep & EDA
│   ├── ML Approach.ipynb                                      # K-Means/PCA Attempt
│   └── Customer Segmentation Final (1).ipynb                    # Final Hierarchical Logic
├── reports/
│   ├── executive_summary.md
│   └── detailed_segmentation_report.md
└── README.md
