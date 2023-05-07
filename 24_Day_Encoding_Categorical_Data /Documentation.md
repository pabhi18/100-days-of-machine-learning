# Day 24: Encoding Categorical Data

In machine learning, we often come across datasets with categorical data. Categorical data is non-numerical data that is represented by labels or names. Examples of categorical data include gender, color, and type of car.

There are two types of data: numerical data and categorical data. Numerical data can be measured and is represented by numbers, whereas categorical data cannot be measured and is represented by labels or names.


## Types of Categorical Data

Categorical data can be further classified into two types: 
- Nominal data 
- Ordinal data.

Nominal data is a type of categorical data that has no inherent order or ranking. This means that the values or categories of nominal data cannot be arranged in any particular order. For example, colors, gender, or countries are examples of nominal data.

On the other hand, ordinal data is also a type of categorical data, but it has an inherent order or ranking to it. This means that the values or categories of ordinal data can be arranged in a particular order. For example, educational level (high school, bachelor's degree, master's degree), or customer ratings (poor, fair, good, excellent) are examples of ordinal data.


## Types of Encoding

To use categorical data in machine learning algorithms, we need to convert them into numerical values. There are several ways to encode categorical data, including:

- Ordinal Encoding
- One Hot Encoding
- Label Encoding


## Ordinal Encoding

Ordinal encoding is a process of converting ordinal data into numerical data. Ordinal data has a specific order, and ordinal encoding assigns a unique numerical value to each category based on its rank or position in the order.

For example, if we have a dataset with a column for education level that includes categories like "High School", "College", and "Graduate School", we can use ordinal encoding to assign the values 1, 2, and 3 respectively to these categories based on their rank in the order.

## Label Encoding
Label encoding is a process of converting nominal data into numerical data. Nominal data has no order or ranking, and label encoding assigns a unique numerical value to each category. However, unlike ordinal encoding, there is no order or ranking assigned to these values and it should be noted that label encoding should only be applied to output data, or the target variable in a machine learning model.
For example, if we have a dataset with a column for color that includes categories like "Red", "Green", and "Blue", we can use label encoding to assign the values 1, 2, and 3 respectively to these categories.

## Example


```python
import pandas as pd
import numpy as np
```


```python
df = pd.read_csv('customer.csv')
```


```python
df.sample(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>age</th>
      <th>gender</th>
      <th>review</th>
      <th>education</th>
      <th>purchased</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>34</th>
      <td>86</td>
      <td>Male</td>
      <td>Average</td>
      <td>School</td>
      <td>No</td>
    </tr>
    <tr>
      <th>36</th>
      <td>34</td>
      <td>Female</td>
      <td>Good</td>
      <td>UG</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>19</th>
      <td>97</td>
      <td>Male</td>
      <td>Poor</td>
      <td>PG</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>13</th>
      <td>57</td>
      <td>Female</td>
      <td>Average</td>
      <td>School</td>
      <td>No</td>
    </tr>
    <tr>
      <th>16</th>
      <td>59</td>
      <td>Male</td>
      <td>Poor</td>
      <td>UG</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>22</th>
      <td>18</td>
      <td>Female</td>
      <td>Poor</td>
      <td>PG</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>46</th>
      <td>64</td>
      <td>Female</td>
      <td>Poor</td>
      <td>PG</td>
      <td>No</td>
    </tr>
    <tr>
      <th>11</th>
      <td>74</td>
      <td>Male</td>
      <td>Good</td>
      <td>UG</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>8</th>
      <td>65</td>
      <td>Female</td>
      <td>Average</td>
      <td>UG</td>
      <td>No</td>
    </tr>
    <tr>
      <th>47</th>
      <td>38</td>
      <td>Female</td>
      <td>Good</td>
      <td>PG</td>
      <td>Yes</td>
    </tr>
  </tbody>
</table>
</div>




```python
df = df.iloc[:,2:]
```


```python
df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>review</th>
      <th>education</th>
      <th>purchased</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Average</td>
      <td>School</td>
      <td>No</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Poor</td>
      <td>UG</td>
      <td>No</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Good</td>
      <td>PG</td>
      <td>No</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Good</td>
      <td>PG</td>
      <td>No</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Average</td>
      <td>UG</td>
      <td>No</td>
    </tr>
  </tbody>
</table>
</div>




```python
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(df.iloc[:,0:2],df.iloc[:,-1], test_size=0.2)
```


```python
from sklearn.preprocessing import OrdinalEncoder
```


