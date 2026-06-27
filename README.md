# Customer Churn Prediction

Predicting which customers are likely to cancel their subscription using machine learning, based on the Telco Customer Churn dataset.

---

## Problem Statement
Customer churn is one of the most critical business problems in subscription-based services. Identifying high-risk customers early allows businesses to take proactive retention actions before losing them.

---

## Dataset
- **Source:** [Telco Customer Churn — Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Size:** 7,032 rows, 21 columns
- **Target:** Churn (Yes/No)

---

## Workflow
1. Data loading and exploration
2. Data cleaning — fixed TotalCharges string issue, dropped 11 null rows
3. Exploratory Data Analysis — churn by contract, tenure, monthly charges
4. Preprocessing — encoding, train/test split, scaling
5. Modeling — Logistic Regression and Random Forest
6. Evaluation — AUC, confusion matrix, feature importance

---

## Results

Model : | Logistic Regression | AUC score : 0.832 |
Model : | Random Forest | AUC score : 0.817 |

**Final Model:** Logistic Regression with AUC of 0.832

---

## Key Findings
- Customers on **month-to-month contracts** churn significantly more than yearly contracts
- **New customers** (low tenure) are at the highest churn risk
- Higher **monthly charges** correlate with increased churn
- **Tenure** is the single most important predictor of churn

---

## Business Insight
> High-risk customer profile: New customers on month-to-month contracts paying high monthly charges on fiber optic internet.

**Recommendations:**
- Offer discounts to month-to-month customers in their first 3 months
- Target fiber optic customers with loyalty programs
- Focus retention efforts on customers with tenure under 12 months

---

## Libraries Used
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
