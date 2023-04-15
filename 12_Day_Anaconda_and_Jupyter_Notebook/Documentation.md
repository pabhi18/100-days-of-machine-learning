# Day 12: Anaconda and Jupyter Notebook

In today's session, we will cover the basics of Anaconda, Jupyter Notebook and downloading data from Kaggle.


## Anaconda
Anaconda is an open-source distribution of Python that is used for data science and machine learning tasks. It comes with pre-installed popular data science packages and makes it easy to manage packages and environments.

### To download Anaconda, follow these steps:
• Go to the Anaconda website: https://www.anaconda.com/products/individual <br>
• Select the appropriate version for your operating system (Windows, Mac, or Linux) <br>
• Download the installer and run it <br>
• Follow the installation instructions <br>
• Once installed, you can launch Anaconda Navigator and start using Jupyter Notebook.


## Jupyter Notebook
Jupyter Notebook is an open-source web application that allows you to create and share documents that contain live code, equations, visualizations, and narrative text. It is a powerful tool for data analysis and machine learning tasks.

### To start Jupyter Notebook, follow these steps:
• Launch Anaconda Navigator  <br>
• Click on the Jupyter Notebook icon  <br>
• Jupyter Notebook will open in your default web browser <br>
• Downloading data from Kaggle 

### Kaggle is a popular platform for data science competitions and provides a large number of datasets for practice. Follow these steps to download data from Kaggle:

• Go to the Kaggle website: https://www.kaggle.com/ <br>
• Create an account (if you don't have one already) <br>
• Search for the dataset you want to download <br>
• Click on the dataset and select "Download" <br>
• Once the data is downloaded, you can upload it to Jupyter Notebook for analysis. <br>
• Uploading data to Jupyter Notebook 

### To upload data to Jupyter Notebook, follow these steps:

• Launch Jupyter Notebook <br>
• Navigate to the folder where you want to upload the data <br>
• Click on the "Upload" button in the top right corner <br>
• Select the file you want to upload and click "Open" <br>
• Once the file is uploaded, you can start analyzing the data in Jupyter Notebook.


## Introduction to Jupyter Notebook

```python
print("Hello World")
```

    Hello World


### Import Dataset

Over here I will import the Dataset


```python
import pandas as pd
```


```python
df = pd.read_csv('Student Mental health.csv')
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
      <th>Timestamp</th>
      <th>Choose your gender</th>
      <th>Age</th>
      <th>What is your course?</th>
      <th>Your current year of Study</th>
      <th>What is your CGPA?</th>
      <th>Marital status</th>
      <th>Do you have Depression?</th>
      <th>Do you have Anxiety?</th>
      <th>Do you have Panic attack?</th>
      <th>Did you seek any specialist for a treatment?</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>8/7/2020 12:02</td>
      <td>Female</td>
      <td>18.0</td>
      <td>Engineering</td>
      <td>year 1</td>
      <td>3.00 - 3.49</td>
      <td>No</td>
      <td>Yes</td>
      <td>No</td>
      <td>Yes</td>
      <td>No</td>
    </tr>
    <tr>
      <th>1</th>
      <td>8/7/2020 12:04</td>
      <td>Male</td>
      <td>21.0</td>
      <td>Islamic education</td>
      <td>year 2</td>
      <td>3.00 - 3.49</td>
      <td>No</td>
      <td>No</td>
      <td>Yes</td>
      <td>No</td>
      <td>No</td>
    </tr>
    <tr>
      <th>2</th>
      <td>8/7/2020 12:05</td>
      <td>Male</td>
      <td>19.0</td>
      <td>BIT</td>
      <td>Year 1</td>
      <td>3.00 - 3.49</td>
      <td>No</td>
      <td>Yes</td>
      <td>Yes</td>
      <td>Yes</td>
      <td>No</td>
    </tr>
    <tr>
      <th>3</th>
      <td>8/7/2020 12:06</td>
      <td>Female</td>
      <td>22.0</td>
      <td>Laws</td>
      <td>year 3</td>
      <td>3.00 - 3.49</td>
      <td>Yes</td>
      <td>Yes</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
    </tr>
    <tr>
      <th>4</th>
      <td>8/7/2020 12:13</td>
      <td>Male</td>
      <td>23.0</td>
      <td>Mathemathics</td>
      <td>year 4</td>
      <td>3.00 - 3.49</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
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
    </tr>
    <tr>
      <th>96</th>
      <td>13/07/2020 19:56:49</td>
      <td>Female</td>
      <td>21.0</td>
      <td>BCS</td>
      <td>year 1</td>
      <td>3.50 - 4.00</td>
      <td>No</td>
      <td>No</td>
      <td>Yes</td>
      <td>No</td>
      <td>No</td>
    </tr>
    <tr>
      <th>97</th>
      <td>13/07/2020 21:21:42</td>
      <td>Male</td>
      <td>18.0</td>
      <td>Engineering</td>
      <td>Year 2</td>
      <td>3.00 - 3.49</td>
      <td>No</td>
      <td>Yes</td>
      <td>Yes</td>
      <td>No</td>
      <td>No</td>
    </tr>
    <tr>
      <th>98</th>
      <td>13/07/2020 21:22:56</td>
      <td>Female</td>
      <td>19.0</td>
      <td>Nursing</td>
      <td>Year 3</td>
      <td>3.50 - 4.00</td>
      <td>Yes</td>
      <td>Yes</td>
      <td>No</td>
      <td>Yes</td>
      <td>No</td>
    </tr>
    <tr>
      <th>99</th>
      <td>13/07/2020 21:23:57</td>
      <td>Female</td>
      <td>23.0</td>
      <td>Pendidikan Islam</td>
      <td>year 4</td>
      <td>3.50 - 4.00</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
    </tr>
    <tr>
      <th>100</th>
      <td>18/07/2020 20:16:21</td>
      <td>Male</td>
      <td>20.0</td>
      <td>Biomedical science</td>
      <td>Year 2</td>
      <td>3.00 - 3.49</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
      <td>No</td>
    </tr>
  </tbody>
</table>
<p>101 rows × 11 columns</p>
</div>




```python

```