```python
oe = OrdinalEncoder(categories=[['Poor', 'Average', 'Good'], ['School', 'UG', 'PG']])
```


```python
oe.fit(X_train)
```




<style>#sk-container-id-1 {color: black;background-color: white;}#sk-container-id-1 pre{padding: 0;}#sk-container-id-1 div.sk-toggleable {background-color: white;}#sk-container-id-1 label.sk-toggleable__label {cursor: pointer;display: block;width: 100%;margin-bottom: 0;padding: 0.3em;box-sizing: border-box;text-align: center;}#sk-container-id-1 label.sk-toggleable__label-arrow:before {content: "▸";float: left;margin-right: 0.25em;color: #696969;}#sk-container-id-1 label.sk-toggleable__label-arrow:hover:before {color: black;}#sk-container-id-1 div.sk-estimator:hover label.sk-toggleable__label-arrow:before {color: black;}#sk-container-id-1 div.sk-toggleable__content {max-height: 0;max-width: 0;overflow: hidden;text-align: left;background-color: #f0f8ff;}#sk-container-id-1 div.sk-toggleable__content pre {margin: 0.2em;color: black;border-radius: 0.25em;background-color: #f0f8ff;}#sk-container-id-1 input.sk-toggleable__control:checked~div.sk-toggleable__content {max-height: 200px;max-width: 100%;overflow: auto;}#sk-container-id-1 input.sk-toggleable__control:checked~label.sk-toggleable__label-arrow:before {content: "▾";}#sk-container-id-1 div.sk-estimator input.sk-toggleable__control:checked~label.sk-toggleable__label {background-color: #d4ebff;}#sk-container-id-1 div.sk-label input.sk-toggleable__control:checked~label.sk-toggleable__label {background-color: #d4ebff;}#sk-container-id-1 input.sk-hidden--visually {border: 0;clip: rect(1px 1px 1px 1px);clip: rect(1px, 1px, 1px, 1px);height: 1px;margin: -1px;overflow: hidden;padding: 0;position: absolute;width: 1px;}#sk-container-id-1 div.sk-estimator {font-family: monospace;background-color: #f0f8ff;border: 1px dotted black;border-radius: 0.25em;box-sizing: border-box;margin-bottom: 0.5em;}#sk-container-id-1 div.sk-estimator:hover {background-color: #d4ebff;}#sk-container-id-1 div.sk-parallel-item::after {content: "";width: 100%;border-bottom: 1px solid gray;flex-grow: 1;}#sk-container-id-1 div.sk-label:hover label.sk-toggleable__label {background-color: #d4ebff;}#sk-container-id-1 div.sk-serial::before {content: "";position: absolute;border-left: 1px solid gray;box-sizing: border-box;top: 0;bottom: 0;left: 50%;z-index: 0;}#sk-container-id-1 div.sk-serial {display: flex;flex-direction: column;align-items: center;background-color: white;padding-right: 0.2em;padding-left: 0.2em;position: relative;}#sk-container-id-1 div.sk-item {position: relative;z-index: 1;}#sk-container-id-1 div.sk-parallel {display: flex;align-items: stretch;justify-content: center;background-color: white;position: relative;}#sk-container-id-1 div.sk-item::before, #sk-container-id-1 div.sk-parallel-item::before {content: "";position: absolute;border-left: 1px solid gray;box-sizing: border-box;top: 0;bottom: 0;left: 50%;z-index: -1;}#sk-container-id-1 div.sk-parallel-item {display: flex;flex-direction: column;z-index: 1;position: relative;background-color: white;}#sk-container-id-1 div.sk-parallel-item:first-child::after {align-self: flex-end;width: 50%;}#sk-container-id-1 div.sk-parallel-item:last-child::after {align-self: flex-start;width: 50%;}#sk-container-id-1 div.sk-parallel-item:only-child::after {width: 0;}#sk-container-id-1 div.sk-dashed-wrapped {border: 1px dashed gray;margin: 0 0.4em 0.5em 0.4em;box-sizing: border-box;padding-bottom: 0.4em;background-color: white;}#sk-container-id-1 div.sk-label label {font-family: monospace;font-weight: bold;display: inline-block;line-height: 1.2em;}#sk-container-id-1 div.sk-label-container {text-align: center;}#sk-container-id-1 div.sk-container {/* jupyter's `normalize.less` sets `[hidden] { display: none; }` but bootstrap.min.css set `[hidden] { display: none !important; }` so we also need the `!important` here to be able to override the default hidden behavior on the sphinx rendered scikit-learn.org. See: https://github.com/scikit-learn/scikit-learn/issues/21755 */display: inline-block !important;position: relative;}#sk-container-id-1 div.sk-text-repr-fallback {display: none;}</style><div id="sk-container-id-1" class="sk-top-container"><div class="sk-text-repr-fallback"><pre>OrdinalEncoder(categories=[[&#x27;Poor&#x27;, &#x27;Average&#x27;, &#x27;Good&#x27;], [&#x27;School&#x27;, &#x27;UG&#x27;, &#x27;PG&#x27;]])</pre><b>In a Jupyter environment, please rerun this cell to show the HTML representation or trust the notebook. <br />On GitHub, the HTML representation is unable to render, please try loading this page with nbviewer.org.</b></div><div class="sk-container" hidden><div class="sk-item"><div class="sk-estimator sk-toggleable"><input class="sk-toggleable__control sk-hidden--visually" id="sk-estimator-id-1" type="checkbox" checked><label for="sk-estimator-id-1" class="sk-toggleable__label sk-toggleable__label-arrow">OrdinalEncoder</label><div class="sk-toggleable__content"><pre>OrdinalEncoder(categories=[[&#x27;Poor&#x27;, &#x27;Average&#x27;, &#x27;Good&#x27;], [&#x27;School&#x27;, &#x27;UG&#x27;, &#x27;PG&#x27;]])</pre></div></div></div></div></div>




