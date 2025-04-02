# Bias Detection in Credit Approvals

![screenshot-localhost_8888-2025 04 02-07_48_17](https://github.com/user-attachments/assets/848020bf-35bb-4bad-a75e-e07e5808cfed)

### Project Overview

This project analyzes potential biases in loan approval decisions based on gender and age. Using the German Credit dataset, the study examines disparities in approval rates across different demographic groups and performs statistical significance tests to identify unfair treatment.

This project can help financial institutions:

- Audit credit models for gender/age biases
- Quantify approval rate disparities
- Generate regulatory-ready fairness reports
- Implement bias mitigation strategies

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

**Classification Report**
- High false negatives for Class 0: Only catches 27% of good applicants
- Over-prediction of defaults: 94% recall for defaults suggests aggressive risk-aversion
- Accuracy is misleading: 74% looks decent but masks poor non-default detection

**Gender Bias Analysis**
- Both genders under-approved: Model approves only ~12% vs actual 29-34%
- Male applicants: Higher false denials (FPR 81.1% vs 71.9%), but slightly better approval rates (+3.6% disparity)
- Statistical parity: Minimal difference (0.006), but error rates favor females (1.13× lower)

**Age Group Bias Analysis**
- Young applicants (18-25): Highest actual approval (38.6%) but still under-predicted (12.4%). Highest false denials (FPR 78%).
- Older applicants (51+): Lowest model approval (10.4%). Best FNR (1.5%) - model is most accurate here.
- Statistical parity: 26-35 group is reference point; 18-25 has 1.3× higher approval ratio

### Conclusion

This project demonstrates how data-driven fairness analysis can uncover biases in credit approval processes. By applying statistical and machine learning techniques, we can create more equitable financial systems and ensure fair treatment for all applicants.

### Source

![German Credit Data from Kaggle](https://www.kaggle.com/datasets/varunchawla30/german-credit-data)
