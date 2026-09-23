# E-Commerce Customer Churn & Retention Analytics

**Author:** Aqsa Fatima  
**Year:** 2024

---

## Project Overview

A complete, end-to-end data analytics project that analyses customer purchasing behaviour, calculates business KPIs, segments customers using RFM analysis, investigates churn patterns, and builds machine learning models to predict customer churn. All findings are translated into concrete, actionable business recommendations.

---

## Project Description

This project uses a large e-commerce transaction dataset (250,000 records, 49,661 unique customers) spanning January 2020 to September 2023. The analysis follows a structured analytics pipeline:

**Data Cleaning → EDA → KPIs → Customer Segmentation → Churn Analysis → ML Modelling → Business Recommendations**

The project honestly evaluates the ML model's performance and explains why the model's predictive power is limited — not due to modelling errors, but because the churn label in this dataset shows near-zero correlation with available features (a characteristic of synthetically generated datasets). The core business value of the project lies in the KPI calculations, RFM segmentation, and actionable recommendations.

---

## Business Problem

> *Which customers are at risk of churning, and what business actions can reduce that risk?*

A 20% customer churn rate represents an estimated ~$136 million in lost Customer Lifetime Value (CLV). Understanding churn patterns and implementing targeted retention strategies is essential for business sustainability.

---

## Objectives

1. Clean and preprocess the raw dataset (missing values, data types, duplicate columns).
2. Explore purchasing patterns, revenue trends, and customer demographics.
3. Define and calculate core business KPIs (AOV, CLV, churn rate, return rate).
4. Segment customers using RFM (Recency, Frequency, Monetary) analysis.
5. Analyse churn across demographics, product categories, and payment methods.
6. Build and evaluate churn prediction models (Logistic Regression + Random Forest).
7. Deliver actionable business recommendations based on real data findings.

---

## Dataset

| Property | Value |
|----------|-------|
| **Name** | E-Commerce Customer Data for Behavior Analysis |
| **Source** | Kaggle |
| **Link** | https://www.kaggle.com/datasets/uom190346a/e-commerce-customer-behavior-dataset |
| **File** | `ecommerce_customer_data_large.csv` |
| **Rows** | 250,000 transactions |
| **Unique Customers** | 49,661 |
| **Date Range** | January 2020 – September 2023 |
| **Columns** | Customer ID, Purchase Date, Product Category, Product Price, Quantity, Total Purchase Amount, Payment Method, Age, Returns, Customer Name, Gender, Churn |

---

## Technologies Used

| Tool / Library | Purpose |
|----------------|---------|
| **Python 3.9+** | Core programming language |
| **Pandas** | Data loading, cleaning, manipulation |
| **NumPy** | Numerical operations |
| **Matplotlib** | Data visualisation |
| **Seaborn** | Statistical visualisation |
| **Scikit-learn** | Machine learning (Logistic Regression, Random Forest, evaluation metrics) |
| **Jupyter Notebook** | Interactive development environment |

---

## Project Structure

```
Project/
│
├── AqsaFatima_EcommerceChurnAnalytics.ipynb   # Main Jupyter Notebook
├── AqsaFatima_ProjectReport.docx              # Full project report (Word)
├── README.md                                   # This file
├── requirements.txt                            # Python dependencies
└── ecommerce_customer_data_large.csv          # Dataset (place here before running)
```

Charts saved as PNG files during notebook execution:
- `fig_monthly_revenue.png`
- `fig_category_revenue.png`
- `fig_order_distribution.png`
- `fig_demographics.png`
- `fig_payment_methods.png`
- `fig_returns_by_category.png`
- `fig_rfm_segments.png`
- `fig_age_gender_spending.png`
- `fig_payment_by_age.png`
- `fig_churn_overview.png`
- `fig_churn_breakdown.png`
- `fig_churn_rfm.png`
- `fig_model_evaluation.png`
- `fig_feature_importance.png`

---

## Setup & Installation Instructions

### Prerequisites

- Python 3.9 or higher
- pip (Python package manager)
- Jupyter Notebook or JupyterLab

### Step 1 — Clone or Download the Project

Download or copy all project files into a single directory.

### Step 2 — Install Dependencies

Open a terminal in the project directory and run:

```bash
pip install -r requirements.txt
```

### Step 3 — Place the Dataset

Ensure the dataset file `ecommerce_customer_data_large.csv` is in the **same directory** as the notebook.

> Download from: https://www.kaggle.com/datasets/uom190346a/e-commerce-customer-behavior-dataset

### Step 4 — Launch Jupyter Notebook

```bash
jupyter notebook
```

Then open `AqsaFatima_EcommerceChurnAnalytics.ipynb` in the browser.

---

## How to Run the Notebook

1. Open the notebook in Jupyter.
2. Click **Kernel → Restart & Run All** to execute all cells from top to bottom.
3. All outputs, charts, and model results will appear inline.
4. Chart PNG files will be saved in the same directory.

The notebook is designed to run **end-to-end without any manual edits** — all paths are relative and all required libraries are standard.

---

## Key KPIs

| KPI | Value |
|-----|-------|
| Total Revenue | ~$681 Million |
| Total Transactions | 250,000 |
| Unique Customers | 49,661 |
| Avg Order Value (AOV) | ~$2,725 |
| Avg Transactions / Customer | ~5 |
| Estimated Customer Lifetime Value (CLV) | ~$13,703 |
| Return Rate | ~50% |
| Customer Churn Rate | ~20% |

---

## Key Insights

1. **~20% Churn Rate = ~$136M in Lost CLV**: Approximately 9,929 of 49,661 customers have churned. At a CLV of ~$13,700, this represents enormous lost revenue potential.

2. **Revenue is Stable but Flat**: Monthly revenue held steady at ~$15M throughout 2020–2023 with no growth trend. This signals a business that is maintaining rather than growing its customer base.

3. **50% Return Rate is a Critical Risk**: Half of all transactions result in a return. This is a systemic operational problem affecting all four product categories equally.

4. **Diversified Revenue is a Strength**: Books, Clothing, Electronics, and Home each contribute ~25% of total revenue. No single category dominates.

5. **Young and Older Customers Churn Slightly More**: Ages 18-25 (21.1%) and 56-70 (20.5%) show marginally higher churn. Targeted retention for these groups is warranted.

6. **ML Churn Model is Limited by Data**: All available features show near-zero correlation with Churn (|r| < 0.01). Both ML models achieve ~0.50 ROC-AUC — consistent with random prediction. Richer behavioural data is required for a useful predictive model.

---

## Business Recommendations

| # | Recommendation | Expected Impact |
|---|---------------|-----------------|
| R1 | Launch tiered Loyalty Programme for Champion & Loyal segments | Increase average transactions per customer, reduce churn |
| R2 | Run personalised Win-Back campaigns for At Risk & Lost segments | Recover a portion of at-risk CLV |
| R3 | Investigate and reduce ~50% return rate (product quality, descriptions, size guides) | Lower logistics costs, improve customer satisfaction |
| R4 | Design age-targeted retention offers for 18-25 and 56-70 groups | Reduce above-average churn in these age groups |
| R5 | Launch revenue growth initiatives (new categories, promotions, subscriptions) | Break flat revenue trend |
| R6 | Collect richer behavioural data (NPS, session time, support tickets) | Enable genuinely predictive churn modelling |

---

## Notes

- Do **not** create a GitHub repository from this README. The repository will be created and managed separately.
- The notebook file path assumes `ecommerce_customer_data_large.csv` is in the same directory. Update the path in Section 2 of the notebook if your file is located elsewhere.
- All results are computed from the actual dataset. No data was fabricated or invented.
