# Experiment 07 — Customer Segmentation and Predictive Analytics Using Machine Learning

## Domain

Customer Analytics

## Objective

The objective of this experiment is to perform customer segmentation and predictive analytics using historical online retail transaction data.

The UCI Online Retail dataset is processed to remove missing values, cancelled transactions, invalid records and outliers. Customer-level behavioural features are then created using RFM analysis and additional purchasing features.

K-Means clustering and hierarchical clustering are used to identify customer segments. PCA is used for dimensionality reduction and visualization. Supervised machine learning models are then developed to classify high-value customers.

## Dataset

**UCI Online Retail Dataset**

The dataset contains retail transaction information including:

- InvoiceNo
- StockCode
- Description
- Quantity
- InvoiceDate
- UnitPrice
- CustomerID
- Country

The dataset contains historical online retail transactions used to analyse customer purchasing behaviour.

## Tasks Performed

### Task 1 — Data Import and Preprocessing

- Imported the UCI Online Retail dataset
- Checked dataset dimensions and structure
- Identified missing CustomerID values
- Removed duplicate records
- Removed cancelled transactions
- Removed invalid quantities
- Removed invalid unit prices
- Calculated transaction revenue using Quantity × UnitPrice

### Task 2 — Customer Feature Engineering

Customer-level features were created from the transaction data, including:

- Recency
- Frequency
- Monetary Value
- Quantity Purchased
- Average Transaction Value
- Purchase Frequency

These features were used to represent customer purchasing behaviour.

### Task 3 — Data Transformation

- Treated extreme values using outlier handling
- Applied logarithmic transformation where required
- Standardized customer-level numerical features
- Prepared the data for clustering algorithms

### Task 4 — K-Means Customer Segmentation

K-Means clustering was applied to identify groups of customers with similar purchasing behaviour.

The number of clusters was analysed using:

- Elbow Method
- Silhouette Score

The resulting customer clusters were used for further customer profiling and analysis.

### Task 5 — Hierarchical Clustering

Hierarchical clustering was performed to examine the structure of customer groups.

A dendrogram was generated to visualize the hierarchical relationships between customers.

### Task 6 — PCA Visualization

Principal Component Analysis (PCA) was used to reduce the customer feature space for visualization.

The customer segments were visualized using:

- 2D PCA visualization
- Interactive 3D PCA visualization using Plotly

### Task 7 — Customer Profiling

The identified customer segments were analysed using their purchasing characteristics.

The segment profiles were compared using:

- Average Recency
- Average Frequency
- Average Monetary Value
- Quantity Purchased
- Average Transaction Value
- Purchase Frequency

A high-value customer segment was identified based on the monetary value of the customer segments.

### Task 8 — Predictive Modelling

Supervised machine learning models were developed to classify customers into:

- High Value
- Non-High Value

The following models were implemented:

- Random Forest
- Support Vector Machine (SVM)

### Task 9 — Model Evaluation

The predictive models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Confusion Matrix
- ROC Curves

The performance of Random Forest and SVM was compared using the evaluation metrics.

### Task 10 — Feature Importance

Feature importance was analysed using the Random Forest model to identify the customer attributes that contribute to high-value customer classification.

### Task 11 — Marketing Recommendations

Segment-wise marketing recommendations were developed based on customer purchasing behaviour.

Recommendations include:

- Loyalty rewards and personalized offers for high-value customers
- Repeat-purchase campaigns for regular customers
- Re-engagement campaigns for low-value or inactive customers

## Technologies

- R
- dplyr
- readxl
- stringr
- ggplot2
- cluster
- randomForest
- e1071
- pROC
- plotly

## Deliverables

- R Google Colab notebook
- PDF report
- Customer segmentation visualizations
- Model performance comparison
- ROC curves and confusion matrices
- Customer segment analysis
- Business/marketing recommendations
