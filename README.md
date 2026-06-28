# Customer Segmentation using RFM and K-Means++

Customer segmentation project based on RFM analysis and K-Means++ clustering algorithm using the Online Retail dataset. The project includes data preprocessing, feature engineering, customer clustering, evaluation, and interactive dashboards developed in Power BI.


## Introduction

Customer segmentation is an important task in customer relationship management, enabling businesses to better understand purchasing behavior and develop targeted marketing strategies.

This project applies RFM (Recency, Frequency, Monetary) analysis to extract customer behavioral features from the Online Retail dataset. The K-Means++ clustering algorithm is then used to segment customers into meaningful groups based on their purchasing patterns.

The project covers the complete data analysis workflow, including data preprocessing, feature engineering, customer segmentation, cluster evaluation, visualization, and interactive dashboards developed with Power BI.

## Dataset

The project uses the **Online Retail** dataset from the UCI Machine Learning Repository.

The dataset contains transactional records of a UK-based online retail company between **01/12/2010** and **09/12/2011**. Most customers are wholesalers purchasing gifts and merchandise in bulk.

### Original Features

| Feature | Description |
|----------|-------------|
| InvoiceNo | Invoice number |
| StockCode | Product code |
| Description | Product description |
| Quantity | Quantity purchased |
| InvoiceDate | Transaction date and time |
| UnitPrice | Unit price |
| CustomerID | Customer identifier |
| Country | Customer country |

### Processed Datasets

The repository includes several intermediate datasets generated during preprocessing:

| File | Description |
|------|-------------|
| Online Retail.csv | Original dataset |
| bang1_clean.csv | Dataset after preprocessing and data cleaning |
| bang2_invoice.csv | Dataset aggregated by InvoiceNo |
| bang3_rfm.csv | Customer-level RFM dataset |
| kết quả phân cụm.csv | Final customer segmentation results |

## Project Workflow

The overall workflow of the project is illustrated below.

<p align="center">
  <img src="ảnh/workflow.svg" width="900">
</p>

The workflow consists of the following stages:

1. **Data Exploration**
   - Explore the Online Retail dataset.
   - Analyze data characteristics and identify data quality issues.

2. **Data Preprocessing**
   - Clean and transform the transactional data.
   - Aggregate transactions and construct customer-level RFM features.

3. **Customer Segmentation**
   - Normalize RFM features.
   - Apply the K-Means++ algorithm to group customers into distinct segments.

4. **Cluster Evaluation**
   - Determine the optimal number of clusters.
   - Evaluate clustering quality using internal validation metrics, including the Elbow Method, Silhouette Score, Davies–Bouldin Index, and Calinski–Harabasz Index.

5. **Visualization and Business Analysis**
   - Interpret the characteristics of each customer segment.
   - Build interactive Power BI dashboards to support business insights and decision-making.

### Directory Description

| Directory | Description |
|-----------|-------------|
| `data` | Original dataset and intermediate datasets generated during preprocessing and customer segmentation. |
| `notebook` | Jupyter Notebook containing the complete implementation of the customer segmentation workflow. |
| `Power BI` | Interactive dashboard for analyzing customer segments and business insights. |
| `ảnh` | Figures, workflow diagrams, evaluation results, and visualizations used throughout the project. |

## Results

The K-Means++ algorithm successfully segmented customers into four distinct groups based on their RFM characteristics.

| Cluster | Segment | Description |
|---------|----------|-------------|
| 0 | Regular Customers | Average purchasing behavior. |
| 1 | Loyal Customers | Frequent customers with consistent purchases. |
| 2 | VIP Customers | High-value customers with high frequency and spending. Many wholesalers belong to this segment. |
| 3 | Inactive Customers | Customers who have not purchased recently. |

