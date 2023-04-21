# Day 14: Working with CSV Files

When working with data in Python, one common way to gather data is through CSV files. CSV, which stands for comma-separated values, is a file format used to store data in a tabular form, with each row representing a record and each column representing a field.

## Types of Gathering Data

There are several ways to gather data, including:<br>

CSV files <br>
JSON/SQL <br>
Fetch API<br>
Web scraping

## In this documentation, we will focus on working with CSV files.

### Importing Pandas
To work with CSV files in Python, we need to import the Pandas library. Pandas provides powerful tools for data manipulation and analysis.


```python
import pandas as pd

```

### Opening a Local CSV File

To open a local CSV file, we can use the read_csv() function. We simply pass the file path as an argument.


```python
df = pd.read_csv('aug_train.csv')
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
      <th>enrollee_id</th>
      <th>city</th>
      <th>city_development_index</th>
      <th>gender</th>
      <th>relevent_experience</th>
      <th>enrolled_university</th>
      <th>education_level</th>
      <th>major_discipline</th>
      <th>experience</th>
      <th>company_size</th>
      <th>company_type</th>
      <th>last_new_job</th>
      <th>training_hours</th>
      <th>target</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>8949</td>
      <td>city_103</td>
      <td>0.920</td>
      <td>Male</td>
      <td>Has relevent experience</td>
      <td>no_enrollment</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>&gt;20</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1</td>
      <td>36</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>29725</td>
      <td>city_40</td>
      <td>0.776</td>
      <td>Male</td>
      <td>No relevent experience</td>
      <td>no_enrollment</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>15</td>
      <td>50-99</td>
      <td>Pvt Ltd</td>
      <td>&gt;4</td>
      <td>47</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>11561</td>
      <td>city_21</td>
      <td>0.624</td>
      <td>NaN</td>
      <td>No relevent experience</td>
      <td>Full time course</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>5</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>never</td>
      <td>83</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>33241</td>
      <td>city_115</td>
      <td>0.789</td>
      <td>NaN</td>
      <td>No relevent experience</td>
      <td>NaN</td>
      <td>Graduate</td>
      <td>Business Degree</td>
      <td>&lt;1</td>
      <td>NaN</td>
      <td>Pvt Ltd</td>
      <td>never</td>
      <td>52</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>666</td>
      <td>city_162</td>
      <td>0.767</td>
      <td>Male</td>
      <td>Has relevent experience</td>
      <td>no_enrollment</td>
      <td>Masters</td>
      <td>STEM</td>
      <td>&gt;20</td>
      <td>50-99</td>
      <td>Funded Startup</td>
      <td>4</td>
      <td>8</td>
      <td>0.0</td>
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
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>19153</th>
      <td>7386</td>
      <td>city_173</td>
      <td>0.878</td>
      <td>Male</td>
      <td>No relevent experience</td>
      <td>no_enrollment</td>
      <td>Graduate</td>
      <td>Humanities</td>
      <td>14</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1</td>
      <td>42</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>19154</th>
      <td>31398</td>
      <td>city_103</td>
      <td>0.920</td>
      <td>Male</td>
      <td>Has relevent experience</td>
      <td>no_enrollment</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>14</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4</td>
      <td>52</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>19155</th>
      <td>24576</td>
      <td>city_103</td>
      <td>0.920</td>
      <td>Male</td>
      <td>Has relevent experience</td>
      <td>no_enrollment</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>&gt;20</td>
      <td>50-99</td>
      <td>Pvt Ltd</td>
      <td>4</td>
      <td>44</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>19156</th>
      <td>5756</td>
      <td>city_65</td>
      <td>0.802</td>
      <td>Male</td>
      <td>Has relevent experience</td>
      <td>no_enrollment</td>
      <td>High School</td>
      <td>NaN</td>
      <td>&lt;1</td>
      <td>500-999</td>
      <td>Pvt Ltd</td>
      <td>2</td>
      <td>97</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>19157</th>
      <td>23834</td>
      <td>city_67</td>
      <td>0.855</td>
      <td>NaN</td>
      <td>No relevent experience</td>
      <td>no_enrollment</td>
      <td>Primary School</td>
      <td>NaN</td>
      <td>2</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1</td>
      <td>127</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
<p>19158 rows × 14 columns</p>
</div>



### Opening a CSV File from an URL

We can also open a CSV file directly from a URL using the read_csv() function. We pass the URL as an argument.


```python
url = 'https://raw.githubusercontent.com/cs109/2014_data/master/countries.csv'
data = pd.read_csv(url)
data
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
      <th>Region</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Algeria</td>
      <td>AFRICA</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Angola</td>
      <td>AFRICA</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Benin</td>
      <td>AFRICA</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Botswana</td>
      <td>AFRICA</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Burkina</td>
      <td>AFRICA</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>189</th>
      <td>Paraguay</td>
      <td>SOUTH AMERICA</td>
    </tr>
    <tr>
      <th>190</th>
      <td>Peru</td>
      <td>SOUTH AMERICA</td>
    </tr>
    <tr>
      <th>191</th>
      <td>Suriname</td>
      <td>SOUTH AMERICA</td>
    </tr>
    <tr>
      <th>192</th>
      <td>Uruguay</td>
      <td>SOUTH AMERICA</td>
    </tr>
    <tr>
      <th>193</th>
      <td>Venezuela</td>
      <td>SOUTH AMERICA</td>
    </tr>
  </tbody>
