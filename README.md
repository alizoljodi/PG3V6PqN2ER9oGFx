# Term Deposit Subscription Campaign Optimization

## Overview

As a growing player in the European banking sector, optimizing customer engagement and campaign efficiency is critical. This project aims to develop data-driven models to predict the likelihood of success for marketing calls promoting term deposit subscriptions. By analyzing customer and call-related features, we propose a multi-layered solution to enhance campaign effectiveness while reducing wasted resources.

## Dataset

The dataset includes 13 input features and an output variable (`y`) that indicates whether the customer agreed to the subscription. Key features include:

- **Demographic Information**: Age, job, marital status, and education level.
- **Financial Status**: Account balance, loan status, and housing information.
- **Campaign Interaction**: Number of contacts made, duration of the last call (in seconds), and date of the most recent contact.

### Key Insights from Exploratory Analysis
- About 93% of customers declined to join the campaign.
- The average call duration exceeds 250 seconds.
- The average number of calls per customer is slightly below 3.
- Over 37,000 calls were unsuccessful, resulting in more than 7,700 employee hours being spent without achieving desired outcomes.
![image](https://github.com/user-attachments/assets/f1131f51-b0b5-4ae8-afc9-916327d66158)

## Proposed Solution

### Step 1: Predictive Model for Success Estimation
We developed a **Gradient Boosting Classifier** as our first solution:
- **Objective**: Identify customers unlikely to convert and remove them from the potential customer list.
- **Training**: The model was trained and cross-validated using 5-fold validation.
- **Performance**: Achieved an accuracy of **93%**, enabling the reduction of 93% of the 7,700 employee hours from the previous campaign, saving over **7,000 hours**.

### Step 2: High-Precision Model for Future Engagement
We trained a **Linear Discriminant Analysis (LDA)** model as our second solution:
- **Objective**: Identify customers who are more likely to accept the offer in future calls, even if they declined initially.
- **Performance**: Achieved an accuracy of **92.6%**, providing a high-precision tool to focus on potential customers and improve success rates in subsequent interactions.

### Step 3: Customer Clustering and Success Analysis
A clustering algorithm was applied to segment customers based on shared features:
- **Objective**: Group customers into five distinct clusters and compute the probability of success within each cluster.
- **Outcome**: These clusters provide actionable insights for targeted engagement strategies and optimized resource allocation.

## Key Benefits
- Significant reduction in wasted employee hours.
- Enhanced targeting of potential customers through precision-driven models.
- Data-driven strategies for improved campaign outcomes and increased conversion rates.

## Tools and Techniques
- **Machine Learning Models**: Gradient Boosting Classifier, Linear Discriminant Analysis (LDA).
- **Validation**: 5-fold cross-validation for reliable performance metrics.
- **Clustering**: Algorithmic grouping of customers to identify patterns and probabilities of success.

## Conclusion

By integrating these models and approaches, we have developed a comprehensive solution to optimize term deposit subscription campaigns. This strategy enhances customer engagement, minimizes resource wastage, and ensures data-driven decision-making for future campaigns.
