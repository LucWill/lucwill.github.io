---
layout: post
title: "(Un)satisfied? Why Job Satisfaction Is Hard to Predict"
date: 2025-03-28
categories: [Data Science, Analysis]
tags: [job satisfaction, data science, regression, limitations]
---

![Title Image](/assets/images/job-satisfaction/A_photograph_of_a_crumpled_piece_of_standard_graph.png)

*How satisfied are we with our jobs? And can this satisfaction be predicted from objective data?*
As part of my Data Science course, I set out to explore this question — and learned that data doesn’t always give us the answers we expect.

---

## 🎯 Business Question

**Can we predict developers' job satisfaction based on demographic and professional variables?**
If so, which factors have the greatest impact?

---

## 📄 The Data

The analysis is based on the [StackOverflow Developer Survey](https://insights.stackoverflow.com/survey), one of the largest surveys of software developers worldwide.
The dataset contains over 65,000 responses, covering:
- Professional experience
- Working hours
- Salary
- Company size
- Tools used
- And more

Important: Only about **30,000** participants provided information about their **Job Satisfaction**.

---

## 🔍 Approach

### 1. **Data Cleaning**
I simplified and prepared the dataset:
- Removed or encoded categorical variables
- Replaced missing values with averages or assigned specific categories
- Focused on numerical variables

### 2. **Modeling**
I attempted to build a regression model to predict **Job Satisfaction** (on a scale from 0 to 10):
- First using **Linear Regression**
- Then using a **Random Forest Regressor**  
**Result:** Both models performed poorly.

---

## 📊 Results & Visualizations

### Job Satisfaction Distribution

Most respondents rate their job satisfaction in the upper range of the scale:

![Job Satisfaction Distribution](/assets/images/job-satisfaction/job_sat_distribution.png)

---

### Influencing Factors

A Random Forest model reveals the **top factors influencing job satisfaction**:

![Feature Importance](/assets/images/job-satisfaction/feature_importance.png)

Interestingly:
- Salary and work experience play a role.
- Subjective self-assessments such as **Purchase Influence** or **JobSatPoints** appear.
- However, **no single feature is dominant** — the model struggles to explain much of the variance.

---

### Correlations

A correlation analysis supports this finding:  
**The correlations between job satisfaction and other variables are very weak.**  
Only self-assessed influence in the company shows a slight correlation.

---

## ❗️ Key Insights

**The main takeaway of my analysis is:**
> **The available data is not suitable for reliably predicting job satisfaction.**

**Why?**
- Only half of the respondents provided job satisfaction ratings.
- Job satisfaction is a subjective, complex phenomenon not easily captured by objective metrics.
- Crucial factors (e.g., team dynamics, leadership, personal values) are not covered in the dataset.

---

## 🚀 Next Steps

A more meaningful analysis would require:
- A higher response rate for job satisfaction
- Inclusion of qualitative factors
- An analysis of free-text responses using **Natural Language Processing (NLP)**

---

## 💡 Conclusion

Sometimes the most valuable insight in a data science project is realizing **where the limits of data-driven analysis lie.**
That is exactly what I learned in this project — and I want to share this as a reminder:  
**Not every problem can be solved with data.**

---

### 📂 Appendix

All data and visualizations used in this analysis are available in this repository.
