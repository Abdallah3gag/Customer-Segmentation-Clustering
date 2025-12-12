# Credit Card Customer Segmentation Using Machine Learning

This project applies **machine learning clustering techniques** to segment credit card users based on their
spending behavior, cash withdrawals, payments, and credit activity. By leveraging **K-Means** and **Hierarchical Clustering**
I identify distinct customer groups to understand financial behavior, assess risk levels, and provide actionable business insights.

---

## Project Objectives

- Segment credit card customers into meaningful behavioral groups  
- Analyze spending patterns, cash advance usage, and repayment habits  
- Compare the performance of K-Means and Hierarchical Clustering  
- Provide insights for risk management and targeted marketing strategies  

---

## Dataset Overview

The dataset contains anonymized financial data of credit card users, including:

- **BALANCE** – Outstanding balance on the card  
- **PURCHASES** – Total amount spent on purchases  
- **CASH_ADVANCE** – Total cash withdrawn
- **CREDIT_LIMIT** – Maximum allowed spending  
- **PAYMENTS** – Amount repaid to the bank  
- Additional frequency-based features such as purchase and cash advance frequency  

These features describe each customer’s credit card usage and behavior.

---

## Data Preprocessing

Several preprocessing steps were applied to prepare the data for clustering:

### 1. Handling Missing Values

### 2. Handling Outliers

### 3. Scaling the Data

### 4. Dimensionality Reduction (PCA)
- **Principal Component Analysis (PCA)** was applied to reduce dimensionality, remove noise
-  and improve cluster separation while retaining most of the variance.

---

## Clustering Models

### K-Means Clustering
- Formed **3 distinct clusters**  
- Clearly separated customer segments based on spending, cash advance, and repayment behavior  
- **Silhouette Score:** 0.361  

### Hierarchical Clustering
- Produced **3 clusters**  
- Slightly lower separation compared to K-Means  
- **Silhouette Score:** 0.307  

---

## Customer Segments Profiling

### K-Means Clusters
- **Cluster 0:** High Spend Active Users  
- **Cluster 1:** Low Activity Customers  
- **Cluster 2:** Cash Advance Heavy Users  

### Hierarchical Clustering Clusters
- **Cluster 0:** Moderate Spend Users  
- **Cluster 1:** High Spend Active Users  
- **Cluster 2:** Cash Advance Heavy Users  

---

## Key Insights

- **High Spend Active Users:** Frequent purchases, high spending, low cash advance usage  
- **Moderate/Low Activity Users:** Occasional purchases, moderate balances, low risk  
- **Cash Advance Heavy Users:** Minimal purchases, rely on cash withdrawals, high-risk segment  

**Model Recommendation:**  
- **Hierarchical Clustering**  is preferred for this dataset because its clusters offer more meaningful insights into customer behavior and risk, even if its Silhouette Score is slightly lower.  



---

## Project Structure

```text
Credit-Card-Customer-Segmentation/
│
├── data/
│   └── ccdata.csv                 # Credit card dataset
│
├── notebooks/
│   └── CreditCard_Segmentation.ipynb   # Jupyter notebook with full analysis
│
├── src/
│   ├── preprocessing.py           # Data cleaning, scaling, and PCA
│   ├── clustering.py              # K-Means & Hierarchical clustering code
│   └── profiling.py               # Cluster profiling and visualization
│
├── requirements.txt               # Python dependencies
├── README.md                      # Project documentation
