# Day 3: Types of Machine Learning

Machine Learning can be broadly classified into four types: supervised, unsupervised, semi-supervised, and reinforcement learning. In this documentation, we will take a closer look at each of these types of Machine Learning and understand their applications with examples.

<img src="learning.png" height="200">


## Supervised Learning

Supervised learning is a type of ML where the model is trained on labeled data, meaning that the input data is associated with known output values. The goal of supervised learning is to predict the output for new, unseen inputs.

For example, consider a dataset of student records that includes their IQ scores, CGPA, and whether they got placed in a job or not. The task here is to predict whether a new student will get placed in a job or not, based on their IQ and CGPA. This is a binary classification problem, as the output is a binary variable (yes or no).

Another example is to predict the salary of an employee based on their years of experience. This is a regression problem, as the output is a numerical value.

### Regression
Regression is a type of supervised learning where the output variable is a continuous numerical value. In the student placement example, the task is to predict a student's expected salary based on their IQ and CGPA.

### Classification
Classification is a type of supervised learning where the output variable is categorical. In the student placement example, the task is to predict whether a student will get placed in a job or not based on their IQ and CGPA.


## Unsupervised Learning

Unsupervised learning is a type of ML where the model is trained on unlabeled data, meaning that there is no known output value associated with the input data. The goal of unsupervised learning is to discover patterns and relationships in the data.

For example, consider a dataset of student records that includes their IQ scores and CGPA. The task here is to group the students based on their similarities in terms of IQ and CGPA. This is a clustering problem, as there is no known output value associated with each data point.

Unsupervised Learning can further be classified into four types: Clustering, Dimensionality Reduction, Anomaly Detection, and Association.

### Clustering

Clustering is a type of unsupervised learning where the algorithm groups data points together based on their similarities. In the student example, clustering can group students with similar IQ and CGPA together.

### Dimensionality Reduction

Dimensionality Reduction is a type of unsupervised learning where the algorithm reduces the number of input variables by identifying the most important features that contribute to the output.

### Anomaly Detection

Anomaly Detection is a type of unsupervised learning where the algorithm identifies outliers or abnormal data points in the dataset.

### Association

Association in Machine Learning is about discovering relationships between items in large datasets, such as identifying which products are often purchased together.


## Semi-Supervised Learning

Semi-supervised learning is a type of ML where the model is trained on a combination of labeled and unlabeled data. This is useful when it is difficult or expensive to obtain a large amount of labeled data, but there is plenty of unlabeled data available.

For example, consider Google Photos, which uses semi-supervised learning to automatically categorize and tag photos. The model is trained on a small set of labeled data (such as photos that have already been manually labeled), but can then use unsupervised learning to categorize the rest of the photos.


## Reinforcement Learning

Reinforcement learning is a type of ML where the model learns from feedback in the form of rewards or punishments. The goal of reinforcement learning is to learn a policy that maximizes the cumulative reward over time.

An example of reinforcement learning could be training a self-driving car to learn how to navigate through traffic by rewarding it for making correct decisions and penalizing it for making wrong ones. The car is constantly learning from its mistakes and adjusting its behavior accordingly.

#

In conclusion, Machine Learning can be classified into four main types: supervised, unsupervised, semi-supervised, and reinforcement learning. Each type of Machine Learning has its own strengths and weaknesses and is suitable for different use cases depending on the nature of the problem and the available data.




