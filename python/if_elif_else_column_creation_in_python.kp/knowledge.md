---
title: Generating a fresh column by utilizing if-elif-else stipulation
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To create a new column based on if-elif-else condition in Python, use the .apply() method along with a lambda function that specifies the conditions and outputs the desired results.
---

**Contents**

[TOC]

## Introduction
Creating a new column based on if-elif-else condition is a common task in data analysis using Python. In this guide, we will discuss how to create a new column based on if-elif-else condition using pandas library.

## Installing Pandas
Before we dive into creating a new column based on if-elif-else condition, we need to make sure we have pandas library installed in our system. If you don't have pandas installed, you can install it by running the following command in your terminal.

```bash
pip install pandas
```

## Creating a new column based on if-elif-else condition
To create a new column based on if-elif-else condition, we need to use the apply function of pandas. The apply function allows us to apply a function to each row or column of a pandas data frame.

Here is an example code snippet of creating a new column based on if-elif-else condition.

```python
import pandas as pd

# Creating a panda data frame
data = {'Name': ['John', 'Mike', 'Sarah', 'Mary'],
        'Age': [25, 33, 28, 21]}

df = pd.DataFrame(data)

# Creating a new column based on if-elif-else condition
df['Gender'] = df.apply(lambda row: 'Male' if row.Age > 30 else 'Female', axis=1)

print(df)
```

In the above code snippet, we have created a panda data frame with two columns 'Name' and 'Age'. We have used the apply function with a lambda function to create a new column 'Gender' based on if-elif-else condition. The lambda function checks if the age of each row is greater than 30, if it is, then it sets the gender to Male, else it sets the gender to Female.

## Conclusion
In this guide, we have learned how to create a new column based on if-elif-else condition using pandas library in Python. The apply function was used to apply a lambda function to each row of a pandas data frame, which allowed us to create a new column based on the if-elif-else condition.
