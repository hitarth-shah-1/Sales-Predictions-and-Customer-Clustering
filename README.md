## Overview

This project explores the U.S. vodka market using data analysis and machine learning to provide actionable insights for optimizing sales performance, assortment planning, and inventory management. The analysis includes data cleaning, feature engineering, predictive modeling, and clustering techniques to address key business challenges.

## Business Objectives

The primary business problems addressed in this project are:

*   **Sales Performance:** Understanding and improving vodka sales across different regions and stores.
*   **Assortment Planning:** Optimizing the selection of vodka brands and package types offered in each store.
*   **Overstocking:** Reducing excess inventory and minimizing storage costs.
*   **Risk of External Factors:** Evaluating external factors

## Data Highlights

### Initial Dataset Overview

*   **Item Information:** Code, Name, Package Type, Retail $ amount
*   **Total Sales:** \$219 Million
*   **Total Stores:** 232
*   **Average Price:** \$24.8

### Key Findings

*   Identification of top-selling vodka brands.
*   Analysis of sales variations across different states.

## Feature Engineering

The following feature engineering techniques were applied to enhance model accuracy:

*   **Interaction Terms:** Examining relationships between features and the target variable (sales).
*   **Dummy Variables:** Converting categorical variables (e.g., Store Size) into numerical format.
*   **Normalized Data:** Scaling features (e.g., Count of weeks in stock) to a 0-1 range.
*   **Log Transformations:** Reducing skewness in features like Retail Price.
*   **New Columns:** Adding new features (Spirits Direct, Flavored Vodka, etc.) to capture additional data insights.

## Model Description

### Clustering

Clustering techniques were used to segment stores, customers, and products based on relevant features:

*   **Store-Level:** Vodka sales, retail price, household demographics, store age, average net worth.
*   **Demographics & Demand:** Vodka sales, household demographics, vodka-wine ratio, stock availability.
*   **Product:** Packaging types (1L, 750ml), vodka-tequila ratios.
*   **Shelf Space Optimization:** Stock availability (normalized weeks in stock), retail price, vodka-tequila ratio.

### Feature Selection

*   **Ensemble Model:** Evaluated feature contributions across decision trees using Random Forests.
*   **Ridge Regression:** Refined feature importance while reducing overfitting. Top features include Store\_State\_NY, Count\_Week\_Instock\_Normalized, and package-related variables.

### Modeling

Evaluated predictive models, including XGBoost, ANN, and Linear Regression, using metrics like RMSE, MAE, and R-squared. The Voting Regressor model delivered superior performance for vodka sales forecasting (RMSE of 14800).

## Challenges and Workarounds

*   [Details of specific challenges encountered and the solutions implemented]

## Recommendations and Opportunities

*   **Store Assortment:** Predictive models can forecast sales of Vodka brands, aiding in strategic product assortment planning
*   **Customer Clusters for Store-Specific Assortment:**
    *   Cluster 0: Target niche promotions and unique products
    *   Cluster 1: Stock high-demand, mid-priced brands
    *   Cluster 2: Emphasize premium product selection
*   **Product Clusters:**
    *   Cluster 0: Broad product range with moderate similarities; suitable for general-purpose bundles targeting a wide audience
    *   Cluster 1: Tightly grouped products with consistent characteristics; ideal for price-based or complementary bundles
    *   Cluster 2: Distinct group of premium/niche products; suitable for high-end or limited-edition bundles
    *   Cluster 3: Small, unique product group; best promoted individually or paired with popular
*   **Shelf Space Clusters:**
    *   Cluster 0: Prioritize shelf space for easy customer access to high-demand, frequent-purchase items
    *   Cluster 1: Highlight premium products with end caps or creative shelf arrangements to boost cross-sales
    *   Cluster 2: Focus on improving stock consistency and rationalizing shelf space for low-demand items
*   **Anomaly Detection:** Identification of products with unusual stocking and pricing behaviors, such as high availability and high price, low availability and low price, and mid-price with low availability.
