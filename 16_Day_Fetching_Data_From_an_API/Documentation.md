# Day 16: Fetching Data from an API

In this documentation, we will discuss how to fetch data from an API using Python.

## What is an API?

API stands for Application Programming Interface, which allows software to communicate with other software. In simpler terms, it allows different software systems to interact with each other. An API provides a set of protocols and tools for building software applications.

## Steps to Fetch Data from an API using Python

### Step 1: Import necessary libraries
The first step is to import the necessary libraries. We will use the 'pandas' and 'requests' libraries to fetch and manipulate data from the API.


```python
import pandas as pd
import requests
```

### Step 2: Fetch data from the API
The next step is to fetch the data from the API. We will use the 'requests' library to make a request to the API.


```python
res=requests.get('https://api.covid19api.com/summary')
```

### Step 3: Convert the JSON data to a Pandas DataFrame
The data returned by the API is in JSON format. We can use the 'json()' method to convert it to a Python dictionary. We will then extract the necessary columns from the dictionary and convert it to a Pandas DataFrame.


```python
df=pd.DataFrame(res.json()['Countries'])[['Country','CountryCode','NewConfirmed','TotalConfirmed','NewDeaths','TotalDeaths','NewRecovered','TotalRecovered' ]]
```


```python
df
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
      <th>Country</th>
      <th>CountryCode</th>
      <th>NewConfirmed</th>
      <th>TotalConfirmed</th>
      <th>NewDeaths</th>
      <th>TotalDeaths</th>
      <th>NewRecovered</th>
      <th>TotalRecovered</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Afghanistan</td>
      <td>AF</td>
      <td>0</td>
      <td>209451</td>
      <td>0</td>
      <td>7896</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Albania</td>
      <td>AL</td>
      <td>14</td>
      <td>334457</td>
      <td>0</td>
      <td>3598</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Algeria</td>
      <td>DZ</td>
      <td>2</td>
      <td>271496</td>
      <td>0</td>
      <td>6881</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Andorra</td>
      <td>AD</td>
      <td>0</td>
      <td>47890</td>
      <td>0</td>
      <td>165</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Angola</td>
      <td>AO</td>
      <td>0</td>
      <td>105288</td>
      <td>0</td>
      <td>1933</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>192</th>
      <td>Venezuela (Bolivarian Republic)</td>
      <td>VE</td>
      <td>5</td>
      <td>552162</td>
      <td>0</td>
      <td>5854</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>193</th>
      <td>Viet Nam</td>
      <td>VN</td>
      <td>0</td>
      <td>11526994</td>
      <td>0</td>
      <td>43186</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>194</th>
      <td>Yemen</td>
      <td>YE</td>
      <td>0</td>
      <td>11945</td>
      <td>0</td>
      <td>2159</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>195</th>
      <td>Zambia</td>
      <td>ZM</td>
      <td>0</td>
      <td>343135</td>
      <td>0</td>
      <td>4057</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>196</th>
      <td>Zimbabwe</td>
      <td>ZW</td>
      <td>0</td>
      <td>264276</td>
      <td>0</td>
      <td>5671</td>
      <td>0</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
<p>197 rows × 8 columns</p>
</div>



### Step 4: Check the shape of the DataFrame
It is always a good practice to check the shape of the DataFrame to ensure that we have fetched the data correctly.


```python
df.shape
```




    (197, 8)



### Step 5: Save the DataFrame to a CSV file
Finally, we can save the DataFrame to a CSV file using the 'to_csv()' method.


```python
df.to_csv('Covid_Data.csv')
```

This is a simple way to fetch data from an API using Python.

## Additional Resources

For more information about working with APIs in Python, you can refer to the following resources: <br>

• <a href="https://docs.python-requests.org/en/latest/">Requests library documentation</a> <br>
• <a href="https://pandas.pydata.org/docs/">Pandas library documentation</a> 


```python

```
