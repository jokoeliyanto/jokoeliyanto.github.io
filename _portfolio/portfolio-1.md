---
title: "Credit Card Default Prediction Using Machine Learning"
excerpt: "<img src='/images/credit_card_default_ml.png'>"
collection: portfolio
---


Business Understanding
====== 

**Problem Statement**

The bank faces challenges in assessing creditworthiness due to a manual and traditional credit scoring process. This leads to slow credit evaluation, limited accuracy, and an inability to differentiate risk levels among borrowers. As a result, the bank may grant loans to high-risk customers, which can lower portfolio quality and increase financial losses.

**Business Objective & Goal**

1. Develop a ML model to predict customer default probability with at least 85% accuracy within 3 months.
2. Reduce credit scoring time from about 2 hours to under 10 minutes through automation.
3. Segment customers by risk level (low, medium, high) based on that ML model

---

Data Understanding
====== 
The dataset used is **Default of Credit Card Clients** from the [UCI Machine Learning Repository](https://doi.org/10.24432/C55S3H), containing **30,000 records**.  
The target variable is `default.payment.next.month` (1 = default, 0 = no default).  

It includes **23 explanatory variables**, with highlights as follows:

| Code | Variable Name | Description | Type |
|------|---------------|-------------|------|
| X1   | Credit Limit  | Credit amount granted (NT$) | Numeric |
| X2   | Gender | 1 = male, 2 = female | Categorical |
| X3   | Education | 1 = graduate school, 2 = university, 3 = high school, 4 = others | Categorical |
| X4   | Marital Status | 1 = married, 2 = single, 3 = others | Categorical |
| X5   | Age | Age of client in years | Numeric |
| X6–X11 | Payment Status (Apr–Sep 2005) | Repayment history: -1 = on time, 1 = one-month delay, etc. | Ordinal |
| X12–X17 | Bill Statement Amounts (Apr–Sep 2005) | Monthly bill amounts (NT$) | Numeric |
| X18–X23 | Payment Amounts (Apr–Sep 2005) | Monthly repayment amounts (NT$) | Numeric |

---


Reference
====== 
Yeh, I. (2009). *Default of Credit Card Clients* [Dataset]. UCI Machine Learning Repository.  
👉 https://doi.org/10.24432/C55S3H
