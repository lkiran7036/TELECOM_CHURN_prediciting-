# Telecom Churn Prediction Project

## Business Problem Overview

In the highly competitive telecom industry, where customers frequently switch between providers, customer retention becomes crucial. With a typical annual churn rate of 15-25%, telecom companies face significant challenges. The cost of acquiring a new customer is substantially higher, by 5-10 times, than retaining an existing one, making customer retention a critical focus area, especially for incumbent operators aiming to retain high-value customers. This project involves analyzing customer-level data from a leading telecom firm to build predictive models for identifying high-risk churn customers and pinpointing primary churn indicators.

## Understanding and Defining Churn

Churn in the telecom industry can occur in two payment models:

- **Postpaid:** Customers pay after service usage. Churn is directly identifiable when customers request service termination.
- **Prepaid:** Customers prepay for services. Churn is inferred when customers cease usage without notice, complicating churn predictions due to potential temporary service suspensions (e.g., travel).

Given the prevalence of prepaid services in India and Southeast Asia, this project focuses on this market and adopts a usage-based churn definition.

### Definitions of Churn

- **Revenue-based churn:** Customers not using any revenue-generating services like calls, internet, or SMS over a period might be considered churners, especially if their revenue falls below a certain threshold (e.g., INR 4 per month).
- **Usage-based churn:** Customers showing no service usage, both incoming and outgoing, are considered churners.

The project uses the usage-based model to define churn, emphasizing the need to identify churn early enough to manage retention proactively.

## High-value Churn

About 80% of revenue typically comes from the top 20% of customers. This project targets these high-value customers, defining them based on the 70th percentile of the average recharge amount in the initial months of data collection.

## Understanding the Business Objective and the Data

The dataset spans four consecutive months, labeled as months 6 to 9. The aim is to predict potential churn in the ninth month using data from the first three months to understand typical customer behaviors and lifecycle phases, which include:

- **Good phase:** The customer exhibits standard behavior with satisfactory service usage.
- **Action phase:** The customer might show varied behavior due to declining service satisfaction or better offers from competitors.
- **Churn phase:** The customer has likely ceased using the services, marking this as the churn phase.

### Data Preparation Steps

1. **Feature Derivation:** Extract new features based on business insights.
2. **High-value Customer Filtering:** Focus analyses on high-value customers using defined recharge thresholds.
3. **Churn Tagging and Feature Removal:** Identify churners based on service usage in the churn phase and remove features related to this phase for model training.

## Modelling Strategy

The approach includes preprocessing data, feature engineering, exploratory analysis, dimensionality reduction (e.g., PCA), and model training with a focus on handling class imbalance due to the low churn rate.

### Model Evaluation

Select evaluation metrics that prioritize identifying churners accurately, reflecting the business objective of minimizing customer loss.

### Feature Importance

Use logistic regression or tree-based models to understand and visualize the predictors of churn, aiding in strategic decision-making for churn management.

## Recommendations and Conclusion

Offer strategies for customer retention based on predictive insights, helping the telecom company reduce churn and enhance customer satisfaction.