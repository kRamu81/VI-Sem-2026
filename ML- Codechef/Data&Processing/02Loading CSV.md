Loading CSV - Worked Example
We have a dataset of students stored in a CSV file (students.csv). Each row represents one student, and the dataset contains:

Age → student’s age
Salary → part-time salary in INR
Hours_Studied → number of hours studied per day
Passed → whether the student passed the exam (Yes or No)
Our task is to load this dataset into Python using Pandas and take a quick look at it.
```python
# Step 1: Import pandas
import pandas as pd

# Step 2: Load the dataset (make sure students.csv is in the same folder as this script)
df = pd.read_csv("students.csv")

# Step 3: View the first few rows
print("First 5 rows of the dataset:")
print(df.head())

# Step 4: Separate features and label
features = df[["Age", "Salary", "Hours_Studied"]]
label = df["Passed"]

print("\nFeatures (X):")
print(features.head())

print("\nLabel (y):")
print(label.head())
```

Output:
```
First 5 rows of the dataset:
   Age  Salary  Hours_Studied Passed
0   20   30000              5    Yes
1   22   25000              2     No
2   19   40000              6    Yes
3   21   35000              1     No
4   23   28000              4    Yes

Features (X):
   Age  Salary  Hours_Studied
0   20   30000              5
1   22   25000              2
2   19   40000              6
3   21   35000              1
4   23   28000              4

Label (y):
0    Yes
1     No
2    Yes
3     No
4    Yes
Name: Passed, dtype: object```
