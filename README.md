# Credit Card Transaction & Customer Spending Analysis

## Business Problem
A financial services company wants to understand customer spending behaviour, identify high-value customers, track monthly transaction trends, and flag merchant categories driving most revenue.

## Objective
Analyse 50,000 real credit card transactions to uncover spending patterns, segment customers, detect anomalies, and provide actionable business recommendations.

## Dataset
- **Source:** Kaggle — Credit Card Transactions Dataset by Rajatsurana979
- **Size:** 50,000 transactions | 9 columns
- **Period:** January 2023 — October 2023

## Tools
- **PostgreSQL** — primary analysis engine
- **Python** (pandas, matplotlib, seaborn) — data loader + visualisations
- **Excel** — stakeholder KPI report

## Repository Structure
├── Creditcard.ipynb          # Main analysis notebook
├── transaction_analysis.png  # 4 key visualisations
├── credit_card_analysis.xlsx # Excel KPI report
└── README.md
## Analysis Workflow
- Layer 1 → PostgreSQL setup + data loading
- Layer 2 → Cleaned View creation with enriched columns
- Layer 3 → Customer spending segmentation
- Layer 4 → Merchant category performance
- Layer 5 → Monthly trend + MoM growth analysis
- Layer 6 → Age group segmentation
- Layer 7 → Anomaly detection using Z-scores

## Key Findings
1. **Travel dominates revenue** — $12.9M out of $22.1M total (58%) with avg transaction of $1,539
2. **Stable but not growing** — MoM growth oscillates between -8.41% and +11.59% with no multiplicative spike
3. **Pareto distribution** — Top 11.5% of customers drive 52% of total revenue
4. **Boomers lead spending** — 51-65 age group generates highest revenue at $5.74M
5. **Anomaly detection** — 20 high value transactions flagged (Z-score > 4), all in Travel category

## Business Recommendations
- Prioritise Travel category for premium card rewards and airline partnerships
- Launch retention programme for High tier customers — they generate 52% of revenue
- Target Low tier customers (76.7% of base) with cashback offers to move them up
- Acquire Gen Z customers now — lowest segment today but highest long term potential
- Implement category-specific Z-scores for more accurate fraud detection

## SQL Queries Written
| Query | Concept |
|-------|---------|
| Top 10 customers by spending | Basic aggregation |
| Monthly revenue trend | Date functions + GROUP BY |
| Category performance | RANK window function |
| Customer segmentation | NTILE window function |
| Month over Month growth | LAG window function + CTE |
| Spending tiers | CASE WHEN |
| Anomaly detection | Z-score + CROSS JOIN |

## How To Run
1. Open `Creditcard.ipynb` in Google Colab
2. Upload `credit_card_transaction_flow.csv` to Colab
3. Run Master Cell first — installs PostgreSQL and loads data
4. Run cells 2-15 in order

### Author
Abhishek Kale
[GitHub](https://github.com/kaleabhishek)