</table>
<p>194 rows × 2 columns</p>
</div>



### Sep Parameter
The sep parameter is used to specify the delimiter or separator used in the CSV file to separate columns. By default, the read_csv() function assumes that the separator is a comma, but if the CSV file uses a different separator or comma is missing in a CSV file we need to specify it using the 'sep' parameter.


```python
pd.read_csv('movie_titles_metadata.tsv',sep='\t')
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
      <th>m0</th>
      <th>10 things i hate about you</th>
      <th>1999</th>
      <th>6.90</th>
      <th>62847</th>
      <th>['comedy' 'romance']</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>m1</td>
      <td>1492: conquest of paradise</td>
      <td>1992</td>
      <td>6.2</td>
      <td>10421.0</td>
      <td>['adventure' 'biography' 'drama' 'history']</td>
    </tr>
    <tr>
      <th>1</th>
      <td>m2</td>
      <td>15 minutes</td>
      <td>2001</td>
      <td>6.1</td>
      <td>25854.0</td>
      <td>['action' 'crime' 'drama' 'thriller']</td>
    </tr>
    <tr>
      <th>2</th>
      <td>m3</td>
      <td>2001: a space odyssey</td>
      <td>1968</td>
      <td>8.4</td>
      <td>163227.0</td>
      <td>['adventure' 'mystery' 'sci-fi']</td>
    </tr>
    <tr>
      <th>3</th>
      <td>m4</td>
      <td>48 hrs.</td>
      <td>1982</td>
      <td>6.9</td>
      <td>22289.0</td>
      <td>['action' 'comedy' 'crime' 'drama' 'thriller']</td>
    </tr>
    <tr>
      <th>4</th>
      <td>m5</td>
      <td>the fifth element</td>
      <td>1997</td>
      <td>7.5</td>
      <td>133756.0</td>
      <td>['action' 'adventure' 'romance' 'sci-fi' 'thri...</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>611</th>
      <td>m612</td>
      <td>watchmen</td>
      <td>2009</td>
      <td>7.8</td>
      <td>135229.0</td>
      <td>['action' 'crime' 'fantasy' 'mystery' 'sci-fi'...</td>
    </tr>
    <tr>
      <th>612</th>
      <td>m613</td>
      <td>xxx</td>
      <td>2002</td>
      <td>5.6</td>
      <td>53505.0</td>
      <td>['action' 'adventure' 'crime']</td>
    </tr>
    <tr>
      <th>613</th>
      <td>m614</td>
      <td>x-men</td>
      <td>2000</td>
      <td>7.4</td>
      <td>122149.0</td>
      <td>['action' 'sci-fi']</td>
    </tr>
    <tr>
      <th>614</th>
      <td>m615</td>
      <td>young frankenstein</td>
      <td>1974</td>
      <td>8.0</td>
      <td>57618.0</td>
      <td>['comedy' 'sci-fi']</td>
    </tr>
    <tr>
      <th>615</th>
      <td>m616</td>
      <td>zulu dawn</td>
      <td>1979</td>
      <td>6.4</td>
      <td>1911.0</td>
      <td>['action' 'adventure' 'drama' 'history' 'war']</td>
    </tr>
  </tbody>
</table>
<p>616 rows × 6 columns</p>
</div>



### Names Parameter
The names parameter in the pd.read_csv() function is used to specify the names of the columns in the resulting DataFrame. 
This is useful when the CSV file does not include column names or when we want to assign custom names to the columns. By using the 'names' parameter, we can ensure that the resulting DataFrame has the appropriate column names.


```python
pd.read_csv('movie_titles_metadata.tsv',sep='\t', names= ['sno','name','release_year','rating','votes','genres'])
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
      <th>sno</th>
      <th>name</th>
      <th>release_year</th>
      <th>rating</th>
      <th>votes</th>
      <th>genres</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>m0</td>
      <td>10 things i hate about you</td>
      <td>1999</td>
      <td>6.9</td>
      <td>62847.0</td>
      <td>['comedy' 'romance']</td>
    </tr>
    <tr>
      <th>1</th>
      <td>m1</td>
      <td>1492: conquest of paradise</td>
      <td>1992</td>
      <td>6.2</td>
      <td>10421.0</td>
      <td>['adventure' 'biography' 'drama' 'history']</td>
    </tr>
    <tr>
      <th>2</th>
      <td>m2</td>
      <td>15 minutes</td>
      <td>2001</td>
      <td>6.1</td>
      <td>25854.0</td>
      <td>['action' 'crime' 'drama' 'thriller']</td>
    </tr>
    <tr>
      <th>3</th>
      <td>m3</td>
      <td>2001: a space odyssey</td>
      <td>1968</td>
      <td>8.4</td>
      <td>163227.0</td>
      <td>['adventure' 'mystery' 'sci-fi']</td>
    </tr>
    <tr>
      <th>4</th>
      <td>m4</td>
      <td>48 hrs.</td>
      <td>1982</td>
      <td>6.9</td>
      <td>22289.0</td>
      <td>['action' 'comedy' 'crime' 'drama' 'thriller']</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>612</th>
      <td>m612</td>
      <td>watchmen</td>
      <td>2009</td>
      <td>7.8</td>
      <td>135229.0</td>
      <td>['action' 'crime' 'fantasy' 'mystery' 'sci-fi'...</td>
    </tr>
    <tr>
      <th>613</th>
      <td>m613</td>
      <td>xxx</td>
      <td>2002</td>
      <td>5.6</td>
      <td>53505.0</td>
      <td>['action' 'adventure' 'crime']</td>
    </tr>
    <tr>
      <th>614</th>
      <td>m614</td>
      <td>x-men</td>
      <td>2000</td>
      <td>7.4</td>
      <td>122149.0</td>
      <td>['action' 'sci-fi']</td>
    </tr>
    <tr>
      <th>615</th>
      <td>m615</td>
      <td>young frankenstein</td>
      <td>1974</td>
      <td>8.0</td>
      <td>57618.0</td>
      <td>['comedy' 'sci-fi']</td>
    </tr>
    <tr>
      <th>616</th>
      <td>m616</td>
      <td>zulu dawn</td>
      <td>1979</td>
      <td>6.4</td>
      <td>1911.0</td>
      <td>['action' 'adventure' 'drama' 'history' 'war']</td>
    </tr>
  </tbody>
</table>
<p>617 rows × 6 columns</p>
</div>



### Header Parameter
The header parameter in the pd.read_csv() function is used to specify which row of the CSV file contains the header or column names.
For example, if the header row is the second row in the CSV file, we can use header=1 to specify that. The default value for header is 0, which assumes that the first row contains the column names.


```python
pd.read_csv('test.csv', header=1)
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
      <th>0</th>
      <th>enrollee_id</th>
      <th>city</th>
      <th>city_development_index</th>
      <th>gender</th>
      <th>relevent_experience</th>
      <th>enrolled_university</th>
      <th>education_level</th>
      <th>major_discipline</th>
      <th>experience</th>
      <th>company_size</th>
      <th>company_type</th>
      <th>last_new_job</th>
      <th>training_hours</th>
      <th>target</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>29725</td>
      <td>city_40</td>
      <td>0.776</td>
      <td>Male</td>
      <td>No relevent experience</td>
      <td>no_enrollment</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>15</td>
      <td>50-99</td>
      <td>Pvt Ltd</td>
      <td>&gt;4</td>
      <td>47</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>11561</td>
      <td>city_21</td>
      <td>0.624</td>
      <td>NaN</td>
      <td>No relevent experience</td>
      <td>Full time course</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>5</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>never</td>
      <td>83</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>33241</td>
      <td>city_115</td>
      <td>0.789</td>
      <td>NaN</td>
      <td>No relevent experience</td>
      <td>NaN</td>
      <td>Graduate</td>
      <td>Business Degree</td>
      <td>&lt;1</td>
      <td>NaN</td>
      <td>Pvt Ltd</td>
      <td>never</td>
      <td>52</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>666</td>
      <td>city_162</td>
      <td>0.767</td>
      <td>Male</td>
      <td>Has relevent experience</td>
      <td>no_enrollment</td>
      <td>Masters</td>
      <td>STEM</td>
      <td>&gt;20</td>
      <td>50-99</td>
      <td>Funded Startup</td>
      <td>4</td>
      <td>8</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>



### Index_col Parameter
We can also specify which column to use as the index using the index_col parameter.


```python
pd.read_csv('aug_train.csv',index_col='enrollee_id')
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
      <th>city</th>
      <th>city_development_index</th>
      <th>gender</th>
      <th>relevent_experience</th>
      <th>enrolled_university</th>
      <th>education_level</th>
      <th>major_discipline</th>
      <th>experience</th>
      <th>company_size</th>
      <th>company_type</th>
      <th>last_new_job</th>
      <th>training_hours</th>
      <th>target</th>
    </tr>
    <tr>
      <th>enrollee_id</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>8949</th>
      <td>city_103</td>
      <td>0.920</td>
      <td>Male</td>
      <td>Has relevent experience</td>
      <td>no_enrollment</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>&gt;20</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1</td>
      <td>36</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>29725</th>
      <td>city_40</td>
      <td>0.776</td>
      <td>Male</td>
      <td>No relevent experience</td>
      <td>no_enrollment</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>15</td>
      <td>50-99</td>
      <td>Pvt Ltd</td>
      <td>&gt;4</td>
      <td>47</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>11561</th>
      <td>city_21</td>
      <td>0.624</td>
      <td>NaN</td>
      <td>No relevent experience</td>
      <td>Full time course</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>5</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>never</td>
      <td>83</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>33241</th>
      <td>city_115</td>
      <td>0.789</td>
      <td>NaN</td>
      <td>No relevent experience</td>
      <td>NaN</td>
      <td>Graduate</td>
      <td>Business Degree</td>
      <td>&lt;1</td>
      <td>NaN</td>
      <td>Pvt Ltd</td>
      <td>never</td>
      <td>52</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>666</th>
      <td>city_162</td>
      <td>0.767</td>
      <td>Male</td>
      <td>Has relevent experience</td>
      <td>no_enrollment</td>
      <td>Masters</td>
      <td>STEM</td>
      <td>&gt;20</td>
      <td>50-99</td>
      <td>Funded Startup</td>
      <td>4</td>
      <td>8</td>
      <td>0.0</td>
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
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>7386</th>
      <td>city_173</td>
      <td>0.878</td>
      <td>Male</td>
      <td>No relevent experience</td>
      <td>no_enrollment</td>
      <td>Graduate</td>
      <td>Humanities</td>
      <td>14</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1</td>
      <td>42</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>31398</th>
      <td>city_103</td>
      <td>0.920</td>
      <td>Male</td>
      <td>Has relevent experience</td>
      <td>no_enrollment</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>14</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4</td>
      <td>52</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>24576</th>
      <td>city_103</td>
      <td>0.920</td>
      <td>Male</td>
      <td>Has relevent experience</td>
      <td>no_enrollment</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>&gt;20</td>
      <td>50-99</td>
      <td>Pvt Ltd</td>
      <td>4</td>
      <td>44</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>5756</th>
      <td>city_65</td>
      <td>0.802</td>
      <td>Male</td>
      <td>Has relevent experience</td>
      <td>no_enrollment</td>
      <td>High School</td>
      <td>NaN</td>
      <td>&lt;1</td>
      <td>500-999</td>
      <td>Pvt Ltd</td>
      <td>2</td>
      <td>97</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>23834</th>
      <td>city_67</td>
      <td>0.855</td>
      <td>NaN</td>
      <td>No relevent experience</td>
      <td>no_enrollment</td>
      <td>Primary School</td>
      <td>NaN</td>
      <td>2</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1</td>
      <td>127</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
<p>19158 rows × 13 columns</p>
</div>



### use_cols Parameter
It is used to select a subset of columns from the CSV file to load.


```python
pd.read_csv('aug_train.csv',usecols=['enrollee_id','gender','education_level'])
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
      <th>enrollee_id</th>
      <th>gender</th>
      <th>education_level</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>8949</td>
      <td>Male</td>
      <td>Graduate</td>
    </tr>
    <tr>
      <th>1</th>
      <td>29725</td>
      <td>Male</td>
      <td>Graduate</td>
    </tr>
    <tr>
      <th>2</th>
      <td>11561</td>
      <td>NaN</td>
      <td>Graduate</td>
    </tr>
    <tr>
      <th>3</th>
      <td>33241</td>
      <td>NaN</td>
      <td>Graduate</td>
    </tr>
    <tr>
      <th>4</th>
      <td>666</td>
      <td>Male</td>
      <td>Masters</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>19153</th>
      <td>7386</td>
      <td>Male</td>
      <td>Graduate</td>
    </tr>
    <tr>
      <th>19154</th>
      <td>31398</td>
      <td>Male</td>
      <td>Graduate</td>
    </tr>
    <tr>
      <th>19155</th>
      <td>24576</td>
      <td>Male</td>
      <td>Graduate</td>
    </tr>
    <tr>
      <th>19156</th>
      <td>5756</td>
      <td>Male</td>
      <td>High School</td>
    </tr>
    <tr>
      <th>19157</th>
      <td>23834</td>
      <td>NaN</td>
      <td>Primary School</td>
    </tr>
  </tbody>
</table>
<p>19158 rows × 3 columns</p>
</div>



### Skiprows/nrows Parameter
They are used to skip certain rows or load only a specified number of rows.


```python
pd.read_csv('aug_train.csv',nrows=100)
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
      <th>enrollee_id</th>
      <th>city</th>
      <th>city_development_index</th>
      <th>gender</th>
      <th>relevent_experience</th>
      <th>enrolled_university</th>
      <th>education_level</th>
      <th>major_discipline</th>
      <th>experience</th>
      <th>company_size</th>
      <th>company_type</th>
      <th>last_new_job</th>
      <th>training_hours</th>
      <th>target</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>8949</td>
      <td>city_103</td>
      <td>0.920</td>
      <td>Male</td>
      <td>Has relevent experience</td>
      <td>no_enrollment</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>&gt;20</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1</td>
      <td>36</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>29725</td>
      <td>city_40</td>
      <td>0.776</td>
      <td>Male</td>
      <td>No relevent experience</td>
      <td>no_enrollment</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>15</td>
      <td>50-99</td>
      <td>Pvt Ltd</td>
      <td>&gt;4</td>
      <td>47</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>11561</td>
      <td>city_21</td>
      <td>0.624</td>
      <td>NaN</td>
      <td>No relevent experience</td>
      <td>Full time course</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>5</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>never</td>
      <td>83</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>33241</td>
      <td>city_115</td>
      <td>0.789</td>
      <td>NaN</td>
      <td>No relevent experience</td>
      <td>NaN</td>
      <td>Graduate</td>
      <td>Business Degree</td>
      <td>&lt;1</td>
      <td>NaN</td>
      <td>Pvt Ltd</td>
      <td>never</td>
      <td>52</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>666</td>
      <td>city_162</td>
      <td>0.767</td>
      <td>Male</td>
      <td>Has relevent experience</td>
      <td>no_enrollment</td>
      <td>Masters</td>
      <td>STEM</td>
      <td>&gt;20</td>
      <td>50-99</td>
      <td>Funded Startup</td>
      <td>4</td>
      <td>8</td>
      <td>0.0</td>
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
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>95</th>
      <td>12081</td>
      <td>city_65</td>
      <td>0.802</td>
      <td>Male</td>
      <td>Has relevent experience</td>
      <td>Full time course</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>9</td>
      <td>50-99</td>
      <td>Pvt Ltd</td>
      <td>1</td>
      <td>33</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>96</th>
      <td>7364</td>
      <td>city_160</td>
      <td>0.920</td>
      <td>NaN</td>
      <td>No relevent experience</td>
      <td>Full time course</td>
      <td>High School</td>
      <td>NaN</td>
      <td>2</td>
      <td>100-500</td>
      <td>Pvt Ltd</td>
      <td>1</td>
      <td>142</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>97</th>
      <td>11184</td>
      <td>city_74</td>
      <td>0.579</td>
      <td>NaN</td>
      <td>No relevent experience</td>
      <td>Full time course</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>2</td>
      <td>100-500</td>
      <td>Pvt Ltd</td>
      <td>1</td>
      <td>34</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>98</th>
      <td>7016</td>
      <td>city_65</td>
      <td>0.802</td>
      <td>Male</td>
      <td>Has relevent experience</td>
      <td>no_enrollment</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>6</td>
      <td>50-99</td>
      <td>Pvt Ltd</td>
      <td>2</td>
      <td>14</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>99</th>
      <td>8695</td>
      <td>city_11</td>
      <td>0.550</td>
      <td>Male</td>
      <td>Has relevent experience</td>
      <td>no_enrollment</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>6</td>
      <td>10/49</td>
      <td>Pvt Ltd</td>
      <td>2</td>
      <td>27</td>
      <td>1.0</td>
    </tr>
  </tbody>
</table>
<p>100 rows × 14 columns</p>
</div>



### Squeeze parameters
The 'squeeze' parameter is used to convert a DataFrame with a single column into a pandas Series.


```python
pd.read_csv('aug_train.csv',usecols=['gender'], squeeze=True)
```

    
      pd.read_csv('aug_train.csv',usecols=['gender'], squeeze=True)





    0        Male
    1        Male
    2         NaN
    3         NaN
    4        Male
             ... 
    19153    Male
    19154    Male
    19155    Male
    19156    Male
    19157     NaN
    Name: gender, Length: 19158, dtype: object



### Encoding Parameter
The 'encoding' parameter is used to specify the character encoding used in the CSV file. By default, encoding='utf-8'. If the CSV file uses a different encoding, we need to specify it using the 'encoding' parameter.


```python
pd.read_csv('zomato.csv',encoding='latin-1')
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
      <th>Restaurant ID</th>
      <th>Restaurant Name</th>
      <th>Country Code</th>
      <th>City</th>
      <th>Address</th>
      <th>Locality</th>
      <th>Locality Verbose</th>
      <th>Longitude</th>
      <th>Latitude</th>
      <th>Cuisines</th>
      <th>...</th>
      <th>Currency</th>
      <th>Has Table booking</th>
      <th>Has Online delivery</th>
      <th>Is delivering now</th>
      <th>Switch to order menu</th>
      <th>Price range</th>
      <th>Aggregate rating</th>
      <th>Rating color</th>
      <th>Rating text</th>
      <th>Votes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>6317637</td>
      <td>Le Petit Souffle</td>
      <td>162</td>
      <td>Makati City</td>
      <td>Third Floor, Century City Mall, Kalayaan Avenu...</td>
      <td>Century City Mall, Poblacion, Makati City</td>
      <td>Century City Mall, Poblacion, Makati City, Mak...</td>
      <td>121.027535</td>
      <td>14.565443</td>
      <td>French, Japanese, Desserts</td>
      <td>...</td>
      <td>Botswana Pula(P)</td>
      <td>Yes</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
      <td>3</td>
      <td>4.8</td>
      <td>Dark Green</td>
      <td>Excellent</td>
      <td>314</td>
    </tr>
    <tr>
      <th>1</th>
      <td>6304287</td>
      <td>Izakaya Kikufuji</td>
      <td>162</td>
      <td>Makati City</td>
      <td>Little Tokyo, 2277 Chino Roces Avenue, Legaspi...</td>
      <td>Little Tokyo, Legaspi Village, Makati City</td>
      <td>Little Tokyo, Legaspi Village, Makati City, Ma...</td>
      <td>121.014101</td>
      <td>14.553708</td>
      <td>Japanese</td>
      <td>...</td>
      <td>Botswana Pula(P)</td>
      <td>Yes</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
      <td>3</td>
      <td>4.5</td>
      <td>Dark Green</td>
      <td>Excellent</td>
      <td>591</td>
    </tr>
    <tr>
      <th>2</th>
      <td>6300002</td>
      <td>Heat - Edsa Shangri-La</td>
      <td>162</td>
      <td>Mandaluyong City</td>
      <td>Edsa Shangri-La, 1 Garden Way, Ortigas, Mandal...</td>
      <td>Edsa Shangri-La, Ortigas, Mandaluyong City</td>
      <td>Edsa Shangri-La, Ortigas, Mandaluyong City, Ma...</td>
      <td>121.056831</td>
      <td>14.581404</td>
      <td>Seafood, Asian, Filipino, Indian</td>
      <td>...</td>
      <td>Botswana Pula(P)</td>
      <td>Yes</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
      <td>4</td>
      <td>4.4</td>
      <td>Green</td>
      <td>Very Good</td>
      <td>270</td>
    </tr>
    <tr>
      <th>3</th>
      <td>6318506</td>
      <td>Ooma</td>
      <td>162</td>
      <td>Mandaluyong City</td>
      <td>Third Floor, Mega Fashion Hall, SM Megamall, O...</td>
      <td>SM Megamall, Ortigas, Mandaluyong City</td>
      <td>SM Megamall, Ortigas, Mandaluyong City, Mandal...</td>
      <td>121.056475</td>
      <td>14.585318</td>
      <td>Japanese, Sushi</td>
      <td>...</td>
      <td>Botswana Pula(P)</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
      <td>4</td>
      <td>4.9</td>
      <td>Dark Green</td>
      <td>Excellent</td>
      <td>365</td>
    </tr>
    <tr>
      <th>4</th>
      <td>6314302</td>
      <td>Sambo Kojin</td>
      <td>162</td>
      <td>Mandaluyong City</td>
      <td>Third Floor, Mega Atrium, SM Megamall, Ortigas...</td>
      <td>SM Megamall, Ortigas, Mandaluyong City</td>
      <td>SM Megamall, Ortigas, Mandaluyong City, Mandal...</td>
      <td>121.057508</td>
      <td>14.584450</td>
      <td>Japanese, Korean</td>
      <td>...</td>
      <td>Botswana Pula(P)</td>
      <td>Yes</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
      <td>4</td>
      <td>4.8</td>
      <td>Dark Green</td>
      <td>Excellent</td>
      <td>229</td>
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
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
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
      <th>9546</th>
      <td>5915730</td>
      <td>NamlÛ± Gurme</td>
      <td>208</td>
      <td>ÛÁstanbul</td>
      <td>Kemankeô Karamustafa Paôa Mahallesi, RÛ±htÛ±...</td>
      <td>Karakí_y</td>
      <td>Karakí_y, ÛÁstanbul</td>
      <td>28.977392</td>
      <td>41.022793</td>
      <td>Turkish</td>
      <td>...</td>
      <td>Turkish Lira(TL)</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
      <td>3</td>
      <td>4.1</td>
      <td>Green</td>
      <td>Very Good</td>
      <td>788</td>
    </tr>
    <tr>
      <th>9547</th>
      <td>5908749</td>
      <td>Ceviz AÛôacÛ±</td>
      <td>208</td>
      <td>ÛÁstanbul</td>
      <td>Koôuyolu Mahallesi, Muhittin íìstí_ndaÛô Cadd...</td>
      <td>Koôuyolu</td>
      <td>Koôuyolu, ÛÁstanbul</td>
      <td>29.041297</td>
      <td>41.009847</td>
      <td>World Cuisine, Patisserie, Cafe</td>
      <td>...</td>
      <td>Turkish Lira(TL)</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
      <td>3</td>
      <td>4.2</td>
      <td>Green</td>
      <td>Very Good</td>
      <td>1034</td>
    </tr>
    <tr>
      <th>9548</th>
      <td>5915807</td>
      <td>Huqqa</td>
      <td>208</td>
      <td>ÛÁstanbul</td>
      <td>Kuruí_eôme Mahallesi, Muallim Naci Caddesi, N...</td>
      <td>Kuruí_eôme</td>
      <td>Kuruí_eôme, ÛÁstanbul</td>
      <td>29.034640</td>
      <td>41.055817</td>
      <td>Italian, World Cuisine</td>
      <td>...</td>
      <td>Turkish Lira(TL)</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
      <td>4</td>
      <td>3.7</td>
      <td>Yellow</td>
      <td>Good</td>
      <td>661</td>
    </tr>
    <tr>
      <th>9549</th>
      <td>5916112</td>
      <td>Aôôk Kahve</td>
      <td>208</td>
      <td>ÛÁstanbul</td>
      <td>Kuruí_eôme Mahallesi, Muallim Naci Caddesi, N...</td>
      <td>Kuruí_eôme</td>
      <td>Kuruí_eôme, ÛÁstanbul</td>
      <td>29.036019</td>
      <td>41.057979</td>
      <td>Restaurant Cafe</td>
      <td>...</td>
      <td>Turkish Lira(TL)</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
      <td>4</td>
      <td>4.0</td>
      <td>Green</td>
      <td>Very Good</td>
      <td>901</td>
    </tr>
    <tr>
      <th>9550</th>
      <td>5927402</td>
      <td>Walter's Coffee Roastery</td>
      <td>208</td>
      <td>ÛÁstanbul</td>
      <td>CafeaÛôa Mahallesi, BademaltÛ± Sokak, No 21/B,...</td>
      <td>Moda</td>
      <td>Moda, ÛÁstanbul</td>
      <td>29.026016</td>
      <td>40.984776</td>
      <td>Cafe</td>
      <td>...</td>
      <td>Turkish Lira(TL)</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
      <td>2</td>
      <td>4.0</td>
      <td>Green</td>
      <td>Very Good</td>
      <td>591</td>
    </tr>
  </tbody>
</table>
<p>9551 rows × 21 columns</p>
</div>



### Convertors

Converters in pandas are used to transform data values during data reading or writing. They can be used to convert data types, perform custom transformations, or handle missing data.


```python
def rename(name):
    if name == "Royal Challengers Bangalore":
        return "RCB"
    else:
        return name
rename("Royal Challengers Bangalore")
pd.read_csv('IPL Matches 2008-2020.csv',converters={'team1':rename})
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
      <th>id</th>
      <th>city</th>
      <th>date</th>
      <th>player_of_match</th>
      <th>venue</th>
      <th>neutral_venue</th>
      <th>team1</th>
      <th>team2</th>
      <th>toss_winner</th>
      <th>toss_decision</th>
      <th>winner</th>
      <th>result</th>
      <th>result_margin</th>
      <th>eliminator</th>
      <th>method</th>
      <th>umpire1</th>
      <th>umpire2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>335982</td>
      <td>Bangalore</td>
      <td>2008-04-18</td>
      <td>BB McCullum</td>
      <td>M Chinnaswamy Stadium</td>
      <td>0</td>
      <td>RCB</td>
      <td>Kolkata Knight Riders</td>
      <td>Royal Challengers Bangalore</td>
      <td>field</td>
      <td>Kolkata Knight Riders</td>
      <td>runs</td>
      <td>140.0</td>
      <td>N</td>
      <td>NaN</td>
      <td>Asad Rauf</td>
      <td>RE Koertzen</td>
    </tr>
    <tr>
      <th>1</th>
      <td>335983</td>
      <td>Chandigarh</td>
      <td>2008-04-19</td>
      <td>MEK Hussey</td>
      <td>Punjab Cricket Association Stadium, Mohali</td>
      <td>0</td>
      <td>Kings XI Punjab</td>
      <td>Chennai Super Kings</td>
      <td>Chennai Super Kings</td>
      <td>bat</td>
      <td>Chennai Super Kings</td>
      <td>runs</td>
      <td>33.0</td>
      <td>N</td>
      <td>NaN</td>
      <td>MR Benson</td>
      <td>SL Shastri</td>
    </tr>
    <tr>
      <th>2</th>
      <td>335984</td>
      <td>Delhi</td>
      <td>2008-04-19</td>
      <td>MF Maharoof</td>
      <td>Feroz Shah Kotla</td>
      <td>0</td>
      <td>Delhi Daredevils</td>
      <td>Rajasthan Royals</td>
      <td>Rajasthan Royals</td>
      <td>bat</td>
      <td>Delhi Daredevils</td>
      <td>wickets</td>
      <td>9.0</td>
      <td>N</td>
      <td>NaN</td>
      <td>Aleem Dar</td>
      <td>GA Pratapkumar</td>
    </tr>
    <tr>
      <th>3</th>
      <td>335985</td>
      <td>Mumbai</td>
      <td>2008-04-20</td>
      <td>MV Boucher</td>
      <td>Wankhede Stadium</td>
      <td>0</td>
      <td>Mumbai Indians</td>
      <td>Royal Challengers Bangalore</td>
      <td>Mumbai Indians</td>
      <td>bat</td>
      <td>Royal Challengers Bangalore</td>
      <td>wickets</td>
      <td>5.0</td>
      <td>N</td>
      <td>NaN</td>
      <td>SJ Davis</td>
      <td>DJ Harper</td>
    </tr>
    <tr>
      <th>4</th>
      <td>335986</td>
      <td>Kolkata</td>
      <td>2008-04-20</td>
      <td>DJ Hussey</td>
      <td>Eden Gardens</td>
      <td>0</td>
      <td>Kolkata Knight Riders</td>
      <td>Deccan Chargers</td>
      <td>Deccan Chargers</td>
      <td>bat</td>
      <td>Kolkata Knight Riders</td>
      <td>wickets</td>
      <td>5.0</td>
      <td>N</td>
      <td>NaN</td>
      <td>BF Bowden</td>
      <td>K Hariharan</td>
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
      <td>...</td>
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
      <th>811</th>
      <td>1216547</td>
      <td>Dubai</td>
      <td>2020-09-28</td>
      <td>AB de Villiers</td>
      <td>Dubai International Cricket Stadium</td>
      <td>0</td>
      <td>RCB</td>
      <td>Mumbai Indians</td>
      <td>Mumbai Indians</td>
      <td>field</td>
      <td>Royal Challengers Bangalore</td>
      <td>tie</td>
      <td>NaN</td>
      <td>Y</td>
      <td>NaN</td>
      <td>Nitin Menon</td>
      <td>PR Reiffel</td>
    </tr>
    <tr>
      <th>812</th>
      <td>1237177</td>
      <td>Dubai</td>
      <td>2020-11-05</td>
      <td>JJ Bumrah</td>
      <td>Dubai International Cricket Stadium</td>
      <td>0</td>
      <td>Mumbai Indians</td>
      <td>Delhi Capitals</td>
      <td>Delhi Capitals</td>
      <td>field</td>
      <td>Mumbai Indians</td>
      <td>runs</td>
      <td>57.0</td>
      <td>N</td>
      <td>NaN</td>
      <td>CB Gaffaney</td>
      <td>Nitin Menon</td>
    </tr>
    <tr>
      <th>813</th>
      <td>1237178</td>
      <td>Abu Dhabi</td>
      <td>2020-11-06</td>
      <td>KS Williamson</td>
      <td>Sheikh Zayed Stadium</td>
      <td>0</td>
      <td>RCB</td>
      <td>Sunrisers Hyderabad</td>
      <td>Sunrisers Hyderabad</td>
      <td>field</td>
      <td>Sunrisers Hyderabad</td>
      <td>wickets</td>
      <td>6.0</td>
      <td>N</td>
      <td>NaN</td>
      <td>PR Reiffel</td>
      <td>S Ravi</td>
    </tr>
    <tr>
      <th>814</th>
      <td>1237180</td>
      <td>Abu Dhabi</td>
      <td>2020-11-08</td>
      <td>MP Stoinis</td>
      <td>Sheikh Zayed Stadium</td>
      <td>0</td>
      <td>Delhi Capitals</td>
      <td>Sunrisers Hyderabad</td>
      <td>Delhi Capitals</td>
      <td>bat</td>
      <td>Delhi Capitals</td>
      <td>runs</td>
      <td>17.0</td>
      <td>N</td>
      <td>NaN</td>
      <td>PR Reiffel</td>
      <td>S Ravi</td>
    </tr>
    <tr>
      <th>815</th>
      <td>1237181</td>
      <td>Dubai</td>
      <td>2020-11-10</td>
      <td>TA Boult</td>
      <td>Dubai International Cricket Stadium</td>
      <td>0</td>
      <td>Delhi Capitals</td>
      <td>Mumbai Indians</td>
      <td>Delhi Capitals</td>
      <td>bat</td>
      <td>Mumbai Indians</td>
      <td>wickets</td>
      <td>5.0</td>
      <td>N</td>
      <td>NaN</td>
      <td>CB Gaffaney</td>
      <td>Nitin Menon</td>
    </tr>
  </tbody>
</table>
<p>816 rows × 17 columns</p>
</div>




```python
pd.read_csv('aug_train.csv')
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
      <th>enrollee_id</th>
      <th>city</th>
      <th>city_development_index</th>
      <th>gender</th>
      <th>relevent_experience</th>
      <th>enrolled_university</th>
      <th>education_level</th>
      <th>major_discipline</th>
      <th>experience</th>
      <th>company_size</th>
      <th>company_type</th>
      <th>last_new_job</th>
      <th>training_hours</th>
      <th>target</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>8949</td>
      <td>city_103</td>
      <td>0.920</td>
      <td>Male</td>
      <td>Has relevent experience</td>
      <td>no_enrollment</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>&gt;20</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1</td>
      <td>36</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>29725</td>
      <td>city_40</td>
      <td>0.776</td>
      <td>Male</td>
      <td>No relevent experience</td>
      <td>no_enrollment</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>15</td>
      <td>50-99</td>
      <td>Pvt Ltd</td>
      <td>&gt;4</td>
      <td>47</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>11561</td>
      <td>city_21</td>
      <td>0.624</td>
      <td>NaN</td>
      <td>No relevent experience</td>
      <td>Full time course</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>5</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>never</td>
      <td>83</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>33241</td>
      <td>city_115</td>
      <td>0.789</td>
      <td>NaN</td>
      <td>No relevent experience</td>
      <td>NaN</td>
      <td>Graduate</td>
      <td>Business Degree</td>
      <td>&lt;1</td>
      <td>NaN</td>
      <td>Pvt Ltd</td>
      <td>never</td>
      <td>52</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>666</td>
      <td>city_162</td>
      <td>0.767</td>
      <td>Male</td>
      <td>Has relevent experience</td>
      <td>no_enrollment</td>
      <td>Masters</td>
      <td>STEM</td>
      <td>&gt;20</td>
      <td>50-99</td>
      <td>Funded Startup</td>
      <td>4</td>
      <td>8</td>
      <td>0.0</td>
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
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>19153</th>
      <td>7386</td>
      <td>city_173</td>
      <td>0.878</td>
      <td>Male</td>
      <td>No relevent experience</td>
      <td>no_enrollment</td>
      <td>Graduate</td>
      <td>Humanities</td>
      <td>14</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1</td>
      <td>42</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>19154</th>
      <td>31398</td>
      <td>city_103</td>
      <td>0.920</td>
      <td>Male</td>
      <td>Has relevent experience</td>
      <td>no_enrollment</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>14</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4</td>
      <td>52</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>19155</th>
      <td>24576</td>
      <td>city_103</td>
      <td>0.920</td>
      <td>Male</td>
      <td>Has relevent experience</td>
      <td>no_enrollment</td>
      <td>Graduate</td>
      <td>STEM</td>
      <td>&gt;20</td>
      <td>50-99</td>
      <td>Pvt Ltd</td>
      <td>4</td>
      <td>44</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>19156</th>
      <td>5756</td>
      <td>city_65</td>
      <td>0.802</td>
      <td>Male</td>
      <td>Has relevent experience</td>
      <td>no_enrollment</td>
      <td>High School</td>
      <td>NaN</td>
      <td>&lt;1</td>
      <td>500-999</td>
      <td>Pvt Ltd</td>
      <td>2</td>
      <td>97</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>19157</th>
      <td>23834</td>
      <td>city_67</td>
      <td>0.855</td>
      <td>NaN</td>
      <td>No relevent experience</td>
      <td>no_enrollment</td>
      <td>Primary School</td>
      <td>NaN</td>
      <td>2</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1</td>
      <td>127</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
<p>19158 rows × 14 columns</p>
</div>



### For more details and advanced usage of working with CSV files in pandas, refer to the https://pandas.pydata.org/docs/reference/api/pandas.read_csv.html


```python

```
