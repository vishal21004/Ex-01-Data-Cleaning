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
```
/* 
Name : M.A.Vishal
Register Number : 212222230177
**Data Cleaning - Data_set.csv**
import numpy as np
import pandas as pd
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
df['current_overall_rank'] = df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
df['watchers'] = df['watchers'].fillna(df['watchers'].median())
df.head()
df.info()
df.isnull().sum()

**Data Cleannig - Loan_data.csv**
data = pd.read_csv("/content/Loan_data.csv")
print(data)
data.head(5)
data.isnull()
data.isnull().sum()
data['Gender'] = data["Gender"].fillna(data['Gender'].mode()[0])
data['Dependents'] = data["Dependents"].fillna(data['Dependents'].mode()[0])
data['Self_Employed'] = data["Self_Employed"].fillna(data['Self_Employed'].mode()[0])
data['Credit_History'] = data["Credit_History"].fillna(data['Credit_History'].mode()[0])
data.head()
data['LoanAmount']=data['LoanAmount'].fillna(data['LoanAmount'].median())
data.head()
data['Loan_Amount_Term']=data['Loan_Amount_Term'].fillna(data['Loan_Amount_Term'].mean())
data.head()
data.info()
data.isnull().sum()
*/
```
# OUPUT
## Data Cleaning - Data_set.csv
![data set 1](https://user-images.githubusercontent.com/127843647/227855015-cee6a94f-187b-41e5-9b67-4fbb655d58e7.jpeg)

## Before Cleaning

![data set 2](https://user-images.githubusercontent.com/127843647/227855058-9f0e9586-0d54-4ef0-8ecf-fd39a281cdf6.jpeg)
![data set3](https://user-images.githubusercontent.com/127843647/227855154-35e5ae04-41dc-4181-a5e2-04f57cd0487d.jpeg)
![data set 4](https://user-images.githubusercontent.com/127843647/227855186-797e5ccd-dd74-4a62-815f-69b17ecc1916.jpeg)

## Mode

![data set mode](https://user-images.githubusercontent.com/127843647/227855718-72d2e18e-ccef-4627-b8c7-b8338caba6de.jpeg)

## Mean
![data set mean](https://user-images.githubusercontent.com/127843647/227855754-09f13a21-ed5b-4f47-99d3-bc56ba44e414.jpeg)


## Median
![data  set median](https://user-images.githubusercontent.com/127843647/227855776-53ef4188-5c09-41b3-a9c5-d24c3d268803.jpeg)

## After Cleaning
![data set after cleaning](https://user-images.githubusercontent.com/127843647/227855806-abf49fa6-2141-49bf-b9c5-d8c5b742dcef.jpeg)


## Data Cleaning - Loan_data.csv
![loan data 1](https://user-images.githubusercontent.com/127843647/227855851-7a07603e-93bd-45f6-ae23-09ed6895918f.jpeg)


## Before Cleaning
![loan data 2](https://user-images.githubusercontent.com/127843647/227855939-d3e30ab5-27f3-459a-88be-366789bbcb39.jpeg)
![loan data 3](https://user-images.githubusercontent.com/127843647/227855976-1936afba-d65a-4239-bec8-f7526d138a5d.jpeg)
![loan data 4](https://user-images.githubusercontent.com/127843647/227855995-ab951c62-72ea-44ea-afc7-f3eb062d6b26.jpeg)

## Mode
![loan data mode](https://user-images.githubusercontent.com/127843647/227856030-f32b965e-2073-4cf2-bd12-8198fb9c4eb9.jpeg)


## Mean

![loan data mean ](https://user-images.githubusercontent.com/127843647/227856052-383a12e4-62dc-4425-8831-a032e488c04c.jpeg)

## Median

![loan data median](https://user-images.githubusercontent.com/127843647/227856080-7d73d6db-4860-41ae-b074-04da648708b1.jpeg)

## After Cleaning

![loan data 6](https://user-images.githubusercontent.com/127843647/227856225-2fcddba3-edcd-43fb-8de6-216cb21430a0.jpeg)
 
# RESULT
Thus the given data is read, cleansed and the cleaned data is saved into the file.


