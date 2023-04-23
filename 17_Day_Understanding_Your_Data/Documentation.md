# Day 16: Understanding Your Data

When working with a dataset, it is important to understand the data thoroughly before diving into analysis. Here are some basic questions that you should ask about your data: <br>

1. How big is the data?  <br>
2. How does the data look like? <br>
3. What is the data type of cols? <br>
4. Are there any missing values? <br>
5. How does the data look mathematically? <br>
6. Are there duplicate values? <br>
7. How is the correlation between cols? <br>

To answer these questions, you can use various pandas functions. Let's see how to use them:


```python
import pandas as pd
```

## 1. How big is the data?

This question will help you understand the number of observations and features in the dataset.


```python
df = pd.read_csv('my_dataset.csv')
print(df.shape)
```

    (891, 12)


## 2. How does the data look like?
This question will help you understand what the dataset looks like and what kind of values are present in it.


```python
df = pd.read_csv('my_dataset.csv')
print(df.sample(5))
```

         PassengerId  Survived  Pclass                             Name     Sex  \
    475          476         0       1      Clifford, Mr. George Quincy    male   
    869          870         1       3  Johnson, Master. Harold Theodor    male   
    692          693         1       3                     Lam, Mr. Ali    male   
    866          867         1       2     Duran y More, Miss. Asuncion  female   
    214          215         0       3              Kiernan, Mr. Philip    male   
    
          Age  SibSp  Parch         Ticket     Fare Cabin Embarked  
    475   NaN      0      0         110465  52.0000   A14        S  
    869   4.0      1      1         347742  11.1333   NaN        S  
    692   NaN      0      0           1601  56.4958   NaN        S  
    866  27.0      1      0  SC/PARIS 2149  13.8583   NaN        C  
    214   NaN      1      0         367229   7.7500   NaN        Q  


## 3. What is the data type of cols?
This question will help you understand the data types of each feature in the dataset.


```python
df = pd.read_csv('my_dataset.csv')
print(df.info())
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 891 entries, 0 to 890
    Data columns (total 12 columns):
     #   Column       Non-Null Count  Dtype  
    ---  ------       --------------  -----  
     0   PassengerId  891 non-null    int64  
     1   Survived     891 non-null    int64  
     2   Pclass       891 non-null    int64  
     3   Name         891 non-null    object 
     4   Sex          891 non-null    object 
     5   Age          714 non-null    float64
     6   SibSp        891 non-null    int64  
     7   Parch        891 non-null    int64  
     8   Ticket       891 non-null    object 
     9   Fare         891 non-null    float64
     10  Cabin        204 non-null    object 
     11  Embarked     889 non-null    object 
    dtypes: float64(2), int64(5), object(5)
    memory usage: 83.7+ KB
    None


## 4. Are there any missing values? 
This question will help you understand if there are any missing values in the dataset that need to be handled.


```python
df = pd.read_csv('my_dataset.csv')
print(df.isnull().sum())
```

    PassengerId      0
    Survived         0
    Pclass           0
    Name             0
    Sex              0
    Age            177
    SibSp            0
    Parch            0
    Ticket           0
    Fare             0
    Cabin          687
    Embarked         2
    dtype: int64


## 5. How does the data look mathematically? 
This question will help you understand the basic statistics of the dataset such as mean, median, and standard deviation.


```python
df = pd.read_csv('my_dataset.csv')
print(df.describe())
```

           PassengerId    Survived      Pclass         Age       SibSp  \
    count   891.000000  891.000000  891.000000  714.000000  891.000000   
    mean    446.000000    0.383838    2.308642   29.699118    0.523008   
    std     257.353842    0.486592    0.836071   14.526497    1.102743   
    min       1.000000    0.000000    1.000000    0.420000    0.000000   
    25%     223.500000    0.000000    2.000000   20.125000    0.000000   
    50%     446.000000    0.000000    3.000000   28.000000    0.000000   
    75%     668.500000    1.000000    3.000000   38.000000    1.000000   
    max     891.000000    1.000000    3.000000   80.000000    8.000000   
    
                Parch        Fare  
    count  891.000000  891.000000  
    mean     0.381594   32.204208  
    std      0.806057   49.693429  
    min      0.000000    0.000000  
    25%      0.000000    7.910400  
    50%      0.000000   14.454200  
    75%      0.000000   31.000000  
    max      6.000000  512.329200  


## 6. Are there duplicate values? 
This question will help you understand if there are any duplicate observations in the dataset that need to be removed.


```python
df = pd.read_csv('my_dataset.csv')
print(df.duplicated().sum())
```

    0


## 7. How is the correlation between cols? 
This question will help you understand the relationship between the different features in the dataset and if there are any strong correlations between them.


```python
df = pd.read_csv('my_dataset.csv')
print(df.corr())
```

                 PassengerId  Survived    Pclass       Age     SibSp     Parch  \
    PassengerId     1.000000 -0.005007 -0.035144  0.036847 -0.057527 -0.001652   
    Survived       -0.005007  1.000000 -0.338481 -0.077221 -0.035322  0.081629   
    Pclass         -0.035144 -0.338481  1.000000 -0.369226  0.083081  0.018443   
    Age             0.036847 -0.077221 -0.369226  1.000000 -0.308247 -0.189119   
    SibSp          -0.057527 -0.035322  0.083081 -0.308247  1.000000  0.414838   
    Parch          -0.001652  0.081629  0.018443 -0.189119  0.414838  1.000000   
    Fare            0.012658  0.257307 -0.549500  0.096067  0.159651  0.216225   
    
                     Fare  
    PassengerId  0.012658  
    Survived     0.257307  
    Pclass      -0.549500  
    Age          0.096067  
    SibSp        0.159651  
    Parch        0.216225  
    Fare         1.000000  


    /var/folders/s1/prjs0rvs11x47frsjkk0xwyc0000gn/T/ipykernel_3450/3312821703.py:2: FutureWarning: The default value of numeric_only in DataFrame.corr is deprecated. In a future version, it will default to False. Select only valid columns or specify the value of numeric_only to silence this warning.
      print(df.corr())


#### By answering these basic questions, you can get a good understanding of your dataset and proceed with your analysis with confidence.


```python

```
