# Customer Segmentation with Credit Card Data

This repository contains a Python code that performs customer segmentation using the Credit Card Dataset (https://www.kaggle.com/arjunbhasin2013/ccdata) available on Kaggle. Customer segmentation is a critical task for businesses to understand their customer base better and tailor marketing strategies accordingly.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Dependencies](#dependencies)
- [Code Overview](#code-overview)
- [Results](#results)


## Introduction

Customer segmentation involves grouping customers with similar characteristics and behaviors into distinct segments. This helps businesses understand their customers better, target their marketing efforts more effectively, and personalize their services.

In this project, we use Python and various libraries to perform customer segmentation on a credit card dataset. The main steps include data preprocessing, exploratory data analysis, dimensionality reduction using PCA (Principal Component Analysis), and clustering using K-Means. Additionally, we employ autoencoders for further feature reduction before clustering.

## Dataset

The dataset used for this project is the Credit Card Dataset (https://www.kaggle.com/arjunbhasin2013/ccdata), or you can download it from this repository. It has 17 features and 8950 rows. The Dataset summarizes the usage behavior of about 8950 active credit card holders during the last 6 months. The file is at a customer level with 18 behavioral variables.

- CUST_ID : Identification of Credit Card holder (Categorical)
- BALANCE : Balance amount left in their account to make purchases
- BALANCE_FREQUENCY : How frequently the Balance is updated, score between 0 and 1 (1 = frequently updated, 0 = not frequently updated)
- PURCHASES : Amount of purchases made from account
- ONEOFF_PURCHASES : Maximum purchase amount done in one-go
- INSTALLMENTS_PURCHASES : Amount of purchase done in installment
- CASH_ADVANCE : Cash in advance given by the user
- PURCHASES_FREQUENCY : How frequently the Purchases are being made, score between 0 and 1 (1 = frequently purchased, 0 = not frequently purchased)
- ONEOFFPURCHASESFREQUENCY : How frequently Purchases are happening in one-go (1 = frequently purchased, 0 = not frequently purchased)
- PURCHASESINSTALLMENTSFREQUENCY : How frequently purchases in installments are being done (1 = frequently done, 0 = not frequently done)
- CASHADVANCEFREQUENCY : How frequently the cash in advance being paid
- CASHADVANCETRX : Number of Transactions made with "Cash in Advanced"
- PURCHASES_TRX : Numbe of purchase transactions made
- CREDIT_LIMIT : Limit of Credit Card for user
- PAYMENTS : Amount of Payment done by user
- MINIMUM_PAYMENTS : Minimum amount of payments made by user
- PRCFULLPAYMENT : Percent of full payment paid by user
- TENURE : Tenure of credit card service for user

## Dependencies

To run the code in this project, you will need the following Python libraries:

- pandas
- numpy
- seaborn
- matplotlib
- scikit-learn
- TensorFlow/Keras (for autoencoders)

## Code Overview

Here is a brief overview of the main steps in the code:

1. Data loading and initial exploration.
2. Handling missing data.
3. Dropping irrelevant features (e.g., customer ID).
4. Exploratory data analysis to understand the dataset.
5. Data scaling using StandardScaler.
6. Applying K-Means clustering to find customer segments.
7. Using PCA for dimensionality reduction and visualization.
8. Implementing autoencoders for further feature reduction.
9. Repeating K-Means clustering on the reduced feature set.

## Results

The code in this project generates valuable insights and customer segments based on the provided credit card dataset. Customer segmentation is a powerful technique that enables businesses to better understand their customer base and tailor their strategies for improved customer satisfaction and profitability.

### Exploratory Data Analysis

Before diving into segmentation, the code conducts exploratory data analysis (EDA) to gain a comprehensive understanding of the dataset. Some of the key insights obtained during EDA include:

- **Balance Analysis**: The average balance left in customer accounts is approximately $1,564.
- **Balance Frequency**: Most customers' account balances are frequently updated, with an average score of around 0.9 (1 being frequently updated and 0 not frequently updated).
- **Purchases**: The average purchase amount is approximately $1,000.
- **One-Off Purchases**: On average, customers make one-off purchases of around $600.
- **Purchase Frequency**: The average purchase frequency is approximately 0.5.
- **Credit Limit**: The average credit card limit for users is approximately $4,500.
- **Payment Behavior**: A significant percentage of customers do not pay their balance in full, with a PRC_FULL_PAYMENT average of about 15%.
- **Tenure**: The average tenure of credit card service for customers is approximately 11 years.

### K-Means Clustering

The code applies K-Means clustering to segment customers based on their credit card usage behavior. Some key findings from K-Means clustering include:

- **Optimal Number of Clusters**: The optimal number of clusters is determined using the "elbow method." In this case, it suggests that 4 to 8 clusters are reasonable choices. The code ultimately selects 8 clusters for further analysis.
- **Cluster Characteristics**: Each cluster exhibits unique characteristics in terms of balance, purchase behavior, credit limit, and more.
- **Cluster Visualization**: The code generates histograms for various features, allowing for a visual comparison of the different clusters' behaviors.
  
### Principal Component Analysis (PCA)

PCA is used for dimensionality reduction and visualization of the data. Some important points related to PCA include:

- **Dimensionality Reduction**: PCA reduces the dataset's dimensionality while preserving the most critical information.
- **Visualization**: Principal components are used to create a scatter plot, providing a visual representation of how well the clusters separate in lower dimensions.
- **Cluster Separation**: The PCA visualization shows how well the clusters are separated in the reduced feature space.

### Autoencoders

To further reduce the number of features from 17 to 10, the code employs autoencoders, a type of neural network. Key details about autoencoders include:

- **Feature Reduction**: Autoencoders are used to reduce the dataset's dimensions while retaining essential information.
- **Training**: The autoencoder is trained on the scaled dataset to perform this feature reduction.
- **Cluster Analysis**: K-Means clustering is applied again on the reduced feature set to observe how clusters change based on feature reduction.

The entire process provides a comprehensive view of customer segments based on credit card behavior, enabling businesses to tailor marketing strategies, enhance customer experiences, and make data-driven decisions to improve overall customer satisfaction and profitability.

By analyzing the results, businesses can gain insights into their customer base, identify high-value customer segments, and develop targeted marketing campaigns and services to meet specific customer needs and preferences.
