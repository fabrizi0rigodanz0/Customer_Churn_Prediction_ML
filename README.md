# FarTrend Customer Segmentation and Recommendation System

## Project Overview

In the dynamic realm of e-commerce, understanding customer behavior is pivotal for strategic marketing. FarTrend, an emerging e-commerce giant, has experienced rapid growth by offering a diverse range of products, from fashion to electronics, catering to over 3400 customers across various demographics. Despite their success, FarTrend faces challenges in personalizing marketing efforts and predicting future purchasing behavior, crucial for sustaining growth and enhancing customer satisfaction.

## Project Goals

FarTrend's extensive customer database reveals purchasing patterns over the past year but lacks actionable insights to anticipate the needs of new customers. Traditional marketing strategies have yielded moderate success; however, the leadership team believes that a more data-driven approach could unlock exponential growth.

The objective of this project is to develop a machine learning model that segments FarTrend's customer base and predicts future purchases of new customers within their first year. This model aims to transform FarTrend's approach to customer engagement by delivering personalized marketing campaigns and tailored product recommendations.

## Data Description

The IT department has extracted a dataframe with the main transactions performed by the customers.

### Variables

- **InvoiceNo**: Invoice number. A 6-digit integral number uniquely assigned to each transaction. If this code starts with the letter 'C', it indicates a cancellation.
- **StockCode**: Product (item) code. A 5-digit integral number uniquely assigned to each distinct product.
- **Description**: Product (item) name.
- **Quantity**: The quantities of each product (item) per transaction.
- **InvoiceDate**: The day and time when each transaction was generated.
- **UnitPrice**: Product price per unit.
- **CustomerID**: Unique customer number.
- **Country**: The name of the country where each customer resides.

## Data Quality and Customer Understanding

### Exploratory Data Analysis

We began by loading the dataset and examining its structure. Here are the initial insights:

- **Entries**: 541,909
- **Columns**: 8

### Data Cleaning and Preparation

#### Missing Values

- **CustomerID**: 24.93% missing
- **Description**: 0.27% missing

#### Strategy

- Remove rows with missing **CustomerID** and **Description** values.
- Handle duplicates and ensure data integrity.
- Address outliers in **Quantity** and **UnitPrice**.

#### Exploratory Data Analysis

- Identified patterns in categorical and numerical variables.
- Highlighted the need for normalization and feature engineering for better analysis.

### Feature Engineering

Key features were engineered to better understand customer behavior:

1. **Total Spend per Transaction**
2. **Purchase Frequency**
3. **Average Spend per Visit**
4. **Product Variety per Transaction**
5. **Time Since Last Purchase**
6. **Day of the Week and Hour of Purchase**
7. **Cancellation Rate**
8. **Geographical Insights**
9. **Seasonality Trends**

### Data Insights

- **Customer Segmentation**: Identified high-value customers and low-engagement segments.
- **Geographical Distribution**: Majority from the UK, with significant international presence.
- **Product Popularity**: Key products identified for inventory and marketing strategies.

## Customer Segmentation Based on Purchase Profile

### Baseline Model

#### Methodology

- **Feature Scaling**: Standardized features before applying PCA.
- **PCA**: Reduced dimensionality to six components, capturing over 85% of the variance.

#### K-Means Clustering

- Applied K-Means clustering on PCA-transformed data.
- Determined the optimal number of clusters using the Elbow method and Silhouette scores.
- Selected three clusters for further analysis.

### Second Model

#### Hierarchical Clustering

- Applied hierarchical clustering and compared it with K-Means.
- Found K-Means to provide a more balanced and interpretable segmentation.

### Suggested Clusters

#### Clusters Characteristics

1. **Cluster 0 - Emerging Shoppers**: Lower engagement, potential for growth.
2. **Cluster 1 - Consistent Shoppers**: Reliable, mid-level engagement.
3. **Cluster 2 - High-Value Loyalists**: Highly engaged, significant contributors to revenue.

## Recommendation System

### Building the Recommendation System

#### Methodology

- Developed a content-based recommendation system using cosine similarity.
- Generated segment-specific item similarity matrices for personalized recommendations.
- Evaluated the system using precision and recall metrics.

#### Results

- **Average Precision**: 0.104
- **Average Recall**: 0.327

### Recommendations for Marketing

#### Strategy

- Utilize the recommendation system for personalized email campaigns, dynamic website content, targeted promotions, and strategic inventory management.
- Incorporate broader data sources like customer feedback, real-time behavior, demographic, and psychographic data to enhance the system's accuracy.

#### Conclusion

Enhancing the recommendation system with comprehensive data inputs promises not only to heighten its predictive accuracy but also to make personalized marketing tactics more impactful, ultimately driving customer satisfaction, loyalty, and revenue growth.

## Implementation Steps

### Step 1: Data Collection and Preparation

- Gather all relevant transaction data.
- Clean and preprocess the data to handle missing values, duplicates, and outliers.
- Perform exploratory data analysis to understand the data distribution and key patterns.

### Step 2: Feature Engineering

- Create new features that capture important aspects of customer behavior.
- Standardize the features to ensure they are on a comparable scale.

### Step 3: Customer Segmentation

- Apply PCA to reduce dimensionality.
- Use K-Means clustering to segment customers into distinct groups.
- Validate the clusters and adjust the number of clusters as needed.

### Step 4: Recommendation System

- Develop a content-based recommendation system using cosine similarity.
- Create segment-specific item similarity matrices for personalized recommendations.
- Evaluate the recommendation system using precision and recall metrics.

### Step 5: Marketing Strategies

- Integrate the recommendation system into personalized email campaigns.
- Dynamically adjust website content based on customer segments.
- Implement targeted promotions and strategic inventory management.

### Step 6: Continuous Improvement

- Continuously collect new data to refine and improve the recommendation system.
- Incorporate additional data sources for better accuracy.
- Monitor the performance of marketing campaigns and adjust strategies accordingly.

## Conclusion

This project aims to transform FarTrend's customer engagement through a data-driven approach to segmentation and personalized recommendations. By leveraging the insights gained from this analysis, FarTrend can enhance customer satisfaction, foster loyalty, and drive revenue growth in the competitive e-commerce landscape.
