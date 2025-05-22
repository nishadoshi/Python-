# Customer Repurchase Prediction – UK Online Retail Data

This project analyzes customer transaction data from a UK-based online retail store to predict whether a first-time buyer will make a repeat purchase. The goal is to uncover patterns in customer behavior and build a machine learning model that can help identify potential returning customers.

---

##  Dataset

The dataset is sourced from the UCI Machine Learning Repository and includes transactional records for a UK-based online retailer between 2010 and 2011. Key fields include:

- **InvoiceDate**
- **CustomerID**
- **Product Description**
- **Quantity**
- **UnitPrice**
- **Country**

---

## Data Cleaning

- Removed rows with missing `CustomerID`
- Filtered out records with `Quantity <= 0` or `UnitPrice <= 0`
- Converted `InvoiceDate` to datetime format
- Created `TotalPrice` = `Quantity * UnitPrice`

---

## Exploratory Data Analysis (EDA)

- Identified top-selling products by revenue and quantity
- Plotted total revenue over time
- Observed key insights such as:
  - "Dotcom Postage" had high revenue despite low quantity sold
  - Seasonal sales trends in late Q4

---

##  Feature Engineering

- Built **Recency**, **Frequency**, and **Monetary (RFM)** features per customer
- Created a binary target variable `returning_customer`, indicating if a customer made a repeat purchase

---

## Modeling

- Trained a **Random Forest Classifier** using RFM features
- Tuned hyperparameters using GridSearchCV
- Evaluated model using:
  - Confusion Matrix
  - Precision, Recall, F1 Score
  - Threshold tuning to reduce false positives
  - ROC & threshold-vs-metrics plot

---

##  Key Results

- Achieved best F1 score (0.813) at a threshold of 0.50
- Explored alternative thresholds to reduce false positives
- Precision vs Recall tradeoff visualized to guide future strategy

---

##  Tools Used

- Python (Pandas, Scikit-learn, Matplotlib, Seaborn)
- Jupyter Notebook

---

## Contact

Feel free to reach out if you'd like to collaborate or discuss the project!

