# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE

Code for DATA 1

Name :S.S.Nithyaa sri
Register Number : 22008434
**Data Cleaning - Data_set.csv**

```

import numpy as np
import pandas as pd
3/18/23, 12:12 AM Ex-01-Data-Cleaning/README.md at main · premalatha-sureshbabu/Ex-01-Data-Cleaning
https://github.com/premalatha-sureshbabu/Ex-01-Data-Cleaning/blob/main/README.md 2/10
OUPUT for DATA 1
Before Cleaning
import seaborn as sbn
df = pd.read_csv("/content/Data_set.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['show_name'] = df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on'] = df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network'] = df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
df['rating'] = df['rating'].fillna(df['rating'].mean())
df['current_overall_rank'] =
df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
df['watchers'] = df['watchers'].fillna(df['watchers'].median())
df.head()
df.info()
df.isnull().sum()

```

# OUPUT for DATA 1
![11](https://user-images.githubusercontent.com/119122478/226107963-4e4fcd06-495c-4a3c-ac67-96ef543f59e3.png)

# before Cleaning

![12](https://user-images.githubusercontent.com/119122478/226108063-23b8fa14-620d-4727-bc02-0c07ba20a343.png)
![image](https://user-images.githubusercontent.com/119122478/226108100-dbec5ada-e1de-4fab-bd1b-b3e4846ab7aa.png)
![14](https://user-images.githubusercontent.com/119122478/226108136-3741d0d1-2603-499c-bf49-281aab378d2a.png)
![15](https://user-images.githubusercontent.com/119122478/226108254-8cf27585-bec7-4a73-8559-dd16ebbb22cd.png)

# Mode

![16](https://user-images.githubusercontent.com/119122478/226108307-9aa8e5c7-e019-4944-b69f-ce744c4832cd.png)

# Mean

![17 1](https://user-images.githubusercontent.com/119122478/226108364-7e76af53-876e-439d-bd65-4bf1bafc1b43.png)

# Median
![18](https://user-images.githubusercontent.com/119122478/226108446-bd540ff9-190e-4a83-b659-0085ff910d51.png)

# After Cleaning
![19](https://user-images.githubusercontent.com/119122478/226108494-c0a8ed21-5502-4514-9f97-cf938f1e70cc.png)
![20 1](https://user-images.githubusercontent.com/119122478/226108543-c3c56b58-18bf-48ca-a863-4638cbaa0325.png)

# Code for DATA 2

Name :S.S.Nithyaasri
Register Number : 22008434

```
import pandas as pd

import numpy as np

import seaborn as sns

df = pd.read_csv("/content/Loan_data.csv")

df
df.head()
df.describe()
df.tail()
df.isnull()
df.isnull().sum()
df.shape
df.columns
df.duplicated
#Using mode method to fill the data in columns as Object(String)
#mode()[0] - Takes the most reccuring value and fills the empty cells
df['Gender'] = df['Gender'].fillna(df['Gender'].mode()[0])
df['Dependents'] = df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Self_Employed'] = df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
#Using mean method to fill the data
df['LoanAmount'] = df['LoanAmount'].fillna(df['LoanAmount'].mean())
df['Loan_Amount_Term'] = df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['Credit_History'] = df['Credit_History'].fillna(df['Credit_History'].mean())
sns.boxplot(y="LoanAmount",data=df)
#Checking the total no.of null values
again
df.isnull().sum()
#Checking info of the dataset to check all the columns have entries
df.info()
```

# Output for DATA 2

![21](https://user-images.githubusercontent.com/119122478/226108693-f44c119e-4ff4-42ba-871b-a5b5740f54e4.png)
![22](https://user-images.githubusercontent.com/119122478/226108783-f356828b-5276-4925-8a37-aea01107edbe.png)

# Before cleaning

![23](https://user-images.githubusercontent.com/119122478/226108819-207b9381-966f-4164-8f7b-8fb9ef4256e4.png)
![24](https://user-images.githubusercontent.com/119122478/226108888-c350f401-cc5a-41bf-bae3-9797a72f0c63.png)
![25](https://user-images.githubusercontent.com/119122478/226108933-551f27c7-3782-443c-bd96-5d01338d66d6.png)
![26](https://user-images.githubusercontent.com/119122478/226108974-404a9de6-1f0a-4f53-b43d-3d0e257ea65f.png)
![27](https://user-images.githubusercontent.com/119122478/226109013-fad08956-cdfa-4b2d-8560-6238f9ddd60d.png)
![28](https://user-images.githubusercontent.com/119122478/226109065-8cbed5df-bcfd-4c14-b076-1a1adb8e9079.png)

# Mode
![29 1](https://user-images.githubusercontent.com/119122478/226109151-a04ddc0d-9360-449a-8b52-060aecb0bd48.png)

# Mean
![29 2](https://user-images.githubusercontent.com/119122478/226109196-48080397-985c-41e2-985d-976231546e09.png)

# Median
![29 3](https://user-images.githubusercontent.com/119122478/226109229-011f32ed-3e7f-490b-91e5-348856e33d4f.png)

# After cleaning
![29 4](https://user-images.githubusercontent.com/119122478/226109318-3abf96c0-7238-450d-b76a-c8d32d27f93d.png)

# RESULT
Thus the given data is read,cleansed and cleaned data is saved into the file.
