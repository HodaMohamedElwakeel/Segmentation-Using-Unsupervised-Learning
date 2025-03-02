# Customer Segmentation using Unsupervised Learning

## Project Overview

This project aims to segment customers based on their transactional behavior and demographic features using unsupervised machine learning techniques. The segmentation helps identify customer groups that share similar behaviors, enabling businesses to optimize their coupon offerings to enhance loyalty and satisfaction.

## Dataset

The dataset consists of five interrelated tables:

- **Customers**: Contains customer demographic information.
- **Genders**: Maps gender IDs to gender names.
- **Cities**: Maps city IDs to city names.
- **Transactions**: Includes transaction details such as transaction date, coupon usage, and transaction status.

## Features Used for Segmentation

1. **Recency**: Number of days since the customer's last transaction.
2. **Frequency**: Number of transactions made by the customer.
3. **Monetary**: Number of successful coupon burns.
4. **Gender**: Encoded categorical feature representing customer gender.
5. **City**: Encoded categorical feature representing the customer's city.
6. **Coupon Usage Frequency**: Number of coupons used by the customer.
7. **Transaction Status**: Encoded categorical feature indicating transaction success.

## Preprocessing Steps

1. **Data Merging**: Integrated customers, genders, cities, and transactions datasets.
2. **Handling Missing Values**:
   - Numerical features: Filled missing values with the median.
   - Categorical features: Filled missing values with the mode.
3. **Encoding Categorical Features**: Applied Label Encoding to `Gender`, `City`, and `Transaction Status`.
4. **Feature Scaling**: Standardized numerical values using `StandardScaler`.

## Unsupervised Machine Learning Models

### 1. K-Means Clustering

- Used the **Elbow Method** to determine the optimal number of clusters.
- Trained the K-Means model with the optimal number of clusters.
- Evaluated the model using **Silhouette Score**.

### 2. Hierarchical Clustering

- Used **Dendrograms** to visualize hierarchical clustering.
- Trained an **Agglomerative Clustering** model with the optimal number of clusters.
- Evaluated the model using **Silhouette Score**.

## Results

- The **Elbow Method** helped determine the optimal number of clusters.
- Both K-Means and Hierarchical Clustering were applied and evaluated.
- Silhouette Scores indicate the quality of segmentation.

## Insights & Recommendations

1. **High-Value Customers**: Customers with high frequency and monetary value should receive exclusive high-discount coupons.
2. **Infrequent Shoppers**: Customers with low frequency but high monetary value should receive personalized offers to encourage repeat purchases.
3. **Low-Engagement Customers**: Customers with low frequency and low coupon usage may require targeted marketing campaigns.
4. **City-Based Promotions**: Cities with higher engagement can receive location-based discounts.

## How to Run the Code

1. Ensure you have the required libraries installed:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn scipy
   ```
2. Place the dataset file (`E-commerce_data.xlsx`) in the correct directory.
3. Run the Python script to generate customer segments and visualizations.

## Future Improvements

- Implement additional clustering algorithms such as **DBSCAN** for noise handling.
- Incorporate more customer behavioral features.
- Use **Principal Component Analysis (PCA)** for dimensionality reduction before clustering.

## Author

Hoda Mohamed


