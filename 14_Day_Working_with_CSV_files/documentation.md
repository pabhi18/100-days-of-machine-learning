# 1. Importing pandas


```python
import pandas as pd
```

# 2. Opening a local csv file


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



# 3. Opening a csv file from an URL


```python
import requests
from io import StringIO

url = "https://raw.githubusercontent.com/cs109/2014_data/master/countries.csv"
headers = {"User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.14; rv:66.0) Gecko/20100101 Firefox/66.0"}
req = requests.get(url, headers=headers)
data = StringIO(req.text)

pd.read_csv(data)
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



# 4. Sep Parameter


```python
pd.read_csv('movie_titles_metadata.tsv',sep='\t',names=['sno','name','release_year','rating','votes','genres'])
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



# 5. Index_col parameter


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



# 6. Header parameter


```python
pd.read_csv('test.csv',header=1)
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



# 7. use_cols parameter


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



# 8. Squeeze parameters


```python
pd.read_csv('aug_train.csv',usecols=['gender'],squeeze=True)
```




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



# 9. Skiprows/nrows Parameter


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



# 10. Encoding parameter


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



# 11. Skip bad lines


```python
pd.read_csv('BX-Books.csv', sep=';', encoding="latin-1",error_bad_lines=False)
```

    b'Skipping line 6452: expected 8 fields, saw 9\nSkipping line 43667: expected 8 fields, saw 10\nSkipping line 51751: expected 8 fields, saw 9\n'
    b'Skipping line 92038: expected 8 fields, saw 9\nSkipping line 104319: expected 8 fields, saw 9\nSkipping line 121768: expected 8 fields, saw 9\n'
    b'Skipping line 144058: expected 8 fields, saw 9\nSkipping line 150789: expected 8 fields, saw 9\nSkipping line 157128: expected 8 fields, saw 9\nSkipping line 180189: expected 8 fields, saw 9\nSkipping line 185738: expected 8 fields, saw 9\n'
    b'Skipping line 209388: expected 8 fields, saw 9\nSkipping line 220626: expected 8 fields, saw 9\nSkipping line 227933: expected 8 fields, saw 11\nSkipping line 228957: expected 8 fields, saw 10\nSkipping line 245933: expected 8 fields, saw 9\nSkipping line 251296: expected 8 fields, saw 9\nSkipping line 259941: expected 8 fields, saw 9\nSkipping line 261529: expected 8 fields, saw 9\n'





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
      <th>ISBN</th>
      <th>Book-Title</th>
      <th>Book-Author</th>
      <th>Year-Of-Publication</th>
      <th>Publisher</th>
      <th>Image-URL-S</th>
      <th>Image-URL-M</th>
      <th>Image-URL-L</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0195153448</td>
      <td>Classical Mythology</td>
      <td>Mark P. O. Morford</td>
      <td>2002</td>
      <td>Oxford University Press</td>
      <td>http://images.amazon.com/images/P/0195153448.0...</td>
      <td>http://images.amazon.com/images/P/0195153448.0...</td>
      <td>http://images.amazon.com/images/P/0195153448.0...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0002005018</td>
      <td>Clara Callan</td>
      <td>Richard Bruce Wright</td>
      <td>2001</td>
      <td>HarperFlamingo Canada</td>
      <td>http://images.amazon.com/images/P/0002005018.0...</td>
      <td>http://images.amazon.com/images/P/0002005018.0...</td>
      <td>http://images.amazon.com/images/P/0002005018.0...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0060973129</td>
      <td>Decision in Normandy</td>
      <td>Carlo D'Este</td>
      <td>1991</td>
      <td>HarperPerennial</td>
      <td>http://images.amazon.com/images/P/0060973129.0...</td>
      <td>http://images.amazon.com/images/P/0060973129.0...</td>
      <td>http://images.amazon.com/images/P/0060973129.0...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0374157065</td>
      <td>Flu: The Story of the Great Influenza Pandemic...</td>
      <td>Gina Bari Kolata</td>
      <td>1999</td>
      <td>Farrar Straus Giroux</td>
      <td>http://images.amazon.com/images/P/0374157065.0...</td>
      <td>http://images.amazon.com/images/P/0374157065.0...</td>
      <td>http://images.amazon.com/images/P/0374157065.0...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0393045218</td>
      <td>The Mummies of Urumchi</td>
      <td>E. J. W. Barber</td>
      <td>1999</td>
      <td>W. W. Norton &amp;amp; Company</td>
      <td>http://images.amazon.com/images/P/0393045218.0...</td>
      <td>http://images.amazon.com/images/P/0393045218.0...</td>
      <td>http://images.amazon.com/images/P/0393045218.0...</td>
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
      <th>271355</th>
      <td>0440400988</td>
      <td>There's a Bat in Bunk Five</td>
      <td>Paula Danziger</td>
      <td>1988</td>
      <td>Random House Childrens Pub (Mm)</td>
      <td>http://images.amazon.com/images/P/0440400988.0...</td>
      <td>http://images.amazon.com/images/P/0440400988.0...</td>
      <td>http://images.amazon.com/images/P/0440400988.0...</td>
    </tr>
    <tr>
      <th>271356</th>
      <td>0525447644</td>
      <td>From One to One Hundred</td>
      <td>Teri Sloat</td>
      <td>1991</td>
      <td>Dutton Books</td>
      <td>http://images.amazon.com/images/P/0525447644.0...</td>
      <td>http://images.amazon.com/images/P/0525447644.0...</td>
      <td>http://images.amazon.com/images/P/0525447644.0...</td>
    </tr>
    <tr>
      <th>271357</th>
      <td>006008667X</td>
      <td>Lily Dale : The True Story of the Town that Ta...</td>
      <td>Christine Wicker</td>
      <td>2004</td>
      <td>HarperSanFrancisco</td>
      <td>http://images.amazon.com/images/P/006008667X.0...</td>
      <td>http://images.amazon.com/images/P/006008667X.0...</td>
      <td>http://images.amazon.com/images/P/006008667X.0...</td>
    </tr>
    <tr>
      <th>271358</th>
      <td>0192126040</td>
      <td>Republic (World's Classics)</td>
      <td>Plato</td>
      <td>1996</td>
      <td>Oxford University Press</td>
      <td>http://images.amazon.com/images/P/0192126040.0...</td>
      <td>http://images.amazon.com/images/P/0192126040.0...</td>
      <td>http://images.amazon.com/images/P/0192126040.0...</td>
    </tr>
    <tr>
      <th>271359</th>
      <td>0767409752</td>
      <td>A Guided Tour of Rene Descartes' Meditations o...</td>
      <td>Christopher  Biffle</td>
      <td>2000</td>
      <td>McGraw-Hill Humanities/Social Sciences/Languages</td>
      <td>http://images.amazon.com/images/P/0767409752.0...</td>
      <td>http://images.amazon.com/images/P/0767409752.0...</td>
      <td>http://images.amazon.com/images/P/0767409752.0...</td>
    </tr>
  </tbody>
</table>
<p>271360 rows × 8 columns</p>
</div>



# 12. dtypes parameter


```python
pd.read_csv('aug_train.csv',dtype={'target':int}).info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 19158 entries, 0 to 19157
    Data columns (total 14 columns):
     #   Column                  Non-Null Count  Dtype  
    ---  ------                  --------------  -----  
     0   enrollee_id             19158 non-null  int64  
     1   city                    19158 non-null  object 
     2   city_development_index  19158 non-null  float64
     3   gender                  14650 non-null  object 
     4   relevent_experience     19158 non-null  object 
     5   enrolled_university     18772 non-null  object 
     6   education_level         18698 non-null  object 
     7   major_discipline        16345 non-null  object 
     8   experience              19093 non-null  object 
     9   company_size            13220 non-null  object 
     10  company_type            13018 non-null  object 
     11  last_new_job            18735 non-null  object 
     12  training_hours          19158 non-null  int64  
     13  target                  19158 non-null  int32  
    dtypes: float64(1), int32(1), int64(2), object(10)
    memory usage: 2.0+ MB


