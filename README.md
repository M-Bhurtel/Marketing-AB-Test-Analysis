# A/B Test Analysis for a Marketing Campaign

This repository contains a comprehensive analysis of a marketing A/B test. The goal is to determine if a new ad campaign resulted in a statistically significant increase in user conversions. The analysis concludes with a data-driven recommendation for business stakeholders.

---

## 📋 Table of Contents
- [Project Goal](#-project-goal)
- [Dataset](#-dataset)
- [Methodology](#-methodology)
- [Key Findings](#-key-findings)
- [Business Recommendation](#-business-recommendation)
- [Tools & Libraries](#-tools--libraries)
- [How to Run](#-how-to-run)

---

## 🎯 Project Goal

The primary objective of this analysis is to evaluate the effectiveness of a new ad campaign. By comparing the conversion rates of a treatment group (shown the new ad) against a control group (shown a PSA), we can determine if the campaign provides a positive return on investment and should be launched to a wider audience.

---

## 📊 Dataset

The dataset used for this analysis is `marketing_AB.csv`. It contains 588,101 records of user interactions during the A/B test.

**Columns:**
- `user_id`: Unique identifier for each user.
- `test_group`: Indicates whether the user was in the `ad` (treatment) or `psa` (control) group.
- `converted`: Boolean flag (`True`/`False`) indicating if the user made a purchase.
- `total_ads`: Total number of ads the user saw.
- `most_ads_day`: The day of the week the user saw the most ads.
- `most_ads_hour`: The hour of the day the user saw the most ads.

---

## ⚙️ Methodology

The analysis was conducted in a Jupyter Notebook (`Marketing_AB_Test.ipynb`) and follows a structured workflow:

1.  **Data Cleaning & Preparation:**
    - Loaded the dataset using Pandas.
    - Standardized column names and handled data type conversions.
    - Ensured data integrity by checking for duplicates and missing values.

2.  **Exploratory Data Analysis (EDA):**
    - Calculated and compared baseline conversion rates for both groups.
    - Visualized user distribution, ad exposure patterns, and peak activity times using Matplotlib.
    - Identified a significant sample size imbalance between the control and treatment groups, a key consideration for the analysis.

3.  **Statistical Inference:**
    - **Power Analysis:** Performed a retrospective power analysis to calculate the Minimum Detectable Effect (MDE), confirming the experiment's validity.
    - **Hypothesis Testing:** Conducted a one-sided Z-test for proportions to determine if the observed increase in conversion rate was statistically significant (α = 0.05).
    - **Confidence Interval:** Calculated a 95% confidence interval for the lift in conversion rates to quantify the effect size.

---

## 📈 Key Findings

The analysis confirmed that the new ad campaign was a success. The treatment group showed a statistically significant improvement in conversion rates compared to the control group.

| Metric | Control (PSA) | Treatment (Ad) |
| :--- | :---: | :---: |
| **Conversion Rate** | **1.79%** | **2.55%** |

**Statistical Test Results:**
- **Absolute Lift:** **+0.77%**
- **p-value:** **< 0.0001**
- **95% Confidence Interval for Lift:** **[0.60%, 0.94%]**

The p-value is significantly lower than the 0.05 alpha level, leading us to **reject the null hypothesis**. The confidence interval further supports this, indicating that the true lift is very likely to be positive and meaningful.



## 💡 Business Recommendation

### Recommendation
Based on the strong, statistically significant results, the recommendation is to **launch the new ad campaign to the wider user base.** The campaign has proven its effectiveness in driving a positive lift in user conversions.

### Proposed Next Steps
1.  **Return on Ad Spend (ROAS) Analysis:** To fully assess profitability, a follow-up analysis should incorporate the campaign's cost to calculate the ROAS.
2.  **User Segmentation Analysis:** Investigate if the ad's effectiveness differs across user segments (e.g., by peak activity hour or total ads seen) to optimize future ad spend and targeting.

---

## 🛠️ Tools & Libraries

- **Programming Language:** Python
- **Libraries:**
  - `pandas` for data manipulation.
  - `numpy` for numerical operations.
  - `matplotlib` for data visualization.
  - `scipy` and `statsmodels` for statistical analysis.


**Contact:**  Mohani Lal Bhurtel - https://www.linkedin.com/in/mohanibhurtel/
