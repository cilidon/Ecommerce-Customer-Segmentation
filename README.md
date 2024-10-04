# Customer Segmentation using RFM Analysis and Clustering for The Look E-commerce

## Introduction

This project focuses on customer segmentation for The Look, an e-commerce platform, using RFM (Recency, Frequency, Monetary) analysis and K-means clustering. The Look dataset is a comprehensive e-commerce dataset that includes information about customers, products, orders, and more.

The primary goal of this project is to gain deeper insights into customer behavior and create meaningful segments that can drive targeted marketing strategies and improve overall customer engagement. By understanding different customer groups, The Look can tailor its approach to each segment, potentially increasing customer loyalty, sales, and lifetime value.

## 1. Background and Overview

E-commerce businesses like The Look face the challenge of effectively engaging with a diverse customer base. Customer segmentation allows for more personalized marketing efforts and improved resource allocation. This project utilizes RFM analysis, a proven method for customer segmentation in retail and e-commerce, combined with K-means clustering to identify distinct customer groups based on their purchasing behavior.

The analysis pipeline includes:
- Exploratory Data Analysis (EDA)
- Data cleaning and preprocessing
- RFM analysis
- Feature scaling and normalization
- Principal Component Analysis (PCA)
- K-means clustering
- Cluster visualization and profiling
- Generating recommendations for each segment

## 2. Data Structure Overview

The project uses The Look dataset, which includes the following key tables:

| Table Name | Description |
|------------|-------------|
| users      | Customer information including demographics |
| orders     | Order details including dates and status |
| order_items| Individual items within each order, including product and price information |

For the RFM analysis, we focused on the following columns:
- user_id: Unique identifier for each customer
- order_date: Date of the order
- order_id: Unique identifier for each order
- order_value: Monetary value of the order (derived from order_items)

## 3. Executive Summary

Our analysis revealed four distinct customer segments based on their RFM scores:

1. Occasional/One-time Customers (42.19%)
2. Regular Customers (28.49%)
3. Lapsed Customers (19.32%)
4. Best Customers (10.00%)

These segments provide a foundation for targeted marketing strategies and personalized customer experiences.

## 4. Insights Deep Dive

### RFM Analysis
- Recency: Ranges from 110 days for Occasional Customers to 1055 days for Lapsed Customers.
- Frequency: Order frequency varies from 0.56 for Occasional Customers to 5.29 for Best Customers.
- Monetary: Average order value ranges from $23.20 for Occasional Customers to $403.58 for Best Customers.

### Clustering Results
- Cluster 0 (Occasional/One-time Customers): Recent purchases but low frequency and monetary value.
- Cluster 1 (Regular Customers): Moderate recency, frequency, and monetary value.
- Cluster 2 (Lapsed Customers): Very low recency, low frequency, and moderate monetary value.
- Cluster 3 (Best Customers): Moderate recency, high frequency, and high monetary value.

### Key Findings
- A large portion of customers (42.19%) are occasional or one-time buyers, presenting an opportunity for conversion to regular customers.
- Best customers, while only 10% of the base, likely contribute significantly to overall revenue.
- There's a substantial group of lapsed customers (19.32%) who haven't made a purchase in a long time, indicating a need for re-engagement strategies.

## 5. Recommendations

Based on our analysis, we recommend the following strategies for each customer segment:

1. Occasional/One-time Customers (42.19%):
   - Implement re-engagement campaigns to encourage more frequent purchases
   - Offer product recommendations based on initial purchases
   - Provide educational content about product benefits and use cases

2. Regular Customers (28.49%):
   - Introduce or upgrade loyalty programs
   - Launch cross-sell and upsell campaigns based on purchase history
   - Offer personalized product bundles or discounts

3. Lapsed Customers (19.32%):
   - Create win-back campaigns with attractive offers
   - Conduct surveys to understand reasons for decreased activity
   - Send new product announcements or major updates since their last purchase

4. Best Customers (10.00%):
   - Develop a VIP program with premium benefits
   - Provide early access to sales and new products
   - Offer personal shopping assistance or concierge service

## 6. Assumptions and Caveats

- The analysis assumes that RFM metrics are good indicators of customer value and behavior.
- K-means clustering assumes spherical clusters, which may not always represent real-world customer segments accurately.
- The optimal number of clusters (4) was chosen based on the elbow method and silhouette score. Different numbers of clusters might be appropriate for other datasets or business objectives.
- This analysis provides a snapshot of customer behavior and should be updated regularly to capture changing patterns.
- The recommendations are general and should be adapted based on The Look's specific business context and additional customer data not included in this analysis.
- The dataset used is a sample and may not represent the entire customer base of The Look.

---

For detailed implementation and code, please refer to the main script in this repository.