```python
X_train = oe.transform(X_train)
X_test = oe.transform(X_test)
```


```python
X_train

```




    array([[2., 2.],
           [2., 2.],
           [0., 2.],
           [1., 1.],
           [0., 2.],
           [1., 2.],
           [0., 1.],
           [1., 2.],
           [2., 2.],
           [2., 1.],
           [2., 0.],
           [1., 1.],
           [2., 1.],
           [1., 1.],
           [0., 1.],
           [1., 1.],
           [0., 1.],
           [1., 0.],
           [0., 2.],
           [1., 0.],
           [2., 2.],
           [0., 2.],
           [1., 0.],
           [0., 0.],
           [1., 1.],
           [0., 0.],
           [0., 0.],
           [2., 0.],
           [2., 1.],
           [0., 2.],
           [1., 0.],
           [0., 0.],
           [1., 1.],
           [2., 0.],
           [1., 2.],
           [0., 2.],
           [2., 2.],
           [2., 1.],
           [0., 2.],
           [2., 1.]])




```python
X_test
```




    array([[0., 1.],
           [2., 1.],
           [2., 2.],
           [1., 0.],
           [2., 0.],
           [2., 0.],
           [0., 2.],
           [2., 0.],
           [0., 2.],
           [0., 0.]])




```python
from sklearn.preprocessing import LabelEncoder
```


```python
le = LabelEncoder()
```


```python
le.fit(y_train)
```