# 13. Handling Dates


```python
pd.read_csv('IPL Matches 2008-2020.csv',parse_dates=['date']).info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 816 entries, 0 to 815
    Data columns (total 17 columns):
     #   Column           Non-Null Count  Dtype         
    ---  ------           --------------  -----         
     0   id               816 non-null    int64         
     1   city             803 non-null    object        
     2   date             816 non-null    datetime64[ns]
     3   player_of_match  812 non-null    object        
     4   venue            816 non-null    object        
     5   neutral_venue    816 non-null    int64         
     6   team1            816 non-null    object        
     7   team2            816 non-null    object        
     8   toss_winner      816 non-null    object        
     9   toss_decision    816 non-null    object        
     10  winner           812 non-null    object        
     11  result           812 non-null    object        
     12  result_margin    799 non-null    float64       
     13  eliminator       812 non-null    object        
     14  method           19 non-null     object        
     15  umpire1          816 non-null    object        
     16  umpire2          816 non-null    object        
    dtypes: datetime64[ns](1), float64(1), int64(2), object(13)
    memory usage: 108.5+ KB



```python
def rename(name):
    if name == "Royal Challengers Bangalore":
        return "RCB"
    else:
        return name
```


```python
rename("Royal Challengers Bangalore")
```




    'RCB'



# 14. Convertors


```python
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



# 15. na_values parameter


```python
pd.read_csv('aug_train.csv',na_values=['Male',])
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



# 16. Loading a huge dataset in chunks


```python
dfs = pd.read_csv('aug_train.csv',chunksize=5000)
```


```python
for chunks in dfs:
    print(chunk.shape)
```

    (4158, 14)
    (4158, 14)
    (4158, 14)
    (4158, 14)



```python

```
