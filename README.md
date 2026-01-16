# Customer Segmentation Analysis

## Project Overview
This project performs a customer segmentation analysis on a dataset of mall customers. The goal is to identify distinct groups of customers based on their purchasing behavior to enable targeted marketing strategies.

## Dataset
The dataset consists of 200 customer records with the following features:
- **Gender**: Male/Female
- **Age**: Customer's age
- **Yearly Income (k$)**: Annual income in thousands of dollars
- **Purchase Spending (1-100)**: A score assigned based on customer behavior and spending nature

## Methodology
The project follows a standard Data Mining pipeline:
1.  **Data Preprocessing**: Checking for null values, renaming columns for clarity (e.g., `Annual Income (k$)` to `Yearly Income`), and dropping unnecessary columns like `CustomerID`.
2.  **Exploratory Data Analysis (EDA)**: Visualizing distributions, such as the gender ratio (Female: ~55%, Male: ~45%).
3.  **Clustering Algorithm**: Used **K-Means Clustering** to segment the data.
4.  **Optimizing K**: Applied the **Elbow Method** to determine the optimal number of clusters, identifying **K=5** as the ideal number where the Within-Cluster Sum of Squares (WCSS) levels off.

## Feature Insights
*   **Role of Age**: Bivariate analysis and 3D interactive charts revealed that **Age** plays a minor role in this specific segmentation.
    *   In the modern era, high yearly income and purchase spending are observed across various age groups, including younger demographics.
    *   The primary differentiation in these clusters is driven by **Income** and **Spending Score**.

## Results & Clusters
The analysis successfully segmented the customers into 5 distinct tiers. Based on the 3D visualization of Income, Spending, and Age, the key segments are:

-   **VIP (High Income, High Spending)**:
    -   These customers earn a high annual income and also spend significantly.
    -   *Strategy*: Prioritize for exclusive offers, loyalty programs, and luxury product launches.

-   **PRO / Savvy (High Income, Low Spending)**:
    -   These customers earn well but are conservative spenders.
    -   *Strategy*: Target with value-proposition marketing or promotions to convert their spending potential.

-   **Standard (Middle Income, Middle Spending)**:
    -   The average customer base with moderate income and spending.

-   **Low Income, High Spending**:
    -   Younger demographic spending more than they earn.
    -   *Strategy*: Monitor for credit risk or target with budget-friendly fashion.

-   **Low Income, Low Spending**:
    -   Conservative spenders with limited budget.


## Bonus: Hierarchical Clustering
To validate the findings, **Hierarchical Clustering** (Ward's Method) was performed.
- **Dendrogram Analysis**: The dendrogram suggested a natural grouping of **2 to 3 clusters** (based on a cut at y=3.5).
- **Comparison**: 
    - **K-Means** found 5 granularity levels (subgroups).
    - **Hierarchical Clustering** likely grouped these into broader categories (e.g., High Value vs. Low Value).
    - The K=5 approach from K-Means provides more actionable specific segments for marketing than the broader K=3 from Hierarchical clustering.

## Conclusion
The K-Means model with K=5 effectively separates the customer base into actionable groups, allowing for precise business decision-making and personalized customer experiences. While Hierarchical Clustering suggests a broader structure (2-3 groups), the 5-cluster model offers better granularity for targeted campaigns.
