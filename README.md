# **PURWADHIKA CAPSTONE 3 & 4: MACHINE LEARNING & CLOUD COMPUTING (DTIDS On-Campus Batam 2024)**

This project aims to build a machine learning classification model to predict customer churn for a telecom customer churn dataset provided by Purwadhika. The model is then uploaded to the Google Cloud Platform (GCP) to enable single value and batch predictions.

# Telco Customer Churn Prediction

**1. Business Domain Understanding** 

Customer Churn is defined as the event when customers decide to stop subscribing to a service provided by a company. The telecommunications industry, in particular, suffers from a high degree of customer churn. This is due to a myriad of different factors. Some of the reasons that cause customers to churn in the industry are poor service quality, competitors offering customers with better deals, and the low barrier to switching to other providers. 
Customer churn is a very important indicator of the liquidity of a telecom company, as its short-term profit is measured by the revenue gained from the periodic cash flows obtained from subscription contracts. The cutoff of these regular subscriptions would mean losing the company's primary means of financing its operations and repaying its short-term debt. Therefore, it can be concluded that minimizing the loss of regular customer subscriptions (minimizing churn) is of the utmost importance for a telecommunications company.

**2. Business Problem Formulation**

The given dataset shows that a significant amount of customers ended up churning from a telecom company. By implementing a machine learning classification model to predict whether its customers will churn or not, the company could reduce the rate of churn of its customers and reduce their losses resulting from churn. The company could also set up preventive measures to stop customers from churning, such as delivering targeted retention programs or offering personalized discounts or offers based on a given customer's characteristics. In addition to that, the company would have the benefit of automating its churn identification process, instead of identifying which customers will churn manually. This results in the improvement of the time and cost efficiency of customer retention decision-making.

**3. Analytical Context**

The telecom company wants to prevent customers from churning. 
Customers who are predicted to churn will be offered special discounts or offers for cheaper or better quality services in order to prevent them from churning. 
The historical data was collected from about 5000 of the company's customers about the types of subcriptions the customers were subscribed to, data about their subscription transactions, and whether the customer churned their subscriptions by the end of the observation period.
The company is interested to know which customers will stop their subscriptions based on the features provided in this dataset. By classifying customers into those who will churn and those who won't, we could target customer retention programs to customers who are predicted to churn, and continue serving customers who aren't predicted to churn as usual. By doing this, we can prevent customers from churning without incurring too much unnecessary retention costs.

The dataset contains observations for around 5000 of the company's customers. This project aims to build an ML model that can predict if the customer will churn from the company or not based on certain features provided in the dataset.
This project aims to simulate the role of a data scientist in the telecommunications company.

**4. Evaluation Metric**

This project aims to identify as many churning customers as possible (higher recall), at the cost of having a bias towards falsely identifying non-churning customers as churning (lower precision). As the cost of misclassifying non-churning customers as churning is non-zero and the cost of misclassifying churning customers as not churning is higher, the evaluation metric should be f2, the weighted average of recall and precision with recall having the larger weight. This is done with assumption that the cost incurred for implementing customer retention strategies is lower than the cost incurred by customer churn. This is assumed from the premise that the profits gained from a customer subscription should ideally exceed the retention cost of targeting the particular customer, in order for the retention efforts to be worth while.
Therefore, we will focus more on the model's recall score because we are more intersted in minimizing false negatives than we are in minimizing false positives for the positive class.

- **False Negative (FN):** if a customer is predicted not to churn, but he/she actually did. 
- **False Positive (FP):** if a customer is predicted to churn, but he/she actually did not. 

- **Cost of FN:** we lost a customer to churn.
- **Cost of FP:** We incurred unnecessary cost from targeting a non-churning customer.
