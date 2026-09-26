E-Commerce Customer Segmentation

A machine learning project that uses K-Means clustering to divide e-commerce customers into meaningful groups based on their purchasing behavior, engagement, spending, and profitability.

Project Overview

The goal of this project is to understand different types of customers and create useful customer segments for business decision-making.

The project uses customer data and applies K-Means clustering to identify 4 customer groups.

Dataset

The project uses the E-Commerce Customer Segmentation 2026 dataset from Kaggle.

Dataset: datascikhan/e-commerce-customer-segmentation-2026

The dataset contains customer information related to:

Age
Customer tenure
Total purchases
Average order value
Total spending
Purchase frequency
Days since last purchase
Returns and complaints
Satisfaction
Email engagement
Click-through rate
Conversion rate
Customer lifetime value
Customer acquisition cost
Customer profitability
Features Used

The clustering model uses 16 customer features:

age
tenure_months
total_purchases
avg_order_value_usd
total_spent_usd
purchase_frequency
days_since_last_purchase
return_count
complaint_count
satisfaction_score
email_open_rate
click_through_rate
conversion_rate
customer_lifetime_value_usd
customer_acquisition_cost_usd
customer_profitability_usd

The purchase_frequency feature was converted from categories such as Rarely, Monthly, Weekly, and Daily into numerical values.

Data Preprocessing

The following preprocessing techniques were used:

Feature selection
Categorical value conversion
Skewness analysis
Log transformation
Yeo-Johnson transformation
StandardScaler normalization

customer_lifetime_value_usd was removed from the clustering features after feature analysis.

Clustering Method

The project uses K-Means clustering.

The number of clusters was analyzed using:

Elbow Method
Silhouette Score

The final model uses:

Number of clusters: 4
Algorithm: K-Means
Random State: 42
Customer Segments

The four clusters were interpreted as:

Segment	Description
Frequent Low-Spending Customers	Customers who purchase frequently but spend relatively less
High-Value At-Risk Customers	High-value customers who may need re-engagement
High-Value Loyal Customers	Valuable customers with strong purchasing behavior
Low-Engagement Customers	Customers with lower engagement and purchasing activity
Visualization

Several visualizations were created to understand the customer segments:

Feature distributions
Boxplots for outlier analysis
Correlation heatmap
Spending analysis
Purchase frequency comparison
Recency comparison
Customer segment distribution
PCA scatter plot showing the 4 customer clusters

PCA was used to reduce the feature space to two dimensions for visualization.

Business Recommendations

Recommendations were created for each customer segment.

Examples include:

Product bundles and cross-selling for frequent low-spending customers
Re-engagement campaigns for high-value at-risk customers
Loyalty rewards for high-value loyal customers
Targeted marketing campaigns for low-engagement customers

The recommendations are saved in:

customer_recommendations.csv
Model

The trained K-Means model is saved as:

customer_segmentation_kmeans.pkl
Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
Google Colab
Kaggle Dataset
Project Workflow
Dataset
   ↓
Data Cleaning
   ↓
EDA
   ↓
Feature Selection
   ↓
Feature Transformation
   ↓
Standardization
   ↓
Elbow Method + Silhouette Score
   ↓
K-Means Clustering
   ↓
4 Customer Segments
   ↓
Cluster Analysis
   ↓
PCA Visualization
   ↓
Business Recommendations
Files
E-Commerce-Customer-Segmentation/
│
├── customer_segmentation.ipynb
├── customer_recommendations.csv
├── customer_segmentation_kmeans.pkl
└── README.md
How to Run
1. Install the required libraries
pip install pandas numpy matplotlib seaborn scikit-learn
2. Open the notebook

Open:

customer_segmentation.ipynb

The notebook can be run using Google Colab or Jupyter Notebook.

Conclusion

This project demonstrates how unsupervised machine learning can be used to segment e-commerce customers based on their behavior.

The final K-Means model creates 4 customer segments, which are analyzed using statistical summaries and visualizations. Business recommendations are then created for each segment to support customer engagement and marketing strategies.
