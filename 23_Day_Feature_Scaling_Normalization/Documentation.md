# Day 23:Feature Scaling - Normalization

Normalization is a common technique used in data preparation for machine learning. The purpose of normalization is to change the values of numeric columns in the dataset to use a common scale, without losing important information or distorting differences in the range of values. This ensures that the features are on the same scale, which can help machine learning algorithms perform better.


## Types Of Normalization
There are several types of normalization techniques available, including:
•Min-Max Scaling <br>
•Mean Normalization <br>
•Max Absorb <br>
•Robust Scaling <br>


## Min-Max Scaling: 
This technique scales the values in a column to a range between 0 and 1, using the following formula:
X_norm = (X - X_min) / (X_max - X_min)
where X is the original value, X_min and X_max are the minimum and maximum values in the column, respectively, and X_norm is the normalized value.

## Mean Normalization: 
This technique scales the values in a column so that they have zero mean and unit variance. The formula used for mean normalization is:
X_norm = (X - X_mean) / X_std
where X is the original value, X_mean is the mean value of the column, X_std is the standard deviation of the column, and X_norm is the normalized value.

## Max Absorb:
 This technique scales the values in a column to a range between -1 and 1, using the following formula:
X_norm = X / max(abs(X))

## Robust Scaling: 
This technique scales the values in a column based on their percentiles, making it more robust to outliers. The formula used for robust scaling is:
X_norm = (X - Q2) / (Q3 - Q1)
where X is the original value, Q1, Q2, and Q3 are the 25th, 50th, and 75th percentiles of the column, respectively, and X_norm is the normalized value.

## Standardization vs Normalization

Standardization and normalization are both methods of scaling the data, but they differ in their approach.  Normalization scales the data to a fixed range, while standardization scales the data so that it has zero mean and unit variance.Standardization is useful when the features are normally distributed and when we want to give equal importance to all the features. Normalization is useful when we want to compare the relative magnitudes of different features, and when the features have varying scales or are not normally distributed. The choice between these techniques ultimately depends on the nature of the data and the problem at hand.
