# 💳 Credit Card Clustering – K-Means Project

A beginner-friendly machine learning project that groups credit card customers by similar usage and payment behavior using **K-Means Clustering**.

## Dataset

- **Source:** [Credit Card Dataset for Clustering (Kaggle)](https://www.kaggle.com/datasets/arjunbhasin2013/ccdata)
- **File:** `CC GENERAL.csv`
- **Size:** 8,950 customers and 18 columns

## Selected Features

- `PURCHASES_FREQUENCY` – how often customers make purchases
- `CASH_ADVANCE_FREQUENCY` – how often customers use cash advances
- `PRC_FULL_PAYMENT` – proportion of full payments
- `BALANCE_FREQUENCY` – how often a card balance is recorded

  This is **unsupervised learning**: there is no target variable (`y`)

## Workflow

1. Load and explore the CSV dataset with Pandas
2. Select four behavioral features and scale them using `StandardScaler`
3. Compare 2–8 clusters with the Elbow Method and Silhouette Score
4. Apply K-Means with **5 clusters**
5. Visualize and compare customer groups
6. Save the results to `credit_card_segments.csv`

## Results

| Cluster | Customers | Example profile |
|---|---:|---|
| 0 | 2,874 | Frequent purchases, low full-payment rate |
| 1 | 1,186 | Low balance activity and low card usage |
| 2 | 1,157 | Frequent purchases, high full-payment rate |
| 3 | 1,063 | Frequent cash advances, higher balances |
| 4 | 2,670 | Low purchase frequency, ongoing balances |

The **sampled Silhouette Score** for 5 clusters is approximately **0.442** (1,200 sampled customers, `random_state=42`). Seven clusters score slightly higher at **0.447**, but five were chosen for simpler interpretation. These scores are specific to this feature set and sampling method.


## Limitations

Customer segments depend on the selected features and scaling. Cluster IDs do not represent customer value or creditworthiness. This project is for learning and exploration, **not credit-risk assessment or automated lending decisions**.
