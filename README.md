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

### Orders
<img width="663" alt="image" src="https://github.com/user-attachments/assets/73fe3be4-a1af-4f6d-b1d1-fe3406023bd7">

### Order_Items
<img width="935" alt="image" src="https://github.com/user-attachments/assets/69de0d03-69c1-40b0-bacb-88312de33828">

### Users
<img width="938" alt="image" src="https://github.com/user-attachments/assets/05a39cad-8eec-41e3-a56e-c46ab670d4e8">


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

The analysis revealed five distinct customer segments: Champions, Loyal Customers, New Customers, At-Risk Customers, and Lost Customers. Key findings include:

1. Champions and Loyal Customers (23.41% combined) drive significant revenue, accounting for over 50% of total sales.

2. New Customers form the largest segment (33.14%), indicating strong acquisition but weak retention.
 
3. At-Risk and Lost Customers (43.45% combined) represent a substantial portion of our customer base, highlighting urgent retention needs.


These insights provide a foundation for targeted marketing strategies to enhance customer retention, reactivation, and overall lifetime value.

## 4. Insights Deep Dive

### Clustering Results

1. Champions (Cluster 2: 5.91%)
 - Highest frequency (6.01 purchases) and monetary value ($436.58)
 - Recent activity (130.73 days)
 - Small but extremely valuable segment

2. Loyal Customers (Cluster 3: 17.50%)
 - High monetary value ($205.16) and moderate frequency (3.57 purchases)
 - Very recent activity (121.52 days)
 - Solid base of reliable customers

3. New Customers (Cluster 1: 33.14%)
 - Very recent first purchase (84.11 days)
 - Low frequency (1.37 purchases) and monetary value ($74.72)
 - Largest segment, indicating strong acquisition

4. At-Risk Customers (Cluster 4: 23.91%)
 - Moderate recency (322.79 days)
 - Low frequency (1.46 purchases) and monetary value ($81.18)
 - Significant segment showing signs of disengagement

5. Lost Customers (Cluster 0: 19.54%)
 - High recency (579.34 days)
 - Low frequency (1.59 purchases) and moderate monetary value ($94.17)
 - Substantial segment of inactive customers

### Key Findings
- Customer Value Distribution: Champions and Loyal Customers, while comprising only 23.41% of the customer base, likely contribute over 50% of total revenue.
- Acquisition vs. Retention: The large New Customer segment (33.14%) suggests effective acquisition strategies, but the sizeable At-Risk and Lost segments indicate retention challenges.
- Engagement Spectrum: There's a clear divide between highly engaged customers (Champions and Loyal) and those showing low engagement (At-Risk and Lost), with New Customers in a critical transition phase.
- Lost Customers show higher monetary value than At-Risk Customers, suggesting potential value in reactivation efforts.
- Frequency Patterns: A stark contrast exists between the high purchase frequency of Champions (6.01) and the low frequency of other segments (1.37-1.59), indicating opportunities for increasing purchase frequency across most segments.

## 5. Recommendations

Based on the analysis, the following strategies are recommended for each customer segment:

1. Champion Nurturing Program
 - Implement an exclusive VIP program for Champions
 - Offer early access to new products and special events
 - Provide personalized service and recognition

2. Loyal Customer Upgrade Initiative
 - Create targeted campaigns to increase purchase frequency
 - Introduce a tiered loyalty program to encourage higher spending
 - Offer bundled products or services to increase average order value

3. New Customer Onboarding and Engagement
 - Develop a comprehensive onboarding program to guide new customers
 - Implement a series of welcome emails with product education and offers
 - Create early-stage loyalty incentives to encourage repeat purchases

4. At-Risk Customer Reactivation
 - Launch a win-back campaign with personalized offers
 - Conduct surveys to understand reasons for decreased engagement
 - Implement a re-engagement email series with targeted content and promotions

5. Lost Customer Recovery
 - Develop a multi-channel reactivation campaign
 - Offer a "We Miss You" discount or special bundle
 - Create content addressing potential reasons for disengagement

## 6. Assumptions and Caveats

- K-means clustering assumes spherical clusters, which may not always represent customer segments accurately.
- The optimal number of clusters (5) was chosen based on the elbow method and silhouette score. Different numbers of clusters might be appropriate for other datasets or business objectives.

---

For detailed implementation and code, please refer to the main script in this repository.
