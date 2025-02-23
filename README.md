# Customer Churn Prediction

## Objective
The primary objective of this analysis is to predict customer churn—whether a customer will leave or remain with the company. By identifying patterns that lead to churn, we aim to provide actionable insights that allow the business to take proactive measures to retain valuable customers. Understanding the key factors influencing customer decisions enables the development of a predictive model to improve customer retention strategies.

## Dataset Description
The dataset contains customer account details, call behavior metrics (day, evening, night, and international call minutes), and the number of interactions customers have with customer service. The goal is to identify factors contributing most to customer churn, uncover patterns, and use these insights to build an effective predictive model for better retention efforts.

## Exploratory Data Analysis (EDA)

### Key Insights:
1. **Relationships between charges and minutes**
   - There is a perfect correlation between charge columns (e.g., day charge, evening charge) and the corresponding minutes columns (e.g., day minutes, evening minutes).
   - No significant relationship was found between these charge and minute variables and other dataset columns.

2. **Customer Service Interactions**
   - Customers who contact customer service frequently tend to have a higher likelihood of churning.
   - This suggests that dissatisfaction or unresolved issues with the service may be leading to churn, making customer service interactions a potential red flag.

3. **International Plan**
   - Customers without an international plan exhibit a significantly higher median churn rate.
   - This indicates that the presence or absence of an international plan plays an important role in retention.
   - Customers with an international plan tend to have a lower churn rate, suggesting that offering or maintaining such plans could help reduce churn.

4. **VoiceMail Plan**
   - Customers subscribed to a voicemail plan have a lower churn rate.
   - This suggests that voicemail service adds value to customers, encouraging retention.

## Feature Engineering
Feature importance analysis was conducted to identify key features influencing churn.  
- **Total day charge** and **Total day minutes** emerged as the most influential factors.
- Right-skewed features were transformed using a log transformation.
- Left-skewed features were handled using a reciprocal log transformation.

## Modeling and Metrics
The following algorithms were selected based on the dataset’s size and complexity:

- **Logistic Regression and Decision Tree**: Baseline models for interpretability and ease of use.
- **Random Forest and Gradient Boosting**: More robust models with higher performance.

### Model Evaluation Metrics:
- **F1-Score**
- **Recall**
- **Precision**

### Key Findings from Modeling:
1. **Random Forest**
   - Showed signs of overfitting, performing significantly better on training data than test data.
   - This suggests the model may not generalize well to unseen data.

2. **Gradient Boosting**
   - Demonstrated consistent performance between training and testing data.
   - Showed marginally better Precision and F1-Score compared to other models.
   - Metrics for training and testing were closer, indicating better generalization.

### Best Model Selection
- **Gradient Boosting was selected as the best model** due to its balanced performance, better generalization, and higher precision and F1-Score.

## Conclusion
Key factors influencing customer churn include:
- **Presence of an international plan**
- **Frequency of customer service interactions**
- **Total charges and minutes across different time periods**

These insights can be used to develop targeted retention strategies, such as improving customer service interactions and offering incentives for international plans, to reduce churn and enhance customer loyalty.

---

## How to Install Dependencies
1. Clone the repository:
    ```
   pip install -r requirements.txt
   ```
