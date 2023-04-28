# Pandas Profiling

Pandas Profiling

Pandas Profiling is an open source Python library that allows users to quickly generate reports with exploratory data analysis on datasets. It provides a comprehensive overview of the data, including statistics about the variables, missing values, and correlations between variables. The library is particularly useful when working with large datasets, as it automates much of the exploratory data analysis process and can help identify potential issues or trends in the data.

## Installation

Pandas Profiling can be installed using pip, a package installer for Python. To install, simply run the following command:


```python
!pip install pandas-profiling
```

    Collecting pandas-profiling
      Downloading pandas_profiling-3.6.6-py2.py3-none-any.whl (324 kB)
    [2K     [90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m324.4/324.4 kB[0m [31m3.0 MB/s[0m eta [36m0:00:00[0m00:01[0m00:01[0m
    [?25hCollecting ydata-profiling
      Downloading ydata_profiling-4.1.2-py2.py3-none-any.whl (345 kB)
    [2K     [90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m345.9/345.9 kB[0m [31m3.9 MB/s[0m eta [36m0:00:00[0m00:01[0m00:01[0m
    [?25hRequirement already satisfied: requests<2.29,>=2.24.0 in /Library/anaconda3/lib/python3.10/site-packages (from ydata-profiling->pandas-profiling) (2.28.1)
    Requirement already satisfied: tqdm<4.65,>=4.48.2 in /Library/anaconda3/lib/python3.10/site-packages (from ydata-profiling->pandas-profiling) (4.64.1)
    Collecting htmlmin==0.1.12
      Downloading htmlmin-0.1.12.tar.gz (19 kB)
      Preparing metadata (setup.py) ... [?25ldone
    [?25hRequirement already satisfied: jinja2<3.2,>=2.11.1 in /Library/anaconda3/lib/python3.10/site-packages (from ydata-profiling->pandas-profiling) (3.1.2)
    Collecting visions[type_image_path]==0.7.5
      Downloading visions-0.7.5-py3-none-any.whl (102 kB)
    [2K     [90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m102.7/102.7 kB[0m [31m4.9 MB/s[0m eta [36m0:00:00[0m
    [?25hRequirement already satisfied: numpy<1.24,>=1.16.0 in /Library/anaconda3/lib/python3.10/site-packages (from ydata-profiling->pandas-profiling) (1.23.5)
    Collecting typeguard<2.14,>=2.13.2
      Downloading typeguard-2.13.3-py3-none-any.whl (17 kB)
    Requirement already satisfied: seaborn<0.13,>=0.10.1 in /Library/anaconda3/lib/python3.10/site-packages (from ydata-profiling->pandas-profiling) (0.12.2)
    Collecting pydantic<1.11,>=1.8.1
      Downloading pydantic-1.10.7-cp310-cp310-macosx_10_9_x86_64.whl (2.9 MB)
    [2K     [90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m2.9/2.9 MB[0m [31m4.0 MB/s[0m eta [36m0:00:00[0m00:01[0m00:01[0m
    [?25hRequirement already satisfied: PyYAML<6.1,>=5.0.0 in /Library/anaconda3/lib/python3.10/site-packages (from ydata-profiling->pandas-profiling) (6.0)
    Requirement already satisfied: statsmodels<0.14,>=0.13.2 in /Library/anaconda3/lib/python3.10/site-packages (from ydata-profiling->pandas-profiling) (0.13.5)
    Requirement already satisfied: pandas!=1.4.0,<1.6,>1.1 in /Library/anaconda3/lib/python3.10/site-packages (from ydata-profiling->pandas-profiling) (1.5.3)
    Collecting scipy<1.10,>=1.4.1
      Downloading scipy-1.9.3-cp310-cp310-macosx_10_9_x86_64.whl (34.3 MB)
    [2K     [90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m34.3/34.3 MB[0m [31m8.8 MB/s[0m eta [36m0:00:00[0m00:01[0mm0:01[0mm
    [?25hCollecting matplotlib<3.7,>=3.2
      Downloading matplotlib-3.6.3-cp310-cp310-macosx_10_12_x86_64.whl (7.3 MB)
    [2K     [90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m7.3/7.3 MB[0m [31m2.6 MB/s[0m eta [36m0:00:00[0m00:01[0m00:01[0mm
    [?25hCollecting multimethod<1.10,>=1.4
      Downloading multimethod-1.9.1-py3-none-any.whl (10 kB)
    Collecting imagehash==4.3.1
      Downloading ImageHash-4.3.1-py2.py3-none-any.whl (296 kB)
    [2K     [90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m296.5/296.5 kB[0m [31m6.5 MB/s[0m eta [36m0:00:00[0ma [36m0:00:01[0m
    [?25hCollecting phik<0.13,>=0.11.1
      Downloading phik-0.12.3-cp310-cp310-macosx_10_13_x86_64.whl (652 kB)
    [2K     [90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m652.9/652.9 kB[0m [31m6.7 MB/s[0m eta [36m0:00:00[0ma [36m0:00:01[0m
    [?25hRequirement already satisfied: pillow in /Library/anaconda3/lib/python3.10/site-packages (from imagehash==4.3.1->ydata-profiling->pandas-profiling) (9.4.0)
    Requirement already satisfied: PyWavelets in /Library/anaconda3/lib/python3.10/site-packages (from imagehash==4.3.1->ydata-profiling->pandas-profiling) (1.4.1)
    Requirement already satisfied: attrs>=19.3.0 in /Library/anaconda3/lib/python3.10/site-packages (from visions[type_image_path]==0.7.5->ydata-profiling->pandas-profiling) (22.1.0)
    Collecting tangled-up-in-unicode>=0.0.4
      Downloading tangled_up_in_unicode-0.2.0-py3-none-any.whl (4.7 MB)
    [2K     [90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m4.7/4.7 MB[0m [31m8.5 MB/s[0m eta [36m0:00:00[0ma [36m0:00:01[0m
    [?25hRequirement already satisfied: networkx>=2.4 in /Library/anaconda3/lib/python3.10/site-packages (from visions[type_image_path]==0.7.5->ydata-profiling->pandas-profiling) (2.8.4)
    Requirement already satisfied: MarkupSafe>=2.0 in /Library/anaconda3/lib/python3.10/site-packages (from jinja2<3.2,>=2.11.1->ydata-profiling->pandas-profiling) (2.1.1)
    Requirement already satisfied: packaging>=20.0 in /Library/anaconda3/lib/python3.10/site-packages (from matplotlib<3.7,>=3.2->ydata-profiling->pandas-profiling) (22.0)
    Requirement already satisfied: python-dateutil>=2.7 in /Library/anaconda3/lib/python3.10/site-packages (from matplotlib<3.7,>=3.2->ydata-profiling->pandas-profiling) (2.8.2)
    Requirement already satisfied: pyparsing>=2.2.1 in /Library/anaconda3/lib/python3.10/site-packages (from matplotlib<3.7,>=3.2->ydata-profiling->pandas-profiling) (3.0.9)
    Requirement already satisfied: contourpy>=1.0.1 in /Library/anaconda3/lib/python3.10/site-packages (from matplotlib<3.7,>=3.2->ydata-profiling->pandas-profiling) (1.0.5)
    Requirement already satisfied: kiwisolver>=1.0.1 in /Library/anaconda3/lib/python3.10/site-packages (from matplotlib<3.7,>=3.2->ydata-profiling->pandas-profiling) (1.4.4)
    Requirement already satisfied: fonttools>=4.22.0 in /Library/anaconda3/lib/python3.10/site-packages (from matplotlib<3.7,>=3.2->ydata-profiling->pandas-profiling) (4.25.0)
    Requirement already satisfied: cycler>=0.10 in /Library/anaconda3/lib/python3.10/site-packages (from matplotlib<3.7,>=3.2->ydata-profiling->pandas-profiling) (0.11.0)
    Requirement already satisfied: pytz>=2020.1 in /Library/anaconda3/lib/python3.10/site-packages (from pandas!=1.4.0,<1.6,>1.1->ydata-profiling->pandas-profiling) (2022.7)
    Requirement already satisfied: joblib>=0.14.1 in /Library/anaconda3/lib/python3.10/site-packages (from phik<0.13,>=0.11.1->ydata-profiling->pandas-profiling) (1.1.1)
    Requirement already satisfied: typing-extensions>=4.2.0 in /Library/anaconda3/lib/python3.10/site-packages (from pydantic<1.11,>=1.8.1->ydata-profiling->pandas-profiling) (4.4.0)
    Requirement already satisfied: urllib3<1.27,>=1.21.1 in /Library/anaconda3/lib/python3.10/site-packages (from requests<2.29,>=2.24.0->ydata-profiling->pandas-profiling) (1.26.14)
    Requirement already satisfied: charset-normalizer<3,>=2 in /Library/anaconda3/lib/python3.10/site-packages (from requests<2.29,>=2.24.0->ydata-profiling->pandas-profiling) (2.0.4)
    Requirement already satisfied: idna<4,>=2.5 in /Library/anaconda3/lib/python3.10/site-packages (from requests<2.29,>=2.24.0->ydata-profiling->pandas-profiling) (3.4)
    Requirement already satisfied: certifi>=2017.4.17 in /Library/anaconda3/lib/python3.10/site-packages (from requests<2.29,>=2.24.0->ydata-profiling->pandas-profiling) (2022.12.7)
    Requirement already satisfied: patsy>=0.5.2 in /Library/anaconda3/lib/python3.10/site-packages (from statsmodels<0.14,>=0.13.2->ydata-profiling->pandas-profiling) (0.5.3)
    Requirement already satisfied: six in /Library/anaconda3/lib/python3.10/site-packages (from patsy>=0.5.2->statsmodels<0.14,>=0.13.2->ydata-profiling->pandas-profiling) (1.16.0)
    Building wheels for collected packages: htmlmin
      Building wheel for htmlmin (setup.py) ... [?25ldone
    [?25h  Created wheel for htmlmin: filename=htmlmin-0.1.12-py3-none-any.whl size=27081 sha256=7dd927b7316cacbeab64b0eed9fa9f83046ec0a06617bd94140a43459bad3c09
      Stored in directory: /Users/abhinavpratap/Library/Caches/pip/wheels/ea/1c/a8/5cec3479cd45136a7111e2d96aac299b219b199c411665250b
    Successfully built htmlmin
    Installing collected packages: htmlmin, typeguard, tangled-up-in-unicode, scipy, pydantic, multimethod, matplotlib, imagehash, visions, phik, ydata-profiling, pandas-profiling
      Attempting uninstall: scipy
        Found existing installation: scipy 1.10.0
        Uninstalling scipy-1.10.0:
          Successfully uninstalled scipy-1.10.0
      Attempting uninstall: matplotlib
        Found existing installation: matplotlib 3.7.0
        Uninstalling matplotlib-3.7.0:
          Successfully uninstalled matplotlib-3.7.0
    [31mERROR: pip's dependency resolver does not currently take into account all the packages that are installed. This behaviour is the source of the following dependency conflicts.
    gensim 4.3.0 requires FuzzyTM>=0.4.0, which is not installed.[0m[31m
    [0mSuccessfully installed htmlmin-0.1.12 imagehash-4.3.1 matplotlib-3.6.3 multimethod-1.9.1 pandas-profiling-3.6.6 phik-0.12.3 pydantic-1.10.7 scipy-1.9.3 tangled-up-in-unicode-0.2.0 typeguard-2.13.3 visions-0.7.5 ydata-profiling-4.1.2


## Usage

Pandas Profiling can be used to generate reports on any pandas dataframe. To generate a report, simply import the library and call the profile_report() function, passing in the dataframe as a parameter:


```python
import pandas as pd
import pandas_profiling as pp
```


```python
df = pd.read_csv('train.csv')
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
      <th>PassengerId</th>
      <th>Survived</th>
      <th>Pclass</th>
      <th>Name</th>
      <th>Sex</th>
      <th>Age</th>
      <th>SibSp</th>
      <th>Parch</th>
      <th>Ticket</th>
      <th>Fare</th>
      <th>Cabin</th>
      <th>Embarked</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>Braund, Mr. Owen Harris</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>A/5 21171</td>
      <td>7.2500</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>Cumings, Mrs. John Bradley (Florence Briggs Th...</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>PC 17599</td>
      <td>71.2833</td>
      <td>C85</td>
      <td>C</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>1</td>
      <td>3</td>
      <td>Heikkinen, Miss. Laina</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>STON/O2. 3101282</td>
      <td>7.9250</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>1</td>
      <td>1</td>
      <td>Futrelle, Mrs. Jacques Heath (Lily May Peel)</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>113803</td>
      <td>53.1000</td>
      <td>C123</td>
      <td>S</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>0</td>
      <td>3</td>
      <td>Allen, Mr. William Henry</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>373450</td>
      <td>8.0500</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Generate a profile report
report = pp.ProfileReport(df)
```


```python
# Save the report as an HTML file
report.to_file('report.html')
```


    Summarize dataset:   0%|          | 0/5 [00:00<?, ?it/s]



    Generate report structure:   0%|          | 0/1 [00:00<?, ?it/s]



    Render HTML:   0%|          | 0/1 [00:00<?, ?it/s]



    Export report to file:   0%|          | 0/1 [00:00<?, ?it/s]


## Features

The Pandas Profiling report includes the following sections: <br>

### • Overview:
This section provides general information about the dataset, such as the number of rows and columns, memory usage, and the number of missing values. <br>
### • Variables:
This section provides detailed information on each variable in the dataset, including descriptive statistics, distribution of values, and correlation analysis. <br>
### • Interactions:
This section provides an analysis of the relationships between variables, including correlation analysis, scatter plots, and heat maps. <br>
Missing Values: This section provides an overview of the missing values in the dataset, including a heatmap and a summary of the percentage of missing values per variable. <br>
### • Sample:
This section provides a sample of the dataset, allowing you to see a preview of the data. <br>
### • Warnings: 
This section provides a list of potential issues or anomalies in the data, such as highly correlated variables or variables with a high percentage of missing values.

## Conclusion

Pandas Profiling is a powerful tool for quickly and efficiently performing EDA on large datasets. It provides a comprehensive report that includes detailed information on each variable, interactions between variables, and missing values. The interactive visualizations and customizable options make it easy to identify patterns and relationships in the data.


```python

```
