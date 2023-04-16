# Day 13: Framing a Machine Learning Problem

In this session, we will learn about framing a machine learning problem by exploring an example of decreasing churn rate of Netflix.


## Business Problem to Machine Learning Problem
As a business, Netflix's primary goal is to increase its revenue by retaining more customers. However, it has been observed that a significant number of customers are leaving the platform, which is a major concern. Therefore, Netflix's machine learning problem is to predict which customers are likely to churn so that proactive measures can be taken to retain them. By reducing the churn rate, Netflix can prevent revenue loss and increase revenue by retaining loyal customers. In summary, Netflix's business problem of revenue growth has been transformed into an ML problem of churn prediction.

## Type of Problem
Using the same example, we will discuss the type of problem we are dealing with. <br>
The problem of decreasing the churn rate of Netflix can be framed as a classification problem: predicting whether a customer will cancel their subscription or not. However, instead of focusing solely on predicting the outcome, we should be concerned with understanding the likelihood of a customer canceling. This way, we can offer targeted discounts or promotions to customers who are most likely to churn, improving our chances of retaining them as subscribers. Therefore, this becomes a regression problem, where the goal is to predict the probability of a customer canceling their subscription.

## Getting Data
To build a machine learning model for this problem, we need to collect relevant data. In the context of Netflix, we can consider the following factors to predict churn: <br>

1. Watch Time: How much time a customer spends watching Netflix. <br>
2. Search but not find: When a customer searches for content but does not find what they are looking for. <br>
3. Content left in the middle: When a customer stops watching a show or movie before it ends. <br>
4. Clicked on recommendation (order of recommendation): The order of recommended shows or movies a customer clicks on.

## Metrics to Measure
After collecting data, we need to determine how to measure the effectiveness of our model. In this case, we can use metrics such as accuracy, precision, recall, and F1-score to evaluate the performance of our model.

## Online vs Batch Learning
In this case, online learning may be more appropriate because we want to constantly update our model to reflect the changing behavior of customers. Batch learning, on the other hand, would require collecting a large amount of data before updating the model.

## Check Assumptions
Finally, we need to check the assumptions we made when building the model. For example, we assume that our code will run on all machines with the required software and hardware specifications. We also assume that there are no compatibility issues with the dependencies and packages used in our code. However, it is important to thoroughly test our code on different machines and environments to ensure that it runs smoothly and produces accurate results.
