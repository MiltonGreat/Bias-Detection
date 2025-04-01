# Bias Detection in Credit Approvals

![screenshot-localhost_8888-2025 04 01-19_18_35](https://github.com/user-attachments/assets/a25f8e65-d2c6-4c5f-a5cb-1b0d19b017c8)

### Project Overview

This project analyzes potential biases in loan approval decisions based on gender and age. Using the German Credit dataset, the study examines disparities in approval rates across different demographic groups and performs statistical significance tests to identify unfair treatment.
The scorecard is designed to provide an interpretable and data-driven approach to credit scoring, which can be used in financial lending and risk evaluation.

#### Objectives

- Calculate overall approval rates to establish baseline metrics.
- Analyze disparities by gender and age to detect potential biases.
- Perform statistical tests (e.g., Chi-square) to determine significance.
- Compute Disparate Impact Ratios to quantify bias.
- Recommend strategies for fairer lending decisions.

### Dataset

The dataset contains credit application information, including applicant demographics, financial status, and loan outcomes. Key variables include:

- Age
- Gender
- Credit History
- Employment Duration
- Loan Amount
- Default (Target Variable: 1 = Default, 0 = No Default)

### Methodology

1. Data Preprocessing
- Column names were mapped from German to English.
- Missing values were handled through data cleaning.
- Age was categorized into groups for better comparison.
- Gender was extracted from encoded categorical data.

2. Bias Analysis
- Overall Approval Rate Calculation
- Approval Rates by Gender and Age Group
- Chi-Square Test for Statistical Significance
- Disparate Impact Ratio Calculation
- Intersectional Analysis (Gender & Age)
- Visualization using Heatmaps

### Key Findings

- Overall Approval Rate: 30.00%
- Gender Bias: Present (Female applicants had higher approval rates)
- Age Bias: Present (Older applicants faced lower approval odds)
- Intersectional Effects: Compounding biases were detected across gender and age groups.
- Disparate Impact Analysis: Several age groups had ratios below 0.8, indicating potential discrimination.

### Recommendations

- Review and refine approval criteria to reduce bias.
- Implement fairness-aware algorithms for lending decisions.
- Conduct periodic bias audits to track fairness over time.
- Explore alternative creditworthiness indicators that are less prone to historical biases.

### Conclusion

This project demonstrates how data-driven fairness analysis can uncover biases in credit approval processes. By applying statistical and machine learning techniques, we can create more equitable financial systems and ensure fair treatment for all applicants.

### Source

![German Credit Data from Kaggle](https://www.kaggle.com/datasets/varunchawla30/german-credit-data)
