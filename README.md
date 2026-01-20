# Customer Segmentation with RFM and k-NN

## Overview
This project performs customer segmentation and value prediction using retail transaction data. It combines the classic **RFM (Recency, Frequency, Monetary)** marketing framework with a **k-Nearest Neighbors (k-NN)** classifier to identify and predict high-value customers.

The goal is to demonstrate how transactional data can be cleaned, engineered, and modeled to support data-driven marketing and retention strategies. I didn’t change the core analysis, but I improved how it’s communicated and interpreted.

---

## Dataset
The dataset consists of retail transaction records with fields such as:
- Invoice number
- Invoice date
- Customer ID
- Quantity
- Unit price
- Country

Cancelled and refund transactions are removed to ensure analysis reflects real purchases.

---

## Methodology

### 1. Data Loading & Diagnostics
- Load Excel-based transactional data
- Inspect schema, shape, and basic distributions

### 2. Data Cleaning
- Remove cancelled/refunded invoices
- Drop transactions with missing customer identifiers
- Ensure numeric and date fields are properly formatted

### 3. Feature Engineering (RFM)
For each customer:
- **Recency**: Days since last purchase
- **Frequency**: Number of purchases
- **Monetary**: Total amount spent

These features capture purchasing behavior and customer value.

### 4. Customer Segmentation
- RFM metrics are scored using quantiles
- Customers are grouped into value segments
- High-value customers (top ~25%) are identified for targeted analysis

### 5. Machine Learning
- Train a **k-Nearest Neighbors (k-NN)** classifier using RFM features
- Predict customer value segments
- Evaluate performance using accuracy and classification metrics

---

## Key Insights
- A small percentage of customers account for a disproportionate share of revenue
- High-value customers tend to purchase more frequently and spend more per transaction
- RFM features are effective predictors of customer value when paired with simple ML models

---

## Technologies Used
- Python
- pandas, numpy
- matplotlib
- scikit-learn

---


## Use Cases
- Customer retention and loyalty programs
- Targeted marketing campaigns
- Customer lifetime value modeling
- Introductory customer analytics and ML demonstrations

---

## Next Steps
- Compare k-NN with other classifiers (logistic regression, trees, SVM)
- Add time-based validation
- Incorporate churn prediction
- Visualize segments more deeply with clustering techniques

---

### Future Enhancements with Deep Learning and Generative AI
While classical machine learning models were appropriate for this project,
future iterations could explore deep learning approaches if larger and richer
datasets become available.

Potential extensions include:
- Deep neural networks to capture nonlinear customer behavior patterns at scale
- Sequence-based models (e.g., RNNs or Transformers) to model purchase behavior over time
- Generative AI tools to automatically generate customer segment summaries
  for marketing and business stakeholders

These approaches were not implemented here due to the size of the dataset
and the importance of interpretability for business decision-making.
