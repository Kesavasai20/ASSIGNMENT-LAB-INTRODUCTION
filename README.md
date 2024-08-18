# ASSIGNMENT-LAB-INTRODUCTION
### Prepared By : K KESAVA SAI
### Register Number : 212223230105
### DEPT : AIDS 2nd YEAR
### Requirements :
Python 3.x

Pandas library

### Data :
The data used for this assignment is from bank_train.csv, which includes various columns related to client information and their interactions with the bank.

### CODE :
### ACTIVITY 1 :
## Task 1. Write a Python program to select the 'name' and 'score' columns from the following DataFrame.
```
import pandas as pd
import numpy as np

exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
    'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
    'attempts': [1, 3, 4, 3, 5, 3, 6, 1, 7, 1]
}

df = pd.DataFrame(exam_data)

selected_columns = df[['name', 'score']]
print(selected_columns)
```
### Output:
![image](https://github.com/user-attachments/assets/e9380517-a82f-4125-9c34-db0da47d8901)


## Task 2: Selecting the data where attempts are greater than 3.
```
filtered_data = df[df['attempts'] > 3]
print(filtered_data)
```
### Output:
![image](https://github.com/user-attachments/assets/50c90f80-ad6b-4853-ba50-3cb2718e2b94)

## Task 3: Indexing rows and columns based on conditions.
```
data = {
    'name': ['Alice', 'Bob', 'Charlie', 'Dave'],
    'age': [25, 35, 40, 28],
    'gender': ['F', 'M', 'M', 'M'],
    'salary': [50000, 70000, 60000, 80000]
}

df = pd.DataFrame(data)
```
# a. Select rows where age is greater than 30:
```
age_filtered = df[df['age'] > 30]
print("Rows where age is greater than 30:\n", age_filtered)
```
### Output:
![image](https://github.com/user-attachments/assets/f3260b4e-1326-441d-b948-883411445728)

# b. Select rows where name contains 'e':
```
name_filtered = df[df['name'].str.contains('e')]
print("Rows where name contains 'e':\n", name_filtered)
```
### Output:
![image](https://github.com/user-attachments/assets/50c09317-37b8-46e8-bd1b-549de8028897)

# c. Select rows where gender is 'M' and salary is greater than 65000:
```
gender_salary_filtered = df[(df['gender'] == 'M') & (df['salary'] > 65000)]
print("Rows where gender is 'M' and salary is greater than 65000:\n", gender_salary_filtered)
```
### Output:
![image](https://github.com/user-attachments/assets/745382cc-0d38-487b-8153-ce1180e4e476)

# d. Select columns 'name' and 'age'
```
name_age = df[['name', 'age']]
print("Columns 'name' and 'age':\n", name_age)
```
### Output:
![image](https://github.com/user-attachments/assets/bfc810d7-ba97-40fe-8adb-b3e3b1f314a7)

# **ACTIVITY 2 :**
This section covers the tasks in Activity 2, which involve filtering and selecting specific rows and columns from the bank_train.csv dataset.
import pandas as pd

### Task a
## Condition: 
Select the rows where clients with primary education have subscribed to a deposit.
```
primary_education_subscribed = df_bank.loc[(df_bank['education'] == 'primary') & (df_bank['deposit'] == 'yes')]
print(primary_education_subscribed)
```
### Output:
![image](https://github.com/user-attachments/assets/5192346c-2cc3-4d61-ab73-8c5dc475e937)

## Task b: Select the rows where clients have not subscribed to a deposit
## Condition: 
Select the rows where clients have not subscribed to a deposit.
```
not_subscribed = df_bank.loc[df_bank['deposit'] == 'no']
print(not_subscribed)
```
### Output:
![image](https://github.com/user-attachments/assets/d8a67745-ae4b-4149-a0b8-7f967a567a83)

## Task c: Select the rows where clients who have subscribed to a deposit either have a housing or a personal loan
## Condition: 
Select the rows where clients who have subscribed to a deposit either have a housing or a personal loan.
```
subscribed_with_loans = df_bank.loc[(df_bank['deposit'] == 'yes') & ((df_bank['housing'] == 'yes') | (df_bank['loan'] == 'yes'))]
print(subscribed_with_loans)
```
### Output:
![image](https://github.com/user-attachments/assets/7c9a65c7-1a8e-49b9-8c28-ccf511ad0963)

## Task d: Select the rows where clients with secondary education who have not subscribed to a deposit
## Condition: 
Select the rows where clients with secondary education who have not subscribed to a deposit.
````
secondary_not_subscribed = df_bank.loc[(df_bank['education'] == 'secondary') & (df_bank['deposit'] == 'no')]
print(secondary_not_subscribed)
````
### Output:
![image](https://github.com/user-attachments/assets/f1fd7f89-c9bc-4406-84ce-f892d4e6bb7d)

## Task e: Select the rows where clients who have subscribed to a term deposit as an outcome of the successful marketing campaign
## Condition: 
Select the rows where clients who have subscribed to a term deposit as an outcome of the successful marketing campaign.
```
subscribed_success = df_bank.loc[(df_bank['deposit'] == 'yes') & (df_bank['poutcome'] == 'success')]
print(subscribed_success)
```
### Output:
![image](https://github.com/user-attachments/assets/fbc5c64b-31eb-41b9-860a-3c95307e8d6b)

## Task f: Select the rows where unemployed clients have not subscribed to deposit
## Condition: 
Select the rows where unemployed clients have not subscribed to a deposit.
```
unemployed_not_subscribed = df_bank.loc[(df_bank['job'] == 'unemployed') & (df_bank['deposit'] == 'no')]
print(unemployed_not_subscribed)
```
### Output:
![image](https://github.com/user-attachments/assets/28060a01-3eae-462d-9ed7-bf8f6852c39b)

## Task g: Select columns 'name' and 'salary' where age is less than or equal to 30
## Condition: 
Select columns 'name' and 'salary' where age is less than or equal to 30. (Note: Adjust 'name' and 'salary' to the actual column names.)
```
young_clients = df_bank.loc[df_bank['age'] <= 30, ['job', 'balance']]
print(young_clients)
```
### Output:
![image](https://github.com/user-attachments/assets/dd02d911-fba6-4581-8914-0ebee3be42f9)

### Results
The results above demonstrate how to filter and select data using Pandas' loc method based on specific conditions. This can be useful in analyzing marketing data and understanding client behavior.


