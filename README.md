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
```
Name :S.S.Nithyaa sri
Register Number : 22008434
**Data Cleaning - Data_set.csv**
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

# OUPUT for data 1
![11](https://user-images.githubusercontent.com/119122478/226107963-4e4fcd06-495c-4a3c-ac67-96ef543f59e3.png)

# After Cleaning

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




