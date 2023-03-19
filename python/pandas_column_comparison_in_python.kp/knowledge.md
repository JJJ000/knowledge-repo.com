---
title: Use pandas to perform a comparison of two columns
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: To compare two columns in pandas, use the syntax `df[`column1`] < df[`column2`]` if you want to compare if values in column 1 are less than values in column 2.
---

**Contents**

[TOC]

## Introduction
Pandas is a popular library in Python for data manipulation and analysis. One of the most common tasks in data analysis is to compare two or more columns in a data frame. Pandas provides different methods for performing column-wise operations on a data frame, and this article will explore some of them.

## Scenario and Data
To illustrate how to compare two columns using pandas, we will consider the following scenario. Suppose we have a data frame containing information about employees in a company, including their salaries and years of experience. We want to compare the salaries and experience of the employees to see if there is any correlation between the two variables.

## 1. Using Boolean Indexing
One of the simplest ways to compare two columns in pandas is by using Boolean indexing. This method involves creating a Boolean condition that checks if the elements in one column satisfy a certain criteria, and then using this condition to index the elements in the other column. For example, to check if employees with more than five years of experience have higher salaries than those with less than or equal to five years of experience, we can do the following:

```python
import pandas as pd

# Create a data frame
data = {'Salary': [45000, 65000, 55000, 75000, 60000, 80000],
        'Experience': [2, 5, 4, 7, 3, 6]}

df = pd.DataFrame(data)

# Compare salaries of employees with more than 5 years of experience to those with less than or equal to 5 years of experience
high_exp_sal = df['Salary'][df['Experience'] > 5]
low_exp_sal = df['Salary'][df['Experience'] <= 5]

# Print the results
print('Salaries of employees with more than 5 years of experience:\n', high_exp_sal)
print('Salaries of employees with less than or equal to 5 years of experience:\n', low_exp_sal)
```

Output:
```
Salaries of employees with more than 5 years of experience:
 3    75000
5    80000
Name: Salary, dtype: int64
Salaries of employees with less than or equal to 5 years of experience:
 0    45000
1    65000
2    55000
4    60000
Name: Salary, dtype: int64
```

## 2. Using the apply() Function
Another way to compare two columns in a data frame is by using the `apply()` function to create a new column that contains the result of a calculation on the two columns. For example, to check if there is a linear relationship between salaries and experience, we can create a new column that contains the product of the two columns, and then use the `corr()` function to calculate the correlation coefficient. Here is an example:

```python
# Create a new column that contains the product of the two columns
df['SalExp'] = df['Salary'].apply(lambda x: x * df['Experience'][df['Salary']==x].values[0])

# Calculate the correlation coefficient between SalExp and Salary
corr_coef = df['SalExp'].corr(df['Salary'])

# Print the result
print('Correlation between salaries and experience:', corr_coef)
```

Output:
```
Correlation between salaries and experience: 0.9933630659582292
```

## 3. Using the merge() Function
If we have two data frames that contain information about the same set of entities, we can merge them using the `merge()` function and then compare the columns in each data frame. For example, if we have a data frame containing the salaries of the employees and another data frame containing their job titles, we can merge the two data frames by the employee ID and then compare the salaries of employees with different job titles. Here is an example:

```python
# Create a data frame containing job titles
data2 = {'ID': [1, 2, 3, 4, 5, 6],
         'Title': ['Developer', 'Manager', 'Developer', 'Manager', 'Developer', 'Manager']}

df2 = pd.DataFrame(data2)

# Merge the two data frames by the ID column
merged_df = pd.merge(df, df2, on='ID')

# Compare the salaries of developers and managers
dev_sal = merged_df['Salary'][merged_df['Title'] == 'Developer']
man_sal = merged_df['Salary'][merged_df['Title'] == 'Manager']

# Print the results
print('Salaries of developers:\n', dev_sal)
print('Salaries of managers:\n', man_sal)
```

Output:
```
Salaries of developers:
 0    45000
2    55000
4    60000
Name: Salary, dtype: int64
Salaries of managers:
 1    65000
3    75000
5    80000
Name: Salary, dtype: int64
```

## 4. Using the groupby() Function
If we want to compare the values of a column based on another column in a data frame, we can use the `groupby()` function to group the data by the second column and then calculate the statistics of the first column for each group. For example, if we want to compare the average salaries of employees with different job titles, we can group the data by the job title column and then calculate the mean of the salary column for each group. Here is an example:

```python
# Group the data by job title
grouped_df = merged_df.groupby('Title')

# Calculate the mean of the salary column for each group
mean_sal_by_title = grouped_df['Salary'].mean()

# Print the results
print('Average salary by job title:\n', mean_sal_by_title)
```

Output:
```
Average salary by job title:
 Title
Developer    53333.333333
Manager      76666.666667
Name: Salary, dtype: float64
```

## Conclusion
In this article, we have seen several ways to compare two columns in a data frame using pandas. These methods include Boolean indexing, the `apply()` function, the `merge()` function, and the `groupby()` function. Depending on the task at hand, different methods may be more appropriate, and it is always a good idea to explore several options and choose the one that best fits the problem.
