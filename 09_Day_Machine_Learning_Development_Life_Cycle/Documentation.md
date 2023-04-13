# Day 9: Machine Learning Development Life Cycle (MLDLC/MLDC)

The Machine Learning Development Life Cycle (MLDLC/MLDC) is a process that outlines the stages involved in the development, deployment, and maintenance of a machine learning project. It involves several stages that enable a systematic approach to building, testing, and deploying machine learning models. 


## Frame the problem: 
Identify the problem that needs to be solved and define it in a clear and concise manner.

## Gather data: 
Collect data from various sources like CSV, API, and Web Scraping, as well as from databases. <br>
CSV (Comma-Separated Values) is a file format that stores data in a tabular form, where each row represents a record and each column represents a feature or attribute of that record. <br>
APIs (Application Programming Interfaces) allow you to access data from external sources using programming languages. <br>
Web scraping involves extracting data from websites using automated tools or web scrapers.

## Data Preprocessing: 
This step involves cleaning the data by removing duplicate values, missing values, and outliers. It also involves scaling the data to a common scale. <br>
Removing duplicates involves identifying and removing identical records in the dataset. <br>
Removing missing values involves identifying and handling missing values in the dataset. This can be done by imputing the missing values or removing the records altogether. <br>
Outliers are data points that are significantly different from other data points in the dataset. Outliers can be identified using statistical methods and handled by either removing them or adjusting their values. <br>
Scaling involves transforming the data so that each feature has a similar scale. This can be done using standardization or normalization techniques.

## Exploratory Data Analysis: 
This step involves visualizing the data and conducting univariate and bivariate analysis, outlier detection, and managing imbalanced data. <br>
Visualization involves creating plots such as histograms, scatter plots, and box plots to explore the distribution of the data and identify patterns. <br>
Univariate analysis involves analyzing the distribution of individual features or variables in the dataset. <br>
Bivariate analysis involves analyzing the relationship between two variables in the dataset. <br>
Outlier detection involves identifying and handling outliers in the data. <br>
Managing imbalanced data involves handling datasets where one class is more dominant than the other. This can be done by undersampling the dominant class or oversampling the minority class to balance the dataset.

## Feature Engineering and Selection: 
This step involves selecting the most relevant features for the model and transforming the data into a suitable format for model training.

## Model Training, Evaluation, and Selection: 
This step involves selecting the appropriate algorithm for the problem and training the model on the dataset. It also involves evaluating the performance of the model and selecting the best model for deployment.

## Model deployment: 
This step involves deploying the model in a production environment for real-world use. This can involve setting up an API or integrating the model with other software systems.

## Testing: 
This step involves testing the model in a production environment to ensure that it performs as expected. <br>
A/B testing is a type of testing used in the Machine Learning Development Life Cycle to evaluate the performance of two versions of a model, A and B, in a real-world environment. It is also known as split testing, which is a marketing experiment to test multiple variations of a campaign and determine the better performer. For instance, marketers may show version A of a piece of marketing content to one half of their audience and version B to another.

## Optimization: 
This step involves ensuring the model's performance is maintained over time. This includes tasks such as data backup, load balancing to ensure the model can handle increased traffic, and retraining the model to incorporate new data or address changes in the business environment. In addition, models may be retrained using different algorithms or hyperparameters to improve performance.

# 
By following these steps, we can ensure that the Machine Learning model is developed and deployed in a structured and efficient manner.



