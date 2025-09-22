---
title: "Credit Default Risk Prediction"
excerpt: "Credit Default Prediction with Machine Learning<br/><img src='/images/credit-default.png'>"
collection: portfolio
---

## Credit Default Prediction with Machine Learning

### Business Understanding
In the banking industry, **credit default risk** is one of the biggest challenges. When borrowers fail to repay their loans or credit card obligations, banks face:

- Direct financial losses  
- A decline in loan portfolio quality  
- Increased cost of loss reserves  

Traditionally, credit scoring systems classify applicants into *eligible* or *not eligible*. However, this binary approach does not capture the variation in risk. For example, a borrower with a **10% default probability** is different from one with **40%**, even though both may be categorized as *eligible*.  

With Machine Learning, banks can:

- Predict the **probability of default** for each customer instead of a binary classification.  
- Improve risk management accuracy.  
- Optimize loan portfolios by adjusting credit limits, interest rates, or additional requirements according to risk levels.  
- Reduce losses and increase long-term profitability.  

**Key business questions that ML models can answer:**

1. Who are the customers with the highest risk of default?  
2. What is the probability of default for each borrower?  
3. How can banks balance credit growth with risk management?  

With these insights, management can build a more **data-driven credit strategy** that is fairer, more accurate, and sustainable.

---

### Data Understanding
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

### Reference
Yeh, I. (2009). *Default of Credit Card Clients* [Dataset]. UCI Machine Learning Repository.  
👉 https://doi.org/10.24432/C55S3H