<style>#sk-container-id-2 {color: black;background-color: white;}#sk-container-id-2 pre{padding: 0;}#sk-container-id-2 div.sk-toggleable {background-color: white;}#sk-container-id-2 label.sk-toggleable__label {cursor: pointer;display: block;width: 100%;margin-bottom: 0;padding: 0.3em;box-sizing: border-box;text-align: center;}#sk-container-id-2 label.sk-toggleable__label-arrow:before {content: "▸";float: left;margin-right: 0.25em;color: #696969;}#sk-container-id-2 label.sk-toggleable__label-arrow:hover:before {color: black;}#sk-container-id-2 div.sk-estimator:hover label.sk-toggleable__label-arrow:before {color: black;}#sk-container-id-2 div.sk-toggleable__content {max-height: 0;max-width: 0;overflow: hidden;text-align: left;background-color: #f0f8ff;}#sk-container-id-2 div.sk-toggleable__content pre {margin: 0.2em;color: black;border-radius: 0.25em;background-color: #f0f8ff;}#sk-container-id-2 input.sk-toggleable__control:checked~div.sk-toggleable__content {max-height: 200px;max-width: 100%;overflow: auto;}#sk-container-id-2 input.sk-toggleable__control:checked~label.sk-toggleable__label-arrow:before {content: "▾";}#sk-container-id-2 div.sk-estimator input.sk-toggleable__control:checked~label.sk-toggleable__label {background-color: #d4ebff;}#sk-container-id-2 div.sk-label input.sk-toggleable__control:checked~label.sk-toggleable__label {background-color: #d4ebff;}#sk-container-id-2 input.sk-hidden--visually {border: 0;clip: rect(1px 1px 1px 1px);clip: rect(1px, 1px, 1px, 1px);height: 1px;margin: -1px;overflow: hidden;padding: 0;position: absolute;width: 1px;}#sk-container-id-2 div.sk-estimator {font-family: monospace;background-color: #f0f8ff;border: 1px dotted black;border-radius: 0.25em;box-sizing: border-box;margin-bottom: 0.5em;}#sk-container-id-2 div.sk-estimator:hover {background-color: #d4ebff;}#sk-container-id-2 div.sk-parallel-item::after {content: "";width: 100%;border-bottom: 1px solid gray;flex-grow: 1;}#sk-container-id-2 div.sk-label:hover label.sk-toggleable__label {background-color: #d4ebff;}#sk-container-id-2 div.sk-serial::before {content: "";position: absolute;border-left: 1px solid gray;box-sizing: border-box;top: 0;bottom: 0;left: 50%;z-index: 0;}#sk-container-id-2 div.sk-serial {display: flex;flex-direction: column;align-items: center;background-color: white;padding-right: 0.2em;padding-left: 0.2em;position: relative;}#sk-container-id-2 div.sk-item {position: relative;z-index: 1;}#sk-container-id-2 div.sk-parallel {display: flex;align-items: stretch;justify-content: center;background-color: white;position: relative;}#sk-container-id-2 div.sk-item::before, #sk-container-id-2 div.sk-parallel-item::before {content: "";position: absolute;border-left: 1px solid gray;box-sizing: border-box;top: 0;bottom: 0;left: 50%;z-index: -1;}#sk-container-id-2 div.sk-parallel-item {display: flex;flex-direction: column;z-index: 1;position: relative;background-color: white;}#sk-container-id-2 div.sk-parallel-item:first-child::after {align-self: flex-end;width: 50%;}#sk-container-id-2 div.sk-parallel-item:last-child::after {align-self: flex-start;width: 50%;}#sk-container-id-2 div.sk-parallel-item:only-child::after {width: 0;}#sk-container-id-2 div.sk-dashed-wrapped {border: 1px dashed gray;margin: 0 0.4em 0.5em 0.4em;box-sizing: border-box;padding-bottom: 0.4em;background-color: white;}#sk-container-id-2 div.sk-label label {font-family: monospace;font-weight: bold;display: inline-block;line-height: 1.2em;}#sk-container-id-2 div.sk-label-container {text-align: center;}#sk-container-id-2 div.sk-container {/* jupyter's `normalize.less` sets `[hidden] { display: none; }` but bootstrap.min.css set `[hidden] { display: none !important; }` so we also need the `!important` here to be able to override the default hidden behavior on the sphinx rendered scikit-learn.org. See: https://github.com/scikit-learn/scikit-learn/issues/21755 */display: inline-block !important;position: relative;}#sk-container-id-2 div.sk-text-repr-fallback {display: none;}</style><div id="sk-container-id-2" class="sk-top-container"><div class="sk-text-repr-fallback"><pre>LabelEncoder()</pre><b>In a Jupyter environment, please rerun this cell to show the HTML representation or trust the notebook. <br />On GitHub, the HTML representation is unable to render, please try loading this page with nbviewer.org.</b></div><div class="sk-container" hidden><div class="sk-item"><div class="sk-estimator sk-toggleable"><input class="sk-toggleable__control sk-hidden--visually" id="sk-estimator-id-2" type="checkbox" checked><label for="sk-estimator-id-2" class="sk-toggleable__label sk-toggleable__label-arrow">LabelEncoder</label><div class="sk-toggleable__content"><pre>LabelEncoder()</pre></div></div></div></div></div>




```python
le.classes_
```




    array(['No', 'Yes'], dtype=object)




```python
y_train = le.transform(y_train)
y_test = le.transform(y_test)
```


```python
y_train
```




    array([1, 0, 1, 0, 1, 1, 0, 0, 1, 1, 0, 1, 1, 0, 0, 0, 1, 0, 0, 0, 1, 1,
           1, 1, 0, 1, 0, 0, 1, 1, 1, 0, 1, 0, 1, 0, 1, 1, 0, 0])



## Conclusion

Categorical data is an important type of data in machine learning, and encoding it into numerical values is essential for using it in machine learning algorithms. Depending on the type of categorical data, we can use different encoding techniques such as ordinal encoding, one hot encoding, and label encoding to convert it into numerical values.
